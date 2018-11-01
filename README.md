# JQuery_Tutorial
## 目錄
* [環境設置](https://github.com/Ura777/JQuery_Tutorial#%E7%92%B0%E5%A2%83%E8%A8%AD%E7%BD%AE)
* [Java環境變數設置](https://github.com/Ura777/JQuery_Tutorial#java%E7%92%B0%E5%A2%83%E8%AE%8A%E6%95%B8%E8%A8%AD%E7%BD%AE)
* [Visual Studio Code相關設定](https://github.com/Ura777/JQuery_Tutorial#visual-studio-code%E7%9B%B8%E9%97%9C%E8%A8%AD%E5%AE%9A)
* [課程介紹](https://github.com/Ura777/JQuery_Tutorial#%E8%AA%B2%E7%A8%8B%E4%BB%8B%E7%B4%B9)
  * [Ch00 - Tomcat的管理](https://github.com/Ura777/JQuery_Tutorial#ch00---tomcat%E7%9A%84%E7%AE%A1%E7%90%86)
  * [Ch01 - 我的第1個jQuery](https://github.com/Ura777/JQuery_Tutorial#ch01---%E6%88%91%E7%9A%84%E7%AC%AC1%E5%80%8Bjquery)
  * [Ch02 - CSS&DOM]()
* * *
## 環境設置
* 作業系統 = Windows 7
* JDK版本 = [1.8.0_171](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* Apache Tomcat版本 = [9.0.8](https://tomcat.apache.org/download-90.cgi)
* Visual Studio Code版本 = [Windows x64 User Installer Stable Build](https://aka.ms/win32-x64-user-stable)
* jQuery版本 = [3.3.1](https://code.jquery.com/jquery-3.3.1.min.js)
* * *
## Java環境變數設置
* 取得並複製JDK安裝路徑  
 
        路徑通常為：  
		C:\Program Files\Java\jdk1.8.0_162
 
* 控制台 &gt; 所有控制台項目 &gt; 系統 &gt; 點選右邊的進階系統設定 &gt; 點選上方的進階標籤 &gt; 環境變數
* 在Administrator的使用者變數(U)區塊中點選新增按鈕，根據對應的欄位輸入以下的資料：  
 
    | 欄位名稱      | 輸入內容                            |
    |:-------------:|:-----------------------------------:|
    | 變數名稱(N)   | JAVA_HOME                           |
    | 變數值(V)     | C:\Program Files\Java\jdk1.8.0_162  |
 
* 在系統變數(S)的區塊中點選變數名稱為Path的選項 &gt; 點選編輯按鈕
* 按下鍵盤的右方向鍵 &gt; 輸入分號 &gt; 輸入以下內容：  
 
        %JAVA_HOME%\bin;
 
* 輸入完之後，一直按下確定按鈕。
* 打開命令提示字元視窗，輸入以下指令後按下Enter：  
 
        java
 
* 出現列表Java的功能列表，代表環境變數設置成功。
* * *
## Visual Studio Code相關設定
* 更改字體大小
  * 上方選單點選檔案 &gt; 喜好設定 &gt; 設定
  * 點選右邊視窗的使用者設定標籤，在下方輸入以下程式碼：
 
        {  
            "editor.fontSize": 22
        }
 
  * 按下快捷鍵Ctrl+S儲存
* * *
## 課程介紹
## Ch00 - Tomcat的管理
* 更改通訊埠
  * 去安裝Tomcat的路徑中尋找server.xml
 
        路徑通常為：  
		C:\Program Files\Apache Software Foundation\Tomcat 9.0\conf\server.xml
 
  * 使用文字編輯器開啟server.xml &gt; 尋找以下的程式碼：
 
        <Connector port="8080" protocol="HTTP/1.1"  
               connectionTimeout="20000"  
               redirectPort="8443" /> 
 
  * 將8080改成想要設定的數字
 
        例如：
		80
 
  * 修改完成後儲存檔案 &gt; 重新啟動Tomcat
* 虛擬資料夾與真實資料夾的對應
  * 去安裝Tomcat的路徑中尋找server.xml
 
        路徑通常為：  
		C:\Program Files\Apache Software Foundation\Tomcat 9.0\conf\server.xml
 
  * 使用文字編輯器開啟server.xml &gt; 尋找以下的程式碼：
 
        <Host name="localhost"  appBase="webapps"  
            unpackWARs="true" autoDeploy="true">
 
  * 在上述的程式碼下方新增以下的程式碼：
 
        <Context path="/虛擬資料夾名稱" docBase = "實體資料夾位置" debug="0" />  
		  
		例如：  
		<Context path="/test" docBase = "C:\JavaScript_Tutorial" debug="0" />
 
  * 修改完成後儲存檔案 &gt; 重新啟動Tomcat
  * 虛擬資料夾與實體資料夾的名稱都不能有中文字
* * *
## Ch01 - 我的第1個jQuery
* Import jQuery
  * Download jQuery [v3.3.1](https://code.jquery.com/jquery-3.3.1.min.js)
  * 滑鼠點擊右鍵 &gt; 另存新檔
  * 使用以下的程式碼將jquery.js匯入
  
        <script src="存放jquery.js的資料夾名稱/jquery-3.3.1.min.js"></script>
  
* 我的第1個jQuery
  * 利用jQuery套用CSS到清單的項目中
* 串聯 Chaining
  * jQuery依序呼叫多個函數
* 回撥函數 Callback Function
  * jQueyr的動畫效果都是使用此來達成
* * *
## Ch02 - CSS&DOM
* 新增DOM元素
  * 新增後會成為最後1個子元素
  * appendTo()
* 指定DOM元素套用CSS樣式
  * addClass();
* 所有元素都套用CSS樣式
  * 選擇器的部分填寫"*"
* 使用ID屬性來選擇元素
* 使用Class屬性來選擇元素
* 使用多個Class屬性來選擇元素
* 使用巢狀Class屬性來選擇元素
  * 選擇器寫法說明如下：
 
        父元素是div，子元素是p。
        例如："div p"
 
        父元素是div的p子元素。
        例如："div > p"

        緊接著div元素之後的span兄弟元素。
        例如："div + span"
 
* 同時選擇多種不同的元素
  * 使用逗號來隔開選擇器
  * 可以使用組合HTML Tag名稱與class屬性、id屬性，來選擇特定的元素。
* 篩選選擇器Even & Odd
  * 篩選符號是「:」，「:」之後的就是篩選屬性。
  * 可以用來完成表格的斑馬樣式
* 篩選選擇器First & Last
* 篩選選擇器Has & Empty
  * has(指定元素) -&gt; 只要有指定元素就好，不一定需要是直接子元素。
  * empty -> 符合選擇器所指定而且沒有任何內容的空元素
* 篩選選擇器Contains
  * contains('指定字串') -&gt; 篩選出包含指定字串內容的元素。
* 屬性選擇器 - 選擇包含指定網址的超連結
  * 屬性選擇器是使用正規運算式(Regular Expression)的符號來找到目標。
  * 字串符號 -&gt; *
  * 開頭字串符號 -&gt; ^
  * 結尾字串 -&gt; $
  * *= -&gt; 表示只需要包含等號後面的值就算是符合條件
* 屬性選擇器 - 選擇ID屬性值是特定開頭或結尾的元素
  * $= -&gt; 表示只需要結尾是等號後面的值就算是符合條件
* 讀取指定元素的CSS
  * css()
  * 參數為CSS樣式屬性名稱，例如：color、font-size。
* 設定指定元素的CSS
  * css()
  * 參數為("CSS樣式屬性名稱","CSS樣式屬性值")。
  * 也可以一次設定多個CSS樣式，樣式之間使用「,」隔開。
* 新增指定元素的CSS
  * addClass()
  * 參數為CSS樣式選擇器名稱
* 移除指定元素的CSS
  * removeClass()
  * 沒有參數時，移除所有的CSS。
  * 有參數時，移除特定的CSS。
  * 可以一次移除多個CSS，CSS之間用1個半形的空白字元分隔。
* 新增或移除指定元素的CSS
  * toggleClass()
  * 當指定的元素沒有套用指定的CSS時，就會套用。
  * 當指定的元素已經套用指定的CSS時，就會移除。
* 取代DOM子元素
  * html()是取代成另外一個HTML子元素
  * text()是取代文字內容
* 新增DOM子元素
  * prepend()是新增成為第1個子元素
  * append()是新增成為最後1個子元素
* 插入DOM子元素
  * before()是在指定的元素前面插入兄弟元素。
  * after()是在指定的元素後面插入兄弟元素。
* 移除DOM子元素
  * remove()
* 取得被包裝在jQuery物件的DOM元素個數
  * 使用.length取得
* 直接存取DOM元素
  * 對於取回的jQuery物件，因為被包裝的DOM元素可能不只1個。
  * 使用get()來取出指定的DOM元素
  * 參數為index，從0開始。
  * 也可以使用類似陣列所以方式來取得DOM元素
  * .textContent屬性可以取得指定DOM元素的文字內容
* * *


