# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전

### 공통
| 한글명 | 영문명     | 설명               |
|-----|---------|------------------|
| 비속어 | profanity | 욕설로 이름에 포함되면 안되는 단어 |

### 상품
| 한글명 | 영문명     | 설명               |
|-----|---------|------------------|
| 상품  | product | 메뉴의 구성요소 예) 후라이드 |
| 가격  | price   | 상품의 가격           |

### 메뉴
| 한글명    | 영문명          | 설명                                  |
|--------|--------------|-------------------------------------|
| 메뉴     | menu         | 하나 이상의 상품으로 구성된 집합, 구매는 메뉴 단위로 이루어짐 |
| 전시     | display      | 메뉴를 전시하여 손님이 주문할 수 있는 상태여부          |
| 비전시    | hide         | 메뉴를 비전시하여 손님이 주문할 수 없는 상태여부         |
| 메뉴구성상품 | menu product | 메뉴를 구성하는 상품들                        |
| 가격  | price   | 메뉴의 가격                              |
| 메뉴그룹   | menu group  | 메뉴를 유사한 유형에 따라 분류한 집합 예) 세트메뉴       |

### 주문 테이블
| 한글명      | 영문명              | 설명                                             |
|----------|------------------|------------------------------------------------|
| 테이블      | order table      | 매장 주문한 손님이 식사하는 테이블. 주문 테이블을 할당받아야 매장 주문이 가능하다 |
| 테이블 착석   | sit              | 주문 테이블에 손님이 앉는다                                |                                
| 테이블 청소   | clear            | 주문 테이블을 치운다                                    |
| 손님 수     | number of guests | 방문한 손님 수                                       |                                                             
| 테이블 사용 여부 | occupied | 테이블 사용 여부                                      |                                                             

### 주문
| 한글명    | 영문명             | 설명              |
|--------|-----------------|-----------------|
| 주문 유형  | order type      | 주문의 상태          |
| 주문 상태  | order status    | 손님이 주문할 수 있는 방법 |
| 주문된 메뉴 | order line item | 주문을 할 때 선택된 메뉴  |  

#### 배달 주문
| 한글명     | 영문명              | 설명                                  |
|---------|------------------|-------------------------------------|
| 주문      | order            | 손님이 배달로 음식을 받도록 신청한 주문              |
| 배달지 주소  | delivery address | 배달 될 음식이 도착할 주소                     |
| 배달      | delivery         | 손님이 원하는 장소로 음식을 보내주는 행위             |
| 접수      | waiting          | 손님이 주문을 요청하고, 매장이 주문을 접수하기 전의 주문 상태 |
| 접수 완료   | accepted         | 매장에서 주문을 접수한 주문 상태                   |
| 음식 완료   | served           | 접수된 음식이 다 만들어진 상태                   |
| 배달 시작   | delivering       | 배달이 시작된 상태                          |
| 배달 완료   | delivered        | 배달이 완료된 상태                          |
| 주문 완료   | completed        | 배달이 고객에게 전달되고 주문이 종료가 된 상태          |
| 배달 대행사	 | kitchen rider    | 배달 대행 업체                            |

#### 포장 주문
| 한글명    | 영문명            | 설명                                   |
|--------|----------------|--------------------------------------|
| 주문     | order          | 손님이 매장에서 음식을 가져가는 방법으로 신청한 주문        |
| 접수 대기  | waiting        | 손님이 주문을 요청하고, 매장에서 주문을 접수하기 전의 주문 상태 |
| 접수 완료  | accepted       | 매장에서 주문을 접수한 주문 상태                   |
| 서빙 완료  | served         | 접수된 음식이 다 만들어진 상태                    |
| 주문 완료   | completed      | 손님이 음식을 가져간 상태로 주문이 종료된 상태           |

#### 매장 주문
| 한글명    | 영문명         | 설명                                             |
|--------|-------------|------------------------------------------------|
| 주문     | order       | 손님이 원하는 상품을 구매하는 행위                            |
| 테이블 | order table | 매장 주문한 손님이 식사하는 테이블. 주문 테이블을 할당받아야 매장 주문이 가능하다 |
| 접수 대기  | waiting     | 손님이 주문을 요청하고, 매장에서 주문을 접수하기 전의 주문 상태           |
| 접수 완료  | accepted    | 매장에서 주문을 접수한 주문 상태                             |
| 서빙 완료  | served      | 접수된 음식이 매장 내 손님에게 전달 된 상태                      |
| 주문 완료  | completed   | 손님이 음식을 다 먹고 주문 테이블도 정리된 상태                    |


## 모델링

### 상품 (*Product*)

#### 속성
- price (가격)
  - price 는 0원 이상이어야 한다.
- name (이름)
  - name 은 비어있을 수 없으며, 비속어가 포함될 수 없다. 

#### 행위
- Product 를 등록할 수 있다.
- Product 의 price 를 변경할 수 있다.
  - Menu 의 가격이 MenuProduct 들의 가격의 합보다 크면 Menu 가 hide 된다.

### 메뉴 (*Menu*)

#### 속성
- price (가격)
  - price 는 0원 이상이어야 한다.
- name (이름)
  - name 은 비어있을 수 없으며, 비속어가 포함될 수 없다.
- menuGroup (메뉴그룹)
  - menuGroup 의 이름은 비워 둘 수 없다.
