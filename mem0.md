# Mem0

- 단순히 저장하는게 아니고, 일관되게, 추려서 저장한다. 개인화에도 쓸 수 있고, context 유지에도 쓸 수 있음.
- 가볍게 만들어졌다. (장점)
  - 자주 업뎃되는거는 우리 입장에서는 단점
- 엔터 사업도 하는데, 일부분이 오픈소스인 형태
- 세가지 메소드를 제공: 주로는 add와 search
  - add
  - search
  - update
- 저장시에 vectordb + rdb + graphdb 세가지를 모두 다 씀
  - base는 vectordb (최신만 가지고 있음)
  - graph는 관계
  - key-value는 전체 저장 관점 (과거 정보도 바뀌는게 보임)
- flow
  - add: deduct llm 거친 뒤의 정보를 db search 해서 새로운거면 저장함 -> 새로운거 판단도 llm이 함. (판단의 tool로 add, update, delete를 사용)


 # MemGPT

- 장단기 메모리를 고려해서 Context length를 어떻게 효율적으로 잘 관리할 것인가. 외부 저장 장치를 이용해서 효율적으로 관리하겠다.
- Archival: 문서
- Recall: 전체 chat
  - 일부가 Archival로 전달
 - 장기/단기 정의 필요
 - In-Context 메모리 - 항상 프롬포트에서 들고다니는거
   - Core Memory(2k): initial memory. human + persona
   - functions
     - core_memory_append
     - core_memory_replace
-
