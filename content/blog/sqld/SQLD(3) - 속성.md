+++
author = "Mincheol Park"
categories = ["SQLD"]
tags = ["SQLD", "1강"]
date = "2020-09-02"
description = ""
title = "SQLD(3) - 속성"
+++

# 속성의 개념

> 업무에서 필요로 하는 인스턴스로 관리하고자 하는 의미상 더 이상 분리되지 않는 최소의 데이터 단위.

속성은 엔터티에 속한 엔터티에 대한 자세하고 구체적인 정보를 나타내며 각각의 속성은 구체적인 값을 갖게 됩니다.  
 ex) 사원 엔터티 = 사원번호, 사원이름, 부서

<br>
<br>

# 속성의 정의

1.  업무에서 필요로 한다.
2.  의미상 더 이상 분리되지 않는다.
3.  엔터티를 설명하고 인스턴스의 구성요소가 된다.

`생년월일`은 생년, 생월, 생일로 구분되어질 수 있지만 사실상 하나의 의미를 나타내기 때문에 하나의 속성으로 간주할 수 있습니다.
하지만 서로 관련이 없는 `이름과 주소`를 '이름주소'라는 속성으로 정의하면 한 속성에 2개의 의미를 가지게 되므로 기본속성으로서 성립되지 않습니다.

<br>
<br>

# 엔터티, 인스턴스, 속성, 속성값에 대한 관계

> 한 개의 엔터티는 두 개 이상의 인스턴스의 집합이어야 한다.  
> 한 개의 엔터티는 두 개 이상의 속성을 갖는다.  
> 한 개의 속성은 한 개의 속성값을 가진다.

<p align="center"><img src="/img/blog/SQL_033.jpg"></p>
<br>
<br>

# 속성의 표기법

<p align="center"><img src="/img/blog/SQL_034.jpg"></p>
<br>

# 속성의 특징

속성은 다음과 같은 성질을 가지고 있으며 이중 하나의 성질을 만족하지 못하면 적절하지 않은 속성일 확률이 높다.

> - 엔터티와 마찬가지로 반드시 해당 업무에서 필요하고 관리하고자 하는 정보이어야 한다.
> - 정규화 이론에 근간하여 정해진 주식별자에 함수적 종속성을 가져야 한다.
> - 하나의 속성에는 한 개의 값만을 가진다. 하나의 속성에 여러 개의 값이 있는 다중값일 경우 별도의 엔터티를 이용하여 분리한다.
>   <br>
>   <br>

# 속성의 분류

## 속성의 특징에 따라

> **기본속성(Basic Attribute)** : 속성은 업무분석을 통해 바로 정의한 속성  
> **설계속성(Designed Attribute)** : 원래 업무상 존재하지는 않지만 설계를 하면서 도출해내는 속성  
> **파생속성(Derived Attribute)** : 다른 속성으로부터 계산이나 변형이 되어 생성되는 속성

1. 기본속성  
   기본 속성은 업무로부터 추출한 모든 속성이 여기에 해당하며 엔터티에 가장 일반적이고 많은 속성을 차지한다. 코드성 데이터, 엔터티를 식별하기 위해 부여된 일련번호, 그리고 다른 속성을 계산하거나 영향을 받아 생성된 속성을 제외한 모든 속성은 기본속성이다. 주의해야 할 것은 업무로부터 분석한 속성이라도 이미 업무상 코드로 정의한 속성이 많다는 것이다. 이러한 경우도 속성의 값이 원래 속성을 나타내지 못하므로 기본속성이 되지 않는다.

2. 설계속성  
   설계속성은 업무상 필요한 데이터 이외에 데이터 모델링을 위해, 업무를 규칙화하기 위해 속성을 새로 만들거나 변형하여 정의하는 속성이다. 대개 코드성 속성은 원래 속성을 업무상 필요에 의해 변형하여 만든 설계속성이고 일련번호와 같은 속성은 단일(Unique)한 식별자를 부여하기 위해 모델 상에서 새로 정의하는 설계속성이다.

3. 파생속성  
   파생속성은 다른 속성에 영향을 받아 발생하는 속성으로서 보통 계산된 값들이 이에 해당된다. 다른 속성에 영향을 받기 때문에 프로세스 설계 시 데이터 정합성을 유지하기 위해 유의해야 할 점이 많으며 가급적 파생속성을 적게 정의하는 것이 좋다.

<br>

## 엔터티 구성방식에 따라

> **PK(Primary Key)** : 엔터티를 식별할 수 있는 속성  
> **FK(Foreign Key)** : 다른 엔터티와의 관계에서 포함된 속성  
> **일반속성** : 엔터티에 포함되어 있고 PK, FK에 포함되지 않은 속성

<br>

# 도메인

각 속성은 가질 수 있는 값의 범위가 있는데 이를 그 속성의 도메인(Domain)이라 한다. 예를 들면 학생이라는 엔터티가 있을 때 학점이라는 속성의 도메인은 0.0에서 4.0 사이의 실수 값이며 주소라는 속성은 길이가 20자리 이내인 문자열로 정의할 수 있다. 여기서 물론 각 속성은 도메인 이외의 값을 갖지 못한다. 따라서 도메인을 좀더 이해하기 쉽게 정리하면, 엔터티 내에서 속성에 대한 데이터타입과 크기 그리고 제약사항을 지정하는 것이라 할 수 있다.

<br>

# 속성의 몀명

- 해당업무에서 사용하는 이름을 부여해야 한다.
- 서술식 속성명은 사용하지 않는다.
- 약어 사용은 가급적 제한한다.
- 전체 데이터모델에서 유일성을 확보하는 것이 좋다.

출처: SQL 전문가 가이드 - KDB 한국데이터베이스진흥원
