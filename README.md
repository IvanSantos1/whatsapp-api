
## Usage

### Start new whatsapp session

`https://whatsapp.contrateumdev.com.br/start?sessionName=session1`

### Get QRCode (quickly!!)

`https://whatsapp.contrateumdev.com.br/qrcode?sessionName=session1&image=true`
- png

`https://whatsapp.contrateumdev.com.br/qrcode?sessionName=session1`
- json (base64)

### Close whatsapp session

`https://whatsapp.contrateumdev.com.br/close?sessionName=session1`

### Send message (POST method)

```javascript
(async () => {
  const response = await fetch('https://whatsapp.contrateumdev.com.br/sendText', {
    method: 'POST',
    headers: {
      'Accept': 'application/json',
      'Content-Type': 'application/json'
    },
    body: JSON.stringify(
        {
            sessionName: "session1", 
            number: '556334140378',
            text:"Hello\nWorld"
        }
    )
  });
  const content = await response.json();

  console.log(content);
})();  
```

### Send File (POST method)

```javascript
(async () => {
    const response = await fetch('https://whatsapp.contrateumdev.com.br/sendFile', {
    method: 'POST',
    headers: {
      'Accept': 'application/json',
      'Content-Type': 'application/json'
    },
    body: JSON.stringify(
        {
            sessionName: "session1", 
            number: '556334140378',
            base64Data:"44696d61", //hexadecimal
            fileName:"test.txt",
            caption: "Document" //optional
        }
    )
  });
  const content = await response.json();

  console.log(content);
})();  
```
