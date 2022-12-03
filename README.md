# Booking-Management-System
A Project to make the Bookig  Management System
[dango-1.pdf](https://github.com/HarshSrivastava12215211/Booking-Management-System/files/10146907/dango-1.pdf)
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    
        
    <title>Movie Design</title>
    <style>
        * {
            margin: 0;
          }
          
          body {
            font-family: "Roboto", sans-serif;
          }
          
          .navbar {
            width: 100%;
            height: 50px;
            background-color: black;
            position: sticky;
            top: 0;
          }
          
          .navbar-container {
            display: flex;
            align-items: center;
            padding: 0 10px;
            height: 100%;
            color: white;
            font-family: "Sen", sans-serif;
          }
          
          .logo-container {
            flex: 1;
          }
          
          .logo {
            font-size: 20px;
            color: #4dbf00;
          }
          
          .menu-container {
            flex: 6;
          }
          
          .menu-list {
            display: flex;
            list-style: none;
          }
          
          .menu-list-item {
            margin-right: 30px;
          }
          
          .menu-list-item.active {
            font-weight: bold;
          }
          .profile-container {
            flex: 2;
            display: flex;
            align-items: center;
            justify-content: flex-end;
          }
          
          .profile-text-container {
            margin: 0 20px;
          }
          
          .profile-picture {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            object-fit: cover;
          }
          
          .toggle {
            width: 40px;
            height: 20px;
            background-color: white;
            border-radius: 30px;
            display: flex;
            align-items: center;
            justify-content: space-around;
            position: relative;
          }
          
          .toggle-icon {
            color: goldenrod;
          }
          
          .toggle-ball {
            width: 18px;
            height: 18px;
            background-color: black;
            position: absolute;
            right: 1px;
            border-radius: 50%;
            cursor: pointer;
            transition: 1s ease all;
          }
          
        
          
          .left-menu-icon {
            color: white;
            font-size: 20px;
            margin-bottom: 40px;
          }
          
          .container {
            background-color: #151515;
            min-height: calc(100vh - 50px);
            color: white;
          }
          
          .content-container {
            margin-left: 0px;
          }
          
          .featured-content {
            height: 50vh;
            padding: 50px;
          }
          
          .featured-title {
            width: 200px;
          }
          
          .featured-desc {
            width: 500px;
            color: lightgray;
            margin: 30px 0;
          }
          
          .featured-button {
            background-color: #4dbf00;
            color: white;
            padding: 10px 20px;
            border-radius: 10px;
            border: none;
            outline: none;
            font-weight: bold;
          }
          
          .movie-list-container {
            padding: 0 20px;
          }
          
          .movie-list-wrapper {
            position: relative;
            overflow: hidden;
          }
          
          .movie-list {
            display: flex;
            align-items: center;
            height: 300px;
            transform: translateX(0);
            transition: all 1s ease-in-out;
          }
          
          .movie-list-item {
            margin-right: 30px;
            position: relative;
          }
          
          .movie-list-item:hover .movie-list-item-img {
            transform: scale(1.2);
            margin: 0 30px;
            opacity: 0.5;
          }
          
          .movie-list-item:hover .movie-list-item-title,
          .movie-list-item:hover .movie-list-item-desc,
          .movie-list-item:hover .movie-list-item-button {
            opacity: 1;
          }
          
          .movie-list-item-img {
            transition: all 1s ease-in-out;
            width: 270px;
            height: 200px;
            object-fit: cover;
            border-radius: 20px;
          }
          
          .movie-list-item-title {
            background-color: #333;
            padding: 0 10px;
            font-size: 32px;
            font-weight: bold;
            position: absolute;
            top: 10%;
            left: 50px;
            opacity: 0;
            transition: 1s all ease-in-out;
          }
          
          .movie-list-item-desc {
            background-color: #333;
            padding: 10px;
            font-size: 14px;
            position: absolute;
            top: 30%;
            left: 50px;
            width: 230px;
            opacity: 0;
            transition: 1s all ease-in-out;
          }
          
          .movie-list-item-button {
            padding: 10px;
            background-color: #4dbf00;
            color: white;
            border-radius: 10px;
            outline: none;
            border: none;
            cursor: pointer;
            position: absolute;
            bottom: 20px;
            left: 50px;
            opacity: 0;
            transition: 1s all ease-in-out;
          }
          
          .arrow {
            font-size: 120px;
            position: absolute;
            top: 90px;
            right: 0;
            color: lightgray;
            opacity: 0.5;
            cursor: auto;
          }
          
          .container.active {
            background-color: white;
          }
          
          .movie-list-title.active {
            color: black;
          }
          
          .navbar-container.active {
            background-color: white;
          
            color: black;
          }
          
          
          
          
          .left-menu-icon.active{
              color: black;
          }
          
          .toggle.active{
              background-color: black;
          }
          
          .toggle-ball.active{
              background-color: white;
              transform: translateX(-20px);
          }
          
          @media only screen and (max-width: 940px){
              .menu-container{
                  display: none;
              }
          }
          Footer
          
    </style>
</head>

<body>
    
    <div class="navbar">
        <div class="navbar-container">
            <div class="logo-container">
                <h1 class="logo">Book my show</h1>
            </div>
            <div class="menu-container">
                <ul class="menu-list">
                    <li class="menu-list-item active">Home</li>
                    <li class="menu-list-item">Movies</li>
                    <li class="menu-list-item">Series</li>
                    <li class="menu-list-item">Popular</li>
                    <li class="menu-list-item">Trends</li>

                </ul>
            </div>
            <div class="profile-container">
                <img class="profile-picture" src="profile.jpg" alt="">
                <div class="profile-text-container">
                    <span class="profile-text">Profile</span>
                    <i class="fas fa-caret-down"></i>
                </div>
               
            </div>
        </div>
    </div>
    
    </div>
    <div class="container">
        <div class="content-container">
            <div class="featured-content"
                style="background: linear-gradient(to bottom, rgba(0,0,0,0), #151515), url(f-t-1.png);">
                <img class="featured-title" src="" alt=""><br><br><br><br><br<br><br><br<br><br><br<br><br><br<br><br><br<br><br><br<br><br>
                <h1>Dark</h1>
                <p class="featured-desc"> A missing child sets four families on a frantic hunt for answers as they unearth a mind bending mystery that spans three generations.</p>
                <button class="featured-button">BOOK TICKETS</button>
            </div>
            <div class="movie-list-container">
                <h1 class="movie-list-title">NEW RELEASES</h1>
                <div class="movie-list-wrapper">
                    <div class="movie-list">
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="har.png" alt="">
                            <span class="movie-list-item-title">Her</span>
                            <p class="movie-list-item-desc">Theodore Twombly, an introverted writer, buys an Artificial Intelligence system to help him write. However, when he finds out about the AI's ability to learn and adapt, he falls in love with it.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="starwaes.png" alt="">
                            <span class="movie-list-item-title">Star Wars</span>
                            <p class="movie-list-item-desc">Star Wars is an American epic space opera multimedia franchise created by George Lucas, which began with the eponymous 1977 film and quickly became a worldwide pop-culture phenomenon.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="storm.png" alt="">
                            <span class="movie-list-item-title">Storm</span>
                            <p class="movie-list-item-desc">After learning about some major developing storms, Pete, a storm chaser, heads to Silverton to film tornadoes. Soon, he discovers that a tornado shifts course and heads towards a high school.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="img5.png" alt="">
                            <span class="movie-list-item-title">1917</span>
                            <p class="movie-list-item-desc">Two soldiers, assigned the task of delivering a critical message to another battalion, risk their lives for the job in order to prevent them from stepping right into a deadly ambush.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="Avengers.png" alt="">
                            <span class="movie-list-item-title">Avengers-Age Of Ultron</span>
                            <p class="movie-list-item-desc">Tony Stark builds an artificial intelligence system named Ultron with the help of Bruce Banner. When the sentient Ultron makes plans to wipe out the human race, the Avengers set out to stop him.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="img/6.jpg" alt="">
                            <span class="movie-list-item-title">Her</span>
                            <p class="movie-list-item-desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. At
                                hic fugit similique accusantium.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="img/7.jpg" alt="">
                            <span class="movie-list-item-title">Her</span>
                            <p class="movie-list-item-desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. At
                                hic fugit similique accusantium.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                    </div>
                    <i class="fas fa-chevron-right arrow"></i>
                </div>
            </div>
            <div class="movie-list-container">
                <h1 class="movie-list-title">MONTHS MOST LIKED</h1>
                <div class="movie-list-wrapper">
                    <div class="movie-list">
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="oblivion.png" alt="">
                            <span class="movie-list-item-title">oblivion</span>
                            <p class="movie-list-item-desc">Jack Harper, a drone repairman stationed on Earth that has been ravaged by war with extraterrestrials, questions his identity after rescuing the woman who keeps appearing in his dreams.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="hobbit.png" alt="">
                            <span class="movie-list-item-title">Hobbit</span>
                            <p class="movie-list-item-desc">The Hobbit is a series of three epic high fantasy adventure films directed by Peter Jackson. The films are subtitled An Unexpected Journey, The Desolation of Smaug, and The Battle of the Five Armies.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="due date.png" alt="">
                            <span class="movie-list-item-title">Due Date</span>
                            <p class="movie-list-item-desc">Peter Highman must reach Los Angeles to make it in time for his child's birth. However, he is forced to travel with Ethan, an aspiring actor, who frequently lands him in trouble.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="kickass.png" alt="">
                            <span class="movie-list-item-title">KickAss</span>
                            <p class="movie-list-item-desc">Comic book geek Dave sets out to become Kick-Ass, a real-life superhero. Big Daddy and Hit-Girl attempt to dismantle the underworld empire of mob boss Frank D'Amico, when Kick-Ass gets involved.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="emoji movie.png" alt="">
                            <span class="movie-list-item-title">Emozi Movie</span>
                            <p class="movie-list-item-desc">Gene, a multi-expression emoji, gets sentenced to be deleted after he messes up a message his user Alex sends to his crush. Gene escapes the agents sent to destroy him and accepts his uniqueness.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="img/1.jpg" alt="">
                            <span class="movie-list-item-title">Her</span>
                            <p class="movie-list-item-desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. At
                                hic fugit similique accusantium.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="img/1.jpg" alt="">
                            <span class="movie-list-item-title">Her</span>
                            <p class="movie-list-item-desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. At
                                hic fugit similique accusantium.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                    </div>
                    <i class="fas fa-chevron-right arrow"></i>
                </div>
            </div>
            <div class="featured-content"
                style="background: linear-gradient(to bottom, rgba(0,0,0,0), #151515), url(ft1.png);">
                <br><br><br><br><br><br>
                <img class="featured-title" src="Untitled.png" width="56px">
                <p class="featured-desc">Sergio Corbucci's Grand Guignol spaghetti western is set on the USA-Mexican border just after the Civil War. Django, an ex-Union soldier, wreaks bloody vengeance on the Ku Klux Klan.</p>
                <button class="featured-button">BOOK TICKETS</button>
            </div>
            <div class="movie-list-container">
                <h1 class="movie-list-title">OLD GOLD</h1>
                <div class="movie-list-wrapper">
                    <div class="movie-list">
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="im19.png" alt="">
                            <span class="movie-list-item-title">Dragon Cry</span>
                            <p class="movie-list-item-desc">Natsu and his friends travel to the island kingdom of Stella to recapture the Dragon Cry, a magical artefact with enough power to destroy the world.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="aquaman.png" alt="">
                            <span class="movie-list-item-title">Aquaman</span>
                            <p class="movie-list-item-desc">Half-human, half-Atlantean Arthur is born with the ability to communicate with marine creatures. He goes on a quest to retrieve the legendary Trident of Atlan and protect the water world.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="1920.png" alt="">
                            <span class="movie-list-item-title">1920</span>
                            <p class="movie-list-item-desc">1920 is a series of Indian horror films. The story is written by Vikram Bhatt, for all three films in the series. The first film released in 2008 is directed by Vikram Bhatt, the second film released in 2012 is directed by Bhushan Patel and the third film directed by Tinu Suresh Desai released in 2016.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="1920lond.png" alt="">
                            <span class="movie-list-item-title">1920London</span>
                            <p class="movie-list-item-desc">Shivangi, a princess, is married to Veer who gets possessed by an evil witch. She seeks the help of Jai, an exorcist and her ex-lover, to rid Veer of the dark influence.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="batman.png" alt="">
                            <span class="movie-list-item-title">    Batman</span>
                            <p class="movie-list-item-desc">Batman is a superhero appearing in American comic books published by DC Comics. The character was created by artist Bob Kane and writer Bill Finger, and debuted in the 27th issue of the comic book Detective Comics on March 30, 1939.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="pathogglory.png" alt="">
                            <span class="movie-list-item-title">Path of Glory</span>
                            <p class="movie-list-item-desc">General Mireau decides to take on an impossible mission to capture a German post. However, when his men decide to back out from the mission he insults them.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                        <div class="movie-list-item">
                            <img class="movie-list-item-img" src="img/1.jpg" alt="">
                            <span class="movie-list-item-title">Her</span>
                            <p class="movie-list-item-desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. At
                                hic fugit similique accusantium.</p>
                            <button class="movie-list-item-button">Book Ticket</button>
                        </div>
                    </div>
                    
                </div>
            </div>
            
        </div>
    </div>
</body>

</html>
