# HANNOK CLOCK [KR]  
# 2026년도 개인 프로젝트 입니다.  
<p align="center">
<img width="800" height="845" alt="image" src="https://github.com/user-attachments/assets/af22b5d3-5297-4c82-b13e-03bd50dc7c84" />
</p>

* HANNOK CLOCK 이란 한옥 모양의 탁상용 시계의 프로젝트 입니다.  
* 주요 기능은 다음과 같습니다.
  우선 주요 인터페이스 공부 및 무선 기능 개발 Bare Metal 시스템 개발
  1차 목표  
  1. 시계기능 : 년월일 (요일) 시분초 정보 제공  
  2. 이벤트 알람 기능 : 특정 알람 기능  
  3. 블루투스 스피커 기능 : 휴대폰과 Bluetooth 기능으로 통해 음악 재생  
  4. 앨범 기능 특정 포멧의 이미지 BMP 파일 형태로 화면에 표시 1초 ~ 1000초 까지 조정  
  5. 온도 표시 기능 (온습도센서 I2C)
  6. 습도 표시 기능 
  7. 광량 센서 기능 (광 센서) 통해 디스플레이 자동 밝기 조절  
    
  2차 목표  
  1. IOT 시스템 구측 Zigbee 를 통한 각 방마다 정보 수집  
  2. 네트워크 [구축 외부]--[Main IOT관리]--[Zigbee1, Zigbee2...]  
     　　　　　　　　└------------┴----------[Bluetooth]--[Phone]  
     　　　　　　　　　　　　
## 다음과 같은 순서로 진행을 합니다.  
[✔️ Step 1 : 목표, 부품선정  ](https://github.com/lostroid/hanok_clock/blob/main/notes/Step1_kr.md)  
[✔️ Step 2 : 기구 설계, 초기 모델 조립  ](https://github.com/lostroid/hanok_clock/blob/main/notes/Step2_kr.md)  
[✔️ Step 3 : 아트웍  ](https://github.com/lostroid/hanok_clock/blob/main/notes/Step3_kr.md)  
[✔️ Step 4 : PCB조립  ](https://github.com/lostroid/hanok_clock/blob/main/notes/step4_kr.md)   
[✔️ Step 5 : 케이스 제작  ](https://github.com/lostroid/hanok_clock/blob/main/notes/step5.kr.md)   
[✔️ Step 6 : 조립  ]   
[✔️ Step 7 : 개발  ]   
⚠️ 실제 순차적으로 진행을 하면서 일부 펌웨어와 하드웨어 개선으로 step을 앞뒤로 이동 할 수는 있습니다.  

