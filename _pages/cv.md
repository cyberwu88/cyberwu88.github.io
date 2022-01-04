---
layout: page
permalink: /cv/
title: CV
nav: cv
---

<!-- Place PDF download link at the top right. -->
<div class="row" style="margin-top: -3.5em;">
	<a class="ml-auto mr-2" href="/assets/pdf/vitae.pdf" target="_blank">
	  <img height="60px" src="/assets/img/pdf_icon.svg">
	</a>
</div>

General Information
Full Name:
Contact: 
Languages: English(Native), Cantonese(Fluent)

Research Areas
My research focuses

<div class="news">
            <h2>News</h2>
            {% if site.news  -%} 
            <div class="table-responsive">
              <table class="table table-sm table-borderless">
              {%- assign news = site.news | reverse -%} 
              {% for item in news limit: site.news_limit %} 
                <tr>
                  <th scope="row">{{ item.date | date: "%b %-d, %Y" }}</th>
                  <td>
                    {% if item.inline -%} 
                      {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
                    {%- else -%} 
                      <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
                    {%- endif %} 
                  </td>
                </tr>
              {%- endfor %} 
              </table>
            </div>
          {%- else -%} 
            <p>No news so far...</p>
          {%- endif %} 
          </div>
