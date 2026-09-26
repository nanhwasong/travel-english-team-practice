# 여행영어 앱 Firestore 데이터 설계

## 1. users
사용자 기본정보
- 문서 ID: 로그인한 사용자의 uid
- name: 사용자 이름
- email: 이메일
- createdAt: 가입 날짜

## 2. trips
사용자가 입력한 여행 일정
- 문서 ID: 자동 생성
- userId: 여행을 만든 사용자 uid
- city: 여행 도시
- startDate: 출발일
- endDate: 귀국일
- dailySentenceGoal: 하루 학습 문장 수
- createdAt: 등록 날짜

## 3. sentences
AI가 생성한 여행영어 문장
- 문서 ID: 자동 생성
- tripId: 연결된 여행 ID
- placeName: 사용할 장소
- english: 영어 문장
- korean: 한국어 뜻
- situation: 사용 상황
- audioUrl: 발음 음성 주소
- createdAt: 생성 날짜

## 4. progress
문장별 학습 결과
- 문서 ID: 자동 생성
- userId: 학습한 사용자 uid
- sentenceId: 학습한 문장 ID
- status: learning 또는 completed
- correctCount: 맞힌 횟수
- wrongCount: 틀린 횟수
- lastStudiedAt: 마지막 학습 날짜