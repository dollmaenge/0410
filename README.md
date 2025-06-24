# 0410

파일 입출력
외부->자바 : Input
자바->외부 : Output

바이트기반의 스트림(~Stream)
Input Stream -> FileInputStream
ㄴ공통필드     ㄴfilterInputStream
ㄴ메서드       ㄴByteInputStream

int read() : 한번에 1byte씩 읽어서반환
int read(byte[] b) : 읽어와서 바이트 배열에 넣는다.

OutputStream -> FileOutpuStream
ㄴint write(int b) : 1byte 를출력
ㄴint write(byte[] b) : 매개변수로 주어진 배열의 모든 바이트를 출력

문자열.getByte(bytr[] b) : 문자열을 바이트 배열로 변환

문자 기반의 스트임(~Reader, ~Writer)
Reader -> FileReader

FileReader는 기본적으로 운영체제의 기본문자 인코딩을 사용을 해서 파일을 읽는다.
그래서 한글을 별도의 처리없이 읽을 수 있다.

Writer -> FileWriter
ㄴwrite()
문자열을 직접 전달해도 쓰는것이 가능하다

인코딩 : 컴퓨터가 문자를 숫자로 바꾸는 규칙
UTF-8 : 전세계문자를 지원, 한글은 3바티으
EUC-KR : 한글전용

보조 스트림 변수명 = new 보조 스트림(기반 스트림);

바이트 기반 보조스트림

BufferedInputStream : 읽어오는것
BufferedOutputStream : 쓰는것

보조스트림으로 파일 복사하기
BufferedInputStream(FileInputStream)
BufferedOutputStream(FileOutputStream)



---------------------------------------
요일 열거형 만들기
Weekday 라는 열거형을 정의하고, 요일 이름을 상수로 넣는다.

메인 메서드에서 오늘요일이 SUNDAY면 "쉬는날입니다"출력
그외에는 "출근하는 날입니다" 를 출력해라

---------------------------------------

Operation 열거형을 정의하고
추상메서드 apply(int x, int y)를 갖고있다.
PLUS,MINUS,MULTI,DIV상수를 가지고 있습니다.
main메서드 에서 모든 연산을 수행하여 출력하세요

---------------------------------------
OrderStatus열거형을 만들고
ORDERED, SHEPPED, DELIVERED 상수를 정의한다.
온라인 쇼핑몰의 주문상태를 관리하는 시스템을 만들고자 한다.
상태에 따라 다음상태로 바뀐다
각 상태에서 next()메서드를 호출하면 다음상태로 전환되도록 구현하기

ORDERED -> SHEPPED
SHEPPED -> DELIVERED
DELIVERED -> "완료 상태이며 상태전환불가"

OrderStatus status = OrderStatus.ORDERED;
status = status.next(); //SHEPPED
status = status.next(); //DELIVERED
status = status.next(); //예외발생












