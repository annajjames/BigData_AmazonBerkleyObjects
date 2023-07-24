## Problem Statement
1. Amazon product listings metadata is available as a JSON file with each JSON object corresponding to a product. This makes it difficult to generate reports such as brands, colors, models available for a product, or the language specific keywords associated for a product.
2. A product has multiple images which are neither labeled nor available in a single directly.

## Background
Amazon Berkley Objects (ABO) is a collection of 147,702 product listings with multilingual metadata and 398,212 unique catalogue images. Each JSON object/each product has number of keys like brand name, product description, keyworkds, item dimensions, model, etc.
Business wants to easilty generate reports to analyze gaps in terms of models, brands available for a product, or regulary add or modify keywords to keep the site up-to-date and to reflect the trending keyword search.
Business also wants to store all images of a product together.

## Objective
1. Transform the raw data to a form that is ready for consumption by the downstream systems using **PySpark**. The final transformed data is made available in a **gold delta table** format.
2. Create an unsupervised image clustering model using **Mlib**.

Raw data schema:
![image](https://github.com/annajjames/BigData_AmazonBerkleyObjects/assets/58715002/92b43436-d1a9-468f-8b1f-5370b01631e2)

Gold table schema:
![image](https://github.com/annajjames/BigData_AmazonBerkleyObjects/assets/58715002/8c91b76e-5296-4698-b4c4-62bad5f97288)


## Attribution
- Credit for the data, including all images: Amazon.com
- Credit for building the dataset, archives, and benchmark sets: Matthieu GuillauminAmazon.com Thomas DideriksenAmazon.com Kenan DengAmazon.com Himanshu AroraAmazon.com Arnab DhuaAmazon.com Xi (Brian) ZhangAmazon.com Tomas Yago-VicenteAmazon.com Jasmine CollinsUC Berkeley Shubham GoelUC Berkeley Jitendra MalikUC Berkele.
s3://amazon-berkeley-objects/listings/metadata/
