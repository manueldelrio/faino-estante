All notable changes to this project will be documented in this file. The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) and the project adheres to [Semantic Versioning](https://semver.org/).


* **Major versions** are used for versions of entire system, namedly structure changes that affects to all parts. It is expected that every version of the system follows a *1.x.x* syntax because major changes should have a better place into a fork.

* Addition of new accesories (containers, drawers...) may be reflected in **minor versions**.

* **Patch versions** are suitable for modelling issues and changes in drawings.

Onshape uses its own [Gitflow version management](https://learn.onshape.com/learn/article/gitflow-version-management). In Faino Estante Onshape Document, there are two main branches: master and develop. New features must be created into new branches and merge them into develop branch to test its compatibility before merge all into master. In Github feature branches should not be expected so all changes should be made directly into develop branch (it is expected that changes only concern to exported 2D and 3D files from Onshape and to .md files).


# changelog

## 1.1.0 - 2020-08-26
### Added
* **Full modelled shelving system**. This version includes the following parts:
    * side frames
    * cross beams
    * shelves
    * wall fixations
All parts are exported into 3D models in STEP format and 2D drawings in PDF and DXF format and stored into **files folder**.

* DIWO.md, repository for designers, manufacturers and suppliers.
* files/README.md, files folder explanation
### Changed
* README.md. Added full explanation and images.

## 0.1.0 - 2020-07-10
### Added
- README.md. Brief description and link to shelving system Onshape document.
- LICENSE.md
- CHANGELOG.md
- Files folder for exported models and drawings from Onshape document.
