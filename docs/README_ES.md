# Trailer Widget 1.0

By SUXESS TEAM

> El Trailer Widget 1.0 es un módulo básico en HTML que puede ser embebido en cualquier sitio web, este muestra el trailer de la creación y los botones de renta y compra.

## Languages
  - [English](../README.md)

## Características principales

  - Código HTML
  - Responsive con CCS Flexbox
  - Iframe de video incrustado desde Mowies.com. La URL del video tiene un parámetro para remover el mensaje de calidad de video y el icono de cerrar.
  - Los links de los botones de renta y de compra son personalizables y se toman de la creación previamente publicada en la plataforma mowies.com.
  - Soportado en cualquier editor básico de HTML
  - Soportado en Chrome, Firefox, Safari (Falta hacer testing en Microsoft Edge)


## Demo

https://www.mowies.com/site/trailer-test/


## Setup

### 1. Copiar código HTML completo y pegarlo en algún lugar del website que soporte HTML.

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

### 2. Reemplazar URL del trailer.

  - Ir a la creación publicada en mowies.com, hacer click en el botón “Ver Trailer” y copiar la URL que aparece en la barra de direcciones. Ejemplo: https://www.mowies.com/trailer/watch/5e862e2acc76b604df940092/dbb52a3d-f763-4dbe-bc83-33eb696f2d0f?goBack=true
  - Pegar la URL en la sección del código, reemplazando donde dice **TRAILER_URL_HERE**. La URL debe de quedar dentro de las comillas.
  - Reemplazar el parámetro **?goBack=true** por **?mode=embedded**. La URL debe de quedar así: https://www.mowies.com/trailer/watch/5e862e2acc76b604df940092/dbb52a3d-f763-4dbe-bc83-33eb696f2d0f?mode=embedded

### 3. Reemplazar URL de los botones RENTAR y COMPRAR.

  - Ir a la creación publicada en mowies.com, hacer click en el botón “RENTAR” y copiar la URL que aparece en la barra de direcciones. Ejemplo https://www.mowies.com/payment-gateway?assetType=creation&assetId=5e862e2acc76b604df940092&username=mowies&operationType=2
  - Pegar la URL en la sección del código, reemplazando donde dice URL **RENT_URL_HERE**. La URL debe de quedar dentro de las comillas.
  - Cerciorarse que al final del link esté el parámetro **&operationType=2**. El número **2** indica que es la URL de rentar.
  - Repetir el proceso de nuevo, pero esta vez reemplazado el texto que dice **BUY_URL_HERE**. Cerciorarse que al final del link esté el parámetro **&operationType=1**. El número **1** indica que es la URL de comprar.
