# 금융 사막화에 따른 ​방문형 은행 장소 추천 (전라남도 대상)
## 금융 사막화란?
- 은행이나 증권사 등 금융기관의 유인 점포가 수도권에만 남고 농촌 등 비수도권에선 사라지는 현상​
- 금융소외계층의 금융 접근성은 더욱 악화되며 서비스 선택 권리도 제한

## 문제 분석 및 목표 방향
전라남도 내 금융 사막화 지역을 판별하고, 고령층과 금융 취약계층이 오프라인 금융 서비스를 더 쉽게 이용할 수 있도록 방문형 은행 서비스 제공 우선지역을 추천

## 분석 파일 목록 및 설명
1. housing_data_preprocessing.ipynb
전라남도의 법정동 기준 인구 데이터를 전처리

2. geo_data_preprocessing.ipynb
전라남도의 개별/공동주택 정보와 은행 위치 정보를 결합하여 다음 정보를 추출:

특정 주소를 기준으로 반경 x km 내의 은행 개수 파악
특정 주소를 기준으로 가장 가까운 은행까지의 거리 및 대중교통 소요시간 계산
3. k_means_cluster_analysis.ipynb
전처리한 데이터를 기반으로 전라남도 내의 금융 사막화 지역을 군집화를 통해 파악

4. economic_data_preprocessing.ipynb
각 행정구역 별 산업 경제지표 데이터를 전처리

5. DBSCAN_cluster_analysis.ipynb
금융 사막화 지역으로 판별된 곳들을 지리적 위치를 기준으로 군집화하고 경제지표를 반영

## 사용된 데이터 정리 
전국 인구통계 데이터 (법정동 기준)
전국_202401_70세_이상_인구통계_법정동.csv

출처: https://www.data.go.kr/data/15099158/fileData.do

금융결제원 - 금융회사코드 조회
codefilex.csv

출처: https://www.kftc.or.kr/archive/bankListByCode

전남 개별/공동주택 공시가격 정보 (법정동 기준)
전남_개별주택가격정보.csv

전남_공동주택가격정보.csv

출처: https://www.vworld.kr/dtna/dtna_fileDataView_s001.do​

전남 읍면동별 산업대분류 별 경제지표 데이터 (행정동 기준)
전남_산업체별경제지표정보.csv

출처: https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_2KI2011&vw_cd=MT_ZTITLE&list_id=J1_3_001_001_001_002&seqNo=&lang_mode=ko&language=kor&obj_var_id=&itm_id=&conn_path=MT_ZTITLE%20%E2%80%8B
