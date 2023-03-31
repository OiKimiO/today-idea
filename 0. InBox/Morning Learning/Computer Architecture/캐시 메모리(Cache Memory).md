### 날짜 : 2023-03-31 08:39
### 주제 : 캐시 메모리(Cache Memory)
---
### 태그
* #cache, #memory

### 메모
* 속도가 빠른 장치와 느린 장치의 병목현상을 줄이기 위해 나온 장치
	* CPU 코어와 메모리 사이의 병목현상 완화
	* 웹 브라우저 캐시 파일은 하드디스크와 웹페이지 사이의 병목 현상 완화

* CPU가 캐시메모리를 사용하는 방식
	* CPU는 주기억장치에서 저장된 데이터를 읽어올 때
	* 자주 사용하는 데이터를 캐시 메모리에 저장
	* 이후 다음에 사용할 때 캐시 메모리 가져오면서 속도 향상시킴
	
* 속도와 크기에 따라 분류한 캐시 메모리의 종류
	* L1
		* CPU 내부에 존재
	* L2
		* CPU와 RAM사이에 존재
	* L3
		* 메인보드에 존재
		
* 캐시 메모리의 작동 원리
	* 시간 지역성
		* for나 while같은 반복문에서 사용하는 조건 변수 처럼 참조된 데이터는 잠시후 또 참조될 가능성이 높음
	* 공간 지역성
		* A[0], A[1]과 같이 연속 접근시 참조된 데이터 근처에 있는 데이터가 잠시 후 또 사용될 가능성이 높음
		
* 캐시 Miss 3가지
	* Cold miss
		* 해당 메모리 주소를 처음 불러서 나는 미스
	* Conflict miss
		* 캐시 메모리에 A,B 데이터를 저장해야 하는데, A와 B가 같은 메모리 주소에 할당되어 있어서 나는 미스
	* Capacity miss
		* 캐시 메모리에 공간이 부족해서 나는 미스
		* 캐시 크기를 늘리면 캐시 접근 속도가 느려지고 파워를 많이 먹는 단점이 생김

* 구조 및 작동 방식
	* Direct Mapped Cache
		* 간단하고 빠르지만, Conflict Miss가 발생하는 단점있음
	* Fully Associative Cache
		* 비어있는 캐시가 있으면, 마음대로 주소를 저장
		* 저장할 때는 매우 간단하지만, 찾을 때가 문제
	* Set Associative Cache
		* Direct + Fully 방식
		* Direct에 비해 속도는 느리지만 저장이 빠르고, Fully에 저장은 느린 대신 검색이 빠른 중간형

### 출처(참고문헌)
-  [캐시 메모리](https://github.com/gyoogle/tech-interview-for-developer/blob/master/Computer%20Science/Computer%20Architecture/%EC%BA%90%EC%8B%9C%20%EB%A9%94%EB%AA%A8%EB%A6%AC(Cache%20Memory).md)


### 연결문서
- 