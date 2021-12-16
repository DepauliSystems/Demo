An example of adding an **add to basket button** to your product details page or any other location you want to display it.
This button works synchronously with CheckoutJS, since you are going to need this module in order to add product to CheckoutJS. 


```HTML
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <div>
        <p>Super Product</p>
        <p>10$</p>
    </div>
    <div id="#expressCheckout"></div>

    <script src="https://api.qs-pay.com/checkout/package/sdk?store-id=ee7bdc31-8c13-4111-9225-cb780b46e1a1&locale=en_US"></script>
    <script src="belowscript.js"></script>
</body>
</html>
```

```javascript
    QSPay.button({
        style: {
            layout: 'horizontal',
            color: 'light',
            shape: 'rect',
            label: 'qspay'
        },
        createOrder: function(){
            return actions.create('your custom api calls in order to have a product JSON here')
        },
        onApprove: function(){
            //this method runs after successful buy operation
        },
        onCancel: function(){
            //this method runs after consumer closes the express checkout or fails the payment then bails.
        },
    }).render('#expressCheckout');
```