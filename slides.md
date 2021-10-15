---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
highlighter: shiki
lineNumbers: true
drawings:
    persist: false
    enabled: true
---

# End-to-End Wireframe Parsing

---

# Framework

<img src="/public/image-20211014152118935.png" alt="image-20211014152118935" style="zoom: 50%;" />

<style>
img{
  display: block;
  margin: 0 auto;
}
</style>

---

# Feature extraction backbone

1. Extract semantically meaningful features for the successive modules. 
2. Input images are resized into squares.
3. Using the Stacked Hourglass network.
4. Intermediate supervision was imposed on the output of each hourglass module.
5. The total loss  is the sum of the loss on those modules.

<img src="https://imgconvert.csdnimg.cn/aHR0cHM6Ly9tbWJpei5xcGljLmNuL21tYml6X3BuZy9WQmNEMDJqRmhnbGZkbEZ1WEYyRW1oMzdBQUNnT25uUldvaFkyMVVlZGliYlhlelBMSHVjNWg0M1dONVRsM2ZSUlplZVd6cElYbDJyaWJkTVZnOXhBV25RLzY0MA?x-oss-process=image/format,png" alt="img" style="zoom: 33%;" />

<img src="https://pic3.zhimg.com/v2-202a2358835054794c6356b77ddb7a82_r.jpg" alt="preview" style="zoom:50%;" />

<style>
img{
  display: block;
  margin: 0 auto;
}
</style>

---

# Junction proposal module

1. Dividing the image into $W_b$ × $𝐻_𝑏$ bins. 
2. For each bin, predicting whether there exists a junction inside it and its relative location inside this bin.
3. Outputing a junction likelihood map 𝐽 and an offset map O: 

<img src="/image-20211014160340711.png" alt="image-20211014160340711" style="zoom:40%;" /><img src="/image-20211014160347360.png" alt="image-20211014160347360" style="zoom:40%;" />

### Non-Maximum Suppression
<br/>
<img src="/image-20211014153724802.png" alt="image-20211014153724802" style="zoom:55%;" />

1. N(𝑏) represents the 8 nearby bins around 𝑏. 
2. Suppressing the pixel values that are not the local maxima on the junction map. 
3. It cna be implemented with a max-pooling operator. 
4. The final output is the top 𝐾 junction positions with the highest probabilities in $𝐽'$.

<style>
img{
  display: inline-block;
  margin-left: 50px;
}
</style>

---

# Line Sampling module

Generating a list of line candidates during the training stage, so the line verification network can learn to predict the existence of a line. 

### Static Line Sampler

Static line sampler returns $N_{S+}$ positive samples and $N_{S-}$ negative samples that are directly derived from the ground truth labels.

1. Rasterizing all the ground truth lines onto a 64 × 64 low-resolution bitmap.
2. For each possible connections formed by a pair of ground truth junctions that is not a ground truth line, defining its hardness score to be the average pixel density on the bitmap along this line.
3. $S^−$ is set to be the top 2000 lines with the highest hardness scores.

---

### Dynamic Line Sampler

Sampling the lines using the predicted junctions from the junction proposal module.

Let $𝑚_𝑖:= arg min_𝑗||\widehat{p_𝑖} − p_𝑗||_2$ be the index of the best matching ground truth junction for the 𝑖th junction candidates. If the ℓ2-distance between $\widehat{p_𝑖}$ and $p_{𝑚𝑖}$ is less than the threshold 𝜂, we say that the junction candidate $\widehat{p_𝑖}$ is matched.

<img src="/image-20211014190033865.png" alt="image-20211014190033865" style="zoom:50%;" />

---

<img src="/image-20211014192027368.png" alt="image-20211014192027368" style="zoom:67%;" />

<style>
img{
  display: block;
  margin: 0 auto;
}
</style>

---

#  Line verification module

1. Feeding the coordinates into a LoI pooling layer, which returns a fixed-length feature vector.
2. Passing the feature vector into a network composed of two FC layers and get a logit.

### LoI pooling

1. Computing the coordinates of $𝑁_𝑝$ uniform spaced middle points along the line with linear interpretation.
2. Calculating the feature values at those $𝑁_𝑝$ points in the backbone’s feature map using bilinear interpretation to avoid quantization artifacts.<br/>
   𝐶 × $𝑁_𝑝$（𝐶 is the channel dimension of the feature map from the backbone network）
3. Reducing the size of the feature vector with a 1D max pooling layer.<br/>
   𝐶 × $\lceil\frac{𝑁_𝑝}{s} \rceil$（𝑠 is the size of stride of the max pooling layer）
4. This vector is then flattened and returned as the output of LoI pooling layer.

---

<img src="/image-20211014152118935.png" alt="image-20211014152118935" style="zoom: 50%;" />

<style>
img{
  display: block;
  margin: 0 auto;
}
</style>

---

# Result 

<img src="/image-20211014154138741.png" alt="image-20211014154138741" style="zoom: 58%;" />

<style>
img{
  display: block;
  margin: 0 auto;
}
</style>

---

<img src="/image-20211014192342184.png" alt="image-20211014192342184" style="zoom: 50%;" />

<style>
img{
  display: block;
  margin: 0 auto;
}
</style>

---

<img src="/image-20211014192500573.png" alt="image-20211014192500573" style="zoom:67%;" />

<style>
img{
  display: block;
  margin: 0 auto;
}
</style>
