---
title: 'repository 생성 후 초기 세팅 git bash로 해결하기'
date: 2020-09-10
tags:
  - git
---

최초에 github을 이용하여 나만의 코드들을 저장할 저장소, repository를 github 사이트에서 생성하면 이 repository는 원격저장소(remote repository)가 됩니다.

실질적으로 코드 생성은 개인의 컴퓨터에서 하게 되는데 개인의 컴퓨터에 존재하는 repository는 로컬저장소(local repository)가 됩니다.

최초에 repository를 생성할시 사이트에 존재하는 remote repository와 개인의 컴퓨터에 존재하는 local repository를 연동해줄 필요가 있습니다.

commit 이나 pull, push 는 vscode나 atom, intelliJ와 같은 코드 편집기, 개발 환경 툴에서 코드를 생성하고 곧바로 그 환경에서 하는 것이 편하지만

처음 repository를 연동하는 것은 터미널(mac 기준)에서 하는 것이 편하고 깔끔하다고 생각이되어 git bash로 하는 편입니다.

git bash를 이용하여 두 저장소를 연동하는 방법은 다음과 같습니다.

<br>
<br>

1. 로컬저장소로 만들 파일로 위치 이동.

2. 로컬 저장소로 설정 (한번 설정하면 끝)

```
git init
```

3. 파일들을 staging area || index로 이동

```
git add . || file_name
```

. 은 전부를 추가하고 file_name을 써주면 해당 file만 추가됩니다.

4. staging area 의 파일들을 로컬 저장소에 저장

```
git commit -m “”
```

""안에 간략한 commit message를 입력

5. 로컬저장소와 원격저장소 연결 (처음에만 연결해주면 됨)

```
git remote add origin [원격저장소주소]
```

6. 원격저장소에 저장

```
git push -u origin master
```

Local repository check

```
git status
```

6번까지의 과정을 마쳐 저장소 연동이 끝나면 그 뒤로는 3(add),4(commit),6(push)의 과정만을 반복하여 로컬 저장소에서 수정,제거,추가한 코드들을 원격저장소에 저장하면 됩니다.
