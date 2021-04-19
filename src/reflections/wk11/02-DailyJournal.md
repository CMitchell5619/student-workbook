# Day Two Daily Journal

## AFTERNOON CHALLENGE ##

[Day Two Daily Project](https://github.com/KurtisEberhardt/undertakings)

https://github.com/KurtisEberhardt/undertakings

## Emotions

WebAPis. New, but mostly the same. Feels like a lot of copy paste. 

## Day Two Daily Qs

What is the difference between a primary key and a foreign key

Primary is for the actual table, foreign is the axis for the join.

What is an Alias?

When you use a variable for the table.

Demonstrate how you would query a join statement that would get all of a doctors patients from the following collections:

CREATE TABLE doctors (
  id INT NOT NULL AUTO_INCREMENT,
  -- CODE OMITTED
  PRIMARY KEY (id)
)

CREATE TABLE patients (
  id INT NOT NULL AUTO_INCREMENT,
  -- CODE OMITTED
  PRIMARY KEY (id)
)

CREATE TABLE doctors (
  id INT NOT NULL AUTO_INCREMENT,
  doctorId INT NOT NULL,
  patientId INT NOT NULL,

  FOREIGN KEY (doctorId)
    REFERENCES doctors(id),
  FOREIGN KEY (patientId)
    REFERENCES patients(id),
)