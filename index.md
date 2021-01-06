<div class="row">
  <div class="column left" style="background-color:#white;">
    <h1>Welcome to <b>Introduction to Russian</b></h1>
    <h2>This website offers a light introduction to the Russian language.</h2> 
    <p>Including:</p>
  <ol>
  <li>The Russian alphabet.</li>
  <li>Basic grammar.</li>
  <li>Fun interactive activities to introduce vocabulary.</li>
</ol>
  </div>
  <div class="column right" style="background-color:#b7cad9;">
    <h2>Learn a new word!</h2>

<button onclick="loadWord()">Click to see another word</button>
<p>&nbsp;</p>
<p id="word"></p>

<script>
var words = [ 
'часы', 
'дом', 
'неделя',    
'книга',
'стол',
'лампа',
'карандаш',
'окно',
'стул',
'улица',
'мужчина',
'женщина',
'мальчик',
'девочка'
];

var examples = [
'<i>clock</i>', 
'<i>house</i>', 
'<i>week</i>',
'<i>book</i>',
'<i>table</i>',
'<i>lamp</i>',
'<i>pencil</i>',
'<i>window</i>',
'<i>chair</i>',
'<i>street</i>',
'<i>man</i>',
'<i>woman</i>',
'<i>boy</i>',
'<i>girl</i>'
];

var wordNo;
var meaningNo;
function loadWord() {
    meaningNo = Math.floor(Math.random() * (words.length));
    if(meaningNo !== wordNo) {
    	document.getElementById("word").innerHTML = "<dt>" + words[meaningNo] + "</dt>" + "<dd>" + examples[meaningNo] + "</dd>";
   	wordNo = meaningNo;
    	return wordNo;
    	}
    	else {
    	loadWord();
    	}
	}
loadWord();
</script>
  </div>
</div>
 



<hr>
<div class="row">
  <div class="col-md-4">
    <div class="thumbnail">
    <img src="images/moscow1.jpg" alt="The Red Square in Moscow" style="height:100%">
        <div class="caption">
		<p style="text-align:center;"><a href="https://commons.wikimedia.org/wiki/File:Moscow_-_Red_Square.jpg">"Red Square, Moscow, Russia"</a>, by <a href="https://commons.wikimedia.org/wiki/User:Rex/Photos">Bart Slingerland</a> licensed under <a href="https://creativecommons.org/licenses/by-sa/3.0/">CC BY-SA 3.0</a>.<br></p>
		<p>&nbsp;</p>
		<p>The Red Square in Moscow. It is home to the Kremlin, GUM department store, the State History Museum, Lenin's Mausoleum, and of course, St Basil’s Cathedral. All the major streets of Moscow radiate from here. Red Square is the central square of Moscow and the symbolic center of all Russia. </p>
        </div>
    </div>
  </div>
  <div class="col-md-4">
    <div class="thumbnail">
        <img src="images/rusflag2.jpg" alt="The Russian flag" style="height:100%">
        <div class="caption">
		<p style="text-align:center;"><a href="https://commons.wikimedia.org/wiki/File:Russia_Flag.svg">"Flag of Russia"</a>, by <a href="https://commons.wikimedia.org/w/index.php?title=Special:Search&search=Professorsolo2015&ns0=1&ns6=1&ns12=1&ns14=1&ns100=1&ns106=1">Professorsolo2015</a> licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0/">CC BY-SA 4.0</a>.<br></p>
		<p>&nbsp;</p>
          <p>The Russian flag.</p>
           <p>&nbsp;</p>
           <p>&nbsp;</p>
        </div>
    </div>
  </div>
   <div class="col-md-4">
    <div class="thumbnail">
        <img src="images/stp (1).jpg" alt="The Winter Palace in Saint Petersburg" style="height:100%">
        <div class="caption">
		<p style="text-align:center;">by <a href="https://pixabay.com/users/al-grishin-7086105/">Alexander Grishin</a> licensed under <a href="https://creativecommons.org/publicdomain/zero/1.0/deed.en">CC0</a>.<br></p>
		<p>&nbsp;</p>
          <p>The Winter Palace in St. Petersburg. It was the official residence of the Russian Emperors from 1732 to 1917. Today, the palace and its precincts form the Hermitage Museum.</p>
          <p>&nbsp;</p>
        </div>
      </div>
  </div>
</div>
