# STEP 1 (KR)

## 디자인

디자인 외형이 먼저 정해져야 합니다.

1. 작아서 책상 위에 둘 수 있어야 한다.
2. 한옥 형태로 모양 선정

<img width="800" height="479" alt="한옥 시계 디자인 스케치" src="https://github.com/user-attachments/assets/71c0a76a-be7f-4532-879a-55b5cc93667d" />

## 부품 선정

디자인이 어느 정도 정해지면 실제 PCB 보드 크기를 기준으로 부품을 선정합니다.  
기능에 맞는 부품을 Digi-Key 또는 Mouser에서 가격순으로 검색했습니다.

### 1. MCU — WeAct STM32WBA65Cx Core Board (AliExpress 판매 모델)

MCU를 PCB에 직접 넣을 수도 있지만, RF 특성을 잘 몰라 무선 성능이 떨어질 것 같아 모듈을 선택했습니다.

<img width="800" height="733" alt="WeAct STM32WBA65 코어 보드" src="https://github.com/user-attachments/assets/78a00d19-2171-4c25-a49e-12571f4663f4" />

### 2. 디스플레이 (단점: 정확한 모델명 없음)

기존에 사용했던 SPI 인터페이스 모델 3종(2.4인치, 2.8인치, IPS 2.8인치)을 선택했습니다.

- 해상도: TFT LCD 240×320 (SPI1)
- 드라이버: ST7789V, ILI9341
- 속도: 50MHz

<img width="400" height="351" alt="2.4인치 TFT LCD" src="https://github.com/user-attachments/assets/9e639963-53bf-40e9-a25a-ea6270a02005" />
<img width="400" height="554" alt="2.8인치 TFT LCD" src="https://github.com/user-attachments/assets/8c32b567-1792-4177-847a-c5f26188a3a8" />

### 3. 온습도 센서 — SHT40-AD1B-R2 (I2C)

가스·온도·습도·공기질 통합 센서(모델명)를 쓰려 했으나 가격이 너무 비싸서 제외했습니다. ❌

<img width="300" height="241" alt="제외한 통합 환경 센서" src="https://github.com/user-attachments/assets/3cea2360-102d-4403-8d2f-c92a0914f1f1" />

대신 아래 온습도 센서(SHT40, I2C 인터페이스)를 사용합니다. ✅

<img width="300" height="258" alt="SHT40 온습도 센서" src="https://github.com/user-attachments/assets/0dc8c86c-877d-4898-b50c-d3b842ff15c1" />

### 4. 광센서 — LTR-329ALS-01

주변 밝기를 감지해 LCD 밝기를 조절하는 용도입니다.

<img width="300" height="234" alt="LTR-329ALS-01 광센서" src="https://github.com/user-attachments/assets/53554522-f561-4839-b787-7b105d06a96f" />

### 5. SD 카드 소켓 — MSD-4-A

보드에서 SDIO를 쓸 수 없어 SPI로 연결합니다.

<img width="300" height="201" alt="MSD-4-A SD 카드 소켓" src="https://github.com/user-attachments/assets/563323e3-5d35-433f-8cb7-e561e47bc006" />

### 6. 오디오 앰프 — TAS5815PWPR

사용할 5W 스피커에 비해 오버 스펙입니다.
스테레오 30W 출력에, 모노 구성 시 최대 60W까지 낼 수 있습니다.

<img width="300" height="143" alt="TAS5815 오디오 앰프" src="https://github.com/user-attachments/assets/5400f659-040a-4f67-90bc-2fc14790233f" />

### 7. 기타 부품

- **MIC2860-2DYC6-TR**: LCD 백라이트 밝기 조절
- **TPS61288LRQQR**: 5V → 12V 승압 (앰프 전원)
