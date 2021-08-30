---
layout: default
permalink: /view-from-england/
title: The View from England
---
Apart from the warring history, there were many more reasons why France and the French were such a popular choice for satire. The French were at the opposite end of the scale in terms of politics, values and beliefs: they were Catholic, and their society was run by an effeminate (and many thought, degenerate) court and a despot king, who maintained his authority through violence. The infamous lettres de cachet (the means by which an individual could be sentenced without trial), the Bastille fortress, and implements of torture were all read as symbols of an oppressive regime. There were many people on this side of the Channel who fervently believed that life was just better in England.

William Hogarth is renowned for his enigmatic patriotism and his dislike of anything foreign (although this is itself a stereotype of his character). He is remembered for thinking that much of France was full of despotism, religious zeal, wooden clogs (sabots) and foppery. It is Hogarth who establishes in visual form the stereotype of the poverty-stricken Frenchman which is reused and recycled by the satirists after him. In the first half of the century a generic Frenchman had appeared in numerous plays and literary texts. In John Arbuthnot's The History of John Bull (1712) the Englishman is contrasted against his foreign counterparts Louis Baboon (France, corruption of the king, Louis Bourbon) and Nick Frog (Holland). The French as a whole would not yet be known as frogs until the turn of the century. Rather, a Frenchman was portrayed as a monkey, because of his chattering nature and scrawny physique.

In the 1790s Gillray picks up the simian qualities of the older representations of Frenchmen, but makes them more grotesque and fiendish. The events of the French Revolution were recognised as momentous even at the time, although for the most part news was followed on this side of the Channel with a curiosity born of self interest. From the outset until 1792 there was a marked optimism about the Revolution, although Edmund Burke's Reflections on the Revolution in France of 1790 caused many people to change their minds. After the execution of Louis XVI the stereotype of the Frenchman was no longer a laughing matter. They were no longer portrayed as foppish and generally harmless fools, but as dangerous sans-culottes, appearing in swarms as a grotesque, undifferentiated mass, or becoming diabolical or mad, devoid of humanity and behaving like wild beasts.

<div class="container mb-3">
  <div class="row">
{% assign rows = site.england.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
{% assign offset = forloop.index0 | times: 2 %}
{% assign sorted = site.england | sort:"order" %}
    {% for author in sorted limit:2 offset:offset %}
    <div class="col-md-4 mb-3">
      <div class="card h-100" >
        <a href="{{site.baseurl}}{{ author.permalink }}" class="stretched-link">
          <img class="card-img-top" src="{{site.baseurl}}{{author.image | replace: "images/", "images/thumbnails/" }}" alt="Card image cap" width="300" height="300"/>
        </a>
        <div class="card-body">
          <h3 class="lead mt-2">
            <a href="{{site.baseurl}}{{ author.permalink }}" class="stretched-link">{{author.title}}</a>
          </h3>
          <p class="text-info">{{author.accession}}</p>
        </div>
      </div>
    </div>
    {% endfor %}
  {% endfor %}
  </div>
</div>
