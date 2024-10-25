# Facial-Recognition-Flask-API
This API enables facial recognition functionality by comparing a user-uploaded image with a reference image. The API returns True if the images match and False otherwise, allowing applications to implement secure access control through facial recognition.

# Features
* Image Comparison: Compares a user image with a reference image.
* RESTful API: Simple to integrate with various platforms.
* Supports multiple image formats: Accepts common image file formats for comparison.

# API Endpoint
URL: https://your-ngrok-url/verify
Method: POST
Content-Type: multipart/form-data
### Request Parameters
user_image: The image of the user to be verified (file).
reference_image: The reference image for comparison (file).
### Sample Request
To use this API, you need to send a POST request with the required parameters.

# Testing with Postman

### Step-by-Step Guide
1. Open Postman.
2. Create a new request:
  Click on "New" and select "Request."
3. Name your request and create or choose a collection to save it in.
4. Set the request type to `POST`.
   Enter the URL: `https://your-ngrok-url/verify`
5. Select the Body tab:
   Choose `form-data`.
6. Add the required key-value pairs:
   Key: `user_image`
7. Value: Choose your user image file.
   Key: `reference_image`
8. Value: Choose your reference image file.
9. Click the `Send` button.

### Sample Response
On a successful request, the response will be a JSON object indicating whether the images matched:
```
{
  "match": true
}
```
or
```
{
  "match": false
}
```

