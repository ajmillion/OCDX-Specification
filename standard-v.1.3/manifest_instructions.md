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
			
		},
		"provenance": {
			"narrative": "" #Describes the workflow involved in collecting and filtering (or cleaning) the data. This could be a link to someplace that describes the data provenance. Recommended information includes how the data was collected, from where, by whom, and using what applications/scripts/etc. Is not required; is not repeatable. If unknown, unclear or not applicable write No Assertion. 
		},
		"publications": { #Paper citation(s) if applicable. Is not required. Is repeatable. Use APA 6th edition. If unknown, unclear or not applicable write No Assertion. 
			"publication": ""
		},
		"locations": {
			"location": { #Provide a link to where the data can be retrieved from. Is not required; is repeatable. If unknown, unclear or not applicable write No Assertion. 
				"url": {},
				"comment": {} #Statement about the location - for instance, where/how can I get the actual dataset if not from a URL? Not required; not repeatable. If unknown, unclear or not applicable write No Assertion.
			}
		},
		"files": { #Container for attributes below. The file(s) could contain either data, or, it could include a file that contains a URL to a dynamic, ongoing dataset. Both types of data files could exist in a dataset. Is required; is repeatable. If unknown, unclear or not applicable write No Assertion.
			"file": {
				"name": "" #Name of each file in the manifest. Is required; is not repeatable. Transcribe from source. If unknown, unclear or not applicable write No Assertion. 
			},
			"format": "", #File formats researchers will download in order to access the datasets. Is required; is not repeatable. Transcribe from source. If unknown, unclear or not applicable write No Assertion. 
			"abstract": "",  #After downloading and opening files, what will a person be looking at? Text, integers, photos, visualizations of networks etc.? Is not required; is not repeatable. If unknown, unclear or not applicable write No Assertion. 
			"size": "", #Size of disk on file. Is required; is not repeatable. Use international system of quantities file size (written as a number) type. If unknown, unclear or not applicable write No Assertion.
			"url": "", #URL to retrieve dataset. Is required. Is not repeatable. If unknown, unclear or not applicable write No Assertion. 
			"checksum": "" #A hash of the file contents. Is required; is not repeatable. If unknown, unclear write No Assertion. 
		},
		"permissions": "" #Are there any notices or statements that limit access and use of datasets stored in the repository or host site? Are there any steps a researcher should take to gain access to the data source? Are there any types of projects or institutions that will not be permitted to use the data source? Is not required. Is not repeatable. If unknown, unclear or not applicable write No Assertion. 
	},
	"dates": {
		"date": { 
			"date": "" #The date that the dataset was extracted, retrieved or produced. Is not required; is not repeatable. Format: yyy-mm-dd. 
		},
		"label": "" #Date type: Start, end, retrieved, No Assertion.
	},
	"creators": { #Person or persons responsible for the creation of the dataset. Is required; is repeatable. If unknown, unclear or not applicable write No Assertion. 
		"creator": {
			"name": "", #Person or organization with a role in producing the dataset. Is required. Is repeatable. Enter as First name Last name. If unknown, unclear or not applicable write No Assertion. 
			"role": { #The role played by a creator in creating the dataset. Is not required. Is not repeatable. If unknown, unclear or not applicable write No Assertion. 
				"label": "" #Corporate sponsor; Grant funder; Primary investigator; Other, No Assertion.
			}
		},
		"type": {
			"label": "" #Educational institutions; Government; NGO; Individual; Private for profit entity, No Assertion.
		},
		"contact": "" #How to contact the creator. Is required; is repeatable. If unknown, unclear or not applicable write No Assertion.
	}
}
