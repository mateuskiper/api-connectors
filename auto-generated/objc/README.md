# SwaggerClient

## REST API for the BitMEX Trading Platform  [View Changelog](/app/apiChangelog)  -  #### Getting Started  Base URI: [https://www.bitmex.com/api/v1](/api/v1)  ##### Fetching Data  All REST endpoints are documented below. You can try out any query right from this interface.  Most table queries accept `count`, `start`, and `reverse` params. Set `reverse=true` to get rows newest-first.  Additional documentation regarding filters, timestamps, and authentication is available in [the main API documentation](/app/restAPI).  _All_ table data is available via the [Websocket](/app/wsAPI). We highly recommend using the socket if you want to have the quickest possible data without being subject to ratelimits.  ##### Return Types  By default, all data is returned as JSON. Send `?_format=csv` to get CSV data or `?_format=xml` to get XML data.  ##### Trade Data Queries  _This is only a small subset of what is available, to get you started._  Fill in the parameters and click the `Try it out!` button to try any of these queries.  - [Pricing Data](#!/Quote/Quote_get)  - [Trade Data](#!/Trade/Trade_get)  - [OrderBook Data](#!/OrderBook/OrderBook_getL2)  - [Settlement Data](#!/Settlement/Settlement_get)  - [Exchange Statistics](#!/Stats/Stats_history)  Every function of the BitMEX.com platform is exposed here and documented. Many more functions are available.  ##### Swagger Specification  [⇩ Download Swagger JSON](swagger.json)  -  ## All API Endpoints  Click to expand a section. 

This ObjC package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.2.0
- Package version: 
- Build package: io.swagger.codegen.languages.ObjcClientCodegen

## Requirements

