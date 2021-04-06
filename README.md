# API Doc

## Start Session
<u>Start Session</u>
``GET : https://whatsapp.contrateumdev.com.br/start?sessionName=MySession99/``
<hr>

## Close Session
<u>Close Session</u>
``GET : https://whatsapp.contrateumdev.com.br/close?sessionName=MySession99/``
<hr>

## Get QR CODE
<u>Get QRCODE</u>
``GET : https://whatsapp.contrateumdev.com.br/qrcode?sessionName=MySession99&image=true``
> - image
<hr>

## Get QR CODE base64
<u>Get QRCODE</u>
``GET : https://whatsapp.contrateumdev.com.br/qrcode?sessionName=MySession99``
> - json (base64) ** recommended
<hr>

## Send Message
<u>Send Message</u>
``GET : https://whatsapp.contrateumdev.com.br/sendText``
> Request Body
> - sessionName - name of session started
> - number - number with code of country
> - text - text of send to number
<hr>

## Send Files
<u>Send Files</u>
``GET : https://whatsapp.contrateumdev.com.br/sendFile``
> Request Body
> - sessionName - name of session started
> - number - number with code of country
> - base64Data:"44696d61",//hexadecimal
> - fileName: "test.txt",
> - caption - text (optional)
<hr>

### Send message (POST method)

```javascript
$.post({
  method: 'POST',
  url: `https://whatsapp.contrateumdev.com.br/sendText`,
  contentType:"application/json; charset=utf-8",
  dataType:"json",
  data: JSON.stringify({
      sessionName: `session99`,
      number: `5531995360492`,
      text: `Olá`
  }),
  success: function(resultado, status, xhr) {
      console.log(resultado)
  }
}) 
```

### Send File (POST method)

```javascript
$.post({
  method: 'POST',
  url: `https://whatsapp.contrateumdev.com.br/sendFile`,
  contentType:"application/json; charset=utf-8",
  dataType:"json",
  data: JSON.stringify({
     sessionName: "session99", 
      number: '556334140378',
      base64Data:"44696d61", //hexadecimal
      fileName:"test.txt",
      caption: "Document" //optional
  }),
  success: function(resultado, status, xhr) {
      console.log(resultado)
  }
}) 

```
