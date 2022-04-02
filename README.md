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
        
        {
        "username": "temp",
        "name": "Temp User",
        "date_joined": "2022-04-02T04:08:37+00:00"
        }

  

## api/wallet/

-   Authentication Required*
-   GET - List all wallets owned by the user.
-   POST - Add new Wallet  
    - “address” (ETH address, String, less than 100 char, unique)  
    - “nick_name” (An identifier/name for wallet, String, less than 200 char).  
    - “balance”
