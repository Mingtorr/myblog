+++
author = "Mincheol Park"
categories = ["Blog"]
tags = ["Markdown"]
date = "2020-09-08"
description = "How to use markdown"
title = "마크다운 문법정리"
+++

> 마크다운(markdown)은 일반 텍스트 문서의 양식을 편집하는 문법이다.  
> README 파일이나 온라인 문서, 혹은 일반 텍스트 편집기로 문서 양식을 편집할 때 쓰인다.  
> 마크다운을 이용해 작성된 문서는 쉽게 HTML 등 다른 문서형태로 변환이 가능하다.  
> _위키백과_

#

# 제목 (Headings)

HTML과 같이 h1부터 h6까지 표시할 수 있으며 #의 갯수로 표현이 가능합니다.  
h1이 가장 크고 h6가 가장 작습니다.

```markdown
# h1

## h2

### h3

#### h4

##### h5

###### h6
```

위의 결과는 다음과 같습니다.

# h1

## h2

### h3

#### h4

##### h5

###### h6

#

---

#

# 개행 (Newline)

마크다운에서 엔터를 친다고 줄바꿈이 되지 않습니다.  
 줄바꿈을 하기 위한 방법은 다음과 같습니다.

1.  문장의 끝에서 스페이스바를 2번 누른다.
2.  줄을 띄우고 싶은 부분에서 # 적는다.

줄바꿈을 여러번해 공간을 만들고 싶다면 #을 이용하세요.  
이를 활용하면 자신이 원하는대로 개행을 할 수 있습니다.

```
줄바꿈 하고 싶어요!
#
개행되었습니다!
```

---

#

# 인용문 (Blockquotes)

인용문은 `>`을 사용합니다. `>`의 갯수에 따라 중첩사용이 가능합니다.

```markdown
> 인용문은 이렇게 사용합니다.
>
> > 중첩사용도 가능합니다!
```

> 인용문은 이렇게 사용합니다.
>
> > 중첩사용도 가능합니다!

**Note**로 강조하기 가능합니다

---

#

# 표 (Tables)

테이블은 엔터키 위의 | 를 이용하여 작성합니다.  
기본적인 폰트체의 적용도 가능합니다.

```markdown
| name | age |
| ---- | --- |
| Park | 24  |
| Lim  | 24  |
```

| name | age |
| ---- | --- |
| Park | 24  |
| Lim  | 24  |

#### 폰트체를 적용한 테이블

```markdown
| Italics   | Bold     | Code   |
| --------- | -------- | ------ |
| _italics_ | **bold** | `code` |
```

| Italics   | Bold     | Code   |
| --------- | -------- | ------ |
| _italics_ | **bold** | `code` |

---

#

# 목록 (List)

순서를 표기하는 목록과 순서가 없는 목록 2가지 방법으로 목록을 표기할 수 있습니다.

**Ordered List**

```
1. First item
2. Second item
3. Third item
```

1. First item
2. Second item
3. Third item

**Unordered List**  
순서가 없는 목록을 작성할 경우 -, \*, + 를 사용하여 작성할 수 있습니다.

- List item
- Another item
- And another item

**Nested list**  
탭이나 스페이스바를 통해 인라인 블럭으로 작성이 가능합니다.

- Fruit
  - Apple
  - Orange
  - Banana
- Dairy
  - Milk
  - Cheese

---

#

# 코드블럭

Tab키 위의 `를 사용하여 한줄의 인라인 코드를 작성할 수 있습니다.  
여러 줄의 코드를 작성할 경우 ``` 으로 감싸 사용할 수 있습니다.

```html
<head>
  <meta charset="utf-8" />
  <title>Example HTML5 Document</title>
</head>
```

---

#

# 링크 (Link)

링크는 인라인 링크와 url링크로 구현할 수 있습니다.

```markdown
인라인링크  
[깃허브](https://github.com/)
url 링크  
<https://github.com/>
```

인라인링크  
[깃허브](https://github.com/)  
url 링크  
<https://github.com/>

---

#

# 이미지 (Image)

이미지 크기는 10MB 이하만 가능합니다.
이미지를 사용하는 방법은 다음과 같습니다.

```markdown
![이미지 설명](이미지 링크)
![토리](/images/torr.jpg")
```

![이미지 설명](이미지 링크)  
![torr](/images/torr.jpg)
