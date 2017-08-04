# 170615 WEB 개발하기
# 1 - 필수 CSS 스터디 (1)

## (1) Box 모델 : CSS 요소가 표시되는데 필요한 구성 요소의 집합
### Content : 실제내용
### Padding : 내부 여백
- padding : 모든 여백
- padding-left(right, top, bottom)해서 따로 설정 가능
- padding을 늘리면 content는 그대로이므로 박스가 넓어짐
### Border : 테두리선
- border : 10px   solid                             #000
-          선굵기  선스타일(dotted, dashed, double)    색
### Margin : 다른 요소와의 간격
- margin : 상하좌우 모든가격
- margin-left(right, top, bottom)으로 해서 따로 설정 가능
- margin 겹침 현상 : 2개의 요소가 세로로 나열될 때 큰 값의 margin만 적용되는 현상 - margin이 35인 박스 두개가 세로로 있으면 간격이 70이 아닌 35
