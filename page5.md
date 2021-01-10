<h1 align="center">Resources</h1>
<p>&nbsp;</p>
<div class="container-fluid">
<div class="row">
<div id="resources">
  <div class="column">
   <a href="http://masterrussian.com/">
     <div class="card">
      <h3>MasterRussian</h3>
      <p>grammar help</p>
       </div>
      </a>
 </div>

 <div class="column">
      <a href="https://translate.yandex.com/">
    <div class="card">
      <h3>Yandex Translate</h3>
      <p>translation tool</p>
       </div>
       </a>
 </div>
  
   <div class="column">
      <a href="https://ru.euronews.com/">
     <div class="card">
      <h3>Euronews</h3>    
      <p>news in Russian</p>
      </div>
      </a>
 </div>
  
   <div class="column">
<a href="https://www.wordreference.com/">
     <div class="card">
      <h3>WordReference</h3>
      <p>RU⇌EN dictionary</p>
       </div>
	</a>
 </div>
 
 <div class="column">
<a href="https://www.russianbookshop.co.uk/index.php">
     <div class="card">
      <h3>Russian Bookshop</h3>
      <p>Russian language books</p>
       </div>
	</a>
 </div>
</div>
</div>
<hr />
<p>For more fun ways to learn Russian visit <a href="https://www.digitaldialects.com/Russian.htm">Russian language games</a></p>
<hr />
<h4>Search Russian wikipedia</h4>

<header class="searchForm-container">
<img src="https://image.ibb.co/e6vOFQ/wikipedia.png" alt="Wikipedia Logo">
<form class="searchForm">
        <input type="search" class="searchForm-input">
        <button type="submit" class="icon searchIcon">
          <img src="https://image.ibb.co/cpG8zk/search.png" alt="Magnifying Glass Icon">
        </button>
        <a href="" class="icon randomIcon">
          <img src="https://image.ibb.co/fR5OX5/random.png" alt="Shuffle Icon">
        </a>
      </form>
</header>
<section class="searchResults"></section>
  
<script>
  function handleSubmit(event) {
    // prevent page from reloading when form is submitted
  event.preventDefault();
  // get the value of the input field
  const input = document.querySelector('.searchForm-input').value;
  // remove whitespace from the input
  const searchQuery = input.trim();
  // call `fetchResults` and pass it the `searchQuery`
  fetchResults(searchQuery);
}

function fetchResults(searchQuery) {
	  const endpoint = `https://ru.wikipedia.org/w/api.php?action=query&list=search&prop=info&inprop=url&utf8=&format=json&origin=*&srlimit=20&srsearch=${searchQuery}`;
  	fetch(endpoint)
  		.then(response => response.json())
  		.then(data => {
        const results = data.query.search;
  	  	displayResults(results);
		})
       .catch(() => document.querySelector('.searchForm-input').value = 'Please enter a search term.');
       //.catch(() => console.log('An error occured'));
}

function displayResults(results) {
  const searchResults = document.querySelector('.searchResults');
  searchResults.innerHTML = '';
  results.forEach(result => {
  const url = encodeURI(`https://ru.wikipedia.org/wiki/${result.title}`);
  
  searchResults.insertAdjacentHTML('beforeend',
  
  `<div class="resultItem">
  <h3 class="resultItem-title">
  <a href="${url}" target="_blank" rel="noopener">${result.title}</a>
  </h3>
  <span class="resultItem-snippet">${result.snippet}</span><br>
  <a href="${url}" class="resultItem-link" target="_blank" rel="noopener">${url}</a>
  </div>`
  );
  
});

console.log(results);
}
const form = document.querySelector('.searchForm');
form.addEventListener('submit', handleSubmit);
</script>


 </div>

<p>&nbsp;</p>
