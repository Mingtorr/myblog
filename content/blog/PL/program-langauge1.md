+++
author = "Mincheol Park"
categories = ["PL"]
tags = ["PL", "1강"]
date = "2020-09-03"
description = "How to use markdown"
title = "프로그래밍 언어론 1강"
+++

# 프로그래밍 언어론 1강 -프로그래밍 언어와 추상화

---

# 프로그래밍 언어란?

1. 프로그램 제작의 도구
2. 사고에 영향을 미치는 도구
3. 추상화의 도구

-> 사용하는 프로그래밍 언어에 따라 문제를 보는 시각이 달라집니다.
따라서 유연한 사고를 할 수 있어야 합니다.

---

# 추상화란?

사전적 정의

1. existing as a quality or conecpt rather than as something real or sold.
2. to make a shortenend form of a thing by separtating out what is important.

따라서 추상화는 중요한 부분만 추출하고, 관심없는 부분은 무시합니다.  
 예를 들어 우리에게 냉장고에 중요한 부분은 물건을 넣으면 시원해진다는 것입니다.
하지만 냉장고를 제작하는 사람은 전력을 얼마나 소모하고, 문을 몇개 달것인지가 가장 중요한 요소일 것입니다.
또한 환경에 관심있는 사람은 냉매가 가장 중요한 요소일 것입니다.
이처럼 각자의 관점에 따라서 중요하게 생각하는 것이 다르므로 중요한 요소를 뽑아내고 중요하지 않은 것을 숨겨 복잡하지 않도록 만드는 것이 추상화입니다.

프로그래밍 언어에서의 추상화의 예  
 type : int, float  
 계산 : 1+2, 1.0 + 2.0

1+2 와 1.0+2.0 의 계산결과는 같습니다.
하지만 컴퓨터에서의 계산방식은 전혀 다른 로직을 통해 계산되지만 우리는 신경쓰지  
 않습니다. 이는 추상화를 시켜주기 때문에 우리가 전혀 신경쓸 필요가 없었기 때문입니다.

# 추상화에도 단계가 있습니다.

추상화의 단계가 높아질 수록 우리가 해야할 일은 줄어들고 더 쉽게 할 수 있습니다.

컴퓨터에서의 추상화에도 단계가 있습니다.

정렬방식 중 quicksort는 for문의 반복을 통해 구현할 수 있습니다.
하지만 함수로 되어 있는 라이브러리를 사용하면 더 높은 추상화 단계를 이용하는 것입니다.
더 높은 추상화 단계를 사용하려면 현재까지 가장 높은 단계인 객체지향을 사용하면 됩니다.

---

# 프로그래밍 언어의 정의

정의 : 기계와 인간이 판독가능한 형태로 계산을 서술하는 표기 체계
기계가 판독하기 위해서는 번역을 해주는 컴파일러가 있어야 하며, 사람이 쉽게 이해하기 위해서는 추상화 매커니즘이 있어야 합니다.

- \*계산\*\* : 컴퓨터가 실행할 수 있는 어떤 과정
  = 튜링 기계(turing machine)가 할 수 있는 일

기계 판독성 : 효율적인 번역기 가능
= 모호성이 없고, 빠른 시간 내에 번역

인간 판독성 : 프로그램 하나를 전체로 이해하기 위한 세부사항의 양을 줄임
= 추상화 매커니즘의 개발