# MBTI 검사지 처럼 체크박스 구현하기

MBTI검사지는 해당 문제를 체크하면 자동으로 다음 문항으로 스크롤 된다.

이를 구현 하기 위해서는

```js
q1Ref.current.scrollIntoView({ behavior: "smooth" });
```

이 scrollIntoView를 사용하는데 주의사항은 smooth 부드러운 모션과 내려가는건 ios 기기에서는 지원하지 않는다.

그래서 ios도 부드러운 모션으로 하기 위해서는 smoothscroll polyfill 이 필요하다.
