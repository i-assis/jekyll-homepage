---
layout: page
title: 🔍
permalink: /search/
---

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
</head>
<body>

<!-- Search input field -->
  <div class="main-search form-group mb-0 border-bottom">
  <div class="input-group">
    <input id="search" name="main_input" class="form-control border-0" placeholder="search in posts..." type="text">
    <div class="input-group-append">
      <span class="input-group-text border-0"><i class="fa fa-search" aria-hidden="true"></i></span>
    </div>
  </div>
</div>

<!-- Search result container -->
<div class="search-results position-absolute">
      <ul id="results" class="search-results-ul card shadow border border-top-0">
      </ul>
</div>

<!-- Script pointing to Jekyll Instant Search js -->
<script src="/assets/js/search-script.js" type="text/javascript"></script>

<!-- Jekyll Instant Search Configuration -->
<script>
SimpleJekyllSearch({
  searchInput: document.getElementById('search'),
  resultsContainer: document.getElementById('results'),
  searchResultTemplate: '<li> <a href="{url}" tabindex="1"> <p>{title}</p> <p>{url}</p> </a> </li>',
  noResultsText: '<li><p>No results found!</p></li>',
  json: '/search.json'
})
</script>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>

<!-- show site search results -->
<script>
  $(document).ready(function() {
    $('#search').on('blur', function() {
    $('.search-results').fadeOut('medium');
});
  $('#search').on('focus', function() {
      $('.search-results').show();
  });

    });
  </script>

</body>
</html>
