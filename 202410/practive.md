# with mongal shell script

ctrl + l : clear

## command

whoami - 로그인한 사용자 이름 표시 (ログインしたUSERの名前表示)

sudo su - root로 변경　（root

pwd - 지금 있는 곳을 알려줌　（現在の居場所を表示）

cd (change directory) : cd 만 치면 홈 디렉토리로 돌아옴　（cdだけだとhome directoryに戻る）

cd .. : 위 디렉토리로 이동　（上のdirectoryに移動）

set : 유저 정보 표시　（USER情報表示）

printenv [set값] : set값 표시　

## ls, touch, alias
### ls -a (all)
```text
. .. 를 포함한 모든 파일을 보여줌　（. .. を含んだすべてのファイルを表示）
```
### ls -l
```text
ls의 자세한 내용 출력 （詳しい内容を出力）

출력내용　（出力内容）
-rw-r--r-- 1 root     root      3444 Jul  5  2023 adduser.conf
```

### ls -il | grep .conf
```test
list 에서 .conf가 포함된 파일만 표시　（listから.confが含まれたファイルだけ表示）

| -> command 를 구분하는 역할　（｜は、コマンドを区別する役割）
```

### touch network_test 
```text
텅 빈 파일 생성 (空のファイル作成)
```
### ifconfig | grep inet > network_test
```text
덮어쓰기　（上書き）
```
### ifconfig | grep inet >> network_test 
```text
추가 （追記）
```

### `alias ls="ls -l"` 
```text
ls 명령어를 "ls -l"의 의미로 변경　（コマンドの意味変更）
```

### `unalias ls `
```text 
변경사항 삭제（変更取り消し）
```

# 함수 (関数)

### function 関数名() {コマンド;}
### function test() { ls -al /etc | grep .conf;}
### create files() {}
```
create_files() {
  for letter in {a..z}; do
    touch "$letter.txt"
  done
}

create files
결과창

```


### declare -f [함수이름]
```textr
함수들의 정보 확인　（関数らの情報確認）

결과창
（結果）
```
