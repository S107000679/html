<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
	<title>T-shirt 王的行動網站</title>
	<link rel="stylesheet" href="http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.css" />
    <script src="http://code.jquery.com/jquery-2.2.3.min.js"></script>
    <script src="http://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.js"></script>    
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<script>
	  var i = 0;
      var img = new Array("google衣服.jpg", "google衣服2.jpg", "google衣服3.jpg");
      var msg = new Array("Docker是一個開放原始碼軟體專案，讓應用程式部署在軟體貨櫃下的工作可以自動化進行", 
	    "Dockers是有能力打包應用程式及其虛擬容器，可以在任何Linux伺服器上執行的依賴性工具", 
		"Docker利用Linux核心中的資源分離機制，例如cgroups，以及Linux核心命名空間（namespaces），來建立獨立的容器（containers）"); 
	  function prev(){
	    i--; 
	    if (i < 0) {i = 2;}
	    $("#roleimg").attr("src", img[i]);		
		$("#rolemsg").text(msg[i]);
      }
	  function next(){
	    i++; 
	    if (i > 2) {i = 0;}
	    $("#roleimg").attr("src", img[i]);		
		$("#rolemsg").text(msg[i]);
      }
	</script>
  </head>
  <body>  
    <div data-role="page" id="home">
      <div data-role="header" data-position="fixed">  
 	    <h1>T-shirt google</h1>
      </div>
      <div data-role="content">	    
		<img src="google衣服.jpg" width="100%"> 
	    <a href="#story" data-rel="dialog" data-role="button" data-icon="arrow-r">google介紹</a>
		<a href="#role" data-role="button" data-icon="arrow-r">google功能介紹</a>
		<a href="https://www.google.com.tw/" data-rel="external" data-role="button" data-icon="arrow-r">google官方網站</a>
	  </div>
      <div data-role="footer" data-position="fixed">
	    <h4>&copy;快樂學Docker</h4>
	  </div>
    </div>
	
	<div data-role="page" id="story">
	  <div data-role="header">
	    <h1>google介紹</h1>	            
      </div>
      <div data-role="content">
        <p>是源自美國的跨國科技公司，為Alphabet Inc.的子公司，業務範圍涵蓋網際網路廣告、網際網路搜尋、
		雲端運算等領域，開發並提供大量基於網際網路的產品與服務，其主要利潤來自於AdWords等廣告服務。
		Google由在史丹佛大學攻讀理工博士的賴利·佩吉和謝爾蓋·布林共同建立，因此兩人也被稱為「Google Guys」</p>
      </div>
	</div>
	
	<div data-role="page" id="role">
	  <div data-role="header">
	    <h1>google介紹</h1>	            
      </div>
	  <div data-role="content">
	    <img id="roleimg" src="google.jpg" width="100%">
		<p id="rolemsg">1996年1月，加州史丹佛大學理學博士生的賴利·佩吉和謝爾蓋·布林在學校開始研究一項關於搜尋的研究專案。
		區別於傳統搜尋根據關鍵字在頁面中出現次數來進行結果排序的方法，兩人開發了一個對網站之間的關係做精確分析的搜尋引擎。
		[29]這個名為PageRank的引擎通過檢查網頁中的反向連結以評估站點的重要性，此引擎的精確度勝於當時的基本搜尋技術。
		最初，佩吉和布林將這個搜尋引擎命名為「BackRub」，直到後來改為「Google」。這個新名字來源於一個數學大數googol
		（數字1後有100個0，即自然數10100）單字錯誤的拼寫方式，象徵著為人們提供搜尋海量優質資訊的決心。
		Google搜尋引擎在史丹佛大學的網站上啟用，域名為google.stanford.edu。</p>
	  </div>
	  <div data-role="footer" data-position="fixed">
	    <div data-role="navbar">
	      <ul>
            <li><a href="#home" class="ui-btn-active ui-state-persist">回首頁</a></li>
            <li><a href="javascript:prev();">上一個</a></li>
            <li><a href="javascript:next();">下一個</a></li>
          </ul>
	    </div>  
      </div>
	</div>	
  </body>
</html>
