---
layout: default
permalink: /view-from-france/
title: The View from France
---
For most French people who thought of England at all, it represented a land of liberty, with freedoms of belief, of speech, and of the press. But this admiration came with a qualification: the English, they said, thought a little too well of themselves. The English stereotype in French literature and drama was a 'milord', who was typically haughty, socially ill at ease, a woman hater, and someone who suffered from a form of melancholy. This malady was deemed to be peculiar to inhabitants of English shores, and was likely to result in acts of suicide. On the whole the perceived notion of the English national character was disagreeable.

The dangers of Revolution and the subsequent war curtailed the popular leisure activity of travel. During the lull in hostilities of the short-lived peace of Amiens (1802-3), and after the abdication of Napoleon (1814) the English flooded into Paris en masse. Most of the French caricatures in this exhibition are from around 1814-5. During this time the old stereotype was made more contemptible. The English appeared so often in the French caricatures of this time not simply because they were there, although their reappearance after the prolonged absences did have a novelty value. They were also targeted because they were despised as an Occupying Power. They were unwelcome guests, who plundered France's resources, drank Paris dry and offended its residents with their bad habits and unfashionable clothes.

In terms of physical appearance the English stereotype in the French satires is not wholly based upon the fat and stocky John-Bullesque stereotype. This type does appear, but he is amongst a wide variety of equally unattractive, misshapen men and women. The intention of the artist was to make the visitors look awkward and ungainly, having squeezed their bodies into ill-fitting hats and clothes. Their efforts to mimic Parisian fashions are laughable. They are such strange shapes, that nothing they wore could possibly disguise their plainness. Their outer wrappings mirror their inner souls: they themselves are plain and dull, the ladies unwilling or unable to fill silence with conversation, and the men prone to drink and urinating indoors.

<div class="container mb-3">
  <div class="row">
{% assign rows = site.france.size | divided_by: 2.0 | ceil %}
{% for i in (1..rows) %}
{% assign offset = forloop.index0 | times: 2 %}
{% assign sorted = site.france | sort:"order" %}
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
        </div>
      </div>
    </div>
    {% endfor %}
  {% endfor %}
  </div>
</div>
