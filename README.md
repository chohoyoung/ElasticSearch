엘라스틱 서치
======================

# 1. 일래스틱서치 기초
## 1.1 자료구조 개념
### 1.1.1 색인(Index)
색인은 els(Elastic search)가 논리적인 자료를 저장하는 논리 공간. 더 작은 조각으로 나누어 질 수 있음.
색인을 여러 서버에 분산 할 수 있다. 각 색인은 하나이상의 샤드(shard)로 구성되며 샤드마다 레플리카(replica)를 가질 수 있다.
### 1.1.2 다큐먼트(Document)
1. 다큐먼트는 하나의 데이터이다. 
2. 다큐먼트는 모든 공통 필드에 대한 타입이 동일해야한다. 예를 들어 title이라는 필드를 포함한 모든 다큐먼트는 title필드에 대해 동일한 자료 타입(예: String)을 따라야 한다. 
3. 다큐먼트는 여러 필드를 포함하며 각 필드는 한 다큐먼트에 여러번 등장 할 지도 모른다 (이것을 복수값(multivalued)이라 한다). 
4. 필드마다 타입(텍스트, 숫자, 날짜 등)이 정해져 있으며, 필드 타입은 복합 타입이 될수 있다. 즉 필드는 하위 다큐먼트, 배열등을 가질 수 있다. 
5. 다큐먼트의 구조는 고정할 필요가 없다, 다큐먼트마다 필드 집합이 틀려도 된다. 
6. 클라이언트 입장에서 다큐먼트는 JSON객체를 뜻한다. 
7. 다큐먼트는 색인 한곳에 저장된다. 
8. 다큐먼트마다 독자적인 식별자와 다큐먼트 타입이 존재한다. 
9. 다큐먼트는 다큐먼트 타입과 관련된 유일한 식별자를 요구한다.
10. 다큐먼트는 단일 색인 안에서 타입이 동일하지 않지만 식별자는 동일한 다큐먼트가 두개 존재할 수 있다.