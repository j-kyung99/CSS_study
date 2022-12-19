# grid 정리

    행과 열 두 가지 방향으로 배치 가능
      => 복잡한 레이아웃 작성에 매우 적합
    (헤더, 사이드바, 컨테이너, 푸터 등)

## Grid Container(그리드 컨테이너)

    grid를 적용하는 전체 영역, 열과 행을 가지며 그리드 아이템들을 배치

## Grid Item(그리드 아이템)

    grid 컨테이너의 자식 요소들

## Grid Line(그리드 라인)

    grid를 그리는 행/열을 그려주는 선(각 선은 라인 넘버를 지님)

## Grid Track(그리드 트랙)

    grid 라인 사이의 행/열 공간

## Grid Cell(그리드 셀)

    grid 한 칸(= 유닛)

## Grid Area(그리드 영역)

    4개의 그리드 라인으로 둘러싸인 공간(셀이 묶인 영역)
      -> 식별자를 통해 요소 배치

### grid-template-rows : row(행)의 높이 지정

```javascript
grid-template-rows: row1높이 row2높이;
```

### grid-template-columns : column(열)의 높이 지정

```javascript
grid-template-columns: column1높이 column2높이;
```

### fr : 상대적인 크기를 지정할 수 있음(비율)

### repeat() 함수 => repeat(반복횟수, 반복값);

```javascript
grid-template-columns: 140px 140px 140px 140px;
===
grid-template-columns: repeat(4, 140px);
```

### min-max함수 => minmax(트랙의 최솟값, 트랙의 최댓값)

    - max-content : 그리드 트랙을 차지하는 최대 콘텐츠 범위(=auto)
    - min-content : 그리드 트랙을 차지하는 최소 콘텐츠 범위

```javascript
minmax(auto, max - content);
//그리드 아이템 콘텐츠 크기에 맞추어 영역 설정
```

- auto-fill과 사용하여 반응형 그리드 영역을 만들 수 있음

### grid-auto-rows(columns) : 암시적 행(열)의 크기 적용

- grid-template-rows 속성 사용 시 새롭게 추가될 아이템에는 적용되지 않음 => 이를 해결하기 위해 auto 사용

### Gap

    그리드 컨테이너와 아이템 요소들의 간격을 설정하는 속성
    (fr단위는 사용할 수 없음)

- margin과 gap의 차이점

  - margin : 인접한 요소의 존재와 상관 X, 불필요한 공간을 만듦
  - gap : 인접한 요소가 있을때만 공간을 만듦, 불필요한 공간 X

- row-gap, column-gap
- 축약형: gap: <row-gap> <column-gap>

### grid-column(row)-start ~ grid-column(row)-end

    마음대로 레이아웃 지정 가능
    - span 사용 시 몇 칸 차지하는지 작성

```javascript
grid-column-start: 1,
grid-column-end: 3
===
grid-column: 1 / 3
```

### grid-template-area

    직관적인 레이아웃 지정 가능
    빈칸은 .이나 none으로 작성하면 됨
