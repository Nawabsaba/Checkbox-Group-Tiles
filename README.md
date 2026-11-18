# Checkbox-Group-Tiles


# HTML Program : -
      <!DOCTYPE html>
      <html lang="en">
         <head>
            <meta charset="UTF-8" />
            <meta http-equiv="X-UA-Compatible" content="IE=edge" />
            <meta name="viewport" content="width=device-width, 
                 initial-scale=1.0" />
          <link rel="stylesheet" href="style.css" />
       <title>Checkbox Group Tiles</title>
        </head>
        <body>
        <div class="checkbox-group">

      <div class="checkbox">
        <label class="checkbox-wrapper">
          <input type="checkbox" class="checkbox-input">
          <span class="checkbox-tile">
            <span class="checkbox-icon">
              <ion-icon name="logo-github"></ion-icon>
            </span>
            <span class="checkbox-label">Github</span>
          </span>
        </label>
      </div>
      <div class="checkbox">
        <label class="checkbox-wrapper">
          <input type="checkbox" class="checkbox-input">
          <span class="checkbox-tile">
            <span class="checkbox-icon">
              <ion-icon name="logo-discord"></ion-icon>
            </span>
            <span class="checkbox-label">Discord</span>
          </span>
        </label>
      </div>
      <div class="checkbox">
        <label class="checkbox-wrapper">
          <input type="checkbox" class="checkbox-input">
          <span class="checkbox-tile">
            <span class="checkbox-icon">
              <ion-icon name="logo-css3"></ion-icon>
            </span>
            <span class="checkbox-label">CSS3</span>
          </span>
        </label>
      </div>
      <div class="checkbox">
        <label class="checkbox-wrapper">
          <input type="checkbox" class="checkbox-input">
          <span class="checkbox-tile">
            <span class="checkbox-icon">
              <ion-icon name="paper-plane"></ion-icon>
            </span>
            <span class="checkbox-label">Telgram</span>
          </span>
        </label>
      </div>
      <div class="checkbox">
        <label class="checkbox-wrapper">
          <input type="checkbox" class="checkbox-input">
          <span class="checkbox-tile">
            <span class="checkbox-icon">
              <ion-icon name="fitness"></ion-icon>
            </span>
            <span class="checkbox-label">Fitness</span>
          </span>
        </label>
      </div>
      <div class="checkbox">
        <label class="checkbox-wrapper">
          <input type="checkbox" class="checkbox-input">
          <span class="checkbox-tile">
            <span class="checkbox-icon">
              <ion-icon name="logo-html5"></ion-icon>
            </span>
            <span class="checkbox-label">HTML5</span>
          </span>
        </label>
      </div>
      <div class="checkbox">
        <label class="checkbox-wrapper">
          <input type="checkbox" class="checkbox-input">
          <span class="checkbox-tile">
            <span class="checkbox-icon">
              <ion-icon name="logo-angular"></ion-icon>
            </span>
            <span class="checkbox-label">Angular</span>
          </span>
        </label>
      </div>
      <div class="checkbox">
        <label class="checkbox-wrapper">
          <input type="checkbox" class="checkbox-input">
          <span class="checkbox-tile">
            <span class="checkbox-icon">
              <ion-icon name="logo-slack"></ion-icon>
            </span>
            <span class="checkbox-label">Slack</span>
          </span>
        </label>
      </div>

    </div>
    <!-- end checkbox-group -->
    <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
    <script nomodule src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js"></script>
    </body>
    </html>

# CSS Program : -
        @import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap");
       :root {
       --primary-color:  #2676ab;
       --dark-color:     #494949;
       --darker-color:   #00000066;
      }
      /* reset */
      *,
      *:after,
      *:before {
      box-sizing: border-box;
      }

    body {
       font-family: "Inter", sans-serif;
       min-height: 100vh;
       display: flex;
       align-items: center;
       background-color: #e1e1e1;
       overflow: hidden;
    }

     .checkbox-group {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        margin: 0 auto;
        max-width: 600px;
    }

     .checkbox-input { display: none; }

     .checkbox-tile {
        display: flex;
        position: relative;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 7rem;
        height: 7rem;
        border-radius: 0.5rem;
        border: 2.5px solid transparent;
        background-color: white;
        box-shadow: 0 5px 10px #00000022;
        transition: 0.25s ease;
        cursor: pointer;
    }

     .checkbox-group > * {
          margin: 0.5rem;
    }

     .checkbox-icon ion-icon {
        font-size: 3rem;
     }
     
      /* checkbox icon */
        .checkbox-tile::before {
         content: "";
         position: absolute;
         width: 1.25rem;
         height: 1.25rem;
         border: 3px solid var(--darker-color);
         border-radius: 50%;
         top: 0.25rem;
         left: 00.25rem;
         transition: 0.25s ease;
         background-image: url("check.png");
         background-size: 35px;
         background-position: 50%;
         transform: scale(0);
    }

     .checkbox-tile:hover::before {
         transform: scale(1);
    }

     .checkbox-tile:hover {
          border-color: var(--darker-color);
    }

      .checkbox-icon {
          transition: 0.5s ease;
          color: var(--dark-color);
    }

     .checkbox-label {
         color: var(--dark-color);
         transition: 0.4s ease;
         font-weight: 500;
    }

    /* checked */
      .checkbox-input:checked + .checkbox-tile {
         border-color: var(--primary-color);
    } 

     .checkbox-input:checked + .checkbox-tile::before {
         border-color: var(--primary-color);
         background-color: var(--primary-color);
         transform: scale(1);
     } 

       .checkbox-input:checked + .checkbox-tile .checkbox-icon,
       .checkbox-input:checked + .checkbox-tile .checkbox-label {
       color: var(--primary-color);
     }
