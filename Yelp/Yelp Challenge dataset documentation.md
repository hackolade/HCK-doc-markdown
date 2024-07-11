     

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

Printed On: Thu Jul 11 2024 23:13:03 GMT+0200 (Central European Summer Time)

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

##### 1\. Model

##### 1.1 Model **Yelp Challenge dataset**

##### 1.1.1 **Yelp Challenge dataset** Entity Relationship Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image2.png?raw=true)

##### 1.1.2 **Yelp Challenge dataset** Properties

##### 1.1.2.1 **Details** tab

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td><span>Model name</span></td><td>Yelp Challenge dataset</td></tr><tr><td><span>Description</span></td><td><div class="docs-markdown"><p>Schema inferred from the reverse-engineering of a Yelp Challenge dataset available from <a href=https://www.yelp.com/dataset_challenge/dataset>https://www.yelp.com/dataset_challenge/dataset</a></p></div></td></tr><tr><td><span>Author</span></td><td>Pascal</td></tr><tr><td><span>Version</span></td><td>1.2</td></tr><tr><td><span>Target</span></td><td>MongoDB</td></tr><tr><td><span>DB version</span></td><td>v5.0</td></tr><tr><td><span>Synchronization Id</span></td><td>db8a6750-5b42-11e8-9c3f-1d376af9020b</td></tr><tr><td><span>Comments</span></td><td><div class="docs-markdown"><p>The dataset was downloaded and loaded to a MongoDB, then reverse-engineered with Hackolade. The relationships were manually documented to enrich the model.</p><p>This schema shows the power of JSON with the embedding of many attributes logically grouped, one form of implicit relationships. At the same time, the schema is fairly relational, which makes total sense given the conceptual entities. As a result, there's no denormalization. Given the size of the collections, it makes sense to perform this kind of traditional foreing key relationships.</p><p>Note that only fields found in 100% of the sampled documents are 'required' (and differentiated thanks to a solid line box) as opposed to the other fields with dashed line boxes.</p><p>The sampling parameters were:</p><ul><li>absolute up to 1000 documents max per collection</li><li>alpha order of fields</li></ul></div></td></tr></tbody></table>

##### 1.1.2.2 **Zeiss** tab

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td><span>Dropdown selection</span></td><td>Option 1</td></tr></tbody></table>

##### 1.1.2.3 **Options** tab

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody></tbody></table>

##### 1.1.3 **Yelp Challenge dataset** DB Definitions

### <a id="0dd81200-2b24-11e6-b7e5-591297143e36"></a>1.1.3.1 Field **address**

##### 1.1.3.1.1 **address** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image3.png?raw=true)

##### 1.1.3.1.2 **address** Hierarchy

Parent field: **Definitions**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#7107ebf0-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#760da090-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7bfbe070-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7ee803e0-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#85787730-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#87afc990-dc5b-11e9-b819-e3f2d5171928 class="margin-NaN">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 1.1.3.1.3 **address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>address</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="7107ebf0-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.2 Field **houseNum**

##### 1.1.3.2.1 **houseNum** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>houseNum</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.buildingNumber()</td></tr><tr><td>Sample</td><td>123</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="760da090-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.3 Field **street**

##### 1.1.3.3.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.street()</td></tr><tr><td>Sample</td><td>Main Street</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="7bfbe070-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.4 Field **box**

##### 1.1.3.4.1 **box** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>box</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.secondaryAddress()</td></tr><tr><td>Sample</td><td>10</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="7ee803e0-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.5 Field **city**

##### 1.1.3.5.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.city()</td></tr><tr><td>Sample</td><td>Anytown</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="85787730-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.6 Field **state**

##### 1.1.3.6.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.state({ abbreviated: true })</td></tr><tr><td>Sample</td><td>CA</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="87afc990-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.7 Field **zip**

##### 1.1.3.7.1 **zip** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>zip</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.state({ abbreviated: true })</td></tr><tr><td>Sample</td><td>12345</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="diagramViews"></a>

##### 2\. ER Diagram Views

### <a id="65013f10-4748-11eb-a6d2-ebfe0d19463b"></a>2.1 Diagram **Domain view**

##### 2.1.1 **Domain view** Entity Relationship Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image4.png?raw=true)

##### 2.1.2 **Domain view** Graph Diagram

### <a id="containers"></a>

##### 3\. Databases

### <a id="3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6"></a>3.1 Database **yelp**

##### 3.1.1 **yelp** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Database name</td><td>yelp</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Enable sharding</td><td>true</td></tr></tbody></table>

### <a id="3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6-children"></a>3.1.2 **yelp** Collections

### <a id="0dd7ead0-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1 Collection **businesses**

##### 3.1.2.1.1 **businesses** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image5.png?raw=true)

##### 3.1.2.1.2 **businesses** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>businesses</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>Storage engine</td><td>WiredTiger</td></tr><tr><td>Validation level</td><td>Off</td></tr><tr><td>Validation action</td><td>Warn</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

##### 3.1.2.1.3 **businesses** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36 class="margin-0">business_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>pk, dk</td><td><div class="docs-markdown"><p>Unique key for businesses</p></div></td><td><div class="docs-markdown"><p>Sat Nov 04 2017 10:12:00 GMT+0100 (Romance Standard Time): some comments</p></div></td></tr><tr><td><a href=#0dd81219-2b24-11e6-b7e5-591297143e36 class="margin-0">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#06399180-d360-11ec-adc4-432dcbbfc12a class="margin-0">phoneNumber</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3c5d7210-9df8-11ec-afe5-55c2aa6d0440 class="margin-0">business_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#f2783d2a-e747-4dce-bacd-afad337fc159 class="margin-5">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#36b05f0b-d7de-4a3b-9c53-1286a559cbd9 class="margin-5">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8f31cc6d-6b38-415f-b3f4-05a60906eb39 class="margin-5">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8ac10954-b0fe-4f7e-8024-8f10c0e56e2e class="margin-5">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8673c0e2-894f-40b1-ab14-b21d4ec2ba85 class="margin-5">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#1220765a-7bd9-4fbe-bb99-608ddd423dca class="margin-5">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#4445c459-a91f-418c-9a59-f771b5cc2858 class="margin-0">full_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#db37ab7b-dc16-43f2-9499-a6ff179ee49a class="margin-5">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bf165921-9e1c-44fa-89d9-6cc2b7bc8c18 class="margin-5">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#05497756-a7ae-4c65-b4d4-04e346d04e3e class="margin-5">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#cbfd60c9-1108-4360-8f0c-ab8bc0bf1ddb class="margin-5">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#a4968124-98ec-43fa-8161-3cb86a1f2a0d class="margin-5">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#84afa995-565b-41ed-8a48-030c1ba8c1d4 class="margin-5">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead2-2b24-11e6-b7e5-591297143e36 class="margin-0">attributes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead3-2b24-11e6-b7e5-591297143e36 class="margin-5">Accepts&nbsp;Credit&nbsp;Cards</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead4-2b24-11e6-b7e5-591297143e36 class="margin-5">Accepts&nbsp;Insurance</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead5-2b24-11e6-b7e5-591297143e36 class="margin-5">Alcohol</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead6-2b24-11e6-b7e5-591297143e36 class="margin-5">Ambience</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead7-2b24-11e6-b7e5-591297143e36 class="margin-10">casual</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead8-2b24-11e6-b7e5-591297143e36 class="margin-10">classy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead9-2b24-11e6-b7e5-591297143e36 class="margin-10">divey</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eada-2b24-11e6-b7e5-591297143e36 class="margin-10">hipster</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadb-2b24-11e6-b7e5-591297143e36 class="margin-10">intimate</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadc-2b24-11e6-b7e5-591297143e36 class="margin-10">romantic</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadd-2b24-11e6-b7e5-591297143e36 class="margin-10">touristy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eade-2b24-11e6-b7e5-591297143e36 class="margin-10">trendy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadf-2b24-11e6-b7e5-591297143e36 class="margin-10">upscale</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae0-2b24-11e6-b7e5-591297143e36 class="margin-5">Attire</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae1-2b24-11e6-b7e5-591297143e36 class="margin-5">By&nbsp;Appointment&nbsp;Only</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae2-2b24-11e6-b7e5-591297143e36 class="margin-5">BYOB/Corkage</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae3-2b24-11e6-b7e5-591297143e36 class="margin-5">Caters</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae4-2b24-11e6-b7e5-591297143e36 class="margin-5">Coat&nbsp;Check</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae5-2b24-11e6-b7e5-591297143e36 class="margin-5">Delivery</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae6-2b24-11e6-b7e5-591297143e36 class="margin-5">Dogs&nbsp;Allowed</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae7-2b24-11e6-b7e5-591297143e36 class="margin-5">Drive-Thru</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae8-2b24-11e6-b7e5-591297143e36 class="margin-5">Good&nbsp;For</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae9-2b24-11e6-b7e5-591297143e36 class="margin-10">breakfast</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaea-2b24-11e6-b7e5-591297143e36 class="margin-10">brunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaeb-2b24-11e6-b7e5-591297143e36 class="margin-10">dessert</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaec-2b24-11e6-b7e5-591297143e36 class="margin-10">dinner</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaed-2b24-11e6-b7e5-591297143e36 class="margin-10">latenight</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaee-2b24-11e6-b7e5-591297143e36 class="margin-10">lunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaef-2b24-11e6-b7e5-591297143e36 class="margin-5">Good&nbsp;For&nbsp;Dancing</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e0-2b24-11e6-b7e5-591297143e36 class="margin-5">Good&nbsp;For&nbsp;Groups</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e1-2b24-11e6-b7e5-591297143e36 class="margin-5">Good&nbsp;for&nbsp;Kids</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e2-2b24-11e6-b7e5-591297143e36 class="margin-5">Happy&nbsp;Hour</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e3-2b24-11e6-b7e5-591297143e36 class="margin-5">Has&nbsp;TV</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e4-2b24-11e6-b7e5-591297143e36 class="margin-5">Music</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e5-2b24-11e6-b7e5-591297143e36 class="margin-10">background_music</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e6-2b24-11e6-b7e5-591297143e36 class="margin-10">dj</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e7-2b24-11e6-b7e5-591297143e36 class="margin-10">jukebox</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e8-2b24-11e6-b7e5-591297143e36 class="margin-10">karaoke</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e9-2b24-11e6-b7e5-591297143e36 class="margin-10">live</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ea-2b24-11e6-b7e5-591297143e36 class="margin-10">video</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811eb-2b24-11e6-b7e5-591297143e36 class="margin-5">Noise&nbsp;Level</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ec-2b24-11e6-b7e5-591297143e36 class="margin-5">Open&nbsp;24&nbsp;Hours</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ed-2b24-11e6-b7e5-591297143e36 class="margin-5">Order&nbsp;at&nbsp;Counter</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ee-2b24-11e6-b7e5-591297143e36 class="margin-5">Outdoor&nbsp;Seating</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ef-2b24-11e6-b7e5-591297143e36 class="margin-5">Parking</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f0-2b24-11e6-b7e5-591297143e36 class="margin-10">garage</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f1-2b24-11e6-b7e5-591297143e36 class="margin-10">lot</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f2-2b24-11e6-b7e5-591297143e36 class="margin-10">street</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f3-2b24-11e6-b7e5-591297143e36 class="margin-10">valet</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f4-2b24-11e6-b7e5-591297143e36 class="margin-10">validated</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f5-2b24-11e6-b7e5-591297143e36 class="margin-5">Price&nbsp;Range</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f6-2b24-11e6-b7e5-591297143e36 class="margin-5">Smoking</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f7-2b24-11e6-b7e5-591297143e36 class="margin-5">Take-out</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f8-2b24-11e6-b7e5-591297143e36 class="margin-5">Takes&nbsp;Reservations</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f9-2b24-11e6-b7e5-591297143e36 class="margin-5">Waiter&nbsp;Service</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fa-2b24-11e6-b7e5-591297143e36 class="margin-5">Wheelchair&nbsp;Accessible</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fb-2b24-11e6-b7e5-591297143e36 class="margin-5">Wi-Fi</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fd-2b24-11e6-b7e5-591297143e36 class="margin-0">categories</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fe-2b24-11e6-b7e5-591297143e36 class="margin-5">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81201-2b24-11e6-b7e5-591297143e36 class="margin-0">hours</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81202-2b24-11e6-b7e5-591297143e36 class="margin-5">Friday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81203-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81204-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81205-2b24-11e6-b7e5-591297143e36 class="margin-5">Monday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81206-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81207-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81208-2b24-11e6-b7e5-591297143e36 class="margin-5">Saturday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81209-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120a-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120b-2b24-11e6-b7e5-591297143e36 class="margin-5">Sunday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120c-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120d-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120e-2b24-11e6-b7e5-591297143e36 class="margin-5">Thursday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120f-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81210-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81211-2b24-11e6-b7e5-591297143e36 class="margin-5">Tuesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81212-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81213-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81214-2b24-11e6-b7e5-591297143e36 class="margin-5">Wednesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81215-2b24-11e6-b7e5-591297143e36 class="margin-10">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81216-2b24-11e6-b7e5-591297143e36 class="margin-10">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81217-2b24-11e6-b7e5-591297143e36 class="margin-0">latitude</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81218-2b24-11e6-b7e5-591297143e36 class="margin-0">longitude</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121a-2b24-11e6-b7e5-591297143e36 class="margin-0">neighborhoods</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121b-2b24-11e6-b7e5-591297143e36 class="margin-5">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121c-2b24-11e6-b7e5-591297143e36 class="margin-0">open</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121d-2b24-11e6-b7e5-591297143e36 class="margin-0">review_count</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121e-2b24-11e6-b7e5-591297143e36 class="margin-0">stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81220-2b24-11e6-b7e5-591297143e36 class="margin-0">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0dd811fc-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.1 Field **business\_id**

