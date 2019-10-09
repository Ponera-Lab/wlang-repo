# Webarq - CMS Lang

## Introduction

Required this vendor to allow translation on CMS

## Code Samples

To select translation row:

> SomeModel::from('some as al')  
>   ->select('al.column1', 'al.column2')  
>   ->selectTranslate('language-code', 'al.columnTranslate1', 'al.columnTranslate2')  
>   ->where('al.column2', 3)  
>   ->whereTranslate('al.columnTranslate1', 'like', '%something%');  
    
## Installation

Follow these instruction to completed the package installation on your project  
  
1. Add composer repositories
> "minimum-stability": "dev",   
    "repositories": [  
        {  
            "type": "vcs",  
            "url": "git@dev.webarq.info:webarq/vendor-lang-l.5.3.git"  
        }    
    ] ,  
  "require" : {  
          "webarq/lang": "*"  
   }  
  
2. Register the service provider class to the providers array in config/app.php.  
> Webarq\Lang\Laravel\WlProvider::class    

3. Register the facade class to the aliases array in config/app.php  
> 'Wl' => Webarq\Lang\Laravel\WlFacade::class 