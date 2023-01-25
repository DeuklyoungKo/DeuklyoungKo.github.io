---
layout: single
permalink: /guide/
---
# 컨텐츠등록 가이드

## 컨텐츠 추가 방법 3가지
    1. jekyll을 자신의 컴퓨터에 설치하여 로컬에서 문서 추가 및 수정 후 로컬 사이트 에서 확인 후 github에 push하여 github페이지에서 확인
    2. jekyll설치 안하고 로컬에서 문서 추가 및 수정 후 github에 push하여 github페이지에서 확인
    3. github 웹사이트에서 문서 추가 및 수정 후 github페이지에서 확인

* github에 파일을 추가하거나 수정하면 github에서 jekyll 빌드하는 시간이 1분 정도 걸립니다. 빌드 상태는 github 해당 repository - Actions 탭에서 확인 가능합니다.


## 컨텐츠 분류
해당 사이트 내에 글을 작성할 수 있는 곳은
```m
국문 : 연구성과, SHINE 데이터, 언론보도
영문 : 연구성과, SHINE 데이터, 언론보도
```
입니다.

## 컨텐츠 등록 폴더
이 중 **연구성과**와 **언론보도**는 리스트만 있는 페이지이며 해당 제목 클릭 시 새 탭에서 설정된 사이트가 보이게 됩니다.
콘텐츠 추가는 국문 영문 각각 Markdown 파일을 특정 폴더에 추가하는 방식으로 구성이 되어 있으며 콘텐츠별 저장 폴더는 다음과 같습니다.
```m
연구성과 국문 : /collections/_results
연구성과 영문 : /collections/_results_eng
SHINE 데이터 국문 : /collections/_shineData
SHINE 데이터 영문 : /collections/_shineData_eng
언론보도 국문 : /collections/_posts
언론보도 영문 : /collections/_posts_eng
```

## 컨텐츠 파일명
컨텐츠 파일명은 년도-월-일-파일제목.md(또는 .markdown) 양식으로 이루어 지며 파일명의 해당 년월일이 작성일로 인식되도록 되어 있습니다. 파일제목에 국문이 포함되면 오류가 발생할 소지가 있으니 가급적 영문으로 작성하는 것이 좋습니다.
```m
ex) 2022-11-02-contentstitle.md
or  2022-11-02-covid19Result2022.markdown
```

