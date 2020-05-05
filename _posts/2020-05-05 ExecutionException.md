ExecutionException
---
java.util.concurrent.ExecutionException: org.apache.catalina.LifecycleException:

tomcat-api 를 jdk 에 옮겨서 해결함. 버젼 차이때문인거 같음.
db version은 다 맞춰놨고 db connector 들 다 있어서

servlet api 3.0 3.1 차이인가 싶어서 1시간 넘게 왔다갔다 하다가 
stackoverflow 찾아서 clean 후 restart 후 해결
