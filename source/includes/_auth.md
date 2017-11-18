# Authentication

> To authorize, use this code:

```ruby
require 'BellaBug'

api = BellaBug::APIClient.authorize!('meowmeowmeow')
```

```python
import BellaBug

api = BellaBug.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const BellaBug = require('BellaBug');

let api = BellaBug.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

BellaBug uses API keys to allow access to the API. You can register a new BellaBug API key at our [developer portal](http://example.com/developers).

BellaBug expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>
