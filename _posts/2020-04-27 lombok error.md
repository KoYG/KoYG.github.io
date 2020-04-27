lombok 설치 error
---
[ @Setter(onMethod_ = @Autowired) Error 
log랑 위에 에러 발생시

1. eclipse.ini -vm 설정
2.  lombok 버전 확인
하위 버젼이면 사용 안됨.
3. .m2에 repository 삭제하고 
 maven update > restart
4. java -jar lombok.jar
lombok.jar파일을 추가 

5. -javaagent:lombok.jar추가