![image](https://github.com/semicon/app/assets/30399464/bc6fe924-844e-4366-a139-b11d9116492b)

# link ปิดแถบแจ้งเตือน Google Apps Script
https://semicon.github.io/app/?apps=[url webapps]

# example:
https://semicon.github.io/app/?apps=https://script.google.com/macros/s/AKfycbzEYcTuj-nCd37T5fyE5nlG7QAm_0dn5GfYWrTX9l096pP5695gvPzHe91jaS2b6GD3Cg/exec

# Code
<code>
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
    <iframe id="myframe" class="responsive-iframe" src="" allowFullScreen></iframe>
  </div>

  
  <script>
    const apps = new URL(window.location);
    const formUrl = apps.searchParams.get('apps');
    const url = decodeURIComponent(formUrl)
          document.getElementById('myframe').src = url
  </script>
</code>