- menuProduct (메뉴 구성 상품)
  - menuProduct 의 수량은 0 이상이어야 한다.
  - Menu 의 모든 menuProduct 가격의 합이 price 보다 이하이어야 한다.
- displayed (전시여부)

#### 행위
- menuGroup 을 등록할 수 있다.
- Menu 를 등록할 수 있다.
  - 특정 menuGroup 에 속해야 한다.
- Menu 의 price 를 변경할 수 있다.
- Menu 를 display 를 true 로 할 수 있다.
- Menu 를 display 를 false 로 변경 할 수 있다.
- Product 의 price가 변경될 때, Menu 의 가격이 MenuProduct 들의 가격의 합보다 크면 Menu 가 hide 된다.


### 주문 테이블 (*Order Table*)

#### 속성
- name (이름)
  - name 은 비어있을 수 없다.
- numberOfGuests (손님 수)
  - numberOfGuests 는 0 이상이어야 한다.
- occupied (테이블 사용 여부)

#### 행위
- OrderTable 을 등록할 수 있다.
- OrderTable 을 점유 상태로 설정할 수 있다.
- OrderTable 을 clear 할 수 있다.
  - numberOfGuests 를 0으로 변경한다.
  - occupied 를 false 로 변경한다.
  - Order 가 완료되지 않는 경우 clear 할 수 없다.
- OrderTable 의 손님 수를 변경할 수 있다.
  - occupied 가 true 이어야 한다.

### 주문 (*Order*)

#### 주문된 메뉴 (*OrderLineItem*)
- orderLineItem
  - Menu 는 등록이 되어있어야 한다.
  - delivery, takeout 의 경우 Order 의 quantity는 0 이상이어야 한다.

#### 배달 주문 (*Delivery Order*)

##### 속성
- deliveryAddress (배달지 주소)
  - deliveryAddress 는 비어있을 수 없다.
- quantity (주문 항목 수량)
  - quantity는 0 이상이어야 한다.
- orderType (주문 상태)
  - orderType 은 delivery 이다.
- orderStatus (주문 상태)
  - waiting -> accepted -> served -> delivering -> delivered -> completed 의 순서를 가진다.

##### 행위
- DeliveryOrder 을 등록할 수 있다.
  - orderStatus 를 waiting 으로 변경한다.
  - Menu 의 displayed 가 false 인 경우 주문할 수 없다.
- DeliveryOrder 를 수락할 수 있다.
  - orderStatus 는 waiting 이어야 한다.
  - orderStatus 를 accepted 로 변경한다.
  - 배달을 위해 kitchenRider 를 호출한다.
- DeliveryOrder 의 음식을 다 만들어 완료할 수 있다.
  - orderStatus 는 accepted 이어야 한다.
  - orderStatus 를 served 로 변경한다.
- DeliveryOrder 의 배달을 시작할 수 있다.
  - orderStatus 는 served 이어야 한다.
  - orderStatus 를 delivering 로 변경한다.
- DeliveryOrder 의 배달을 완료할 수 있다. 
  - orderStatus 는 delivering 이어야 한다.
  - orderStatus 를 delivered 로 변경한다.
- DeliveryOrder 를 완료할 수 있다.
  - orderStatus 는 delivered 이어야 한다.
  - orderStatus 를 completed 로 변경한다.

#### 포장 주문 (*Takeout Order*)

##### 속성
- quantity (주문 항목 수량)
  - quantity는 0 이상이어야 한다.
- orderType (주문 상태)
  - orderType 은 takeout 이다.
- orderStatus (주문 상태)
  - waiting -> accepted -> served -> completed 의 순서를 가진다.

##### 행위
- TakeoutOrder 을 등록할 수 있다.
  - orderStatus 를 waiting 으로 변경한다.
  - Menu 의 displayed 가 false 인 경우 주문할 수 없다.
- TakeoutOrder 를 접수 완료할 수 있다.
  - orderStatus 는 waiting 이어야 한다.
  - orderStatus 를 accepted 로 변경한다.
- TakeoutOrder 의 서빙할 수 있다.
  - orderStatus 는 accepted 이어야 한다.
  - orderStatus 를 served 로 변경한다.
- TakeoutOrder 를 완료할 수 있다.
  - orderStatus 는 served 이어야 한다.
  - orderStatus 를 completed 로 변경한다.

#### 매장 주문 (*Eat-in Order*)

##### 속성
- orderTable (주문 테이블)
  - 점유하고 있어야 한다.
- orderType (주문 상태)
  - orderType 은 eat-in 이다.
- orderStatus (주문 상태)
  - waiting -> accepted -> served -> completed 의 순서를 가진다.

##### 행위
- EatInOrder 을 등록할 수 있다.
  - orderStatus 를 waiting 으로 변경한다.
  - Menu 의 displayed 가 false 인 경우 주문할 수 없다.
- EatInOrder 를 접수 완료할 수 있다.
  - orderStatus 는 waiting 이어야 한다.
  - orderStatus 를 accepted 로 변경한다.
- EatInOrder 의 서빙할 수 있다.
  - orderStatus 는 accepted 이어야 한다.
  - orderStatus 를 served 로 변경한다.
- EatInOrder 를 완료할 수 있다.
  - orderStatus 는 served 이어야 한다.
  - orderStatus 를 completed 로 변경한다.
  - orderTable 을 clear 할 수 있다.
