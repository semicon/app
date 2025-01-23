![image](https://github.com/semicon/app/assets/30399464/bc6fe924-844e-4366-a139-b11d9116492b)

# link ปิดแถบแจ้งเตือน Google Apps Script
1) สร้าง repo ของ github และสร้างไฟล์ index.html ใน repo
2) Build and deployment pages
3) เรียกใช้ URL และใส่  parameter URL.exec ต่อท้าย
   
https://semicon.github.io/app/?apps=[URL.exec webapps]

# example:
https://semicon.github.io/app/?apps=https://script.google.com/macros/s/AKfycbzEYcTuj-nCd37T5fyE5nlG7QAm_0dn5GfYWrTX9l096pP5695gvPzHe91jaS2b6GD3Cg/exec

# Code

<pre>
   // style CSS
  <style>
    .responsive-iframe {
      position: absolute;
      top: 0;
      left: 0;
      bottom: 0;
      right: 0;
      width: 100vw;
      height: 100vh;
      border: none;
    }
  </style>



  <div> 
    // HTML Tag
    <iframe id="myframe" class="responsive-iframe" src="" allowFullScreen></iframe>
  </div>

 

<br><br>
 // Java Script 
  <script>
    const apps = new URL(window.location);
    const formUrl = apps.searchParams.get('apps');
    const url = decodeURIComponent(formUrl)
          document.getElementById('myframe').src = url
  </script>
</pre>
