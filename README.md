# micro

![image](https://user-images.githubusercontent.com/85085962/184563609-955f982d-6676-4333-932b-41b95b196593.png)
```
server.port=8080
server.servlet.context-path=/myservice
```
luego nuestra url vamos a poder acceder de la siguente manera

![image](https://user-images.githubusercontent.com/85085962/184563733-987d2839-d221-4d71-b04b-d81955393c52.png)

anteriormente no era necesario el path /myservice

En el caso que enviemos una variable por la url
```
	//http://localhost:8080/myservice/saludo/juan/pablo
	@GetMapping(value = "saludo/{name}/{apellido}",produces=MediaType.TEXT_PLAIN_VALUE)
	public String saludo(@PathVariable("name") String n,@PathVariable("apellido") String a) {
		return "Bienvenido Sr/a "+n+"con tu appellido: "+a;
	}
  ```
  
