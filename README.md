# bemba-language-corpus


	UPDATES AS OF [06-OCT-2020]
	===========================
	
	DATASET		TARGET		RECORDED	UTTERANCES	STATUS			
	-------		------		--------	----------	------
	- Train		20Hrs		20:35:51	~ 12, 595	100.0%		
	- Valid		02Hrs		TBU		TBU		00.0%
	- Test		01Hrs		TBU		TBU		00.0%
	
	
	FILE ORGANIZATION
	=================
	
	<bemba_language_corpus>
		|
		.-- README.md
		|
		.-- TRACKER.txt
		|
		.-- audio/
		|    |
		|    .-- fold*/
		|	  |
		|	  .-- *_elict/
		|		 |
		|		 .-- *.wav
		|		 |
		|		 .-- *-metadata.json
		|		 |
		|	      	 .-- *_linker.txt
		|		 |
		|		 .-- Session**.txt
		|        
		.-- text/
		|    |
		|    .-- fold*/
		|    |    |
		|    |    .-- AllFiles.txt
		|    |    |
		|    |    .-- Session*.txt
		|    | 
		|    .-- BEEN CORPUS.ods
		|    |    
		|    .-- MAIN_TEXT.txt
		|
		.-- text_source_docs/
			|
			.-- **_fold_**
