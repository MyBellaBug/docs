# Orders

## Create/Update/Delete Orders

```shell
curl "https://api.bellabug.com/orders"
```

> The above command returns JSON structured like this:

```json
HEAD: 201
```

This endpoint accepts posts to create, update, or delete orders. The response code will always be 20X unless an error occurred.

### HTTP Request

`POST https://api.bellabug.com/orders`

### Query Parameters

Parameter | Data type | Required | Description
--------- | --------- | -------- | -----------
order_id | string | true | ID of the order in 3rd party system
status | string | true | The current status of the order, i.e. new, modified, cancelled
retailer | string | true, if status is "new", else false | The name of the retailer
first_name | string | true, if status is "new", else false | The first name for customer placing order
last_name | string | true, if status is "new", else false | The last name for customer placing order
address | string | true, if status is "new", else false | The address for the order to be shipped
city | string | true, if status is "new", else false | The city for the order to be shipped
state | string | true, if status is "new", else false | The state for the order to be shipped
postal_code | string | true, if status is "new", else false | The postal code for the order to be shipped
order_number | string | true, if status is "new", else false | The order number in the 3rd party system
quantity | int | true, if status is "new", else false | The quantity of the item to be shipped
item_sku | string | true, if status is "new", else false | The sku of the item to be shipped
print_surface_1_url | string | true, if status is "new", else false | The URL for Print Surface 1
print_surface_2_url | string | false | The URL for Print Surface 2
return_address | string | false | The address for returns, if different than shipping address
return_city | string | false | The city for returns, if different than shipping address
return_state | string | false | The state for returns, if different than shipping address
return_postal_code | string | false | The postal code for returns, if different than shipping address
po_number | string | false | The Purchase Order number
retailer_dept | string | false | The retailer department


<!--
## Get All Orders

```shell
curl "http://example.com/api/Orders"
  -H "Authorization: meowmeowmeow"
```

 ```ruby
require 'BellaBug'

api = BellaBug::APIClient.authorize!('meowmeowmeow')
api.Orders.get
```

```python
import BellaBug

api = BellaBug.authorize('meowmeowmeow')
api.Orders.get()
```

```javascript
const BellaBug = require('BellaBug');

let api = BellaBug.authorize('meowmeowmeow');
let Orders = api.Orders.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all Orders.

### HTTP Request

`GET http://example.com/api/Orders`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include Orders that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>


## Get a Specific Kitten

```ruby
require 'BellaBug'

api = BellaBug::APIClient.authorize!('meowmeowmeow')
api.Orders.get(2)
```

```python
import BellaBug

api = BellaBug.authorize('meowmeowmeow')
api.Orders.get(2)
```

```shell
curl "http://example.com/api/Orders/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const BellaBug = require('BellaBug');

let api = BellaBug.authorize('meowmeowmeow');
let max = api.Orders.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/Orders/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'BellaBug'

api = BellaBug::APIClient.authorize!('meowmeowmeow')
api.Orders.delete(2)
```

```python
import BellaBug

api = BellaBug.authorize('meowmeowmeow')
api.Orders.delete(2)
```

```shell
curl "http://example.com/api/Orders/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const BellaBug = require('BellaBug');

let api = BellaBug.authorize('meowmeowmeow');
let max = api.Orders.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/Orders/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

-->
