# Peachill-QRCode.js
> Peach-qrcode is based on the implementation of QRCode, the original library has three functions of the extension

- Css selector (Qrcode only supports id selector)

- qr code background color gradient

- support center icon (resizable image)

## Basic Usages

> The usage method is roughly the same as QRCode

```js
<div id="app">
    <div class="test"></div>
</div>
<script src="qrcode.js"></script>
<script>
    //只针对canvas渲染
    var qrcode = new QRCode(".test", {
        text: "http://www.merryzoe.com",
        width: 428,
        height: 428,
        //colorDark : "#ff0000",
        //colorLight : "#ffffff",
        centerIconSrc:'./test.jpg',
        iconWidth:428,
        iconHeight:285,
        linearGradient:true,
//        linearGradientDirection:'to right',
//        linearGradientDirection:'to left',
//        linearGradientDirection:'to top',
//        linearGradientDirection:'to top left',
//        linearGradientDirection:'to top right',
//        linearGradientDirection:'to bottom',
//        linearGradientDirection:'to bottom right',
//        linearGradientDirection:'to bottom left',
        linearGradientFrom:'#3CB371',
        linearGradientTo:'#FFD700',
        linearGradientMiddle:'#FF6347'
    });
</script>
```

**Vue project**

~~~js
	<div id="app">
		<div id="b-download__qr"></div>
	</div>
	import QRCode from 'peachill-qrcode';
	
    mounted() {
		new QRCode("#b-download__qr", {
            text: this.url,
            width: 220,
            height: 220,
            centerIconSrc:require('../assets/images/logo.png'),
            iconWidth:120,
            iconHeight:61,
            linearGradient:true,
            linearGradientFrom:'#3CB371',
            linearGradientTo:'#FFD700',
            linearGradientMiddle:'#FF6347'
        });
     }
~~~

## What's changed

See the CSDN blog for details

https://blog.csdn.net/u012451520/article/details/105953578

## Browser Compatibility

IE9~10, Chrome, Firefox, Safari, Opera, Mobile Safari, Android, Windows Mobile, ETC.（Subsequent adjustments to support IE6）

## Contact
GitHub@StarAndSea-zhang



