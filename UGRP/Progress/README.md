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
## 7/23 곽정호 교수님 미팅 후 회의 

```
  # 알고리즘 팀:
  a. 이슈에 대한 해답 제안
  b. Dynamic Timeslot에 대한 고찰
  c. 협력 디바이스가 늘어날 때 발생할 이슈 고찰
  # 구현 팀:
  리소스 버틀넥 문제 해결에 있어 협력이 미치는 영향을 확인하기 위한 실험을 진행.
  실험 목적:  리소스 버틀넥 문제 해결에 있어 협력이 보여주는 효과를 FPS 를 통해 확인하고,
  협력의 효과에 영향을 주는 조작 변인들을 찾아내고 적절한 조작치를 찾아내어 궁극적으로
  resource bottleneck에 최적화된 협력 방법에 대한 영감을 얻기 위함임 .

   실험 설계:
   주어진 task를 스스로 해결하는 A와 일정한 시간주기로 협력기기(1개)에 협력과제를 보내고 쉬었다가
   다시 과제를 수행하는 것을 반복하는 B를 조작변인에 따른 FPS, Average power consumption,GPU usage,
   Average subtask sol time, task finish time 등의 데이터를 수집.
                        
   조작변인: CPU,GPU CPU,GPU frequency와 task(협력,local,total) 양 또는 time slot 길이. 등
   통제변인: 주어지는 과제 및 종류(image), 과제 처리 알고리즘(Yolo), network 상태.
   얻어야할 결과데이터: FPS, Average power consumption,GPU usage,
   Average subtask sol time, task finish time 등

   실험으로 연구가 기대되는 심화내용
   버틀넥 디텍션 방법: - GPU usage, power, frequency 의 경우, 몇 퍼센트를 기준으로 버틀넥이라 판단할 것인지
    - GPU Temperature, 몇 도를 기준으로 버틀넥으로 판단할지
    - Average subtask sol time(평균 이미지 처리 시간),를 기준으로, 
    단위 소과제당 얼마의 시간이 초과할 경우 버틀넥으로 판단할지
    - 버틀넥 디텍션에 관한 논문 참고해서 결정하기

    무지성이 아닌 풀지성 협력 방법: - 기기의 협력 가능한 상태를 어떻게 정할 것인지(버틀넥 디텍션)
    - 적절한 협력 subtask 양
```                                                              
