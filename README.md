## 프로젝트 이름 및 설명:
"Crime Visualization Map using Python and Folium"

## 프로젝트 소개:
"이 프로젝트는 뉴스 데이터를 활용하여 범죄 발생 지역을 지도에 시각화하는 것을 목표로 합니다."

## 설치 방법:
 "아래 명령을 사용하여 필요한 라이브러리를 설치하세요:"
 pip install folium requests beautifulsoup4

## 사용법:
"main.py 파일을 실행하여 뉴스 데이터를 수집하고 지도에 마크로 표시합니다."

## 예제:
"아래 코드는 crime_location 리스트에 사건 정보를 저장하고 지도에 마크를 추가하는 부분입니다:"

for crime_info in crime_location:
    folium.Marker(
        location=[crime_info['위도'], crime_info['경도']],
        icon=folium.Icon(color=colors[crime_info['사건']], icon='info-sign'),
        popup=f"{crime_info['사건']} 사건\n지역: {crime_info['지역']}"
    ).add_to(m)

## 출력 결과 예시
![사건사고](https://github.com/Leekhoo/crime_map/assets/137920352/073e707a-df84-44c5-8b08-d33f5050821c)