##### 3.1.2.1.3.1.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Description</td><td><div class="docs-markdown"><p>Unique key for businesses</p></div></td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr><tr><td>Comments</td><td><div class="docs-markdown"><p>Sat Nov 04 2017 10:12:00 GMT+0100 (Romance Standard Time): some comments</p></div></td></tr></tbody></table>

### <a id="0dd81219-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.2 Field **name**

##### 3.1.2.1.3.2.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.company.name()</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="06399180-d360-11ec-adc4-432dcbbfc12a"></a>3.1.2.1.3.3 Field **phoneNumber**

##### 3.1.2.1.3.3.1 **phoneNumber** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>phoneNumber</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Faker function</td><td>faker.phone.number('+1-###-###-####')</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="3c5d7210-9df8-11ec-afe5-55c2aa6d0440"></a>3.1.2.1.3.4 Field **business\_address**

##### 3.1.2.1.3.4.1 **business\_address** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image6.png?raw=true)

##### 3.1.2.1.3.4.2 **business\_address** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#f2783d2a-e747-4dce-bacd-afad337fc159 class="margin-NaN">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#36b05f0b-d7de-4a3b-9c53-1286a559cbd9 class="margin-NaN">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8f31cc6d-6b38-415f-b3f4-05a60906eb39 class="margin-NaN">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8ac10954-b0fe-4f7e-8024-8f10c0e56e2e class="margin-NaN">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8673c0e2-894f-40b1-ab14-b21d4ec2ba85 class="margin-NaN">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#1220765a-7bd9-4fbe-bb99-608ddd423dca class="margin-NaN">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.4.3 **business\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_address</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="f2783d2a-e747-4dce-bacd-afad337fc159"></a>3.1.2.1.3.5 Field **houseNum**

##### 3.1.2.1.3.5.1 **houseNum** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>houseNum</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.buildingNumber()</td></tr><tr><td>Sample</td><td>123</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="36b05f0b-d7de-4a3b-9c53-1286a559cbd9"></a>3.1.2.1.3.6 Field **street**

##### 3.1.2.1.3.6.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.street()</td></tr><tr><td>Sample</td><td>Main Street</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="8f31cc6d-6b38-415f-b3f4-05a60906eb39"></a>3.1.2.1.3.7 Field **box**

##### 3.1.2.1.3.7.1 **box** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>box</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.secondaryAddress()</td></tr><tr><td>Sample</td><td>10</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="8ac10954-b0fe-4f7e-8024-8f10c0e56e2e"></a>3.1.2.1.3.8 Field **city**

##### 3.1.2.1.3.8.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.city()</td></tr><tr><td>Sample</td><td>Anytown</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="8673c0e2-894f-40b1-ab14-b21d4ec2ba85"></a>3.1.2.1.3.9 Field **state**

##### 3.1.2.1.3.9.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.state({ abbreviated: true })</td></tr><tr><td>Sample</td><td>CA</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="1220765a-7bd9-4fbe-bb99-608ddd423dca"></a>3.1.2.1.3.10 Field **zip**

##### 3.1.2.1.3.10.1 **zip** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>zip</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.state({ abbreviated: true })</td></tr><tr><td>Sample</td><td>12345</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="4445c459-a91f-418c-9a59-f771b5cc2858"></a>3.1.2.1.3.11 Field **full\_address**

##### 3.1.2.1.3.11.1 **full\_address** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image7.png?raw=true)

##### 3.1.2.1.3.11.2 **full\_address** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#db37ab7b-dc16-43f2-9499-a6ff179ee49a class="margin-NaN">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bf165921-9e1c-44fa-89d9-6cc2b7bc8c18 class="margin-NaN">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#05497756-a7ae-4c65-b4d4-04e346d04e3e class="margin-NaN">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#cbfd60c9-1108-4360-8f0c-ab8bc0bf1ddb class="margin-NaN">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#a4968124-98ec-43fa-8161-3cb86a1f2a0d class="margin-NaN">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#84afa995-565b-41ed-8a48-030c1ba8c1d4 class="margin-NaN">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.11.3 **full\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>full_address</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="db37ab7b-dc16-43f2-9499-a6ff179ee49a"></a>3.1.2.1.3.12 Field **houseNum**

##### 3.1.2.1.3.12.1 **houseNum** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>houseNum</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.buildingNumber()</td></tr><tr><td>Sample</td><td>123</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="bf165921-9e1c-44fa-89d9-6cc2b7bc8c18"></a>3.1.2.1.3.13 Field **street**

##### 3.1.2.1.3.13.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.street()</td></tr><tr><td>Sample</td><td>Main Street</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="05497756-a7ae-4c65-b4d4-04e346d04e3e"></a>3.1.2.1.3.14 Field **box**

##### 3.1.2.1.3.14.1 **box** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>box</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.secondaryAddress()</td></tr><tr><td>Sample</td><td>10</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="cbfd60c9-1108-4360-8f0c-ab8bc0bf1ddb"></a>3.1.2.1.3.15 Field **city**

##### 3.1.2.1.3.15.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.city()</td></tr><tr><td>Sample</td><td>Anytown</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="a4968124-98ec-43fa-8161-3cb86a1f2a0d"></a>3.1.2.1.3.16 Field **state**

##### 3.1.2.1.3.16.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.state({ abbreviated: true })</td></tr><tr><td>Sample</td><td>CA</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="84afa995-565b-41ed-8a48-030c1ba8c1d4"></a>3.1.2.1.3.17 Field **zip**

##### 3.1.2.1.3.17.1 **zip** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>zip</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.location.state({ abbreviated: true })</td></tr><tr><td>Sample</td><td>12345</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd7ead2-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.18 Field **attributes**

##### 3.1.2.1.3.18.1 **attributes** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image8.png?raw=true)

##### 3.1.2.1.3.18.2 **attributes** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd7ead3-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Accepts&nbsp;Credit&nbsp;Cards</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead4-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Accepts&nbsp;Insurance</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead5-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Alcohol</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead6-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Ambience</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae0-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Attire</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae1-2b24-11e6-b7e5-591297143e36 class="margin-NaN">By&nbsp;Appointment&nbsp;Only</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae2-2b24-11e6-b7e5-591297143e36 class="margin-NaN">BYOB/Corkage</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae3-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Caters</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae4-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Coat&nbsp;Check</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae5-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Delivery</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae6-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Dogs&nbsp;Allowed</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae7-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Drive-Thru</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae8-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Good&nbsp;For</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaef-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Good&nbsp;For&nbsp;Dancing</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e0-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Good&nbsp;For&nbsp;Groups</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e1-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Good&nbsp;for&nbsp;Kids</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e2-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Happy&nbsp;Hour</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e3-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Has&nbsp;TV</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e4-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Music</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811eb-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Noise&nbsp;Level</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ec-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Open&nbsp;24&nbsp;Hours</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ed-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Order&nbsp;at&nbsp;Counter</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ee-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Outdoor&nbsp;Seating</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ef-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Parking</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f5-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Price&nbsp;Range</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f6-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Smoking</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f7-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Take-out</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f8-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Takes&nbsp;Reservations</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f9-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Waiter&nbsp;Service</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fa-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Wheelchair&nbsp;Accessible</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fb-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Wi-Fi</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.18.3 **attributes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>attributes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd7ead3-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.19 Field **Accepts Credit Cards**

##### 3.1.2.1.3.19.1 **Accepts Credit Cards** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Accepts Credit Cards</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead4-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.20 Field **Accepts Insurance**

