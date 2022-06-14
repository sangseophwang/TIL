# Margin Collapse

> 같은 위치의 블록끼리 위쪽 및 아래쪽에 margin이 있다면, 이 경우 제일 큰 여백의 크기를
> 가진 단일 여백으로 결합(상쇄)되는 것.

margin collapse는 다음과 같은 세 가지 기본 상황에 발생한다.

1. 인접 형제
- 인접한 컨텐츠간의 margin이 서로 상쇄된다.

2. 부모 박스와 첫번째(마지막) 자식 박스의 상단(하단) 마진이 겹칠 때
- 브라우저는 부모 박스의 첫번째, 혹은 마지막 번째 자식 박스 간의 경계를 그 사이에 있는 border/padding/inline 컨텐츠 유무로 판단한다.
- 따라서 부모와 자식 사이에 inline 컨텐츠가 없거나, 상단(하단)에 명시적으로 padding 또는 border 값을 주지 않았다면 margin이 겹치게 된다.

3. 빈 블록
- border, padding, inline contents, height, min-height, max-height이 없으면 블록의 margin-top과 margin-bottom이 서로 상쇄된다.