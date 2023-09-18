# Quick CMS Stored XSS v6.7

## Author: (Sergio)

**Description:** Multiple Cross-Site Scripting (XSS) vulnerabilities in Quick CMS v6.7 allows a local attacker to execute arbitrary code via a crafted script to the to the Files - Description in the Pages Menu.

**Attack Vectors:** Scripting A vulnerability in the sanitization of the entry in the Description of "Pages- Files Menu" allows injecting JavaScript code that will be executed when the user accesses the web page.

---

### POC:


When logging into the panel, we will go to the "Pages - Files ." section off General Menu. 

![XSS Payload Files description](https://github.com/sromanhu/Quick-CMS-Stored-XSS---Pages/assets/87250597/468a3481-7828-4f20-a02e-78205f91fe53)




We edit that Description Settings and see that we can inject arbitrary Javascript code in the Desription field.


### XSS Payload:

```js
'"><svg/onload=alert('Description')>
```


In the following image you can see the embedded code that executes the payload in the main web.
![XSS resultado Payload Files description](https://github.com/sromanhu/Quick-CMS-Stored-XSS---Pages/assets/87250597/4ca212b3-32c9-4edc-81d6-24cfca9d92be)




</br>

### Additional Information:
https://opensolution.org/cms-system-quick-cms.html

https://owasp.org/Top10/es/A03_2021-Injection/
