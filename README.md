# 키친포스

## 요구 사항

- 제품
    - [x] 이름과 가격으로 제품을 추가한다
        - [x] 가격은 필수고, 0 이상이어야 한다
        - [x] 이름은 필수고, 비속어가 포함되지 않아야 한다
    - [x] 특정 제품의 식별자와 바꿀 가격으로 제품의 가격을 바꾼다
        - [x] 바꿀 가격은 필수고, 0 이상이어야 한다
        - [x] 제품의 식별자로 특정 제품을 조회할 수 있어야 한다
        - [x] 가격을 바꾼 후 특정 제품을 포함한 모든 메뉴를 조회하여, 메뉴의 가격이 메뉴가 포함한 모든 제품의 (가격 * 수량)의 합보다 크면, 메뉴를 숨긴다
    - [x] 제품 전체 목록을 조회한다
- 메뉴
    - [x] 이름, 가격, 포함될 메뉴 그룹의 식별자, 메뉴 공개여부 및 포함할 제품 정보(식별자, 수량) 목록으로 메뉴를 추가한다
        - [x] 가격은 필수고, 0 이상이어야 한다
        - [x] 포함될 메뉴 그룹의 식별자로 특정 메뉴 그룹을 조회할 수 있어야 한다
        - [x] 포함할 제품 정보 목록은 필수다
        - [x] 포함할 제품 정보 목록에는 하나 이상의 제품 정보가 있어야 한다
        - [x] 포함할 제품 정보 목록의 길이와 포함할 제품의 식별자 목록으로 조회한 제품 목록의 길이는 같아야 한다
        - [x] 포함할 제품의 수량은 0 이상이어야 한다
        - [x] 메뉴의 가격이 포함할 제품의 (가격 * 수량)의 합 이하여야 한다
        - [x] 메뉴의 이름은 필수고, 비속어가 포함되지 않아야 한다
    - [x] 특정 메뉴의 식별자와 바꿀 가격으로 메뉴의 가격을 바꾼다
        - [x] 바꿀 가격은 필수고, 0 이상이어야 한다
        - [x] 메뉴의 식별자로 특정 메뉴를 조회할 수 있어야 한다
        - [x] 바꿀 가격이 특정 메뉴가 포함한 모든 제품의 (가격 * 수량)의 합 이하여야 한다
    - [x] 특정 메뉴의 식별자로 메뉴를 공개한다
        - [x] 메뉴의 식별자로 특정 메뉴를 조회할 수 있어야 한다
        - [x] 메뉴의 가격이 메뉴가 포함한 모든 제품의 (가격 * 수량)의 합 이하여야 한다
    - [x] 특정 메뉴의 식별자로 메뉴를 숨긴다
        - [x] 메뉴의 식별자로 특정 메뉴를 조회할 수 있어야 한다
    - [x] 메뉴 전체 목록을 조회한다
- 메뉴 그룹
    - [x] 이름으로 메뉴 그룹을 추가한다
        - [x] 이름은 필수고, 빈 문자열이 아니어야 한다
    - [x] 메뉴 그룹 전체 목록을 조회한다
- 주문
    - [x] 유형, 주문한 메뉴 정보(식별자, 가격, 수량) 목록 및 배달 주소 또는 주문 테이블의 식별자로 주문을 추가한 후, 
            주문을 대기 상태로, 주문 일시를 현재 시점으로 설정한다
        - [x] 유형은 필수다
        - [x] 주문한 메뉴 정보 목록은 필수다
        - [x] 주문한 메뉴 정보 목록에는 하나 이상의 메뉴 정보가 있어야 한다
        - [x] 주문한 메뉴 정보 목록의 길이와 주문한 메뉴의 식별자 목록으로 조회한 메뉴 목록의 길이는 같아야 한다
        - [x] 유형이 매장내 식사가 아니면 메뉴의 수량은 0 이상이어야 한다
        - [x] 주문한 메뉴는 공개된 메뉴여야 한다
        - [x] 주문한 메뉴의 주문 가격은 주문한 메뉴의 식별자로 조회한 메뉴의 가격과 같아야 한다
        - [x] 유형이 배달이면 배달 주소는 필수고, 빈 문자열이 아니어야 한다
        - [x] 유형이 매장내 식사면 주문 테이블의 식별자로 특정 주문 테이블을 조회할 수 있어야 한다
        - [x] 유형이 매장내 식사면 주문 테이블의 식별자로 조회한 주문 테이블이 공석이 아니어야 한다
    - [x] 특정 주문의 식별자로 주문을 접수하고, 
            주문의 유형이 배달이면 주문의 식별자, 주문한 메뉴의 (가격 * 수량)의 합 및 배달 주소로 배달원을 요청한다
        - [x] 식별자로 특정 주문을 조회할 수 있어야 한다
        - [x] 주문은 대기 상태여야 한다
    - [x] 특정 주문의 식별자로 주문한 메뉴(제품)를 전달한다
        - [x] 식별자로 특정 주문을 조회할 수 있어야 한다
        - [x] 주문은 접수 상태여야 한다
    - [x] 특정 주문의 식별자로 배달 진행을 시작한다
        - [x] 식별자로 특정 주문을 조회할 수 있어야 한다
        - [x] 주문의 유형은 배달이어야 한다
        - [x] 주문은 전달 상태여야 한다
    - [x] 특정 주문의 식별자로 배달을 완료한다
        - [x] 식별자로 특정 주문을 조회할 수 있어야 한다
        - [x] 주문의 유형은 배달이어야 한다
        - [x] 주문은 배달 진행 상태여야 한다
    - [x] 특정 주문의 식별자로 주문을 완료한다
        - [x] 식별자로 특정 주문을 조회할 수 있어야 한다
        - [x] 주문의 유형이 배달이면 주문은 배달 완료 상태여야 한다
        - [x] 주문의 유형이 포장 또는 매장내 식사면 주문은 전달 상태여야 한다
        - [x] 주문의 유형이 매장내 식사면 주문 테이블의 접객 인원을 0으로 바꾼다
        - [x] 주문의 유형이 매장내 식사면 주문 테이블을 공석으로 비운다
    - [x] 주문 전체 목록을 조회한다
- 주문 테이블
    - [x] 이름으로 주문 테이블을 추가 후, 접객 인원을 0으로 초기화하고 공석으로 비운다.
        - [x] 이름은 필수고, 빈 문자열이 아니어야 한다
    - [x] 특정 주문 테이블의 식별자로 주문 테이블을 공석이 아니도록 채운다
        - [x] 식별자로 특정 주문 테이블을 조회할 수 있어야 한다
    - [x] 특정 주문 테이블의 식별자로 주문 테이블을 공석으로 비우고, 접객 인원을 0으로 바꾼다
        - [x] 식별자로 특정 주문 테이블을 조회할 수 있어야 한다
        - [x] 주문 테이블에서 받은 주문이 있다면 해당 주문이 완료 상태여야 한다
    - [x] 특정 주문 테이블의 식별자와 바꿀 접객 인원으로 접객 인원을 바꾼다
        - [x] 접객 인원은 0 이상이어야 한다
        - [x] 식별자로 특정 주문 테이블을 조회할 수 있어야 한다
        - [x] 주문 테이블은 공석이 아니어야 한다
    - [x] 주문 테이블 전체 목록을 조회한다

## 용어 사전

| 한글명 | 영문명 | 설명 |
| --- | --- | --- |
|  |  |  |

## 모델링
