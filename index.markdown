---
layout: base
---
{% for image in site.static_files reversed %}
    {% if image.path contains 'assets/media/'  %}
        {% if image.extname == '.jpg' or image.extname == '.jpeg' %}
            {% include story.html %}
        {% elsif image.extname == '.mp4' or image.extname == '.MOV' or image.extname == '.mov' %}
            {% include video.html %}
        {% endif %}
    {% endif %}
{% endfor %}