##### 3.1.2.1.3.20.1 **Accepts Insurance** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Accepts Insurance</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead5-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.21 Field **Alcohol**

##### 3.1.2.1.3.21.1 **Alcohol** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Alcohol</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>Full bar</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd7ead6-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.22 Field **Ambience**

##### 3.1.2.1.3.22.1 **Ambience** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image9.png?raw=true)

##### 3.1.2.1.3.22.2 **Ambience** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd7ead7-2b24-11e6-b7e5-591297143e36 class="margin-NaN">casual</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead8-2b24-11e6-b7e5-591297143e36 class="margin-NaN">classy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead9-2b24-11e6-b7e5-591297143e36 class="margin-NaN">divey</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eada-2b24-11e6-b7e5-591297143e36 class="margin-NaN">hipster</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadb-2b24-11e6-b7e5-591297143e36 class="margin-NaN">intimate</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadc-2b24-11e6-b7e5-591297143e36 class="margin-NaN">romantic</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadd-2b24-11e6-b7e5-591297143e36 class="margin-NaN">touristy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eade-2b24-11e6-b7e5-591297143e36 class="margin-NaN">trendy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadf-2b24-11e6-b7e5-591297143e36 class="margin-NaN">upscale</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.22.3 **Ambience** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Ambience</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd7ead7-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.23 Field **casual**

##### 3.1.2.1.3.23.1 **casual** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>casual</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead8-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.24 Field **classy**

##### 3.1.2.1.3.24.1 **classy** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>classy</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead9-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.25 Field **divey**

##### 3.1.2.1.3.25.1 **divey** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>divey</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eada-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.26 Field **hipster**

##### 3.1.2.1.3.26.1 **hipster** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>hipster</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadb-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.27 Field **intimate**

##### 3.1.2.1.3.27.1 **intimate** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>intimate</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadc-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.28 Field **romantic**

##### 3.1.2.1.3.28.1 **romantic** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>romantic</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadd-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.29 Field **touristy**

##### 3.1.2.1.3.29.1 **touristy** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>touristy</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eade-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.30 Field **trendy**

##### 3.1.2.1.3.30.1 **trendy** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>trendy</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadf-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.31 Field **upscale**

##### 3.1.2.1.3.31.1 **upscale** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>upscale</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae0-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.32 Field **Attire**

##### 3.1.2.1.3.32.1 **Attire** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Attire</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>Casual chic</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd7eae1-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.33 Field **By Appointment Only**

##### 3.1.2.1.3.33.1 **By Appointment Only** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>By Appointment Only</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae2-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.34 Field **BYOB/Corkage**

##### 3.1.2.1.3.34.1 **BYOB/Corkage** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>BYOB/Corkage</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd7eae3-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.35 Field **Caters**

##### 3.1.2.1.3.35.1 **Caters** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Caters</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae4-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.36 Field **Coat Check**

##### 3.1.2.1.3.36.1 **Coat Check** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Coat Check</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae5-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.37 Field **Delivery**

##### 3.1.2.1.3.37.1 **Delivery** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Delivery</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae6-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.38 Field **Dogs Allowed**

##### 3.1.2.1.3.38.1 **Dogs Allowed** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Dogs Allowed</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae7-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.39 Field **Drive-Thru**

##### 3.1.2.1.3.39.1 **Drive-Thru** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Drive-Thru</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae8-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.40 Field **Good For**

##### 3.1.2.1.3.40.1 **Good For** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image10.png?raw=true)

##### 3.1.2.1.3.40.2 **Good For** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd7eae9-2b24-11e6-b7e5-591297143e36 class="margin-NaN">breakfast</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaea-2b24-11e6-b7e5-591297143e36 class="margin-NaN">brunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaeb-2b24-11e6-b7e5-591297143e36 class="margin-NaN">dessert</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaec-2b24-11e6-b7e5-591297143e36 class="margin-NaN">dinner</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaed-2b24-11e6-b7e5-591297143e36 class="margin-NaN">latenight</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaee-2b24-11e6-b7e5-591297143e36 class="margin-NaN">lunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.40.3 **Good For** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good For</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd7eae9-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.41 Field **breakfast**

##### 3.1.2.1.3.41.1 **breakfast** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>breakfast</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaea-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.42 Field **brunch**

##### 3.1.2.1.3.42.1 **brunch** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>brunch</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaeb-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.43 Field **dessert**

##### 3.1.2.1.3.43.1 **dessert** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>dessert</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaec-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.44 Field **dinner**

##### 3.1.2.1.3.44.1 **dinner** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>dinner</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaed-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.45 Field **latenight**

##### 3.1.2.1.3.45.1 **latenight** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>latenight</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaee-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.46 Field **lunch**

##### 3.1.2.1.3.46.1 **lunch** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>lunch</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaef-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.47 Field **Good For Dancing**

##### 3.1.2.1.3.47.1 **Good For Dancing** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good For Dancing</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e0-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.48 Field **Good For Groups**

##### 3.1.2.1.3.48.1 **Good For Groups** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good For Groups</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e1-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.49 Field **Good for Kids**

##### 3.1.2.1.3.49.1 **Good for Kids** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good for Kids</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e2-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.50 Field **Happy Hour**

##### 3.1.2.1.3.50.1 **Happy Hour** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Happy Hour</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e3-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.51 Field **Has TV**

##### 3.1.2.1.3.51.1 **Has TV** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Has TV</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e4-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.52 Field **Music**

##### 3.1.2.1.3.52.1 **Music** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image11.png?raw=true)

##### 3.1.2.1.3.52.2 **Music** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811e5-2b24-11e6-b7e5-591297143e36 class="margin-NaN">background_music</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e6-2b24-11e6-b7e5-591297143e36 class="margin-NaN">dj</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e7-2b24-11e6-b7e5-591297143e36 class="margin-NaN">jukebox</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e8-2b24-11e6-b7e5-591297143e36 class="margin-NaN">karaoke</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e9-2b24-11e6-b7e5-591297143e36 class="margin-NaN">live</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ea-2b24-11e6-b7e5-591297143e36 class="margin-NaN">video</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.52.3 **Music** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Music</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd811e5-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.53 Field **background\_music**

##### 3.1.2.1.3.53.1 **background\_music** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>background_music</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e6-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.54 Field **dj**

##### 3.1.2.1.3.54.1 **dj** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>dj</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e7-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.55 Field **jukebox**

##### 3.1.2.1.3.55.1 **jukebox** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>jukebox</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e8-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.56 Field **karaoke**

##### 3.1.2.1.3.56.1 **karaoke** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>karaoke</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e9-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.57 Field **live**

##### 3.1.2.1.3.57.1 **live** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>live</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ea-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.58 Field **video**

##### 3.1.2.1.3.58.1 **video** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>video</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811eb-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.59 Field **Noise Level**

##### 3.1.2.1.3.59.1 **Noise Level** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Noise Level</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd811ec-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.60 Field **Open 24 Hours**

##### 3.1.2.1.3.60.1 **Open 24 Hours** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Open 24 Hours</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ed-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.61 Field **Order at Counter**

##### 3.1.2.1.3.61.1 **Order at Counter** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Order at Counter</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ee-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.62 Field **Outdoor Seating**

##### 3.1.2.1.3.62.1 **Outdoor Seating** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Outdoor Seating</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ef-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.63 Field **Parking**

##### 3.1.2.1.3.63.1 **Parking** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image12.png?raw=true)

##### 3.1.2.1.3.63.2 **Parking** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811f0-2b24-11e6-b7e5-591297143e36 class="margin-NaN">garage</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f1-2b24-11e6-b7e5-591297143e36 class="margin-NaN">lot</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f2-2b24-11e6-b7e5-591297143e36 class="margin-NaN">street</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f3-2b24-11e6-b7e5-591297143e36 class="margin-NaN">valet</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f4-2b24-11e6-b7e5-591297143e36 class="margin-NaN">validated</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.63.3 **Parking** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Parking</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd811f0-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.64 Field **garage**

##### 3.1.2.1.3.64.1 **garage** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>garage</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f1-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.65 Field **lot**

##### 3.1.2.1.3.65.1 **lot** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>lot</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f2-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.66 Field **street**

##### 3.1.2.1.3.66.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f3-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.67 Field **valet**

##### 3.1.2.1.3.67.1 **valet** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>valet</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f4-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.68 Field **validated**

##### 3.1.2.1.3.68.1 **validated** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>validated</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f5-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.69 Field **Price Range**

##### 3.1.2.1.3.69.1 **Price Range** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Price Range</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f6-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.70 Field **Smoking**

##### 3.1.2.1.3.70.1 **Smoking** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Smoking</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd811f7-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.71 Field **Take-out**

##### 3.1.2.1.3.71.1 **Take-out** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Take-out</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f8-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.72 Field **Takes Reservations**

##### 3.1.2.1.3.72.1 **Takes Reservations** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Takes Reservations</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f9-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.73 Field **Waiter Service**

##### 3.1.2.1.3.73.1 **Waiter Service** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Waiter Service</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811fa-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.74 Field **Wheelchair Accessible**

##### 3.1.2.1.3.74.1 **Wheelchair Accessible** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Wheelchair Accessible</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811fb-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.75 Field **Wi-Fi**

##### 3.1.2.1.3.75.1 **Wi-Fi** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Wi-Fi</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd811fd-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.76 Field **categories**

##### 3.1.2.1.3.76.1 **categories** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image13.png?raw=true)

##### 3.1.2.1.3.76.2 **categories** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811fe-2b24-11e6-b7e5-591297143e36 class="margin-NaN">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.76.3 **categories** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>categories</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811fe-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.77 Field **\[0\]**

##### 3.1.2.1.3.77.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81201-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.78 Field **hours**

##### 3.1.2.1.3.78.1 **hours** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image14.png?raw=true)

##### 3.1.2.1.3.78.2 **hours** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81202-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Friday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81205-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Monday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81208-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Saturday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120b-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Sunday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120e-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Thursday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81211-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Tuesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81214-2b24-11e6-b7e5-591297143e36 class="margin-NaN">Wednesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.78.3 **hours** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>hours</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81202-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.79 Field **Friday**

##### 3.1.2.1.3.79.1 **Friday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image15.png?raw=true)

##### 3.1.2.1.3.79.2 **Friday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81203-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81204-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.79.3 **Friday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Friday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81203-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.80 Field **close**

##### 3.1.2.1.3.80.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81204-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.81 Field **open**

##### 3.1.2.1.3.81.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81205-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.82 Field **Monday**

##### 3.1.2.1.3.82.1 **Monday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image16.png?raw=true)

##### 3.1.2.1.3.82.2 **Monday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81206-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81207-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.82.3 **Monday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Monday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81206-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.83 Field **close**

