---
layout: page
title: Home
id: home
permalink: /
---

# mindmate 질문 리스트 공유 공간!

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  💡아래 요소들 클릭을 통해 최근의 질문들을 확인해보세요!
</p>

<strong>Recently updated notes</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  <link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard/dist/web/static/pretendard.css" />
  .wrapper {
    max-width: 46em;
  }
</style>
