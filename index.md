<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <title>Falanadnami</title>
    <meta
      name="viewport"
      content="width=device-width, user-scalable=no, minimum-scale=1.0, maximum-scale=1.0"
    />
    <meta name="apple-mobile-web-app-capable" content="yes" />
    <meta aframe-injected="" name="mobile-web-app-capable" content="yes" />
    <script src="https://aframe.io/releases/1.1.0/aframe.min.js"></script>
    <script src="https://supermedium.com/superframe/components/audioanalyser/examples/build.js"></script>
    <script src="https://supermedium.com/superframe/components/audioanalyser/examples/components/audioanalyser-volume-bind.js"></script>
    <script src="https://supermedium.com/superframe/components/audioanalyser/examples/components/audioanalyser-waveform.js"></script>
    <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
  </head>
  <body>
    <a-scene
      antialias="true"
      renderer="logarithmicDepthBuffer: true;"
      embedded
      loading-screen="enabled: false;"
      arjs="sourceType: webcam; debugUIEnabled: false;"
    >
      <a-assets>
        <audio
          id="song"
          src="https://cdn.glitch.com/d0ed2509-3236-43cf-8b1d-42bed0438605%2Fdzwony_rozne_z_czech.wav?v=1623330504643"
          autoplay
          loop
        ></audio>
      </a-assets>

      <a-entity
        id="analyser"
        audioanalyser="src:#song"
        audioanalyser-waveform="radius:0.5"
        rotation="90 0 0"
        position="0 5 0"
        scale="0.5 0.5 0.5"
        visible=""
        look-controls="true"
      ></a-entity>

      <a-camera
        position="0 0 0"
        rotation=""
        camera="active:true"
        look-controls="true"
        wasd-controls=""
        data-aframe-inspector-original-camera=""
      ></a-camera>
    </a-scene>
  </body>
</html>

