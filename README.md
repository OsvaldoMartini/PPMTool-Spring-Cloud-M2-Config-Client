### PPMTool-Spring-Cloud-M2-Config-Client

Using:

spring boot web
spring boot thyme

```
    ...
    @Controller
    public class RateController {

        @Value("${rate}")
        String rate;
        ...

        @RequestMapping("/rate")
        public String getRate(Model m) {

        ...

```

http://localhost:8080/rate
