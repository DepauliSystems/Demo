An example for simulating basic checkout rendering for every webpage whether it's shopify or any other e-commerce platform.

```HTML
<html>
<head>
    <title>Demo Checkout</title>
</head>
<body>

<div id="checkout">
    <!-- QSPay checkout will be rendered here when DOM loads, no configuration required. -->
</div>

<script src="https://api.qs-pay.com/checkout/package/sdk?store-id=ee7bdc31-8c13-4111-9225-cb780b46e1a1&locale=en_US"></script>
<script type="text/javascript">
    QSPay.checkout().render('#checkout')
</script>
</body>
</html>
```