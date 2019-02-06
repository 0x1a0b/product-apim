# WSO2 API Management

WSO2 API Management is an Open Source API Management tool that allows APIs/Services to be Secured, Monitored and Rate Controlled. This tool allows API Developers to design, publish, version and manage API lifecycles. It allows application developers to discover and start consuming APIs. The lightweight API Gateway intercepts all API requests applying Security, Rate Limiting and Monitoring aspects on your APIs.

More information about this product can be found [here](http://wso2.com/api-management/)

## Building from source

1. Download and install JDK 8 update 77 or later
2. Make sure you have npm 5.x or above installed.
3. Get a clone or download the source from this repository (https://github.com/wso2/carbon-apimgt)
4. Run the Maven command ``mvn clean  install`` from within the carbon-apimgt directory.
5. Get a clone or download the source from this repository (https://github.com/wso2/product-apim)
6. Make sure you have Docker v17.09.0 or above installed.
7. Run the Maven command ``mvn clean install`` from within the product-apim directory.

## Running the product

### Running WSO2 API Manager Default Profile
1. Go to the default runtime dir wso2apim-${project.version}/wso2/default/bin directory and execute the carbon.sh script: ``./carbon.sh``

### Running WSO2 API Manager Gateway
1. Download the API Manager gateway distribution from [releases](https://github.com/wso2/product-apim/releases) OR if you built from source, find the binary from product-apim/gateway/target.
2. Extract the distribution. Ex: unzip wso2apim-gateway-${project.version}.zip
3. Go to the wso2apim-gateway-${project.version} directory and execute ``bin/ballerina run service services.bsz``

#### Note:

* Make sure you start the Gateway from ``wso2apim-gateway-3.0.0`` root directory; not inside ``/bin`` directory.
* Make sure you start the Gateway at the end, after starting all the other servers.
* After Publishing an API to gateway make sure that you restart the gateway by executing ``bin/ballerina run service services.bsz org/wso2/carbon/apimgt/gateway``

### Testing

* Open your web browser and type the URL https://localhost:9443/publisher to go to the API Publisher application which allows you to design and publish APIs.
* On the web browser type the URL https://localhost:9443/store to visit the API Store to discover and consume APIs.

## Product profiles

### Running WSO2 Key Manager Profile
1. Download the product distribution from [releases](https://github.com/wso2/product-apim/releases) OR if you built from source, find the binary from product-apim/product/target.
2. Extract the distribution. Ex: unzip wso2apim-${project.version}.zip
3. Go to the key manager runtime dir wso2apim-${project.version}/wso2/key-manager/bin directory and execute the carbon.sh script: ``./carbon.sh``
