---
theme: seriph
background: /cover.jpg
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

# Multimodal Emotion Recognition

---
layout: intro
---

# Contents

1. Multimodal Transformer for Unaligned Multimodal Language Sequences
2. Multimodal Emotion Recognition With Transformer-Based Self Supervised Feature Fusion

---

# Transformer

<img src="/transformer_resideual_layer_norm_3.png" alt="img" style="zoom: 50%;" />

<style>
img{
  margin: 0 auto;
  box-shadow: 0 0 6px 2px #eee;
}
</style>

---
layout: intro
---

# SSE-FT

## Multimodal Emotion Recognition With Transformer-Based Self Supervised Feature Fusion

IEEE Access 2020

S. Siriwardhana, T. Kaluarachchi, M. Billinghurst and S. Nanayakkara

<a target="_blank" href="https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9206016">Paper Link</a>

---

# Challenges

<main>
  <p>1. Inherent data non-alignment</p>
  <p>2. Long-range dependencies</p>
</main>

<img src="/image-20211215164627988.png" alt="image-20211215164627988" style="zoom:45%;" />

<style>
main{
  margin-top: 50px;
}
img{
  position: absolute;
  top: 120px;
  right: 120px;
  box-shadow: 0 0 6px 2px #eee;
}
</style>

---

# Framework

<img src="/image-20211215170630905.png" alt="image-20211215170630905" style="zoom: 47%;" />

<style>
img{
  margin: 0 auto;
  box-shadow: 0 0 6px 2px #eee;
}
</style>

---

<img id="a" src="/image-20211215182927712.png" alt="image-20211215182927712" style="zoom: 45%;" />

<div id="b">
  <img src="/image-20211215182104430.png" alt="image-20211215182104430" style="zoom:33%;" />
  <img id="c" src="/image-20211215182156369.png" alt="image-20211215182156369" style="zoom:40%;" />
</div>

<style>
#a{
  margin-top: 50px;
  box-shadow: 0 0 6px 2px #eee;
}
#b{
  position: absolute;
  top: 110px;
  right: 30px;
}
#c{
  margin-top: 120px;
}
</style>

---

<img src="/image-20211215183621504.png" alt="image-20211215183621504" style="zoom:65%;" />

<style>
img{
  margin: 0 auto;
  box-shadow: 0 0 6px 2px #eee;
}
</style>

---

<img src="/image-20211215182359600.png" alt="image-20211215182359600" style="zoom: 67%;" />

<style>
img{
  margin: 0 auto;
  box-shadow: 0 0 6px 2px #eee;
}
</style>

---

<img src="/image-20211215182416818.png" alt="image-20211215182416818" style="zoom:67%;" />

<style>
img{
  margin: 0 auto;
  box-shadow: 0 0 6px 2px #eee;
}
</style>

---

<img src="/image-20211215182434504.png" alt="image-20211215182434504" style="zoom:65%;" />

<style>
img{
  margin: 0 auto;
  box-shadow: 0 0 6px 2px #eee;
}
</style>

---
layout: intro
---

# MulT

## Multimodal Transformer for Unaligned Multimodal Language Sequences

Proc Conf Assoc Comput Linguist Meet 2019

Tsai YH, Bai S, Pu Liang P, Kolter JZ, Morency LP, Salakhutdinov R

<a target="_blank" href="https://arxiv.org/pdf/1906.00295.pdf">Paper Link</a>

---

# Challenges

<div id="a">
  <p>1. How to represent raw data modalitiest</p>
  <p>2. How to fuse such modalities before the prediction layer</p>
  <div id="b">
    <p>1) High dimensionality of embeddings</p>
    <p>2) Longer sequence lengths of features</p>
    <p>3) Mismatch between sizes and sequence lengths of features across modalities</p>
  </div>
</div>

<style>
#a{
  margin-top: 60px;
}
#b{
  padding-left: 16px;
}
</style>

---

# Framework

<img src="/image-20211215185316890.png" alt="image-20211215185316890" style="zoom:60%;" />

<style>
img{
  position: absolute;
  left: 420px;
  top: 30px;
  box-shadow: 0 0 6px 2px #eee;
}
</style>

---

<img src="/image-20211215190158306.png" alt="image-20211215190158306" style="zoom: 55%;" />

<style>
img{
  margin: 0 auto;
  margin-top: -40px;
  box-shadow: 0 0 6px 2px #eee;
}
</style>

---

<img src="/image-20211215190835861.png" alt="image-20211215190835861" style="zoom: 62%;" />

<style>
img{
  margin: 0 auto;
  margin-top: -20px;
  box-shadow: 0 0 6px 2px #eee;
}
</style>

---

<img src="/image-20211215193609719.png" alt="image-20211215193609719"/>

<style>
img{
  box-shadow: 0 0 6px 2px #eee;
  margin-top: 30px;
}
</style>

---

<img src="/image-20211215193654044.png" alt="image-20211215193654044"/>

<style>
img{
  box-shadow: 0 0 6px 2px #eee;
  margin-top: 30px;
}
</style>
