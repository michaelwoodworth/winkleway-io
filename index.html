<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>The Winkle Way</title>
<style>
  :root {
    --cream:#f8f4ed; --sand:#e4dfd2; --rockweed:#c6c2a5; --ink:#584c34;
  }
  html,body{
    height:100%; margin:0; background:linear-gradient(to bottom,var(--cream),var(--sand) 60%,var(--rockweed));
    font-family:system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif; color:#222;
  }
  .hero-wrap{
    position:relative; max-width:1200px; margin:6vh auto; border-radius:16px; overflow:hidden;
    box-shadow:0 12px 36px rgba(0,0,0,.22); aspect-ratio:16/9; background:#000;
  }
  .hero-wrap iframe{ position:absolute; inset:0; width:100%; height:100%; border:0; }
  .shoreline{
    position:fixed; left:0; right:0; bottom:0; height:38vh; pointer-events:none; opacity:.08;
    background:url('data:image/svg+xml;utf8,\
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 400">\
        <path d="M0,300 C200,250 400,350 600,300 C800,250 1000,350 1200,300 L1200,400 L0,400 Z" fill="none" stroke="%23584c34" stroke-width="2"/>\
        <path d="M50,330 q80,-25 160,0 t160,0 t160,0 t160,0 t160,0" fill="none" stroke="%23584c34" stroke-width="1"/>\
      </svg>') center bottom/cover no-repeat;
  }

  /* Unmute button */
  .unmute-btn{
    position:absolute; right:12px; bottom:12px; z-index:5;
    border:0; border-radius:999px; padding:.65rem .9rem; font-weight:600;
    background:rgba(248,244,237,.9); color:#222; box-shadow:0 4px 16px rgba(0,0,0,.25);
    display:flex; align-items:center; gap:.5rem; cursor:pointer;
    backdrop-filter:saturate(140%) blur(2px);
  }
  .unmute-btn:hover{ transform:translateY(-1px); }
  .unmute-btn:active{ transform:translateY(0); }
  .unmute-icon{
    width:18px; height:18px; display:inline-block;
    background:url('data:image/svg+xml;utf8,\
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">\
        <path fill="%23222" d="M5 10v4h3l4 3V7l-4 3H5zm10.54 1a4.5 4.5 0 0 1-2.2 3.9l.84 1.46A6 6 0 0 0 18.54 11a6 6 0 0 0-4.36-5.36l-.84 1.46A4.5 4.5 0 0 1 15.54 11z"/>\
      </svg>') center/contain no-repeat;
  }
  .sr-only{ position:absolute; width:1px; height:1px; padding:0; margin:-1px; overflow:hidden; clip:rect(0,0,0,0); white-space:nowrap; border:0; }
</style>
</head>
<body>
  <!-- Optional tiny title -->
  <!-- <div class="site-title" style="text-align:center;letter-spacing:.06em;font-weight:600;margin:2.5vh 0 0;opacity:.75;">The Winkle Way</div> -->

  <div class="hero-wrap">
    <!-- IMPORTANT: set ORIGIN below to your exact site origin (no trailing slash) -->
    <iframe id="hero-iframe"
      src="https://www.youtube-nocookie.com/embed/ooVDvDKgDjA?autoplay=1&mute=1&playsinline=1&rel=0&modestbranding=1&enablejsapi=1&origin=https://thewinkleway.com"
      title="The Winkle Way Hero Video"
      allow="autoplay; accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      referrerpolicy="origin-when-cross-origin"
      allowfullscreen
      loading="eager">
    </iframe>

    <button class="unmute-btn" id="unmuteBtn" type="button" aria-pressed="false">
      <span class="unmute-icon" aria-hidden="true"></span>
      Unmute
      <span class="sr-only"> video</span>
    </button>
  </div>

  <div class="shoreline"></div>

  <script>
    (function(){
      const iframe = document.getElementById('hero-iframe');
      const btn = document.getElementById('unmuteBtn');
      const videoId = "ooVDvDKgDjA";
      const base = "https://www.youtube-nocookie.com/embed/" + videoId;
      const common = "playsinline=1&rel=0&modestbranding=1&enablejsapi=1&origin=https%3A%2F%2Fthewinkleway.com";

      function postCommand(func, args=[]){
        try {
          iframe.contentWindow.postMessage(JSON.stringify({event:"command", func, args}), "*");
        } catch(e) {
          /* ignore – we'll fallback if needed */
        }
      }

      btn.addEventListener('click', () => {
        // Preferred: unmute via postMessage (no external API file required)
        postCommand("unMute");
        postCommand("setVolume", [80]);
        postCommand("playVideo");

        // Visual state
        btn.setAttribute('aria-pressed','true');
        btn.textContent = "Sound on";

        // Fallback: if unmute didn’t take (e.g., blocked), reload with sound.
        // Give it a short moment; if still muted, reload src with mute=0.
        setTimeout(() => {
          // We can't read player state without the full API, so we just force a sound-on reload.
          // Users expect this on first tap anyway.
          const withSound = `${base}?autoplay=1&mute=0&${common}`;
          // Only switch if we're still on a muted URL
          if (iframe.src.includes("mute=1")) {
            iframe.src = withSound;
          }
        }, 250);
      });

      // Keyboard access: space/enter to toggle
      btn.addEventListener('keydown', (e) => {
        if (e.key === 'Enter' || e.key === ' ') {
          e.preventDefault();
          btn.click();
        }
      });
    })();
  </script>
</body>
</html>
