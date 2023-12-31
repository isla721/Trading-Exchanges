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
spread가 크고, incoming market order가 적을 때, 시장가 주문을 하면 price improvement(현재 시장가격보다 더 높은 가격으로 매도 혹은 더 낮은 가격으로 매수)가 일어날 수 있다

#### 4.3.3 Market Impact
- price concessions: 많은 물량을 매도 혹은 매수할 때 덧붙이거나 할인하는 가격
- 많은 물량을 매매하는 건 시장(가격)의 변화를 가져오지만, liquidity가 높은 market일 수록 대량 매매에도 price impact가 적다.

#### 4.3.4 Execution Price Uncertainty
시장가 주문을 하면 실제로 어떤 가격에 매매될 지 불확실하다는 특징이 있다

### 4.4 Limit orders
지정가 주문은 주문자가 특정 가격으로 거래를 하려고 할 때 사용됩니다.
주문이 시장 가격에 즉시 체결되지 않고, 지정된 가격까지 가격이 이동할 때까지 대기합니다.
주문자는 원하는 가격에 거래를 하지만, 가격이 도달하지 않을 경우 주문이 체결되지 않을 수 있습니다.
- limit order book
  - 체결되지 않은 채 기다리고 있는 limit order 목록이 기록된 파일
- A limit order is an instruction to trade at the best available, but only if it is no worse than the limit price specified by the trader.
- buy limit orders with high prices and sell limit orders with low prices are **aggressively priced**.
#### 4.4.1 Limit Price Placement
- Terms Traders Use to Describe Standing Limit Orders
![Terms Traders Use to Describe Standing Limit Orders](4.2.png)
- marketable limit order
  - an order that the broker can execute immediately when a trader submits it
#### 4.4.2 Standing Limit Orders Are Trading Options That Offer Liquidity
standing limit order 를 liquidity 를 제공하는 option 으로 바라봐보자.
- standing limit order가 option이 되는 이유: since traders can choose whether they want to trade with a standing limit order, standing limit orders are options to trade.
  - sell limit orders -> call options (사람들에게 사고싶을 때 살 수 있는 기회를 준다)
  - buy limit orders -> put options (사람들에게 팔고싶을 때 팔 수 있는 기회를 준다)
- standing limit order vs option contracts
  - option contract는 특정 buyer와 하는 약속이고 premium 이 있지만, standing limit order는 buyer(or seller)를 찾는 것을 market에 맡겨둠으로써 누구나 option을 얻을 수 있게 한다.
  - option value (to trade) of limit order는 limit price, how long the orders will stand, price volatility 에 따라 결정된다.
- Option value: 특정 가격으로 주식 또는 다른 금융 자산을 거래하려는 정도
  - limit price가 market과 가까울수록 value가 높다.
  - trader가 limit order 가 오래 남아 있을 거라고 예상한다면 (-> volatility가 높아지는 것이기 때문), option value가 높아진다.
  - price volatility가 높을 수록 option value가 높다.
#### 4.4.3 The Expected Compensation for Offering Liquidity
- limit order를 submit 하는데 대한 compensation은 a better price!
- trading을 얼른 하고 싶은 사람이라면, they will have to chase the price.
#### 4.4.4 The Risk of Using Standing Limit Orders
- execution uncertainty
  - 언제 체결될 지 알 수 없다는 불확실성
- ex post regret
  - If prices change before they can restore their original position, they will lose money and regret.
  - adverse selection risk is the most important cause of ex post regret.
  - 지정가를 시장가와 크게 차이를 둔다면, 거래 체결 후 후회할 가능성이 적긴 하다
