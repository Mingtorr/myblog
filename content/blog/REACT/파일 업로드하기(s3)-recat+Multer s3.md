+++
author = "Mincheol Park"
date = "2020-09-07"
description = "React+Multer+node.js+mysql"
title = "파일 업로드하기(aws s3) React+Multer+node.js+mysql"
categories = ["react"]
tags=["React","multer","node.js","mysql"]
draft = true
+++

지난 시간에 multer를 이용하여 로컬스토리지에 사진을 저장해보았습니다.  
 이번 시간에는 multer s3를 이용하여 사진을 저장하는 방법을 알아보겠습니다.
[파일 업로드하기(로컬스토리지) React+Multer+node.js 보러가기]()

# AWS S3를 사용하는 이유는?

저는 웹사이트를 구현할 때 multer를 이용하여 로컬스토리지에 저장하는 방식으로 구현했다가 이후 s3에 업로드 하는 방식으로 교체 했습니다.  
aws s3의 5GB 무료 제공이라는 혜택이 매력적이었고, 어짜피 ec2를 통해 배포를 시킬 것이라면 s3를 이용하지 않을 이유가 없었기 때문입니다.

## 1.
