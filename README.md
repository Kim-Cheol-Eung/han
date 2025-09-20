## **💡1. 프로젝트 개요**

**1-1. 프로젝트 소개**
- 프로젝트 명 : 인공지능기반의 노인 낙상 예측 시스템 구현
- 프로젝트 정의 : 실시간 낙상 예측 및 감지 시스템
  <img width="400" height="400" alt="image" src="https://www.hanemall.com/img/product/2023-04-12_so2d2" /></br>

**1-2. 개발 배경 및 필요성**
- 낙상 후 사망률이 높아 예방과 신속한 대응이 필수적이다. 기존의 낙상 감지 시스템(CCTV, 웨어러블 기기, 응급 버튼 등)은 개인정보 보호, 착용 거부감, 비효율적인 감지 등의 한계를 가진다. 이를 해결하기 위해 인공지능(AI) 기반 실시간 낙상 예측 및 감지 시스템이 필요하다.

**1-3. 프로젝트 특장점**
- 인력 기반 감지 : 병원 내 인력에 의존하는 낙상 감지는 실시간 인지 및 대응에 한계가 명확하며, 잦은 오류와 인력 소모를 야기함. 본 시스템은 AI 기반 자동 감지로 이러한 인력 의존도를 낮춤.
- 단순 센서/웨어러블 기기 : 단순 센서는 실시간 인지에 한계가 있고, 웨어러블 기기는 환자의 지속적인 착용이 어려워 실효성이 낮음. 본 시스템은 비침습적인 CCTV 기반으로 이러한 착용의 불편함과 실효성 문제를 
해결.
- 정확도 및 실시간성 : 기존 시스템이 제공하지 못하는 실시간 낙상 감지 및 높은 정확도를 제공함.
- 통합 분석 : YOLOv8을 통한 객체 탐지, AlphaPose를 통한 자세 추정, ST-GCN을 통한 시간 흐름 분석을 결합한 다중 조건 기반 앙상블 로직으로 낙상을 판단. 이는 단순 센서 기반 시스템으로는 불가능한 정밀한 판단을 가능하게 함.- 확장성 및 범용성 : 다양한 병실 구조와 환자 유형에도 적용 가능하도록 설계되어, 기존 시스템 대비 확장성이 뛰어남.
 - 대부분의 유사 연구가 객체 탐지나 자세 추정 중 한 가지 기술에 중점을 두는 반면, 본 프로젝트는 YOLOv8, AlphaPose, ST-GCN을 유기적으로 결합하여 낙상 감지의 정확도와 신뢰성을 극대화하였음.
 - 대부분의 연구가 공개된 일반 데이터 셋을 활용하고, 실제 데이터를 추가해서 보강하였음. 본 프로젝트는 실제 병원 병실 내 낙상 장면을 직접 촬영한 영상 데이터를 기반으로 학습용 데이터 셋을 구축했음. 이는 실제 병원 환경에서 발생할 수 있는 다양한 시나리오(정상, 위험, 낙상 자세 등)를 반영하여 모델의 현실 적용 가능성과 정확도를 높일 수 있음.
 - 감지 모델 개발에만 집중하는 경우가 많은 유사 연구와 달리, 본 프로젝트는 감지된 낙상 정보를 의료진 단말기로 즉시 전송하는 실시간 알림 시스템을 구축하였음. 이는 실제 병원 환경에서 즉각적인 대응을 가능하게 하는 중요한 실용적 차별점임.

**1-4. 소프트웨어(S/W) 주요 기능**
- 실시간 객체 탐지 : YOLOv8 기반으로 환자 및 의료진을 실시간으로 인식하여 사람의 위치를 추출함
- 포즈 추정 및 자세 분석 : AlphaPose를 통해 사람의 관절 위치를 추출하고, 낙상 위험 행동(넘어짐, 쓰러짐 등)을 분석함
- 의미 기반 추천 : 단순한 ‘정확 단어 일치’가 아닌 맥락과 의미를 기반으로 한 결과 제공
- 맞춤형 필터링 및 정렬 : 사용자 성향에 따라 검색 결과 필터 및 순위 조정
- 멀티플랫폼 지원 : 웹·모바일 등 다양한 기기 환경에서 최적화된 검색 경험 제공

**1-5. 하드웨어(H/W) 주요 기능**
- 적외선(열화상) 카메라 : 카메라를 활용한 실시간 영상 수집
- 테스트 및 실증 침대 : 데이터 수집 및 실증 침대 구현

**1-6. 기대 효과 및 활용 분야**
- 기대 효과 : 비접촉 및 비침습성 모니터링, 높은 실시간성 및 정확도, 비용 효율성
- 활용 분야 : 의료 및 요양 시설, 가정 내 스마트 헬스케어

