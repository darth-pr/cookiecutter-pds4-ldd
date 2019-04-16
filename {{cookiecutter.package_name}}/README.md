# Welcome to the {{ cookiecutter.dictionary_name }} Local Data Dictionary (LDD)

The {{ cookiecutter.dictionary_name }} contains high level classes and attributes ...

This is a development repository for the {{ cookiecutter.dictionary_name }} LDD. The official releases of the {{ cookiecutter.dictionary_name }} LDD 
are available at <{{ cookiecutter.release_url }}>. Development releases are available at <{{ cookiecutter.package_url }}/releases }}. 

# {{ cookiecutter.dictionary_name }} LDD

## Dicationary Attributes

The following attributes are being used for ***development*** purposes: 

- Information Model Version: {{ cookiecutter.dev_information_model_version }} 
- Dictionary Version: {{ cookiecutter.dev_dictionary_version }}


## Namespace Attributes

- Namespace Id: {{ cookiecutter.namespace_id }}
- XML Schema Namespace: {{ cookiecutter.schema_namespace }}
- XML Namespace Prefix: {{ cookiecutter.namespace_id }}
- Governance Level: {{ cookiecutter.governance_level }}
- Registration Authority: {{ cookiecutter.registration_authority }}
- Registration Date: {{ cookiecutter.registration_date }}
- Registrar: {{ cookiecutter.registrar }}

## Stewardship

- Steward Name: {{ cookiecutter.steward_name }}
- Steward Id: {{ cookiecutter.steward_id }}
- Steward Lead: {{ cookiecutter.steward_lead }}

### Current Stewards

| Name | Affiliation | Role |
| ---- | ----------- | ----- |

***

# Getting Started

## Useful Resources


## Building the {{ cookiecutter.dictionary_name }} 

```
git clone {{ cookiecutter.package_url }}.git
cd {{ cookiecutter.package_name }}
python setup.py lddtool
```

## Contributing


### Stewards

Stewards of the {{ cookiecutter.dictionary_name }} can commit directly to the dictionary repository but should generally follow the same process as the community. They also determine when, how, or whether a community patch gets merged back into the [canonical dictionary repository]({{ cookiecutter.package_url }}). In order to commit to this repository one needs to be part of the [PDS Dictionary Stewards](https://github.com/orgs/nasa-pds-data-dictionaries/teams/pds-dictionary-stewards) and listed in the [Current Stewards](#Current-Stewards).


### Community

Contributions from the community are welcomed! These contributions will not be a part of an official releases until they pass PDS4 Data Dictionary Release Process. Before official release any community contirbution may be reverted. At the discretion of the steward(s) the requested changes will be merged, altered, or rejected into the the development version of the LDD. Please submit a patch or file an issue following the process described below.


### Submitting a Patch

To contribute a patch, follow these instructions.

1. File a GitHub issue at https://github.com/nasa-pds-data-dictionaries/{{ cookiecutter.package_name }}/issues/new. This will create an issue with an assigned issue ID .

2. [Fork the repo](http://help.github.com/fork-a-repo) on which you're working, clone your forked repo to your local computer, and set up the upstream remote:
    ```
    git clone https://github.com/<YourGitHubUserName>/{{ cookiecutter.package_name }}.git
    git remote add upstream https://github.com/nasa-pds-data-dictionaries/{{ cookiecutter.package_name }}.git
    ```
3. Go into {{ cookiecutter.package_name }} directory
    ```
    cd {{ cookiecutter.package_name }}
    ```
4. Checkout out a new local branch based on your master and update it to the latest. The convention is to name the branch after the current GitHub issue, e.g. {{ cookiecutter.issue }}-xxx where xxx is the issue ID.
    ```
    git checkout -b {{ cookiecutter.issue }}-xxx
    ```
5. Do the changes to the relavant files and keep your code clean. If you find another bug, you want to fix while being in a new branch, please fix it in a separated branch instead.

6. Add relevant files to the staging  area.
    ```
    git add <files>
    ```
7. For every commit please write a short (max 72 characters) summary of the change. Use markdown syntax for simple styling. Please include any GitHub issue numbers in your summary.
    ```
    git commit -m “[{{ cookiecutter.issue }}-xxx] Put change summary here ”
    ```
    **NEVER leave the commit message blank!** Provide a detailed, clear, and complete description of your commit!

8. Before submitting a pull request, update your branch to the latest code.
    ```
    git checkout master
    git pull --rebase upstream master
    git checkout {{ cookiecutter.issue }}-xxx
    git rebase -i master
    ```
9. Push the code to your forked repository
    ```
    git push origin {{ cookiecutter.package_name }}-xxx
    ```
10. In order to make a pull request,
  * Navigate to the {{ cookiecutter.package_name }} repository you just pushed to (e.g. https://github.com/<YourGitHubUserName>/{{ cookiecutter.package_name }})
  * Click "Pull Request".
  * Write your branch name in the branch field (this is filled with "master" by default)
  * Click "Update Commit Range".
  * Ensure the changesets you introduced are included in the "Commits" tab.
  * Ensure that the "Files Changed" incorporate all of your changes.
  * Fill in some details about your potential patch including a meaningful title.
  * Click "Send pull request".

### Filing an Issue

If you encounter errors in {{ cookiecutter.package_name }} or want to suggest an improvement or a new
feature, please visit the {{ cookiecutter.package_name }} issue tracker 
https://github.com/nasa-pds-data-dictionaries/{{ cookiecutter.package_name }}/issues.  There you can also find the
latest information on known issues and recent bug fixes and enhancements.

***

# {{ cookiecutter.dictionary_name }} Dictionary Releases

## Latest Release:

- Release Date: {{ cookiecutter.dictionary_release_date }} 
- Information Model Version: {{ cookiecutter.information_model_version }}
- Dictionary Version: {{ cookiecutter.dictionary_version }}
- Dictionary: [{{ cookiecutter.dictionary_filename }}]({{ cookiecutter.artifact_repo_url }}/{{ cookiecutter.dictionary_filename }})
- Schema: [{{ cookiecutter.schema_filename }}]({{ cookiecutter.artifact_repo_url }}/{{ cookiecutter.schema_filename }})
- Schematron: [{{ cookiecutter.schematron_filename }}]({{ cookiecutter.artifact_repo_url }}/{{ cookiecutter.schematron_filename }})
- Dictionary Label: [{{ cookiecutter.dictionary_label_filename }}]({{ cookiecutter.artifact_repo_url }}/{{ cookiecutter.dictionary_label_filename }})

## Previous Releases:

| Namespace | Information Model Version | Dictionary Version | Release Artifacts |
| --------- | ------------------------- | ------------------ | ----------------- |

 
