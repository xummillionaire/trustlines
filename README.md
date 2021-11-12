
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>XRPL Trustline Status</title>
	<link rel="stylesheet" type="text/css" href="/style-min.css?v=1.2.8">
	<!-- Global site tag (gtag.js) - Google Analytics -->
	<script async src="https://www.googletagmanager.com/gtag/js?id=G-H4FDXQ0WMV"></script>
	<script>
	  window.dataLayer = window.dataLayer || [];
	  function gtag(){dataLayer.push(arguments);}
	  gtag('js', new Date());

	  gtag('config', 'G-H4FDXQ0WMV');
	</script>	
</head>
<body>
	<nav>
	  <a href="https://trustlines.xrplstatus.com/">Trustlines</a>
	  <a href="https://orders.xrplstatus.com/">Limit Orders</a>
	  <a href="https://helpvincent.xrplstatus.com/">Help VINCENT</a>
	</nav>
	<h1>XRPL Trustline Status</h1>
	<p class="intro step1">1. Enter your XRP Ledger account address to retrieve your account's trustlines:</p>
	<fieldset class="form">
		<form onsubmit="return false;">
			<input type="text" name="address" id="address" placeholder="Enter your XRP Ledger address" minlength="25" maxlength="35">
			<input type="button" name="go" id="submit_address" value="Go">
		</form>
	</fieldset>
	<p class="intro step2">2. Choose a trustline to load its status. All <em>its</em> trustlines (including yours) are then stacked sequentially side by side to form a "progress bar" and give a visual representation of which accounts <em>might</em> have had the airdrop.</p>	
	<div class="legend">
		<span class="off">=0 balance</span>
		<span class="on">>0 balance</span>
		<span class="stats"></span>
	</div>	
	<div id="output"></div>
	<p class="copyright"><img src="/logo.gif" width="50" height="50"><br>© 2021 XRP Fact Checker<br><br><strong>TipBot setup for sending tips: <a href="https://tipbot.tips/" target="_blank">https://tipbot.tips/</a></strong></p>
	<p class="credit">
		<a class="twitter" href="https://twitter.com/intent/user?screen_name=xrpfactchecker" target="_blank"><i></i>@xrpfactchecker</a>
		<a class="twitter tipbot" onclick="alert('Be sure to setup TipBot (tipbot.tips) successfully before sending a tip. Thank you!');" href="https://twitter.com/intent/tweet?text=%2B1%20xrp%20%40xrpfactchecker%20%23tipwithxumm" target="_blank"><i></i>Tip 1 XRP</a>		
	</p>
	<script type="text/javascript">
		let account_address = '';
		let preload_issuer  = '';
	</script>	
	<script type="text/javascript" src="/trustlines-min.js?v=1.2.8"></script>
</body>
</html>
