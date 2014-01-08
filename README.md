- Data Warehousing
	- SQL for reporting and analytics
	- Infrastructure complications
		 - Additional maintenance
		 - Data duplication
		 - ETL processes
		 - Real Time?


 - MongoDB used map/reduce
   - Extremely powerful
   - Intended for complex data analysis
   - Overkill for simple queries

 - Aggregation Framework (new)
   - Declared in JSON, executes in C++
   - Flexible, functional and simple


 - Pipelines
   - Process a stream of documents
   - Series of operators

### Operators
 - $match
   - Filter documents
   - Uses existing query syntax
   - geospatial

 - $project
   - Reshape documents
   - Include, exclude or rename fields
   - Inject computed fields
   - Create sub-document fields

 - $group
   - Group documents by an ID
   - Other output fields are computed
   - Processes all data in memory

 - $unwind
   - Operate on an array field
   - Yield new documents for each array element
   - Pipe to $group to aggregate documents

 - $sort, $limit, $skip
   - Sort documents by one or more fields
   - Limit and skip follow cursor


### Usage
 - collection.aggregate() method
 - aggregate database command

### Limitations
 - Result limited by BSON document size
 - Pipeline operator memory limit
 - Some BSON types unsupported

### Sharding
 - Split pipeline at first $group or $sort
 - Early $match may excuse shards
 - CPU and memory implications for mongos