---
layout: post
category: [deep_learning, neural_architecture_search]
title:  "Neural Architecture Search with Reinforcement Learning"
author: sodabori
date:   2021-08-02 03:18:00 +0900
og_image: assets/posts/Neural_Architecture_Search_with_Reinforcement_Learning/nasrl_controller.png
og_description: "Neural Architecture Search의 가능성을 보인 첫번째 논문에 대해 소개하는 글입니다."
---
2012년 ImageNet Challenge에서 Deep Learning기반의 AlexNet이 상당히 좋은 이미지 분류 성능을 보여준 이후 Deep Learning은 수 많은 아이디어들을 사용하여 모델의 구조를 계속 변경하면서 좋은 성능을 얻도록 발전 해왔다.
<div class="sx-picture">
  <a href="/assets/posts/Neural_Architecture_Search_with_Reinforcement_Learning/imagenet_challenge.png" data-lity>
    <img src="/assets/posts/Neural_Architecture_Search_with_Reinforcement_Learning/imagenet_challenge.png"/>
  </a>
  <span class="sx-subtitle">ImageNet Challenge</span>
</div>
이후 2014년에는 Network안에서 여러가지 형태의 receptive feild를 가지도록 다양한 형태의 convolution을 사용하는 GoogleNet이 ImageNet challenge에서 우승을 차지하였고 2015년에는 그 동안 layer