##### 3.1.2.1.3.83.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81207-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.84 Field **open**

##### 3.1.2.1.3.84.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81208-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.85 Field **Saturday**

##### 3.1.2.1.3.85.1 **Saturday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image17.png?raw=true)

##### 3.1.2.1.3.85.2 **Saturday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81209-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120a-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.85.3 **Saturday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Saturday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81209-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.86 Field **close**

##### 3.1.2.1.3.86.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd8120a-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.87 Field **open**

##### 3.1.2.1.3.87.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd8120b-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.88 Field **Sunday**

##### 3.1.2.1.3.88.1 **Sunday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image18.png?raw=true)

##### 3.1.2.1.3.88.2 **Sunday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd8120c-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120d-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.88.3 **Sunday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Sunday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd8120c-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.89 Field **close**

##### 3.1.2.1.3.89.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd8120d-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.90 Field **open**

##### 3.1.2.1.3.90.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd8120e-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.91 Field **Thursday**

##### 3.1.2.1.3.91.1 **Thursday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image19.png?raw=true)

##### 3.1.2.1.3.91.2 **Thursday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd8120f-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81210-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.91.3 **Thursday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Thursday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd8120f-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.92 Field **close**

##### 3.1.2.1.3.92.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81210-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.93 Field **open**

##### 3.1.2.1.3.93.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81211-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.94 Field **Tuesday**

##### 3.1.2.1.3.94.1 **Tuesday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image20.png?raw=true)

##### 3.1.2.1.3.94.2 **Tuesday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81212-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81213-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.94.3 **Tuesday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Tuesday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81212-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.95 Field **close**

##### 3.1.2.1.3.95.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81213-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.96 Field **open**

##### 3.1.2.1.3.96.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81214-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.97 Field **Wednesday**

##### 3.1.2.1.3.97.1 **Wednesday** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image21.png?raw=true)

##### 3.1.2.1.3.97.2 **Wednesday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81215-2b24-11e6-b7e5-591297143e36 class="margin-NaN">close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81216-2b24-11e6-b7e5-591297143e36 class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.97.3 **Wednesday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Wednesday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0dd81215-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.98 Field **close**

##### 3.1.2.1.3.98.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81216-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.99 Field **open**

##### 3.1.2.1.3.99.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd81217-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.100 Field **latitude**

##### 3.1.2.1.3.100.1 **latitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>latitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81218-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.101 Field **longitude**

##### 3.1.2.1.3.101.1 **longitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>longitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121a-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.102 Field **neighborhoods**

##### 3.1.2.1.3.102.1 **neighborhoods** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image22.png?raw=true)

##### 3.1.2.1.3.102.2 **neighborhoods** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd8121b-2b24-11e6-b7e5-591297143e36 class="margin-NaN">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.1.3.102.3 **neighborhoods** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>neighborhoods</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121b-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.103 Field **\[0\]**

##### 3.1.2.1.3.103.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0dd8121c-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.104 Field **open**

##### 3.1.2.1.3.104.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121d-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.105 Field **review\_count**

##### 3.1.2.1.3.105.1 **review\_count** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_count</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0dd8121e-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.106 Field **stars**

##### 3.1.2.1.3.106.1 **stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>stars</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0dd81220-2b24-11e6-b7e5-591297143e36"></a>3.1.2.1.3.107 Field **type**

##### 3.1.2.1.3.107.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

##### 3.1.2.1.4 **businesses** Indexes

<table class="index-table"><thead><tr><td class="table-property-column">Property</td><td class="table-column-property">idx_address</td><td class="table-column-property">idx_city</td></tr></thead><tbody><tr><td>Name</td><td class="table-column-indexes">idx_address</td><td class="table-column-indexes">idx_city</td></tr><tr><td>Activated</td><td class="table-column-indexes">true</td><td class="table-column-indexes">true</td></tr><tr><td>Key</td><td class="table-column-indexes">business_address('ascending')</td><td class="table-column-indexes">city('ascending')</td></tr><tr><td>Unique</td><td class="table-column-indexes">false</td><td class="table-column-indexes">false</td></tr><tr><td>Drop duplicates</td><td class="table-column-indexes">false</td><td class="table-column-indexes">false</td></tr><tr><td>Sparse</td><td class="table-column-indexes">false</td><td class="table-column-indexes">false</td></tr><tr><td>Background indexing</td><td class="table-column-indexes">false</td><td class="table-column-indexes">false</td></tr><tr><td>Storage engine</td><td class="table-column-indexes">WiredTiger</td><td class="table-column-indexes">WiredTiger</td></tr></tbody></table>

##### 3.1.2.1.5 **businesses** Target Script

