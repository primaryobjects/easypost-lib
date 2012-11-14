EasyPost
--------

An easy method for reading POST data in Node.js web applications. EasyPost supports both form submissions and REST client posts. It also provides a single location for maintaining the code that reads POST data, allowing you to enhance it, such as with checks for flooding attacks, etc.

```bash
$ npm install easypost
```

## Usage
```
var easypost = require('easypost');
```
### Reading POST Data From a Form
```
    easypost.get(req, res, function (data) {
        res.render('index', { txtName: data.txtName });
    });
```
### Reading POST Data From a REST Client
```
    easypost.get(req, res, function (data) {
        data = JSON.parse(data);
        res.render('index', { txtName: data.txtName });
    });
```
## Notes

In the above examples, the first example assumes your form contains the element:

```
[input type='text' id='txtName' /]
```

The second example assumes a REST client has posted the following data:

```
{"txtName": "My Name"}
```

You can view a tutorial article using EasyPost at http://www.primaryobjects.com/CMS/Article144.aspx

## Author

Kory Becker
http://www.primaryobjects.com
