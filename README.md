# JPetStore
Sample Spring MVC project for the SSD class

__주의: 먼저 우측 상단의 Fork 버튼을 클릭하여 이 리파지토리(https://github.com/cspark0/jpetstore)를 자신의 Github 계정으로 Fork(복사) 한 후 이용하기 바랍니다.__

### STS 또는 Eclipse에 import하는 방법 (local repository 생성)

1. File >> Import... >> Git - Projects from Git >> Clone URI 선택
2. fork된  URI 입력(예: https://github.com/your_Github_username/jpetstore.git), username & password 입력  
3. master branch 선택  
4. Browse 버튼을 클릭하여 local repository를 저장할 폴더 선택(예: C:\Users\사용자\git)  
5. __Project import를 위한 wizard를 선택하는 창에서 "Cancel"을 선택하여 중단__   
6. Window >> Perspective >> Open Perspective >> Other... >> Git 선택  
7. 왼쪽 repository 목록에서 jpetstore가 생성되었는지 확인하고 그 이름을 마우스 우클릭하고 메뉴에서 Imports Project... 선택
8. open된 Imports Project 창에서 Finish 선택  
9. Eclipse 우측 상단의 "Java EE" perspective 아이콘을 클릭하여 jpetstore 프로젝트가 import되었는지 확인
10. pom.xml에 등록된 library들이 모두 다운로드되고 프로젝트가 빌드 완료될 때까지 기다림   

### 프로젝트 실행 방법
1. Apache Tomcat v9.0을 다운로드 및 설치하고, Eclipse의 Servers 창에 등록함      
2. 프로젝트를 Tomcat server에 deploy(drag&drop)하고 Synchronized 상태인지 확인한 후 server를 start함
3. 프로젝트 이름을 right-click 후 Run As > Run On Server를 실행하여  웹 브라우저를 띄우고 접속함(URL을 외부의 Chrome brower 등에서 직접 입력해도 됨)
 
#### 참고: 프로젝트에 포함되어 있는 HSQL DB를 이용해서 실행하는 방법
* src/main/resources/dataAccessContext-mybatis.xml: <context:property-placeholder>의 location 속성을 "classpath:jdbc.hsqldb.properties" 로 변경
* src/main/resources/db/hsqldb 폴더에 대해 Properties 메뉴(Alt + Enter)를 실행하여 절대경로 확인 (copy)
* Windows 명령 프롬프트(cmd.exe)를 실행하고 cd 명령을 이용하여 위에서 확인한 경로로 이동 (paste)
* set 명령을 실행하여 현재 시스템에 JAVA_HOME 환경변수가 JDK 설치폴더의 경로로 설정되어 있는지 확인 (없을 경우 설정 필요)    
* server.bat 실행 (이 때 HSQL DB 서버가 실행되고 테이블과 초기 데이터들이 hsqldb/jpetstore.script에 의해 자동 생성됨)
* 주의: HSQL DB 서버가 실행되면 src/main/resources/db/hsqldb 폴더에 jpetstore.log, jpetstore.lck, jpetstore.tmp 등 임시파일이 생성되며, Eclipse에서 프로젝트 삭제, export 등이 제대로 실행되지 않음. 이를 위해서는 cmd 창에서 HSQL DB 서버를 종료하고(Ctrl+C) cmd 창도 종료해야 함


### Git 사용법 참조

* 윤웅식, 만들면서 배우는 Git+GitHub 입문, 한빛미디어, 2015.  
* 오오츠카 히로키, 소셜 코딩으로 이끄는 GitHub 실천 기술, 제이펍, 2015.  
* <https://backlog.com/git-tutorial/kr/>  
* <https://nolboo.kim/blog/2013/10/06/github-for-beginner/> 및 링크된 문서들  
* <http://itmir.tistory.com/461>  
* <http://jwgye.tistory.com/38?category=689862>  
* 그밖의 온라인 자료들  
