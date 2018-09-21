A database of Countries, States and Cities in T-SQL. This is a good tool to have if you are building ecommerce websites that require location data about customers.

Countries fields:
Id INT PRIMARY KEY,
  CountryName varchar(100) NOT NULL,
  iso3 varchar(3) DEFAULT NULL,
  iso2 varchar(2) DEFAULT NULL,
  countrycode int DEFAULT NULL,
  PhoneCode varchar(255) NULL,
  capital varchar(255) NULL,
  currency varchar(255) NULL,
  created_at varchar(255) NULL,
  updated_at varchar(255) NOT NULL,
  flag tinyint NOT NULL
  
  Note the "countrycode" is an ISO 3166-1 value
  
  State fields:
  Id INT PRIMARY KEY,
  StateName VARCHAR(255) NOT NULL,
  CountryId INT NOT NULL,
  created_at VARCHAR(255) NULL,
  updated_at VARCHAR(255) NULL,
  flag tinyint NOT NULL DEFAULT '1'
  
  City fields:
  Id INT PRIMARY KEY,
  CityName varchar(255) NOT NULL,
  StateId INT NOT NULL,
  CountryId INT NOT NULL,
  created_at VARCHAR(255) NOT NULL,
  updated_on VARCHAR(255) NOT NULL,
  flag tinyint NOT NULL DEFAULT '1'

