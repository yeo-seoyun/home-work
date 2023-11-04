ss# mission-01

## flex 사용하여 배치하기
1 전체 영역을 .container 로 지정
```sh
  .container {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    }
```
2 .minibox로 하단의 작은 박스 묶어주기
``` sh
.mini-box {
  width: 505px;
  display: flex;
  justify-content: space-between;
  margin: auto;
}
```

## section 영역 만들기
1 각 박스들을 section으로 묶기
```sh
<section class="item-1">

</section>
.
.
<section class="item-2">

</section>
.
.
<section class="item-3">

</section>
```
2 section안에 div로 박스 컨텐츠 영역 지정
```sh
<section class="item-1">
  <div class="item-1box">
  </div>
</section>
.
.
<section class="item-2">
  <div class="item-2box">
  </div>
</section>
.
.
<section class="item-3">
  <div class="item-3box">
  </div>
</section>
```


## overflow: hidden 사용하기
1 .item-1box 영역에 overflow: hidden 지정
```sh
.item-1box,
.item-2box,
.item-3box {
  width: section 크기 보다 작게 지정;
  height: 크기지정;
  position: relative;
  margin: auto;
  overflow: hidden;
}
```
- **overflow: hidden**을 사용하여 구매하기 button이 숨겨지는 영역 만들어주기
- position: relative; 를 이용하여 부모요소 적용
  - 'button'의 **위치를 조정**하기 위한 사용

## button 영역
```sh
.btn-1,
.btn-2,
.btn-3 {
  position: absolute;
  bottom: 15px;
  left: -70px;
  width: 112px;
  height: 42px;
}
```
- position: absolute; 를 이용하여 자식요소 적용
  - **bottom**, **left**로 button의 hover 전의 위치 조정

## hover 효과
```sh
.item-1:hover .btn-1,
.item-2:hover .btn-2,
.item-3:hover .btn-3 {
  transform: translateX(65px);
  background: royalblue;
}
```
- **transform: translateX(65px);** 를 사용하여 hover시의 button위치 조정

