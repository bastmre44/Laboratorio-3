# API Onboarding Report

## DummyJSON API

------------------------------------------------------------------------

## 1. API Summary

**Name:** DummyJSON API\
**Base URL:** https://dummyjson.com\
**Authentication Type:** JWT (required for protected endpoints such as
/auth/me)\
**Rate Limit:** Not explicitly documented (free public testing API)

------------------------------------------------------------------------

## 2. Endpoints Table

  ------------------------------------------------------------------------------------------------------------
  Method   URL                              Query Params   Headers           Expected Status  Obtained Status
  -------- -------------------------------- -------------- ----------------- ---------------- ----------------
  GET      /products                        None           None              200              200

  GET      /products/1                      None           None              200              200

  GET      /products/search                 q=phone        None              200              200

  GET      /products/category/smartphones   None           None              200              200

  GET      /products?limit=5&skip=10        limit, skip    None              200              200

  GET      /users                           None           None              200              200

  GET      /products/999999                 None           None              404              404

  GET      /products?limit=abc              invalid limit  None              400              400

  GET      /auth/me                         None           None              401              401

  GET      /auth/me                         None           Authorization:    403              403
                                                           Bearer                             
                                                           invalidtoken123                    
  ------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 3. Evidence of Responses

### Successful Responses

1.  **List Products -- 200 OK**\
    Returned JSON list of products including id, title, price and other
    attributes.

2.  **Get Product by ID -- 200 OK**\
    Returned single product object with id = 1.

3.  **Search Products -- 200 OK**\
    Returned filtered list of products containing the word "phone".

------------------------------------------------------------------------

### Failed Responses

1.  **404 Not Found**\
    Requesting product ID 999999 returned:\
    { "message": "Product not found" }

2.  **400 Bad Request**\
    Sending invalid limit parameter returned:\
    { "message": "Invalid 'limit' - must be a number" }

3.  **401 Unauthorized**\
    Accessing /auth/me without token returned 401.

4.  **403 Forbidden**\
    Accessing /auth/me with invalid token returned 403.

------------------------------------------------------------------------

## 4. Notes

-   The API follows REST principles.
-   Pagination is handled using limit and skip parameters.
-   Authentication is required only for protected endpoints.
-   DummyJSON is suitable for testing REST tools such as Postman and
    HTTPie.
