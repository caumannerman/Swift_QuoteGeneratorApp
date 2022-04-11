# Swift_QuoteGeneratorApp
UIKit을 이용한 SWIFT APP 예제 


## UIKit 
UI 관리, 이벤트 처리 ( 제스처, 애니메이션, 이미지 등 ..)
### => mvc패턴에서 View와 Controller(ViewController)가 너무 밀접하다!
### ===> ViewController가 거의모든 일 담당, ViewController가 View의 LifeCycle에 관여.
### ===> 즉, View와 Controller를 분리하기 어렵고, 프로젝트 규모가 커질수록 Controller가 비대해져, 유지보수가 힘들어짐.
### =====> MVVM, VIPER 패턴 등으로 MVC의 단점 해결할 수 있다 



## UIView
IOS 화면을 구성하는 기본 개체 
<img width="940" alt="" src="https://user-images.githubusercontent.com/75043852/162706935-4ff5c621-ccd4-47f7-a470-187a6cdd561e.jpeg">



## ViewController 
앱의 근간, 모든 앱은 최소한 하나 이상의 ViewController를 가지고있다. 

### => data에 따라 view 업데이트
### => view와 함께 User 이벤트에 응답
### => view 관리, 레이아웃 관리



## AutoLayout

<img width="940" alt="" src="https://user-images.githubusercontent.com/75043852/162708694-ab243031-52f0-441d-a039-f42ae91a87f4.jpeg">

### => 다양한 IPhone 크기&비율, 해상도에 대응 
### => 크기가 다른 기기에서도 똑같은 화면!
### => 세로, 가로 모두 지원 


## Outlet변수
=> storyboard에 등록한 UIObject에 접근하여 controller하기 위하여 변수에 Binding한 것.
==> Storage : Strong/Weak 은 메모리 회수 정책을 의미함 
===> Strong -> 다른 곳에서 참조하고있다면 메모리에서 제거X => 누수 가능성...
===> Weak -> 다른 곳에서 참조하고있더라도 시스템이 인위적으로 메모리에서 제거 가능

## Action 함수

Touch Down, Touch Down Repeat, Touch Up Inside, Touch Up Outside 등 여러가지 ..

## Content Huging Priority : 자신의 크기가 늘어나는 것에 저항하는 힘 
==> 우선순위가 높으면 자신의 크기 유지, 낮으면 크기가 늘어남 

==> ex) 가로 길이가 300인 UIView 내에서, 두 개의 라벨 모두 leading, top, trailing Constraint를 20으로 설정해주면, 두 라벨 사이 간격이 남게 되어 누군가는 늘어나서, leading, top, trailing Constraints를 만족시켜야한다.
이 때 무엇이 커질지 설정해주는 것이 "Hugging priority이다.

<img width="823" alt="스크린샷 2022-04-11 오후 7 43 14" src="https://user-images.githubusercontent.com/75043852/162724043-c4d2a4fc-5095-43a8-95ff-9fba055ae90b.png">
<img width="834" alt="스크린샷 2022-04-11 오후 7 43 24" src="https://user-images.githubusercontent.com/75043852/162724065-96502ac0-4fad-4d07-84c0-e7039b0b4612.png">



## Content Compression Resistance Priority : 자신의 크기가 줄어드는 것에 저항하는 힘 
==> 우선순위 높으면 자신의 크기 유지, 낮으면 크기가 줄어듦

==> ex) 위와 같은 두 개의 라벨에 매우 긴 text가 들어가게되어 공간이 부족하게 되고, 누군가가 줄어들어 top,leading, trailing constraints를 만족시켜야하는 상황에 적용

<img width="836" alt="스크린샷 2022-04-11 오후 7 47 04" src="https://user-images.githubusercontent.com/75043852/162724739-b6c57902-473e-48ca-a9a0-cf15c37f0676.png">

<img width="836" alt="스크린샷 2022-04-11 오후 7 47 21" src="https://user-images.githubusercontent.com/75043852/162724747-b81a358f-e821-423b-ab30-36242ad5b821.png">

## 이렇게 TableView 내에서 Vertical하게 배치된 Title, Content 라벨 간에, 데이터에 따른 text라벨 크기 변화에 대하여 
## 1. 공간이 남으면 ~~ 
## 2. 공간이 부족하면 ~~ 과 같이 일일이 예측 불가능한 경우들에서의 UI를 대처할 수 있게 된다. 



<p>
<img width="340" alt="스크린샷 2021-12-27 오후 4 24 45" src="https://user-images.githubusercontent.com/75043852/147446351-7e83cf64-dc6a-4074-9739-a3193d3965f0.png">
<img width="340" alt="스크린샷 2021-12-27 오후 4 24 53" src="https://user-images.githubusercontent.com/75043852/147446381-b8b2047f-1f18-40b5-8759-567e94abe1e9.png">
</p>

특이사항: 초기 앱 실행시, 명언이 생성되지 않고, '명언 생성' 버튼을 눌러야 최초의 명언이 생성되었음.
-> 따라서 viewDidAppear함수를 Override하여 "명언 생성"버튼의 IBAction click이벤트를 인위적으로 방생시켜주었다.
=> 초기 앱 실행시부터 명언이 생성되어 표시된다.

