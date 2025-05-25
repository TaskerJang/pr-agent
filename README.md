# 🚀 PR-Agent: AI 기반 Pull Request 자동화 도구

## 🎯 소개
2025 오픈소스 컨트리뷰션 아카데미(OSSCA) 체험형 프로젝트로, Qodo에서 개발한 AI 기반 Pull Request 자동화 도구에 테스트 및 문서화 기여를 수행했습니다.

### ⏰ 프로젝트 기간
- **전체**: 2025.3.6 - 2025.5.27 (6주)
- **Git 심화 과정**: 2025.4.14 - 2025.4.27
- **오픈소스 심화 멘토링**: 2025.4.28 - 2025.5.27

## 💻 기술 스택
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-009639?style=for-the-badge&logo=pytest&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AI](https://img.shields.io/badge/AI/ML-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)

## 🔧 구현 내용

### 1. PR-Agent 핵심 기능 분석
#### 주요 명령어
- **/describe**: PR에 대한 자동 설명 생성 및 라벨링
- **/review**: 코드 리뷰 및 보안 취약점 분석
- **/improve**: 코드 개선 제안 및 최적화 방안 제시
- **/ask**: 특정 질문에 대한 AI 기반 답변 제공

#### 프롬프트 엔지니어링 분석
```python
# AI 모델에게 전달되는 프롬프트 구조 분석
def analyze_prompt_structure():
    """
    - 효과적인 결과를 위한 프롬프트 최적화
    - 컨텍스트 제한과 토큰 관리 전략
    - 다양한 유형의 PR에서 성능 테스트
    """
```

### 2. 단위 테스트 및 문서화 구현

#### 핵심 기여 사항
```python
def test_clip_tokens_comprehensive():
    """
    21개의 포괄적인 테스트 케이스 구현:
    - 엣지 케이스 검증
    - 에러 케이스 처리
    - Unicode 문자 처리
    - 매개변수 조합 테스트
    """
    
def clip_tokens(text: str, max_tokens: int, factor: float = 0.9) -> str:
    """
    완전한 함수 문서화:
    
    Args:
        text (str): 클리핑할 텍스트
        max_tokens (int): 최대 토큰 수
        factor (float): 안전 계수 (기본값: 0.9)
        
    Returns:
        str: 클리핑된 텍스트
        
    Examples:
        >>> clip_tokens("Hello world", 5)
        "Hello"
    """
```

#### 테스트 커버리지
1. **기본 기능 테스트**
   - 정상적인 텍스트 클리핑
   - 빈 문자열 처리
   - None 값 처리

2. **엣지 케이스 테스트**
   - 매우 긴 텍스트 처리
   - 특수 문자 포함 텍스트
   - Unicode 문자 처리

3. **매개변수 검증**
   - 다양한 factor 값 테스트
   - 경계값 테스트
   - 잘못된 매개변수 처리

### 3. 메인테이너와의 협업 경험
```python
# Python 베스트 프랙티스 적용
def test_empty_input_text(self):
    """Test that empty input returns empty string."""
    assert clip_tokens("", 10) == ""
    # 개선: == None → is None
    assert clip_tokens(None, 10) is None  # mrT23님 피드백 반영
```

## 📦 프로젝트 설정

### 개발 환경 구축
```bash
# 저장소 포크 및 클론
git clone https://github.com/TaskerJang/pr-agent.git
cd pr-agent

# 가상환경 생성
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 의존성 설치
pip install -r requirements.txt
```

### 테스트 실행
```bash
# 단위 테스트 실행
pytest tests/unittest/test_clip_tokens.py -v

# 전체 테스트 실행
pytest tests/ -v

# 커버리지 확인
pytest --cov=pr_agent tests/
```

## 🏗 개인 기여 영역

### 전문 분야
```
TaskerJang 기여 영역/
├── 테스트 엔지니어링/        # 21개 포괄적 단위 테스트 작성
├── 기술 문서화/              # 완전한 함수 문서화 구현  
├── 코드 품질 개선/           # Python 베스트 프랙티스 적용
├── 학습 기록 및 공유/        # 10편 블로그 포스팅
└── 오픈소스 기여 프로세스/   # Fork부터 PR까지 완전 정복
```

## 📚 기술 문서

<details>
<summary><b>PR-Agent 분석 시리즈</b></summary>

1. [PR-Agent 기본 설정 및 사용법 분석](https://velog.io/@tasker_dev/PR-Agent-기본-설정-및-사용법-분석)
2. [PR-Agent의 describe 명령어 분석](https://velog.io/@tasker_dev/PR-Agent의-describe-명령어-분석)
3. [PR-Agent의 describe 명령어 프롬프트 분석](https://velog.io/@tasker_dev/PR-Agent의-describe-명령어-프롬프트-분석)
4. [PR-Agent Review 기능 분석](https://velog.io/@tasker_dev/PR-Agent-Review-기능-분석)
5. [PR-Agent Improve 기능 분석](https://velog.io/@tasker_dev/PR-Agent-Improve-기능-분석)
6. [PR-Agent 실습](https://velog.io/@tasker_dev/PR-Agent-실습)

</details>

<details>
<summary><b>오픈소스 기여 가이드</b></summary>

1. [PR-Agent 오픈소스의 주요 이슈와 개선 방향](https://velog.io/@tasker_dev/PR-Agent-오픈소스의-주요-이슈와-개선-방향)
2. [PR-Agent algo 폴더 리팩토링을 통한 오픈소스 기여하기](https://velog.io/@tasker_dev/PR-Agent-algo-폴더-리팩토링을-통한-오픈소스-기여하기)
3. [오픈소스 기여하기 Fork부터 PR까지 완전 정복](https://velog.io/@tasker_dev/오픈소스-기여하기-Fork부터-PR까지-완전-정복)

</details>

<details>
<summary><b>심층 분석</b></summary>

- [Qodo Merge(PR-Agent) AI 기반 Pull Request 협업 도구 심층 분석](https://velog.io/@tasker_dev/Qodo-MergePR-Agent-AI-기반-Pull-Request-협업-도구-심층-분석)

</details>

## 🎉 프로젝트 성과

<div align="center">
  
### 🚀 Pull Requests

</div>

<table>
<tr>
<td width="100%">
<div align="center">
  
[![PR](https://img.shields.io/badge/PR-1816-brightgreen?style=for-the-badge&logo=github)](https://github.com/qodo-ai/pr-agent/pull/1816)
[![Status](https://img.shields.io/badge/Status-MERGED-success?style=for-the-badge)](https://github.com/qodo-ai/pr-agent/pull/1816)

</div>

### 📋 단위 테스트 및 문서화 구현

> utils.py clip_tokens 함수에 21개의 포괄적인 단위 테스트와 완전한 문서화를 추가했습니다.

**주요 구현 사항**
- ✨ 21개 종합 테스트 케이스
- 📚 완전한 함수 문서화
- 🔍 엣지 케이스 및 에러 처리
- 🌐 Unicode 문자 지원
- ✅ 100% 하위 호환성 유지

**메인테이너 피드백**
- 💬 "Thanks @TaskerJang" - mrT23님
- 🔧 Python 베스트 프랙티스 적용 (`== None` → `is None`)
- ⚡ 코드 품질 개선 제안 즉시 수용 및 반영
- 🤝 실제 오픈소스 커뮤니티 협업 경험

</td>
</tr>
</table>

### 📊 개인 기여 성과

<div align="center">

| 기여 영역 | 세부 내용 | 성과 |
|-----------|-----------|------|
| **단위 테스트** | 21개 포괄적 테스트 케이스 | ✅ **완료** |
| **함수 문서화** | 완전한 docstring 및 사용 예제 | ✅ **완료** |
| **코드 품질** | Python 베스트 프랙티스 적용 | ✅ **완료** |
| **학습 기록** | 10편 기술 블로그 포스팅 | ✅ **완료** |
| **PR 성공** | PR #1816 MERGED | ✅ **성공** |

</div>

**핵심 성과**
- 🔥 **PR #1816 MERGED**: utils.py clip_tokens 함수 개선
- 📚 **완전한 문서화**: 개발자 경험 향상을 위한 상세 가이드
- 🧪 **21개 테스트 케이스**: 모든 시나리오 검증 및 안정성 확보
- 📝 **10편 블로그**: 체계적 학습 과정 기록 및 지식 공유

## 📖 전체 활동 후기

<div align="center">
  
[![Velog](https://img.shields.io/badge/Velog-2025_PR_Agent_체험형-20C997?style=for-the-badge&logo=velog&logoColor=white)](https://velog.io/@tasker_dev/2025-오픈소스-컨트리뷰션-아카데미-체험형-PR-Agent-프로젝트-후기)

**6주간의 열정적인 AI 오픈소스 기여 여정을 기술 블로그에서 확인해보세요!**

</div>

### 🏆 주요 성과 및 배운 점

- **실제 MERGE 성공의 성취감**: 전 세계 개발자들이 사용하는 AI 도구에 실질적 기여
- **메인테이너와의 직접 소통**: 진정한 오픈소스 커뮤니티 문화 체험  
- **체계적인 테스트 엔지니어링**: 21개 테스트 케이스를 통한 완벽한 품질 검증
- **완전한 문서화 구현**: 개발자 경험 향상을 위한 상세한 API 문서 작성
- **지속적인 학습 기록**: 10편의 블로그 포스팅을 통한 지식 공유 및 기여 과정 문서화

## 🔗 참고 자료

<table>
<tr>
<td><a href="https://github.com/qodo-ai/pr-agent">🤖 PR-Agent 원본 저장소</a></td>
<td><a href="https://www.qodo.ai/">🏢 Qodo 공식 사이트</a></td>
<td><a href="https://docs.qodo.ai/">📚 Qodo Merge 문서</a></td>
</tr>
<tr>
<td><a href="https://openai.com/api/">🔑 OpenAI API</a></td>
<td><a href="https://pytest.org/">🧪 pytest 문서</a></td>
<td><a href="https://python.org/">🐍 Python 공식 문서</a></td>
</tr>
</table>

