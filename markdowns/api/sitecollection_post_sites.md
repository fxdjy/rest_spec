# Create Site

Use this API to create a new Site.
### HTTP request
```http


```
### Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| X-Sample-Header  | string  | Sample of how the HTTP headers used by the API could be displayed.|

### Request body
In the request body, supply a JSON representation of [Site](../resources/site.md) object.


### Response
If successful, this method returns `201, Created` response code and [Site](../resources/site.md) object in the response body.

### Example
##### Response
Here is an example of the response.
```json
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 26
{
  "id": "String-value"
}
```