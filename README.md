# DropWizard Pagination using Jersey Declarative Hyperlinking

Implemented DropWizard Pagination using [Jersey Declarative Hyperlinking](https://jersey.github.io/documentation/latest/declarative-linking.html).

Supports content negotiation using Accept headers. Uses [Eclipse MOXy](http://www.eclipse.org/eclipselink/#moxy) to support JAXB/JSON binding. 

[HTTP Link headers](http://tools.ietf.org/html/rfc5988#section-5) are added to responses using annotations.

Freemarker templates are used to render the view.


![Screenshot](src/main/resources/screenshot.png?raw=true "Pagination")

Response showing link header with the next set of data to retrieve.

![Link Header](src/main/resources/link-header.png?raw=true "Link Header")

How to start the Pagination application
---

1. Run `mvn clean install` to build your application
1. Start application with `java -jar target/pagination-1.0-SNAPSHOT.jar server config.yml`
1. To check that your application is running enter url `http://localhost:8080`
4. To view the pagination, click this link `http://localhost:8080/items/view`

Health Check
---

To see your applications health enter url `http://localhost:8081/healthcheck`


References
---
1. http://kingsfleet.blogspot.com/2014/05/declarative-linking-in-jersey-29.html
1. http://kingsfleet.blogspot.com/2014/05/reading-and-writing-jax-rs-link-objects.html
1. https://github.com/jersey/jersey/tree/master/examples/declarative-linking
1. https://stackoverflow.com/questions/45578563/api-pagination-in-dropwizard
