# Applicative Join (in NoSQL)

Estimated time:
 - Junior: 6 hours (don't give up, it's a difficult one, we know it)
 - Middle: 4 hours
 - Senior: 3 hours
 - Kuzzle: 1 hour

Technologies:
 - Elasticsearch

## Goals

 - Understand client need from basic spec
 - Use vendor SDK
 - Ability to find information in documentation
 - Basic usage of Elasticsearch API
 - Arguments over advantages and limits of a solution

Some key words that interests us: developer experience, KISS, clean code, maintainability

## Description

This challenge aims to reproduce an INNER JOIN in Elasticsearch, a NoSQL database.

The solution have to be generic and developed to be exposed as a library for other developers.

Typically, an extension of Elasticsearch Query DSL, with a new operator to handle join, can be written but any other generic solution you can think of is also good.

The library need to expose a method/class who handle a join query between at least 2 collections.

You need to use Elasticsearch Javascript SDK to send the queries.

Creating a small and meaningful set of data is part of the test, typically we expect at least 2 collections and 1 relationship one-to-many materialized by a foreign key.

Finally, we will ask you to describe the limits of this kind of system.

BONUS:
 - being able to join through any number (depth) of tables (e.g. Book with author from France: books -> authors -> cities -> countries)
 - any kind of optimization
 - something less boring than books, authors, cities, countries etc

## Example usage

I have a collection containing books and another containing authors.

Each book have a foreign key for a document in the autors collection.

I want to retrieve all books which have been wrote by an author born between 1939 and 1945.

## Resources

_It's up to you to look deep into the documentation_

 - [Elasticsearch JS SDK](https://www.elastic.co/guide/en/elasticsearch/client/javascript-api/current/api-reference.html#_search)
 - [Terms Query](https://docs.kuzzle.io/core/2/guides/main-concepts/realtime-engine/)
