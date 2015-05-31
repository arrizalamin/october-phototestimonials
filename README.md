# october-phototestimonials
This plugin is an extension to the [Mja.Testimonials](https://octobercms.com/plugin/mja-testimonials) plugin. This extension enables uploading photo for testimonials.

## Installation
This plugin requires [Mja.Testimonials](https://octobercms.com/plugin/mja-testimonials), so make sure you have that installed.

Go to System - Updates and in the search field enter ArrizalAmin.PhotoTestimonials

### Usage
Copy /plugins/mja/testimonials/components/testimonials/default.htm to your themes partials/testimonials folder. Where you want your image, add:
~~~
{% for testimonial in testimonials %}
    <div class="col-md-6">
        <figure class="photo">
            <img src="{{ testimonial.photo.path }}" alt="">
        </figure>
        <div class="context">
            <div class="inner">
                <blockquote>{{ testimonial.content|raw }}</blockquote>
                {% if testimonial.author %}
                <p class="who">{{ testimonial.author }}</p>
                {% endif %}
            </div>
        </div>
    </div>
{% endfor %}
~~~
Remember that you can format it any way you like.
