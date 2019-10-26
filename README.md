### PPMTool-Spring-Cloud-M2-Config-Client

Using:

* spring boot web
* spring boot thyme

### Check the Usage of the Model:


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


### '@RefreshScope'


 Add the actuator dependency

````
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-actuator</artifactId>
		</dependency> 
````

When is called the endpoint:
	
	> The Refresh 'actuator' is set in the Client Side
	> this will update the cache
	
	'http://localhost:8080/refresh'

it will return alll field collected from 'Config Server'

Change any value innside of the 'GitHub' like:

	'rate=2.22' in the file "s1rates.properties"

````
 https://github.com/OsvaldoMartini/PPMTool-Spring-Cloud-Config-Wa-Tolls/blob/master/station1/s1rates.properties
````
  After that executethe Refresh call:
  
````
  http://localhost:8080/refresh
```
