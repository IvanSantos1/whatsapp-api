# API Doc

## Start Session
<u>Start Session</u>
``GET : https://whatsapp.contrateumdev.com.br/start?sessionName=MySession99/``
<hr>

## Close Session
<u>Close Session</u>
``GET : https://whatsapp.contrateumdev.com.br/close?sessionName=MySession99/``
<hr>

<u>Get QRCODE</u>
``GET : https://whatsapp.contrateumdev.com.br/qrcode?sessionName=MySession99&image=true``
> - image
<hr>

<u>Get QRCODE</u>
``GET : https://whatsapp.contrateumdev.com.br/qrcode?sessionName=MySession99``
> - json (base64) ** recommended
<hr>

<u>Send Message</u>
``GET : https://whatsapp.contrateumdev.com.br/sendText``
> Request Body
> - sessionName - name of session started
> - number - number with code of country
> - text - text of send to number
<hr>

<u>Send Files</u>
``GET : https://whatsapp.contrateumdev.com.br/sendFile``
> Request Body
> - sessionName - name of session started
> - number - number with code of country
> - base64Data:"44696d61",//hexadecimal
> - fileName: "test.txt",
> - caption - text (optional)
<hr>
