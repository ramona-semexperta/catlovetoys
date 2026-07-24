---
layout: default
title: Home
---

<section class="hero">
  <h1>Play, Pounce, Purr! 🐾</h1>
  <p class="hero-sub">Honest cat toy reviews, comparisons, and real stories — inspired by Alfi, the tabby who ran this whole household.</p>
</section>

<section class="home-grid">
  <div class="home-card">
    <h2>📝 Latest from the Blog</h2>
    <ul class="post-list">
      {% for post in site.posts limit:5 %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
      </li>
      {% endfor %}
    </ul>
    <a class="button" href="{{ '/blog/' | relative_url }}">See all posts →</a>
  </div>

  <div class="home-card">
    <h2>🧸 Toy Comparisons</h2>
    <p>Coming soon: side-by-side comparisons of interactive toys, teasers, balls, catnip toys, and scratchers — built from real testing, not guesswork.</p>
    <a class="button" href="{{ '/toys/' | relative_url }}">Browse toy categories →</a>
  </div>

  <div class="home-card">
    <h2>🐈 Meet Alfi</h2>
    <p>Every good cat brand needs a real cat behind it. Get to know the tabby who inspired all of this.</p>
    <a class="button" href="{{ '/about/' | relative_url }}">Read her story →</a>
  </div>
</section>
