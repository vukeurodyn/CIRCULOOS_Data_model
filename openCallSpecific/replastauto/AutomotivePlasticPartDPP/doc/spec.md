<!-- 10-Header -->  
Entity: AutomotivePlasticPartDPP  
================================<!-- /10-Header -->  
<!-- 15-License -->  
[Open License](https://raw.githubusercontent.com/european-dynamics-rnd/CIRCULOOS_Data_model/refs/heads/main/LICENSE)  
<!-- /15-License -->  
<!-- 20-Description -->  
Global description: **CIRCULOOS data model for the Digital Product Passport of an injection-moulded automotive plastic part in the RePlastAuto value chain, covering product identification, the passport time window and the route the product goes through, with the material inputs and outputs of each step. It follows the StainlessSteelDPP model of the CIRCULOOS Data Platform.**  
version: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## List of properties  

<sup><sub>[*] If there is not a type in an attribute is because it could have several types or different formats/patterns</sub></sup>  
- `address[object]`: The mailing address  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: Property. The country. For example, Spain. Model:'https://schema.org/addressCountry'    
	- `addressLocality[string]`: Property. The locality in which the street address is, and which is in the region. Model:'https://schema.org/addressLocality'    
	- `addressRegion[string]`: Property. The region in which the locality is, and which is in the country. Model:'https://schema.org/addressRegion'    
	- `district[string]`: Property. A district is a type of administrative division that, in some countries, is managed by the local government    
	- `postOfficeBoxNumber[string]`: Property. The post office box number for PO box addresses. For example, 03578. Model:'https://schema.org/postOfficeBoxNumber'    
	- `postalCode[string]`: Property. The postal code. For example, 24004. Model:'https://schema.org/https://schema.org/postalCode'    
	- `streetAddress[string]`: Property. The street address. Model:'https://schema.org/streetAddress'    
	- `streetNr[string]`: Property. Number identifying a specific property on a public street    
- `alternateName[string]`: An alternative name for this item  - `areaServed[string]`: The geographic area where a service or offered item is provided  . Model: [https://schema.org/Text](https://schema.org/Text)- `dataProvider[string]`: A sequence of characters identifying the provider of the harmonised data entity  - `dataSource[*]`: Name of the source file or dataset the record was taken from, for traceability.  - `dateCreated[date-time]`: Entity creation timestamp. This will usually be allocated by the storage platform  - `dateModified[date-time]`: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform  - `description[string]`: A description of this item  - `dppId[*]`: Unique UUID of the Digital Product Passport of this product.  - `endTime[*]`: End time of the Digital Product Passport (ISO 8601 date-time, UTC).  - `factoryInternalBarcode[*]`: Product unique identifier (barcode) assigned at the factory.  - `functionalUnit[*]`: Reference amount of product that the quantities in route are given for, as defined in the project's LCA.  - `id[string]`: Unique entity identifier, with the format urn:ngsi-ld:AutomotivePlasticPartDPP:<dppId>.  - `location[*]`: GeoProperty. Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon  - `name[string]`: The name of this item  - `owner[array]`: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)  - `productName[*]`: Commercial product name, for example Housing.  - `recycledContent[*]`: Expected unitCode: P1. Share of recycled or secondary material in the product, by mass.  - `route[*]`: The process steps the product goes through, each with its operation name, actor, date, production status, energy consumption and material inputs and outputs.  - `seeAlso[*]`: list of uri pointing to additional resources about the item  - `source[string]`: A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object  - `startTime[*]`: Start time of the Digital Product Passport (ISO 8601 date-time, UTC).  - `type[string]`: NGSI Entity type. It has to be AutomotivePlasticPartDPP  - `valueChain[*]`: Identifier of the CIRCULOOS value chain the record belongs to (here "replastauto").  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Required properties  
- `dppId`  - `factoryInternalBarcode`  - `id`  - `productName`  - `route`  - `startTime`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-RequiredProperties -->  
<!-- /40-RequiredProperties -->  
<!-- 50-DataModelHeader -->  
## Data Model description of properties  
Sorted alphabetically (click for details)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
AutomotivePlasticPartDPP:    
  description: CIRCULOOS data model for the Digital Product Passport of an injection-moulded automotive plastic part in the RePlastAuto value chain, covering product identification, the passport time window and the route the product goes through, with the material inputs and outputs of each step. It follows the StainlessSteelDPP model of the CIRCULOOS Data Platform.    
  properties:    
    address:    
      description: The mailing address    
      properties:    
        addressCountry:    
          description: Property. The country. For example, Spain. Model:'https://schema.org/addressCountry'    
          type: string    
        addressLocality:    
          description: Property. The locality in which the street address is, and which is in the region. Model:'https://schema.org/addressLocality'    
          type: string    
        addressRegion:    
          description: Property. The region in which the locality is, and which is in the country. Model:'https://schema.org/addressRegion'    
          type: string    
        district:    
          description: Property. A district is a type of administrative division that, in some countries, is managed by the local government    
          type: string    
        postOfficeBoxNumber:    
          description: Property. The post office box number for PO box addresses. For example, 03578. Model:'https://schema.org/postOfficeBoxNumber'    
          type: string    
        postalCode:    
          description: Property. The postal code. For example, 24004. Model:'https://schema.org/https://schema.org/postalCode'    
          type: string    
        streetAddress:    
          description: Property. The street address. Model:'https://schema.org/streetAddress'    
          type: string    
        streetNr:    
          description: Property. Number identifying a specific property on a public street    
          type: string    
      type: object    
      x-ngsi:    
        model: https://schema.org/address    
        type: Property    
    alternateName:    
      description: An alternative name for this item    
      type: string    
      x-ngsi:    
        type: Property    
    areaServed:    
      description: The geographic area where a service or offered item is provided    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    dataProvider:    
      description: A sequence of characters identifying the provider of the harmonised data entity    
      type: string    
      x-ngsi:    
        type: Property    
    dataSource:    
      allOf:    
        - additionalProperties: no    
          properties:    
            observedAt:    
              format: date-time    
              type: string    
            type:    
              enum:    
                - Property    
              type: string    
            value:    
              type: string    
          required:    
            - type    
            - value    
          type: object    
      description: Name of the source file or dataset the record was taken from, for traceability.    
      x-ngsi:    
        type: Property    
    dateCreated:    
      description: Entity creation timestamp. This will usually be allocated by the storage platform    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateModified:    
      description: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    description:    
      description: A description of this item    
      type: string    
      x-ngsi:    
        type: Property    
    dppId:    
      allOf:    
        - additionalProperties: no    
          properties:    
            observedAt:    
              format: date-time    
              type: string    
            type:    
              enum:    
                - Property    
              type: string    
            value:    
              type: string    
          required:    
            - type    
            - value    
          type: object    
      description: Unique UUID of the Digital Product Passport of this product.    
      x-ngsi:    
        type: Property    
    endTime:    
      allOf:    
        - additionalProperties: no    
          properties:    
            observedAt:    
              format: date-time    
              type: string    
            type:    
              enum:    
                - Property    
              type: string    
            value:    
              format: date-time    
              pattern: ^[0-9]{4}-[0-9]{2}-[0-9]{2}T[0-9]{2}:[0-9]{2}:[0-9]{2}(\.[0-9]+)?(Z|[+-][0-9]{2}:[0-9]{2})$    
              type: string    
          required:    
            - type    
            - value    
          type: object    
      description: End time of the Digital Product Passport (ISO 8601 date-time, UTC).    
      x-ngsi:    
        type: Property    
    factoryInternalBarcode:    
      allOf:    
        - additionalProperties: no    
          properties:    
            observedAt:    
              format: date-time    
              type: string    
            type:    
              enum:    
                - Property    
              type: string    
            value:    
              type: string    
          required:    
            - type    
            - value    
          type: object    
      description: Product unique identifier (barcode) assigned at the factory.    
      x-ngsi:    
        type: Property    
    functionalUnit:    
      allOf:    
        - additionalProperties: no    
          properties:    
            observedAt:    
              format: date-time    
              type: string    
            type:    
              enum:    
                - Property    
              type: string    
            value:    
              type: string    
          required:    
            - type    
            - value    
          type: object    
      description: Reference amount of product that the quantities in route are given for, as defined in the project's LCA.    
      x-ngsi:    
        type: Property    
    id:    
      description: Unique entity identifier, with the format urn:ngsi-ld:AutomotivePlasticPartDPP:<dppId>.    
      type: string    
      x-ngsi:    
        type: Property    
    location:    
      description: GeoProperty. Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon    
      oneOf:    
        - description: GeoProperty. Geojson reference to the item. Point    
          properties:    
            bbox:    
              description: Property. BBox of the  Point    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              description: Property. Coordinates of the Point    
              items:    
                type: number    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - Point    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON Point    
          type: object    
        - description: GeoProperty. Geojson reference to the item. LineString    
          properties:    
            bbox:    
              description: Property. BBox coordinates of the LineString    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              description: Property. Coordinates of the LineString    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - LineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON LineString    
          type: object    
        - description: GeoProperty. Geojson reference to the item. Polygon    
          properties:    
            bbox:    
              description: Property. BBox coordinates of the Polygon    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              description: Property. Coordinates of the Polygon    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 4    
                type: array    
              type: array    
            type:    
              enum:    
                - Polygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON Polygon    
          type: object    
        - description: GeoProperty. Geojson reference to the item. MultiPoint    
          properties:    
            bbox:    
              description: Property. BBox coordinates of the LineString    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              description: Property. Coordinates of the MulitPoint    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPoint    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON MultiPoint    
          type: object    
        - description: GeoProperty. Geojson reference to the item. MultiLineString    
          properties:    
            bbox:    
              description: Property. BBox coordinates of the LineString    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              description: Property. Coordinates of the MultiLineString    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiLineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON MultiLineString    
          type: object    
        - description: GeoProperty. Geojson reference to the item. MultiLineString    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              description: Property. Coordinates of the MultiPolygon    
              items:    
                items:    
                  items:    
                    items:    
                      type: number    
                    minItems: 2    
                    type: array    
                  minItems: 4    
                  type: array    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPolygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON MultiPolygon    
          type: object    
    name:    
      description: The name of this item    
      type: string    
      x-ngsi:    
        type: Property    
    owner:    
      description: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)    
      items:    
        anyOf:    
          - description: Property. Identifier format of any NGSI entity    
            maxLength: 256    
            minLength: 1    
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
            type: string    
          - description: Property. Identifier format of any NGSI entity    
            format: uri    
            type: string    
        description: Relationship. Unique identifier of the entity    
      type: array    
      x-ngsi:    
        type: Property    
    productName:    
      allOf:    
        - additionalProperties: no    
          properties:    
            observedAt:    
              format: date-time    
              type: string    
            type:    
              enum:    
                - Property    
              type: string    
            value:    
              type: string    
          required:    
            - type    
            - value    
          type: object    
      description: Commercial product name, for example Housing.    
      x-ngsi:    
        type: Property    
    recycledContent:    
      allOf:    
        - additionalProperties: no    
          anyOf:    
            - required:    
                - value    
            - required:    
                - minValue    
            - required:    
                - maxValue    
          properties:    
            maxValue:    
              description: Upper bound of the value, when the source declares a range or a maximum.    
              type: number    
            minValue:    
              description: Lower bound of the value, when the source declares a range or a minimum.    
              type: number    
            observedAt:    
              format: date-time    
              type: string    
            type:    
              enum:    
                - Property    
              type: string    
            unitCode:    
              description: Unit of measurement of the value, given as a UN/CEFACT code where one exists.    
              type: string    
            value:    
              description: Exact measured value, when a single figure is known.    
              type: number    
          required:    
            - type    
            - unitCode    
          type: object    
      description: 'Expected unitCode: P1. Share of recycled or secondary material in the product, by mass.'    
      x-ngsi:    
        type: Property    
    route:    
      allOf:    
        - additionalProperties: no    
          properties:    
            observedAt:    
              format: date-time    
              type: string    
            type:    
              enum:    
                - Property    
              type: string    
            value:    
              description: Property. Ordered list of the process steps the product goes through, from the collection of the secondary raw material to the finished product.    
              items:    
                additionalProperties: no    
                properties:    
                  actor:    
                    description: Property. Value chain partner (or external actor) that performs this step.    
                    type: string    
                  date:    
                    description: Property. Date and time (ISO 8601, UTC) at which the operation was performed.    
                    format: date-time    
                    type: string    
                  energyConsumption:    
                    additionalProperties: no    
                    description: Property. Electricity consumed for this route step.    
                    properties:    
                      unitCode:    
                        description: Property. UN/CEFACT code of the unit of the consumed energy, for example WHR (watt hour).    
                        type: string    
                      value:    
                        description: Property. Energy consumed by this route step.    
                        minimum: 0    
                        type: number    
                    required:    
                      - value    
                      - unitCode    
                    type: object    
                  heatConsumption:    
                    additionalProperties: no    
                    description: Property. Heat consumed for this route step, when reported separately from electricity.    
                    properties:    
                      unitCode:    
                        description: Property. UN/CEFACT code of the unit of the consumed energy, for example WHR (watt hour).    
                        type: string    
                      value:    
                        description: Property. Heat consumed by this route step.    
                        minimum: 0    
                        type: number    
                    required:    
                      - value    
                      - unitCode    
                    type: object    
                  inputs:    
                    description: Property. Materials, ancillaries, fuels and water that enter this route step.    
                    items:    
                      additionalProperties: no    
                      properties:    
                        destination:    
                          description: Property. Partner or treatment the output goes to (next actor, recycling, landfill, incineration).    
                          type: string    
                        flowType:    
                          description: Property. Role of the flow in the step. Secondary raw materials and wastes are the flows that link value chains in CIRCULOOS.    
                          enum:    
                            - rawMaterial    
                            - secondaryRawMaterial    
                            - ancillaryMaterial    
                            - fuel    
                            - water    
                            - packaging    
                            - component    
                            - intermediateProduct    
                            - product    
                            - byProduct    
                            - waste    
                            - wastewater    
                            - emission    
                          type: string    
                        material:    
                          description: Property. Name of the material or flow, as written in the source inventory.    
                          type: string    
                        origin:    
                          description: Property. Supplier or place the input comes from.    
                          type: string    
                        quantity:    
                          additionalProperties: no    
                          properties:    
                            unitCode:    
                              description: Property. UN/CEFACT code of the unit, for example KGM (kilogram), LTR (litre), MTK (square metre), H87 (piece).    
                              type: string    
                            value:    
                              description: Property. Amount of the flow per functional unit (see functionalUnit).    
                              minimum: 0    
                              type: number    
                          required:    
                            - value    
                            - unitCode    
                          type: object    
                        transportDistance:    
                          additionalProperties: no    
                          properties:    
                            unitCode:    
                              description: Property. UN/CEFACT code of the unit, for example KGM (kilogram), LTR (litre), MTK (square metre), H87 (piece).    
                              type: string    
                            value:    
                              description: Property. Distance between origin and destination, usually in KMT (kilometre).    
                              minimum: 0    
                              type: number    
                          required:    
                            - value    
                            - unitCode    
                          type: object    
                        transportMode:    
                          description: Property. Means of transport, for example truck, van, car or ship.    
                          type: string    
                      required:    
                        - material    
                        - flowType    
                      type: object    
                    type: array    
                  operation:    
                    description: Property. Name of the process step, as named in the project's LCA inventory or value chain description.    
                    type: string    
                  outputs:    
                    description: Property. Products, by-products, wastes and emissions that leave this route step, with their destination.    
                    items:    
                      additionalProperties: no    
                      properties:    
                        destination:    
                          description: Property. Partner or treatment the output goes to (next actor, recycling, landfill, incineration).    
                          type: string    
                        flowType:    
                          description: Property. Role of the flow in the step. Secondary raw materials and wastes are the flows that link value chains in CIRCULOOS.    
                          enum:    
                            - rawMaterial    
                            - secondaryRawMaterial    
                            - ancillaryMaterial    
                            - fuel    
                            - water    
                            - packaging    
                            - component    
                            - intermediateProduct    
                            - product    
                            - byProduct    
                            - waste    
                            - wastewater    
                            - emission    
                          type: string    
                        material:    
                          description: Property. Name of the material or flow, as written in the source inventory.    
                          type: string    
                        origin:    
                          description: Property. Supplier or place the input comes from.    
                          type: string    
                        quantity:    
                          additionalProperties: no    
                          properties:    
                            unitCode:    
                              description: Property. UN/CEFACT code of the unit, for example KGM (kilogram), LTR (litre), MTK (square metre), H87 (piece).    
                              type: string    
                            value:    
                              description: Property. Amount of the flow per functional unit (see functionalUnit).    
                              minimum: 0    
                              type: number    
                          required:    
                            - value    
                            - unitCode    
                          type: object    
                        transportDistance:    
                          additionalProperties: no    
                          properties:    
                            unitCode:    
                              description: Property. UN/CEFACT code of the unit, for example KGM (kilogram), LTR (litre), MTK (square metre), H87 (piece).    
                              type: string    
                            value:    
                              description: Property. Distance between origin and destination, usually in KMT (kilometre).    
                              minimum: 0    
                              type: number    
                          required:    
                            - value    
                            - unitCode    
                          type: object    
                        transportMode:    
                          description: Property. Means of transport, for example truck, van, car or ship.    
                          type: string    
                      required:    
                        - material    
                        - flowType    
                      type: object    
                    type: array    
                  productionStatus:    
                    description: Property. Outcome of the operation as reported by the production line, for example OK.    
                    type: string    
                required:    
                  - operation    
                  - date    
                  - productionStatus    
                type: object    
              minItems: 1    
              type: array    
          required:    
            - type    
            - value    
          type: object    
      description: The process steps the product goes through, each with its operation name, actor, date, production status, energy consumption and material inputs and outputs.    
      x-ngsi:    
        type: Property    
    seeAlso:    
      description: list of uri pointing to additional resources about the item    
      oneOf:    
        - items:    
            format: uri    
            type: string    
          minItems: 1    
          type: array    
        - format: uri    
          type: string    
      x-ngsi:    
        type: Property    
    source:    
      description: A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object    
      type: string    
      x-ngsi:    
        type: Property    
    startTime:    
      allOf:    
        - additionalProperties: no    
          properties:    
            observedAt:    
              format: date-time    
              type: string    
            type:    
              enum:    
                - Property    
              type: string    
            value:    
              format: date-time    
              pattern: ^[0-9]{4}-[0-9]{2}-[0-9]{2}T[0-9]{2}:[0-9]{2}:[0-9]{2}(\.[0-9]+)?(Z|[+-][0-9]{2}:[0-9]{2})$    
              type: string    
          required:    
            - type    
            - value    
          type: object    
      description: Start time of the Digital Product Passport (ISO 8601 date-time, UTC).    
      x-ngsi:    
        type: Property    
    type:    
      description: NGSI Entity type. It has to be AutomotivePlasticPartDPP    
      enum:    
        - AutomotivePlasticPartDPP    
      type: string    
      x-ngsi:    
        type: Property    
    valueChain:    
      allOf:    
        - additionalProperties: no    
          properties:    
            observedAt:    
              format: date-time    
              type: string    
            type:    
              enum:    
                - Property    
              type: string    
            value:    
              type: string    
          required:    
            - type    
            - value    
          type: object    
      description: Identifier of the CIRCULOOS value chain the record belongs to (here "replastauto").    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - dppId    
    - factoryInternalBarcode    
    - productName    
    - startTime    
    - route    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2021 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/circuloos_data_model/blob/master/AutomotivePlasticPartDPP/LICENSE.md    
  x-model-schema: https://raw.githubusercontent.com/european-dynamics-rnd/CIRCULOOS_Data_model/main/openCallSpecific/replastauto/AutomotivePlasticPartDPP/schema.json    
  x-model-tags: replastauto    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Example payloads    
Not available the example of a AutomotivePlasticPartDPP in JSON-LD format as key-values. This is compatible with NGSI-LD when  using `options=keyValues` and returns the context data of an individual entity.  
#### AutomotivePlasticPartDPP NGSI-LD normalized Example    
Here is an example of a AutomotivePlasticPartDPP in JSON-LD format as normalized. This is compatible with NGSI-LD when not using options and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "@context": [  
    "http://circuloos-ld-context/circuloos-context.jsonld",  
    "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context-v1.8.jsonld"  
  ],  
  "id": "urn:ngsi-ld:AutomotivePlasticPartDPP:REPLASTAUTO-DPP-0001",  
  "type": "AutomotivePlasticPartDPP",  
  "dppId": {  
    "type": "Property",  
    "value": "REPLASTAUTO-DPP-0001"  
  },  
  "factoryInternalBarcode": {  
    "type": "Property",  
    "value": "ELVEZ-0001"  
  },  
  "productName": {  
    "type": "Property",  
    "value": "Automotive plastic part (Housing)"  
  },  
  "startTime": {  
    "type": "Property",  
    "value": "2026-01-01T00:00:00Z"  
  },  
  "endTime": {  
    "type": "Property",  
    "value": "2026-01-31T00:00:00Z"  
  },  
  "route": {  
    "type": "Property",  
    "value": [  
      {  
        "operation": "Injection molding",  
        "actor": "ELVEZ",  
        "date": "2026-01-01T00:00:00Z",  
        "productionStatus": "Not reported",  
        "inputs": [  
          {  
            "material": "Plastic granulates (ABS, PC, PBT, PA, PA66, PMMA, PEI, PES)",  
            "flowType": "rawMaterial",  
            "origin": "Raw material supplier"  
          }  
        ],  
        "outputs": [  
          {  
            "material": "Automotive plastic part (Housing)",  
            "flowType": "product"  
          },  
          {  
            "material": "Scrap material (sprues, rejects)",  
            "flowType": "waste",  
            "destination": "AI vision sorting"  
          }  
        ]  
      },  
      {  
        "operation": "AI vision sorting of post-industrial scrap",  
        "actor": "ELVEZ",  
        "date": "2026-01-01T00:00:00Z",  
        "productionStatus": "Not reported",  
        "inputs": [  
          {  
            "material": "Scrap material (sprues, rejects)",  
            "flowType": "waste",  
            "origin": "ELVEZ injection molding"  
          }  
        ],  
        "outputs": [  
          {  
            "material": "Sorted reground plastic",  
            "flowType": "secondaryRawMaterial",  
            "destination": "ELVEZ injection molding (non-critical parts)"  
          },  
          {  
            "material": "Plastic not suitable for internal reuse",  
            "flowType": "waste",  
            "destination": "External recycler"  
          }  
        ]  
      }  
    ]  
  },  
  "functionalUnit": {  
    "type": "Property",  
    "value": "1 automotive plastic part (same product in AS-IS and TO-BE)"  
  },  
  "valueChain": {  
    "type": "Property",  
    "value": "replastauto"  
  },  
  "dataSource": {  
    "type": "Property",  
    "value": "RePlastAuto-20260330_GRETA_tool_OpenCall_LCI_Template_ELVEZ.xlsx, sheets MODEL and AS_IS (quantities not filled in; ELVEZ marks the information as sensitive data); sorting step from the RePlastAuto project description; dppId, factoryInternalBarcode, dates and productionStatus are illustrative; material flows are taken from the source"  
  }  
}  
```  
</details><!-- /80-Examples -->  
