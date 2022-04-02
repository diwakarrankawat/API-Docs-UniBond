## api/

-   Authentication Required*
-   Wallets owned by user, last 5 transactions
-   Allowed methods - GET.
    

  

## api/user-details/

-   Authentication Required*
-   GET - username, name, date joined
-   POST 
     - “first_name”(required)
     - “last_name”(required)
-   Example -
```JSON
{
    "username": "temp",
    "name": "Temp User",
    "date_joined": "2022-04-02T04:08:37+00:00"
}
```
  

## api/wallet/

-   Authentication Required*
-   GET - List all wallets owned by the user.
-   POST - Add new Wallet  
    - “address” (ETH address, String, less than 100 char, unique)  
    - “nick_name” (An identifier/name for wallet, String, less than 200 char).  
    - “balance”

*GET Example*
```JSON
[
    {
        "id": 1,
        "address": "0xb794f5ea0ba39494ce839613fffba74279579268",
        "nick_name": "First Wallet",
        "balance": 215.21
    },
    {
        "id": 3,
        "address": "0xb794f5ea0ba39494ce839613fffba74279579269",
        "nick_name": "Fake Wallet",
        "balance": 923.0
    },
    {
        "id": 4,
        "address": "0xb794f5ea0ba39494ce839613fffba74279578268",
        "nick_name": "JSON",
        "balance": 323.0
    }
]
```

*POST example*
 ```JSON
{
    "address": "0xb794f5ea0ba39494ce839613fffba74279579268",
    "nick_name": "Some Nick Name",
    "balance": 2390.30
}
```