```
use yelp;

db.createCollection("businesses", {
    "capped": false,
    "validator": {
        "$jsonSchema": {
            "bsonType": "object",
            "title": "businesses",
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

### <a id="0da2aa00-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2 Collection **reviews**

##### 3.1.2.2.1 **reviews** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image23.png?raw=true)

##### 3.1.2.2.2 **reviews** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>reviews</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>Storage engine</td><td>WiredTiger</td></tr><tr><td>Validation level</td><td>Off</td></tr><tr><td>Validation action</td><td>Warn</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

##### 3.1.2.2.3 **reviews** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0da2aa04-2b24-11e6-b7e5-591297143e36 class="margin-0">review_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>pk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa02-2b24-11e6-b7e5-591297143e36 class="margin-0">business_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>fk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa03-2b24-11e6-b7e5-591297143e36 class="margin-0">date</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa05-2b24-11e6-b7e5-591297143e36 class="margin-0">stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa06-2b24-11e6-b7e5-591297143e36 class="margin-0">text</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa07-2b24-11e6-b7e5-591297143e36 class="margin-0">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa08-2b24-11e6-b7e5-591297143e36 class="margin-0">user_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>fk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa09-2b24-11e6-b7e5-591297143e36 class="margin-0">votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0a-2b24-11e6-b7e5-591297143e36 class="margin-5">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0b-2b24-11e6-b7e5-591297143e36 class="margin-5">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0c-2b24-11e6-b7e5-591297143e36 class="margin-5">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0da2aa04-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2.3.1 Field **review\_id**

##### 3.1.2.2.3.1.1 **review\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="0da2aa02-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2.3.2 Field **business\_id**

##### 3.1.2.2.3.2.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Foreign collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Foreign field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

### <a id="0da2aa03-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2.3.3 Field **date**

##### 3.1.2.2.3.3.1 **date** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>date</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.date.past()</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0da2aa05-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2.3.4 Field **stars**

##### 3.1.2.2.3.4.1 **stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>stars</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0da2aa06-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2.3.5 Field **text**

##### 3.1.2.2.3.5.1 **text** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>text</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.lorem.paragraphs(3)</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0da2aa07-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2.3.6 Field **type**

##### 3.1.2.2.3.6.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0da2aa08-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2.3.7 Field **user\_id**

##### 3.1.2.2.3.7.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Foreign collection</td><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td></tr><tr><td>Foreign field</td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

### <a id="0da2aa09-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2.3.8 Field **votes**

##### 3.1.2.2.3.8.1 **votes** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image24.png?raw=true)

##### 3.1.2.2.3.8.2 **votes** Hierarchy

Parent field: **reviews**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0da2aa0a-2b24-11e6-b7e5-591297143e36 class="margin-NaN">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0b-2b24-11e6-b7e5-591297143e36 class="margin-NaN">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0c-2b24-11e6-b7e5-591297143e36 class="margin-NaN">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.2.3.8.3 **votes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>votes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0da2aa0a-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2.3.9 Field **cool**

##### 3.1.2.2.3.9.1 **cool** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cool</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0da2aa0b-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2.3.10 Field **funny**

##### 3.1.2.2.3.10.1 **funny** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>funny</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0da2aa0c-2b24-11e6-b7e5-591297143e36"></a>3.1.2.2.3.11 Field **useful**

##### 3.1.2.2.3.11.1 **useful** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>useful</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

##### 3.1.2.2.4 **reviews** Target Script

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

### <a id="0de02830-2b24-11e6-b7e5-591297143e36"></a>3.1.2.3 Collection **tips**

##### 3.1.2.3.1 **tips** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image25.png?raw=true)

##### 3.1.2.3.2 **tips** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>tips</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>Storage engine</td><td>WiredTiger</td></tr><tr><td>Validation level</td><td>Off</td></tr><tr><td>Validation action</td><td>Warn</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

##### 3.1.2.3.3 **tips** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0de02831-2b24-11e6-b7e5-591297143e36 class="margin-0">_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>pk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02832-2b24-11e6-b7e5-591297143e36 class="margin-0">business_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>fk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02833-2b24-11e6-b7e5-591297143e36 class="margin-0">date</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02834-2b24-11e6-b7e5-591297143e36 class="margin-0">likes</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02835-2b24-11e6-b7e5-591297143e36 class="margin-0">text</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02836-2b24-11e6-b7e5-591297143e36 class="margin-0">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02837-2b24-11e6-b7e5-591297143e36 class="margin-0">user_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>fk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0de02831-2b24-11e6-b7e5-591297143e36"></a>3.1.2.3.3.1 Field **\_id**

##### 3.1.2.3.3.1.1 **\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="0de02832-2b24-11e6-b7e5-591297143e36"></a>3.1.2.3.3.2 Field **business\_id**

##### 3.1.2.3.3.2.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Foreign collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Foreign field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

### <a id="0de02833-2b24-11e6-b7e5-591297143e36"></a>3.1.2.3.3.3 Field **date**

##### 3.1.2.3.3.3.1 **date** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>date</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.date.past()</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0de02834-2b24-11e6-b7e5-591297143e36"></a>3.1.2.3.3.4 Field **likes**

##### 3.1.2.3.3.4.1 **likes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>likes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0de02835-2b24-11e6-b7e5-591297143e36"></a>3.1.2.3.3.5 Field **text**

##### 3.1.2.3.3.5.1 **text** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>text</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0de02836-2b24-11e6-b7e5-591297143e36"></a>3.1.2.3.3.6 Field **type**

##### 3.1.2.3.3.6.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0de02837-2b24-11e6-b7e5-591297143e36"></a>3.1.2.3.3.7 Field **user\_id**

##### 3.1.2.3.3.7.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Foreign collection</td><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td></tr><tr><td>Foreign field</td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

##### 3.1.2.3.4 **tips** Target Script

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

### <a id="0df0f110-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4 Collection **users**

##### 3.1.2.4.1 **users** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image26.png?raw=true)

##### 3.1.2.4.2 **users** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>users</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Description</td><td><div class="docs-markdown"><p>Users description</p></div></td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>Time series</td><td>false</td></tr><tr><td>Storage engine</td><td>WiredTiger</td></tr><tr><td>Validation level</td><td>Off</td></tr><tr><td>Validation action</td><td>Warn</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

##### 3.1.2.4.3 **users** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36 class="margin-0">user_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>pk, dk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f125-2b24-11e6-b7e5-591297143e36 class="margin-0">type</a></td><td class="no-break-word">string</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f123-2b24-11e6-b7e5-591297143e36 class="margin-0">name</a></td><td class="no-break-word">string</td><td>true</td><td></td><td><div class="docs-markdown"><p>First name plus surname</p></div></td><td><div class="docs-markdown"><p>Fri Sep 15 2017 17:31:32 GMT+0200 (Romance Summer Time): MongoDB Demo</p></div></td></tr><tr><td><a href=#0df0f112-2b24-11e6-b7e5-591297143e36 class="margin-0">average_stars</a></td><td class="no-break-word">numeric</td><td>true</td><td></td><td><div class="docs-markdown"><p>Star rating: from 1 to 5.</p></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f113-2b24-11e6-b7e5-591297143e36 class="margin-0">compliments</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f114-2b24-11e6-b7e5-591297143e36 class="margin-5">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f115-2b24-11e6-b7e5-591297143e36 class="margin-5">cute</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f116-2b24-11e6-b7e5-591297143e36 class="margin-5">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f117-2b24-11e6-b7e5-591297143e36 class="margin-5">hot</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f119-2b24-11e6-b7e5-591297143e36 class="margin-5">note</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11a-2b24-11e6-b7e5-591297143e36 class="margin-5">photos</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11b-2b24-11e6-b7e5-591297143e36 class="margin-5">plain</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11c-2b24-11e6-b7e5-591297143e36 class="margin-5">profile</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11d-2b24-11e6-b7e5-591297143e36 class="margin-5">writer</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11e-2b24-11e6-b7e5-591297143e36 class="margin-0">elite</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11f-2b24-11e6-b7e5-591297143e36 class="margin-5">[0]</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f120-2b24-11e6-b7e5-591297143e36 class="margin-0">fans</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f121-2b24-11e6-b7e5-591297143e36 class="margin-0">friends</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f122-2b24-11e6-b7e5-591297143e36 class="margin-5">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f124-2b24-11e6-b7e5-591297143e36 class="margin-0">review_count</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f127-2b24-11e6-b7e5-591297143e36 class="margin-0">votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f128-2b24-11e6-b7e5-591297143e36 class="margin-5">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f129-2b24-11e6-b7e5-591297143e36 class="margin-5">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12a-2b24-11e6-b7e5-591297143e36 class="margin-5">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12b-2b24-11e6-b7e5-591297143e36 class="margin-0">yelping_since</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0df0f126-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.1 Field **user\_id**

##### 3.1.2.4.3.1.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="0df0f125-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.2 Field **type**

##### 3.1.2.4.3.2.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Enum</td><td>user,owner,tester</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0df0f123-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.3 Field **name**

##### 3.1.2.4.3.3.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Description</td><td><div class="docs-markdown"><p>First name plus surname</p></div></td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.helpers.fake('{{person.firstName}} {{person.lastName}}')</td></tr><tr><td>Sample</td><td>John Doe</td></tr><tr><td>Comments</td><td><div class="docs-markdown"><p>Fri Sep 15 2017 17:31:32 GMT+0200 (Romance Summer Time): MongoDB Demo</p></div></td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0df0f112-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.4 Field **average\_stars**

##### 3.1.2.4.3.4.1 **average\_stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>average_stars</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Description</td><td><div class="docs-markdown"><p>Star rating: from 1 to 5.</p></div></td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Unit</td><td>stars</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr><tr><td>Excl max</td><td>false</td></tr><tr><td>Sample</td><td>3</td></tr></tbody></table>

### <a id="0df0f113-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.5 Field **compliments**

##### 3.1.2.4.3.5.1 **compliments** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image27.png?raw=true)

##### 3.1.2.4.3.5.2 **compliments** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f114-2b24-11e6-b7e5-591297143e36 class="margin-NaN">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f115-2b24-11e6-b7e5-591297143e36 class="margin-NaN">cute</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f116-2b24-11e6-b7e5-591297143e36 class="margin-NaN">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f117-2b24-11e6-b7e5-591297143e36 class="margin-NaN">hot</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f119-2b24-11e6-b7e5-591297143e36 class="margin-NaN">note</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11a-2b24-11e6-b7e5-591297143e36 class="margin-NaN">photos</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11b-2b24-11e6-b7e5-591297143e36 class="margin-NaN">plain</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11c-2b24-11e6-b7e5-591297143e36 class="margin-NaN">profile</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11d-2b24-11e6-b7e5-591297143e36 class="margin-NaN">writer</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.4.3.5.3 **compliments** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>compliments</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0df0f114-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.6 Field **cool**

##### 3.1.2.4.3.6.1 **cool** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cool</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f115-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.7 Field **cute**

##### 3.1.2.4.3.7.1 **cute** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cute</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f116-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.8 Field **funny**

##### 3.1.2.4.3.8.1 **funny** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>funny</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f117-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.9 Field **hot**

##### 3.1.2.4.3.9.1 **hot** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>hot</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f119-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.10 Field **note**

##### 3.1.2.4.3.10.1 **note** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>note</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f11a-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.11 Field **photos**

##### 3.1.2.4.3.11.1 **photos** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>photos</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f11b-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.12 Field **plain**

##### 3.1.2.4.3.12.1 **plain** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>plain</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f11c-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.13 Field **profile**

##### 3.1.2.4.3.13.1 **profile** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>profile</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f11d-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.14 Field **writer**

##### 3.1.2.4.3.14.1 **writer** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>writer</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Max value</td><td>5</td></tr></tbody></table>

### <a id="0df0f11e-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.15 Field **elite**

##### 3.1.2.4.3.15.1 **elite** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image28.png?raw=true)

##### 3.1.2.4.3.15.2 **elite** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f11f-2b24-11e6-b7e5-591297143e36 class="margin-NaN">[0]</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.4.3.15.3 **elite** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>elite</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional items</td><td>true</td></tr></tbody></table>

### <a id="0df0f11f-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.16 Field **\[0\]**

##### 3.1.2.4.3.16.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f120-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.17 Field **fans**

##### 3.1.2.4.3.17.1 **fans** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fans</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0df0f121-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.18 Field **friends**

##### 3.1.2.4.3.18.1 **friends** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image29.png?raw=true)

##### 3.1.2.4.3.18.2 **friends** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f122-2b24-11e6-b7e5-591297143e36 class="margin-NaN">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.4.3.18.3 **friends** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>friends</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional items</td><td>true</td></tr></tbody></table>

### <a id="0df0f122-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.19 Field **\[0\]**

##### 3.1.2.4.3.19.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.person.fullName(undefined, undefined, 'female')</td></tr><tr><td>Sample</td><td>Jane Doe</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0df0f124-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.20 Field **review\_count**

##### 3.1.2.4.3.20.1 **review\_count** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_count</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0df0f127-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.21 Field **votes**

##### 3.1.2.4.3.21.1 **votes** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image30.png?raw=true)

##### 3.1.2.4.3.21.2 **votes** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f128-2b24-11e6-b7e5-591297143e36 class="margin-NaN">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f129-2b24-11e6-b7e5-591297143e36 class="margin-NaN">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12a-2b24-11e6-b7e5-591297143e36 class="margin-NaN">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.4.3.21.3 **votes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>votes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

### <a id="0df0f128-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.22 Field **cool**

##### 3.1.2.4.3.22.1 **cool** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cool</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0df0f129-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.23 Field **funny**

##### 3.1.2.4.3.23.1 **funny** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>funny</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0df0f12a-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.24 Field **useful**

##### 3.1.2.4.3.24.1 **useful** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>useful</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Min value</td><td>0</td></tr></tbody></table>

### <a id="0df0f12b-2b24-11e6-b7e5-591297143e36"></a>3.1.2.4.3.25 Field **yelping\_since**

##### 3.1.2.4.3.25.1 **yelping\_since** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>yelping_since</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Faker function</td><td>faker.date.between({ from: '2010-01-01T00:00:00.000Z', to: '2021-12-31T00:00:00 000Z' })</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

##### 3.1.2.4.4 **users** Users (TBD)

<table><thead><tr><td>Username</td><td>Read</td><td>Read Write</td></tr></thead><tbody><tr><td>New User</td><td>false</td><td>false</td></tr></tbody></table>

##### 3.1.2.4.5 **users** Indexes

<table class="index-table"><thead><tr><td class="table-property-column">Property</td><td class="table-column-property">idx_name_stars</td><td class="table-column-property">idx_partial</td></tr></thead><tbody><tr><td>Name</td><td class="table-column-indexes">idx_name_stars</td><td class="table-column-indexes">idx_partial</td></tr><tr><td>Activated</td><td class="table-column-indexes">true</td><td class="table-column-indexes">true</td></tr><tr><td>Key</td><td class="table-column-indexes">name('ascending'), average_stars('descending')</td><td class="table-column-indexes">name('ascending')</td></tr><tr><td>Unique</td><td class="table-column-indexes">true</td><td class="table-column-indexes">true</td></tr><tr><td>Drop duplicates</td><td class="table-column-indexes">true</td><td class="table-column-indexes">false</td></tr><tr><td>Sparse</td><td class="table-column-indexes">true</td><td class="table-column-indexes">false</td></tr><tr><td>Background indexing</td><td class="table-column-indexes">true</td><td class="table-column-indexes">false</td></tr><tr><td>Partial filter exp</td><td class="table-column-indexes"></td><td class="table-column-indexes">{"age" : {"$gte" : 21 } }</td></tr><tr><td>Storage engine</td><td class="table-column-indexes">WiredTiger</td><td class="table-column-indexes">WiredTiger</td></tr></tbody></table>

##### 3.1.2.4.6 **users** Target Script

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
                    "bsonType": "objectId"
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

### <a id="a080d1d0-91f6-11e9-a924-ddc9cd9b071f"></a>3.1.2.5 Collection **checkins**

##### 3.1.2.5.1 **checkins** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image31.png?raw=true)

##### 3.1.2.5.2 **checkins** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>checkins</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>Storage engine</td><td>WiredTiger</td></tr><tr><td>Validation level</td><td>Off</td></tr><tr><td>Validation action</td><td>Warn</td></tr><tr><td>Additional properties</td><td>true</td></tr></tbody></table>

##### 3.1.2.5.3 **checkins** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#9c7dc020-91f6-11e9-a924-ddc9cd9b071f class="margin-0">_id</a></td><td class="no-break-word">objectId</td><td>true</td><td>pk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7dc022-91f6-11e9-a924-ddc9cd9b071f class="margin-0">checkin_info</a></td><td class="no-break-word">document</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e76-91f6-11e9-a924-ddc9cd9b071f class="margin-5">^[a-zA-Z0-9_.-]{3}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e45-91f6-11e9-a924-ddc9cd9b071f class="margin-5">^[a-zA-Z0-9_.-]{4}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e77-91f6-11e9-a924-ddc9cd9b071f class="margin-0">type</a></td><td class="no-break-word">string</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7dc021-91f6-11e9-a924-ddc9cd9b071f class="margin-0">business_id</a></td><td class="no-break-word">string</td><td>true</td><td>fk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="9c7dc020-91f6-11e9-a924-ddc9cd9b071f"></a>3.1.2.5.3.1 Field **\_id**

##### 3.1.2.5.3.1.1 **\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="9c7dc022-91f6-11e9-a924-ddc9cd9b071f"></a>3.1.2.5.3.2 Field **checkin\_info**

##### 3.1.2.5.3.2.1 **checkin\_info** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image32.png?raw=true)

##### 3.1.2.5.3.2.2 **checkin\_info** Hierarchy

Parent field: **checkins**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#9c7e0e76-91f6-11e9-a924-ddc9cd9b071f class="margin-NaN">^[a-zA-Z0-9_.-]{3}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e45-91f6-11e9-a924-ddc9cd9b071f class="margin-NaN">^[a-zA-Z0-9_.-]{4}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.1.2.5.3.2.3 **checkin\_info** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>checkin_info</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="9c7e0e76-91f6-11e9-a924-ddc9cd9b071f"></a>3.1.2.5.3.3 Field **^\[a-zA-Z0-9\_.-\]{3}$**

##### 3.1.2.5.3.3.1 **^\[a-zA-Z0-9\_.-\]{3}$** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>^[a-zA-Z0-9_.-]{3}$</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Sample Name</td><td>9-6</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="9c7e0e45-91f6-11e9-a924-ddc9cd9b071f"></a>3.1.2.5.3.4 Field **^\[a-zA-Z0-9\_.-\]{4}$**

##### 3.1.2.5.3.4.1 **^\[a-zA-Z0-9\_.-\]{4}$** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>^[a-zA-Z0-9_.-]{4}$</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Sample Name</td><td>23-6</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="9c7e0e77-91f6-11e9-a924-ddc9cd9b071f"></a>3.1.2.5.3.5 Field **type**

##### 3.1.2.5.3.5.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>checkin</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="9c7dc021-91f6-11e9-a924-ddc9cd9b071f"></a>3.1.2.5.3.6 Field **business\_id**

##### 3.1.2.5.3.6.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Foreign collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Foreign field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr><tr><td>Sample</td><td>eFA9dqXT5EA_TrMgbo03QQ</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

##### 3.1.2.5.4 **checkins** Indexes

<table class="index-table"><thead><tr><td class="table-property-column">Property</td><td class="table-column-property">_id_</td></tr></thead><tbody><tr><td>Name</td><td class="table-column-indexes">_id_</td></tr><tr><td>Activated</td><td class="table-column-indexes">true</td></tr><tr><td>Key</td><td class="table-column-indexes">_id('ascending')</td></tr></tbody></table>

##### 3.1.2.5.5 **checkins** Target Script

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
                            "bsonType": "number",
                            "title": "^[a-zA-Z0-9_.-]{3}$"
                        },
                        "^[a-zA-Z0-9_.-]{4}$": {
                            "bsonType": "number",
                            "title": "^[a-zA-Z0-9_.-]{4}$"
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

##### 4\. Views

### <a id="5c771580-5193-11e7-b9f2-49270a53df2c"></a>4.1 View **rov\_bussiness**

##### 4.1.1 **rov\_bussiness** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image33.png?raw=true)

##### 4.1.2 **rov\_bussiness** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>View name</td><td>rov_bussiness</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>View on</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Pipeline</td><td>[ { "$project": { "business_id": 1, "name": 1, "full_address": { "houseNum": 1, "street": 1, "box": 1, "city": 1, "state": 1, "zip": 1 }, "type": 1 } } ]</td></tr></tbody></table>

##### 4.1.3 **rov\_bussiness** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#94b971e8-0ab1-4909-ba2a-0f6bd36ae29d class="margin-0">business_id</a></td><td class="no-break-word">objectId</td><td>false</td><td>pk</td><td><div class="docs-markdown"><p>Unique key for businesses</p></div></td><td><div class="docs-markdown"><p>Sat Nov 04 2017 10:12:00 GMT+0100 (Romance Standard Time): some comments</p></div></td></tr><tr><td><a href=#a232e94c-7c9b-473b-9675-42efacc6ece6 class="margin-0">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#4445c459-a91f-418c-9a59-f771b5cc2858 class="margin-0">full_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#40b99e83-38dd-4aef-b0ac-ff1917187c2b class="margin-5">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#698f1525-abd6-4b57-bc52-ad8e471443e0 class="margin-5">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#55c552d5-7b1b-4a81-8941-c52fc84583cc class="margin-5">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c581277e-e249-48f7-af98-39d35e7182cb class="margin-5">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#615a0258-462e-4f9a-96ef-33c768e7925f class="margin-5">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#f83472f5-e902-483e-b117-54488ae70307 class="margin-5">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#f229df59-3fbf-48f4-824a-a3b38795f981 class="margin-0">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="94b971e8-0ab1-4909-ba2a-0f6bd36ae29d"></a>4.1.3.1 Field **business\_id**

##### 4.1.3.1.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="a232e94c-7c9b-473b-9675-42efacc6ece6"></a>4.1.3.2 Field **name**

##### 4.1.3.2.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="4445c459-a91f-418c-9a59-f771b5cc2858"></a>4.1.3.3 Field **full\_address**

##### 4.1.3.3.1 **full\_address** Tree Diagram

##### 4.1.3.3.2 **full\_address** Hierarchy

Parent field: **rov\_bussiness**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#40b99e83-38dd-4aef-b0ac-ff1917187c2b class="margin-NaN">houseNum</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#698f1525-abd6-4b57-bc52-ad8e471443e0 class="margin-NaN">street</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#55c552d5-7b1b-4a81-8941-c52fc84583cc class="margin-NaN">box</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c581277e-e249-48f7-af98-39d35e7182cb class="margin-NaN">city</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#615a0258-462e-4f9a-96ef-33c768e7925f class="margin-NaN">state</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#f83472f5-e902-483e-b117-54488ae70307 class="margin-NaN">zip</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 4.1.3.3.3 **full\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>full_address</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="40b99e83-38dd-4aef-b0ac-ff1917187c2b"></a>4.1.3.4 Field **houseNum**

##### 4.1.3.4.1 **houseNum** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>houseNum</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="698f1525-abd6-4b57-bc52-ad8e471443e0"></a>4.1.3.5 Field **street**

##### 4.1.3.5.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="55c552d5-7b1b-4a81-8941-c52fc84583cc"></a>4.1.3.6 Field **box**

##### 4.1.3.6.1 **box** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>box</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="c581277e-e249-48f7-af98-39d35e7182cb"></a>4.1.3.7 Field **city**

##### 4.1.3.7.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="615a0258-462e-4f9a-96ef-33c768e7925f"></a>4.1.3.8 Field **state**

##### 4.1.3.8.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="f83472f5-e902-483e-b117-54488ae70307"></a>4.1.3.9 Field **zip**

##### 4.1.3.9.1 **zip** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>zip</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="f229df59-3fbf-48f4-824a-a3b38795f981"></a>4.1.3.10 Field **type**

##### 4.1.3.10.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

##### 4.1.4 **rov\_bussiness** Target Script

```
use yelp;

