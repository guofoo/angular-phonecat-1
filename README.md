Note that the ***phones.json*** file contains unique IDs and image URLs for each of the phones. The URLs point to the app/img/phones/ directory, 
which contains pictures for phones.

### Template

To dynamically generate links that will in the future lead to phone detail pages, we used the now-familiar double-curly brace binding 
in the `href` attribute values. In Chapter 2, we added the `{{phone.name}}` binding as the element content. 
In this exercise, the `{{phone.id}}` binding is used in the element attribute.

We also added phone images next to each record using an image tag with the `ngSrc` directive. That directive prevents the browser from 
treating the Angular {{ expression }} markup literally, and initiating a request to invalid URL `http://localhost:8000/app/{{phone.imageUrl}}`, 
which it would have done if we had only specified an attribute binding in a regular src attribute 
```(<img src="{{phone.imageUrl}}">)```. Using the `ngSrc` directive prevents the browser from making an http request to an invalid location.