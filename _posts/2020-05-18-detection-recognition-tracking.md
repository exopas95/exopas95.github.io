---
layout: post
title:  "Recongition vs Detection vs Tracking"
date:   2020-05-18T14:25:52-05:00
author: TreeNulbo
categories: Convolutional-Neural-Network
---

<div align="center">
  <img src="https://user-images.githubusercontent.com/38775259/84569441-8c28d100-adc1-11ea-84da-27ef0ee4a9b7.jpg" width="600", height="400"></img>
</div>

영상처리에서 자주 다루는 용어인 **Recognition, Detection, Tracking** 이 각각 어떤 것인지 알아보고
그 차이는 무엇인지 기록하고자 한다. 매번 볼때마다 살짝 헷갈리는데 특히나 Detection과 Recognition이 주로 헷갈리는 분들이 많다.
이를 조금이나마 돕고자 간단한 예시로 설명을 한 번 해보겠다. 
그리고 차차 업데이트를 통해 각 과정에 쓰이는 알고리즘이 어떤 것들이 있는지 간단한
설명을 하고자 한다. 각 알고리즘에 대한 자세한 설명은 별도의 포스팅을 할 예정이다. 

## Detection vs Recognition
detection은 영상, 이미지에서 대상을 찾는 과정이며 recognition은 찾은 대상을 DB에 저장하는 과정이다.
한 영상에서 사람의 얼굴을 찾는 과정은 detection 이다. 이후 이렇게 찾은 얼굴을 기존에 가지고 있는
DB와 대조하며 누구인지를 식별하는 과정이 바로 recognition 이다.
조금 더 구체적인 예를 들어보자. 영상 분석에서 트럼프 대통령의 얼굴을 찾고 싶다고 해보자. 이때 영상 속에
등장하는 사람들의 얼굴을 찾는 과정이 detection이다. 이후 찾은 얼굴들을 자신이 가지고 있는 DB에 대조하며
트럼프 대통령의 얼굴인지 아닌지를 식별하는 과정이 recognition 이다. <br><br>

Recognition이 직역하면 한국어로 "인식"이기 때문에 많은 분들이 detection과 recognition을 헷갈려하는 것 같다. 
recognition은 어떤 의미에서 **identification** 의 의미로 사용되기 때문에 "인식"이 아닌 "식별"이라고 해석하고
기억해 두면 헷갈일 일이 적어지지 않을까 생각한다.

## Tracking
그렇다면 detection과 tracking의 차이점은 무엇일까? 근본적으로 detection은 영상에서 무언가를 **찾는** 것이지만 tracking은
찾고자 하는 특정 대상의 **위치 변화**를 파악하는 것이다. Tracking은 영상 프레임들 사이의 시공간적 유사성 즉, 대상의 위치, 크기, 형태 등이 유사한 대상을 계속 추적하는 것이다. 이처럼 tracking은 detection 보다 사용할 수 있는 정보들이 많다. tracking 에서는
대상의 위치, 크기, 형태을 정보로 가지고 있지만 detection은 그렇지 않다. 따라서 tracking 의 알고리즘이 detection 알고리즘 보다
간단한 경우가 더 많다. 
