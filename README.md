# submission-validator
A library written in Python that contains validation methods for submissions that goes into EBI archives.

This library is under development, so any contribution encouraged and welcome.  
Please, create a branch from the latest main branch, do your modification(s) and create a Pull Request against the latest main branch.  
We are going to review it and after careful consideration we might merge it into the main branch.

## Prerequisites
  
- [Python3](https://installpython3.com) should be installed in your environment.  
  
## Installation  
  
        pip install submission-validator  

## Developer Notes

### Publish to PyPI

1. Create PyPI Account through the [registration page](https://pypi.org/account/register/).
    
   Take note that PyPI requires email addresses to be verified before publishing.
   
3. Add a `setup.py` configuration file containing the name and version of the project.

3. Package the project for distribution.
 
        python setup.py sdist
        
    Take note that `setup.py` is configured to build a distribution with name `submission-validator`.
    Currently this PyPI project is owned privately and may require access rights to change. 
    Alternatively, the project name in `setup.py` can be changed so that it can be built and
    uploaded to a different PyPI entry.
    
4. Install [Twine](https://pypi.org/project/twine/)

        pip install twine        
    
5. Upload the distribution package to PyPI. 

        twine upload dist/*
        
    Running `python setup.py sdist` will create a package in the `dist` directory of the project
    base directory. Specific packages can be chosen if preferred instead of the wildcard `*`:
    
        twine upload dist/submission-validator-0.1.0.tar