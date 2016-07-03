manifests

	manifest
		standardVersions - Declaration of start for a record using OCDX-Specification v.1.3
	
		id - Unique identifier for manifest
		(is required; is not repeatable)
	
		creator - Name of person creating manifest
		(is required; is not repeatable)
	
		dateCreated - Date that manifest is created
		(is required; is not repeatable)
	
		comment - Details or comments about creator of manifest or the manifest itself
		(is not required; is not repeatable)
	
	researchObject
		title - One sentence title for the dataset
		(is required; is not repeatable)
		
		abstract - Summary of the dataset. Should include dates for creation/capture, institutional affiliations, motivations for data collection, and magnitude of the data. 
		(is required; is not repeatable)
		
		dates
			date - Dates associated with the dataset
			(is required; is repeatable)
			label - Date type, choose one: start, end, retrieved, created
			(is required; is repeatable)
			
		creators
		
			name - Person or organization with a role in producing the dataset
			(is required; is repeatable)
			role - Role played by a creator in creating the datase
			(is not required; is not repeatable)
			label - Corporate sponsor; Grant funder; Primary investigator; Other
			(is not required; is repeatable)
			contact - Creator contact information
			(is required; is repeatable) 
			
	privacyEthics
		oversight - Was institutional oversight applied to data collection and/or analysis? 
		(is required. Is not repeatable)
		
		label - Oversight type, choose one: IRB, REB, REC
		(is not required)
		
		informedConsent - Whether informed consent was obtained or participants were notified of their inclusion
		(is required; is not repeatable)
		
		anonymizedData - Whether anything has been excluded, removed or altered in the dataset in order to protect the identities, integrity and rights of participants
		(is required; is repeatable)
		
			label - Choose one and repeat if necessary: names anonymized, names excluded, date of birth anonymized, date of death anonymized, identifying numbers anonymized, race and ethcnitiy categories anonymized, religious affiliation anonymized, health and wellness data anonymized, location or GPS coordinates anonymized
			
			privacyConsiderations - Any special considerations that need to be taken in order to ensure use or re-use of a dataset maintains the rights and privacy of subjects? 
			(is required; is not repeatable)
			
		provenance
			narrative - Workflow involved in collecting and filtering (or cleaning) the data. Recommended information includes how the data was collected, from where, by whom, and using what applications/scripts/etc
			(is not required; is not repeatable) 
			
		publications - Paper citations
		(is not required; is repeatable)
		
		locations
			location - URL to where the data can be retrieved
			(is not required; is repeatable)
			
			comment
			(is not required; is not repeatable)
				
	files - Container for data. It could include a file that contains a URL to a dynamic, ongoing dataset. Both types of data files could exist in a dataset
		(is required; is repeatable)
			name - Name of each file in the dataset 
			(is required; is not repeatable)
			
			format - File type
			(is required; is not repeatable)
			
			abstract - Decription of file
			(is not required; is not repeatable)
			
			size - Size of disk on file
			(is required; is not repeatable)
			
			url - URL to file
			(is required; is not repeatable)
			
			checksum - Hash of the file contents
			(is required; is not repeatable) 
			 
			permissions - Notices or statements that limit access and use of file
			(is not required; is not repeatable) 
			
			dates
				date - The date that the file was extracted, retrieved or produced
				(is not required; is not repeatable)
				
				label - Date type: Start, end, retrieved
				(is not required; is not repeatable)
