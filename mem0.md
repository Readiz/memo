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
  - base는 vectordb
  - graph는 관계
  - key-value는 전체 저장 관점
- flow
  - add: deduct llm 거친 뒤의 정보를 db search 해서 새로운거면 저장함 -> 새로운거 판단도 llm이 함. (판단의 tool로 add, update, delete를 사용)


 # MemGPT
