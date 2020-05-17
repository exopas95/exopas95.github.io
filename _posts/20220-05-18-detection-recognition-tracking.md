---
layout: post
title:  "Recongition vs Detection vs Tracking"
date:   2020-05-18T14:25:52-05:00
author: 엄세웅
categories: CNN
---

영상처리에서 자주 다루는 용어인 Recognition, Detection, Tracking 이 각각 어떤 것인지 알아보고
그 차이는 무엇인지 기록하고자 한다. 매번 볼때마다 살짝 헷갈리는데 특히나 Detection과 Recognition이 주로 헷갈리는 분들이 많다.
이를 조금이나마 돕고자 간단한 예시로 설명을 한 번 해보겠다. 
그리고 차차 업데이트를 통해 각 과정에 쓰이는 알고리즘이 어떤 것들이 있는지 간단한
설명을 하고자 한다. 각 알고리즘에 대한 자세한 설명은 별도의 포스팅을 할 예정이다.

## Detection vs Recognition
Detection은 영상, 이미지에서 대상을 찾는 과정이며 Recognition은 찾은 대상을 DB에 저장하는 과정이다.
한 영상에서 사람의 얼굴을 찾는 과정은 Detection 이다. 이후 이렇게 찾은 얼굴을 기존에 가지고 있는
DB와 대조하며 누구인지를 식별하는 과정이 바로 Recognition 이다.
조금 더 구체적인 예를 들어보자. 영상 분석에서 트럼프 대통령의 얼굴을 찾고 싶다고 해보자. 이때 영상 속에
등장하는 사람들의 얼굴을 찾는 과정이 Detection이다. 이후 찾은 얼굴들을 자신이 가지고 있는 DB에 대조하며
트럼프 대통령의 얼굴인지 아닌지를 식별하는 과정이 Recognition 이다. <br><br>

Recognition이 직역하면 한국어로 "인식"이기 때문에 많은 분들이 Detection과 Recognition을 헷갈려하는 것 같다. 
Recognition은 어떤 의미에서 Identification 의 의미로 사용되기 때문에 "인식"이 아닌 "식별"이라고 해석하고
기억해 두면 헷갈일 일이 적어지지 않을까 생각한다.

## Tracking



