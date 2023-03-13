# RestFQL Specification

Version: 1
Date: 2023/03/13

## Overview

The current state of software development requires serving information to multiple consumer applications. Nevertheless, the base technology of the serving side does not support the transformation of information to the different requirements of the consuming sides.
There are also existing technologies that solve this need, nevertheless, they have breaking changes and non-standard usage of the existing protocols, which has side effects like increased complexity of caching systems.

## Goals 

- Allow filtering of the response on data retrieval.
- Follow current rest specification 
- Keep compatibility with the current cache capabilities.
- Not intervene in the data sourcing process.
- work over JSON responses.

## Approach 

To achieve the goals expressed before the taken approach is the use of a query language based defined as a subset of the existing gql that will be passed in the requests of the consumer application as a query parameter field called fql of the standard GET requests.

The producer will interpret this parameter and intercept the response and filter the fields requested in the fql query parameter.




