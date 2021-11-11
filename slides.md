---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
highlighter: shiki
lineNumbers: true
drawings:
    persist: false
    enabled: true
# cover
# fact
# intro
# quote
# section
# statement
---

# Transformer In CV

---
layout: intro
---

# Contents

1. Vit
2. Swin Transformer
3. GG-Transformer

---

# Transformer

<img src="https://github.com/shenduldh/ML_learning/raw/main/NLP/NLP.assets/transformer_resideual_layer_norm_3.png" alt="img" style="zoom: 50%;" />

<style>
img{
  margin: 0 auto;
}
</style>

---
layout: intro
---
# Vit

## An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale

Alexey Dosovitskiy, Lucas Beyer, Alexander Kolesnikov, Dirk Weissenborn, Xiaohua Zhai, Thomas Unterthiner, Mostafa Dehghani, Matthias Minderer, Georg Heigold, Sylvain Gelly, Jakob Uszkoreit, Neil Houlsby 

Google Research, Brain Team

ICLR(2021)

<a target="_blank" href="https://arxiv.org/pdf/2010.11929.pdf">论文链接</a>

---

<img src="slides.assets/image-20211111104513302.png" alt="image-20211111104513302" style="zoom: 50%;" />

* 用 Attention 代替 CNN
* Pre-train on large datasets
* Fine-tune on smaller downstream tasks

<style>
img{
  margin: 0 auto;
}
</style>

---
layout: intro
---

# Swim Transformer

## Swin Transformer: Hierarchical Vision Transformer using Shifted Windows

Ze Liu, Yutong Lin, Yue Cao, Han Hu, Yixuan Wei, Zheng Zhang, Stephen Lin, Baining Guo

Microsoft Research Asia

CoRR(2021)

<a target="_blank" href="https://arxiv.org/pdf/2103.14030.pdf">论文链接</a>

---

<img src="slides.assets/image-20211111105153514.png" alt="image-20211111105153514" style="zoom:80%;" />

* Window Attention
* Hierarchical
* Shifted Windows

<style>
img{
  margin: 0 auto;
  margin-top: 50px;
}
</style>

---

<img src="slides.assets/image-20211111111304155.png" alt="image-20211111111304155" style="zoom: 40%;" />
<br/><br/>
<img src="slides.assets/image-20211111111329850.png" alt="image-20211111111329850" style="zoom: 40%;" />

<style>
img{
  margin: 0 auto;
}
</style>

---


<img src="slides.assets/image-20211111110759961.png" alt="image-20211111110759961" style="zoom:50%;" />
<img src="slides.assets/image-20211111110956981.png" alt="image-20211111110956981" style="zoom:50%;" />


<style>
img{
  margin: 0 auto;
}
</style>

---
layout: intro
---

# GG-Transformer

## Glance-and-Gaze Vision Transformer

Qihang Yu, Yingda Xia, Yutong Bai, Yongyi Lu, Alan Yuille, Wei Shen

The Johns Hopkins University, Shanghai Jiaotong University

NeurIPS(2021)

<a target="_blank" href="https://arxiv.org/pdf/2106.02277.pdf">论文链接</a>

---

<img src="slides.assets/image-20211111112921919.png" alt="image-20211111112921919" style="zoom: 60%;" />

* 全局信息: AdaptivelyDilatedSplitting + Glance Branch
* 局部信息: Gaze Branch

<style>
img{
  margin: 0 auto;
}
</style>

---

<img src="slides.assets/image-20211111112859682.png" alt="image-20211111112859682" style="zoom:50%;" />

<style>
img{
  margin: 0 auto;
  margin-top: 200px;
}
</style>
---

# Comparison

<img src="slides.assets/image-20211111114047039.png" alt="image-20211111114047039" style="zoom:53%;" />

<style>
img{
  margin: 0 auto;
}
</style>
