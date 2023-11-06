## 구현 요구사항 정리
### 1. 로또 실제 구현되는 클래스 생성 : LottoController
* Application 클래스에 LottoController 생성 : 
  * LottoController.begin()
* lottoController.play() 실행
  * 실제로 로또게임 구현 메서드 : play()
    * 로또 금액 입력 : InputView.showMoney()
      * 입력 받은 로또 금액을 LottoMoney의 inputMoney에 넣어줌.
      * 입력 받은 로또 급액을 1000으로 나눈 몫을 LottoMoney의 count에 넣어줌.
    * 로또 번호 발행 : lottoMoney.setNumbers()
      * getRandomLotto() : 
        * Randoms.pickUniqueNumbersInRange()를 이용해 6개의 임의의 수를 리스트로 받음.
        * sort()를 이용하여 정렬 시켜준 뒤 리스트 반환.
    * 로또 번호 출력 : InputView.viewNumber()
      * 이렇게 받은 리스트를 돌면서 한 줄의 당첨 번호들을 출력.
    * 로또 당첨 번호 입력 : InputView.insertLottoNum()
      * validateLottoNum() :
        * oneToFourFive() : 1부터 45사이의 숫자인지 검증
        * isExisted() : 중복 된 수인지 검증.
          * Lotto 클래스에 작성
      * numToList() : 
        * 입력한 당첨번호 String을 리스트로 변환해줌.
    * 로또 보너스 번호 입력 : InputView.insertBonusNum()
      * 보너스 번호 입력
      * validateBonusNum() : 
        * 1에서 45사이의 수인지와 중복된 수인지 검증.

