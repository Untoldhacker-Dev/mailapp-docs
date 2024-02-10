# API Documentation

## Error Responses:

1. Unauthorized

- **Code:** UNAUTHORIZED
- **Message:** Missing or invalid authentication information in the request. Further requests will be denied. Please ensure proper authorization.

2. 404 Not Found

- **Code:** NOT_FOUND
- **Message:** Invalid Id for {id}

3. ### 403 Forbidden

- **Code:** FORBIDDEN
- **Message:** Your request has been blocked by API admin.
- **Code:** FORBIDDEN
- **Message:** Your API request for the sendMail function has been rejected. This action is not allowed due to a violation of our Terms of Service. If you have further inquiries or wish to address this matter, please contact our support team.
- **Code:** FORBIDDEN
- **Message:** Your request cannot be processed as your account credits are exhausted. To continue using our service, please recharge your account or wait for refill of next day.
- **Code:** API_DISABLED
- **Message:** Your request cannot be processed as you have disabled the accesses to this API endpoint from your MailApp dashboard, please enable it from there to keep using.
- 400 Bad Request

- **Error:** Cannot send mail to an empty recipient
- **Error:** Cannot send mail without a subject

5. ### 500 Internal Server Error

- **Code:** INTERNAL_SERVER_ERROR
- **Message:** {error message}
- 

## Success Response:

- **Status:** 200 OK
- **Data:** { "ok": true }