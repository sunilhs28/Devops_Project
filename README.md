# HDFC-Bank-New

<HTML>
<HEAD>
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<!-- 201709/SFR/Flex@/031 : cross frame scripting - Netbanking | High Start-->
<style id="antiClickjack">body{display:none !important;}</style>
<script type="text/javascript">
   if (self === top) {
       var antiClickjack = document.getElementById("antiClickjack");
       antiClickjack.parentNode.removeChild(antiClickjack);
   } else {
       top.location = self.location;
   }
</script>
<!-- 201709/SFR/Flex@/031 : cross frame scripting - Netbanking | High  End-->
<TITLE>Welcome to HDFC Bank NetBanking</TITLE>
<script language="javascript">
	var daemon			= 'NETBANKING';
	var p_remoteaddress	= '';
	var RsaAuthReq		= '';
	
	var l_path = window.location.pathname;

	if(l_path == undefined || l_path == '' || l_path.indexOf("/netbanking") < 0){
		window.location.href = window.location.protocol + "//" + window.location.host +"/netbanking";
	}
	<!-- FLEXENH-674-06/11/2020-Roshni Soni-CTA handling for BB Redirection-START-->
	var redirectParam = getQueryVariable("redirect");
	function getQueryVariable(variable) { 
		var query = window.location.search.substring(1);
		var vars = query.split("&");
			for (var i=0;i<vars.length;i++){	
				console.log(vars[i]);
				var pair=vars[i].split("=");
				if (pair[0] == variable) {
					return pair[1];
				}
			}
	}
	<!-- FLEXENH-674-06/11/2020-Roshni Soni-CTA handling for BB Redirection-END-->
</script>
</HEAD>
	<FRAMESET border="false" frameBorder="O" frameSpacing="0" rows="*" cols="*">
		<FRAMESET border="false" frameBorder="O" frameSpacing="0" rows="*,30" cols="*">
			<FRAME marginwidth="0" marginheight="0" NAME="login_page" SRC="RSNBLogin.html?v=18" NORESIZE="true" scrolling="yes"/>
			<!--<FRAME marginwidth="0" marginheight="0" NAME="footer" SRC="footer.html" NORESIZE="true" scrolling="no"/>-->
		</FRAMESET>
	</FRAMESET>
</HTML>
