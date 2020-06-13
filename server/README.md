
1. Clone this repo
2. Run `npm install`
3. Run `npm start`

you must setup your database postgres.
type this on your postgres terminal:

Create Database facedatabase;

Create Table users (
    id serial PRIMARY KEY,
    name VARCHAR(100),
    email text UNIQUE NOT NULL,
    entries BIGINT DEFAULT 0,
    joined TIMESTAMP NOT NULL
);

Create Table login (
    id serial PRIMARY KEY,
    hash VARCHAR(100) NOT NULL,
    email text UNIQUE NOT NULL,
);
