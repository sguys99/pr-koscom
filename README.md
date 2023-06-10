# pr-koscom

## 실습순서

### 1. 저장소 복제하기
원격저장소를 복제하려 로컬저상소를 생성하고 저장소 내부로 진입한다.
```bash
$ git clone https://github.com/sguys99/pr-koscom.git
$ cd pr-koscom
```

### 2. 브랜치 생성하기
실습을 위한 브랜치를 `feature/<깃허브 유저네임>-practice` 라는 이름으로 만들고 전환한다.
```bash
$ git branch feature/<깃허브 유저네임>-practice
$ git checkout feature/<깃허브 유저네임>-practice
```

### 3. 실습 환경 만들고 커밋하기
`results` 디렉토리 안에 깃허브 `유저네임`으로 디렉토리를 만들고, 그 안에 실습을 진행할 `src` 폴더를 복사한다.

```bash
$ mkdir results/<깃허브 유저네임>
$ cp -r src results/<깃허브 유저네임>/src
```

초기 커밋을 진행한다.
```bash
$ git add .
$ git commit -m "initial commit"
```

### 4. 코드 수정하고 커밋하기
**중요** `results/<깃허브 유저네임>/src/pr_practice.py` 파일을 열어서, `<NAME>`과 `<EMAIL>` 부분을 본인의 정보로 수정한다.

예시
```python
print("My name is Hong gil-dong")
print("Please contact me at gd.hong@email.com")
```

수정 사항을 커밋한다.
```bash
$ git add .
$ git commit -m "Modify name and email in pr_practice.py"
```

### 5. 원격 저장소로 푸시하기
```bash
$ git push -u origin feature/<깃허브 유저네임>-practice
```

### 6. 풀 리퀘스트 생성하기
원격 저장소에서 본인이 푸시한 브랜치 이름을 찾아서, Pull Request를 생성한다.
(Assignee와 Reviewer도 지정)

### 7. Master 브랜치에 머지하기
Reviewer 승인 후 직접 Master 브랜치에 머지한다.