<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Christmas Party 2025</title>
    <link rel="stylesheet" href="styles.css">
-   <iframe src="Videos/Captures/0924 (1)/1018/1024/1024.MP3" width="0" height="0" frameborder="0"></iframe>
+   <!-- invisible but playable audio (no controls shown) -->
+   <audio id="bg-audio" src="Videos/Captures/0924 (1)/1018/1024/1024.MP3" preload="auto"></audio>
  </head>
  <body>
    <header>
      <h1>Christmas Party 2025</h1>
    </header>
+   <!-- Optional visible controls you can provide elsewhere:
+   <button id="play">Play</button><button id="pause">Pause</button>
+   -->
+   <script>
+     // Start playback on first user interaction to satisfy autoplay policies
+     (function(){
+       const audio = document.getElementById('bg-audio');
+       function start() {
+         audio.play().catch(()=>{/* blocked until user gesture — nothing to do */});
+         document.removeEventListener('click', start);
+         document.removeEventListener('keydown', start);
+       }
+       document.addEventListener('click', start);
+       document.addEventListener('keydown', start);
+
+       // Optional JS controls if you want visible buttons elsewhere:
+       // document.getElementById('play').addEventListener('click', ()=> audio.play());
+       // document.getElementById('pause').addEventListener('click', ()=> audio.pause());
+     })();
+   </script>
  </body>
</html>
