# 1902-NIMS-report

## Abstract

I did two project as assignment in 2019 NIMS(National Institute for Mathematical Sciences) winter workshop. The first one is classifing iris data with decision tree and random forest. Error rates of two algorithms were both low and data set was not that big, so I judged algorithms are both suit for the classification.
The second one is making suggestion system for house from public data. I made norm for reckoning how much far from the codition for finding houses, suggested some houses and marked the houses on the map. Since the datasets I used don't include specific address of houses, the code functions as suggestion for streets.

## report 01

Iris 데이터에 랜덤 포레스트를 적용시켜 보았습니다. 하지만 워낙 데이터 개수가 적고 트리 방식으로도 정확도 96%, 오류가 발생한 데이터 6개였기 때문에, 유의미한 차이가 보이지는 않았습니다.

## report 02

김성운 박사님 수업시간에 다룬 내용에서, 1 유클리디안 거리에 따른 추출 함수화 2 유클리디안 거리에 가중치 주기 3 지도에 후보지 표시하기를 더 해봤습니다. 가중치를 부여하는 합리적인 아이디어는 생각하지 못하여 개인적 경험에 따라 임의로 부여하고 코드만 만들어 봤습니다. 합리적인 가중치에 대해서는 설문조사를 시행해 데이터를 수합해 보는 것도 좋을 것 같습니다. 그리고 행정안전부에서 제공하는 위치정보요약 DB를 활용해서 각 도로명 주소별 대표주소를 부여했습니다. 원 데이터에 도로 주소까지는 포함되어 있는 것에 착안해, 위치정보요약 DB에 주어진 각 건물의 주소에 대하여, 도로 주소로 묶어 평균을 내어 활용했습니다. 좌표 체계가 달라 pyproj 라이브러리를 설치하여 위도,경도 좌표계로 변환하였습니다. 다만 전국 데이터를 모두 하기엔 용량이 너무 커서, 시간관계상 서울지역 데이터만 변환해두었습니다. 그리고 후보지역으로 추출된 주택을 지도에 표시하는 것까지 구현했습니다. 

![image](https://user-images.githubusercontent.com/51018363/110056532-5b9b2400-7da2-11eb-89f0-1625673e2931.png)
