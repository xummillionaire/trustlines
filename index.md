
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">

<!-- Begin Jekyll SEO tag v2.7.1 -->
<title>trustlines</title>
<meta name="generator" content="Jekyll v3.9.0" />
<meta property="og:title" content="trustlines" />
<meta property="og:locale" content="en_US" />
<link rel="canonical" href="https://xummillionaire.github.io/trustlines/" />
<meta property="og:url" content="https://xummillionaire.github.io/trustlines/" />
<meta property="og:site_name" content="trustlines" />
<meta name="twitter:card" content="summary" />
<meta property="twitter:title" content="trustlines" />
<script type="application/ld+json">
{"url":"https://xummillionaire.github.io/trustlines/","@type":"WebSite","headline":"trustlines","name":"trustlines","@context":"https://schema.org"}</script>
<!-- End Jekyll SEO tag -->

    <link rel="stylesheet" href="/trustlines/assets/css/style.css?v=bc4e68b307ce7956a7bc2467b78cf42b08b67f22">
    <!-- start custom head snippets, customize with your own _includes/head-custom.html file -->

<!-- Setup Google Analytics -->



<!-- You can set your favicon here -->
<!-- link rel="shortcut icon" type="image/x-icon" href="/trustlines/favicon.ico" -->

<!-- end custom head snippets -->

  </head>
  <body>
    <div class="container-lg px-3 my-5 markdown-body">
      
      <h1><a href="https://xummillionaire.github.io/trustlines/">trustlines</a></h1>
      

      <html>
<h3 id="title" style="margin: 0 auto;text-align: center;">MGA BAGONG TRUST LINES by Edmar</h3>
<h3 id="title" style="margin: 0 auto;text-align: center;">DYOR - Do Your Own Research. Your own decision, action and responsibility. Diamond hands! Twitter? I-DYOR mo na yan aba! </h3>
  <div style="text-align: center;">Tumatanggap ng Tip kahit butal --&gt;&gt; <a href="https://xumm.app/detect/request:rBovVT5K3EdmoHbx9G6BamjNBLPLGvyU3e">Open with xumm</a></div>
  <div class="loader" style="margin: 0 auto;"></div>
<table class="center">
  <tr>
    <td><p id="newTokens"></p></td>
  </tr>
  <script>
  var CHECKED_LIST = [];
today = new Date(); today.setHours(0); today.setMinutes(0); today.setSeconds(0);



function getNewTokens() {
  console.log("START");
  String.prototype.inList=function(list){
    return (list.indexOf(this.toString()) != -1)
  }
  tokens = JSON.parse(httpGet("https://api.xrpldata.com/api/v1/tokens"));
  var total = 0;
  var allLink = '';
  var newTokens = '';
  for(var token in tokens.issuers) {
      var currencyCode = getCurrencyCode(tokens.issuers[token].tokens[0].currency);
      var createdDate = new Date(Date.parse(tokens.issuers[token].tokens[0].created.date));
      if(createdDate > today && CHECKED_LIST.indexOf(currencyCode) == -1) {
          total++
          var amount = tokens.issuers[token].tokens[0].amount;
          var url = 'https://xumm.community/?issuer='+ token + "&currency=" + currencyCode + '&limit=' + amount;
          
          var kyc = tokens.issuers[token].data.kyc ? 'YES' : 'NO'
          allLink = allLink + '_____________________DYOR    '   +   total + '<br>'
                            + 'Currency: $' + currencyCode + '<br>' + 'KYC: ' + kyc + '<br>'
                            + 'Created date: ' + createdDate + ' | ' + 'Total trustline: ' + tokens.issuers[token].tokens[0].trustlines + '<br>'
                            + 'LINK: ' + url.link(url) + '<br>';
      }
  }
   document.getElementById("newTokens").innerHTML = allLink;
  console.log('END');
}
getNewTokens();
setInterval(getNewTokens, 45000);
</script>
</table></html>


      
    </div>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/anchor-js/4.1.0/anchor.min.js" integrity="sha256-lZaRhKri35AyJSypXXs4o6OPFTbTmUoltBbDCbdzegg=" crossorigin="anonymous"></script>
    <script>anchors.add();</script>
  </body>
</html>
