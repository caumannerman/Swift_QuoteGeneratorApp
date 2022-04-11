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



<p>
<img width="340" alt="스크린샷 2021-12-27 오후 4 24 45" src="https://user-images.githubusercontent.com/75043852/147446351-7e83cf64-dc6a-4074-9739-a3193d3965f0.png">
<img width="340" alt="스크린샷 2021-12-27 오후 4 24 53" src="https://user-images.githubusercontent.com/75043852/147446381-b8b2047f-1f18-40b5-8759-567e94abe1e9.png">
</p>
