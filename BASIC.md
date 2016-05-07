###### 비개발자를 위한 MySQL
# SELECT 기초

우리는 분석을 하기 위해 데이터를 가져올 필요가 있습니다. 이번 장에서 데이터베이스에서 데이터를 가져오는 방법을 알아봅시다.

## SQL
MySQL에서는 데이터베이스에서 데이터를 읽고 쓰기 위해서 **SQL**이라는 **언어**를 사용합니다. SQL은 데이터베이스를 위해 만들어진 질의어(Query Language)로 말 그대로 데이터베이스에 [질의](http://krdic.naver.com/detail.nhn?docid=36205500)하듯이 사용할 수 있습니다. 잠깐 어떤식으로 사용하는지 엿볼까요?

```sql
SELECT name, age FROM customers;
```

`전혀 질문하듯이 사용하지 않는데?` 하실 수 있습니다. 하지만 이정도면 프로그래밍 세계에서 정말 이해하기 쉬운 편입니다! 사실 조금만 익숙해지면 누구든지 이용할 수 있는 사용하기 쉬운 언어입니다. 위 문장을 조금만 더 들여다봅시다.

SELECT는 '선택하다'라는 뜻을 가지고 있습니다. 또 FROM은 '~로 부터'라는 뜻을 가지고 있습니다. 조합해보면 `이름(name)과 나이(age)를 고객들(customers)로 부터 선택하다`를 의미합니다. 영어 문법이랑 비슷하죠?

그럼 이제 SELECT에 대해서 좀 더 자세히 알아보겠습니다.

## 기초 문법
SELECT는 MySQL에서 데이터를 가져오기 위해서 사용하는 명령어 입니다. 데이터를 삽입할 때는 INSERT, 수정할 때는 UPDATE, 삭제할 때는 DELETE를 사용합니다. 우리는 데이터 분석을 하기 위해 데이터를 가져와야하기 때문에 SELECT에 대해서 자세히 알아보겠습니다.

```sql
SELECT * FROM table;
```

가장 기초적인 문법입니다. `table에서 모든 것을 가져오겠다.`라는 의미를 가지고 있습니다. \*은 와일드 카드(Wild card)로 **모든 것**을 의미합니다. ;은 명령을 마칠때 사용합니다. 문장을 마칠 때 쓰는 '.'와 비슷합니다. 좀 더 자세히 뜯어봅시다.

```sql
 SELECT        *       FROM table;
#선택한다      모든것을    table로 부터
```

여기서 `*`과 `table` 부분은 바뀔 수 있습니다. `SELECT`와 `FROM`은 예약어로 문법에서 이미 이 단어는 무엇에 사용할 것이다라고 정의해 놓은 단어기 때문에 바꿀 수 없습니다.<br>
`*` 부분은 `table`에서 정의된 컬럼을 적는 부분입니다. 만약 `name`과 `age` 컬럼이 `table`에 있다면 `*`을 적었을 때 `name`과 `age`에 대한 로우를 모두 볼 수 있습니다. 만약 여기서 `*`을 `name`로 바꾼다면 `age`는 볼 수 없고 `name`에 대한 로우만 볼 수 있습니다. 필요하지 않은 데이터를 출력할 경우 분석에 혼란을 야기할 수 있기 때문에 `*` 부분을 잘 정의하는 것이 중요합니다. 정의되지 않은 컬럼 이름을 넣을 경우에는 문법 에러가 나게됩니다.<br>
`table` 부분은 정의된 테이블의 이름을 넣으면 됩니다. 만약 `customers`과 `menus`라는 테이블이 있다면 `table`자리에 `customers`와 `menus`를 넣을 수 있습니다. 그 외에 정의되지 않은 테이블 이름을 적을 경우 문법 에러가 나게됩니다.

## 에러
MySQL을 이용하다보면 많은 에러를 볼 수 있습니다. SELECT에 대해서 더 자세히 알아보기 전에 에러 유형을 살펴보면 앞으로 공부할 때 에러 때문에 삽질하는 일이 줄어들 수 있습니다.

1. 오타
  * 초심자들이 가장 많이 내는 에러입니다. SQL 실행을 했을 때 에러가 났다면 테이블 이름을 틀렸거나 컬럼의 이름을 틀리지 않았는지 확인해봅시다. 예약어는 파란색으로 하이라이팅 되므로 만약 하이라이팅되지 않았다면 오타가 났는지 살펴봅시다.
2. 순서
  * 영어 문법을 보면 주어 자리, 동사 자리, 형용사 자리 등 순서가 맞아야 합니다. SQL도 마찬가지 입니다. 아직은 간단한 문법만 배웠지만 심화된 내용을 보면 SELECT와 FROM외에도 많은 예약어가 있습니다. 이런 예약어에도 순서가 있습니다. 순서는 [이곳](http://dev.mysql.com/doc/refman/5.7/en/select.html)에서 자세히 볼 수 있습니다.
3. 사용법
  * 후에 IS, LIKE, IN등을 배울 때 사용법이 틀려서 제대로 데이터가 안나오는 경우가 있습니다. 사용법에 유의합시다.

## 작성중
영어 문장 구조를 나타낼때 말하는 5가지 형식에 대해서 아시나요? MySQL에도 5형식과 같이 다양하게 구성할 수 있습니다.<br>
SELECT 문법을 영문 5형식에 비유하여 설명해보겠습니다.

1. 1형식
  ```sql
  SELECT * FROM customers;
  ```
  가장 기본적인 문법입니다. custo