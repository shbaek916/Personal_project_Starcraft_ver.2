#### 본 레포지토리에 대한 설명

###### Analysis_and_Modeling.ipynb 
- 본 프로젝트의 본격적 분석 및 승패 예측
###### Preprocessing_1_data_split.ipynb
- 본래 670만행의 거대한 로그데이터이기에 EDA 와 Data Wrangling에 용이하게 원본데이터의 game_id 값에 따라 나눔
###### Preprocessing_2_data_organizing(1).ipynb
- Train 데이터의 분석하고자 하는 특성을 추출
###### Preprocessing_2_data_organizing(1)_test_data.ipynb
- Test 데이터의 분석하고자 하는 특성을 추출
###### Preprocessing_2_data_organizing(2).ipynb
- 본격적 분석에 앞서 데이터 전처리 진행
###### Project 1. 스타크래프트2 승패의 정량적 분석 [백송하].docx
- 코드스테이츠 제출용 기획서



# Personal_project_Starcraft_ver.2
## _스타크래프트 2 승패 정량적 분석_

#### 개요 & 프로젝트의 목적

- 앞서 진행했던 프로젝트에서는 원본데이터에서 ability event와 ability event에서 추출하여 재가공한 worker, 생산한 일꾼의 수가 승부에 가장 큰 영향을 미치는 것으로 나타났습니다. 이번 프로젝트에서는 ability event에서 좀 더 많은 특성들을 추출하여 ability event 중 어느 특성이 가장 승패에 영향을 주는 지, 또 이를 이용해서 플레이어들이 어떤 특성에 집중해야 하는 지 알려주기 위함입니다.

- 실시간 전략 게임인 스타크래프트는 일대일 혹은 다대다의 승부에서 각자의 종족을 선택해 승부를 겨루는 게임입니다. 스타크래프트는 플레이하게 되는 맵의 지형과 전략이 더욱 중요한 게임이지만, 정량적인 분석이 필요없는 것은 아닙니다. 게임내 자원관리, 유닛 생산량, 특정 활동의 횟수, 이런 것들은 플레이어가 실시간으로 세우는 전략을 어떻게 실행하고 있느냐, 즉 플레이어의 ‘피지컬’ 을 판단할 수 있는 지표가 되기도 합니다. 따라서 이런 지표들을 선정하여 플레이어들 스스로 실력을 상승시키는데 선택과 집중을 할 수 있게 돕는 것이 이번 프로젝트의 목적입니다.

#### 활용된 데이터 
- 2020년 4월 종료된 Blizzard 사의 Starcraft II 게임의 행동 데이터 분석 대회 (DACON)
- https://dacon.io/competitions/official/235583/overview/description

#### 분석과 결과
- nonworker, 비생산유닛, 혹은 공격유닛의 생산과 buildings, 생산된 건물의 수가 가장 중요했던 것으로 나타났습니다
- 건물의 수가 많고 상대의 건물수가 상대적으로 적을 때 승리할 확률이 더 높았습니다
- 비생산 유닛의 수가 상대보다 상대적으로 많을 때 승리할 확률이 높았습니다
- 공격명령의 수도 상대적으로 더 많이 내린쪽이 승리할 확률이 높았습니다
- 실제로 공격명령수, 일반유닛 생산수, 건물 생산수가 승률에 영향을 미친다.
- 정확도는 0.57로 앞서 진행했던 섹션 2 프로젝트의 결과보다는 조금 낮다. (0.61)
- 자세한 내용은 Analysis_and_Modeling.ipynb 파일 내 "Analysis" 목차를 이용해주십시오.

#### 한계점과 아쉬운 점
- 많은 특성들을 추출해내지 못했다
- 건물과 유닛이 쓸 수 있는 특수능력들(업그레이드, 공격마법, 방어마법 등)이 있는데 각 유닛들과 건물들의 능력의 이름 하나하나 추출하기 어려웠다
- 약 4만개의 모든 게임의 최대 시간이 10분을 넘지 않았다
- 10분이 넘는 게임들을 일반화할 방식을 고안해내지 못했다
- 데이터 자체에서 게임에서 정말 중요한 특성이 없었다
- 게임에서 자원채취량, 처치한 적 유닛 수, 파괴한 적 건물 수 등을 파악할 수 없어 수치로 볼 수 있는 경기 양상을 파악할 수 없었다



