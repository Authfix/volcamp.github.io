---
layout: default
title: Volcamp.io - Les intervenants
---
<section class="page-header" style="background-image:url(https://www.volcamp.io/asset/images/chainedespuys_header.jpg);">
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-lg-8">
                <div class="content text-center">
                    <h1 class="mb-3 text-white text-capitalize letter-spacing">Nos intervenants</h1>
                    <div class="divider mx-auto mb-4 bg-white"></div>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="section-speaker section">
    <div class="container">
        <div class="row section-heading">
            <div class="col-lg-8">
                <div class="heading">
                    <div class="pl-90">
                        <h2>Les speakers</h2>
                    </div>
                </div>
            </div>
        </div>
        <div class="row">
            {% assign speakers = site.speakers | sort_natural: 'name' %}
            {% for speaker in speakers %}
            <div class="col-lg-4 col-sm-6">
                <div class="speaker-block mb-5">
                    <div class="img-block"><img src="{{ site.baseurl }}/asset/images/speakers/{{ speaker.photo }}" alt="{{ speaker.name }}" class="img-fluid">
                        <ul class="list-inline speaker-social">
                            <li class="list-inline-item"><a href="/speakers/{{ speaker.url }}"><i class="icon-mic"></i></a></li>
                            <li class="list-inline-item"><a href="https://twitter.com/{{ speaker.twitter }}"><i class="icon-twitter"></i></a></li>
                            <li class="list-inline-item"><a href="https://www.linkedin.com/in/{{ speaker.linkedin }}"><i class="icon-linkedin-squared"></i></a></li>
                        </ul>
                    </div>
                    <div class="speaker-info">
                        <h4 class="mb-0 mt-3">{{ speaker.name }}</h4>
                        <p>{{ speaker.abstract }}</p>
                    </div>
                </div>
            </div>
            {% else %}
                Rien à voir ici.
            {% endfor %}
        </div>
    </div>
</section>