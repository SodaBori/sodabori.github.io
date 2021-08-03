---
layout: post
category: [deep_learning]
title:  "전통적인 Deep Learning Model의 발전사"
author: sodabori
date:   2021-08-02 03:18:00 +0900
og_image: assets/posts/Traditional_Deep_Learning/nasrl_controller.png
og_description: "전통적인 Deep Learning Model들이 어떻게 발전해왔는지에 대한 이야기를 나눕니다."
---
# Deep Learning의 태동기

기존에 빛을 보지 못했던 Deep Learning은 2012년 ImageNet Challenge에서 Deep Learning기반의 AlexNet이 상당히 좋은 이미지 분류 성능을 보여준 이후 엄청난 속도로 발전해왔다. 특히 이러한 발전은 Model의 Architecture들을 변경해오면서 주로 이루어졌다.

<div class="sx-picture">
  <a href="/assets/posts/Traditional_Deep_Learning/imagenet_challenge.png" data-lity>
    <img src="/assets/posts/Traditional_Deep_Learning/imagenet_challenge.png"/>
  </a>
  <span class="sx-subtitle">ImageNet Challenge</span>
</div>

위의 그림에서 2012년부터의 Model들은 모두 Deep Learing 기반의 모델들을 나타낸다. 이 때 **AlexNet**은 처음으로 Deep Convolutional Netowrk가 Image Classification에서 좋은 성능을 가질 수 있다는 것을 보여줬다. 그리고 이후 2014년에는 2가지 방향의 새로운 Network들이 등장했는데 먼저 첫번째로 **GoolgeNet**의 경우 Network에서 반복되는 구조를 보여주며 각 구조에서는 다양한 Receptive Field를 가지도록 다양한 크기의 Kernel들을 사용하여 Output을 만들어 낸 뒤 결과 값을 Aggregation하는 형태를 취한다. 또한 2014년에는 다른 방향의 연구도 진행되었는데 그것이 바로 **VGGNet**이다. VGGNet의 경우 AlexNet 대비 작은 크기의 Kernel(3x3)을 사용한다. 대신 Layer를 깊게 쌓음으로써 기존의 큰 Kernel들이 가질 수 있었던 넓은 Receptive Field를 가질 수 있도록 한다. 이 전략은 같은 수준의 Receptive Field를 더 작은 파라미터를 통해서 달성할 수 있다는 점에서 더 나은 Generalization을 기대할 수 있다. 하지만 VGGNet의 경우 Layer의 수를 19 ~ 22개로 한정하는 모습을 보여주는데 이는 당시의 Computational Power의 부족 때문이 아니라 VGGNet의 구조를 사용하여 Layer의 수를 무작정 늘릴 경우 성능이 오히려 떨어지는 문제가 발생했기 때문이다. 이 문제는 Machine Learning에서 흔히 말하는 Overfitting 문제라고 보기는 힘들다. 왜냐하면 Layer의 수가 무작정 증가하였을 때 Validation Loss 뿐만 아니라 Train Loss도 동시에 증가하기 때문이다. 이 배경을 바탕으로 2015년에 **ResNet**이 발표 되었다.