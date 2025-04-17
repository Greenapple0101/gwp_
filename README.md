
# 🌱 OLED TFT Insulator GWP Analysis
150 이하 GWP(Global Warming Potential)를 목표로 한 **OLED TFT 절연막 패턴 형성 공정 온실가스 분석**  
MATLAB · Python (pandas · matplotlib · scikit‑learn)

---

## 📘 프로젝트 개요
OLED 디스플레이 제조 과정에서 **절연막(Insulator) 패턴**을 형성할 때 발생하는 온실가스 배출을 정량화하고, 공정·재료·장비별 배출 기여도를 분석합니다.  
궁극적으로 **공정당 GWP ≤ 150** 을 달성하기 위한 최적 공정 파라미터를 찾는 것이 목표입니다.

* **연구실** : 임경수 교수님 Lab (수학과 학부연구생)  
* **기간** : 2025 .01 – 진행 중

---

## 🗂️ 폴더·파일 구조
```text
gwp-analysis/
├── gwp/                       # (비공개) 원본·중간 산출물
├── MR_24_02_05.ipynb          # 주요 Python 분석 노트북
├── Reconstructed data.csv     # 재구성(clean)된 공개 가능 데이터 샘플
└── README.md                  # 현재 문서
```
> **주의**  `gwp/` 디렉터리와 일부 CSV 원본은 연구실 내부 데이터이므로 외부 공개 대상이 아닙니다.

---

## 🛠 기술 스택

| 분류 | 도구 |
|------|------|
| 분석 | **Python 3.11** (pandas · NumPy · matplotlib · seaborn · scikit‑learn) |
| 시각 | matplotlib · seaborn |
| 문서 | Jupyter Notebook |
| 버전 관리 | Git · GitHub |

---

## ⚙️ 로컬 실행 방법
1. **가상환경(선택)**
   ```bash
   python -m venv venv
   source venv/bin/activate      # Windows: venv\Scripts\activate
   ```

2. **필수 라이브러리 설치**
   ```bash
   pip install -r requirements.txt   # 없으면 pandas numpy matplotlib scikit-learn jupyter 설치
   ```

3. **Jupyter Lab/Notebook 실행**
   ```bash
   jupyter lab
   # 브라우저에서 MR_24_02_05.ipynb 열기
   ```

> 노트북이 참조하는 소스 데이터(CSV)는 `gwp/` 혹은 같은 경로에 위치해야 합니다.  
> 외부 공개용 샘플은 `Reconstructed data.csv` 파일로 제공됩니다.

---

## 🎯 연구 진행 현황
- [x] 원본 데이터 수집 & 단위 통일
- [x] Exploratory Data Analysis (EDA) 완료
- [x] 다중 회귀 · 트리 모델 베이스라인 구축
- [ ] 공정별 LCA(Life Cycle Assessment) 파라미터 확장
- [ ] 최적 공정 파라미터 탐색(Genetic Algorithm)
- [ ] 연구 논문 초안 작성

---

## 📊 예시 결과
| 공정 단계 | GWP 기여도(%) |
|-----------|--------------|
| ALD Coat  | 41.3 |
| Anneal    | 27.5 |
| Etch      | 18.2 |
| Clean     | 13.0 |

- **Feature Importance** : 공정 온도·가스 플로우가 총 변동의 62 % 설명  
- **시뮬레이션** : 가스 플로우 –15 % 조정 시 GWP 평균 –12 % 달성

> ※ 수치는 샘플 데이터 기준이며, 실제 연구 결과는 내부 보고서에 포함됩니다.

---

## 👩‍💻 기여자
| 이름 | 역할 |
|------|------|
| **백서연** | 데이터 정제 · Python EDA & 모델링 |
| **임경수 교수님** | 연구 지도 · 실험 설계 |

---

## 📄 라이선스
```
© 2024 임경수 Lab — Internal Research Data (No Public Redistribution)
```

---

> 💬 문의 : seoyeon.baek@example.com
```

1. 이 내용을 **README.md** 로 저장  
2. 커밋 & 푸시:
   ```bash
   git add README.md
   git commit -m "docs: add full README for GWP analysis project"
   git push origin main
   ```