db.createView("rov_bussiness",
	"businesses",
	[
	    {
	        "$project": {
	            "business_id": 1,
	            "name": 1,
	            "full_address": {
	                "houseNum": 1,
	                "street": 1,
	                "box": 1,
	                "city": 1,
	                "state": 1,
	                "zip": 1
	            },
	            "type": 1
	        }
	    }
	]
);
```

### <a id="090874c0-5206-11e7-8e65-9b1d6a151b1d"></a>4.2 View **rov\_reviews**

##### 4.2.1 **rov\_reviews** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image34.png?raw=true)

##### 4.2.2 **rov\_reviews** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>View name</td><td>rov_reviews</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6><span class="name-container">yelp</span></a></td></tr><tr><td>View on</td><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td></tr><tr><td>Pipeline</td><td>[ { "$project": { "business": { "business_id": "$business_id", "name": "$name", "type": "$type", "open": "$open", "stars": "$stars", "review_count": "$review_count", "full_address": { "houseNum": "$houseNum", "street": "$street", "box": "$box", "city": "$city", "state": "$state", "zip": "$zip" }, "city": "$city", "state": "$state", "latitude": "$latitude", "longitude": "$longitude" }, "user": { "user_id": "$user_id", "name": "$name", "type": "$type", "votes": { "cool": "$votes.cool", "funny": "$votes.funny", "useful": "$votes.useful" }, "yelping_since": "$yelping_since" }, "username": { "user_id": "$user_id", "type": "$type", "name": "$name", "average_stars": "$average_stars", "compliments": "$compliments", "elite": "$elite", "fans": "$fans", "friends": "$friends", "review_count": "$review_count", "votes": "$votes", "yelping_since": "$yelping_since" } } }, { "$lookup": { "from": "users", "as": "username", "localField": "user_id", "foreignField": "name" } }, { "$unionWith": "users" }, { "$unionWith": "businesses" } ]</td></tr></tbody></table>

##### 4.2.3 **rov\_reviews** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#31c7d9ba-d2ab-4157-9da1-e30052b7dbd2 class="margin-0">username</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bf4740f7-b066-4834-b340-2beb61923a96 class="margin-5">[0]</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#d62e97af-4f4a-46a1-a3f0-8e3095272224 class="margin-10">user_id</a></td><td class="no-break-word">objectId</td><td>false</td><td>pk</td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#5dae6feb-f43e-4e3f-b2af-949a8977f206 class="margin-10">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#d2e256f4-af97-4f76-909b-b855150a85e2 class="margin-10">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"><p>First name plus surname</p></div></td><td><div class="docs-markdown"><p>Fri Sep 15 2017 17:31:32 GMT+0200 (Romance Summer Time): MongoDB Demo</p></div></td></tr><tr><td><a href=#731a3826-1f3e-418a-a8ca-854de9146f30 class="margin-10">average_stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"><p>Star rating: from 1 to 5.</p></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3708979a-46ff-4d65-af6d-b7dd4908e0f9 class="margin-10">compliments</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f114-2b24-11e6-b7e5-591297143e36 class="margin-15">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f115-2b24-11e6-b7e5-591297143e36 class="margin-15">cute</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f116-2b24-11e6-b7e5-591297143e36 class="margin-15">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f117-2b24-11e6-b7e5-591297143e36 class="margin-15">hot</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f119-2b24-11e6-b7e5-591297143e36 class="margin-15">note</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11a-2b24-11e6-b7e5-591297143e36 class="margin-15">photos</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11b-2b24-11e6-b7e5-591297143e36 class="margin-15">plain</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11c-2b24-11e6-b7e5-591297143e36 class="margin-15">profile</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11d-2b24-11e6-b7e5-591297143e36 class="margin-15">writer</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ab687bcb-0fc6-4e0d-bff4-12f9c18cfe58 class="margin-10">elite</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11f-2b24-11e6-b7e5-591297143e36 class="margin-15">[0]</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bf642ae0-8472-44bf-bdef-d284f9794c36 class="margin-10">fans</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3e08e8b3-fbfe-4983-8d01-9ecfa7df453c class="margin-10">friends</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f122-2b24-11e6-b7e5-591297143e36 class="margin-15">[0]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#dc3f4657-c57b-4846-bcff-5f8559405009 class="margin-10">review_count</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#e1b580dc-eb61-42c2-b28a-526b855ed6d6 class="margin-10">votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f128-2b24-11e6-b7e5-591297143e36 class="margin-15">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f129-2b24-11e6-b7e5-591297143e36 class="margin-15">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12a-2b24-11e6-b7e5-591297143e36 class="margin-15">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#80eaada8-dec4-4ac9-87d6-ac27aee9e4bf class="margin-10">yelping_since</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ea4706fc-0103-4991-a4c2-198cb08206ee class="margin-0">business</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#6f5de18b-d47d-46e3-8105-7ad9600c4ded class="margin-5">business_id</a></td><td class="no-break-word">objectId</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#492a3b33-6faa-467d-8f51-5494a7047432 class="margin-5">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ddc180f4-ee83-4839-96cc-24901f57933e class="margin-5">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#63a66d1b-af25-4381-9d22-d03d01b3a27c class="margin-5">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#f3647e00-fab7-48cb-8b11-27f11d3cf4a1 class="margin-5">stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#1b6da19b-940e-435f-b72d-2103ef4bb2ae class="margin-5">review_count</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#5174bf87-ddb9-45f1-a9cf-a0be4ba7305d class="margin-5">full_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#a1463d2e-8297-42d3-a5e9-50313bfa9be8 class="margin-10">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#83111583-5bcb-4772-afbb-c9a6a3348d37 class="margin-10">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0bc83abc-0fa9-4a4d-a41b-6b3b1494355c class="margin-10">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ca9b3eda-30c4-4480-aeb6-481ef8a004a4 class="margin-10">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#545989db-57f2-49c3-9ef2-e20e09bb67f1 class="margin-10">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#60ae6b1d-7f1f-450b-99a2-8fa3a2615ffc class="margin-10">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bcfd7800-79e5-4fa6-a6dc-cfcf8beca70f class="margin-5">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3a118d62-b189-43cc-a365-556a41e0e870 class="margin-5">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#55fb95c9-6d11-49ae-a893-35c31ec166da class="margin-5">latitude</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#482b18b8-f285-46dc-a570-3f764027d509 class="margin-5">longitude</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#35a6eb0d-8075-4118-b00d-5b3bbe3d3491 class="margin-0">user</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#fd08128d-0267-41b8-a279-f177701bdd2c class="margin-5">user_id</a></td><td class="no-break-word">objectId</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c40f7443-2709-4235-8f54-7e2df6f8da50 class="margin-5">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#d9bc0292-0bf7-4d38-8d93-4cfd68054681 class="margin-5">type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#def3ba2c-ba89-4a54-bb07-970204249754 class="margin-5">votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#aa5143d2-370b-4967-be3b-87c8d6678e43 class="margin-10">cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#dd85f69f-3059-4470-aa7f-38001459b5cf class="margin-10">funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#cec67ce0-2cb9-454a-9e24-46937ba45376 class="margin-10">useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7e93b31c-76cc-4ced-a4aa-d4ef07bcaa29 class="margin-5">yelping_since</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="31c7d9ba-d2ab-4157-9da1-e30052b7dbd2"></a>4.2.3.1 Field **username**

##### 4.2.3.1.1 **username** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image35.png?raw=true)

##### 4.2.3.1.2 **username** Hierarchy

Parent field: **rov\_reviews**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#bf4740f7-b066-4834-b340-2beb61923a96 class="margin-NaN">[0]</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 4.2.3.1.3 **username** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>username</td></tr><tr><td>Technical name</td><td>username</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Unique items</td><td>false</td></tr><tr><td>Additional items</td><td>true</td></tr></tbody></table>

### <a id="bf4740f7-b066-4834-b340-2beb61923a96"></a>4.2.3.2 Field **\[0\] New Field**

##### 4.2.3.2.1 **\[0\] New Field** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image36.png?raw=true)

##### 4.2.3.2.2 **\[0\] New Field** Hierarchy

Parent field: **username**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#d62e97af-4f4a-46a1-a3f0-8e3095272224 class="margin-NaN">user_id</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#5dae6feb-f43e-4e3f-b2af-949a8977f206 class="margin-NaN">type</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#d2e256f4-af97-4f76-909b-b855150a85e2 class="margin-NaN">name</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#731a3826-1f3e-418a-a8ca-854de9146f30 class="margin-NaN">average_stars</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3708979a-46ff-4d65-af6d-b7dd4908e0f9 class="margin-NaN">compliments</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ab687bcb-0fc6-4e0d-bff4-12f9c18cfe58 class="margin-NaN">elite</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bf642ae0-8472-44bf-bdef-d284f9794c36 class="margin-NaN">fans</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3e08e8b3-fbfe-4983-8d01-9ecfa7df453c class="margin-NaN">friends</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#dc3f4657-c57b-4846-bcff-5f8559405009 class="margin-NaN">review_count</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#e1b580dc-eb61-42c2-b28a-526b855ed6d6 class="margin-NaN">votes</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#80eaada8-dec4-4ac9-87d6-ac27aee9e4bf class="margin-NaN">yelping_since</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 4.2.3.2.3 **\[0\] New Field** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="d62e97af-4f4a-46a1-a3f0-8e3095272224"></a>4.2.3.3 Field **user\_id**

##### 4.2.3.3.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="5dae6feb-f43e-4e3f-b2af-949a8977f206"></a>4.2.3.4 Field **type**

##### 4.2.3.4.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="d2e256f4-af97-4f76-909b-b855150a85e2"></a>4.2.3.5 Field **name**

##### 4.2.3.5.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="731a3826-1f3e-418a-a8ca-854de9146f30"></a>4.2.3.6 Field **average\_stars**

##### 4.2.3.6.1 **average\_stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>average_stars</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="3708979a-46ff-4d65-af6d-b7dd4908e0f9"></a>4.2.3.7 Field **compliments**

##### 4.2.3.7.1 **compliments** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>compliments</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="ab687bcb-0fc6-4e0d-bff4-12f9c18cfe58"></a>4.2.3.8 Field **elite**

##### 4.2.3.8.1 **elite** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>elite</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="bf642ae0-8472-44bf-bdef-d284f9794c36"></a>4.2.3.9 Field **fans**

##### 4.2.3.9.1 **fans** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fans</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="3e08e8b3-fbfe-4983-8d01-9ecfa7df453c"></a>4.2.3.10 Field **friends**

##### 4.2.3.10.1 **friends** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>friends</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="dc3f4657-c57b-4846-bcff-5f8559405009"></a>4.2.3.11 Field **review\_count**

##### 4.2.3.11.1 **review\_count** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_count</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="e1b580dc-eb61-42c2-b28a-526b855ed6d6"></a>4.2.3.12 Field **votes**

##### 4.2.3.12.1 **votes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>votes</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="80eaada8-dec4-4ac9-87d6-ac27aee9e4bf"></a>4.2.3.13 Field **yelping\_since**

##### 4.2.3.13.1 **yelping\_since** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>yelping_since</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="ea4706fc-0103-4991-a4c2-198cb08206ee"></a>4.2.3.14 Field **business**

##### 4.2.3.14.1 **business** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image37.png?raw=true)

##### 4.2.3.14.2 **business** Hierarchy

Parent field: **rov\_reviews**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#6f5de18b-d47d-46e3-8105-7ad9600c4ded class="margin-NaN">business_id</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#492a3b33-6faa-467d-8f51-5494a7047432 class="margin-NaN">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ddc180f4-ee83-4839-96cc-24901f57933e class="margin-NaN">type</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#63a66d1b-af25-4381-9d22-d03d01b3a27c class="margin-NaN">open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#f3647e00-fab7-48cb-8b11-27f11d3cf4a1 class="margin-NaN">stars</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#1b6da19b-940e-435f-b72d-2103ef4bb2ae class="margin-NaN">review_count</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#5174bf87-ddb9-45f1-a9cf-a0be4ba7305d class="margin-NaN">full_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#bcfd7800-79e5-4fa6-a6dc-cfcf8beca70f class="margin-NaN">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#3a118d62-b189-43cc-a365-556a41e0e870 class="margin-NaN">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#55fb95c9-6d11-49ae-a893-35c31ec166da class="margin-NaN">latitude</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#482b18b8-f285-46dc-a570-3f764027d509 class="margin-NaN">longitude</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 4.2.3.14.3 **business** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business</td></tr><tr><td>Technical name</td><td>business</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="6f5de18b-d47d-46e3-8105-7ad9600c4ded"></a>4.2.3.15 Field **business\_id**

##### 4.2.3.15.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Technical name</td><td>business_id</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="492a3b33-6faa-467d-8f51-5494a7047432"></a>4.2.3.16 Field **name**

##### 4.2.3.16.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Technical name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="ddc180f4-ee83-4839-96cc-24901f57933e"></a>4.2.3.17 Field **type**

##### 4.2.3.17.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="63a66d1b-af25-4381-9d22-d03d01b3a27c"></a>4.2.3.18 Field **open**

##### 4.2.3.18.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Technical name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="f3647e00-fab7-48cb-8b11-27f11d3cf4a1"></a>4.2.3.19 Field **stars**

##### 4.2.3.19.1 **stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>stars</td></tr><tr><td>Technical name</td><td>stars</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="1b6da19b-940e-435f-b72d-2103ef4bb2ae"></a>4.2.3.20 Field **review\_count**

##### 4.2.3.20.1 **review\_count** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_count</td></tr><tr><td>Technical name</td><td>review_count</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="5174bf87-ddb9-45f1-a9cf-a0be4ba7305d"></a>4.2.3.21 Field **full\_address**

##### 4.2.3.21.1 **full\_address** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image38.png?raw=true)

##### 4.2.3.21.2 **full\_address** Hierarchy

Parent field: **business**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#a1463d2e-8297-42d3-a5e9-50313bfa9be8 class="margin-NaN">houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#83111583-5bcb-4772-afbb-c9a6a3348d37 class="margin-NaN">street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0bc83abc-0fa9-4a4d-a41b-6b3b1494355c class="margin-NaN">box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#ca9b3eda-30c4-4480-aeb6-481ef8a004a4 class="margin-NaN">city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#545989db-57f2-49c3-9ef2-e20e09bb67f1 class="margin-NaN">state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#60ae6b1d-7f1f-450b-99a2-8fa3a2615ffc class="margin-NaN">zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 4.2.3.21.3 **full\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>full_address</td></tr><tr><td>Technical name</td><td>full_address</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="a1463d2e-8297-42d3-a5e9-50313bfa9be8"></a>4.2.3.22 Field **houseNum**

##### 4.2.3.22.1 **houseNum** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>houseNum</td></tr><tr><td>Technical name</td><td>houseNum</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="83111583-5bcb-4772-afbb-c9a6a3348d37"></a>4.2.3.23 Field **street**

##### 4.2.3.23.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Technical name</td><td>street</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="0bc83abc-0fa9-4a4d-a41b-6b3b1494355c"></a>4.2.3.24 Field **box**

##### 4.2.3.24.1 **box** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>box</td></tr><tr><td>Technical name</td><td>box</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="ca9b3eda-30c4-4480-aeb6-481ef8a004a4"></a>4.2.3.25 Field **city**

##### 4.2.3.25.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Technical name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="545989db-57f2-49c3-9ef2-e20e09bb67f1"></a>4.2.3.26 Field **state**

##### 4.2.3.26.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Technical name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="60ae6b1d-7f1f-450b-99a2-8fa3a2615ffc"></a>4.2.3.27 Field **zip**

##### 4.2.3.27.1 **zip** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>zip</td></tr><tr><td>Technical name</td><td>zip</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="bcfd7800-79e5-4fa6-a6dc-cfcf8beca70f"></a>4.2.3.28 Field **city**

##### 4.2.3.28.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Technical name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="3a118d62-b189-43cc-a365-556a41e0e870"></a>4.2.3.29 Field **state**

##### 4.2.3.29.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Technical name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="55fb95c9-6d11-49ae-a893-35c31ec166da"></a>4.2.3.30 Field **latitude**

##### 4.2.3.30.1 **latitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>latitude</td></tr><tr><td>Technical name</td><td>latitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="482b18b8-f285-46dc-a570-3f764027d509"></a>4.2.3.31 Field **longitude**

##### 4.2.3.31.1 **longitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>longitude</td></tr><tr><td>Technical name</td><td>longitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="35a6eb0d-8075-4118-b00d-5b3bbe3d3491"></a>4.2.3.32 Field **user**

##### 4.2.3.32.1 **user** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image39.png?raw=true)

##### 4.2.3.32.2 **user** Hierarchy

Parent field: **rov\_reviews**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#fd08128d-0267-41b8-a279-f177701bdd2c class="margin-NaN">user_id</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c40f7443-2709-4235-8f54-7e2df6f8da50 class="margin-NaN">name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#d9bc0292-0bf7-4d38-8d93-4cfd68054681 class="margin-NaN">type</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#def3ba2c-ba89-4a54-bb07-970204249754 class="margin-NaN">votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7e93b31c-76cc-4ced-a4aa-d4ef07bcaa29 class="margin-NaN">yelping_since</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 4.2.3.32.3 **user** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user</td></tr><tr><td>Technical name</td><td>user</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="fd08128d-0267-41b8-a279-f177701bdd2c"></a>4.2.3.33 Field **user\_id**

##### 4.2.3.33.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Technical name</td><td>user_id</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="c40f7443-2709-4235-8f54-7e2df6f8da50"></a>4.2.3.34 Field **name**

##### 4.2.3.34.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Technical name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

### <a id="d9bc0292-0bf7-4d38-8d93-4cfd68054681"></a>4.2.3.35 Field **type**

##### 4.2.3.35.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="def3ba2c-ba89-4a54-bb07-970204249754"></a>4.2.3.36 Field **votes**

##### 4.2.3.36.1 **votes** Tree Diagram

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image40.png?raw=true)

##### 4.2.3.36.2 **votes** Hierarchy

Parent field: **user**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#aa5143d2-370b-4967-be3b-87c8d6678e43 class="margin-NaN">cool</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#dd85f69f-3059-4470-aa7f-38001459b5cf class="margin-NaN">funny</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#cec67ce0-2cb9-454a-9e24-46937ba45376 class="margin-NaN">useful</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 4.2.3.36.3 **votes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>votes</td></tr><tr><td>Technical name</td><td>votes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>DBRef</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="aa5143d2-370b-4967-be3b-87c8d6678e43"></a>4.2.3.37 Field **cool**

##### 4.2.3.37.1 **cool** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cool</td></tr><tr><td>Technical name</td><td>cool</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="dd85f69f-3059-4470-aa7f-38001459b5cf"></a>4.2.3.38 Field **funny**

##### 4.2.3.38.1 **funny** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>funny</td></tr><tr><td>Technical name</td><td>funny</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="cec67ce0-2cb9-454a-9e24-46937ba45376"></a>4.2.3.39 Field **useful**

##### 4.2.3.39.1 **useful** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>useful</td></tr><tr><td>Technical name</td><td>useful</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="7e93b31c-76cc-4ced-a4aa-d4ef07bcaa29"></a>4.2.3.40 Field **yelping\_since**

##### 4.2.3.40.1 **yelping\_since** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>yelping_since</td></tr><tr><td>Technical name</td><td>yelping_since</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Field-level encryption</td><td>false</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr class="tab-header"><td colspan="2"><b>JsonDetails</b></td></tr><tr><td>Personally Identifiable Information</td><td>false</td></tr><tr><td>Information Classification</td><td>Restricted</td></tr></tbody></table>

##### 4.2.4 **rov\_reviews** Target Script

```
use yelp;

