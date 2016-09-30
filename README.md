# Watson-Helper

Extract phone numbers and emails from arbitrary text.

Features:
- Extract multiple phone number formats across different countries
- Extract multiple email number formats across multiple domains
- Extract any custom information like invoiceno, ticketid, purchaseordernumber, UID etc
- Unit tested
- Examples enclosed

### Background
A recent IBM Watson customer was exploring Watson conversation api. For the customer extraction of phone numbers and email was a key usecase. This data needs to be captured during the conversation. Hence to assist the customer I wrote this library. This library now can help customers with similar usecase extract their set of data usually expressed in conversations or personal blogs. I have  released the first version that can address 3 key usecases. Few other key usecases are in pipeline. 


## Examples

### Basic example
Extraction of one or more phone numbers, email or custom data(like invoiceno, ticketid, purchaseordernumber, UID etc ) from a user supplied text.
```js
var helper = require('watsonhelper');
var phonelist = helper.phoneextractor("I am moving to hyderabad and my mobile number is  +919538099898, You can also call me at 08042227967");

var email = helper.emailextractor("I am moving to US and my email id is  shunandi@gmail.com, You can also email me at shubhradeepnandi@gmail.com");

var invoiceno = helper.extractor("<Extracting What>", "Your invoice is generated it is inv1105576", <REGEX STRING>);

### Limitations
This software cannot capture every single combination imaginable. Especially number-to-letter substitution is difficult to detect e.g:
- O4!4.Ol2;341 (= 0414 012 341)

In my experience very few users write their phone number this way. From a programming point of view it would be possible to cover for edge cases like above, but I have chosen not to.

### Issues, bug reports
shunandi@gmail.com

### License
https://spdx.org/licenses/Apache-2.0
