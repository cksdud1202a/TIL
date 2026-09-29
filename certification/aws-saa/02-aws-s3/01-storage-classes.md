# [AWS] S3 스토리지 클래스

## 스토리지 클래스란
S3 스토리지 클래스는 저장소의 종류를 의미
- 필요조건에 따라 분류해서 저장해야 비용이 절감

## 스토리지 클래스 유형

### S3 Standard
자주 접근하는 파일들을 저장하는 기본 스토리지

### S3 Intelligent-Tiering
불규칙한 접근 패턴을 AWS가 자동으로 분석해 가장 비용 효율적인 계층으로 데이터를 분배

### S3 Standard-IA (Infrequent Access)
거의 접근하지 않지만, 필요 시 즉시 조회해야 하는 스토리지

### S3 One Zone-IA
S3 Standard-IA + (단일 AZ에만 저장 → 고가용성 X)

### S3 Glacier Instant Retrieval
거의 접근하지 않지만, 필요 시 즉시 조회해야 하는 스토리지

### S3 Glacier Flexible Retrieval
거의 접근하지 않고, 조회 시 최대 1시간 소요되도 괜찮을 때 쓰는 스토리지

### S3 Glacier Deep Archive
거의 접근하지 않고, 조회 시 최대 12시간 소요되도 괜찮을 때 쓰는 스토리지

## 접근 빈도에 따른 분류

### 1. 자주 접근
- S3 Standard

### 2. 거의 접근하지 않음
- S3 Standard-IA
- S3 One Zone-IA
- S3 Glacier Instant Retrieval
- S3 Glacier Flexible Retrieval
- S3 Glacier Deep Archive

### 3. 접근 빈도가 불규칙적일 때
- S3 Intelligent-Tiering

## 즉시 조회 여부

### 1. 즉시 조회 가능
- S3 Standard
- S3 Standard-IA
- S3 One Zone-IA
- S3 Glacier Instant Retrieval
- S3 Intelligent-Tiering

### 2. 조회 시 시간 소요
- S3 Glacier Flexible Retrieval
- S3 Glacier Deep Archive

## [Glacier]
Glacier 스토리지 클래스는 법/감사/규정 목적으로 장기 보관할 때 사용한다. 
이 목적이 아닌데 거의 접근하지 않는다면 S3 Glacier 유형을 쓰지 않고 S3 Standard-IA를 사용
