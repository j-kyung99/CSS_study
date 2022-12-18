# flex 정리

## axis = 축

    자식 요소의 정렬 방향 제어
    - row & column

## flex-direction

    flex container 내의 item 들의 정렬 방향 결정 속성
    (reverse 속성은 가급적 사용하지 말기)

## justify-content

    main axis로 어떻게 정렬(수평)

    - flex-start : 자식 요소를 맨처음으로 배치
    - flex-end : 자식 요소를 맨끝으로 배치
    - center : 주축의 중앙으로 배치
    - space-between : 자식 요소들 사이에 같은 간격 (컨테이너 너비에 꽉차게 / 양 끝은 0)
    - space-around : 둘레에 같은 간격 (양 끝은 사이 크기의 1/2)
    - space-evenly : 모든 간격이 균등(사이 크기 = 양 끝 크기)

## align

    일직선으로 맞춤(수직)
    (items = 한줄, content = 두줄 이상->단락별로 정렬)

    - stretch : 부모 요소에 맞게 늘림

## flex-wrap: wrap;

    부모의 총 넓이보다 자식 요소의 총 넓이가 더 넓을 때 부모 안에 들어갈 수 있게 다음 줄에 정렬해줌
    (flex-direction의 영향을 받음)

- 자동 맞춤 요소 : 아이템의 크기는 변경하지 않고 위치만 조정할 수 있게해줌

## flex-basis

    부모 요소의 주축이 되는 방향으로 flex 아이템의 초기값 지정

```javascript
flex-basis: 40px;
/* 40px보다 폭이 작은 것은 40px로 설정, 40px보다 폭이 큰 것은 크기에 맞게 알아서 늘어남
```

## flex-grow

    자식 요소의 flex item이 차지하는 비율 지정

## flex-shrink

    컨테이너 안에서 자식 요소인 flex 아이템을 자동으로 줄여서 적절하게 배치 (기본값은 1임 = 자동 축소 설정 O)
    *** but, 부모 요소에 flex-wrap 적용 시 shrink는 적용되지 않음!

## flex 축약 속성

    flex : <flex-grow> <flex-shrink> <flex-basis>
    (기본값은 0, 1, auto)

## align-self

    교차축 기준으로 '개별아이템' 요소 정렬

## order

    아이템 요소들의 순서 결정 (음수, 0, 양수 모두 사용 가능 -> 숫자가 작을수록 우선 순위)

## z-index

    덮어 씌우기 가능 (z축 기준)
