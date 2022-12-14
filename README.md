#NFT Aggregator
-----
__Plan:__
1. [Installation](#installation)
2. [Usage](#usage)
3. [Example](#example)
-----

<a id='installation'></a>
__Installation__

-----
1. You need to instal all libraries from Requirements.txt.
2. Install program where you can use PostgreSQL, usually pgAdmin4.
3. Download 'src' file and open test.py.
4. Firstly, in the code change values in 'database', 'password' and API Key, which you can get from your account in Moralis.
```
conn = psycopg2.connect(database="your database", user = "postgres", password = "your password", 
                        host = "127.0.0.1", port = "5432")
url = "https://solana-gateway.moralis.io/nft/mainnet/{}/metadata"
headers = {
    "accept": "application/json",
    "X-API-Key": "Your Moralis API key"
} 
```
5. Secondly, change values of password and database name in the below code.
```
app.config['SQLALCHEMY_DATABASE_URI'] = 'postgresql+psycopg2://postgres:YOURPASSWORD@localhost/YOURDATABASE'
```
6. After that, you need to create database using Terminal. Write all commands one by one, like in the below code.
```
python

from test import db /*Instead of 'test' you need write name of your python file*/

db.create_all()
```
7. Well done, now your application web service is ready. 
-----

<a id='usage'></a>
__Usage__

-----
1. On the main page you can read information about 'Omni' aggregator, then you need to Log In.
![](src/img/main.PNG)
2. On the page Log In you need to sign in or if you do not have an account sign up.
![](src/img/login.PNG)
3. After clicking on 'Sign In', you will be redirected to search page.
Paste the NFT address of Solana blockchain NFT and click icon 'search'.
![](src/img/search.PNG)
-----

__Example__

-----
1. Main Page.
![](src/img/main.PNG)

2. Login or Registration.
![](src/img/login.PNG)

3. Creating an account.
![](src/img/registrer.PNG)

4. Sign in.
![](src/img/signin.PNG)

5. Enter NFT address.
![](src/img/readme.PNG)

6. Read information.
![](src/img/info.PNG)
