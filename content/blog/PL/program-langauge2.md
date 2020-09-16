+++
author = "Mincheol Park"
categories = ["PL"]
tags = ["PL"]
date = 2020-09-13T20:00:12+09:00
description = "프로그래밍에서의 패러다임"
title = "프로그래밍에서의 패러다임"
+++

# 1. 패러다임(paradigm) 이란?

> 한 시대의 과학을 보는 공통된 시각( 세상을 보는 눈).  
> a very clear or typical example of something.  
> an example or pattern of a word, showing all its froms in grammar.  
> ex) 천동설과 지동설

## 2. 프로그래밍에서의 패러다임

> 컴퓨터에서 계산 수행의 의미와 실행될 작업들의 구성 방법에 관한 개념적인 수단

특정 패러다임을 지원하는 언어에 익숙할수록 문제를 이해하는 사고 방식도 그 패러다임에 치우치게 됩니다  
프로그래밍에서의 패러다임은 프로그래밍을 하는 양식, 계산 수행을 한다는 것이 무엇인가? , 실행작업의 구성에 대한 생각하는 방법의 차이에 따라 달라질 수 있습니다.**어떤 것이 더 좋고 나쁘다는 없습니다.**

<br>

## 프로그래밍 패러다임의 종류

명령형(imperative), 객체지향(object-oriented), 함수형(functional), 논리형(logic) 이 대표적인 4가지이다.

<br>

## 명령형 패러다임

**전통적인 계산 모델**. 처리 장치가 메모리와 분리되어 있으며 대표적으로 C언어가 있습니다.
명령형 패러다임에서 계산을 보는 시각은 수학적으로 보기보다는 컴퓨터 하드웨어를 중심에 두고 생각합니다.
**`실행되는 컴퓨터를 직접적으로 모델링`**할 수 있다는 장점이 있지만 **`낮은 수준의 추상화,수학적 모델의 부재, 수학적 모델이 없어 정확성 증명이 어려운 단점`**이 있습니다. 낮은 수준의 추상화로 인해 C언어의 포인터를 쓰려면 메모리에 대한 이해도 필요합니다. 또한 수학적 모델이 없어 이 프로그램이 100% 완전하게 작동한다는 것을 보장할 수 없습니다.

- 상태 (메모리의 상태)
- 변수 (메모리) - 기억장소의 추상화
- 배정문 (메모리 내용의 변경) - 기억장소 내용의 변경
- 순차적 실행과 루프 (연속적인 변경을 위해) - 제어의 추상화

<br>

## 객체지향 패러다임

**순환적 설계**. 대표적으로 smalltalk 같은 객체지향 언어가 있습니다.
컴퓨터는 컴포넌트들의 네트워크이며 각 컴포넌트는 독립적으로 움직이는 하나의 컴퓨터 객체입니다.

- 객체의 설계 : data와 operatoin
- 서비스의 설계 : 다른 객체에 대한 서비스
  - Ask not what you cna do to your data structures, but ask what your data structures can do for you.
  - 데이터 구조에 대해 무엇을 조작할 것인지 묻지 말고, 데이터 구조가 무엇을 해줄 수 있는지 물어보십시오.

<br>

## 함수형 패러다임

> 함수와 계산결과가 파라미터로 넘어갈 수 있다. 다만 함수가 first-class value는 아니어서 return 받을 때 상당히 제약이 많다. function pointer이용해서 함수를 넘기기 때문

1. Values are treated as single entities (not as "boxes with slots"). Values can be created, but once created they never modified.  
   값은 단일 엔터티로 처리한다. 가치는 창조될 수 있지만, 한번 창조되면 결코 수정되지 않는다.
2. Computation is performed by applying functions to values, and recursively by applying functions to the results.  
   계산은 함수를 값에 적용하여 수행하고, 결과에 함수를 적용하여 재귀적으로 계산한다.
3. Functions are a "first-class" data value, and can be assigned to identifiers, passed as arguments, or returned as the result of exceuting other functions.  
   함수는 "제1종" 데이터 값이며, 식별자에 할당하거나 인수로 전달하거나 다른 함수를 실행한 결과로 반환할 수 있다.

**주요 용어**

- single-assignment form : 변수에 값을 한번만 줄 수 있다. 변수의 값이 한번 정해지면 더 이상 변화되지 않는다.
- referential transparency : 참조투명성, 함수의 값은 오직 매개변수에 의해서만 결정된다.  
   이것이 없으면 수학적으로 정확성을 증명하기 어렵다.  
  **c언어는 참조투명성이 없다.** 그 이유는 global 변수,포인터,정적변수가 존재해서 값이 매개변수에 의해서만 결정되지 않는다.
- lazy evaluation : 지연계산, 필요하지 않은 것은 계산하지 않는다.
- higher-order function : 고차 함수, 함수를 다루는 함수
  함수를 파라미터로 받고 리턴할수 있는 함수.

<br>

## 논리형 패러다임

> 프로그램 자체가 참과 거짓을 밝혀나가는 논리를 써가며 프로그래밍합니다.  
> 백트래킹이라는 방식에 의해서 실행됩니다.

**자동 정리 증명**  
`AMY는 BOBDML 부모이다.`라는 fact가 있으면 `AMY는 BOB의 조상일까? BOB은 BOB의 조상일까?` 라는 질문을 하고 답을 주는 방식에 의해 프로그래밍이 진행된다.

**논리 프로그램의 종류**

- facts, or assumptoins
- rules of inference
- questions, or queries
