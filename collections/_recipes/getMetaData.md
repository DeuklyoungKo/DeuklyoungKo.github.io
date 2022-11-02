---
output: true
title:  "get meata data"
date:   2022-10-31 16:38:55 +0900
categories: jekyll update


header:
  teaser: /assets/images/notice_contents.png
  overlay_image: /assets/images/bg.jpg
  # image: /assets/images/notice_contents.png

  # video:
  #   id: cTuokF7-RXA
  #   provider: youtube



layout: single
# classes: wide

# author_profile: false
# sidebar: false


toc: true
toc_label: "My Table of Contents"
toc_icon: "cog"
toc_sticky: true

---
메타 데이터 가져오기 테스트

# 메타 데이터를 가져노는 방법에 대한 연구

<script>
console.log("To start get metadata")
const contentUrl =  "https://n.news.naver.com/mnews/article/029/0002724752?sid=105"


$.ajax({
    url:contentUrl,
    type:"GET",
    success: function(result) {
        if (result) {
          console.log(result)
        } else {
            alert("불러오기 실패");
        }
    }
});

</script>