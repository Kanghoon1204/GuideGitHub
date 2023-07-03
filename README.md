# GuideGitHub

README.md 파일은 이 레퍼지토리가 어떤 레퍼지토리인지를 설명하는 것으로 시작합니다.
코드 정렬 : Control + Alt + L

GIT HUB 사용법을 정리합니다.

도움이 되는 영상 주소

https://www.youtube.com/watch?v=lelVripbt2M (짧은 영상)

[https://www.youtube.com/watch?v=-27WScuoKQs](https://www.youtube.com/watch?v=1I3hMwQU6GU) (긴 영상)

기본적으로 터미널 명령어를 통해 사용

# 1. 내 컴퓨터에서 인터넷으로 올리기 위해서는 [git]이라는 것을 설치해 줘야한다. 

# 2. git에대한 세팅을 해주여야한다.

   1. Git Bash에 접속
   2. git config --global user.name "나의 이름"
   3. git config --global user.email "나의 이메일" (깃허브 가입 이메일)
   4. git config --list 를 통해서 잘 연결되어있는지 확인한다. (name과 email이 잘 되었는지 확인)

# 3. 나의 코드를 깃허브에 올리는법.

    1. 올릴 파일의 터미널에 접속
    2. git init
    3. git add . (폴더 내부에 있는 전부를 다 올리겠다는 의미)
    4. git status (뭐가 add되었는지 확인)
    5. git commit -m "커밋 메시지" (github에 올라 갈 히스토리를 생성한다.)
    6. git remote add origin 내 레퍼지토리 주소 (내 프로젝트와 내 레퍼지토리의 연결고리를 만들어준다.)
    7. git remote -v 를 통해 확인
    8. git push origin master (master branch를 내 소스 코드 및 파일들을 전송한다.)
    
    ★ 내가 코드를 로컬에서 수정했다면 수정된 코드를 git에 갱신 해야 할 필요가 있을 때,
    
    1. git add .
    2. git status -> 변화가 생긴 것을 감지
    3. git commit -m "커밋 메시지2" (새로운 히스토리 생성)
    4. git push origin master (갱신) -> history를 클릭하면 그 변화를 볼 수 있다.
    
# 4. 나의 코드를 깃허브에서 가져오는 법.
    
    1. 폴더 내 터미널 접속
    2. git clone [가져올 레퍼지토리 주소.] [생성 할 폴더 이름]
    
# 5. 코드를 통해 협업하는 법.

    1. ★3의 방법으로 하면 안된다.★
    2. git checkout -b [생성 할 새로운 브렌치 : A]
    3. git push origin A (A라는 브렌치에 내가 새롭게 작성한 코드 및 프로젝트가 보내짐)
    4. GitHub 홈페이지에서 [pull request] 버튼을 클릭  (merge를 요청하는 작업)
    5. 잘 확인하고, [Merge pull request] 버튼을 클릭 (코드를 합치는 작업을 한다.)

    ★ 최종 소스코드와 내가 작성 중인 코드가 너무 다른 상황 [동기화가 되지 못함]
    
    1. git add.
    2. git commit -m "저장한 코드" (내가 지금까지 작성한 코드는 어딘가 남겨놔야 한다.)
    3. git pull origin master (마스터 브랜치로부터 새로운 코드를 받아오는 동기화 작업을 한다.)
    4. git push origin master (합쳐진 코드를 다시 마스터로 보낼 수 있다.)
    

# 6. 프로젝트를 과거의 것으로 되돌리는 방식.

    1. Reset (이전의 행적을 정산) , Revert (이전의 행적을 남김.)
    2. git log -> commit 메시지가 등장한다. (HASH를 알아내는 과정)
    3. git reset --hard [복사한 내용]
    
    ★ Reset를 복원하려면, 백업파일을 불러 옴 (.git파일)
    1. git reset --hard (HASH가 없으면 마지막 파일로 돌아감)

    1. git revert [복사한 내용]
    2. :wq 를 입력. (이전의 변화가 사라진다.)

# 7. Branch를 생성하기
https://inpa.tistory.com/entry/GIT-%E2%9A%A1%EF%B8%8F-%EA%B9%83-Branch-%EC%A0%95%EB%A6%AC-branch-checkout-merge-rebase 정리가 잘 된 블로
  git branch -a를 통해 리스트를 확인한다.
    1. git swich [이동 할 브렌치]
    2. git swich -c [이동하면서 생성 할 브렌치]
    3. git brach -d(D) [브렌치 명] (대문자로 사용시 강제 삭제)
    4. git branch -m [기존 브렌치 명] to [새 브렌치 명]

    프로젝트는 한 폴더에 있지만 브랜치가 어디냐에 따라서 내용이 달라진다.
    
