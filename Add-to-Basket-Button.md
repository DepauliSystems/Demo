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
    <div id="#addToCart"></div>

    <script src="https://api.qs-pay.com/checkout/package/sdk?store-id=ee7bdc31-8c13-4111-9225-cb780b46e1a1&locale=en_US"></script>
    <script src="belowscript.js"></script>
</body>
</html>
```

```javascript
QSPay.addToCart({
    createCartRequest: function(actions) {
        return actions.create('Your product JSON. | This method support async await')
    },
    onClick: function(){
        //a callback which runs after adding product successfuly
        //you can implement your own method where you want to render Checkout
        //or you can redirect user to a shopping cart route which renders CheckoutJS
        //e.g. window.location.href = '/basket'
    }
}).render('#addToCart')
```