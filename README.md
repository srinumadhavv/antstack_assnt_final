# antstack_final

THIS IS AN APPLICATION BUILT FOR ANSTACK AS AN ASSIGNMNENT

TO USE THIS APPLICATION :

1. Create a folder named ANTSTACK

2. cd ANTSTACK

3.git clone https://github.com/srinumadhavv/antstack_backend

4.git clone https://github.com/srinumadhavv/antstack_frontend

5.in /ANTSTACK place the docker-compose-file in this repo 

6.The folder structure looks similar to this with files in antstack_backend and antstack_frontend

https://user-images.githubusercontent.com/43718077/152755801-a61c5fe6-f896-41ba-9246-9709f463028a.png
    
7.open terminal and run --> docker compose up

8.open browser and redirect to http://localhost:3000/ for using react 

9.redirect to http://localhost:8000/ for backend server

10. Use postman to test apis:

    redirect to http://localhost:8000/docs for proper api documentation on using the apis
    
11. Create coupon api:

request_type: POST

request_url: http://localhost:8000/coupons/create

body: {
  "id": "coupon1",
  "start_date": 1644129883,
  "expiry_date": 1744129883,
  "type": "fixed",
  "discount": 10,
  "min_amount": 200
}

response: {
    "id": "coupon2",
    "expiry_date": 1744129883,
    "discount": 10,
    "min_amount": 200
}

12. Get coupons api:

request_type: GET

request_url: http://localhost:8000/coupons/

response:{
    "coupons": [
        {
            "type": "fixed",
            "id": "coupon3",
            "expiry_date": 1744129883,
            "start_date": 1644129883,
            "discount": 10,
            "min_amount": 200
        },
        {
            "type": "fixed",
            "id": "coupon1",
            "expiry_date": 1744129883,
            "start_date": 1644129883,
            "discount": 10,
            "min_amount": 200
        },
        {
            "type": "fixed",
            "id": "coupon2",
            "expiry_date": 1744129883,
            "start_date": 1644129883,
            "discount": 10,
            "min_amount": 200
        }
    ]
}

13. validate coupons api

request_type: POST

request_url: http://localhost:8000/checkout

body:{
  "amount": 1000,
  "coupon": "coupon1"
}

response:{
    "total_amount": 990,
    "discount": 10
}

14.Note: you can access all the frontend apis through http://localhost:3000/ on which you can see the response if the api is used properly to checkout the status code or result use cmd+shift+i then inspect and then head to network hit on api to verify response 

 * please makesure ports 3000 and 8000 are available on host machine.

15.Any clarifications if needed in setup please message to 8639566476 or srinumadhavvysyaraju@gmail.com