**1-7. 기술 스택**
- 프론트엔드 : React, Next.js, Tailwind CSS
- 백엔드 : Python(FastAPI), Node.js, Django
- AI/ML : PyTorch, TensorFlow, Hugging Face, OpenAI API
- 데이터베이스 : PostgreSQL, MongoDB, Elasticsearch
- 클라우드 : AWS
- 배포 및 관리 : Docker, Kubernetes, GitHub Actions

---

## **💡2. 팀원 소개**
| <img width="80" height="100" src="https://pics.craiyon.com/2024-03-29/TAgYq3VcQKe3IkDw6PBd1A.webp"> | <img width="80" height="100" alt="image" src="https://image2.1004gundam.com/item_images/goods/380/1376406813.jpg"> | <img width="80" height="100" alt="image" src="https://image2.1004gundam.com/item_images/goods/380/1376406811.jpg"> | <img width="80" height="100" alt="image" src="https://www.sideshow.com/storage/product-images/903245/green-ranger-dragonzord_mighty-morphin-power-rangers_feature.jpg"> | <img width="80" height="100" alt="image" src="https://e7.pngegg.com/pngimages/767/8/png-clipart-kimberly-hart-katherine-hillard-pink-super-sentai-mighty-morphin-power-rangers-power-rangers-fictional-character-magenta-thumbnail.png"> | <img width="80" height="100" alt="image" src="https://m.herotime.co.kr/web/product/big/202312/852289aa69b6ac9eb8d5f4d03be0c40f.png"> | <img width="80" height="100" alt="image" src="https://ecimg.cafe24img.com/pg168b06062900060/asl1052/web/product/big/20240401/cb914c20ffcaf86d6d8f593f8420793b.jpg">
|:---:|:---:|:---:|:---:|:---:|
| **김철응** | **심가은** | **이유빈** | **김백강** | **유민지** | **최지훈** | **안영휘** |
| • 팀장 <br> • 데이터수집 | • 서류작성&취합 | • 기술개발 | • 장비점검 | • 데이터분석 | • 프로젝트 멘토 <br> | • 지도교수 |
---
## **💡3. 시스템 구성도**
> **(참고)** S/W구성도, H/W구성도, 서비스 흐름도 등을 작성합니다. 시스템의 동작 과정 등을 추가할 수도 있습니다.
- 서비스 구성도
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/28fc8453-d1a0-4184-8fd0-130d93d18545" />


- 엔티티 관계도
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/76e3347b-6d94-491e-8aeb-a7b4601c54d5" />


---
## **💡4. 작품 소개영상**
> **참고**: 썸네일과 유튜브 영상을 등록하는 방법입니다.
```Python
아래와 같이 작성하면, 썸네일과 링크등록을 할 수 있습니다.
[![영상 제목](유튜브 썸네일 URL)](유튜브 영상 URL)

작성 예시 : 저는 다음과 같이 작성하니, 아래와 같이 링크가 연결된 썸네일 이미지가 등록되었네요! 
[![한이음 드림업 프로젝트 소개](https://github.com/user-attachments/assets/16435f88-e7d3-4e45-a128-3d32648d2d84)](https://youtu.be/YcD3Lbn2FRI?si=isERqIAT9Aqvdqwp)
```
[![한이음 드림업 프로젝트 소개](https://github.com/user-attachments/assets/16435f88-e7d3-4e45-a128-3d32648d2d84)](https://youtu.be/YcD3Lbn2FRI?si=isERqIAT9Aqvdqwp)


---
## **💡5. 핵심 소스코드**
- 소스코드 설명 : API를 활용해서 자동 배포를 생성하는 메서드입니다.

```Java
    for i, track in enumerate(tracker.tracks):
        if not track.is_confirmed():
            continue
    
        track_id = track.track_id
        bbox = track.to_tlbr().astype(int)
        center = track.get_center().astype(int)

        action = 'pending..'
        clr = (0, 255, 0)

        if len(track.keypoints_list) == 30: 
        #스켈레톤 데이터의 좌표 추출해서 30개인지 확인(유효한 값 확인)
            pts = np.array(track.keypoints_list, dtype=np.float32)
            out = action_model.predict(pts, frame.shape[:2])
            #스켈레톤 데이터로 자세 예측
            action_name = action_model.class_names[out[0].argmax()]
            action = '{}: {:.2f}%'.format(action_name, out[0].max() *100)
```         if action_name == 'Fall Down':
                clr = (255, 0, 0)
            elif action_name == 'Lying Down':
                clr = (255, 200, 0)