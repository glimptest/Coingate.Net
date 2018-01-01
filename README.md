
# Coingate.Net
A library used to process coingate payment transactions in .Net

Website: https://coingate.com

# Code Examples
<ul>
<li>RebyRuby Gem</li>
<li>Coingate PHP</li>
<li>Omnipay (PHP)</li>
<li>Ruby on Rails Shop Example / Source Code</li>
<li>E-commerce Plugins</li>
</ul>


# Getting Started

Coingate allows you to buy and sell Bitcoin, accept Bitcoin using the merchant API. 
For java/php developers, visit the developer section https://developer.coingate.com/ 
for implementation guide or you can download one of the examples listed.  
Before you can use the API, you need to sig up for a merchant account https://coingate.com/sign_up
For testing, you can sign up here https://sandbox.coingate.com

# Authentication

All Coingate API calls require authentication. You can authenticate your app by providing 3 parameters: API Key, Signature and Nonce.

API Key - You can generate your API Key in account area. From main account navigation go to Apps and create new app.
Nonce - A nonce is an integer that must be increasing with every request.
Signature - It is a HMAC-SHA256 encoded message containing: nonce, app ID and API key.

# Creating an Order

```
          var cg = new Coingate.Net.Coingate("apiKey","apiSecret","appId");
            var orders = cg.CreateOrder(new Order
            {
                Price = 100,
                Currency = "USD",
                ReceiveCurrency = "BTC"
            });
```

# Retrieving an Order

```
          var cg = new Coingate.Net.Coingate("apiKey","apiSecret","appId");
          var orders = cg.GetOrders();
          ...
```