#### 4.4.5 Limit Orders Represent Absent Traders
많은 trader들이 limit order를 사용하는 이유는, broker에게 자기가 원하는 바를 전달하기 위함이다. 브로커가 대신 마켓 보고 trading해주면 이들은 그 시간에 다른 일을 할 수 있음
### 4.5 Stop orders
- orders with stop instruction are called stop orders.
- stop instruction stops an order from executing until price reaches a stop price specified by the trader.
- limit order와의 차이점: limit order와 반대 방향의 limit이라고 생각하면 된다.
  - 예를 들어, 어떤 trader가 한 주식을 10달러 이상이 되면 사고 싶고, 10.37 이상이면 사지 않고 싶을 땐 => 10 stop, 10.37 limit 으로 buy order를 내야 한다. // 근데 이런 경우는 극히 드물겠다. 굳이 10 달러 이상일 때 사야할 이유는 없을 거 같은데.. 더 싸게 사면 좋을 테니~ => 여기를 보니 이럴 수 있겠음. 예를 들어, 10 달러 이상으로 올랐을 경우엔 더 오를 가능성이 있다고 판단하여, 10.2 달러 이하에서 바로 사도록 하면 10달러 정도에 살 수 있겠지.
- commonly use case: price가 자기의 예상과 반대 방향으로 갈 경우 손절하기 위해. 이런 order를 stop loss order 라 부름.
- limit sell order with limit price 5000won => 대개 현재 가격이 5000won 아래일 때 주문을 제출한다. (better price)
- stop sell order with stop price 5000won => 대개 현재 가격이 5000won 이상일 때, 큰 손해를 방지하기 위해 제출한다. (stop loss price)
- stop price와 limit price가 같이 있는 것은 stop limit order.
  - sell order example: 현재 가격이 5달러인데, 만약 4.8 달러 이하로 떨어진다면 4.5달러 이상에선 사고 싶을 때 => 4.8 stop price, 4.5 limit price
  - buy order example: 현재 가격이 5달러인데, 이게 어떤 모멘텀을 가지려면 적어도 5.5 달러 이상은 되어야 사고 싶을 때, 그런데 또 5.9 달러 이하로만 사고 싶을 때 => 5.5 stop price, 5.9 limit price
- 대개는 마켓에 momentum을 더해서, price를 더 불안정하게(destabilize) 만드는 경향이 있다.
  - momentum trading strategies: 오를 때 사고, 떨어질 때 판다. => destabilize prices
  - contrarian traders: 떨어질 때 사고, 오를 때 판다. => stabilize prices

### 4.6 Market-if touched orders
이 주문은 지정된 가격이 도달되면 시장 주문으로 자동 변환되는 특징을 가지고 있습니다. 
- 그 가격을 touch하기만 하면 market order가 되는 order.
- Market-if touched orders: trader는 현재 price가 touch price로 떨어지고 있을 때 buy order를 넣고, 현재 price가 touch price로 올라가고 있을 때 sell order를 넣는다. 
- stop order: 현재 price가 stop price로 올라가고 있을 때 buy order를 넣고, 현재 price가 stop price로 떨어지고 있을 때 sell order를 넣는다
- limit order와의 차이점은? limit order는 trading 가격이 언제나 limit price보다 좋지만(better), market-if-touched order는 market order 가 되어서 touch price보다 좋지 않을 수 있지.
- limit order가 아닌 market-if-touched orders 를 쓰는 경우는? trader가 해당 가격을 닿기만 하면 바로 거래를 하기 원할 때 사용한다. (for some impatient traders...)

### 4.7 Tick-sensitive orders
틱-민감 주문은 가격의 틱(tick) 변동에 따라 주문이 활성화되는 주문 유형입니다.
일정한 가격 간격(틱)으로 주문이 활성화되고 체결됩니다.
예를 들어, 주가가 1달러씩 상승할 때마다 주문이 활성화되고 체결될 수 있습니다.
### 4.8 Market-not-held orders
시장-유지 주문은 주문 접수자가 주문의 체결 가격을 결정할 수 있는 특별한 주문 유형입니다.
주문을 시장에 보내지만 주문 실행 가격은 주문을 받은 측이 판단하게 됩니다. 주문을 받은 측은 최선의 시장 조건을 기다릴 수 있습니다.

### 4.11 Summary
- the most important and most common order types are market order, limit order.
- market order 는 가격에 대한 uncertainty를, limit order는 거래 일시에 대한 uncertainty를 갖고있다.
- limit order는 대개 유동성을 제공하고, market order는 대개 유동성을 take!