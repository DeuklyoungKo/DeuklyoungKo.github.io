# 컨텐츠등록 가이드

## 컨텐츠 분류
해당 사이트 내에 글을 작성할 수 있는 곳은
```
국문 : 연구성과, 데이터 분석, 언론보도
영문 : 연구성과, 데이터 분석, 언론보도
```
입니다.

## 컨텐츠 등록 폴더
이 중 **연구성과**와 **언론보도**는 리스트만 있는 페이지이며 해당 제목 클릭 시 새 탭에서 설정된 사이트가 보이게 됩니다.
콘텐츠 추가는 국문 영문 각각 Markdown 파일을 특정 폴더에 추가하는 방식으로 구성이 되어 있으며 콘텐츠별 저장 폴더는 다음과 같습니다.
```
연구성과 국문, 영문 : /collections/_results
데이터 분석 국문 : /collections/_posts
데이터 분석 영문 : /collections/_posts_eng
언론보도 국문, 영문 : /collections/_media
```
* 데이터 분석 국문과 영문 폴더가 분리되어 있는 이유는 구문에서 리스트 페이징 기능을 사용하기 위함입니다.

컨텐츠 파일명은 년도-월-일-파일제목.md(또는 .markdown) 양식으로 이루어 지며 행당 년월일이 작성일로 인식되도록 되어 있습니다. 파일제목에 국문이 포함되면 오류가 발생할 소지가 있으니 가급적 영문으로 작성하는 것이 좋습니다.
```
ex) 2022-11-02-contentstitle.md
or  2022-11-02-covid19Result2022.markdown
```

## 컨텐츠 별 Front Matter
jekyll 은 콘텐츠의 구성 정보를 콘텐츠 페이지 상단에 YAML값을 사용하도록 되어 있습니다.  
ref) [Front Matter](https://jekyllrb.com/docs/front-matter/)

각 컨텐츠별 Front Matter는 아래와 같습니다.

### 연구성과 국문 Front Matter(등록폴더 : /collections/_results)
```
---
title: [제목]
sourceUrl: [사이트 링크 URL]
---

    ex)
    ---
    title:  "감염병 대응을 위한 바이러스 분석에 대한 연구 자료 Part. 4"
    sourceUrl: https://www.google.com
    ---
```

### 연구성과 영문 Front Matter(등록폴더 : /collections/_results)
```
---
title: [제목]
sourceUrl: [사이트 링크 URL]
language: eng
---

    ex)
    ---
    title:  "Research data on virus analysis for response"
    sourceUrl: https://www.google.com
    language: eng
    ---
```

### 데이터분석 국문 Front Matter(등록폴더 : /collections/_posts)
```
---
title: [제목]
header:
    teaser: [썸네일 이미지가 있을 경우 썸네일 이미지 URL]
---

    ex)
    ---
    title:  "데이터분석 결과 2022 연구 보고"
    header:
        teaser: https://www.fda.gov/files/COVID%20testing%20policy_1600x900_0.png
    ---
```
* header: 와 teaser:사이의 들여쓰기를 지켜야 합니다.

### 데이터분석 영문 Front Matter(등록폴더 : /collections/_posts_eng)
```
---
title: [제목]
header:
    teaser: [썸네일 이미지가 있을 경우 썸네일 이미지 URL]
language: eng
---

    ex)
    ---
    title:  "Global metrics for several key indicators"
    header:
        teaser: https://www.fda.gov/files/COVID%20testing%20policy_1600x900_0.png
    language: eng
    ---
```
* header: 와 teaser:사이의 들여쓰기를 지켜야 합니다.

### 언론보도 국문 Front Matter(등록폴더 : /collections/_media)
```
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

### 언론보도 영문 Front Matter(등록폴더 : /collections/_media)
```m
---
title: [제목]
sourceUrl: [사이트 링크 URL]
sourceImgUrl: [썸네일 이미지 URL]
language: eng
---
[리스트에 나오는 본문내용]
    ex)
    ---
    title:  "KT, 감염병 대응연구 앱 `샤인` 개편…코로나19 연구 나선다"
    sourceUrl: https://shineforall.org/shine-news/?uid=10&mod=document&pageid=1
    sourceImgUrl: https://shineforall.org/wp-content/uploads/kboard_attached/1/202204/6253847cf19ce2830572.jpg
    language: eng
    ---
    KT announced on the 15th that it has expanded and reorganized the research scope of its AI (artificial intelligence)-based infectious disease response research application 'Shine' from flu to COVID-19.
```