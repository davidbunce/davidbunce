---
layout: page
title: What I'm reading
---
A list of books that I have read or re-read in the last few years. Books are listed in reverse chronological order. Inspired by [Chuck Grimmet](https://cagrimmett.com/reading/), who also provided some of the code on his Github page. I only list books that I am reading for work or pleasure (i.e. most academic books and commentaries I read for sermon preparation don't appear here). Books I particularly enjoyed for one reason or another are marked with a star (<span class="star">★</span>).


<div class="last-update">Last updated {{ site.data.reading.lastupdate }}</div>
  {% for entry in site.data.reading.list %}
  <div class="year-container">
    <div class="year">
      <h2>{{ entry.year }}</h2>
      <div class="number">{{ entry.books | size }} books</div>
    </div>
    <div class="books">
      <ul class="reading-list {{ entry.year }}">
        {% for book in entry.books %}
        <li>
          <a href="{{ book.link }}" alt="_blank" rel="nofollow noopener">{{
            book.title
          }}</a>
          <span class="author">by {{ book.author }}</span
          >{% if book.star %}<span class="star">★</span>{% endif %}
        </li>
        {% endfor %}
      </ul>
    </div>
  </div>
  {% endfor %}