# Last Mile

A city simulator to test the concept of infrastructure without public roads.

## Terms

* Space - 1 square meter of empty "land"
* Consumer - Item that occupies space either partially or fully
* System - Collection of consumers.

## Setup

The space is kept as simple as possible for the sake of maintaining focus on simulation rather than high visual fidelity. This is subject to change should the simulation be light on resources.

## Constants

Size: 100km^2 (?)
Maximum Consumers: ?
Maximum Entities: ?
Step Resolution: 1/second

## Environment

### Size

## Consumers

### Types

* Residential
* Commercial
* Industrial
* Government/Public

## Entities

### People

People are the major entity and users of the infrastructure. Without them, corporations, infrastructure, the city, and people themselves wouldn't exist. Their types include:

* Employed
* Unemployed

All people have the following attributes:

* ID
  * Type - GUID
* Name
  * Type - String
* Sex
  * Type - Enum
    * Values - [Male, Female]
* Age
  * Type - Number
    * Units - Years
    * Minimum - 0
    * Maximum - 100
* Life Expectancy
  * Type - Number
    * Units - Years
    * Minimum - 0
    * Maximum - 100
* Fertility
  * Type - Number
    * Minimum - 0
    * Maximum - 100
* Income
  * Type - Number
  * Units - United States Dollars
* Balance
  * Type - Number
  * Units - United States Dollars
* Credit
  * Type - Number
  * Units - United States Dollars
* Skill
  * Type - Number
    * Minimum - 0
    * Maximum - 100
* Household
  * Type - Array
    * Type - People
* Preferences
  * Type - Object
    * Properties    
      * Fiscal
        * Type - Number
          * Minimum - 0 (conservative)
          * Maximum - 100 (liberal)
      * Limits
        * Type - Object
          * Walking Distance
            * Type - Number
              * Units - Meters
              * Minimum - 0
              * Maximum - 5000
          * Commute Distance
            * Type - Number
              * Units - Meters
              * Minimum - 0
              * Maximum - 50000
          * Leisure Distance
            * Type - Number
              * Units - Meters
              * Minimum - 0
              * Maximum - 75000

#### Employed

This is a classification of people that produce income or debt. Their behaviors include:

* Schedule to commute to work for up to 40 hours a week
* Pays taxes for household if income is greater than 0
* Schedule to commute to leisure for up to 25 hours a week

#### Unemployed

This is a classification of people that do not produce income or debt. Types include:

* Homeless
* Child
* Retired

### Corporations

Corporations are similar to people in that they share some attributes, but instead of the usual classifications that define people, corporations exist to hire people and must own at least 1 system. Common attributes include:

* ID
  * Type - GUID
* Name
  * Type - String
* Balance
  * Type - Number
  * Units - United States Dollars
* Credit
  * Type - Number
  * Units - United States Dollars
* Employees
  * Type - Array
    * Type - People
* Property
  * Type - Array
    * Type - System
* 

## Major Concepts

