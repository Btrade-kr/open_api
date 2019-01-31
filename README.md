Btrade API
=====

### API Info

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Btrade는 개발자를 위해 API를 제공하여 다양한 앱과 프로그램을 개발할 수 있는 환경을 제공합니다.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;이제 누구나 쉽게 비트레이드에서 제공되는 API를 통하여

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;사용자 정보, 지갑정보, 주문, 거래 내역, 거래 취소 등의 기능을 사용할 수 있습니다.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;또한 지갑 API를 제공하여 암호화폐 유관 서비스를 구축하는데 도움을 드립니다.

&nbsp;

#### 권한 및 주의사항

```


                                               Description


```
&nbsp;

#### Open API 사용 가이드

```


                                               Description


```

&nbsp;
### API 공지

#### Open API  변경사항 안내 (2018. 10. 02)


&nbsp;&nbsp;&nbsp;안녕하세요.

&nbsp;&nbsp;&nbsp;비트레이드 개발자 센터입니다.

&nbsp;&nbsp;&nbsp;Open API 변경 사항에 대해 아래와 같이 안내 드립니다.


##### Open API 변경사항

&nbsp;&nbsp;&nbsp;해당 변경 사항은 __2018.10.10 11:00__ 부터 적용되오니, 해당 내용과 적용 시점을 반드시 확인하시고

&nbsp;&nbsp;&nbsp;적용해주시기 바랍니다.

&nbsp;

&nbsp;

### Reference

#### Public API
---

#### Ticker - 거래소 마지막 거래 정보

__[GET]__ &nbsp;&nbsp;&nbsp;http://api.btrade.co.kr/api/ticker/currency/BTC

__[Response Body]__

```
{
  "status": "0000",
  "data": {
    "open_price": "10000",
    "close_price": "10000",
    "low": "10000",
    "high": "10000",
    "average_price": "0.0",
    "units_traded": "0E-18",
    "volume_1day": "0E-18",
    "volume_7day": "431.699880000000000000",
    "buy_price": "0000000000.00000000",
    "sell_price": "0000000000.00000000",
    "date": 1548933680756
  }
}
```

__[Input Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|currency|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;코인명 (ALL, BTC, ETH, ETC, LTC, ZEC)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

__[Output Parameters]__

|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Key Name&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|status: 0000|정상|
|open_price|최근 24시간 내 시작 거래금액|
|close_price|최근 24시간 내 마지막 거래금액|
|low|최근 24시간 내 최저 거래금액|
|High|최근 24시간 내 최고 거래금액|
|average_price|최근 24시간 내 평균 거래금액|
|units_traded|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;최근 24시간 내 Currency 거래량&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|
|volume_1day|최근 1일간 Currency 거래량|
|volume_7day|최근 7일간 Currency 거래량|
|buy_price|거래 대기건 최고 구매가|
|sell_price|거래 대기건 최소 판매가|
|date|현재 시간 Timestamp|
|status: 0001|시세 정보 누락|
|status: 0002|구매 가격 정보 누락|
|status: 0003|판매 가격 정보 누락|


&nbsp;

#### Orderbook - 거래소 판/구매 등록 대기 또는 거래 중 내역 정보

__[GET]__ &nbsp;&nbsp;&nbsp;http://localhost:9999/api/orderbook/currency/BTC

__[Response Body]__
````
{
  "status": "0000",
  "data": {
    "timestamp": 1548934145839,
    "order_currency": "BTC",
    "payment_currency": "KRW",
    "bids": [
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "buy",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      }
    ],
    "asks": [
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      },
      {
        "it_action": "sell",
        "it_market_cost": "0000000000.00000000",
        "nResCoin": "00000000.00000000"
      }
    ]
  }
}
````


__[Input Parameter]__

|&nbsp;&nbsp;&nbsp;Parameter Name&nbsp;&nbsp;&nbsp;|Description|
|:------------:|:---------:|
|currency|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;코인명 (ALL, BTC, ETH, ETC, LTC, ZEC)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

&nbsp;

&nbsp;

#### Token
---

#### Create - 최초 토큰 생성

__[POST]__ &nbsp;&nbsp;&nbsp;

```
{
  "deal_money":0.0,
  "amount":0.0,
  "nonce":"1548934309845",
  "hstr":"5bd7e54326f613f40c337493c73cd8dd67923108f67288e8d5fac3c30c9bd1af",
  "apikey":"BTdp2vE53tEb5YwcU41A2w1SYLWCjqKbwpW",
  "grant_type":"APIKEY",
  "expires_in":60
}
```

__[Response Body]__

```
{
  "status": "0000",
  "message": "success",
  "data": {
    "access_token": "5b6af505cac7cf5e856fdc0f915f2788dc8d12f36e9e2ca1e34ce744ee8add35",
    "access_token_expire": "1548937717809",
    "refresh_token": "69be7fad3b045a9e54da0339dce50eba26c4a65e2a002bf6586b21884b35ad59",
    "refresh_token_expire": "1551526117794"
  }
}
```












