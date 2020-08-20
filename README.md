# Trailer Widget 1.0

By SUXESS TEAM

> The Trailer Widget 1.0 is a basic module in HTML that can be embedded in any website, it shows the creation trailer and the rent and purchase buttons.

## Languages

  - [Español](docs/README_ES.md)

## Main Features

  - HTML code
  - Responsive with CCS Flexbox
  - Embedded video iframe from Mowies.com. The video URL has a parameter to remove the video quality message and the close icon.
  - The links of the rent and purchase buttons are customizable and are taken from the creation that was previously published on the mowies.com platform.
  - Supported in any basic HTML editor
  - Supported in Chrome, Firefox, Safari (To test in Microsoft Edge)


## Demo

https://www.mowies.com/site/trailer-test/


## Setup

### 1. Copy complete HTML code below and paste it somewhere on the website that supports HTML.

```html
<div style="position: relative; padding-bottom: 56.25%; height: 0px;">
  <iframe style="position: absolute; top: 0px; left: 0px; width: 100%; height: 100%;" width="560" height="315" src="TRAILER_URL_HERE" frameborder="0" allow="accelerometer; encrypted-media; gyroscope; picture-in-picture"></iframe>
</div>

<div style="background-color: #000000; padding: 25px; display: grid; grid-template-columns: 1fr 1fr 2fr; grid-template-rows: 50px; gap: 3%;">
  <div>
    <a style="color: #ffffff; font-family: Arial, Helvetica, sans-serif; text-decoration: none;" href="RENT_URL_HERE" target="_blank">
      <div style="text-align: center; background-color: #000000; border: 2px solid #ffffff; padding: 15px 10px; border-radius: 30px; min-width: 60px;"><strong>Rentar</strong></div>
    </a>
  </div>

  <div>
    <a style="color: #ffffff; font-family: Arial, Helvetica, sans-serif; text-decoration: none;" href="BUY_URL_HERE" target="_blank">
      <div style="text-align: center; background-color: #23cb51; border: 2px solid #23cb51; padding: 15px 10px; border-radius: 30px; min-width: 60px;"><strong>Comprar</strong></div>
    </a>
  </div>

  <div style="text-align: right; background-color: #000000; padding: 18px 8px 0px 12px; border-radius: 30px; text-decoration: none;">
    <a style="color: #ffffff; font-family: Arial, Helvetica, sans-serif;" href="http://mowies.com/" target="_blank">
      <img alt="" align="right" width="65" height="auto" src="https://chigui-public-assets.s3.amazonaws.com/logo_mowies-xsm.svg" style="border: 0px; width: 65px; height: auto; margin: 0px; opacity: 0.5; float: right;" />
    </a>
  </div>
</div>

<iframe style="display:none;" src='about:blank'></iframe>
```

### 2. Replace trailer URL.

  - Go to the creation published on mowies.com, click on the "See Trailer" button and copy the URL that appears in the address bar. Example: https://www.mowies.com/trailer/watch/5e862e2acc76b604df940092/dbb52a3d-f763-4dbe-bc83-33eb696f2d0f?goBack=true
  - Paste the URL into the code section, replacing where it says **TRAILER_URL_HERE**. The URL must be inside the quotation marks.
  - Replace the parameter **?goBack=true** with **?mode=embedded**. The URL should look like this: https://www.mowies.com/trailer/watch/5e862e2acc76b604df940092/dbb52a3d-f763-4dbe-bc83-33eb696f2d0f?mode=embedded

### 3. Replace URL of RENT and BUY buttons.

  - Go to the creation published on mowies.com, click on the "RENT" button and copy the URL that appears in the address bar. Example: https://www.mowies.com/payment-gateway?assetType=creation&assetId=5e862e2acc76b604df940092&username=mowies&operationType=2
  - Paste the URL in the code section, replacing where it says **RENT_URL_HERE**. The URL must be inside the quotation marks.
  - Make sure that the parameter **&operationType=2** is at the end of the link. The number **2** indicates that it is the rental URL.
  - Repeat the process again, but this time replacing the text that says **BUY_URL_HERE**. Make sure that the parameter **&operationType=1** is at the end of the link. The number **1** indicates that it is the URL to buy.
