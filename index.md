<html>
<h3 id="title" style="margin: 0 auto;text-align: center;">MGA BAGONG TRUST LINES by Edmar</h3>
<h3 id="title" style="margin: 0 auto;text-align: center;">DYOR - Do Your Own Research. Your own decision, action and responsibility. Diamond hands! Twitter? I-DYOR mo na yan aba! </h3>
  
  <div style="text-align: center;">Tumatanggap ng Tip kahit butal -->> <a href="https://xumm.app/detect/request:rBovVT5K3EdmoHbx9G6BamjNBLPLGvyU3e">Open with xumm</a></div>
  
  <div class="loader" style="margin: 0 auto;"></div>

function getNewTokens() {
  console.log("START");

  String.prototype.inList=function(list){
    return (list.indexOf(this.toString()) != -1)
  }

  tokens = JSON.parse(httpGet(""));
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





