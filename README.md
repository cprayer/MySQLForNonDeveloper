# 비개발자를 위한 MySQL

## 데이터란?
데이터란 무언가를 사용하거나 얻기 위한 **재료**라고 할 수 있습니다. 예를들어 의자를 만들기 위해서 필요한 재료의 목록, 만들고자 하는 의자의 크기, 색상 등 이러한 모든 것이 데이터라고 할 수 있습니다. 즉, 필요하다면 모든 것은 데이터가 될 수 있습니다.

## 데이터의 종류
이러한 데이터에도 종류는 있습니다. 크게 두 가지로 나눌 수 있습니다

1. **정형 데이터**
2. **비정형 데이터**

이 외에도 반정형 데이터라는 것이 존재하지만 반정형 데이터는 논외로 치겠습니다.
정형 데이터는 **定型**이라는 한자가 의미하듯이 일정한 형식이나 틀에 맞춰서 작성된 데이터를 의미합니다. 흔히 주변에서 많이 사용하는 엑셀에서 작성된 데이터 시트도 정형 데이터에 속합니다. 

그럼 비정형 데이터는 정형 데이터의 반대겠죠? 비정형 데이터는 일정한 형식이 없는 데이터를 의미합니다. 마구잡이로 적혀있는 SNS의 텍스트들, 사진, 동영상 등이 있습니다.

###### 정형 데이터와 비정형 데이터의 예
<table>
  <tr><td align='center'><b>정형 데이터</b></td><td align='center'><b>비정형 데이터</b></td></tr>
  <tr>
    <td width='50%'>
      <table>
        <tr><td>이름</td><td>주문메뉴</td><td>만족도</td></tr>
        <tr><td>이선협</td><td>스테이크</td><td>10</td></tr>
        <tr><td>김지환</td><td>양갈비</td><td>5</td></tr>
        <tr><td>윤명근</td><td>가지구이</td><td>8</td></tr>
      </table>
    </td>
    <td>
      <img src='https://github.com/kciter/MySQLForNonDeveloper/blob/master/Images/unstructured_data_sns.png?raw=true'>
    </td>
  </tr>
</table>

## 데이터베이스
데이터베이스는 앞서 설명한 데이터들의 모음입니다. 데이터베이스에도 다양한 종류가 있지만 여기서는 관계형 데이터베이스에 대해서 설명하겠습니다. 관계형 데이터베이스는 

## MySQL이란?
MySQL이란 관계형 데이터베이스 관리 시스템입니다. 이렇게 말하면 잘 이해가 안가죠? 좀 더 쉽게 풀어서 설명하자면 서로 **관계**가 있고 **정형**화된 데이터를 모은 것을 관리해주는 시스템! 입니다. 아무래도 이것도 이해하기는 조금 어렵죠?

<img src='https://github.com/kciter/MySQLForNonDeveloper/blob/master/Images/restaurant_database_example.png?raw=true' width='500px'>

그림을 보며 이해해봅시다. 위 그림은 '우리 가게'라는 음식점을 데이터베이스를 간단하게 표현한 그림입니다. 데이터베이스 내에 존재하는 **손님**, **예약자**, **매출**, **메뉴**는 각각 '우리 가게' 데이터베이스 내에 존재하는 테이블입니다. 각각의 테이블 내에는 해당 테이블과 관련된 데이터가 들어가 있습니다. 그리고 테이블은 열에 해당하는 컬럼(Column)과 

처음 들어보는 용어들이 많죠? 먼저 용어정리를 하고 시작합시다.
* 데이터베이스
* 테이블
* 
