# character

HTML, CSS만 이용하여 호랑이 만들기

아래 링크에서 확인 가능합니다.

https://jsk3342.github.io/character/

![Tiger](https://user-images.githubusercontent.com/85912592/162724788-24f0e6bd-e90c-4e2f-b9d6-ab2fd2015332.gif)


## 프로젝트의 목표

CSS를 숨쉬듯 자연스럽게 활용하는것이 목표였습니다. 머릿속에서 떠오르는 이미지를 실제 코드를 통하여 화면에 구현하는것이 목표였으며, 이 과정을 통해 다양한 것들을 시도할 수 있어서 재미있는 시간이였습니다.

## 구현의 어려움

### 1. 곡선을 표현하기 힘들었습니다.

머리 부분을 와이파이 모양처럼 완만한 곡선을 이루고 싶었으나, 아직 구현하지 못하여 일자 모양으로 처리 하였습니다.

### 2. 광선검 이벤트 달기

광선검과 얼굴을 호버 했을때 왕관과 망토가 나오게 하고 싶었으나, 한부위를 호버하게 되면 다른 부위를 동시에 호버하지 못하기 문에 구현에 어려움이 있었습니다.

### 3. z-index 개념

애니메이션을 사용하게 되면 그 요소를 기준으로 인덱스가 재정렬 된다는 사실 때문에 귀를 다시 분리해야 했고 이는 CSS의 stacking context을 이해하는 계기가 되었습니다.

### 4. 이미지 파일 깃허브 페이지 미구현

/ 를 사용하여 이미지의 경로를 절대경로로 설정하여 로컬 환경에서는 잘 작동하였지만 배포 상태에서는 구현되지 않았습니다. 상대 경로로 설정해여 이를 해결하였습니다.



## 만들면서 배운점

### 1. 가상 클래스의 사용.

눈이나 귀, 눈썹 처럼 양쪽에 데칼코마니 처럼 있는 레이아웃을 잡을때 가상 클래스를 자주 활용하다 보니 자연스럽게 익히게 되었습니다.

### 2. 박스 쉐도우 이해.

막연하게 쉐도우 기법을 알고 있었는데 이번 기회에 요소마다 어떤 역할을 하게 되는지 파악하게 되었습니다.

### 3. z-index 활용.

제트 인덱스 또한 막연하게 숫자만 적으면 된다고 생각하였지만, 호랑이의 얼굴과 귀 부분의 구조를 완전이 뜯고 분리해야 사용 가능하였습니다. 정적인 페이지에서는 별 문제 없이 사용 가능하였지만 호랑이의 얼굴에 애니메이션 효과를 주게 되는 순간, z인덱스의 기준점이 효과를 준 호랑이의 얼굴 기준으로 세팅되기 때문에 -인덱스 값을 가지고 있는 자식 요소 호랑이의 귀가 호랑이의 얼굴에 위치하게 되면서 애니매이션을 쓸 수 없게 되었습니다. 하지만 이를 해결하기 위해 HTML 마크업 구조를 변경하여 해결 하였다. 호랑이 얼굴을 담당하는 구조 밖에 만들어 봤지만 전체적인 구조를 파괴한다고 생각하여 호랑이 박스 안에 귀부분과 얼굴 부분을 따로 분리하여 마크업 진행 하였으며, 이렇게 되니 각기 다른 애니메이션을 활용할 수 있어서 만족 하였습니다.

### 4. 폰트 적용

단순히 구글 폰트를 복붙하여 사용하였지만, 이번 기회를 통해서 폰트 복사를 추가 해야하고 사용하는 언어만 기재하여 효과를 주어야 한다고 다시 한번 돌아보는 계기가 됬습니다.

### 5. background-img 활용

얼굴을 호버 하였을때 가상클래스를 활용하여 백그라운드 이미지로 처리 하였으며 전에 배운 이미지 활용 요소들을 배치하여 만족스러운 결과에 다다를수 있었습니다.

### 6. 가상클래스에 호버 이벤트 적용

.클래스 명을 기입하고 가상 요소에 호버를 적용하였으나 작동하지 않았습니다. 구글링 결과 호버의 적용은 클래스에 호버를 적용하고 그것의 가상요소를 선택하는 방식으로 작동해야 함을 알게 되었습니다.

### 7. 정렬 포지션 잡기

레이아웃 요소 중 블럭 레벨 요소와 인라인 요소를 활용하여 각 부위를 적제적소에 활용 가능한가에 대한 프로젝트라고 생각하였으며, 만족할만한 결과를 얻었습니다.


![Tiger_final](https://user-images.githubusercontent.com/85912592/162724819-18aa8596-8702-4bc4-9892-2bbaeb7cc7bc.gif)

