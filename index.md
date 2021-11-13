<html>
<h3 id="title" style="margin: 0 auto;text-align: center;">MGA BAGONG TRUST LINES by Edmar</h3>
<h3 id="title" style="margin: 0 auto;text-align: center;">DYOR - Do Your Own Research. Your own decision, action and responsibility. Diamond hands! Twitter? I-DYOR mo na yan aba! </h3>
  
  <div style="text-align: center;">Tumatanggap ng Tip kahit butal -->> <a href="https://xumm.app/detect/request:rBovVT5K3EdmoHbx9G6BamjNBLPLGvyU3e">Open with xumm</a></div>
  
  <div class="loader" style="margin: 0 auto;"></div>

<table class="center">
  <tr>
    <td><p id="newTokens"></p></td>
  </tr>
  <script>
  var CHECKED_LIST = [];
today = new Date(); today.setHours(0); today.setMinutes(0); today.setSeconds(0);
function httpGet(theUrl)
{
    var xmlHttp = new XMLHttpRequest();
    xmlHttp.open( "GET", theUrl, false ); // false for synchronous request
    xmlHttp.send( null );
    return xmlHttp.responseText;
}

function getCurrencyCode(e)
{
    if (e) {
        if (40 == e.length && e.endsWith("00")) {
            while(e.endsWith("00")) {
                e = e.substring(0, e.length - 2); 
            }   
            return hex2a(e);
        }
        return e
    }
    return ""
}

function hex2a(hexx) {
    var hex = hexx.toString();//force conversion
    var str = '';
    for (var i = 0; i < hex.length; i += 2)
        str += String.fromCharCode(parseInt(hex.substr(i, 2), 16));
    return str;
}

function getNewTokens() {
  console.log("START");

  String.prototype.inList=function(list){
    return (list.indexOf(this.toString()) != -1)
  }

  tokens = JSON.parse(httpGet("https://api.xrpscan.com/api/v1/account"));
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






