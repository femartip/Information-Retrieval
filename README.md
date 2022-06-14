# Information Retrieval Proyect
Sistem for indexing and searching news. It is divided in this files;    
SAR_Indexer.py - Propgram for indexing files. It extracts the news from a local directory, and saves the index in the current directory.    
SAR_Searcher.py - Program for searching news. Given an indexer, it will give the result of the given querry.    
SAR_lib.py - Library for both programms. All methods used in the previous programs are here.

## Detailed Functionality
   ### Indexer
   
  Usage: SAR_Indexer.py [-h] [-S] [-P] [-M] [-O] newsdir index       
   
  Index a directory with news in json format.      
   
  Positional arguments:      
      newsdir         ->        directory with the news.     
      index        ->       name of the file to save the project object.     
  
  Optional arguments:      
  -h, --help     =>   Show this help message and exit     
  -S, --stem     =>   Compute stem index.     
  -P, --permuterm    =>   Compute permuterm index.     
  -M, --multifield   =>   Compute index for all the fields.     
  -O, --positional   =>   Compute positional index.     

  ### Searcher
  
  Usage: SAR_Searcher.py [-h] [-S] [-N | -C] [-A] [-R] [-Q query | -L qlist | -T test] index       

  Search the index.      

  Positional arguments:      
  index       ->     name of the file with the index object.      
  
  Optional arguments:      
  -h, --help     =>     Show this help message and exit      
  -S, --stem      =>   Use stem index by default.    
  -N, --snippet   =>    Show a snippet of the retrieved documents.     
  -C, --count    =>    Show only the number of documents retrieved.     
  -A, --all     =>    Show all the results. If not used, only the first 10 results are showed. Does not apply with -C and -T options.    
  -R, --rank    =>    Rank results. Does not apply with -C and -T options.     
  -Q query, --query query    =>   Query.     
  -L qlist, --list qlist    =>   File with queries.     
  -T test, --test test     =>    File with queries and results, for testing.      
