redoc is document formatting / presentation tool that builds on top of swagger spec's.

See here for more details and examples: https://rebilly.github.io/ReDoc/

This example shows how to add redoc generated pages to the CMS in the portal by following these steps:
1) Create an area in the CMS for your documentation pages
2) Create a new documentation page and name it accordingly
3) Add a 'CA-Javascript' object to the page
4) Modify the javascript file 'redoc.plus.js' in this folder and change the URL's in the 'addElement' function at the start of the file. The URL you use should return the swagger specification for your services. In my example I have just used a template response from a simple gateway policy. You will need to use HTTPS for this to work and also enable CORS processing in the policy (see example policy provided)
----------------------------------------------------------------------------------
function addElement () { 
   updateCSS();
   var newdoc = document.createElement("redoc");
   newdoc.setAttribute('spec-url', 'https://54.252.180.149:8443/swagger/veda');
   document.body.appendChild(newdoc);
   Redoc.init('https://54.252.180.149:8443/swagger/veda', { scrollYOffset: 50});
}
----------------------------------------------------------------------------------
5) Upload the 'redoc.plus.js' file to the CA-Javascript item in the CMS. 
6) Save, Activate and Test
