<html>
<style>
@media print{
   .noprint{
       display:none;
   }
}
</style>

<p id="fname"></p>
<p id="lname"></p>
<p id="email"></p>
<p id="phone"></p>
<p id="mphone"></p>
<p id="street"></p>
<p id="streetnr"></p>
<p id="zip"></p>
<p id="city"></p>
<p id="country"></p>
<p id="qr_uuid"></p>


<img src="https://api.qrserver.com/v1/create-qr-code/?data=https://driverdotcentric.com/download?p=3b8adecf-cce5-4002-8987-fd8136220228%26h=" id="qr-code"/>

<div class="noprint">
<button onclick="printF()">Print me</button>
</div>

</html>

<script language="JavaScript">
  function processParams(){
	var url_string = window.location.href
    var url = new URL(url_string);
    document.getElementById("fname").innerHTML =  'First Name: ' + url.searchParams.get("fname");
    document.getElementById("lname").innerHTML =  'Last Name: ' + url.searchParams.get("lname");
    document.getElementById("email").innerHTML =  'E-Mail Address: ' + url.searchParams.get("email");
    document.getElementById("phone").innerHTML =  'Phone Number: ' + url.searchParams.get("phone");
    document.getElementById("mphone").innerHTML =  'Mobile Phone Number: ' + url.searchParams.get("mphone");
    document.getElementById("street").innerHTML =  'Street: ' + url.searchParams.get("street");
    document.getElementById("streetnr").innerHTML =  'House Number: ' + url.searchParams.get("streetnr");
    document.getElementById("zip").innerHTML =  'Postal Code: ' + url.searchParams.get("zip");
    document.getElementById("city").innerHTML =  'City: ' + url.searchParams.get("city");
    document.getElementById("country").innerHTML =  'Country Name: ' + url.searchParams.get("country");
	document.getElementById("qr_uuid").innerHTML =  'QR UUID: ' + url.searchParams.get("qr_uuid");
	document.getElementById("qr-code").src = 'https://api.qrserver.com/v1/create-qr-code/?data=https://driverdotcentric.com/download?p=3b8adecf-cce5-4002-8987-fd8136220228%26h=' + url.searchParams.get("qr_uuid");
  }
  processParams();
  function printF(){
	window.print();
  }
</script>
