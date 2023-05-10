# TikTokCloner-basic
Clone Básico em html,css e js(puro)

<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>TikTok </title>
    <link rel="stylesheet" href="style.css" />
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet" />
    <link rel="shortcut icon" href="baixados.png" type="image/x-icon">
  </head>
  <body>
    <div class="app__videos">
      <!-- video starts -->
      <div class="video">
        <video class="video__player" src="Download.mp4"></video>
        
       
        
    
        <!-- sidebar -->
        <div class="videoSidebar">
          <div class="videoSidebar__button">
            <span class="material-icons"> favorite_border </span>
            <p>12</p>
          </div>

          <div class="videoSidebar__button">
            <span class="material-icons"> message </span>
            <p>23</p>
          </div>

          <div class="videoSidebar__button">
            <span class="material-icons"> share </span>
            <p>75</p>
          </div>
        </div>

        <!-- footer -->
        <div class="videoFooter">
          <div class="videoFooter__text">
            <h3>Animais engraçados</h3>
            <p class="videoFooter__description">Best Video Ever</p>

            <div class="videoFooter__ticker">
              <span class="material-icons videoFooter__icon"> music_note </span>
              <marquee>Song name</marquee>
            </div>
          </div>
          <img
            src="https://static.thenounproject.com/png/934821-200.png"
            alt=""
            class="videoFooter__record"
          />
        </div>
      </div>
      <!-- video ends -->

      <!-- video starts -->
      <div class="video">
        <video class="video__player" src="TheRock.mp4"></video>

        <!-- sidebar -->
        <div class="videoSidebar">
          <div class="videoSidebar__button">
            <span class="material-icons"> favorite_border </span>
            <p>12</p>
          </div>

          <div class="videoSidebar__button">
            <span class="material-icons"> message </span>
            <p>23</p>
          </div>

          <div class="videoSidebar__button">
            <span class="material-icons"> share </span>
            <p>75</p>
          </div>
        </div>

        <!-- footer -->
        <div class="videoFooter">
          <div class="videoFooter__text">
            <h3> The Rock</h3>
            <p class="videoFooter__description">Best Video Ever</p>

            <div class="videoFooter__ticker">
              <span class="material-icons videoFooter__icon"> music_note </span>
              <marquee>Song name</marquee>
            </div>
          </div>
          <img
            src="https://static.thenounproject.com/png/934821-200.png"
            alt=""
            class="videoFooter__record"
          />
        </div>
      </div>
      <!-- video ends -->
    </div>

    <script>
      const videos = document.querySelectorAll('video');

      for (const video of videos) {
        video.addEventListener('click', function () {
          console.log('clicked');
          if (video.paused) {
            video.play();
          } else {
            video.pause();
          }
        });
      }
    </script>
  
  </body>
</html>





css:* {
    margin: 0;
    box-sizing: border-box;
  }
  
  html {
    scroll-snap-type: y mandatory;
  }
  
  body {
    color: white;
    background-color: black;
    height: 100px;
    display: grid;
    place-items: center;
    
  }
  
  .app__videos {
    position: relative;
    height: 700px;
    background-color: white;
    overflow: scroll;
    width: 100%;
    max-width: 425px;
    scroll-snap-type: y mandatory;
    border-radius: 27px;
    border: solid 1px orange;
    margin: 20px;
    margin-bottom: 20px;
  }
  
  .app__videos::-webkit-scrollbar {
    display: none;
  }
  
  .app__videos {
    -ms-overflow-style: none;
    scrollbar-width: none;
  }
  
  .video {
    position: relative;
    height: 100%;
    width: 100%;
    background-color: white;
    scroll-snap-align: start;
  }
  
  .video__player {
    object-fit: cover;
    width: 100%;
    height: 100%;
  }
  
  .videoSidebar {
    position: absolute;
    top: 48%;
    right: 10px;
  }
  
  .videoSidebar .material-icons {
    font-size: 28px;
    cursor: pointer;
  }
  
  .videoSidebar__button {
    padding: 20px;
    text-align: center;
  }
  
  .videoFooter {
    position: absolute;
    bottom: 20px;
    margin-left: 20px;
    color: white;
    display: flex;
  }
  
  @keyframes spinTheRecord {
    from {
      transform: rotate(0deg);
    }
    to {
      transform: rotate(360deg);
    }
  }
  
  .videoFooter__record {
    animation: spinTheRecord infinite 4s linear;
    height: 50px;
    filter: invert(1);
    position: absolute;
    bottom: 0;
    right: 20px;
  }
  
  .videoFooter__text {
    flex: 1;
  }
  
  .videoFooter__text h3 {
    padding-bottom: 20px;
  }
  
  .videoFooter__icon {
    position: absolute;
  }
  
  .videoFooter__ticker {
    width: 400px;
    display: flex;
    align-items: center;
  }
  
  .videoFooter__ticker marquee {
    height: fit-content;
    margin-left: 30px;
    width: 60%;
    
  }
  
  .videoFooter__description {
    padding-bottom: 20px;
  }
  
  @media (max-width: 425px) {
    .app__videos {
      width: 100%;
      height: 100%;
      max-width: 100%;
      border-radius: 0;
    }
  }

  .video{
    position: relative;
  }
