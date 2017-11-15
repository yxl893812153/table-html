# table-html
实现控件的自由组合
<!DOCTYPE html>
<html>
<head>
	<meta http-equiv="content-type" content="txt/html; charset=utf-8" />
	<title>有问题请联系scuyzl@qq.com</title>
</head>
<body>

	<style type="text/css" media="screen">
	.tdclass{
		height: 120px;
		width: 100px;
		float: left;
		text-align: center;
	}
	.tableclass{
		float: left;
		border: 1px;
	}
		
	</style>




    <table id = "table1" style="float: left;">
    	<tr id='third'>
			<td id="ftop" >
			</td>
			
		</tr>
    </table> 


     <table id = "table2"  style="float: left;">
    	<tr id='forth'>
			<td id="ffth" >
			</td>
		</tr>
    </table>  


	<table border="1" style="float: left; clear: both;" id="tablea">	
		<tr id="second1">
			<td class="tdclass" id="first">
				<span id="shang" onclick="tops()" style="height: 19px; width: 100%; display: block; margin-top: 0px; float: left;"></span>
				<span id="zuo" onclick="leftz()" style="height: 80px; width: 10px; display: block; float: left; "></span>
				A
				<span id="middle1" onclick="mids()" style="height: 80px; width: 10px; display: block; margin-right: 0px; float: right;"></span>
				<span id="xia" style="height: 19px; width: 100%; display: block; float: left;"></span>
			    
		    <!-- <td style="text-align: center; height: 120px; width: 100px;"></td> -->
<!-- 			<td style="text-align: center; height: 140px; width: 100px;">B</td> -->
		</tr>
	</table>

		<table border="1" style="float: left;" id="tableb">	
		<tr id="second2">
			<td class="tdclass" id="second" >
				<span id="shang" onclick="tops()" style="height: 19px; width: 100%; display: block; margin-top: 0px; float: left;"></span>
				<span id="middle2" onclick="mids2()" style="height: 80px; width: 10px; display: block; float: left; "></span>
				B
				<span id="you" onclick="righty()" style="height: 80px; width: 10px; display: block; margin-right: 0px; float: right;"></span>
				<span id="xia" style="height: 19px; width: 100%; display: block; float: left;"></span>
			    
		    <!-- <td style="text-align: center; height: 120px; width: 100px;"></td> -->
<!-- 			<td style="text-align: center; height: 140px; width: 100px;">B</td> -->
		</tr>
	</table>

	<!-- <table border="1" style="float: left;">
		<tr id="second2">
		<td id="second" class="tdclass">
				<span id="shang" onclick="tops()" style="height: 19px; width: 100%; display: block; margin-top: 0px; float: left;"></span>
				<span id="middle2" onclick="mids2()" style="height: 80px; width: 10px; display: block; float: left;"></span>
				B
				<span id="you" onclick="righty()" style="height: 80px; width: 10px; display: block; margin-right: 0px; float: right;"></span>
				<span id="xia" style="height: 19px; width: 100%; display: block; float: left;"></span>
			    
		    </td>
		    <tr>
	</table> -->


<script type="text/javascript">
	function righty(){
		var node = document.getElementById("table2");
		var node2 = document.getElementById("tablea");
		var node3 = document.getElementById("tableb");
		if(ftop){
			node.className = "tableclass";
			node.style.height = "254px";
			node.style.border = '1px solid #000000';
			node2.style.marginTop = '-128px';
			node3.style.marginTop = "-128px";
		}
		if(!ftop){
			node.className = "tableclass";
			node.style.border = '1px solid #000000';
		}
		var node1 = document.getElementById("ffth");
		node1.className = "tdclass";
		// node.className = "tdclass";
		// var texttd = document.createTextNode("D");
		// node.appendChild(texttd);
		// document.getElementById("third").appendChild(node);
	}

	function leftz(){
		var node = document.getElementById("second1");
		var newnode = document.createElement("td");
		newnode.className = "tdclass";
		var refernode  = document.getElementById("first");
		newnode.innerHTML = "D";
		node.insertBefore(newnode,refernode);
	}

	function mids2(){
	 	var node = document.getElementById("second2");
		var newnode = document.createElement("td");
		newnode.className = "tdclass";
		var refernode  = document.getElementById("second");
		newnode.innerHTML = "D";
		node.insertBefore(newnode,refernode);

	 }

	  function tops(){
	  	var node1 = document.getElementById("table1");
	  	node1.className = "tableclass";
	  	node1.style.border = '1px solid #000000';
	  	var node = document.getElementById("ftop");
	  	node.className = "tdclass";
	  	node.style.width = "212px" ;
	  }
	 //  function mids(){
	 //  	var node = document.createElement("td");
		// node.className = "tdclass";
		// var texttd = document.createTextNode("C");
		// node.appendChild(texttd);
		// document.getElementById("second").appendChild(node);


	 //  }
	 
</script>
</body>
</html>
