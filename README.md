# JQuery_Tutorial
## 目錄
* [環境設置]()
* [Java環境變數設置]()
* [Visual Studio Code相關設定]()
* [課程介紹]()
  * [Ch00 - Tomcat的管理]()
* * *
## 環境設置
* 作業系統 = Windows 7
* JDK版本 = [1.8.0_171](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* Apache Tomcat版本 = [9.0.8](https://tomcat.apache.org/download-90.cgi)
* Visual Studio Code版本 = [Windows x64 User Installer Stable Build](https://aka.ms/win32-x64-user-stable)
* jQuery版本 = 3.3.1(https://code.jquery.com/jquery-3.3.1.min.js)
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
  * Download jQuery v3.3.1(https://code.jquery.com/jquery-3.3.1.min.js)
  * 使用以下程式碼將jquery.js匯入
  
        <script src="存放jquery.js的資料夾名稱/jquery-3.3.1.min.js"></script>
  
* 我的第1個jQuery
  * 利用jQuery套用CSS到清單的項目中
* 串聯 Chaining
  * jQuery依序呼叫多個函數
* 回撥函數 Callback Function
  * jQueyr的動畫效果都是使用此來達成

