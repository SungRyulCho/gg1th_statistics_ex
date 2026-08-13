# gg1th_statistics_ex

통계 기본 개념과 Python 기반 데이터 분석을 실습하는 저장소입니다.

## Git 레포지토리 만들기

GitHub에서 `gg1th_statistics_ex` 이름의 저장소를 생성한 뒤, 로컬 프로젝트와 연결했습니다.

```bash
git init
git add .
git commit -m "통계 실습 환경 구성"
git branch -M main
git remote add origin <GitHub_저장소_URL>
git push -u origin main
```

## 가상환경 구성하기

`uv`를 사용하여 빈 Python 프로젝트와 가상환경을 생성했습니다.

```bash
uv init --bare
```

필요한 라이브러리를 설치하면 프로젝트 내부에 `.venv` 가상환경이 생성됩니다.

```bash
uv add ipykernel
```

## 주피터 노트북 사용환경 구성하기

Jupyter Notebook에서 현재 프로젝트의 가상환경을 커널로 선택할 수 있도록 등록했습니다.

```bash
uv run python -m ipykernel install --user --name eda_env --display-name "eda_env"
```

등록 후 IntelliJ IDEA에서 `.ipynb` 파일을 열고, 커널 목록에서 `eda_env`를 선택합니다.

아래 코드로 현재 Notebook이 프로젝트 가상환경을 사용하고 있는지 확인할 수 있습니다.

```python
import sys

print(sys.executable)
```

출력 경로에 아래와 비슷한 내용이 포함되면 정상입니다.

```text
.../gg1th_statistics_ex/.venv/bin/python
```
