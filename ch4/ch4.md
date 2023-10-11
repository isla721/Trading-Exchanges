# Chapter 4 Orders and Order Properties
Order는 trading의 기본 요소이다. 이번 장에서는 주문이 무엇인지, 주문들의 종류와 주문별 특징에 대해 알아본다.

### 4.1 What are orders and why do people use them?
order always specifies:
- which instrument(s) to trade,
- how much to trade,
- whether to buy or sell
- conditions that trade must satisfy:
    - limit prices that the trader will accept
    - how long the order is valid
    - when the order can be executed
    - whether it is ok to partially fill the order,
    - where to present the order
    - how to search for the other side

### 4.2 Some important terms
1. bids and offers
   - bidding price: 구매 가격
   - offering price, asking price: 판매 가격
2. firm/soft price
   - firm: 특정 금액으로만 거래하겠다는 의미(일반적)
   - soft: 거래 전에 가격 수정이 가능하다는 의미
3. best price
   - best bid (market bid): the highest bid price
   - best ask (best offer, market ask, market offer): the lowest offer price
   - BBO(Best Bid and Offer), NBBO(National Best Bid and Offer)
     - (best는 서로 상대방에게 좋은 가격이라고 생각하면 됨)
   - best bid - best ask = bid/ask spread (inside spread)
4. offering liquidity
   - buying and selling order는 각각 상대방에게 살 수 있는, 팔 수 있는 기회를 제공하기 때문에 liquidity를 제공하는 것이다.
   - offering 은 selling과 동의어로 쓰이기도 하고, liquidity를 제공하는 데 쓰이기도 한다
5. standing/expired orders
   - standing orders(=open order): 거래 상대방이 나타나길 기다리는 주문
   - expired orders: 거래 상대방을 만나지 못하고 만료된 주문
6. demanding/taking liquidity
   - demand liquidity
     - Traders who want to trade quickly *demand liquidity*.
   - take liquidity
     - Trader *take liquidity* when they accept offers.
7. agency/proprietary order
   - agency order
      - 대리 주문은 중개인, 브로커, 또는 거래소의 중립적인 역할을 하는 중개업체를 통해 시장에 주문을 전달하는 주문 유형입니다.
   - proprietary order: 
      - 금융 기관이나 자산 운용 회사가 자체 자본을 사용하여 시장에서 주문을 실행하는 주문 유형입니다.
8. pending/working
   - pending: broker에게 주문을 넣었지만 broker가 수락하기 전 상태
   - working: broker가 주문을 수락했지만 아직 action을 하기 전 상태

### 4.3 Market orders
시장 주문은 가능한 가장 빠른 시간에 주문을 실행하기 위해 사용됩니다.
주문이 시장 가격으로 즉시 체결되며, 현재 시장 가격에 있는 최고 매도 가격에서 살 수 있거나 최저 매수 가격에서 팔 수 있습니다.
주문이 빠르게 실행되지만 체결 가격은 보장되지 않으며, 주문이 대량 거래일 때 슬리피지(slippage)가 발생할 수 있습니다.
#### 4.3.1 Market Orders Pay the Spread
Market Orders Pay the BID/ASK Spread

#### 4.3.2 Price Improvement
spread가 크고, incoming market order가 적을 때, price improvement(현재 시장가격보다 더 높은 가격으로 매도 혹은 더 낮은 가격으로 매수)가 일어날 수 있다

#### 4.3.3 Market Impact
- price concessions: 많은 물량을 매도 혹은 매수할 때 덧붙이거나 할인하는 가격
- 많은 물량을 매매하는 건 시장(가격)의 변화를 가져오지만, liquidity가 높은 market일 수록 대량 매매에도 price impact가 적다.

#### 4.3.4 Execution Price Uncertainty
시장가 주문을 하면 실제로 어떤 가격에 매매될 지 불확실하다는 특징이 있다

### 4.4 Limit orders
지정가 주문은 주문자가 특정 가격으로 거래를 하려고 할 때 사용됩니다.
주문이 시장 가격에 즉시 체결되지 않고, 지정된 가격까지 가격이 이동할 때까지 대기합니다.
주문자는 원하는 가격에 거래를 하지만, 가격이 도달하지 않을 경우 주문이 체결되지 않을 수 있습니다.

### 4.5 Stop orders
스톱 주문은 특정 가격에 도달하면 주문을 활성화하는 데 사용됩니다.
주문자가 주가가 특정 가격에 도달할 경우 주문이 시장 주문으로 변환되어 체결됩니다.
스톱 주문은 가격 움직임을 추적하며, 주가가 원하는 방향으로 움직일 때 주문을 활성화시킬 수 있습니다.
### 4.6 Market-if touched orders
이 주문은 지정된 가격이 도달되면 시장 주문으로 자동 변환되는 특징을 가지고 있습니다. 주식이 일정 가격에 도달하면 자동으로 매수나 매도 주문을 실행하고자 할 때 MIT 주문을 사용할 수 있습니다. 스톱 주문은 지정 가격에 도달하면 시장 주문으로 변환되어 주문이 최선의 가격으로 체결되도록 시도되지만, 스톱 주문은 가격이 특정 방향으로 움직이는 동안 활성화되지 않을 수 있습니다. 반면 MIT 주문은 가격이 도달하면 즉시 활성화되며 체결을 시도합니다.
### 4.7 Tick-sensitive orders
틱-민감 주문은 가격의 틱(tick) 변동에 따라 주문이 활성화되는 주문 유형입니다.
일정한 가격 간격(틱)으로 주문이 활성화되고 체결됩니다.
예를 들어, 주가가 1달러씩 상승할 때마다 주문이 활성화되고 체결될 수 있습니다.
### 4.8 Market-not-held orders
시장-유지 주문은 주문 접수자가 주문의 체결 가격을 결정할 수 있는 특별한 주문 유형입니다.
주문을 시장에 보내지만 주문 실행 가격은 주문을 받은 측이 판단하게 됩니다. 주문을 받은 측은 최선의 시장 조건을 기다릴 수 있습니다.