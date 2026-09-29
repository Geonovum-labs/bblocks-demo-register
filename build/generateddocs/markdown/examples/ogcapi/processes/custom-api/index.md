
# Demo OGC API processes instance - LOF (Api)

`geonovum.examples.ogcapi.processes.custom-api` *v1.0*

An example of an OGC API Processes implementation using building blocks - Local Outlier Factor

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### Metadata beschrijving van het LOF Process
#### ttl
```ttl
@prefix apkg: <http://w3id.org/apkg/terms#> .
@prefix schema: <https://schema.org/> .
@prefix dct: <http://purl.org/dc/terms/> .
@prefix dcat: <http://www.w3.org/ns/dcat#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix ex: <http://example.org/ogcapi/custom-api#> .

ex:custom-api a apkg:ApplicationPackage ;
    schema:identifier "https://w3id.org/ogcapi/custom-api" ;
    dct:title "Demo OGC API processes instance - LOF" ;
    dct:description "An example of an OGC API Processes implementation using building blocks - Local Outlier Factor" ;
    dct:issued "2025-12-17"^^xsd:date ;
    dct:modified "2025-12-17"^^xsd:date ;
    schema:softwareVersion "1.0" ;
    dcat:keyword "examples" ;
    dcat:keyword "ogc api" ;
    dcat:keyword "ogc api processes" ;
    schema:sdPublisher ex:publisher ;
    schema:sdDatePublished "2025-12-17"^^xsd:date ;
    schema:sourceOrganization ex:organisation .

ex:localoutlierProcess a apkg:Process ;
    dct:type "CommandLineTool" ;
    apkg:hasInput ex:dataset , ex:n_neighbors , ex:leaf_size , ex:output_column ;
    apkg:hasOutput ex:output_dataset .

ex:dataset a apkg:Parameter ;
    dct:identifier "dataset" ;
    dct:type "string" ;
    apkg:label "Dataset URL" .

ex:n_neighbors a apkg:Parameter ;
    dct:identifier "n_neighbors" ;
    dct:type "int" ;
    apkg:label "Number of neighbors" .

ex:leaf_size a apkg:Parameter ;
    dct:identifier "leaf_size" ;
    dct:type "int" ;
    apkg:label "Leaf size" .

ex:output_column a apkg:Parameter ;
    dct:identifier "output_column" ;
    dct:type "string" ;
    apkg:label "Output column" .

ex:output_dataset a apkg:Parameter ;
    dct:identifier "output_dataset" ;
    dct:type "string" ;
    apkg:label "Output dataset" .


```


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum-labs/bblocks-demo-register](https://github.com/Geonovum-labs/bblocks-demo-register)
* Path: `_sources/ogcapi/processes/custom-api`

