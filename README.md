# Analysis-with-SK-SafeCaster

SK OPEN API에서 제공을 해주는 SafeCaster데이터 즉, COVID-19 안전지수를 수집하여 시각화 후 분석 <br />
API WEB : https://openapi.sk.com/ 

<h2>데이터 수집 과정 </h2>
<p>
  1. SafeCaster API의 법정동 ID 를 수집<br />
  2. SafeCaster API의 <코로나19 안전 지수 (법정동)>를 통해 특정 날의 00시 부터 23시까지의 안전지수를 수집<br />
  3. 시각화를 위한 위, 경도 좌표를 T MAP API를 통하여 수집<br />
  4. 각각 수집한 데이터를 하나의 DataFrame으로 병합 후 저장
</p>
  
<h2> 데이터 시각화 </h2>
  1. Python folium Module의 지도에 Marker 형태로 지정<br />
  2. 수집된 데이터의 00시부터 23시까지의 안전지수 값들로 평균을 구하여 Marker의 색상을 지정<br />
  3. Python vincent Module로 각 지역의 데이터를 Marker에 popup시 표현될 그래프 형태로 변환<br />

<h3> 안전지수 평균에 따른 색상 </h3>
<img src='https://user-images.githubusercontent.com/68526662/123539652-c3241780-d775-11eb-80e9-fc817d02ced5.PNG'>

