## 사전 지식
가장 정리 잘된 아래 글 먼저 읽기
- https://velog.io/@k-svelte-master/what-is-mcp
- https://becomingahacker.org/integrating-agentic-rag-with-mcp-servers-technical-implementation-guide-1aba8fd4e442

## 설계 관련 노하우 정리

### 채팅 노하우
- 구글 genai 패키지 내에서도 채팅 세션은 gemini 가 담당하지 않고 라이브러리에서 처리. 채팅 히스토리를 내부적으로 쌓은 후 히스토리를 한번에 보냄.
- 이때 히스토리에서 유의미한 채팅 내역만 뽑아서 보낼지 말지 조절할 수 있음. (curated)

### 에이전트 설계 패턴
- https://google.github.io/adk-docs/agents/multi-agents/
- Loop Agent
    - https://google.github.io/adk-docs/agents/workflow-agents/loop-agents/#loop-agents
    - 생성 & 평가 루프 가능
  
### 토큰 최적화
- 텍스트 임베딩: https://ai.google.dev/gemini-api/docs/embeddings

## AI Agent
- 프롬프트를 어떤 과정을 거쳐서, 효과적 & 효율적으로 다루기 위한 방안들
### 레퍼런스
- https://news.hada.io/topic?id=18376
- https://www.promptingguide.ai/research/llm-agents
- 에이전트 오픈소스
    - https://github.com/Chainlit/chainlit
    - https://github.com/langchain-ai/langchain
    - https://github.com/crewAIInc/crewAI
    - https://github.com/upsonic/upsonic
    - Cline : https://github.com/cline/cline/blob/main/src/core/task/index.ts

### 적용 사례
- https://medium.com/@nuatmochoi/테크니컬-라이팅을-위한-ai-어시스턴트-구축하기-feat-react-agents-for-amazon-bedrock-304c12527539
- https://aws.amazon.com/blogs/machine-learning/harness-the-power-of-mcp-servers-with-amazon-bedrock-agents/

### 멀티 에이전트
- https://medium.com/@sahin.samia/multi-agent-ai-systems-foundational-concepts-and-architectures-ece9f8859302
- https://github.com/GoogleCloudPlatform/generative-ai/blob/main/gemini/agents/research-multi-agents/intro_research_multi_agents_gemini_2_0.ipynb
- https://www.magicaiprompts.com/blog/openai-swarm-ai-agent-collaboration
- https://github.com/awslabs/multi-agent-orchestrator

### 오픈소스
- LangGraph
- CrewAI
- upsonic
- Google
    - ADK : https://google.github.io/adk-docs/
    - Document RAG: https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-your-data#generative-ai-gemini-grounding-python
- Agents to Agents
    - https://google.github.io/A2A/#/
    - https://github.com/google/A2A
- AWS: InlineAgent https://github.com/awslabs/amazon-bedrock-agent-samples/tree/main/src/InlineAgent

## 엔지니어링 도구
에이전트에 프롬프트를 넣었을 때 잘 동작하는지 평가를 하기 위한 방안들

### 레퍼런스
- https://d2.naver.com/helloworld/3344073
- https://clickup.com/ko/blog/169558/prompt-engineering-tools
- https://github.com/promptfoo/promptfoo
- https://imanishtyagi.medium.com/llmtesting-promptfoo-b43ac17298a4
- https://github.com/ianarawjo/ChainForge
- https://github.com/comet-ml/opik
  
### 종합 정리
- https://latitude-blog.ghost.io/blog/top-7-open-source-tools-for-prompt-engineering-in-2025/
