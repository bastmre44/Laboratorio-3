HTTPie Commands - DummyJSON API

Variables

export BASE_URL=https://dummyjson.com
export RESOURCE=products
export PRODUCT_ID=1
export QUERY=phone



1. List Products

http GET $BASE_URL/$RESOURCE



2. Get Product By ID

http GET $BASE_URL/$RESOURCE/$PRODUCT_ID



3. Search Products

http GET "$BASE_URL/$RESOURCE/search?q=$QUERY"



4. Filter By Category

http GET $BASE_URL/$RESOURCE/category/smartphones


5. Pagination

http GET "$BASE_URL/$RESOURCE?limit=5&skip=10"



6. List Users (Second Resource)

http GET $BASE_URL/users



7. 404 Not Found

http GET $BASE_URL/$RESOURCE/999999



8. 400 Bad Request

http GET "$BASE_URL/$RESOURCE?limit=abc"



9. 401 Unauthorized (No Token)

http GET $BASE_URL/auth/me



10. 403 Forbidden (Invalid Token)

http GET $BASE_URL/auth/me Authorization:"Bearer invalidtoken123"