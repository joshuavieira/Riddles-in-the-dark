<html>
<head>
  <title>Joshua and Ismael - Riddles in the Dark</title>

  <style type="text/css">
    body { text-align: center; }
    div { display: none; }
  </style>

  <script type="text/javascript">

    function changePage(curr, next) {
      var next, currPage, nextPage;

      currPage = document.getElementById(curr);
      nextPage = document.getElementById(next);
      
      currPage.style.display = 'none';
      nextPage.style.display = 'block';
    }

    function start() {
      document.getElementById('start').style.display = 'block';
    }

    var character; // holds the player's character name (or character object if you get that far)

    function chooseCharacter ( name ) {
        // set the character name
        character = name;
        
        // go to the fork in the road page
        changePage('characterChooser', 'forkInTheRoad');
    }
    
  </script>

</head>
<body onload="start();">

  <h1>Riddles In The Dark</h1>
  <h2> Deceptico is on the loose! You must stop him! </h2>

  <div id="start">
    <img src="http://thetortoiseruns.files.wordpress.com/2012/02/haunted_forest__by_dadoundy-d3ba6fo.jpg" alt="scary forset">
    <button onclick="changePage('start', 'characterChooser');">Game Start</button>
  </div>

  <div id="characterChooser">
    <h2>Choose a Character</h2>
    <!-- <img src="locationOfPictureOfIke" onclick="changePage('characterChooser', 'nameoffirstpage');"> -->
    <button onclick="chooseCharacter('Ike');"> Ike </button>
    <button onclick="chooseCharacter('Zelda');"> Aida </button>
    <button onclick="chooseCharacter('Hobbeo');"> Hobbeo </button>
  </div>

  <div id="forkInTheRoad">
    <h2> Choose the place you want to go </h2>
    <button onclick="changePage('characterChooser', 'forestscreen');"> Forest </button>
    <button onclick="changePage('characterChooser', 'cavescreen');"> Cave </button>
    <button onclick="changePage('characterChooser', 'lairscreen');"> Evil Person's Lair </button>
  </div>
  </body>
  </html>
  
  <div id="forestscreen">
   <h2> Forest </h2>
    <p> You enter a dark forest.</p>
    <p> There are many trees that extend skyward. One of the trees has something shining near it. </p>
    <p> There is a pile of leaves on the ground. Next to them, you see a few bushes. </p>
    <button onclick="changePage('forestscreen', 'chestriddle');"> Check Tree </button>
    <button onclick="changePage('forestscreen', 'leaveshint');"> Check Leaves </button>
    <button onclick="changePage('forestscreen', 'bushtrap');"> Check Bushes </button>
  </div>
  
  <div id="chestriddle">
   <h2> A Chest! </h2>
   <p> You found a marvelous, glowing chest! There is no keyhole. </p>
   <p> Instead, you see a small inscription on top of the chest. It reads: </p>
   <p> I have two arms, a face, and even a long body. But I cannot talk, nor can I move. What am I? </p>
    <button onclick="changePage('chestriddle', 'chestwrong');"> A mime </button>
    <button onclick="changePage('chestriddle', 'chestright');"> A clock </button>
    <button onclick="changePage('chestriddle', 'chestwrong');"> Err... I don't know </button>
   </div>
    
   <div id= "leaveshint">
   <h2> A Paper? </h2>
   <p> You found a mysterious envelope... </p>
   <p> Inside is a paper that reads: </p>
   <p> "Do not think about it literally. Think about how many 2nd's." </p>
   <button onclick="changePage('leaveshint', 'forestscreen');"> Back to Forest </button>
   </div>
   
   <div id= "bushtrap">
   <h2> AAAGH! </h2>
   <p> OUCH! You got your nose bitten by a squirrel! </p>
   <p> In a fit of agonizing pain, you ran back to the fork in the road! </p>
   <button onclick="changePage('bushtrap', 'forkInTheRoad');"> Umm... Ok? </button>
   </div>
   
   <div id="chestright">
   <h2> It opened! </h2>
   <p> Congratulations! Upon opening the chest, you found a piece of paper with a small inscription... </p>
   <p> It reads: Power to enter cave. Teleporting to cave in 3...2...1... </p>
   <button onclick="changePage('chestright', 'caveriddle1');"> Wait, Wha- </button>
   </div>
   
   <div id="chestwrong">
   <h2> Darn... </h2>
   <p> The chest refuses to open... </p>
    <button onclick="changePage('chestwrong', 'chestriddle');"> Try Again </button>
   </div>
    
    <div id="cavescreen">
    <h2> Huh? </h2>
    <p> There is a gate blocking the entrance to the cave... </p>
    <p> In front of the cave is a sign that reads: </p>
    <p> Brave ye the forest of mystery. </p>
     <button onclick="changePage('cavescreen', 'forkInTheRoad');"> Go Back </button>
     </div>
     
    <div id="caveriddle1">
    <h1> Uh Oh... </h1>
    <h2> What's that noise? </h2>
    <p> You teleported right into a room within the cave. </p>
    <p> As you scan your surroundings, you hear a distant tapping noise... </p>
    <p> Suddenly, the noise gets closer and closer, until the source reveals itself... </p>
    <p> IT'S A GIANT SPIDER! DO SOMETHING! </p>
    <p> You unsheath your magic sword, ready to face the beast. But... </p>
    <p> The sword cannot cut unless you answer a question first, here it is: </p>
    <p> "WHAT IS THE SPANISH WORD FOR BEWARE?" </p>
     <button onclick="changePage('caveriddle1', 'cavewrong');"> Uno </button>
     <button onclick="changePage('caveriddle1', 'cavewrong');"> Bravo </button>
     <button onclick="changePage('caveriddle1', 'cavewrong');"> Cueva </button>
     <button onclick="changePage('caveriddle1', 'caveright');"> Cuidado </button>
     </div>
     
    <div id="lairscreen">
    <h2> Strange... </h2>
    <p> There is a mysterious force blocking the way to the lair. </p>
    <p> Looking around, you notice that there is a cave nearby that leads straight to the lair. </p>
    <p> Perhaps there is a way within the cave? </p>
     <button onclick="changePage('lairscreen', 'forkInTheRoad');"> Go Back </button>
    </div>
    
    <div id="cavewrong">
    <h1> Wrong... </h1>
    <h2> Death by Spider </h2>
    <p> The sword did not sharpen. Before you could try again, the spider bit your head off. </p>
    <p> Try again! </p>
      <button onclick="changePage('cavewrong', 'forkInTheRoad');"> Put me back in, coach! </button>
    </div>
    
    <div id="caveright">
    <h2> Eureka! </h2>
    <p> The sword shapened! </p>
    <p> In quick succession, you face the spider and slice it clean in half! </p>
    <p> Behind the spider, there is a door leading to a new section. </p>
    <p> Excellent work! </p>
     <button onclick="changePage('caveright', 'bunny');"> That was easy </button>
    </div>
    
    <div id="bunny">
    <h1> D'awww </h1>
    <h2> It's so cuuuute~ </h2>
    <p> Upon entering the next room, you encounter something totally unexpected. </p>
    <p> In the middle of the room you see a small, fluffy bunny! </p>
    <p> AAAAWWW, don't you just wanna hug and squeeze it?! </p>
     <button onclick="changePage('bunny', 'caveriddle2');"> Hug it </button>
     <button onclick="changePage('bunny', 'caveriddle2');"> Squeeze it </button>
    </div>
    
    <div id="caveriddle2">
    <h1> HUH?! </h1>
    <h2> WHAT IN THE WORLD?! </h2>
    <p> Before you could even get close to the bunny...You hear it make a growling noise... </p>
    <p> Suddenly, the bunny transforms into a GIGANTIC DRAGON!! DO SOMETHING!! </p>
    <p> The sword is dull once again, answer this riddle correctly to sharpen it! </p>
    <p> "I HAVE AN OVAL SHAPE. IN THE AIR I AM WHITE, BUT WHEN I LAND I TURN YELLOW AND LOSE MY OVAL SHAPE" </p>
    <p> You are... </p>
     <button onclick="changePage('caveriddle2', 'cave2wrong');"> A beach ball</button>
     <button onclick="changePage('caveriddle2', 'cave2right');"> An egg </button>
     <button onclick="changePage('caveriddle2', 'cave2wrong');"> A marble </button>
     <button onclick="changePage('caveriddle2', 'cave2wrong');"> WOW! A DRAGON! </button>
    </div>
    
    <div id="cave2wrong">
    <h1> Wrong... <h1>
    <h2> Death by Dragon <h2>
    <p> The sword did not sharpen. </p>
    <p> Before you can try again, the dragon burns you to a fine, golden crisp. </p>
    <p> Try again! </p>
     <button onclick="changePage('cave2wrong', 'forkInTheRoad');"> Do I have to? </button>
    </div>
    
    <div id="cave2right">
    <h2> HAVE AT THEE, FELL BEAST </h2>
    <p> The sword sharpened! You launch yourself in the air and slice the dragon's head off! </p>
    <p> The dragon is slain! </p>
    <p> Still... You can't help but feel sad for that poor bunny... oh well. </p>
    <p> You continue to the end of the cave. </p>
    <button onclick="changePage('cave2right', 'castle1');"> Exit Cave </button>
    </div>
    
    <div id="castle1">
    <h1> Welcome to Deceptico's castle </h1>
    <p> You have finally reached Deceptico's lair. </p>
    <p> In the center of the foyer, you see a spiral staircase that stretches for miles and miles. </p>
    <p> It no doubt leads to deceptico's lair. </p>
    <p> The foyer also has a large rug spread across the floor. </p>
    <button onclick="changePage('castle1', 'finalriddle');"> Bring him on! </button>
    <button onclick="changePage('castle1', 'castle2');"> Examine rug </button>
    </div>
    
    <div id="castle2">
    <h2> Interesting... </h2>
    <p> Upon closer inspeccion of the rug, you notice something rather peculiar. </p>
    <p> There is a slightly faded inscription on it that reads "Remember the Forest" </p>
    <p> What could it mean? </p>
    <button onclick="changePage('castle2', 'castle1');"> OK </button>
    </div>
    
    <div id="finalriddle">
    <h1> "MUHAHAHAHAHA!!" </h1>
    <h2> "So... You've made it..." </h2>
    <p> After the long flight of stairs, you have finally reached Deceptico's chambers! </p>
    <p> Upon entering, he surrounds you with mobile suits of armor each carrying rail guns and proton cannons! </p>
    <p> "Well then...Any last words?" said Deceptico. </p>
    <p> Calling to the power of your sword once more, the final riddle emerges! </p>
    <p> This one will mean life or death! Do or die! Here it is: </p>
    <p> "HOW MANY SECONDS ARE IN A YEAR?" </p>
    <p> You courageously raise your sword to the heavens and shout: </p>
    <button onclick="changePage('finalriddle', 'finalwrong');"> 31,536,000 </button>
    <button onclick="changePage('finalriddle', 'finalwrong');"> 365 </button>
    <button onclick="changePage('finalriddle', 'finalwrong');"> 87,978,122 </button>
    <button onclick="changePage('finalriddle', 'ending');"> 12 </button>
    <button onclick="changePage('finalriddle', 'finalwrong');"> WHO PUT MATH IN MY SWORD?! </button>
    </div>
    
    <div id="finalwrong">
    <h1> Your voice echoes in the room... </h1>
    <h2> Aaaaaaannnd... </h2>
    <p> ...Ummm.... </p>
    <p> Your sword did not sharpen. </p>
    <p> Deceptico chuckles as he flies into the sky and gives a signal to his armor suits </p>
    <p> As he flies away, Deceptico's castle explodes with you in it. </p>
    <p> Deceptico is now free to conquer the Earth without interruptions... </p>
    <p> Game Over </p>
    <button onclick="changePage('finalwrong', 'forkInTheRoad');"> What kind of ending is that?! Try Again </button>
    </div>
    
    <div id="ending">
    <h1> Your voice echoes in the room... </h1>
    <h2> Aaaaaaannnd... </h2>
    <p> ...SUCCESS!! </p>
    <p> YOUR SWORD SHARPENS!! </p>
    <p> In one quick succession, you spin with your sword outstretched, causing a mighty wind that blows away all the suits! </p>
    <p> Deceptico crashes against a nearby pillar. </p>
    <p> "I don't understand, how does that make sense?" ponders Deceptico. </p>
    <p> He thinks for a moment...then slaps his forehead and says "OOOH! Twelve 2nds!! January 2nd, Feburary 2nd!" </p>
    <p> He loses his temper and accidentally runs into another pillar, causing him to become unconscious. </p>
    <p> You drag him all the way back to the cave and leave him in a dungeon that was near the dragon's den. </p>
    <p> CONGRATULATIONS!! YOU'VE SAVED THE WORLD!!! </p>
    <button onclick="changePage('ending', 'forkInTheRoad');"> Cool! Let's do that again! </button>
    </div>
