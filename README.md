# Content-based Filtering Recommendation System with Amazon SageMaker MLOps

## 프로젝트 개요
이 프로젝트는 Amazon SageMaker를 활용하여 확장 가능한 Content Based / Collaborate 필터링 추천 시스템을 구축하고 MLOps 파이프라인을 구현한 것입니다. 사용자의 선호도와 아이템의 특성을 분석하여 개인화된 추천을 제공합니다.

## 시스템 아키텍처
![System Architecture](architecture_diagram.png)

### 주요 구성 요소
- **Amazon SageMaker Studio**: 데이터 분석 및 모델 개발
- **Amazon SageMaker Endpoint**: 모델 추론
- **Amazon SageMaker ModelRegistry**: 모델 형상관리
- **Amazon SageMaker PipeLines**: MLOps 파이프라인
- **Amazon SageMaker Projects**: 파이프라인 구성 및 배포
- **AWS CodePipeline**: 파이프라인 배포 자동화
- **Amazon S3**: 데이터 저장소
- **Amazon CloudWatch**: 모니터링 및 로깅

## MLOps 파이프라인
1. **데이터 수집 및 전처리**
   - 데이터 검증 및 클렌징
   - 피처 엔지니어링
   
2. **모델 학습**
   - SageMaker 학습 작업 구성
   - 하이퍼파라미터 최적화
   
3. **모델 평가 및 배포**
   - A/B 테스트
   - 모델 버전 관리
   
4. **모니터링 및 유지보수**
   - MLOps 파이프라인 구성
   - 자동화된 재학습 트리거

## 기술 스택
- Python 3.11+
- AWS SDK (Boto3)
- Amazon SageMaker SDK
- scikit-learn
- pandas
- numpy

## 시작하기

### 필수 조건
1. AWS 계정 및 적절한 IAM 권한
2. AWS CLI 설정
3. Python 환경 설정

### 설치
```bash
# Clone the repository
git clone https://github.com/username/content-based-filtering-mlops.git

# Install dependencies
pip install -r requirements.txt
```

### 환경 설정
```python
# config.py 파일 설정
AWS_REGION = 'your-region'
BUCKET_NAME = 'your-bucket-name'
```

## 사용 방법
1. 데이터 준비
```bash
python scripts/prepare_data.py
```

2. 모델 학습
```bash
python scripts/train_model.py
```

3. 모델 배포
```bash
python scripts/deploy_model.py
```

## 모니터링 및 로깅
- CloudWatch 대시보드를 통한 모니터링
- 모델 성능 메트릭스 추적
- 에러 로깅 및 알림 설정

## 프로젝트 구조
```
.
├── README.md
├── config/
├── data/
├── models/
├── notebooks/
├── scripts/
├── tests/
└── utils/
```

## 라이센스
이 프로젝트는 MIT 라이센스를 따릅니다.

## 연락처
- 이메일: khm970514@gmail.com
- 이슈 트래커: GitHub Issues

## 참고 문헌
- Amazon SageMaker 개발자 가이드