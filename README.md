# KPHIC

# 팀 협업용 깃허브 규칙

이 문서는 우리 팀이 **파이썬 데이터 분석 프로젝트**를 진행할 때  
팀원들이 깃허브를 처음 사용하더라도 혼란 없이 협업할 수 있도록 만든 규칙입니다.

---

## 1. 브랜치 전략

우리 프로젝트는 다음과 같은 브랜치 구조를 사용합니다.

### main 브랜치
- 최종 결과물(발표용, 제출용 등)만 저장
- 항상 안정적이고 동작하는 상태 유지
- 직접 작업하지 않고, `develop`에서 안정화된 내용을 병합하여 업데이트

### develop 브랜치
- 실제 개발이 이루어지는 기본 브랜치
- 모든 팀원은 `develop`에서 작업 시작
- 매일의 커밋, 데이터 분석, 기능 추가는 모두 `develop`에 반영

### feature 브랜치 (필요 시)
- 특정 기능, 분석, 실험 작업을 위한 임시 브랜치
- 네이밍 규칙: `feature/작업명`
  - 예시:
    - `feature/data-cleaning`
    - `feature/model-training`
- 작업 완료 후 `develop`에 병합하고 브랜치는 삭제

---

## 2. 커밋 규칙

- 형식: `[YYYY-MM-DD/작업명] 간단 설명`
- 예시:

[2025-08-20/crawl] 크롤링 함수 및 데이터 추가
[2025-08-20/visualization] 고객 데이터 분포 그래프 추가
[2025-08-20/train] 랜덤포레스트 학습 코드 추가

---

## 3. 작업 흐름

1. 브랜치 확인

git branch

현재 브랜치는 * 표시가 붙습니다.

예시:
* main
  feature/data-cleaning


브랜치 생성
git branch -m 이름


브랜치 생성 + 그 브랜치로 이동
git checkout -b 이름


브랜치 이름 변경
git branch -m 기존이름 새이름


브랜치 삭제 (develop로 이동 후 브랜치 삭제)
git checkout develop
git branch -d 이름


2. 코드 작성 / 분석

3. 커밋:

git add .
git commit -m "[2025-08-20/crawl] 크롤링 함수 및 데이터 추가"


4. 깃허브에 올리기:

git push origin 브랜치이름


5. 코드 리뷰 및 병합

6. 모든 팀원 병합 후 최신 코드 가져오기
git pull origin develop

7. 브런치 생성
git checkout -b [브런치 이름]

---

## 4. 폴더 구조

KPHIC/
data/ # 원본 및 전처리 데이터
model/ # 학습 완료 모델
notebooks/ # Jupyter Notebook
scripts/ # Python 코드
results/ # 그래프, 모델, 리포트
README.md # 프로젝트 소개

