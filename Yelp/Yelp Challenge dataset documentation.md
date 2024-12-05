     

### <a id="documentation-body"></a>

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image1.png?raw=true)

MongoDB Physical Model
----------------------

#### Schema for:

Model name: Yelp Challenge dataset

Author: Pascal

Version: 1.2

File name: Yelp Challenge dataset.hck.json

File path: C:\\Hackolade Studio files\\Models\\MongoDB\\Yelp Challenge dataset.hck.json

Printed On: Thu Dec 05 2024 18:27:58 GMT+0100 (Central European Standard Time)

Created with: [Hackolade](https://hackolade.com/) - Polyglot data modeling for NoSQL databases, storage formats, REST APIs, and JSON in RDBMS

### <a id="contents"></a>

*   [Table of Contents](#contents)
*   [1\. Model](#model)
*   [2\. ER Diagram Views](#diagramViews)
    *   [2.1 Domain view](#65013f10-4748-11eb-a6d2-ebfe0d19463b)
*   [3\. Databases](#containers)
    *   [3.1 yelp](#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6)
        
        [3.1.2. Collections](#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6-children)
        
        [3.1.2.1 businesses](#0dd7ead0-2b24-11e6-b7e5-591297143e36)
        
        [3.1.2.2 reviews](#0da2aa00-2b24-11e6-b7e5-591297143e36)
        
        [3.1.2.3 tips](#0de02830-2b24-11e6-b7e5-591297143e36)
        
        [3.1.2.4 users](#0df0f110-2b24-11e6-b7e5-591297143e36)
        
        [3.1.2.5 checkins](#a080d1d0-91f6-11e9-a924-ddc9cd9b071f)
        
*   [4\. Views](#views)
    *   [4.1 rov\_bussiness](#5c771580-5193-11e7-b9f2-49270a53df2c)
    *   [4.2 rov\_reviews](#090874c0-5206-11e7-8e65-9b1d6a151b1d)
*   [5\. Relationships](#relationships)
    *   [5.1 fk\_tipsBusinesses](#8a3660f0-2b26-11e6-b7e5-591297143e36)
    *   [5.2 fk\_tipsUsers](#aa956d50-2b26-11e6-b7e5-591297143e36)
    *   [5.3 fk\_reviewsUsers](#e2514f70-2b26-11e6-b7e5-591297143e36)
    *   [5.4 fk\_reviewsBusinesses](#fb857d40-2b26-11e6-b7e5-591297143e36)
    *   [5.5 fk businesses.business\_id to checkins.business\_id](#003231f0-91f7-11e9-a924-ddc9cd9b071f)

### <a id="model"></a>

## 1\. Model

### 1.1 Model **Yelp Challenge dataset**

#### 1.1.1 **Yelp Challenge dataset** Entity Relationship Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image2.png?raw=true)

#### 1.1.2 **Yelp Challenge dataset** Properties

##### 1.1.2.1 **Details** tab

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td><span>Model name</span></td><td>Yelp Challenge dataset</td></tr><tr><td><span>Description</span></td><td><div class="docs-markdown"><p>Schema inferred from the reverse-engineering of a Yelp Challenge dataset available from <a href=https://www.yelp.com/dataset_challenge/dataset>https://www.yelp.com/dataset_challenge/dataset</a></p></div></td></tr><tr><td><span>Author</span></td><td>Pascal</td></tr><tr><td><span>Version</span></td><td>1.2</td></tr><tr><td><span>Target</span></td><td>MongoDB</td></tr><tr><td><span>DB version</span></td><td>v7.x</td></tr><tr><td><span>Synchronization Id</span></td><td>db8a6750-5b42-11e8-9c3f-1d376af9020b</td></tr><tr><td><span>Comments</span></td><td><div class="docs-markdown"><p>The dataset was downloaded and loaded to a MongoDB, then reverse-engineered with Hackolade. The relationships were manually documented to enrich the model.</p><p>This schema shows the power of JSON with the embedding of many attributes logically grouped, one form of implicit relationships. At the same time, the schema is fairly relational, which makes total sense given the conceptual entities. As a result, there's no denormalization. Given the size of the collections, it makes sense to perform this kind of traditional foreing key relationships.</p><p>Note that only fields found in 100% of the sampled documents are 'required' (and differentiated thanks to a solid line box) as opposed to the other fields with dashed line boxes.</p><p>The sampling parameters were:</p><ul><li>absolute up to 1000 documents max per collection</li><li>alpha order of fields</li></ul></div></td></tr></tbody></table>

##### 1.1.2.2 **Options** tab

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody></tbody></table>

#### 1.1.3 **Yelp Challenge dataset** DB Definitions

### <a id="0dd81200-2b24-11e6-b7e5-591297143e36"></a>

##### 1.1.3.1 Field **address**

###### 1.1.3.1.1 **address** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image3.png?raw=true)

###### 1.1.3.1.2 **address** Hierarchy

Parent field: **Definitions**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#7107ebf0-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#760da090-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7bfbe070-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7ee803e0-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#85787730-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#87afc990-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 1.1.3.1.3 **address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>address</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="7107ebf0-dc5b-11e9-b819-e3f2d5171928"></a>

##### 1.1.3.2 Field **houseNum**

###### 1.1.3.2.1 **houseNum** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>houseNum</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.buildingNumber()</td></tr><tr><td>Sample</td><td>123</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="760da090-dc5b-11e9-b819-e3f2d5171928"></a>

##### 1.1.3.3 Field **street**

###### 1.1.3.3.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.street()</td></tr><tr><td>Sample</td><td>Main Street</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="7bfbe070-dc5b-11e9-b819-e3f2d5171928"></a>

##### 1.1.3.4 Field **box**

###### 1.1.3.4.1 **box** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>box</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.secondaryAddress()</td></tr><tr><td>Sample</td><td>10</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="7ee803e0-dc5b-11e9-b819-e3f2d5171928"></a>

##### 1.1.3.5 Field **city**

###### 1.1.3.5.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.city()</td></tr><tr><td>Sample</td><td>Anytown</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="85787730-dc5b-11e9-b819-e3f2d5171928"></a>

##### 1.1.3.6 Field **state**

###### 1.1.3.6.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.state({ abbreviated: true })</td></tr><tr><td>Sample</td><td>CA</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="87afc990-dc5b-11e9-b819-e3f2d5171928"></a>

##### 1.1.3.7 Field **zip**

###### 1.1.3.7.1 **zip** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>zip</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.state({ abbreviated: true })</td></tr><tr><td>Sample</td><td>12345</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="diagramViews"></a>

## 2\. ER Diagram Views

### <a id="65013f10-4748-11eb-a6d2-ebfe0d19463b"></a>

### 2.1 Diagram **Domain view**

#### 2.1.1 **Domain view** Entity Relationship Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image4.png?raw=true)

#### 2.1.2 **Domain view** Graph Diagram

### <a id="containers"></a>

## 3\. Databases

### <a id="3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6"></a>

### 3.1 Database **yelp**

#### 3.1.1 **yelp** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Database name</td><td>yelp</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Enable sharding</td><td>true</td></tr></tbody></table>

### <a id="3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6-children"></a>

#### 3.1.2 **yelp** Collections

### <a id="0dd7ead0-2b24-11e6-b7e5-591297143e36"></a>

##### 3.1.2.1 Collection **businesses**

###### 3.1.2.1.1 **businesses** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image5.png?raw=true)

###### 3.1.2.1.2 **businesses** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>businesses</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Description</td><td><div class="docs-markdown"><p>Checking Markdown inline image in description for Hub</p><p><img alt="Inline image" src="data:image/png;base64,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"></p></div></td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>Storage engine</td><td>WiredTiger</td></tr><tr><td>Validation level</td><td>Off</td></tr><tr><td>Validation action</td><td>Warn</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

###### 3.1.2.1.3 **businesses** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36 class="margin-0">business_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>pk, dk</td><td><div class="docs-markdown"><p>Unique key for businesses</p></div></td><td><div class="docs-markdown"><p>Sat Nov 04 2017 10:12:00 GMT+0100 (Romance Standard Time): some comments</p></div></td></tr><tr><td><a href=#0dd81219-2b24-11e6-b7e5-591297143e36 class="margin-0">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#06399180-d360-11ec-adc4-432dcbbfc12a class="margin-0">phoneNumber</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3c5d7210-9df8-11ec-afe5-55c2aa6d0440 class="margin-0">business_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#f2783d2a-e747-4dce-bacd-afad337fc159 class="margin-5">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#36b05f0b-d7de-4a3b-9c53-1286a559cbd9 class="margin-5">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8f31cc6d-6b38-415f-b3f4-05a60906eb39 class="margin-5">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8ac10954-b0fe-4f7e-8024-8f10c0e56e2e class="margin-5">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8673c0e2-894f-40b1-ab14-b21d4ec2ba85 class="margin-5">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#1220765a-7bd9-4fbe-bb99-608ddd423dca class="margin-5">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#4445c459-a91f-418c-9a59-f771b5cc2858 class="margin-0">full_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7107ebf0-dc5b-11e9-b819-e3f2d5171928 class="margin-5">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#760da090-dc5b-11e9-b819-e3f2d5171928 class="margin-5">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7bfbe070-dc5b-11e9-b819-e3f2d5171928 class="margin-5">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7ee803e0-dc5b-11e9-b819-e3f2d5171928 class="margin-5">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#85787730-dc5b-11e9-b819-e3f2d5171928 class="margin-5">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#87afc990-dc5b-11e9-b819-e3f2d5171928 class="margin-5">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead2-2b24-11e6-b7e5-591297143e36 class="margin-0">attributes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead3-2b24-11e6-b7e5-591297143e36 class="margin-5">Accepts&nbsp;Credit&nbsp;Cards</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead4-2b24-11e6-b7e5-591297143e36 class="margin-5">Accepts&nbsp;Insurance</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead5-2b24-11e6-b7e5-591297143e36 class="margin-5">Alcohol</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead6-2b24-11e6-b7e5-591297143e36 class="margin-5">Ambience</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead7-2b24-11e6-b7e5-591297143e36 class="margin-10">casual</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead8-2b24-11e6-b7e5-591297143e36 class="margin-10">classy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead9-2b24-11e6-b7e5-591297143e36 class="margin-10">divey</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eada-2b24-11e6-b7e5-591297143e36 class="margin-10">hipster</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadb-2b24-11e6-b7e5-591297143e36 class="margin-10">intimate</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadc-2b24-11e6-b7e5-591297143e36 class="margin-10">romantic</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadd-2b24-11e6-b7e5-591297143e36 class="margin-10">touristy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eade-2b24-11e6-b7e5-591297143e36 class="margin-10">trendy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadf-2b24-11e6-b7e5-591297143e36 class="margin-10">upscale</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae0-2b24-11e6-b7e5-591297143e36 class="margin-5">Attire</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae1-2b24-11e6-b7e5-591297143e36 class="margin-5">By&nbsp;Appointment&nbsp;Only</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae2-2b24-11e6-b7e5-591297143e36 class="margin-5">BYOB/Corkage</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae3-2b24-11e6-b7e5-591297143e36 class="margin-5">Caters</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae4-2b24-11e6-b7e5-591297143e36 class="margin-5">Coat&nbsp;Check</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae5-2b24-11e6-b7e5-591297143e36 class="margin-5">Delivery</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae6-2b24-11e6-b7e5-591297143e36 class="margin-5">Dogs&nbsp;Allowed</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae7-2b24-11e6-b7e5-591297143e36 class="margin-5">Drive-Thru</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae8-2b24-11e6-b7e5-591297143e36 class="margin-5">Good&nbsp;For</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae9-2b24-11e6-b7e5-591297143e36 class="margin-10">breakfast</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaea-2b24-11e6-b7e5-591297143e36 class="margin-10">brunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaeb-2b24-11e6-b7e5-591297143e36 class="margin-10">dessert</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaec-2b24-11e6-b7e5-591297143e36 class="margin-10">dinner</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaed-2b24-11e6-b7e5-591297143e36 class="margin-10">latenight</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaee-2b24-11e6-b7e5-591297143e36 class="margin-10">lunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaef-2b24-11e6-b7e5-591297143e36 class="margin-5">Good&nbsp;For&nbsp;Dancing</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e0-2b24-11e6-b7e5-591297143e36 class="margin-5">Good&nbsp;For&nbsp;Groups</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e1-2b24-11e6-b7e5-591297143e36 class="margin-5">Good&nbsp;for&nbsp;Kids</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e2-2b24-11e6-b7e5-591297143e36 class="margin-5">Happy&nbsp;Hour</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e3-2b24-11e6-b7e5-591297143e36 class="margin-5">Has&nbsp;TV</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e4-2b24-11e6-b7e5-591297143e36 class="margin-5">Music</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e5-2b24-11e6-b7e5-591297143e36 class="margin-10">background_music</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e6-2b24-11e6-b7e5-591297143e36 class="margin-10">dj</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e7-2b24-11e6-b7e5-591297143e36 class="margin-10">jukebox</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e8-2b24-11e6-b7e5-591297143e36 class="margin-10">karaoke</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e9-2b24-11e6-b7e5-591297143e36 class="margin-10">live</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ea-2b24-11e6-b7e5-591297143e36 class="margin-10">video</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811eb-2b24-11e6-b7e5-591297143e36 class="margin-5">Noise&nbsp;Level</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ec-2b24-11e6-b7e5-591297143e36 class="margin-5">Open&nbsp;24&nbsp;Hours</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ed-2b24-11e6-b7e5-591297143e36 class="margin-5">Order&nbsp;at&nbsp;Counter</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ee-2b24-11e6-b7e5-591297143e36 class="margin-5">Outdoor&nbsp;Seating</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ef-2b24-11e6-b7e5-591297143e36 class="margin-5">Parking</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f0-2b24-11e6-b7e5-591297143e36 class="margin-10">garage</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f1-2b24-11e6-b7e5-591297143e36 class="margin-10">lot</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f2-2b24-11e6-b7e5-591297143e36 class="margin-10">street</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f3-2b24-11e6-b7e5-591297143e36 class="margin-10">valet</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f4-2b24-11e6-b7e5-591297143e36 class="margin-10">validated</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f5-2b24-11e6-b7e5-591297143e36 class="margin-5">Price&nbsp;Range</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f6-2b24-11e6-b7e5-591297143e36 class="margin-5">Smoking</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f7-2b24-11e6-b7e5-591297143e36 class="margin-5">Take-out</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f8-2b24-11e6-b7e5-591297143e36 class="margin-5">Takes&nbsp;Reservations</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f9-2b24-11e6-b7e5-591297143e36 class="margin-5">Waiter&nbsp;Service</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fa-2b24-11e6-b7e5-591297143e36 class="margin-5">Wheelchair&nbsp;Accessible</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fb-2b24-11e6-b7e5-591297143e36 class="margin-5">Wi-Fi</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fd-2b24-11e6-b7e5-591297143e36 class="margin-0">categories</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fe-2b24-11e6-b7e5-591297143e36 class="margin-5">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81201-2b24-11e6-b7e5-591297143e36 class="margin-0">hours</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81202-2b24-11e6-b7e5-591297143e36 class="margin-5">Friday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81203-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81204-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81205-2b24-11e6-b7e5-591297143e36 class="margin-5">Monday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81206-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81207-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81208-2b24-11e6-b7e5-591297143e36 class="margin-5">Saturday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81209-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120a-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120b-2b24-11e6-b7e5-591297143e36 class="margin-5">Sunday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120c-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120d-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120e-2b24-11e6-b7e5-591297143e36 class="margin-5">Thursday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120f-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81210-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81211-2b24-11e6-b7e5-591297143e36 class="margin-5">Tuesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81212-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81213-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81214-2b24-11e6-b7e5-591297143e36 class="margin-5">Wednesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81215-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81216-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81217-2b24-11e6-b7e5-591297143e36 class="margin-0">latitude</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81218-2b24-11e6-b7e5-591297143e36 class="margin-0">longitude</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121a-2b24-11e6-b7e5-591297143e36 class="margin-0">neighborhoods</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121b-2b24-11e6-b7e5-591297143e36 class="margin-5">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121c-2b24-11e6-b7e5-591297143e36 class="margin-0">open</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121d-2b24-11e6-b7e5-591297143e36 class="margin-0">review_count</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121e-2b24-11e6-b7e5-591297143e36 class="margin-0">stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81220-2b24-11e6-b7e5-591297143e36 class="margin-0">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0dd811fc-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.1 Field **business\_id**

###### 3.1.2.1.3.1.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Description</td><td><div class="docs-markdown"><p>Unique key for businesses</p></div></td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr><tr><td>Comments</td><td><div class="docs-markdown"><p>Sat Nov 04 2017 10:12:00 GMT+0100 (Romance Standard Time): some comments</p></div></td></tr></tbody></table>

### <a id="0dd81219-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.2 Field **name**

###### 3.1.2.1.3.2.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.company.name()</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="06399180-d360-11ec-adc4-432dcbbfc12a"></a>

###### 3.1.2.1.3.3 Field **phoneNumber**

###### 3.1.2.1.3.3.1 **phoneNumber** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>phoneNumber</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Faker function</td><td>faker.phone.number()</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="3c5d7210-9df8-11ec-afe5-55c2aa6d0440"></a>

###### 3.1.2.1.3.4 Field **business\_address**

###### 3.1.2.1.3.4.1 **business\_address** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image7.png?raw=true)

###### 3.1.2.1.3.4.2 **business\_address** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#f2783d2a-e747-4dce-bacd-afad337fc159 class="margin-NaN">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#36b05f0b-d7de-4a3b-9c53-1286a559cbd9 class="margin-NaN">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8f31cc6d-6b38-415f-b3f4-05a60906eb39 class="margin-NaN">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8ac10954-b0fe-4f7e-8024-8f10c0e56e2e class="margin-NaN">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8673c0e2-894f-40b1-ab14-b21d4ec2ba85 class="margin-NaN">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#1220765a-7bd9-4fbe-bb99-608ddd423dca class="margin-NaN">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.4.3 **business\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_address</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="f2783d2a-e747-4dce-bacd-afad337fc159"></a>

###### 3.1.2.1.3.5 Field **houseNum**

###### 3.1.2.1.3.5.1 **houseNum** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>houseNum</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.buildingNumber()</td></tr><tr><td>Sample</td><td>123</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="36b05f0b-d7de-4a3b-9c53-1286a559cbd9"></a>

###### 3.1.2.1.3.6 Field **street**

###### 3.1.2.1.3.6.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.street()</td></tr><tr><td>Sample</td><td>Main Street</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="8f31cc6d-6b38-415f-b3f4-05a60906eb39"></a>

###### 3.1.2.1.3.7 Field **box**

###### 3.1.2.1.3.7.1 **box** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>box</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.secondaryAddress()</td></tr><tr><td>Sample</td><td>10</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="8ac10954-b0fe-4f7e-8024-8f10c0e56e2e"></a>

###### 3.1.2.1.3.8 Field **city**

###### 3.1.2.1.3.8.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.city()</td></tr><tr><td>Sample</td><td>Anytown</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="8673c0e2-894f-40b1-ab14-b21d4ec2ba85"></a>

###### 3.1.2.1.3.9 Field **state**

###### 3.1.2.1.3.9.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.state({ abbreviated: true })</td></tr><tr><td>Sample</td><td>CA</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="1220765a-7bd9-4fbe-bb99-608ddd423dca"></a>

###### 3.1.2.1.3.10 Field **zip**

###### 3.1.2.1.3.10.1 **zip** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>zip</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.state({ abbreviated: true })</td></tr><tr><td>Sample</td><td>12345</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="4445c459-a91f-418c-9a59-f771b5cc2858"></a>

###### 3.1.2.1.3.11 Field **full\_address**

###### 3.1.2.1.3.11.1 **full\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>full_address</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>model</td></tr></tbody></table>

### <a id="0dd7ead2-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.12 Field **attributes**

###### 3.1.2.1.3.12.1 **attributes** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image8.png?raw=true)

###### 3.1.2.1.3.12.2 **attributes** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd7ead3-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Accepts&nbsp;Credit&nbsp;Cards</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead4-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Accepts&nbsp;Insurance</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead5-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Alcohol</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead6-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Ambience</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae0-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Attire</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae1-2b24-11e6-b7e5-591297143e36 class="margin-NaN">By&nbsp;Appointment&nbsp;Only</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae2-2b24-11e6-b7e5-591297143e36 class="margin-NaN">BYOB/Corkage</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae3-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Caters</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae4-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Coat&nbsp;Check</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae5-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Delivery</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae6-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Dogs&nbsp;Allowed</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae7-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Drive-Thru</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae8-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Good&nbsp;For</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaef-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Good&nbsp;For&nbsp;Dancing</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e0-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Good&nbsp;For&nbsp;Groups</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e1-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Good&nbsp;for&nbsp;Kids</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e2-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Happy&nbsp;Hour</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e3-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Has&nbsp;TV</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e4-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Music</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811eb-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Noise&nbsp;Level</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ec-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Open&nbsp;24&nbsp;Hours</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ed-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Order&nbsp;at&nbsp;Counter</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ee-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Outdoor&nbsp;Seating</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ef-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Parking</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f5-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Price&nbsp;Range</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f6-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Smoking</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f7-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Take-out</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f8-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Takes&nbsp;Reservations</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f9-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Waiter&nbsp;Service</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fa-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Wheelchair&nbsp;Accessible</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fb-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Wi-Fi</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.12.3 **attributes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>attributes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd7ead3-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.13 Field **Accepts Credit Cards**

###### 3.1.2.1.3.13.1 **Accepts Credit Cards** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Accepts Credit Cards</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead4-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.14 Field **Accepts Insurance**

###### 3.1.2.1.3.14.1 **Accepts Insurance** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Accepts Insurance</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead5-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.15 Field **Alcohol**

###### 3.1.2.1.3.15.1 **Alcohol** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Alcohol</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>Full bar</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd7ead6-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.16 Field **Ambience**

###### 3.1.2.1.3.16.1 **Ambience** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image9.png?raw=true)

###### 3.1.2.1.3.16.2 **Ambience** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd7ead7-2b24-11e6-b7e5-591297143e36 class="margin-NaN">casual</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead8-2b24-11e6-b7e5-591297143e36 class="margin-NaN">classy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead9-2b24-11e6-b7e5-591297143e36 class="margin-NaN">divey</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eada-2b24-11e6-b7e5-591297143e36 class="margin-NaN">hipster</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadb-2b24-11e6-b7e5-591297143e36 class="margin-NaN">intimate</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadc-2b24-11e6-b7e5-591297143e36 class="margin-NaN">romantic</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadd-2b24-11e6-b7e5-591297143e36 class="margin-NaN">touristy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eade-2b24-11e6-b7e5-591297143e36 class="margin-NaN">trendy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadf-2b24-11e6-b7e5-591297143e36 class="margin-NaN">upscale</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.16.3 **Ambience** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Ambience</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd7ead7-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.17 Field **casual**

###### 3.1.2.1.3.17.1 **casual** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>casual</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead8-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.18 Field **classy**

###### 3.1.2.1.3.18.1 **classy** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>classy</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead9-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.19 Field **divey**

###### 3.1.2.1.3.19.1 **divey** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>divey</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eada-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.20 Field **hipster**

###### 3.1.2.1.3.20.1 **hipster** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>hipster</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadb-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.21 Field **intimate**

###### 3.1.2.1.3.21.1 **intimate** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>intimate</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadc-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.22 Field **romantic**

###### 3.1.2.1.3.22.1 **romantic** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>romantic</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadd-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.23 Field **touristy**

###### 3.1.2.1.3.23.1 **touristy** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>touristy</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eade-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.24 Field **trendy**

###### 3.1.2.1.3.24.1 **trendy** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>trendy</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadf-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.25 Field **upscale**

###### 3.1.2.1.3.25.1 **upscale** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>upscale</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae0-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.26 Field **Attire**

###### 3.1.2.1.3.26.1 **Attire** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Attire</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>Casual chic</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd7eae1-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.27 Field **By Appointment Only**

###### 3.1.2.1.3.27.1 **By Appointment Only** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>By Appointment Only</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae2-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.28 Field **BYOB/Corkage**

###### 3.1.2.1.3.28.1 **BYOB/Corkage** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>BYOB/Corkage</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd7eae3-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.29 Field **Caters**

###### 3.1.2.1.3.29.1 **Caters** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Caters</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae4-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.30 Field **Coat Check**

###### 3.1.2.1.3.30.1 **Coat Check** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Coat Check</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae5-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.31 Field **Delivery**

###### 3.1.2.1.3.31.1 **Delivery** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Delivery</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae6-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.32 Field **Dogs Allowed**

###### 3.1.2.1.3.32.1 **Dogs Allowed** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Dogs Allowed</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae7-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.33 Field **Drive-Thru**

###### 3.1.2.1.3.33.1 **Drive-Thru** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Drive-Thru</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae8-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.34 Field **Good For**

###### 3.1.2.1.3.34.1 **Good For** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image10.png?raw=true)

###### 3.1.2.1.3.34.2 **Good For** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd7eae9-2b24-11e6-b7e5-591297143e36 class="margin-NaN">breakfast</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaea-2b24-11e6-b7e5-591297143e36 class="margin-NaN">brunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaeb-2b24-11e6-b7e5-591297143e36 class="margin-NaN">dessert</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaec-2b24-11e6-b7e5-591297143e36 class="margin-NaN">dinner</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaed-2b24-11e6-b7e5-591297143e36 class="margin-NaN">latenight</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaee-2b24-11e6-b7e5-591297143e36 class="margin-NaN">lunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.34.3 **Good For** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good For</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd7eae9-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.35 Field **breakfast**

###### 3.1.2.1.3.35.1 **breakfast** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>breakfast</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaea-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.36 Field **brunch**

###### 3.1.2.1.3.36.1 **brunch** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>brunch</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaeb-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.37 Field **dessert**

###### 3.1.2.1.3.37.1 **dessert** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>dessert</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaec-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.38 Field **dinner**

###### 3.1.2.1.3.38.1 **dinner** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>dinner</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaed-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.39 Field **latenight**

###### 3.1.2.1.3.39.1 **latenight** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>latenight</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaee-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.40 Field **lunch**

###### 3.1.2.1.3.40.1 **lunch** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>lunch</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaef-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.41 Field **Good For Dancing**

###### 3.1.2.1.3.41.1 **Good For Dancing** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good For Dancing</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e0-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.42 Field **Good For Groups**

###### 3.1.2.1.3.42.1 **Good For Groups** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good For Groups</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e1-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.43 Field **Good for Kids**

###### 3.1.2.1.3.43.1 **Good for Kids** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good for Kids</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e2-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.44 Field **Happy Hour**

###### 3.1.2.1.3.44.1 **Happy Hour** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Happy Hour</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e3-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.45 Field **Has TV**

###### 3.1.2.1.3.45.1 **Has TV** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Has TV</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e4-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.46 Field **Music**

###### 3.1.2.1.3.46.1 **Music** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image11.png?raw=true)

###### 3.1.2.1.3.46.2 **Music** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811e5-2b24-11e6-b7e5-591297143e36 class="margin-NaN">background_music</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e6-2b24-11e6-b7e5-591297143e36 class="margin-NaN">dj</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e7-2b24-11e6-b7e5-591297143e36 class="margin-NaN">jukebox</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e8-2b24-11e6-b7e5-591297143e36 class="margin-NaN">karaoke</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e9-2b24-11e6-b7e5-591297143e36 class="margin-NaN">live</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ea-2b24-11e6-b7e5-591297143e36 class="margin-NaN">video</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.46.3 **Music** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Music</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd811e5-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.47 Field **background\_music**

###### 3.1.2.1.3.47.1 **background\_music** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>background_music</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e6-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.48 Field **dj**

###### 3.1.2.1.3.48.1 **dj** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>dj</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e7-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.49 Field **jukebox**

###### 3.1.2.1.3.49.1 **jukebox** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>jukebox</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e8-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.50 Field **karaoke**

###### 3.1.2.1.3.50.1 **karaoke** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>karaoke</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e9-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.51 Field **live**

###### 3.1.2.1.3.51.1 **live** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>live</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ea-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.52 Field **video**

###### 3.1.2.1.3.52.1 **video** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>video</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811eb-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.53 Field **Noise Level**

###### 3.1.2.1.3.53.1 **Noise Level** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Noise Level</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd811ec-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.54 Field **Open 24 Hours**

###### 3.1.2.1.3.54.1 **Open 24 Hours** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Open 24 Hours</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ed-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.55 Field **Order at Counter**

###### 3.1.2.1.3.55.1 **Order at Counter** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Order at Counter</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ee-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.56 Field **Outdoor Seating**

###### 3.1.2.1.3.56.1 **Outdoor Seating** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Outdoor Seating</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ef-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.57 Field **Parking**

###### 3.1.2.1.3.57.1 **Parking** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image12.png?raw=true)

###### 3.1.2.1.3.57.2 **Parking** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811f0-2b24-11e6-b7e5-591297143e36 class="margin-NaN">garage</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f1-2b24-11e6-b7e5-591297143e36 class="margin-NaN">lot</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f2-2b24-11e6-b7e5-591297143e36 class="margin-NaN">street</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f3-2b24-11e6-b7e5-591297143e36 class="margin-NaN">valet</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f4-2b24-11e6-b7e5-591297143e36 class="margin-NaN">validated</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.57.3 **Parking** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Parking</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd811f0-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.58 Field **garage**

###### 3.1.2.1.3.58.1 **garage** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>garage</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f1-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.59 Field **lot**

###### 3.1.2.1.3.59.1 **lot** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>lot</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f2-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.60 Field **street**

###### 3.1.2.1.3.60.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f3-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.61 Field **valet**

###### 3.1.2.1.3.61.1 **valet** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>valet</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f4-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.62 Field **validated**

###### 3.1.2.1.3.62.1 **validated** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>validated</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f5-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.63 Field **Price Range**

###### 3.1.2.1.3.63.1 **Price Range** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Price Range</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f6-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.64 Field **Smoking**

###### 3.1.2.1.3.64.1 **Smoking** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Smoking</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd811f7-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.65 Field **Take-out**

###### 3.1.2.1.3.65.1 **Take-out** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Take-out</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f8-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.66 Field **Takes Reservations**

###### 3.1.2.1.3.66.1 **Takes Reservations** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Takes Reservations</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f9-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.67 Field **Waiter Service**

###### 3.1.2.1.3.67.1 **Waiter Service** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Waiter Service</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811fa-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.68 Field **Wheelchair Accessible**

###### 3.1.2.1.3.68.1 **Wheelchair Accessible** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Wheelchair Accessible</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811fb-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.69 Field **Wi-Fi**

###### 3.1.2.1.3.69.1 **Wi-Fi** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Wi-Fi</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd811fd-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.70 Field **categories**

###### 3.1.2.1.3.70.1 **categories** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image13.png?raw=true)

###### 3.1.2.1.3.70.2 **categories** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811fe-2b24-11e6-b7e5-591297143e36 class="margin-NaN">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.70.3 **categories** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>categories</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811fe-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.71 Field **\[0\]**

###### 3.1.2.1.3.71.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81201-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.72 Field **hours**

###### 3.1.2.1.3.72.1 **hours** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image14.png?raw=true)

###### 3.1.2.1.3.72.2 **hours** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81202-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Friday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81205-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Monday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81208-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Saturday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120b-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Sunday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120e-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Thursday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81211-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Tuesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81214-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Wednesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.72.3 **hours** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>hours</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81202-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.73 Field **Friday**

###### 3.1.2.1.3.73.1 **Friday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image15.png?raw=true)

###### 3.1.2.1.3.73.2 **Friday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81203-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81204-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.73.3 **Friday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Friday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81203-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.74 Field **close**

###### 3.1.2.1.3.74.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81204-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.75 Field **open**

###### 3.1.2.1.3.75.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81205-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.76 Field **Monday**

###### 3.1.2.1.3.76.1 **Monday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image16.png?raw=true)

###### 3.1.2.1.3.76.2 **Monday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81206-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81207-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.76.3 **Monday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Monday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81206-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.77 Field **close**

###### 3.1.2.1.3.77.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81207-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.78 Field **open**

###### 3.1.2.1.3.78.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81208-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.79 Field **Saturday**

###### 3.1.2.1.3.79.1 **Saturday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image17.png?raw=true)

###### 3.1.2.1.3.79.2 **Saturday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81209-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120a-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.79.3 **Saturday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Saturday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81209-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.80 Field **close**

###### 3.1.2.1.3.80.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd8120a-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.81 Field **open**

###### 3.1.2.1.3.81.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd8120b-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.82 Field **Sunday**

###### 3.1.2.1.3.82.1 **Sunday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image18.png?raw=true)

###### 3.1.2.1.3.82.2 **Sunday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd8120c-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120d-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.82.3 **Sunday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Sunday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd8120c-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.83 Field **close**

###### 3.1.2.1.3.83.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd8120d-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.84 Field **open**

###### 3.1.2.1.3.84.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd8120e-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.85 Field **Thursday**

###### 3.1.2.1.3.85.1 **Thursday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image19.png?raw=true)

###### 3.1.2.1.3.85.2 **Thursday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd8120f-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81210-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.85.3 **Thursday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Thursday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd8120f-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.86 Field **close**

###### 3.1.2.1.3.86.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81210-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.87 Field **open**

###### 3.1.2.1.3.87.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81211-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.88 Field **Tuesday**

###### 3.1.2.1.3.88.1 **Tuesday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image20.png?raw=true)

###### 3.1.2.1.3.88.2 **Tuesday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81212-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81213-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.88.3 **Tuesday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Tuesday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81212-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.89 Field **close**

###### 3.1.2.1.3.89.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81213-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.90 Field **open**

###### 3.1.2.1.3.90.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81214-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.91 Field **Wednesday**

###### 3.1.2.1.3.91.1 **Wednesday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image21.png?raw=true)

###### 3.1.2.1.3.91.2 **Wednesday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81215-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81216-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.91.3 **Wednesday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Wednesday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81215-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.92 Field **close**

###### 3.1.2.1.3.92.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81216-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.93 Field **open**

###### 3.1.2.1.3.93.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81217-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.94 Field **latitude**

###### 3.1.2.1.3.94.1 **latitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>latitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81218-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.95 Field **longitude**

###### 3.1.2.1.3.95.1 **longitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>longitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121a-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.96 Field **neighborhoods**

###### 3.1.2.1.3.96.1 **neighborhoods** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image22.png?raw=true)

###### 3.1.2.1.3.96.2 **neighborhoods** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd8121b-2b24-11e6-b7e5-591297143e36 class="margin-NaN">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.1.3.96.3 **neighborhoods** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>neighborhoods</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121b-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.97 Field **\[0\]**

###### 3.1.2.1.3.97.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd8121c-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.98 Field **open**

###### 3.1.2.1.3.98.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121d-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.99 Field **review\_count**

###### 3.1.2.1.3.99.1 **review\_count** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_count</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0dd8121e-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.100 Field **stars**

###### 3.1.2.1.3.100.1 **stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>stars</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0dd81220-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.1.3.101 Field **type**

###### 3.1.2.1.3.101.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

###### 3.1.2.1.4 **businesses** Indexes

<table class="index-table"><thead><tr><td class="table-property-column">Property</td><td class="table-column-property">idx_address</td><td class="table-column-property">idx_city</td></tr></thead><tbody><tr><td>Name</td><td class="table-column-indexes">idx_address</td><td class="table-column-indexes">idx_city</td></tr><tr><td>Activated</td><td class="table-column-indexes">true</td><td class="table-column-indexes">true</td></tr><tr><td>Key</td><td class="table-column-indexes">business_address('ascending')</td><td class="table-column-indexes">city('ascending')</td></tr><tr><td>Unique</td><td class="table-column-indexes">false</td><td class="table-column-indexes">false</td></tr><tr><td>Drop duplicates</td><td class="table-column-indexes">false</td><td class="table-column-indexes">false</td></tr><tr><td>Sparse</td><td class="table-column-indexes">false</td><td class="table-column-indexes">false</td></tr><tr><td>Background indexing</td><td class="table-column-indexes">false</td><td class="table-column-indexes">false</td></tr><tr><td>Storage engine</td><td class="table-column-indexes">WiredTiger</td><td class="table-column-indexes">WiredTiger</td></tr></tbody></table>

###### 3.1.2.1.5 **businesses** Target Script

```
use yelp;

db.createCollection("businesses", {
    "capped": false,
    "validator": {
        "$jsonSchema": {
            "bsonType": "object",
            "title": "businesses",
            "description": "Checking Markdown inline image in description for Hub\n\n![Inline image](https://hackolade.com/img/data-metadata.png)",
            "properties": {
                "_id": {
                    "bsonType": "objectId"
                },
                "business_id": {
                    "bsonType": "objectId",
                    "description": "Unique key for businesses"
                },
                "name": {
                    "bsonType": "string"
                },
                "phoneNumber": {
                    "bsonType": "string"
                },
                "business_address": {
                    "bsonType": "object",
                    "properties": {
                        "houseNum": {
                            "bsonType": "string"
                        },
                        "street": {
                            "bsonType": "string"
                        },
                        "box": {
                            "bsonType": "string"
                        },
                        "city": {
                            "bsonType": "string"
                        },
                        "state": {
                            "bsonType": "string"
                        },
                        "zip": {
                            "bsonType": "string"
                        }
                    },
                    "additionalProperties": false
                },
                "full_address": {
                    "bsonType": "object",
                    "properties": {
                        "houseNum": {
                            "bsonType": "string"
                        },
                        "street": {
                            "bsonType": "string"
                        },
                        "box": {
                            "bsonType": "string"
                        },
                        "city": {
                            "bsonType": "string"
                        },
                        "state": {
                            "bsonType": "string"
                        },
                        "zip": {
                            "bsonType": "string"
                        }
                    },
                    "additionalProperties": false
                },
                "attributes": {
                    "bsonType": "object",
                    "properties": {
                        "Accepts Credit Cards": {
                            "bsonType": "bool"
                        },
                        "Accepts Insurance": {
                            "bsonType": "bool"
                        },
                        "Alcohol": {
                            "bsonType": "string"
                        },
                        "Ambience": {
                            "bsonType": "object",
                            "properties": {
                                "casual": {
                                    "bsonType": "bool"
                                },
                                "classy": {
                                    "bsonType": "bool"
                                },
                                "divey": {
                                    "bsonType": "bool"
                                },
                                "hipster": {
                                    "bsonType": "bool"
                                },
                                "intimate": {
                                    "bsonType": "bool"
                                },
                                "romantic": {
                                    "bsonType": "bool"
                                },
                                "touristy": {
                                    "bsonType": "bool"
                                },
                                "trendy": {
                                    "bsonType": "bool"
                                },
                                "upscale": {
                                    "bsonType": "bool"
                                }
                            },
                            "additionalProperties": true
                        },
                        "Attire": {
                            "bsonType": "string"
                        },
                        "By Appointment Only": {
                            "bsonType": "bool"
                        },
                        "BYOB/Corkage": {
                            "bsonType": "string"
                        },
                        "Caters": {
                            "bsonType": "bool"
                        },
                        "Coat Check": {
                            "bsonType": "bool"
                        },
                        "Delivery": {
                            "bsonType": "bool"
                        },
                        "Dogs Allowed": {
                            "bsonType": "bool"
                        },
                        "Drive-Thru": {
                            "bsonType": "bool"
                        },
                        "Good For": {
                            "bsonType": "object",
                            "properties": {
                                "breakfast": {
                                    "bsonType": "bool"
                                },
                                "brunch": {
                                    "bsonType": "bool"
                                },
                                "dessert": {
                                    "bsonType": "bool"
                                },
                                "dinner": {
                                    "bsonType": "bool"
                                },
                                "latenight": {
                                    "bsonType": "bool"
                                },
                                "lunch": {
                                    "bsonType": "bool"
                                }
                            },
                            "additionalProperties": true
                        },
                        "Good For Dancing": {
                            "bsonType": "bool"
                        },
                        "Good For Groups": {
                            "bsonType": "bool"
                        },
                        "Good for Kids": {
                            "bsonType": "bool"
                        },
                        "Happy Hour": {
                            "bsonType": "bool"
                        },
                        "Has TV": {
                            "bsonType": "bool"
                        },
                        "Music": {
                            "bsonType": "object",
                            "properties": {
                                "background_music": {
                                    "bsonType": "bool"
                                },
                                "dj": {
                                    "bsonType": "bool"
                                },
                                "jukebox": {
                                    "bsonType": "bool"
                                },
                                "karaoke": {
                                    "bsonType": "bool"
                                },
                                "live": {
                                    "bsonType": "bool"
                                },
                                "video": {
                                    "bsonType": "bool"
                                }
                            },
                            "additionalProperties": true
                        },
                        "Noise Level": {
                            "bsonType": "string"
                        },
                        "Open 24 Hours": {
                            "bsonType": "bool"
                        },
                        "Order at Counter": {
                            "bsonType": "bool"
                        },
                        "Outdoor Seating": {
                            "bsonType": "bool"
                        },
                        "Parking": {
                            "bsonType": "object",
                            "properties": {
                                "garage": {
                                    "bsonType": "bool"
                                },
                                "lot": {
                                    "bsonType": "bool"
                                },
                                "street": {
                                    "bsonType": "bool"
                                },
                                "valet": {
                                    "bsonType": "bool"
                                },
                                "validated": {
                                    "bsonType": "bool"
                                }
                            },
                            "additionalProperties": true
                        },
                        "Price Range": {
                            "bsonType": "number"
                        },
                        "Smoking": {
                            "bsonType": "string"
                        },
                        "Take-out": {
                            "bsonType": "bool"
                        },
                        "Takes Reservations": {
                            "bsonType": "bool"
                        },
                        "Waiter Service": {
                            "bsonType": "bool"
                        },
                        "Wheelchair Accessible": {
                            "bsonType": "bool"
                        },
                        "Wi-Fi": {
                            "bsonType": "string"
                        }
                    },
                    "additionalProperties": true
                },
                "categories": {
                    "bsonType": "array",
                    "items": {
                        "bsonType": "string"
                    }
                },
                "hours": {
                    "bsonType": "object",
                    "properties": {
                        "Friday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            },
                            "additionalProperties": true
                        },
                        "Monday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            },
                            "additionalProperties": true
                        },
                        "Saturday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            },
                            "additionalProperties": true
                        },
                        "Sunday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            },
                            "additionalProperties": true
                        },
                        "Thursday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            },
                            "additionalProperties": true
                        },
                        "Tuesday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            },
                            "additionalProperties": true
                        },
                        "Wednesday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            },
                            "additionalProperties": true
                        }
                    },
                    "additionalProperties": true
                },
                "latitude": {
                    "bsonType": "number"
                },
                "longitude": {
                    "bsonType": "number"
                },
                "neighborhoods": {
                    "bsonType": "array",
                    "items": {
                        "bsonType": "string"
                    }
                },
                "open": {
                    "bsonType": "bool"
                },
                "review_count": {
                    "bsonType": "number",
                    "minimum": 0
                },
                "stars": {
                    "bsonType": "number",
                    "maximum": 5,
                    "minimum": 1
                },
                "type": {
                    "bsonType": "string"
                }
            },
            "additionalProperties": true,
            "required": [
                "business_id"
            ]
        }
    },
    "validationLevel": "off",
    "validationAction": "warn",
    "collation": {
        "alternate": "non-ignorable",
        "backwards": false,
        "caseFirst": "off",
        "caseLevel": false,
        "locale": "af",
        "maxVariable": "Null",
        "normalization": false,
        "numericOrdering": false,
        "strength": 1
    }
});

db.businesses.createIndex({
    "business_address": 1
},
{
    "name": "idx_address"
});

db.businesses.createIndex({
    "business_address.city": 1
},
{
    "name": "idx_city"
});
```

### <a id="0da2aa00-2b24-11e6-b7e5-591297143e36"></a>

##### 3.1.2.2 Collection **reviews**

###### 3.1.2.2.1 **reviews** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image23.png?raw=true)

###### 3.1.2.2.2 **reviews** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>reviews</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>Storage engine</td><td>WiredTiger</td></tr><tr><td>Validation level</td><td>Off</td></tr><tr><td>Validation action</td><td>Warn</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

###### 3.1.2.2.3 **reviews** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0da2aa04-2b24-11e6-b7e5-591297143e36 class="margin-0">review_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>pk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa02-2b24-11e6-b7e5-591297143e36 class="margin-0">business_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>fk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa03-2b24-11e6-b7e5-591297143e36 class="margin-0">date</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa05-2b24-11e6-b7e5-591297143e36 class="margin-0">stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa06-2b24-11e6-b7e5-591297143e36 class="margin-0">text</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa07-2b24-11e6-b7e5-591297143e36 class="margin-0">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa08-2b24-11e6-b7e5-591297143e36 class="margin-0">user_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>fk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa09-2b24-11e6-b7e5-591297143e36 class="margin-0">votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0a-2b24-11e6-b7e5-591297143e36 class="margin-5">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0b-2b24-11e6-b7e5-591297143e36 class="margin-5">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0c-2b24-11e6-b7e5-591297143e36 class="margin-5">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0da2aa04-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.2.3.1 Field **review\_id**

###### 3.1.2.2.3.1.1 **review\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="0da2aa02-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.2.3.2 Field **business\_id**

###### 3.1.2.2.3.2.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Foreign collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Foreign field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

### <a id="0da2aa03-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.2.3.3 Field **date**

###### 3.1.2.2.3.3.1 **date** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>date</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.date.past()</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0da2aa05-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.2.3.4 Field **stars**

###### 3.1.2.2.3.4.1 **stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>stars</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0da2aa06-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.2.3.5 Field **text**

###### 3.1.2.2.3.5.1 **text** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>text</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.lorem.paragraphs(3)</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0da2aa07-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.2.3.6 Field **type**

###### 3.1.2.2.3.6.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0da2aa08-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.2.3.7 Field **user\_id**

###### 3.1.2.2.3.7.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Foreign collection</td><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td></tr><tr><td>Foreign field</td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>User Identifier</a></td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

### <a id="0da2aa09-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.2.3.8 Field **votes**

###### 3.1.2.2.3.8.1 **votes** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image24.png?raw=true)

###### 3.1.2.2.3.8.2 **votes** Hierarchy

Parent field: **reviews**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0da2aa0a-2b24-11e6-b7e5-591297143e36 class="margin-NaN">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0b-2b24-11e6-b7e5-591297143e36 class="margin-NaN">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0c-2b24-11e6-b7e5-591297143e36 class="margin-NaN">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.2.3.8.3 **votes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>votes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0da2aa0a-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.2.3.9 Field **cool**

###### 3.1.2.2.3.9.1 **cool** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cool</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0da2aa0b-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.2.3.10 Field **funny**

###### 3.1.2.2.3.10.1 **funny** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>funny</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0da2aa0c-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.2.3.11 Field **useful**

###### 3.1.2.2.3.11.1 **useful** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>useful</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

###### 3.1.2.2.4 **reviews** Target Script

```
use yelp;

db.createCollection("reviews", {
    "capped": false,
    "validator": {
        "$jsonSchema": {
            "bsonType": "object",
            "title": "reviews",
            "properties": {
                "_id": {
                    "bsonType": "objectId"
                },
                "review_id": {
                    "bsonType": "objectId"
                },
                "business_id": {
                    "bsonType": "objectId"
                },
                "date": {
                    "bsonType": "string"
                },
                "stars": {
                    "bsonType": "number",
                    "maximum": 5,
                    "minimum": 1
                },
                "text": {
                    "bsonType": "string"
                },
                "type": {
                    "bsonType": "string"
                },
                "user_id": {
                    "bsonType": "objectId"
                },
                "votes": {
                    "bsonType": "object",
                    "properties": {
                        "cool": {
                            "bsonType": "number",
                            "minimum": 0
                        },
                        "funny": {
                            "bsonType": "number",
                            "minimum": 0
                        },
                        "useful": {
                            "bsonType": "number",
                            "minimum": 0
                        }
                    },
                    "additionalProperties": true
                }
            },
            "additionalProperties": true,
            "required": [
                "review_id",
                "business_id",
                "user_id"
            ]
        }
    },
    "validationLevel": "off",
    "validationAction": "warn",
    "collation": {
        "alternate": "non-ignorable",
        "backwards": false,
        "caseFirst": "off",
        "caseLevel": false,
        "locale": "af",
        "maxVariable": "Null",
        "normalization": false,
        "numericOrdering": false,
        "strength": 1
    }
});
```

### <a id="0de02830-2b24-11e6-b7e5-591297143e36"></a>

##### 3.1.2.3 Collection **tips**

###### 3.1.2.3.1 **tips** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image25.png?raw=true)

###### 3.1.2.3.2 **tips** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>tips</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>Storage engine</td><td>WiredTiger</td></tr><tr><td>Validation level</td><td>Off</td></tr><tr><td>Validation action</td><td>Warn</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

###### 3.1.2.3.3 **tips** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0de02831-2b24-11e6-b7e5-591297143e36 class="margin-0">_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>pk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02832-2b24-11e6-b7e5-591297143e36 class="margin-0">business_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>fk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02833-2b24-11e6-b7e5-591297143e36 class="margin-0">date</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02834-2b24-11e6-b7e5-591297143e36 class="margin-0">likes</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02835-2b24-11e6-b7e5-591297143e36 class="margin-0">text</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02836-2b24-11e6-b7e5-591297143e36 class="margin-0">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02837-2b24-11e6-b7e5-591297143e36 class="margin-0">user_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>fk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0de02831-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.3.3.1 Field **\_id**

###### 3.1.2.3.3.1.1 **\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="0de02832-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.3.3.2 Field **business\_id**

###### 3.1.2.3.3.2.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Foreign collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Foreign field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

### <a id="0de02833-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.3.3.3 Field **date**

###### 3.1.2.3.3.3.1 **date** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>date</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.date.past()</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0de02834-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.3.3.4 Field **likes**

###### 3.1.2.3.3.4.1 **likes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>likes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0de02835-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.3.3.5 Field **text**

###### 3.1.2.3.3.5.1 **text** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>text</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0de02836-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.3.3.6 Field **type**

###### 3.1.2.3.3.6.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0de02837-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.3.3.7 Field **user\_id**

###### 3.1.2.3.3.7.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Foreign collection</td><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td></tr><tr><td>Foreign field</td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>User Identifier</a></td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

###### 3.1.2.3.4 **tips** Target Script

```
use yelp;

db.createCollection("tips", {
    "capped": false,
    "validator": {
        "$jsonSchema": {
            "bsonType": "object",
            "title": "tips",
            "properties": {
                "_id": {
                    "bsonType": "objectId"
                },
                "business_id": {
                    "bsonType": "objectId"
                },
                "date": {
                    "bsonType": "string"
                },
                "likes": {
                    "bsonType": "number"
                },
                "text": {
                    "bsonType": "string"
                },
                "type": {
                    "bsonType": "string"
                },
                "user_id": {
                    "bsonType": "objectId"
                }
            },
            "additionalProperties": true,
            "required": [
                "_id",
                "business_id",
                "user_id"
            ]
        }
    },
    "validationLevel": "off",
    "validationAction": "warn",
    "collation": {
        "alternate": "non-ignorable",
        "backwards": false,
        "caseFirst": "off",
        "caseLevel": false,
        "locale": "af",
        "maxVariable": "Null",
        "normalization": false,
        "numericOrdering": false,
        "strength": 1
    }
});
```

### <a id="0df0f110-2b24-11e6-b7e5-591297143e36"></a>

##### 3.1.2.4 Collection **users**

###### 3.1.2.4.1 **users** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image26.png?raw=true)

###### 3.1.2.4.2 **users** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>users</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Description</td><td><div class="docs-markdown"><p>Users description</p></div></td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>Time series</td><td>false</td></tr><tr><td>Storage engine</td><td>WiredTiger</td></tr><tr><td>Validation level</td><td>Off</td></tr><tr><td>Validation action</td><td>Warn</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

###### 3.1.2.4.3 **users** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36 class="margin-0">User&nbsp;Identifier</a></td><td class="no-break-word">objectId</td><td>true</td><td>pk, dk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f125-2b24-11e6-b7e5-591297143e36 class="margin-0">type</a></td><td class="no-break-word">string</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f123-2b24-11e6-b7e5-591297143e36 class="margin-0">name</a></td><td class="no-break-word">string</td><td>true</td><td></td><td><div class="docs-markdown"><p>First name plus surname</p></div></td><td><div class="docs-markdown"><p>Fri Sep 15 2017 17:31:32 GMT+0200 (Romance Summer Time): MongoDB Demo</p></div></td></tr><tr><td><a href=#0df0f112-2b24-11e6-b7e5-591297143e36 class="margin-0">average_stars</a></td><td class="no-break-word">numeric</td><td>true</td><td></td><td><div class="docs-markdown"><p>Star rating: from 1 to 5.</p></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f113-2b24-11e6-b7e5-591297143e36 class="margin-0">compliments</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f114-2b24-11e6-b7e5-591297143e36 class="margin-5">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f115-2b24-11e6-b7e5-591297143e36 class="margin-5">cute</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f116-2b24-11e6-b7e5-591297143e36 class="margin-5">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f117-2b24-11e6-b7e5-591297143e36 class="margin-5">hot</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f119-2b24-11e6-b7e5-591297143e36 class="margin-5">note</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11a-2b24-11e6-b7e5-591297143e36 class="margin-5">photos</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11b-2b24-11e6-b7e5-591297143e36 class="margin-5">plain</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11c-2b24-11e6-b7e5-591297143e36 class="margin-5">profile</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11d-2b24-11e6-b7e5-591297143e36 class="margin-5">writer</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11e-2b24-11e6-b7e5-591297143e36 class="margin-0">elite</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11f-2b24-11e6-b7e5-591297143e36 class="margin-5">[0]</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f120-2b24-11e6-b7e5-591297143e36 class="margin-0">fans</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f121-2b24-11e6-b7e5-591297143e36 class="margin-0">friends</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f122-2b24-11e6-b7e5-591297143e36 class="margin-5">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f124-2b24-11e6-b7e5-591297143e36 class="margin-0">review_count</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f127-2b24-11e6-b7e5-591297143e36 class="margin-0">votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f128-2b24-11e6-b7e5-591297143e36 class="margin-5">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f129-2b24-11e6-b7e5-591297143e36 class="margin-5">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12a-2b24-11e6-b7e5-591297143e36 class="margin-5">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12b-2b24-11e6-b7e5-591297143e36 class="margin-0">yelping_since</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0df0f126-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.1 Field **User Identifier**

###### 3.1.2.4.3.1.1 **User Identifier** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>User Identifier</td></tr><tr><td>Technical name</td><td>user_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="0df0f125-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.2 Field **type**

###### 3.1.2.4.3.2.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Enum</td><td>user,owner,tester</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0df0f123-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.3 Field **name**

###### 3.1.2.4.3.3.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Description</td><td><div class="docs-markdown"><p>First name plus surname</p></div></td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.helpers.fake('{{person.firstName}} {{person.lastName}}')</td></tr><tr><td>Sample</td><td>John Doe</td></tr><tr><td>Comments</td><td><div class="docs-markdown"><p>Fri Sep 15 2017 17:31:32 GMT+0200 (Romance Summer Time): MongoDB Demo</p></div></td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0df0f112-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.4 Field **average\_stars**

###### 3.1.2.4.3.4.1 **average\_stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>average_stars</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Description</td><td><div class="docs-markdown"><p>Star rating: from 1 to 5.</p></div></td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Unit</td><td>stars</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr><tr><td>Excl max</td><td>false</td></tr><tr><td>Sample</td><td>3</td></tr></tbody></table>

### <a id="0df0f113-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.5 Field **compliments**

###### 3.1.2.4.3.5.1 **compliments** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image27.png?raw=true)

###### 3.1.2.4.3.5.2 **compliments** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f114-2b24-11e6-b7e5-591297143e36 class="margin-NaN">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f115-2b24-11e6-b7e5-591297143e36 class="margin-NaN">cute</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f116-2b24-11e6-b7e5-591297143e36 class="margin-NaN">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f117-2b24-11e6-b7e5-591297143e36 class="margin-NaN">hot</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f119-2b24-11e6-b7e5-591297143e36 class="margin-NaN">note</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11a-2b24-11e6-b7e5-591297143e36 class="margin-NaN">photos</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11b-2b24-11e6-b7e5-591297143e36 class="margin-NaN">plain</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11c-2b24-11e6-b7e5-591297143e36 class="margin-NaN">profile</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11d-2b24-11e6-b7e5-591297143e36 class="margin-NaN">writer</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.4.3.5.3 **compliments** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>compliments</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0df0f114-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.6 Field **cool**

###### 3.1.2.4.3.6.1 **cool** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cool</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f115-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.7 Field **cute**

###### 3.1.2.4.3.7.1 **cute** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cute</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f116-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.8 Field **funny**

###### 3.1.2.4.3.8.1 **funny** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>funny</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f117-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.9 Field **hot**

###### 3.1.2.4.3.9.1 **hot** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>hot</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f119-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.10 Field **note**

###### 3.1.2.4.3.10.1 **note** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>note</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f11a-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.11 Field **photos**

###### 3.1.2.4.3.11.1 **photos** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>photos</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f11b-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.12 Field **plain**

###### 3.1.2.4.3.12.1 **plain** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>plain</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f11c-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.13 Field **profile**

###### 3.1.2.4.3.13.1 **profile** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>profile</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f11d-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.14 Field **writer**

###### 3.1.2.4.3.14.1 **writer** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>writer</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f11e-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.15 Field **elite**

###### 3.1.2.4.3.15.1 **elite** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image28.png?raw=true)

###### 3.1.2.4.3.15.2 **elite** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f11f-2b24-11e6-b7e5-591297143e36 class="margin-NaN">[0]</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.4.3.15.3 **elite** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>elite</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional items</td><td>true</td></tr></tbody></table>

### <a id="0df0f11f-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.16 Field **\[0\]**

###### 3.1.2.4.3.16.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f120-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.17 Field **fans**

###### 3.1.2.4.3.17.1 **fans** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fans</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0df0f121-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.18 Field **friends**

###### 3.1.2.4.3.18.1 **friends** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image29.png?raw=true)

###### 3.1.2.4.3.18.2 **friends** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f122-2b24-11e6-b7e5-591297143e36 class="margin-NaN">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.4.3.18.3 **friends** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>friends</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional items</td><td>true</td></tr></tbody></table>

### <a id="0df0f122-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.19 Field **\[0\]**

###### 3.1.2.4.3.19.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.person.fullName(undefined, undefined, 'female')</td></tr><tr><td>Sample</td><td>Jane Doe</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0df0f124-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.20 Field **review\_count**

###### 3.1.2.4.3.20.1 **review\_count** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_count</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0df0f127-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.21 Field **votes**

###### 3.1.2.4.3.21.1 **votes** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image30.png?raw=true)

###### 3.1.2.4.3.21.2 **votes** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f128-2b24-11e6-b7e5-591297143e36 class="margin-NaN">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f129-2b24-11e6-b7e5-591297143e36 class="margin-NaN">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12a-2b24-11e6-b7e5-591297143e36 class="margin-NaN">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.4.3.21.3 **votes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>votes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0df0f128-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.22 Field **cool**

###### 3.1.2.4.3.22.1 **cool** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cool</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0df0f129-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.23 Field **funny**

###### 3.1.2.4.3.23.1 **funny** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>funny</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0df0f12a-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.24 Field **useful**

###### 3.1.2.4.3.24.1 **useful** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>useful</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0df0f12b-2b24-11e6-b7e5-591297143e36"></a>

###### 3.1.2.4.3.25 Field **yelping\_since**

###### 3.1.2.4.3.25.1 **yelping\_since** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>yelping_since</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.date.between({ from: '2010-01-01T00:00:00.000Z', to: '2021-12-31T00:00:00 000Z' })</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

###### 3.1.2.4.4 **users** Users (TBD)

<table><thead><tr><td>Username</td><td>Read</td><td>Read Write</td></tr></thead><tbody><tr><td>New User</td><td>false</td><td>false</td></tr></tbody></table>

###### 3.1.2.4.5 **users** Indexes

<table class="index-table"><thead><tr><td class="table-property-column">Property</td><td class="table-column-property">idx_name_stars</td><td class="table-column-property">idx_partial</td></tr></thead><tbody><tr><td>Name</td><td class="table-column-indexes">idx_name_stars</td><td class="table-column-indexes">idx_partial</td></tr><tr><td>Activated</td><td class="table-column-indexes">true</td><td class="table-column-indexes">true</td></tr><tr><td>Key</td><td class="table-column-indexes">name('ascending'), average_stars('descending')</td><td class="table-column-indexes">name('ascending')</td></tr><tr><td>Unique</td><td class="table-column-indexes">true</td><td class="table-column-indexes">true</td></tr><tr><td>Drop duplicates</td><td class="table-column-indexes">true</td><td class="table-column-indexes">false</td></tr><tr><td>Sparse</td><td class="table-column-indexes">true</td><td class="table-column-indexes">false</td></tr><tr><td>Background indexing</td><td class="table-column-indexes">true</td><td class="table-column-indexes">false</td></tr><tr><td>Partial filter exp</td><td class="table-column-indexes"></td><td class="table-column-indexes">{"age" : {"$gte" : 21 } }</td></tr><tr><td>Storage engine</td><td class="table-column-indexes">WiredTiger</td><td class="table-column-indexes">WiredTiger</td></tr></tbody></table>

###### 3.1.2.4.6 **users** Target Script

```
use yelp;

db.createCollection("users", {
    "capped": false,
    "validator": {
        "$jsonSchema": {
            "bsonType": "object",
            "title": "users",
            "description": "Users description",
            "properties": {
                "_id": {
                    "bsonType": "objectId"
                },
                "user_id": {
                    "bsonType": "objectId",
                    "title": "User Identifier"
                },
                "type": {
                    "bsonType": "string",
                    "enum": [
                        "user",
                        "owner",
                        "tester"
                    ]
                },
                "name": {
                    "bsonType": "string",
                    "description": "First name plus surname"
                },
                "average_stars": {
                    "bsonType": "number",
                    "description": "Star rating: from 1 to 5. ",
                    "maximum": 5,
                    "minimum": 1
                },
                "compliments": {
                    "bsonType": "object",
                    "properties": {
                        "cool": {
                            "bsonType": "number",
                            "maximum": 5,
                            "minimum": 1
                        },
                        "cute": {
                            "bsonType": "number",
                            "maximum": 5,
                            "minimum": 1
                        },
                        "funny": {
                            "bsonType": "number",
                            "maximum": 5,
                            "minimum": 1
                        },
                        "hot": {
                            "bsonType": "number",
                            "maximum": 5,
                            "minimum": 1
                        },
                        "note": {
                            "bsonType": "number",
                            "maximum": 5,
                            "minimum": 1
                        },
                        "photos": {
                            "bsonType": "number",
                            "maximum": 5,
                            "minimum": 1
                        },
                        "plain": {
                            "bsonType": "number",
                            "maximum": 5,
                            "minimum": 1
                        },
                        "profile": {
                            "bsonType": "number",
                            "maximum": 5,
                            "minimum": 1
                        },
                        "writer": {
                            "bsonType": "number",
                            "maximum": 5,
                            "minimum": 1
                        }
                    },
                    "additionalProperties": true
                },
                "elite": {
                    "bsonType": "array",
                    "additionalItems": true,
                    "items": {
                        "bsonType": "number"
                    }
                },
                "fans": {
                    "bsonType": "number",
                    "minimum": 0
                },
                "friends": {
                    "bsonType": "array",
                    "additionalItems": true,
                    "items": {
                        "bsonType": "string"
                    }
                },
                "review_count": {
                    "bsonType": "number",
                    "minimum": 0
                },
                "votes": {
                    "bsonType": "object",
                    "properties": {
                        "cool": {
                            "bsonType": "number",
                            "minimum": 0
                        },
                        "funny": {
                            "bsonType": "number",
                            "minimum": 0
                        },
                        "useful": {
                            "bsonType": "number",
                            "minimum": 0
                        }
                    },
                    "additionalProperties": true
                },
                "yelping_since": {
                    "bsonType": "string"
                }
            },
            "additionalProperties": true,
            "required": [
                "user_id",
                "type",
                "name",
                "average_stars"
            ]
        }
    },
    "validationLevel": "off",
    "validationAction": "warn",
    "collation": {
        "alternate": "non-ignorable",
        "backwards": false,
        "caseFirst": "off",
        "caseLevel": false,
        "locale": "af",
        "maxVariable": "Null",
        "normalization": false,
        "numericOrdering": false,
        "strength": 1
    }
});

db.users.createIndex({
    "name": 1,
    "average_stars": -1
},
{
    "name": "idx_name_stars",
    "unique": true,
    "dropDups": true,
    "sparse": true,
    "background": true
});

db.users.createIndex({
    "name": 1
},
{
    "name": "idx_partial",
    "unique": true,
    "partialFilterExpression": {
        "age": {
            "$gte": 21
        }
    }
});
```

### <a id="a080d1d0-91f6-11e9-a924-ddc9cd9b071f"></a>

##### 3.1.2.5 Collection **checkins**

###### 3.1.2.5.1 **checkins** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image31.png?raw=true)

###### 3.1.2.5.2 **checkins** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>checkins</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>Storage engine</td><td>WiredTiger</td></tr><tr><td>Validation level</td><td>Off</td></tr><tr><td>Validation action</td><td>Warn</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

###### 3.1.2.5.3 **checkins** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#9c7dc020-91f6-11e9-a924-ddc9cd9b071f class="margin-0">_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>pk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7dc022-91f6-11e9-a924-ddc9cd9b071f class="margin-0">checkin_info</a></td><td class="no-break-word">document</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e76-91f6-11e9-a924-ddc9cd9b071f class="margin-5">^[a-zA-Z0-9_.-]{3}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e45-91f6-11e9-a924-ddc9cd9b071f class="margin-5">^[a-zA-Z0-9_.-]{4}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e77-91f6-11e9-a924-ddc9cd9b071f class="margin-0">type</a></td><td class="no-break-word">string</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7dc021-91f6-11e9-a924-ddc9cd9b071f class="margin-0">business_id</a></td><td class="no-break-word">string</td><td>true</td><td>fk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="9c7dc020-91f6-11e9-a924-ddc9cd9b071f"></a>

###### 3.1.2.5.3.1 Field **\_id**

###### 3.1.2.5.3.1.1 **\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="9c7dc022-91f6-11e9-a924-ddc9cd9b071f"></a>

###### 3.1.2.5.3.2 Field **checkin\_info**

###### 3.1.2.5.3.2.1 **checkin\_info** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image32.png?raw=true)

###### 3.1.2.5.3.2.2 **checkin\_info** Hierarchy

Parent field: **checkins**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#9c7e0e76-91f6-11e9-a924-ddc9cd9b071f class="margin-NaN">^[a-zA-Z0-9_.-]{3}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e45-91f6-11e9-a924-ddc9cd9b071f class="margin-NaN">^[a-zA-Z0-9_.-]{4}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 3.1.2.5.3.2.3 **checkin\_info** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>checkin_info</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="9c7e0e76-91f6-11e9-a924-ddc9cd9b071f"></a>

###### 3.1.2.5.3.3 Field **^\[a-zA-Z0-9\_.-\]{3}$**

###### 3.1.2.5.3.3.1 **^\[a-zA-Z0-9\_.-\]{3}$** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>^[a-zA-Z0-9_.-]{3}$</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Sample Name</td><td>9-6</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="9c7e0e45-91f6-11e9-a924-ddc9cd9b071f"></a>

###### 3.1.2.5.3.4 Field **^\[a-zA-Z0-9\_.-\]{4}$**

###### 3.1.2.5.3.4.1 **^\[a-zA-Z0-9\_.-\]{4}$** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>^[a-zA-Z0-9_.-]{4}$</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Sample Name</td><td>23-6</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="9c7e0e77-91f6-11e9-a924-ddc9cd9b071f"></a>

###### 3.1.2.5.3.5 Field **type**

###### 3.1.2.5.3.5.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>checkin</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="9c7dc021-91f6-11e9-a924-ddc9cd9b071f"></a>

###### 3.1.2.5.3.6 Field **business\_id**

###### 3.1.2.5.3.6.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Foreign collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Foreign field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr><tr><td>Sample</td><td>eFA9dqXT5EA_TrMgbo03QQ</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

###### 3.1.2.5.4 **checkins** Indexes

<table class="index-table"><thead><tr><td class="table-property-column">Property</td><td class="table-column-property">_id_</td></tr></thead><tbody><tr><td>Name</td><td class="table-column-indexes">_id_</td></tr><tr><td>Activated</td><td class="table-column-indexes">true</td></tr><tr><td>Key</td><td class="table-column-indexes">_id('ascending')</td></tr></tbody></table>

###### 3.1.2.5.5 **checkins** Target Script

```
use yelp;

db.createCollection("checkins", {
    "capped": false,
    "validator": {
        "$jsonSchema": {
            "bsonType": "object",
            "title": "checkins",
            "properties": {
                "_id": {
                    "bsonType": "objectId"
                },
                "checkin_info": {
                    "bsonType": "object",
                    "additionalProperties": false,
                    "patternProperties": {
                        "^[a-zA-Z0-9_.-]{3}$": {
                            "bsonType": "number"
                        },
                        "^[a-zA-Z0-9_.-]{4}$": {
                            "bsonType": "number"
                        }
                    }
                },
                "type": {
                    "bsonType": "string"
                },
                "business_id": {
                    "bsonType": "string"
                }
            },
            "additionalProperties": true,
            "required": [
                "_id",
                "checkin_info",
                "type",
                "business_id"
            ]
        }
    },
    "validationLevel": "off",
    "validationAction": "warn",
    "collation": {
        "alternate": "non-ignorable",
        "backwards": false,
        "caseFirst": "off",
        "caseLevel": false,
        "locale": "af",
        "maxVariable": "Null",
        "normalization": false,
        "numericOrdering": false,
        "strength": 1
    }
});

db.checkins.createIndex({
    "_id": 1
},
{
    "name": "_id_"
});
```

### <a id="views"></a>

## 4\. Views

### <a id="5c771580-5193-11e7-b9f2-49270a53df2c"></a>

### 4.1 View **rov\_bussiness**

#### 4.1.1 **rov\_bussiness** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image33.png?raw=true)

#### 4.1.2 **rov\_bussiness** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>View name</td><td>rov_bussiness</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>View on</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Pipeline</td><td>[ { "$project": { "business_id": 1, "name": 1, "full_address": {}, "type": 1 } } ]</td></tr></tbody></table>

#### 4.1.3 **rov\_bussiness** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#94b971e8-0ab1-4909-ba2a-0f6bd36ae29d class="margin-0">business_id</a></td><td class="no-break-word">objectId</td><td>false</td><td>pk</td><td><div class="docs-markdown"><p>Unique key for businesses</p></div></td><td><div class="docs-markdown"><p>Sat Nov 04 2017 10:12:00 GMT+0100 (Romance Standard Time): some comments</p></div></td></tr><tr><td><a href=#a232e94c-7c9b-473b-9675-42efacc6ece6 class="margin-0">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#4445c459-a91f-418c-9a59-f771b5cc2858 class="margin-0">full_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#f229df59-3fbf-48f4-824a-a3b38795f981 class="margin-0">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="94b971e8-0ab1-4909-ba2a-0f6bd36ae29d"></a>

##### 4.1.3.1 Field **business\_id**

###### 4.1.3.1.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="a232e94c-7c9b-473b-9675-42efacc6ece6"></a>

##### 4.1.3.2 Field **name**

###### 4.1.3.2.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="4445c459-a91f-418c-9a59-f771b5cc2858"></a>

##### 4.1.3.3 Field **full\_address**

###### 4.1.3.3.1 **full\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>full_address</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="f229df59-3fbf-48f4-824a-a3b38795f981"></a>

##### 4.1.3.4 Field **type**

###### 4.1.3.4.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

#### 4.1.4 **rov\_bussiness** Target Script

```
use yelp;

db.createView("rov_bussiness",
	"businesses",
	[
	    {
	        "$project": {
	            "business_id": 1,
	            "name": 1,
	            "full_address": {},
	            "type": 1
	        }
	    }
	]
);
```

### <a id="090874c0-5206-11e7-8e65-9b1d6a151b1d"></a>

### 4.2 View **rov\_reviews**

#### 4.2.1 **rov\_reviews** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image34.png?raw=true)

#### 4.2.2 **rov\_reviews** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>View name</td><td>rov_reviews</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>View on</td><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td></tr><tr><td>Pipeline</td><td>[ { "$project": { "username": [ { "user_id": "$user_id", "type": "$type", "name": "$name", "average_stars": "$average_stars", "compliments": { "cool": "$compliments.cool", "cute": "$compliments.cute", "funny": "$compliments.funny", "hot": "$compliments.hot", "note": "$compliments.note", "photos": "$compliments.photos", "plain": "$compliments.plain", "profile": "$compliments.profile", "writer": "$compliments.writer" }, "elite": "$elite", "fans": "$fans", "friends": "$friends", "review_count": "$review_count", "votes": { "cool": "$votes.cool", "funny": "$votes.funny", "useful": "$votes.useful" }, "yelping_since": "$yelping_since" } ], "business": { "business_id": "$business_id", "type": "$type", "stars": "$stars", "full_address": {} }, "user": { "user_id": "$user_id", "type": "$type", "votes": { "cool": "$votes.cool", "funny": "$votes.funny", "useful": "$votes.useful" } } } }, { "$unionWith": "users" }, { "$unionWith": "businesses" } ]</td></tr></tbody></table>

#### 4.2.3 **rov\_reviews** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#31c7d9ba-d2ab-4157-9da1-e30052b7dbd2 class="margin-0">username</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bf4740f7-b066-4834-b340-2beb61923a96 class="margin-5">[0]</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#d62e97af-4f4a-46a1-a3f0-8e3095272224 class="margin-10">user_id</a></td><td class="no-break-word">objectId</td><td>false</td><td>pk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#5dae6feb-f43e-4e3f-b2af-949a8977f206 class="margin-10">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#d2e256f4-af97-4f76-909b-b855150a85e2 class="margin-10">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"><p>First name plus surname</p></div></td><td><div class="docs-markdown"><p>Fri Sep 15 2017 17:31:32 GMT+0200 (Romance Summer Time): MongoDB Demo</p></div></td></tr><tr><td><a href=#731a3826-1f3e-418a-a8ca-854de9146f30 class="margin-10">average_stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"><p>Star rating: from 1 to 5.</p></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3708979a-46ff-4d65-af6d-b7dd4908e0f9 class="margin-10">compliments</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f114-2b24-11e6-b7e5-591297143e36 class="margin-15">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f115-2b24-11e6-b7e5-591297143e36 class="margin-15">cute</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f116-2b24-11e6-b7e5-591297143e36 class="margin-15">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f117-2b24-11e6-b7e5-591297143e36 class="margin-15">hot</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f119-2b24-11e6-b7e5-591297143e36 class="margin-15">note</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11a-2b24-11e6-b7e5-591297143e36 class="margin-15">photos</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11b-2b24-11e6-b7e5-591297143e36 class="margin-15">plain</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11c-2b24-11e6-b7e5-591297143e36 class="margin-15">profile</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11d-2b24-11e6-b7e5-591297143e36 class="margin-15">writer</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ab687bcb-0fc6-4e0d-bff4-12f9c18cfe58 class="margin-10">elite</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11f-2b24-11e6-b7e5-591297143e36 class="margin-15">[0]</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bf642ae0-8472-44bf-bdef-d284f9794c36 class="margin-10">fans</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3e08e8b3-fbfe-4983-8d01-9ecfa7df453c class="margin-10">friends</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f122-2b24-11e6-b7e5-591297143e36 class="margin-15">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#dc3f4657-c57b-4846-bcff-5f8559405009 class="margin-10">review_count</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#e1b580dc-eb61-42c2-b28a-526b855ed6d6 class="margin-10">votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f128-2b24-11e6-b7e5-591297143e36 class="margin-15">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f129-2b24-11e6-b7e5-591297143e36 class="margin-15">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12a-2b24-11e6-b7e5-591297143e36 class="margin-15">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#80eaada8-dec4-4ac9-87d6-ac27aee9e4bf class="margin-10">yelping_since</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ea4706fc-0103-4991-a4c2-198cb08206ee class="margin-0">business</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#6f5de18b-d47d-46e3-8105-7ad9600c4ded class="margin-5">business_id</a></td><td class="no-break-word">objectId</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#492a3b33-6faa-467d-8f51-5494a7047432 class="margin-5">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ddc180f4-ee83-4839-96cc-24901f57933e class="margin-5">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#63a66d1b-af25-4381-9d22-d03d01b3a27c class="margin-5">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#f3647e00-fab7-48cb-8b11-27f11d3cf4a1 class="margin-5">stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#1b6da19b-940e-435f-b72d-2103ef4bb2ae class="margin-5">review_count</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#5174bf87-ddb9-45f1-a9cf-a0be4ba7305d class="margin-5">full_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#a1463d2e-8297-42d3-a5e9-50313bfa9be8 class="margin-10">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#83111583-5bcb-4772-afbb-c9a6a3348d37 class="margin-10">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0bc83abc-0fa9-4a4d-a41b-6b3b1494355c class="margin-10">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ca9b3eda-30c4-4480-aeb6-481ef8a004a4 class="margin-10">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#545989db-57f2-49c3-9ef2-e20e09bb67f1 class="margin-10">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#60ae6b1d-7f1f-450b-99a2-8fa3a2615ffc class="margin-10">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bcfd7800-79e5-4fa6-a6dc-cfcf8beca70f class="margin-5">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3a118d62-b189-43cc-a365-556a41e0e870 class="margin-5">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#55fb95c9-6d11-49ae-a893-35c31ec166da class="margin-5">latitude</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#482b18b8-f285-46dc-a570-3f764027d509 class="margin-5">longitude</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#35a6eb0d-8075-4118-b00d-5b3bbe3d3491 class="margin-0">user</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#fd08128d-0267-41b8-a279-f177701bdd2c class="margin-5">user_id</a></td><td class="no-break-word">objectId</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c40f7443-2709-4235-8f54-7e2df6f8da50 class="margin-5">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#d9bc0292-0bf7-4d38-8d93-4cfd68054681 class="margin-5">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#def3ba2c-ba89-4a54-bb07-970204249754 class="margin-5">votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#aa5143d2-370b-4967-be3b-87c8d6678e43 class="margin-10">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#dd85f69f-3059-4470-aa7f-38001459b5cf class="margin-10">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#cec67ce0-2cb9-454a-9e24-46937ba45376 class="margin-10">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7e93b31c-76cc-4ced-a4aa-d4ef07bcaa29 class="margin-5">yelping_since</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="31c7d9ba-d2ab-4157-9da1-e30052b7dbd2"></a>

##### 4.2.3.1 Field **username**

###### 4.2.3.1.1 **username** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image35.png?raw=true)

###### 4.2.3.1.2 **username** Hierarchy

Parent field: **rov\_reviews**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#bf4740f7-b066-4834-b340-2beb61923a96 class="margin-NaN">[0]</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 4.2.3.1.3 **username** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>username</td></tr><tr><td>Technical name</td><td>username</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Unique items</td><td>false</td></tr><tr><td>Additional items</td><td>true</td></tr></tbody></table>

### <a id="bf4740f7-b066-4834-b340-2beb61923a96"></a>

##### 4.2.3.2 Field **\[0\]**

###### 4.2.3.2.1 **\[0\]** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image36.png?raw=true)

###### 4.2.3.2.2 **\[0\]** Hierarchy

Parent field: **username**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#d62e97af-4f4a-46a1-a3f0-8e3095272224 class="margin-NaN">user_id</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#5dae6feb-f43e-4e3f-b2af-949a8977f206 class="margin-NaN">type</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#d2e256f4-af97-4f76-909b-b855150a85e2 class="margin-NaN">name</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#731a3826-1f3e-418a-a8ca-854de9146f30 class="margin-NaN">average_stars</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3708979a-46ff-4d65-af6d-b7dd4908e0f9 class="margin-NaN">compliments</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ab687bcb-0fc6-4e0d-bff4-12f9c18cfe58 class="margin-NaN">elite</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bf642ae0-8472-44bf-bdef-d284f9794c36 class="margin-NaN">fans</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3e08e8b3-fbfe-4983-8d01-9ecfa7df453c class="margin-NaN">friends</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#dc3f4657-c57b-4846-bcff-5f8559405009 class="margin-NaN">review_count</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#e1b580dc-eb61-42c2-b28a-526b855ed6d6 class="margin-NaN">votes</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#80eaada8-dec4-4ac9-87d6-ac27aee9e4bf class="margin-NaN">yelping_since</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 4.2.3.2.3 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="d62e97af-4f4a-46a1-a3f0-8e3095272224"></a>

##### 4.2.3.3 Field **user\_id**

###### 4.2.3.3.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="5dae6feb-f43e-4e3f-b2af-949a8977f206"></a>

##### 4.2.3.4 Field **type**

###### 4.2.3.4.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="d2e256f4-af97-4f76-909b-b855150a85e2"></a>

##### 4.2.3.5 Field **name**

###### 4.2.3.5.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="731a3826-1f3e-418a-a8ca-854de9146f30"></a>

##### 4.2.3.6 Field **average\_stars**

###### 4.2.3.6.1 **average\_stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>average_stars</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="3708979a-46ff-4d65-af6d-b7dd4908e0f9"></a>

##### 4.2.3.7 Field **compliments**

###### 4.2.3.7.1 **compliments** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>compliments</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="ab687bcb-0fc6-4e0d-bff4-12f9c18cfe58"></a>

##### 4.2.3.8 Field **elite**

###### 4.2.3.8.1 **elite** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>elite</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="bf642ae0-8472-44bf-bdef-d284f9794c36"></a>

##### 4.2.3.9 Field **fans**

###### 4.2.3.9.1 **fans** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fans</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="3e08e8b3-fbfe-4983-8d01-9ecfa7df453c"></a>

##### 4.2.3.10 Field **friends**

###### 4.2.3.10.1 **friends** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>friends</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="dc3f4657-c57b-4846-bcff-5f8559405009"></a>

##### 4.2.3.11 Field **review\_count**

###### 4.2.3.11.1 **review\_count** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_count</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="e1b580dc-eb61-42c2-b28a-526b855ed6d6"></a>

##### 4.2.3.12 Field **votes**

###### 4.2.3.12.1 **votes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>votes</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="80eaada8-dec4-4ac9-87d6-ac27aee9e4bf"></a>

##### 4.2.3.13 Field **yelping\_since**

###### 4.2.3.13.1 **yelping\_since** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>yelping_since</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="ea4706fc-0103-4991-a4c2-198cb08206ee"></a>

##### 4.2.3.14 Field **business**

###### 4.2.3.14.1 **business** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image37.png?raw=true)

###### 4.2.3.14.2 **business** Hierarchy

Parent field: **rov\_reviews**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#6f5de18b-d47d-46e3-8105-7ad9600c4ded class="margin-NaN">business_id</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#492a3b33-6faa-467d-8f51-5494a7047432 class="margin-NaN">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ddc180f4-ee83-4839-96cc-24901f57933e class="margin-NaN">type</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#63a66d1b-af25-4381-9d22-d03d01b3a27c class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#f3647e00-fab7-48cb-8b11-27f11d3cf4a1 class="margin-NaN">stars</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#1b6da19b-940e-435f-b72d-2103ef4bb2ae class="margin-NaN">review_count</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#5174bf87-ddb9-45f1-a9cf-a0be4ba7305d class="margin-NaN">full_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bcfd7800-79e5-4fa6-a6dc-cfcf8beca70f class="margin-NaN">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3a118d62-b189-43cc-a365-556a41e0e870 class="margin-NaN">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#55fb95c9-6d11-49ae-a893-35c31ec166da class="margin-NaN">latitude</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#482b18b8-f285-46dc-a570-3f764027d509 class="margin-NaN">longitude</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 4.2.3.14.3 **business** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business</td></tr><tr><td>Technical name</td><td>business</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="6f5de18b-d47d-46e3-8105-7ad9600c4ded"></a>

##### 4.2.3.15 Field **business\_id**

###### 4.2.3.15.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Technical name</td><td>business_id</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="492a3b33-6faa-467d-8f51-5494a7047432"></a>

##### 4.2.3.16 Field **name**

###### 4.2.3.16.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Technical name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="ddc180f4-ee83-4839-96cc-24901f57933e"></a>

##### 4.2.3.17 Field **type**

###### 4.2.3.17.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="63a66d1b-af25-4381-9d22-d03d01b3a27c"></a>

##### 4.2.3.18 Field **open**

###### 4.2.3.18.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Technical name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="f3647e00-fab7-48cb-8b11-27f11d3cf4a1"></a>

##### 4.2.3.19 Field **stars**

###### 4.2.3.19.1 **stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>stars</td></tr><tr><td>Technical name</td><td>stars</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="1b6da19b-940e-435f-b72d-2103ef4bb2ae"></a>

##### 4.2.3.20 Field **review\_count**

###### 4.2.3.20.1 **review\_count** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_count</td></tr><tr><td>Technical name</td><td>review_count</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="5174bf87-ddb9-45f1-a9cf-a0be4ba7305d"></a>

##### 4.2.3.21 Field **full\_address**

###### 4.2.3.21.1 **full\_address** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image38.png?raw=true)

###### 4.2.3.21.2 **full\_address** Hierarchy

Parent field: **business**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#a1463d2e-8297-42d3-a5e9-50313bfa9be8 class="margin-NaN">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#83111583-5bcb-4772-afbb-c9a6a3348d37 class="margin-NaN">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0bc83abc-0fa9-4a4d-a41b-6b3b1494355c class="margin-NaN">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ca9b3eda-30c4-4480-aeb6-481ef8a004a4 class="margin-NaN">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#545989db-57f2-49c3-9ef2-e20e09bb67f1 class="margin-NaN">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#60ae6b1d-7f1f-450b-99a2-8fa3a2615ffc class="margin-NaN">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 4.2.3.21.3 **full\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>full_address</td></tr><tr><td>Technical name</td><td>full_address</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="a1463d2e-8297-42d3-a5e9-50313bfa9be8"></a>

##### 4.2.3.22 Field **houseNum**

###### 4.2.3.22.1 **houseNum** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>houseNum</td></tr><tr><td>Technical name</td><td>houseNum</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="83111583-5bcb-4772-afbb-c9a6a3348d37"></a>

##### 4.2.3.23 Field **street**

###### 4.2.3.23.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Technical name</td><td>street</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0bc83abc-0fa9-4a4d-a41b-6b3b1494355c"></a>

##### 4.2.3.24 Field **box**

###### 4.2.3.24.1 **box** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>box</td></tr><tr><td>Technical name</td><td>box</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="ca9b3eda-30c4-4480-aeb6-481ef8a004a4"></a>

##### 4.2.3.25 Field **city**

###### 4.2.3.25.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Technical name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="545989db-57f2-49c3-9ef2-e20e09bb67f1"></a>

##### 4.2.3.26 Field **state**

###### 4.2.3.26.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Technical name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="60ae6b1d-7f1f-450b-99a2-8fa3a2615ffc"></a>

##### 4.2.3.27 Field **zip**

###### 4.2.3.27.1 **zip** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>zip</td></tr><tr><td>Technical name</td><td>zip</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="bcfd7800-79e5-4fa6-a6dc-cfcf8beca70f"></a>

##### 4.2.3.28 Field **city**

###### 4.2.3.28.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Technical name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="3a118d62-b189-43cc-a365-556a41e0e870"></a>

##### 4.2.3.29 Field **state**

###### 4.2.3.29.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Technical name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="55fb95c9-6d11-49ae-a893-35c31ec166da"></a>

##### 4.2.3.30 Field **latitude**

###### 4.2.3.30.1 **latitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>latitude</td></tr><tr><td>Technical name</td><td>latitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="482b18b8-f285-46dc-a570-3f764027d509"></a>

##### 4.2.3.31 Field **longitude**

###### 4.2.3.31.1 **longitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>longitude</td></tr><tr><td>Technical name</td><td>longitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="35a6eb0d-8075-4118-b00d-5b3bbe3d3491"></a>

##### 4.2.3.32 Field **user**

###### 4.2.3.32.1 **user** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image39.png?raw=true)

###### 4.2.3.32.2 **user** Hierarchy

Parent field: **rov\_reviews**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#fd08128d-0267-41b8-a279-f177701bdd2c class="margin-NaN">user_id</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c40f7443-2709-4235-8f54-7e2df6f8da50 class="margin-NaN">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#d9bc0292-0bf7-4d38-8d93-4cfd68054681 class="margin-NaN">type</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#def3ba2c-ba89-4a54-bb07-970204249754 class="margin-NaN">votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7e93b31c-76cc-4ced-a4aa-d4ef07bcaa29 class="margin-NaN">yelping_since</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 4.2.3.32.3 **user** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user</td></tr><tr><td>Technical name</td><td>user</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="fd08128d-0267-41b8-a279-f177701bdd2c"></a>

##### 4.2.3.33 Field **user\_id**

###### 4.2.3.33.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Technical name</td><td>user_id</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="c40f7443-2709-4235-8f54-7e2df6f8da50"></a>

##### 4.2.3.34 Field **name**

###### 4.2.3.34.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Technical name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="d9bc0292-0bf7-4d38-8d93-4cfd68054681"></a>

##### 4.2.3.35 Field **type**

###### 4.2.3.35.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="def3ba2c-ba89-4a54-bb07-970204249754"></a>

##### 4.2.3.36 Field **votes**

###### 4.2.3.36.1 **votes** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image40.png?raw=true)

###### 4.2.3.36.2 **votes** Hierarchy

Parent field: **user**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#aa5143d2-370b-4967-be3b-87c8d6678e43 class="margin-NaN">cool</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#dd85f69f-3059-4470-aa7f-38001459b5cf class="margin-NaN">funny</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#cec67ce0-2cb9-454a-9e24-46937ba45376 class="margin-NaN">useful</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

###### 4.2.3.36.3 **votes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>votes</td></tr><tr><td>Technical name</td><td>votes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="aa5143d2-370b-4967-be3b-87c8d6678e43"></a>

##### 4.2.3.37 Field **cool**

###### 4.2.3.37.1 **cool** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cool</td></tr><tr><td>Technical name</td><td>cool</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="dd85f69f-3059-4470-aa7f-38001459b5cf"></a>

##### 4.2.3.38 Field **funny**

###### 4.2.3.38.1 **funny** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>funny</td></tr><tr><td>Technical name</td><td>funny</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="cec67ce0-2cb9-454a-9e24-46937ba45376"></a>

##### 4.2.3.39 Field **useful**

###### 4.2.3.39.1 **useful** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>useful</td></tr><tr><td>Technical name</td><td>useful</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="7e93b31c-76cc-4ced-a4aa-d4ef07bcaa29"></a>

##### 4.2.3.40 Field **yelping\_since**

###### 4.2.3.40.1 **yelping\_since** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>yelping_since</td></tr><tr><td>Technical name</td><td>yelping_since</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

#### 4.2.4 **rov\_reviews** Target Script

```
use yelp;

db.createView("rov_reviews",
	"reviews",
	[
	    {
	        "$project": {
	            "username": [
	                {
	                    "user_id": "$user_id",
	                    "type": "$type",
	                    "name": "$name",
	                    "average_stars": "$average_stars",
	                    "compliments": {
	                        "cool": "$compliments.cool",
	                        "cute": "$compliments.cute",
	                        "funny": "$compliments.funny",
	                        "hot": "$compliments.hot",
	                        "note": "$compliments.note",
	                        "photos": "$compliments.photos",
	                        "plain": "$compliments.plain",
	                        "profile": "$compliments.profile",
	                        "writer": "$compliments.writer"
	                    },
	                    "elite": "$elite",
	                    "fans": "$fans",
	                    "friends": "$friends",
	                    "review_count": "$review_count",
	                    "votes": {
	                        "cool": "$votes.cool",
	                        "funny": "$votes.funny",
	                        "useful": "$votes.useful"
	                    },
	                    "yelping_since": "$yelping_since"
	                }
	            ],
	            "business": {
	                "business_id": "$business_id",
	                "type": "$type",
	                "stars": "$stars",
	                "full_address": {}
	            },
	            "user": {
	                "user_id": "$user_id",
	                "type": "$type",
	                "votes": {
	                    "cool": "$votes.cool",
	                    "funny": "$votes.funny",
	                    "useful": "$votes.useful"
	                }
	            }
	        }
	    },
	    {
	        "$unionWith": "users"
	    },
	    {
	        "$unionWith": "businesses"
	    }
	]
);
```

### <a id="relationships"></a>

## 5\. Relationships

### <a id="8a3660f0-2b26-11e6-b7e5-591297143e36"></a>

### 5.1 Relationship **fk\_tipsBusinesses**

#### 5.1.1 **fk\_tipsBusinesses** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr></tbody></table>

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image41.png?raw=true)![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image42.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td><td><a href=#0de02832-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr></tbody></table>

#### 5.1.2 **fk\_tipsBusinesses** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_tipsBusinesses</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Parent field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td></tr><tr><td>Child field</td><td><a href=#0de02832-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="aa956d50-2b26-11e6-b7e5-591297143e36"></a>

### 5.2 Relationship **fk\_tipsUsers**

#### 5.2.1 **fk\_tipsUsers** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>'User Identifier'</a></td></tr></tbody></table>

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image43.png?raw=true)![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image44.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td><td><a href=#0de02837-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr></tbody></table>

#### 5.2.2 **fk\_tipsUsers** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_tipsUsers</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td></tr><tr><td>Parent field</td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>User Identifier</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td></tr><tr><td>Child field</td><td><a href=#0de02837-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="e2514f70-2b26-11e6-b7e5-591297143e36"></a>

### 5.3 Relationship **fk\_reviewsUsers**

#### 5.3.1 **fk\_reviewsUsers** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>'User Identifier'</a></td></tr></tbody></table>

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image45.png?raw=true)![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image46.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td><td><a href=#0da2aa08-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr></tbody></table>

#### 5.3.2 **fk\_reviewsUsers** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_reviewsUsers</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td></tr><tr><td>Parent field</td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>User Identifier</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td></tr><tr><td>Child field</td><td><a href=#0da2aa08-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="fb857d40-2b26-11e6-b7e5-591297143e36"></a>

### 5.4 Relationship **fk\_reviewsBusinesses**

#### 5.4.1 **fk\_reviewsBusinesses** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr></tbody></table>

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image47.png?raw=true)![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image48.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td><td><a href=#0da2aa02-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr></tbody></table>

#### 5.4.2 **fk\_reviewsBusinesses** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_reviewsBusinesses</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Parent field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td></tr><tr><td>Child field</td><td><a href=#0da2aa02-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="003231f0-91f7-11e9-a924-ddc9cd9b071f"></a>

### 5.5 Relationship **fk businesses.business\_id to checkins.business\_id**

#### 5.5.1 **fk businesses.business\_id to checkins.business\_id** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr></tbody></table>

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image49.png?raw=true)![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image50.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#a080d1d0-91f6-11e9-a924-ddc9cd9b071f>checkins</a></td><td><a href=#9c7dc021-91f6-11e9-a924-ddc9cd9b071f>business_id</a></td></tr></tbody></table>

#### 5.5.2 **fk businesses.business\_id to checkins.business\_id** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk businesses.business_id to checkins.business_id</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Parent field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#a080d1d0-91f6-11e9-a924-ddc9cd9b071f>checkins</a></td></tr><tr><td>Child field</td><td><a href=#9c7dc021-91f6-11e9-a924-ddc9cd9b071f>business_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="edges"></a>