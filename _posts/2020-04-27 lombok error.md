lombok 설치 error
---
[ @Setter(onMethod_ = @Autowired) Error 
발생시

1. eclipse.ini -vm 설정
2.  lombok 버전 확인
하위 버젼이면 사용 안됨.
3. .m2에 repository 삭제하고 
 maven update > restart
4. java -jar lombok.jar
lombok.jar파일을 추가 

5. -javaagent:lombok.jar추가

>6. -Xbootclasspath/p:lombok.jar 추가
후 Restart 
maven clean(자동빌드) > update

사용 안되서 하나하나 입력하다가 결국 찾아서 사용중.

이거 다해도 안되면 **eclipse 저장 Route** lombok 이 이클립스 저장된 위치 *help > about eclipse ide*에서 확인가능하니 바른위치에 잘 저장되었는지 다시 확인해보자. 