db.createView("rov_reviews",
	"reviews",
	[
	    {
	        "$project": {
	            "business": {
	                "business_id": "$business_id",
	                "name": "$name",
	                "type": "$type",
	                "open": "$open",
	                "stars": "$stars",
	                "review_count": "$review_count",
	                "full_address": {
	                    "houseNum": "$houseNum",
	                    "street": "$street",
	                    "box": "$box",
	                    "city": "$city",
	                    "state": "$state",
	                    "zip": "$zip"
	                },
	                "city": "$city",
	                "state": "$state",
	                "latitude": "$latitude",
	                "longitude": "$longitude"
	            },
	            "user": {
	                "user_id": "$user_id",
	                "name": "$name",
	                "type": "$type",
	                "votes": {
	                    "cool": "$votes.cool",
	                    "funny": "$votes.funny",
	                    "useful": "$votes.useful"
	                },
	                "yelping_since": "$yelping_since"
	            },
	            "username": {
	                "user_id": "$user_id",
	                "type": "$type",
	                "name": "$name",
	                "average_stars": "$average_stars",
	                "compliments": "$compliments",
	                "elite": "$elite",
	                "fans": "$fans",
	                "friends": "$friends",
	                "review_count": "$review_count",
	                "votes": "$votes",
	                "yelping_since": "$yelping_since"
	            }
	        }
	    },
	    {
	        "$lookup": {
	            "from": "users",
	            "as": "username",
	            "localField": "user_id",
	            "foreignField": "name"
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

##### 5\. Relationships

### <a id="8a3660f0-2b26-11e6-b7e5-591297143e36"></a>5.1 Relationship **fk\_tipsBusinesses**

##### 5.1.1 **fk\_tipsBusinesses** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr></tbody></table>

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image41.png?raw=true)![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image42.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td><td><a href=#0de02832-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr></tbody></table>

##### 5.1.2 **fk\_tipsBusinesses** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_tipsBusinesses</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Parent field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td></tr><tr><td>Child field</td><td><a href=#0de02832-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="aa956d50-2b26-11e6-b7e5-591297143e36"></a>5.2 Relationship **fk\_tipsUsers**

##### 5.2.1 **fk\_tipsUsers** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr></tbody></table>

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image43.png?raw=true)![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image44.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td><td><a href=#0de02837-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr></tbody></table>

##### 5.2.2 **fk\_tipsUsers** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_tipsUsers</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td></tr><tr><td>Parent field</td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td></tr><tr><td>Child field</td><td><a href=#0de02837-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="e2514f70-2b26-11e6-b7e5-591297143e36"></a>5.3 Relationship **fk\_reviewsUsers**

##### 5.3.1 **fk\_reviewsUsers** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr></tbody></table>

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image45.png?raw=true)![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image46.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td><td><a href=#0da2aa08-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr></tbody></table>

##### 5.3.2 **fk\_reviewsUsers** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_reviewsUsers</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td></tr><tr><td>Parent field</td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td></tr><tr><td>Child field</td><td><a href=#0da2aa08-2b24-11e6-b7e5-591297143e36>user_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="fb857d40-2b26-11e6-b7e5-591297143e36"></a>5.4 Relationship **fk\_reviewsBusinesses**

##### 5.4.1 **fk\_reviewsBusinesses** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr></tbody></table>

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image47.png?raw=true)![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image48.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td><td><a href=#0da2aa02-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr></tbody></table>

##### 5.4.2 **fk\_reviewsBusinesses** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_reviewsBusinesses</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Parent field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td></tr><tr><td>Child field</td><td><a href=#0da2aa02-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="003231f0-91f7-11e9-a924-ddc9cd9b071f"></a>5.5 Relationship **fk businesses.business\_id to checkins.business\_id**

##### 5.5.1 **fk businesses.business\_id to checkins.business\_id** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr></tbody></table>

![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image49.png?raw=true)![Hackolade image](Yelp%20Challenge%20dataset%20documentation/image50.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#a080d1d0-91f6-11e9-a924-ddc9cd9b071f>checkins</a></td><td><a href=#9c7dc021-91f6-11e9-a924-ddc9cd9b071f>business_id</a></td></tr></tbody></table>

##### 5.5.2 **fk businesses.business\_id to checkins.business\_id** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk businesses.business_id to checkins.business_id</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Parent field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#a080d1d0-91f6-11e9-a924-ddc9cd9b071f>checkins</a></td></tr><tr><td>Child field</td><td><a href=#9c7dc021-91f6-11e9-a924-ddc9cd9b071f>business_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="edges"></a>