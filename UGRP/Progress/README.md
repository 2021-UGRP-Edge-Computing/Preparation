# Recording Meeting

## 6/18 UGRP 카톡 회의

  
### 제안된 논문 (검수 전)
https://openreview.net/forum?id=Ek7qrYhJMbn  - Centralizea와 Decentralize 방식의 차이점 비교
https://ieeexplore.ieee.org/abstract/document/9197692?casa_token=YrdPHnnqlQsAAAAA:XmuJI2gHHQCdHBBNbrybhrKd1KLE1vYv_h683jNzIhkLC_BmEX74htbWwc3QjqVFd5AW7VO8m_HL - 최적화 관련
https://arxiv.org/abs/1907.09356 - 최적화 관련

### 장단점 비교
Decentralize:구현이 쉽고, 중앙서버에 관한 병목현상이 없고, 비교적 최신 기술이라는 장점이 있지만 
네트워크에 mutual trust관계의 노드가 없다면 원활하게 learning이 진행되지 않고, 비교적 연구가 덜 되었다는 단점이 있습니다.
Training: 구현이 어렵지만 좀 더 많은 것을 배울 수 있음
Inference: 구현이 쉽지만 UGRP 목표에 어긋나지 않아 보임

### 결과 
Decentralize / Inference 조합을 사용하기로 결정, 다만 추후 상황을 보며 Inference에서 Training으로 변경 가능
Decentralize의 단점 중 Mutual trust 문제는 모든 Node가 딱히 신뢰성을 잃을 만큼 나쁜 상황에 빠지지 않을 것이라 생각하므로 발생하지 않을 것이라 예상.


## 6/2 UGRP 2차 회의 
```
## 조직업무분담추가:
  정리와 행정 추가. 
  정리: 호준, 행정: 성민
  정리: 실험 데이터와 깃허브 담당
  행정: 물품 구매 등 행정 업무 담당


## JETSON TX2 관련:
  해당 물품이 단종되서 JETSON NANO로 변경-> 예산잉여분 발생함.


## 연구업부분담:
  알고리즘 : 성민
  구현 : 준서
  브릿지 : 호준 
  총괄: 진휘

  알고리즘 :  엣지 컴퓨팅 시스템 알고리즘 탐구,매트랩 시뮬레이션 할 것.
  구현 : 알고리즘의 구현이 가능한지 .확장성 있게 구현해야 할 것. 시뮬레이션은 메트랩으로 돌릴 것.
  브릿지: 알고리즘의 구현이 가능한지 적절하게 되었는지 . 일단 구현 서포트해줄 것.
  총괄: 위 셋에게 간섭할 것.

## 깃허브 사용법:
  모듈설치방법 기재요령은 꼭 어떤 컴퓨터에든 같은 방식으로 모듈 설치시 문제가 없도록 기재.
  설치 명령어를 기재할 때에도 실행환경 기재
  에러는 모듈 설치와 관련된 것만.
  페이퍼 섹션에는 검수된 페이퍼만 업로드
  서기 회의록 관련 폴더를 추가해서 리드미 파일 작성요령 확인해서 회의록 올리도록.(정리역할)
```
