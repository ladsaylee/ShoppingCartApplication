#Descripption#

Catalog API with MongoDb

MongoDb - NoSql db (Data stored in db in form of Json)
Setup for MongoDb -
"docker pull mongo" in terminal

"docker run -d -p 27017:27017 --name shopping-mongo mongo"

-d -- dettach mode
-p -- port
xxx:xxxx --  local port: docker port


"docker ps" check the running container 

"docker logs -f shopping-mongo" see logs

"docker exec -it shopping-mongo /bin/bash"

-it -- interactive terminal

mongosh -- enter mongodb
show dbs -- shows existing db
use CatalogDb -- it makes a CatalogDb
db.createCollection('Products')
db.Products.insertMany(add json contain to add products)

show collections - to see tables in dbs

--------------api-----------------------

GET - api/v1/Catalog - Listing products and categories
GET - api/v1/Catalog/{id} - Listing products and categories by id
GET - api/v1/Catalog/GetProductByCategory/{Category} - Get products and category
POST - api/v1/Catalog - Create new Product
PUT - api/v1/Catalog - Update Product
DELETE - api/v1/Catalog/{id} - Delete Product


----------Layered architecture--------------
User
UI Component
Presenation Layer (User interation layer)
Business Logic layer ( process data from db)
Data Access Layer (data base operation)
Data source


-----------Respository Design pattern --------

API
Business Object
Repository ----> Mock Repo while testing
DB

