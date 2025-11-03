
layout: default
title: 搜索
permalink: /search/


<!-- HTML elements for search -->
<input
  type="text"
  id="search-input"
  placeholder="搜索：标题、标签、时间、摘要"
  style="
    transition: box-shadow .4s ease,background .4s ease,-webkit-box-shadow .4s ease;
    display: inline-block;
    margin: 0 12px 12px 0;
    background: #f5f5f500;
    border: 1px solid rgba(0, 0, 0, 0.15);
    border-radius: 6px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
    transition: all 0.23s ease-in-out 0s;
    line-height: 1.7;
    color: #202020;
    max-width: 100%;
    margin-bottom: 15px;
    padding: 0.5rem 0.75rem;
    font-size: 1rem;
    line-height: 1.7;
    width: 325px;
    "
/>

<ul id="results-container"></ul>

<!-- script pointing to jekyll-search.js -->

<script src="https://unpkg.com/simple-jekyll-search@1.10.0/dest/simple-jekyll-search.min.js"></script>

<script>
  SimpleJekyllSearch({
    searchInput: document.getElementById("search-input"),
    resultsContainer: document.getElementById("results-container"),
    json: "/search.json",
    searchResultTemplate: '<li><a href="{url}" title="{desc}">{title}</a></li>',
    noResultsText: "没有搜索到文章",
    limit: 20,
    fuzzy: false,
  });
</script>
