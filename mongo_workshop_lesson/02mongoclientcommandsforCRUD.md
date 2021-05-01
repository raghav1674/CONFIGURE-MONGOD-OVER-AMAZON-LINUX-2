## CREATE DATABASE AND SWITCH TO THAT DATABASE:
  
  - use DB_NAME
  
## CREATE ONE DOCUMENT:
  
  #### TO INSERT MULTIPLE OR SINGLE DOCUMENT(S):

  - db.COLLECTION_NAME.insert({ ... }) 

  #### TO INSERT ONE DOCUMENT:

  - db.COLLECTION_NAME.insertOne({ ... })
 
  #### TO INSERT MUTLIPLE DOCUMENTS: 

  - db.COLLECTION_NAME.insertMany([{...},...,{...}]) 


## READ:
 
  #### Actually find will return the cursor to the document and we can iterate over that cursor to get the next document.

  #### FIND BASED ON THE CONDITION AND FIELDS TO SHOW:
  
  - db.COLLECTION_NAME.find({ filterCondition } , { fieldsToShow }) 

  #### FIND ALL:

  - db.COLLECTION_NAME.find() 

  #### FIND ONE BASED ON CONDITION:

  - db.COLLECTION_NAME.findOne({ filterCondtion },{ fieldsToShow })
  	 

  #### FIND AND PRINT IN PREETY FORMAT:

  - db.COLLECTION_NAME.find({ filterCondition } , { fieldsToShow }).preety() 

## UPDATE:


 #### TO UPDATE ONE OR MANY DOCUMENTS:

  - db.COLLECTION_NAME.update({ filterCondition },{ $set:{ newField(s): Value }})

 #### TO UPDATE ONE DOCUMENT:

 - db.COLLECTION_NAME.updateOne({ filterCondition },{ $set:{ newField(s): Value }}) 

 #### TO UPDATE MANY DOCUMENTS:

 - db.COLLECTION_NAME.updateMany({ filterCondition },{ $set:{ newField(s): Value }})


 #### TO UPDATE THE EXISITING FIELD IN THE DOCUMENT:

 - db.COLLECTION_NAME.update({ filterCondition },{ oldField : newValue })

 NOTE: if the condition of filter does not match the old documents it will create a new document with this new field and value.


## DELETE:
 
  #### TO DELETE ONE OR MANY DOCUMENTS:
  
  - db.COLLECTION_NAME.delete({ filterCondition })

  #### TO DELETE ONE DOCUMENT:
 
  - db.COLLECTION_NAME.deleteOne({ filterCondition })

  #### TO DELETE MANY DOCUMENTS:

  - db.COLLECTION_NAME.deleteMany({ filterCondition })



## FILTER CONDITIONS:

    #### $gt:  greater than 

    { FIELD_NAME : { $gt: VALUE } } 

    Other atomic operators: $lt,$lte,$gte,$ne and many ... 


