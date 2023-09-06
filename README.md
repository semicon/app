# link ตัดแถบสีเทา webapps
https://semicon.github.io/app/?apps=[url webapps]

# example:
https://semicon.github.io/app/?apps=https://script.google.com/macros/s/AKfycbzEYcTuj-nCd37T5fyE5nlG7QAm_0dn5GfYWrTX9l096pP5695gvPzHe91jaS2b6GD3Cg/exec

# Code

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
    <iframe id="myframe" class="responsive-iframe" src="" allowFullScreen="allowFullScreen"></iframe>
  </div>
  <script>
    const apps = new URL(window.location);
    const formUrl = apps.searchParams.get('apps');
    const url = decodeURIComponent(formUrl)
          document.getElementById('myframe').src = url
  </script>

