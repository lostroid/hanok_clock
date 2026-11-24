# STEP 1 (KR)  
  
# 디자인  
디자인 외형이 먼저 정해져야 합니다.
1. 작고 책상 위에서 사용 해야 된다.  
2. 한옥 형태로 모양 선정  
<img width="800" height="479" alt="스크린샷 2026-07-22 011608" src="https://github.com/user-attachments/assets/71c0a76a-be7f-4532-879a-55b5cc93667d" />  
  
# 부품 선정  
디자인이 어느 정도 정해지면 실제 PCB 보드 크기 기준으로 부품 선정  
기능에 적합한 부품을 디지키 또는 마우저 에서 가격 순으로 검색

## 1. MCU (알리에서 판매중인 모델 사용 WeAct-STM32WBA65CxCoreBoard)
PCB를 만들어도 되지만 RF특성 을 제대로 알지 못해 무선 성능이 안 좋을 것 같아 모듈 선택  
<img width="800" height="733" alt="스크린샷 2026-08-07 022641" src="https://github.com/user-attachments/assets/78a00d19-2171-4c25-a49e-12571f4663f4" />  
  
  
## 2. 디스플레이  (단점 특별한 모델명이 없음)
기존에 사용 했던  SPI 인터페이스 3가지 모델 2.4인치, 2.8인치, IPS 2.8인치 3가지 종류 선택  
해상도: TFT LCD 240x320 (SPI1)  
드라이버: ST7789V,  ILI9341  
속도: 50Mhz  
<img width="400" height="351" alt="스크린샷 2026-07-09 025611" src="https://github.com/user-attachments/assets/9e639963-53bf-40e9-a25a-ea6270a02005" />
<img width="400" height="554" alt="스크린샷 2026-07-21 031258" src="https://github.com/user-attachments/assets/8c32b567-1792-4177-847a-c5f26188a3a8" />  
   
  
## 3. 온습도 (SHT40-AD1B-R2)  
가스, 온도, 습도, 공기질 통합 부품을 사용 하려고 했으나 부품 가격이 너무 비싸서 제외❌  
<img width="300" height="241" alt="스크린샷 2026-07-09 015412" src="https://github.com/user-attachments/assets/3cea2360-102d-4403-8d2f-c92a0914f1f1" />
  
아래 온도/습도 센서 사용 인터페이스는 I2C  
<img width="300" height="258" alt="스크린샷 2026-09-02 020523" src="https://github.com/user-attachments/assets/0dc8c86c-877d-4898-b50c-d3b842ff15c1" />  
  
    
## 4. 광센서(LTR-329ALS-01)  
광원을 감지 하여 주변 밝기에 따라 LCD 밝기 조절 목적  
<img width="300" height="234" alt="스크린샷 2026-09-21 234359" src="https://github.com/user-attachments/assets/53554522-f561-4839-b787-7b105d06a96f" />
  
  
## 5. SDCARD 소켓  (MSD-4-A)
보드가 SDIO 까지 쓸 수가 없어서 SPI로 사용  
<img width="300" height="201" alt="스크린샷 2026-09-21 235326" src="https://github.com/user-attachments/assets/563323e3-5d35-433f-8cb7-e561e47bc006" />  

    
## 6. AMP 오디오용 (TAS5815PWPR.pdf)  
스피커에 비에 사양이 오버 스펙입니다.  
5W 스피커에 비하면  30W 출력은 거기다 Mono 구성이라 60W.  
<img width="300" height="143" alt="스크린샷 2026-09-22 000008" src="https://github.com/user-attachments/assets/5400f659-040a-4f67-90bc-2fc14790233f" />  


## 7. 기타 부품  
MIC2860-2DYC6-TR : LCD 밝기 조절  
TPS61288LRQQR : 5V -> 12V AMP 전원 공급  



   
