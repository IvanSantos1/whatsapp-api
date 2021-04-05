
## Usage

### Start new whatsapp session

`https://whatsapp.contrateumdev.com.br/start?sessionName=session99`

### Get QRCode (quickly!!)

`https://whatsapp.contrateumdev.com.br/qrcode?sessionName=session99`
- png

`https://whatsapp.contrateumdev.com.br/qrcode?sessionName=session99`
- json (base64)

### Close whatsapp session

`https://whatsapp.contrateumdev.com.br/close?sessionName=session99`

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
