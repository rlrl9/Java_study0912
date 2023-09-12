# Java_study0912

작성 클래스명 : SelectEmpLab

- main() 메서드에 구현할 내용
1. DB 서버로 접속한다.
2. Random 클래스의 객체를 생성하여 true 와 false 랜덤값을 추출한다.

3. true 이면
   emp 테이블에서 모든 직원들의 이름과 월급, 두 개의 컬럼을 추출하여
   다음 형식으로 표준 출력한다.

   XXX 직원의 월급은 x,xxx달러입니다. 
   XXX 직원의 월급은 x,xxx달러입니다.
   XXX 직원의 월급은 xx,xxx달러입니다.
         :
4. false 이면
   emp 테이블에서 모든 직원들의 이름과 입사 날짜를 입사한지 오래된 순으로 추출하여
   다음 형식으로 표준 출력한다.

   XXX 직원은 xxxx년 xx월 xx일에 입사하였습니다. 
   XXX 직원은 xxxx년 xx월 xx일에 입사하였습니다. 
   XXX 직원은 xxxx년 xx월 xx일에 입사하였습니다. 
         :

작성 클래스명 : CheckEmpLab

1. DB 서버로 접속한다.
2. 검색하려는 직원의 이름을 표준입력 받는다.
3. 해당 직원의 정보를 다음과 같이 출력한다.
    (이름 비교시 대소문자 구분 없이 처리하게 한다.)

- 직원이 존재하면
   xxx 직원은 근무중입니다.
   xxxx년 xx월에 입사했고 현재 xx 번부서에서 근무하고 있습니다.

- 직원이 존재하지 않으면
   xxx 직원은 근무하지 않습니다.

4. 계속 검토하려고 하는지 프롬프트하고 종료하거나 2번부터 반복한다.


