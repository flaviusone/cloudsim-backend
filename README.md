# cloudsim-backend
This repo provides helper java files for the [cloudsim-ui](https://github.com/flaviusone/cloudsim-ui) app. 

Once you add the files to your cloudsim project you can setup the enviroment like this:
```java
			List<Datacenter> datacenterList = new LinkedList<Datacenter>();
			datacenterList.add(datacenter0);
			datacenterList.add(datacenter1);
			
			List<DatacenterBroker> brokerList = new LinkedList<DatacenterBroker>();
			brokerList.add(broker1);
			brokerList.add(broker2);
			
			Gson gson = new Gson();
			get("/", (request, response) -> {
					
				response.type("application/json");
				response.header("Access-Control-Allow-Origin", "*");
				
				return new PayloadContainer(datacenterList, brokerList);
			}, gson::toJson);

```
