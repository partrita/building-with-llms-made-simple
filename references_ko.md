# LLM으로 빌드하기: 참고 자료

## 다중 에이전트 시스템

- [우리의 다중 에이전트 연구 시스템 구축 방법](https://www.anthropic.com/engineering/built-multi-agent-research-system) - Anthropic이 자신들의 다중 에이전트 연구 시스템 구현에 대해 상세히 설명하며, 아키텍처, 과제 및 실제 적용 사례를 다룹니다.
- [다중 에이전트를 만들지 마세요](https://cognition.ai/blog/dont-build-multi-agents) - 다중 에이전트 아키텍처에 대한 비판적 분석으로, 컨텍스트 공유 문제와 상충되는 의사 결정으로 인해 시스템이 취약해진다고 주장하며, 더 신뢰성 있는 단일 스레드 에이전트 구축 원칙을 제시합니다.
- [AI 에이전트 만들기를 멈추세요](https://decodingml.substack.com/p/stop-building-ai-agents) - Hugo Bowne-Anderson의 실용 가이드로, 에이전트가 과대평가되고 남용되고 있다고 주장하며, 대부분의 문제를 복잡한 에이전트 시스템보다 더 효과적으로 해결하는 5가지 대안 워크플로우 패턴(프롬프트 체이닝, 병렬화, 라우팅, 오케스트레이터-워커, 평가자-최적화기)을 제시합니다.

## RAG (검색 증강 생성)

- [RAG 애플리케이션 개선 방법: 6가지 입증된 전략](https://jxnl.co/writing/2024/11/04/how-to-improve-rag-applications-6-proven-strategies/) - 합성 테스트부터 쿼리 라우팅 및 사용자 피드백 수집에 이르기까지 RAG 시스템 개선을 위한 6가지 핵심 전략을 다루는 실용 가이드입니다.
- [Jason Liu의 RAG 기사 모음](https://jxnl.co/writing/category/rag/) - RAG의 기본, 구현 전략, 평가 방법 및 미래 예측을 다루는 포괄적인 기사 모음입니다.

## 평가 방법

- [LLM 평가 FAQ](https://hamel.dev/blog/posts/evals-faq/) - RAG 평가, 모델 선택, 주석 도구 및 합성 데이터 생성에 대한 모범 사례를 다루는 LLM 애플리케이션 평가에 대한 포괄적인 가이드입니다.
- [RAG 평가는 6가지뿐입니다](https://jxnl.co/writing/2025/05/19/there-are-only-6-rag-evals/) - 질문, 컨텍스트, 답변 간의 6가지 핵심 관계를 기반으로 RAG 시스템을 평가하기 위한 체계적인 프레임워크입니다.
- [장문 컨텍스트 질의응답 시스템 평가](https://eugeneyan.com/writing/qa-evals/) - 긴 문서가 포함된 Q&A 시스템 평가에 대한 포괄적인 가이드로, 충실도 대 유용성 메트릭, 데이터셋 구성, 평가 방법, 서술, 기술 및 다중 문서 시나리오에 대한 벤치마크를 다룹니다.
- [Jacky Liang의 트위터](https://x.com/jjackyliang/status/1932817119189643699) - 실제 테스트 전략과 평가 설계의 일반적인 함정에 초점을 맞춰 LLM 평가에 대한 실용적인 접근 방식을 논의하는 간결한 스레드입니다.
- [LLM 기반 자동 평가로 고객 지원 챗봇 개발 가속화](https://tech.instacart.com/turbocharging-customer-support-chatbot-development-with-llm-based-automated-evaluation-6a269aae56b2) - Instacart의 LACE(LLM 지원 챗봇 평가) 프레임워크에 대한 상세한 사례 연구로, 평가 기준 설계, 에이전트 평가 방법(성찰 및 토론), 인간-정렬 검증 및 지속적인 챗봇 개선을 위한 프로덕션 구현을 다룹니다.

## 프로덕션 모범 사례

- [AI 제품을 빠르게 개선하기 위한 현장 가이드](https://hamel.dev/blog/posts/field-guide/) - 오류 분석, 데이터 뷰어, 도메인 전문가 협업, 합성 데이터, 평가 신뢰 및 실험 기반 로드맵을 다루는 포괄적인 가이드입니다.
- [프로덕션 환경의 LLMOps: 실제로 작동하는 287가지 추가 사례 연구](https://www.zenml.io/blog/llmops-in-production-287-more-case-studies-of-what-actually-works) - 287개의 실제 LLM 프로덕션 배포에 대한 포괄적인 분석으로, 에이전트 시스템, 평가 인프라, RAG 아키텍처 및 데이터 플라이휠의 주요 동향을 다룹니다. 이 선별된 컬렉션은 다양한 산업 및 사용 사례에서 실제로 작동하는 것에 대한 귀중한 통찰력을 제공합니다.

## 보안 및 안전

- [안전한 AI 에이전트에 대한 Google의 접근 방식 소개](https://research.google/pubs/an-introduction-to-googles-approach-for-secure-ai-agents/) - Google의 안전한 AI 에이전트 프레임워크로, 기존 보안 제어와 동적 추론 기반 방어를 결합한 하이브리드 심층 방어 전략을 강조합니다.
- [프롬프트 주입으로부터 LLM 에이전트를 보호하기 위한 디자인 패턴](https://arxiv.org/html/2506.08837v2) - 프롬프트 주입 공격에 대해 입증 가능한 저항성을 가진 AI 에이전트 구축을 위한 디자인 패턴 및 모범 사례에 대한 포괄적인 연구입니다.
- [AI 에이전트의 치명적인 삼중고](https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/) - AI 에이전트에서 데이터 유출로 이어질 수 있는 세 가지 위험한 기능(개인 데이터 접근, 신뢰할 수 없는 콘텐츠 노출, 외부 통신)에 대한 비판적 분석입니다.

## AI 기능 및 한계

- [자기 개선의 환상: AI가 천재로 가는 길을 생각할 수 없는 이유](https://medium.com/@vishalmisra/the-illusion-of-self-improvement-why-ai-cant-think-its-way-to-genius-a355ef3e9fd5) - 진정한 자기 개선을 달성하는 데 있어 AI 시스템의 근본적인 한계와 AI가 초지능으로 가는 길을 생각할 수 있다는 오해에 대한 통찰력 있는 분석입니다.

## 프레임워크 및 아키텍처

- [GenAI 시스템의 숨겨진 단순성](https://docs.google.com/presentation/d/1qUh3snfpXj0CAf8dOlPnc8lM-z4uautEP7pqYAIIlNM/edit?usp=sharing) - Hugo Bowne-Anderson과 John Berryman이 주최한 Maven Lightning Lesson의 슬라이드 덱으로, LLM 애플리케이션에 대해 생각할 수 있는 훌륭한 프레임워크를 제공합니다.
- [PocketFlow](https://github.com/The-Pocket/PocketFlow/tree/main) - 에이전트, 워크플로우, RAG 등을 지원하는 미니멀리스트 100줄 LLM 프레임워크로, 종속성 및 공급업체 종속이 없습니다. 에이전트 코딩 기능을 갖추고 있으며 LLM 애플리케이션 구축을 위한 광범위한 쿡북 예제를 포함하여 최소한의 코드로 복잡한 AI 시스템을 만드는 방법을 보여줍니다.

## 임베딩 및 벡터 공간

- [임베딩의 보편적 기하학 활용](https://arxiv.org/html/2505.12540v2) - 쌍을 이루는 데이터 없이 다른 벡터 공간 간에 텍스트 임베딩을 변환하는 방법을 보여주는 획기적인 연구로, 벡터 데이터베이스 보안 및 정보 추출에 중요한 영향을 미칩니다.

## 문서 처리 및 다중 모드 모델

- [SmolDocling-256M-preview](https://huggingface.co/ds4sd/SmolDocling-256M-preview) - OCR, 레이아웃 보존, 코드 인식 및 표, 차트, 수식과 같은 다양한 문서 요소를 지원하는 종단 간 문서 변환을 위한 초소형 비전-언어 모델입니다.

## 비디오 리소스

- [오류 분석: AI 엔지니어링에서 가장 높은 ROI 기술](https://www.youtube.com/watch?v=e2i6JbU2R-s) - Hamel Husain이 AI 애플리케이션에 대한 오류 분석 수행 가이드를 통해 LLM 시스템 개선을 위한 기본 평가 기술을 시연합니다.
- [Andrej Karpathy: 소프트웨어가 다시 바뀌고 있습니다](https://www.youtube.com/watch?v=LCEmiRjPEtQ) - Andrej Karpathy의 기조 연설로, 자연어가 새로운 프로그래밍 인터페이스가 되고 LLM이 유틸리티, 팹 및 운영 체제 역할을 하는 '소프트웨어 3.0' 시대로의 소프트웨어 진화를 탐구합니다.
- [12-Factor 에이전트: 신뢰할 수 있는 LLM 애플리케이션의 패턴](https://www.youtube.com/watch?v=8kMaTybvDUw) - Dex Horthy가 기존 소프트웨어 엔지니어링 원칙을 AI 에이전트에 적용하여 신뢰할 수 있는 LLM 기반 애플리케이션을 구축하기 위한 12가지 핵심 엔지니어링 원칙에 대해 발표합니다.

## LLM 도구 및 자동화

- [도구: 코드가 전부입니다](https://lucumr.pocoo.org/2025/7/3/tools/) - Armin Ronacher의 2025년 블로그 게시물은 모델 컨텍스트 프로토콜(MCP) 및 MCP 서버를 비판적으로 검토하고 구성 가능성 및 컨텍스트 요구 사항의 한계를 강조합니다. 이 게시물은 코드 중심 자동화가 MCP에 의존하는 것보다 더 효율적이고 신뢰할 수 있으며 검증 가능하다고 주장하며, 대부분의 자동화 및 에이전트 코딩 작업에 코드 생성이 여전히 선호되는 이유에 대한 실용적인 통찰력을 제공합니다.

## 도구, 라이브러리 및 자동화

- [Minish Lab](https://minishlab.github.io/) - Model2Vec 및 Potion을 포함한 초고속 NLP 도구 및 모델에 중점을 둔 오픈 소스 회사입니다. Potion은 작고 매우 빠른 임베딩 모델이며, 효율적인 텍스트 처리 및 검색을 위해 llamabot의 기본 빠른 임베더로 사용됩니다.

## 강연 및 컨퍼런스 세션

- [개념 증명 연옥 탈출: 강력한 LLM 기반 애플리케이션 구축 (SciPy 2025)](https://cfp.scipy.org/scipy2025/talk/GJRGVU/) - 이 강연은 LLM 소프트웨어 개발 수명 주기(SDLC)를 소개하고 LLM 프로젝트를 초기 데모 단계를 넘어 이동시키기 위한 구조화된 프레임워크를 제공합니다. LLM을 과학적 파이썬 워크플로우에 통합하고, 비결정성을 처리하고, 구조화된 출력을 추출하고, 신뢰할 수 있는 프로덕션 준비 AI 시스템을 구축하기 위한 전략에 대한 모범 사례를 다룹니다.
