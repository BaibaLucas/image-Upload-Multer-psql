# image-Upload-Multer-psql
How to implement Image upload using Express and Multer (PSQL)

# Tutorial
## Set up PSQL
```
createdb image_upload
psql image_upload

CREATE TABLE image_files(
id SERIAL NOT NULL PRIMARY KEY,
filename TEXT UNIQUE NOT NULL,
filepath TEXT NOT NULL,
mimetype TEXT NOT NULL,
size BIGINT NOT null,
);
```
## Start server
```
npm start
```
## Upload your picture with Postman

Set Body to form-data, key as "image" and value as "file"
Choose your file
Response return "filename" keep it.

## Show your file on Browser

Acces the route from a browser with filename 
http://localhost:${PORT}/image/${filename}

Enjoy

