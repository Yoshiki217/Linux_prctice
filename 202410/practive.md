# with mongal shell script

ctrl + l : clear

## command

whoami - 로그인한 사용자 이름 표시
sudo su - root로 변경
pwd - 지금 있는 곳을 알려줌
cd (change directory) : cd 만 치면 홈 디렉토리로 돌아옴
cd .. : 위 디렉토리로 이동
set : 유저 정보 표시
printenv [set값] : set값 표시
### ls
ls -a (all)
```text
. .. 를 포함한 모든 파일을 보여줌　
```
ls -l
```text
ls의 자세한 내용 출력 （詳しい内容を出力）

출력내용　（出力内容）
-rw-r--r-- 1 root     root      3444 Jul  5  2023 adduser.conf
```

ls -il | grep .conf
```test
list 에서 .conf가 포함된 파일만 표시　（listから.confが含まれたファイルだけ表示）

| -> command 를 구분하는 역할
```

touch network_test 
```text
텅 빈 파일 생성 (空のファイル作成)
```
ifconfig | grep inet > network_test
```text
덮어쓰기
```
ifconfig | grep inet >> network_test 
```text
추가 追記
```

`alias ls="ls -l" : ls 명령어를 "ls -l"의 의미로 변경`

`unalias ls : 변경사항 삭제`

# 함수 (関数)

### function 関数名() {コマンド;}
function test() { ls -al /etc | grep .conf;}

```
create_files() {
  for letter in {a..z}; do
    touch "$letter.txt"
  done
}
```
### 関数を呼び出す
create_files

declare -f [함수이름]
```text
함수들의 정보 확인

결과창

```
