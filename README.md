# java-cli-gradle-postgresql-view

## Description
Creates a small database table
called `dog`. This table, `dog`, has been normalized to 3NF.
Two new tables have been added, `breedLookup` and `colorLookup`.

Creates a new table `dog_expanded` that joins
`dog`, `breedLookup` and `colorLookup`.

Added nonclustered indexes on
`dog`.breedId and `dog`.colorId. Turned `dog_expanded` into a view with an implicit index on `dog_expanded`.id.

## Tech stack
- java
- gradle
  - log4j
  - postgres driver

## Docker stack
- postgresql:alpine
- gradle:jdk11

## To run
`sudo ./install.sh -u`

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`