## 컨텐츠 별 Front Matter
jekyll 은 콘텐츠의 구성 정보를 콘텐츠 페이지 상단에 YAML값을 사용하도록 되어 있습니다.  
ref) [Front Matter](https://jekyllrb.com/docs/front-matter/)

각 컨텐츠별 Front Matter는 아래와 같습니다.

### 연구성과 국문 Front Matter(등록폴더 : /collections/_results)
```m
---
title: [제목]
subTitle: [상세설명]
sourceUrl: [사이트 링크 URL]
institution: [발행기관명, 옵션]
journal: [발행잡지명, 옵션]
---

    ex)
    ---
    title:  "감염병 재난 대비 및 관리"
    subTitle:  "재난및 안전관리 기본법에 따르면, 재난은 국민의 생명,신체,재산과 국가에 피해를 주거나"
    sourceUrl: https://www.kdca.go.kr/contents.es?mid=a20401070407
    institution: 카이스트
    journal: KSPT
    ---
```

### 연구성과 영문 Front Matter(등록폴더 : /collections/_results_eng)
```m
---
title: [제목]
subTitle: [상세설명]
sourceUrl: [사이트 링크 URL]
institution: [발행기관명, 옵션]
journal: [발행잡지명, 옵션]
---

    ex)
    ---
    title:  "Research data on virus analysis for response to infectious diseases Part. 5"
    sourceUrl: https://www.google.com
    subTitle: "Research data on virus analysis for response to infectious diseases sub title  diseases sub title 5"
    institution: KIST
    journal: KSPT
    ---
```

### SHINE 데이터 국문 Front Matter(등록폴더 : /collections/_shineData)
```m
---
title:  [제목]
header:
  teaser: [리스트 페이지 썸네일 이미지 주소]

toc: [페이지내 목차를 사용할지 안할지 설정, true|false, 옵션]
toc_label: [목차 제목, 옵션]
toc_icon: [목차 아이콘, 옵션]
toc_sticky: [목차가 페이지를 따라다니게 할지 안할지 설정,  true|false, 옵션]
---
[본문내용]

    ex1) 목차를 사용할 경우
    ---
    title:  본문 양식에 대한 샘플 페이지
    header:
      teaser: https://www.fda.gov/files/COVID%20testing%20policy_1600x900_0.png

    toc: true
    toc_label: 목차
    toc_icon: cog
    toc_sticky: true
    ---
    본문내용이 입력되는 부분입니다.


    ex2) 목차를 사용 안할 경우
    ---
    title:  본문 양식에 대한 샘플 페이지
    header:
      teaser: https://www.fda.gov/files/COVID%20testing%20policy_1600x900_0.png
    ---
    본문내용이 입력되는 부분입니다.
```
* header: 와 teaser:사이의 2칸 들여쓰기를 주의.
* 목차 아이콘 사용 시 https://fontawesome.com/v5/search?o=r&m=free&s=solid 페이지에서 아이콘 네임 및 저자권 확인.



### SHINE 데이터 영문 Front Matter(등록폴더 : /collections/_shineData_eng)
```m
---
title:  [제목]
header:
  teaser: [리스트 페이지 썸네일 이미지 주소]

toc: [페이지내 목차를 사용할지 안할지 설정, true|false, 옵션]
toc_label: [목차 제목, 옵션]
toc_icon: [목차 아이콘, 옵션] * https://fontawesome.com/v5/search?o=r&m=free&s=solid 페이지에서 아이콘 네임 및 저자권 확인.
toc_sticky: [목차가 페이지를 따라다니게 할지 안할지 설정,  true|false, 옵션]
---
[본문내용]


    ex)
    ---
    title:  "Welcome to SHINE"
    header:
      teaser: https://cdn.pixabay.com/photo/2020/02/09/16/23/coronavirus-4833754_960_720.jpg

    toc: true
    toc_label: contents
    toc_icon: cog
    toc_sticky: true      
    ---
    here is contents area.
```
* header: 와 teaser:사이의 2칸 들여쓰기를 주의.

### 언론보도 국문 Front Matter(등록폴더 : /collections/_posts)
```m
---
title: [제목]
sourceUrl: [사이트 링크 URL]
sourceImgUrl: [썸네일 이미지 URL]
---
[리스트에 나오는 본문내용]

    ex)
    ---
    title:  "KT, 감염병 대응연구 앱 `샤인` 개편…코로나19 연구 나선다"
    sourceUrl: https://shineforall.org/shine-news/?uid=10&mod=document&pageid=1
    sourceImgUrl: https://shineforall.org/wp-content/uploads/kboard_attached/1/202204/6253847cf19ce2830572.jpg
    ---
    KT는 AI(인공지능) 기반 감염병 대응연구 애플리케이션 '샤인'의 연구 범위를 독감에서 코로나19까지 확대 개편했다고 15일 밝혔다.
```

### 언론보도 영문 Front Matter(등록폴더 : /collections/_posts_eng)
```m
---
title: [제목]
sourceUrl: [사이트 링크 URL]
sourceImgUrl: [썸네일 이미지 URL]
---
[리스트에 나오는 본문내용]
    ex)
    ---
    title:  "'Shine', KT reorganizes its infectious disease response research app"
    sourceUrl: https://shineforall.org/shine-news/?uid=10&mod=document&pageid=1
    sourceImgUrl: https://shineforall.org/wp-content/uploads/kboard_attached/1/202204/6253847cf19ce2830572.jpg
    language: eng
    ---
    KT announced on the 15th that it has expanded and reorganized the research scope of its AI (artificial intelligence)-based infectious disease response research application 'Shine' from flu to COVID-19.
```