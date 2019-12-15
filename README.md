### 웹 클라이언트 <-> 웹 서버 통신 개요

1. 요청

성은이 노트북 (web client/ Front-end) --- (naver.com) -----> 웹 서버 (Web Server)
                                            URL 

2. 응답

성은이 노트북 (클라이언트 / Front-end) <--- (naver.com/index.html) ----- 웹 서버 (Web Server)
                                                index.html

3. 브라우저가 응답 받은 html 파일을 그려준다.

성은이 노트북의 브라우저 (크롬) index.html 받아서, 화면에 그려준다.

---

### 커맨드 라인 인터페이스 (CLI) 맛보기

#### CLI (Command Line Interface) vs. GUI (Graphical User Interface)

#### 커맨드 라인 명령어 (Command Line)

```bash
# change directory to Desktop - cd 뒤에 나온 장소로 이동해라
cd Desktop

# make folder named newfolder - newfolder라는 이름을 가진 폴더를 만들어라
mkdir newfolder

cd newfolder (newfolder로 이동해라)

touch newtext.txt (newtext라는 이름을 가진 .txt 파일을 만들어라)

vim newtext.txt (newtext.txt 파일을 vim 에디터로 열어라)

(vim 에디터가 실행된 이후)

i (insert mode 실행)

(텍스트 입력/수정 후 ese를 눌러 insert mode 종료)

:wq (write & quit - 위에서 입력/수정한 내용을 저장하고 vim 에디터를 종료하겠다) 

pwd (print working directory - 현재 나의 위치를 출력해라)

ls (list - 현재 위치한 장소 밑에 무슨 폴더, 파일이 있는지 출력해라. -a 옵션을 붙히면 숨김 파일/폴더까지 출력)

rm newtext.txt (nextext라는 이름의 txt 파일을 지워라)

cd .. (..은 현재 위치한 곳의 상위 경로를 의미한다. ex. newfolder의 상위 경로는 Desktop이다)

rm -r newfolder (newfolder라는 이름의 폴더를 지워라. -r 옵션 필수)
```

---
* 깃헙 레포를 내 노트북으로 가져오는 예제

1. github.com 사이트에서, my-first-repo라는 저장소를 만든다.
2. 1에서 만든 저장소를 CLI 환경에서 내 노트북 (혹은 다른 디바이스)으로 clone(복제)해온다.
    git clone {my-first-repo의 주소}

3. 성은이 노트북 환경에서 파일을 수정/추가한다.
git status (깃헙 사이트에 있는 내 저장소와 비교해서 변경된 상태가 있는지 알려줘)
git add . (. = 내가 수정/추가한 모든것을 add하라)
git commit -m "README.md 파일 수정"
git push origin master (수정된 사항들을 깃헙에 있는 레포에 적용)

4. 깃헙 레포의 변경된 사항을 내 노트북에 있는 파일들과 동기화
git pull origin master