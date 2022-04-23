개발자 티셔츠 쇼팡몰 오픈소스 SW

개발자 목록 
  논리 회로

PWM (Pulse Width Modulation) 펄스 폭 변조

듀티 사이클 : Duty Cycle => 0%, 25%, 50%, 75%, 100%

PWM을 아날로그 신호로 표현 방법

pinMode(13) : 입력 후 출력 (디지털 신호 : 사각파)

 신호 HIGH : 1000ms , LOW : 1000ms => 2000ms 주기를 나타낸다

 주기(사이클)의 절 반 => HIGT => DUTY Cycle : 50%

Analog -> dlgital

2, 양자라 과정 (Quantiediom) 0,11 ->0

1, 새플링 (sampling); bit수/ sec.

3  부호화(Encoding) 0.1로 바꾸는 작업

PWM을 지원하는 아두이노의 디지털 핀

(~3, ~5, ~6, ~9, ~10, ~11)

9600 0-255 int 확장 8ㅏㅂ이트

ADC (analog-Digital Convert)

DAC (Digital-Analog Convert)

void setup() {

	serial.begin(9600);

	pinMode(11, OUTPUT);

	pinMode(10, OUTPUT);

	pinMode(9, OUTPUT);

}

void loop() {

	int red = random(256);

	int blue = random(0, 256);

	int green = random(0, 256);

	analogWriter(11, red);

	analogWriter(10, blue);

	analogWriter(9, green);

 

	serial.print("R: ")

	serial.print(red);

	serial.print("\tB: ")

	serial.print(blue);

	serial.print("\tG: ")

	serial.print(green);

 

	delay(100);

}

가변저항  : 분압기

스케치 코드 작성

아날로그 입력 함수 : analogRead();
- 1개의 입력, 1개의 출력을 받게됨
- 입력 매개 변수는 Analog input pin No.
- 아두이노 보드  :  analog input pin
- pint No : A0 ~ A5