The SDK requires [**ARC (Automatic Reference Counting)**](http://stackoverflow.com/questions/7778356/how-to-enable-disable-automatic-reference-counting) to be enabled in the Xcode project.

## Installation & Usage
### Install from Github using [CocoaPods](https://cocoapods.org/)

Add the following to the Podfile:

```ruby
pod 'SwaggerClient', :git => 'https://github.com/GIT_USER_ID/GIT_REPO_ID.git'
```

To specify a particular branch, append `, :branch => 'branch-name-here'`

To specify a particular commit, append `, :commit => '11aa22'`

### Install from local path using [CocoaPods](https://cocoapods.org/)

Put the SDK under your project folder (e.g. /path/to/objc_project/Vendor/SwaggerClient) and then add the following to the Podfile:

```ruby
pod 'SwaggerClient', :path => 'Vendor/SwaggerClient'
```

### Usage

Import the following:

```objc
#import <SwaggerClient/SWGApiClient.h>
#import <SwaggerClient/SWGDefaultConfiguration.h>
// load models
#import <SwaggerClient/SWGAPIKey.h>
#import <SwaggerClient/SWGAccessToken.h>
#import <SwaggerClient/SWGAffiliate.h>
#import <SwaggerClient/SWGAnnouncement.h>
#import <SwaggerClient/SWGChat.h>
#import <SwaggerClient/SWGChatChannel.h>
#import <SwaggerClient/SWGCommunicationToken.h>
#import <SwaggerClient/SWGConnectedUsers.h>
#import <SwaggerClient/SWGError.h>
#import <SwaggerClient/SWGErrorError.h>
#import <SwaggerClient/SWGExecution.h>
#import <SwaggerClient/SWGFunding.h>
#import <SwaggerClient/SWGGlobalNotification.h>
#import <SwaggerClient/SWGIndexComposite.h>
#import <SwaggerClient/SWGInlineResponse200.h>
#import <SwaggerClient/SWGInstrument.h>
#import <SwaggerClient/SWGInstrumentInterval.h>
#import <SwaggerClient/SWGInsurance.h>
#import <SwaggerClient/SWGLeaderboard.h>
#import <SwaggerClient/SWGLiquidation.h>
#import <SwaggerClient/SWGMargin.h>
#import <SwaggerClient/SWGOrder.h>
#import <SwaggerClient/SWGOrderBookL2.h>
#import <SwaggerClient/SWGPosition.h>
#import <SwaggerClient/SWGQuote.h>
#import <SwaggerClient/SWGQuoteFillRatio.h>
#import <SwaggerClient/SWGSettlement.h>
#import <SwaggerClient/SWGStats.h>
#import <SwaggerClient/SWGStatsHistory.h>
#import <SwaggerClient/SWGStatsUSD.h>
#import <SwaggerClient/SWGTrade.h>
#import <SwaggerClient/SWGTradeBin.h>
#import <SwaggerClient/SWGTransaction.h>
#import <SwaggerClient/SWGUser.h>
#import <SwaggerClient/SWGUserCommissionsBySymbol.h>
#import <SwaggerClient/SWGUserEvent.h>
#import <SwaggerClient/SWGUserPreferences.h>
#import <SwaggerClient/SWGWallet.h>
#import <SwaggerClient/SWGXAny.h>
// load API classes for accessing endpoints
#import <SwaggerClient/SWGAPIKeyApi.h>
#import <SwaggerClient/SWGAnnouncementApi.h>
#import <SwaggerClient/SWGChatApi.h>
#import <SwaggerClient/SWGExecutionApi.h>
#import <SwaggerClient/SWGFundingApi.h>
#import <SwaggerClient/SWGGlobalNotificationApi.h>
#import <SwaggerClient/SWGInstrumentApi.h>
#import <SwaggerClient/SWGInsuranceApi.h>
#import <SwaggerClient/SWGLeaderboardApi.h>
#import <SwaggerClient/SWGLiquidationApi.h>
#import <SwaggerClient/SWGOrderApi.h>
#import <SwaggerClient/SWGOrderBookApi.h>
#import <SwaggerClient/SWGPositionApi.h>
#import <SwaggerClient/SWGQuoteApi.h>
#import <SwaggerClient/SWGSchemaApi.h>
#import <SwaggerClient/SWGSettlementApi.h>
#import <SwaggerClient/SWGStatsApi.h>
#import <SwaggerClient/SWGTradeApi.h>
#import <SwaggerClient/SWGUserApi.h>
#import <SwaggerClient/SWGUserEventApi.h>

```

## Recommendation

It's recommended to create an instance of ApiClient per thread in a multi-threaded environment to avoid any potential issues.

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```objc

SWGDefaultConfiguration *apiConfig = [SWGDefaultConfiguration sharedConfig];

// Configure API key authorization: (authentication scheme: apiExpires)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"api-expires"];
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
//[apiConfig setApiKeyPrefix:@"Bearer" forApiKeyIdentifier:@"api-expires"];

// Configure API key authorization: (authentication scheme: apiKey)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"api-key"];
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
//[apiConfig setApiKeyPrefix:@"Bearer" forApiKeyIdentifier:@"api-key"];

// Configure API key authorization: (authentication scheme: apiSignature)
[apiConfig setApiKey:@"YOUR_API_KEY" forApiKeyIdentifier:@"api-signature"];
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
//[apiConfig setApiKeyPrefix:@"Bearer" forApiKeyIdentifier:@"api-signature"];


NSNumber* *reverse = @false; // If true, will sort results newest first. (optional) (default to false)

SWGAPIKeyApi *apiInstance = [[SWGAPIKeyApi alloc] init];

// Get your API Keys.
[apiInstance aPIKeyGetWithReverse:reverse
              completionHandler: ^(NSArray<SWGAPIKey>* output, NSError* error) {
                            if (output) {
                                NSLog(@"%@", output);
                            }
                            if (error) {
                                NSLog(@"Error: %@", error);
                            }
                        }];

```

## Documentation for API Endpoints

All URIs are relative to *https://www.bitmex.com/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*SWGAPIKeyApi* | [**aPIKeyGet**](docs/SWGAPIKeyApi.md#apikeyget) | **GET** /apiKey | Get your API Keys.
*SWGAnnouncementApi* | [**announcementGet**](docs/SWGAnnouncementApi.md#announcementget) | **GET** /announcement | Get site announcements.
*SWGAnnouncementApi* | [**announcementGetUrgent**](docs/SWGAnnouncementApi.md#announcementgeturgent) | **GET** /announcement/urgent | Get urgent (banner) announcements.
*SWGChatApi* | [**chatGet**](docs/SWGChatApi.md#chatget) | **GET** /chat | Get chat messages.
*SWGChatApi* | [**chatGetChannels**](docs/SWGChatApi.md#chatgetchannels) | **GET** /chat/channels | Get available channels.
*SWGChatApi* | [**chatGetConnected**](docs/SWGChatApi.md#chatgetconnected) | **GET** /chat/connected | Get connected users.
*SWGChatApi* | [**chatNew**](docs/SWGChatApi.md#chatnew) | **POST** /chat | Send a chat message.
*SWGExecutionApi* | [**executionGet**](docs/SWGExecutionApi.md#executionget) | **GET** /execution | Get all raw executions for your account.
*SWGExecutionApi* | [**executionGetTradeHistory**](docs/SWGExecutionApi.md#executiongettradehistory) | **GET** /execution/tradeHistory | Get all balance-affecting executions. This includes each trade, insurance charge, and settlement.
*SWGFundingApi* | [**fundingGet**](docs/SWGFundingApi.md#fundingget) | **GET** /funding | Get funding history.
*SWGGlobalNotificationApi* | [**globalNotificationGet**](docs/SWGGlobalNotificationApi.md#globalnotificationget) | **GET** /globalNotification | Get your current GlobalNotifications.
*SWGInstrumentApi* | [**instrumentGet**](docs/SWGInstrumentApi.md#instrumentget) | **GET** /instrument | Get instruments.
*SWGInstrumentApi* | [**instrumentGetActive**](docs/SWGInstrumentApi.md#instrumentgetactive) | **GET** /instrument/active | Get all active instruments and instruments that have expired in &lt;24hrs.
*SWGInstrumentApi* | [**instrumentGetActiveAndIndices**](docs/SWGInstrumentApi.md#instrumentgetactiveandindices) | **GET** /instrument/activeAndIndices | Helper method. Gets all active instruments and all indices. This is a join of the result of /indices and /active.
*SWGInstrumentApi* | [**instrumentGetActiveIntervals**](docs/SWGInstrumentApi.md#instrumentgetactiveintervals) | **GET** /instrument/activeIntervals | Return all active contract series and interval pairs.
*SWGInstrumentApi* | [**instrumentGetCompositeIndex**](docs/SWGInstrumentApi.md#instrumentgetcompositeindex) | **GET** /instrument/compositeIndex | Show constituent parts of an index.
*SWGInstrumentApi* | [**instrumentGetIndices**](docs/SWGInstrumentApi.md#instrumentgetindices) | **GET** /instrument/indices | Get all price indices.
*SWGInsuranceApi* | [**insuranceGet**](docs/SWGInsuranceApi.md#insuranceget) | **GET** /insurance | Get insurance fund history.
*SWGLeaderboardApi* | [**leaderboardGet**](docs/SWGLeaderboardApi.md#leaderboardget) | **GET** /leaderboard | Get current leaderboard.
*SWGLeaderboardApi* | [**leaderboardGetName**](docs/SWGLeaderboardApi.md#leaderboardgetname) | **GET** /leaderboard/name | Get your alias on the leaderboard.
*SWGLiquidationApi* | [**liquidationGet**](docs/SWGLiquidationApi.md#liquidationget) | **GET** /liquidation | Get liquidation orders.
*SWGOrderApi* | [**orderAmend**](docs/SWGOrderApi.md#orderamend) | **PUT** /order | Amend the quantity or price of an open order.
*SWGOrderApi* | [**orderCancel**](docs/SWGOrderApi.md#ordercancel) | **DELETE** /order | Cancel order(s). Send multiple order IDs to cancel in bulk.
*SWGOrderApi* | [**orderCancelAll**](docs/SWGOrderApi.md#ordercancelall) | **DELETE** /order/all | Cancels all of your orders.
*SWGOrderApi* | [**orderCancelAllAfter**](docs/SWGOrderApi.md#ordercancelallafter) | **POST** /order/cancelAllAfter | Automatically cancel all your orders after a specified timeout.
*SWGOrderApi* | [**orderClosePosition**](docs/SWGOrderApi.md#ordercloseposition) | **POST** /order/closePosition | Close a position. [Deprecated, use POST /order with execInst: &#39;Close&#39;]
*SWGOrderApi* | [**orderGetOrders**](docs/SWGOrderApi.md#ordergetorders) | **GET** /order | Get your orders.
*SWGOrderApi* | [**orderNew**](docs/SWGOrderApi.md#ordernew) | **POST** /order | Create a new order.
*SWGOrderBookApi* | [**orderBookGetL2**](docs/SWGOrderBookApi.md#orderbookgetl2) | **GET** /orderBook/L2 | Get current orderbook in vertical format.
*SWGPositionApi* | [**positionGet**](docs/SWGPositionApi.md#positionget) | **GET** /position | Get your positions.
*SWGPositionApi* | [**positionIsolateMargin**](docs/SWGPositionApi.md#positionisolatemargin) | **POST** /position/isolate | Enable isolated margin or cross margin per-position.
*SWGPositionApi* | [**positionTransferIsolatedMargin**](docs/SWGPositionApi.md#positiontransferisolatedmargin) | **POST** /position/transferMargin | Transfer equity in or out of a position.
*SWGPositionApi* | [**positionUpdateLeverage**](docs/SWGPositionApi.md#positionupdateleverage) | **POST** /position/leverage | Choose leverage for a position.
*SWGPositionApi* | [**positionUpdateRiskLimit**](docs/SWGPositionApi.md#positionupdaterisklimit) | **POST** /position/riskLimit | Update your risk limit.
*SWGQuoteApi* | [**quoteGet**](docs/SWGQuoteApi.md#quoteget) | **GET** /quote | Get Quotes.
*SWGQuoteApi* | [**quoteGetBucketed**](docs/SWGQuoteApi.md#quotegetbucketed) | **GET** /quote/bucketed | Get previous quotes in time buckets.
*SWGSchemaApi* | [**schemaGet**](docs/SWGSchemaApi.md#schemaget) | **GET** /schema | Get model schemata for data objects returned by this API.
*SWGSchemaApi* | [**schemaWebsocketHelp**](docs/SWGSchemaApi.md#schemawebsockethelp) | **GET** /schema/websocketHelp | Returns help text &amp; subject list for websocket usage.
*SWGSettlementApi* | [**settlementGet**](docs/SWGSettlementApi.md#settlementget) | **GET** /settlement | Get settlement history.
*SWGStatsApi* | [**statsGet**](docs/SWGStatsApi.md#statsget) | **GET** /stats | Get exchange-wide and per-series turnover and volume statistics.
*SWGStatsApi* | [**statsHistory**](docs/SWGStatsApi.md#statshistory) | **GET** /stats/history | Get historical exchange-wide and per-series turnover and volume statistics.
*SWGStatsApi* | [**statsHistoryUSD**](docs/SWGStatsApi.md#statshistoryusd) | **GET** /stats/historyUSD | Get a summary of exchange statistics in USD.
*SWGTradeApi* | [**tradeGet**](docs/SWGTradeApi.md#tradeget) | **GET** /trade | Get Trades.
*SWGTradeApi* | [**tradeGetBucketed**](docs/SWGTradeApi.md#tradegetbucketed) | **GET** /trade/bucketed | Get previous trades in time buckets.
*SWGUserApi* | [**userCancelWithdrawal**](docs/SWGUserApi.md#usercancelwithdrawal) | **POST** /user/cancelWithdrawal | Cancel a withdrawal.
*SWGUserApi* | [**userCheckReferralCode**](docs/SWGUserApi.md#usercheckreferralcode) | **GET** /user/checkReferralCode | Check if a referral code is valid.
*SWGUserApi* | [**userCommunicationToken**](docs/SWGUserApi.md#usercommunicationtoken) | **POST** /user/communicationToken | Register your communication token for mobile clients
*SWGUserApi* | [**userConfirm**](docs/SWGUserApi.md#userconfirm) | **POST** /user/confirmEmail | Confirm your email address with a token.
*SWGUserApi* | [**userConfirmWithdrawal**](docs/SWGUserApi.md#userconfirmwithdrawal) | **POST** /user/confirmWithdrawal | Confirm a withdrawal.
*SWGUserApi* | [**userGet**](docs/SWGUserApi.md#userget) | **GET** /user | Get your user model.
*SWGUserApi* | [**userGetAffiliateStatus**](docs/SWGUserApi.md#usergetaffiliatestatus) | **GET** /user/affiliateStatus | Get your current affiliate/referral status.
*SWGUserApi* | [**userGetCommission**](docs/SWGUserApi.md#usergetcommission) | **GET** /user/commission | Get your account&#39;s commission status.
*SWGUserApi* | [**userGetDepositAddress**](docs/SWGUserApi.md#usergetdepositaddress) | **GET** /user/depositAddress | Get a deposit address.
*SWGUserApi* | [**userGetExecutionHistory**](docs/SWGUserApi.md#usergetexecutionhistory) | **GET** /user/executionHistory | Get the execution history by day.
*SWGUserApi* | [**userGetMargin**](docs/SWGUserApi.md#usergetmargin) | **GET** /user/margin | Get your account&#39;s margin status. Send a currency of \&quot;all\&quot; to receive an array of all supported currencies.
*SWGUserApi* | [**userGetQuoteFillRatio**](docs/SWGUserApi.md#usergetquotefillratio) | **GET** /user/quoteFillRatio | Get 7 days worth of Quote Fill Ratio statistics.
*SWGUserApi* | [**userGetWallet**](docs/SWGUserApi.md#usergetwallet) | **GET** /user/wallet | Get your current wallet information.
*SWGUserApi* | [**userGetWalletHistory**](docs/SWGUserApi.md#usergetwallethistory) | **GET** /user/walletHistory | Get a history of all of your wallet transactions (deposits, withdrawals, PNL).
*SWGUserApi* | [**userGetWalletSummary**](docs/SWGUserApi.md#usergetwalletsummary) | **GET** /user/walletSummary | Get a summary of all of your wallet transactions (deposits, withdrawals, PNL).
*SWGUserApi* | [**userLogout**](docs/SWGUserApi.md#userlogout) | **POST** /user/logout | Log out of BitMEX.
*SWGUserApi* | [**userMinWithdrawalFee**](docs/SWGUserApi.md#userminwithdrawalfee) | **GET** /user/minWithdrawalFee | Get the minimum withdrawal fee for a currency.
*SWGUserApi* | [**userRequestWithdrawal**](docs/SWGUserApi.md#userrequestwithdrawal) | **POST** /user/requestWithdrawal | Request a withdrawal to an external wallet.
*SWGUserApi* | [**userSavePreferences**](docs/SWGUserApi.md#usersavepreferences) | **POST** /user/preferences | Save user preferences.
*SWGUserEventApi* | [**userEventGet**](docs/SWGUserEventApi.md#usereventget) | **GET** /userEvent | Get your user events


## Documentation For Models

 - [SWGAPIKey](docs/SWGAPIKey.md)
 - [SWGAccessToken](docs/SWGAccessToken.md)
 - [SWGAffiliate](docs/SWGAffiliate.md)
 - [SWGAnnouncement](docs/SWGAnnouncement.md)
 - [SWGChat](docs/SWGChat.md)
 - [SWGChatChannel](docs/SWGChatChannel.md)
 - [SWGCommunicationToken](docs/SWGCommunicationToken.md)
 - [SWGConnectedUsers](docs/SWGConnectedUsers.md)
 - [SWGError](docs/SWGError.md)
 - [SWGErrorError](docs/SWGErrorError.md)
 - [SWGExecution](docs/SWGExecution.md)
 - [SWGFunding](docs/SWGFunding.md)
 - [SWGGlobalNotification](docs/SWGGlobalNotification.md)
 - [SWGIndexComposite](docs/SWGIndexComposite.md)
 - [SWGInlineResponse200](docs/SWGInlineResponse200.md)
 - [SWGInstrument](docs/SWGInstrument.md)
 - [SWGInstrumentInterval](docs/SWGInstrumentInterval.md)
 - [SWGInsurance](docs/SWGInsurance.md)
 - [SWGLeaderboard](docs/SWGLeaderboard.md)
 - [SWGLiquidation](docs/SWGLiquidation.md)
 - [SWGMargin](docs/SWGMargin.md)
 - [SWGOrder](docs/SWGOrder.md)
 - [SWGOrderBookL2](docs/SWGOrderBookL2.md)
 - [SWGPosition](docs/SWGPosition.md)
 - [SWGQuote](docs/SWGQuote.md)
 - [SWGQuoteFillRatio](docs/SWGQuoteFillRatio.md)
 - [SWGSettlement](docs/SWGSettlement.md)
 - [SWGStats](docs/SWGStats.md)
 - [SWGStatsHistory](docs/SWGStatsHistory.md)
 - [SWGStatsUSD](docs/SWGStatsUSD.md)
 - [SWGTrade](docs/SWGTrade.md)
 - [SWGTradeBin](docs/SWGTradeBin.md)
 - [SWGTransaction](docs/SWGTransaction.md)
 - [SWGUser](docs/SWGUser.md)
 - [SWGUserCommissionsBySymbol](docs/SWGUserCommissionsBySymbol.md)
 - [SWGUserEvent](docs/SWGUserEvent.md)
 - [SWGUserPreferences](docs/SWGUserPreferences.md)
 - [SWGWallet](docs/SWGWallet.md)
 - [SWGXAny](docs/SWGXAny.md)


## Documentation For Authorization


## apiExpires

- **Type**: API key
- **API key parameter name**: api-expires
- **Location**: HTTP header

## apiKey

- **Type**: API key
- **API key parameter name**: api-key
- **Location**: HTTP header

## apiSignature

- **Type**: API key
- **API key parameter name**: api-signature
- **Location**: HTTP header


## Author

support@bitmex.com


