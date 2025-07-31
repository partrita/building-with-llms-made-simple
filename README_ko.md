# LLM을 활용한 간단한 프로그램 만들기

LLM을 활용하여 파이썬 프로그램을 만드는 방법에 대한 튜토리얼입니다.

Eric J. Ma (@ericmjl)가 ❤️로 만들었습니다.

## 설치 안내

이 튜토리얼을 위해서는 몇 가지 구성 요소를 설치해야 합니다:

### 0. Pixi 설치

Pixi는 의존성 관리에 사용할 패키지 관리 도구입니다. 다음 방법 중 하나를 사용하여 설치하십시오:

**리눅스 및 macOS** (curl 사용):

```bash
curl -fsSL https://pixi.sh/install.sh | bash
```

**윈도우** (PowerShell 사용):

```powershell
iwr -useb https://pixi.sh/install.ps1 | iex
```

설치 후 변경 사항을 적용하려면 터미널을 다시 시작해야 할 수 있습니다.

### 1. Ollama 설치

이 튜토리얼에서 사용되는 로컬 LLM 모델을 실행하려면 Ollama가 필요합니다.

- **리눅스**: [https://ollama.com/download/linux](https://ollama.com/download/linux) 방문
- **macOS**: [https://ollama.com/download/mac](https://ollama.com/download/mac) 방문
- **윈도우**: [https://ollama.com/download/windows](https://ollama.com/download/windows) 방문

플랫폼에 맞는 설치 지침을 따르십시오.

### 2. 설치 스크립트 실행

Ollama를 설치한 후 다음 명령을 실행하여 다음을 수행하십시오:

- 필요한 LLM 모델 가져오기
- uv (파이썬 패키지 관리자) 설치
- 가상 환경 설정
- 모든 필수 의존성 설치

```bash
pixi run start
```

이 명령은 다음을 수행합니다:

1. 다음 Ollama 모델을 가져옵니다:
   - `llama3.2`
   - `phi4`
   - `gemma2:2b`
2. uv가 아직 설치되지 않은 경우 설치합니다.
3. 파이썬 가상 환경을 만듭니다.
4. 모든 필수 의존성을 설치합니다.

> 다운로드에 시간이 걸릴 수 있으므로 튜토리얼 세션에 도착하기 전에 이 작업을 수행하십시오!

### 3. 노트북 실행

설치가 완료되면 다음을 사용하여 노트북을 실행할 수 있습니다:

```bash
# 첫 번째 노트북 실행
uvx marimo edit --sandbox notebooks/01_simple_bot.py

# 또는 두 번째 노트북 실행
uvx marimo edit --sandbox notebooks/02_structured_bot.py
```

## 수동 설치 (대안)

구성 요소를 수동으로 설치하려면:

1. [https://ollama.com/download](https://ollama.com/download)에서 Ollama를 설치합니다.

2. 필요한 모델을 가져옵니다:

   ```bash
   ollama pull llama3.2
   ollama pull phi4
   ollama pull gemma2:2b
   ```

3. uv를 설치합니다:

   ```bash
   curl -fsSL https://astral.sh/uv/install.sh | bash
   ```

   설치 가이드는 여기에 있으며 윈도우 설치 지침도 포함되어 있습니다: https://docs.astral.sh/uv/getting-started/installation/

4. 노트북을 실행합니다:

   ```bash
   cd notebooks/ # 매우 중요합니다!
   uvx marimo edit --sandbox 01_simple_bot.py # 또는 다른 노트북
   ```

## 문제 해결

- **Ollama 모델 다운로드 문제**: 모델 다운로드에 문제가 발생하면 안정적인 인터넷 연결과 충분한 디스크 공간이 있는지 확인하십시오.
- **uv 설치 문제**: uv 설치에 실패하면 pip를 사용하여 설치해 볼 수 있습니다: `pip install uv`
- **노트북 오류**: 모든 의존성이 올바르게 설치되었고 Ollama가 백그라운드에서 실행 중인지 확인하십시오.
