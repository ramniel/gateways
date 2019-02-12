# Available Scripts

- To build open a console and execute ./build.sh
- To run open a console and execute ./run.sh

# Endpoints:

## Create a gateway:
POST http://localhost:8080/gateways<br>
body: {<br>
"serial": "string", //a unique serial number ej: AbC123<br>
"name": "string", //a human-readable name ej: Gateway A<br>
"ip": "string" //an IPv4 address ej: 10.0.0.1<br>
}

## Delete a gateway:
DELETE http://localhost:8080/gateways/{serial} // ej: http://localhost:8080/gateways/AbC123

## Get all stored gateways:
GET http://localhost:8080/gateways

## Get a single gateway:
GET http://localhost:8080/gateways/{serial} // ej: http://localhost:8080/gateways/AbC123

## Add a device from a gateway
POST http://localhost:8080/gateways/{serial}/device<br>
body: {<br>
"vendor": "string", // ej: Vendor A<br>
"status": "online|offline" // ej: online<br>
}

## Remove a device from a gateway
DELETE http://localhost:8080/gateways/{serial}/device/{device_uid} // ej: http://localhost:8080/gateways/AbC123/device/1
