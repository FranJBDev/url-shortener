# url-shortener

Para probarlo en postman hacer POST a:
**http://localhost:5000/api/url/shorten**

> Tambien en Postman en headers agregar

    KEY: Content-Type
    VALUE: application/json

con un objeto como este donde va un link largo.

```json
{ 
    "longUrl": "https://www.amazon.com.mx/XP-Pen-Generaci%C3%B3n-Tableta-Pantalla-Pulgadas/dp/B08S6RKG4Z/?_encoding=UTF8&pd_rd_w=qPZx4&content-id=amzn1.sym.49817a84-0bcd-497b-b987-7eb2210a5a09&pf_rd_p=49817a84-0bcd-497b-b987-7eb2210a5a09&pf_rd_r=4AXM6FP7BFDY9RXYE5X9&pd_rd_wg=OYKLd&pd_rd_r=487d6f03-73dc-479e-8828-a4fc5277d3e8&ref_=pd_gw_ci_mcx_mr_hp_atf_m"
}
```

Debe regresar un objeto como este:

```json
{ 
    "urlCode": "w-zBtmAd0", "longUrl": "https://www.amazon.com.mx/XP-Pen-Generaci%C3%B3n-Tableta-Pantalla-Pulgadas/dp/B08S6RKG4Z/?_encoding=UTF8&pd_rd_w=qPZx4&content-id=amzn1.sym.49817a84-0bcd-497b-b987-7eb2210a5a09&pf_rd_p=49817a84-0bcd-497b-b987-7eb2210a5a09&pf_rd_r=4AXM6FP7BFDY9RXYE5X9&pd_rd_wg=OYKLd&pd_rd_r=487d6f03-73dc-479e-8828-a4fc5277d3e8&ref_=pd_gw_ci_mcx_mr_hp_atf_m", "shortUrl": "http:localhost:5000/w-zBtmAd0", "date": "Sat Oct 01 2022 14:48:24 GMT-0600 (hora de verano del Pacífico de México)", "\_id": "6338a798aacd82b0bb8d6960", "\_\_v": 0
}
```

> Copia el valor de shortUrl y pegalo en un navegador debera redirigir a la url original
