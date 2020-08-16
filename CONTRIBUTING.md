Contributing to WESTPA=  
For a more updated version, check https://github.com/westpa/westpa/wiki/WESTPA-Developer%27s-Guide.

==Guidelines:==
* All contributions are submitted by making Pull Requests, ''even from developers who have write permission on the WESTPA repository.'' 
* All code should pass the [[GitHub Actions continuous integration (CI) tests]].
* All code should be documented (Section 5).
* No changes are ever committed without review and approval by a core WESTPA developer. Every effort will be made to respond to a Pull Request (PR) within a week. 

==Development process:==

===1. Post your coding plans===
To post your coding plans, please open an issue or comment on a relevant issue on [[GitHub|https://github.com/westpa/westpa/issues]]. To avoid any duplication of efforts, @ltchong may contact you to set up a videoconferencing call with other developers to discuss your plans. 

===2. Develop your contribution===
If @ltchong or @mczwier confirms that your coding plans are not duplicating existing efforts, create your own copy of the WESTPA repository by clicking on the Fork button on [[GitHub|https://github.com/westpa/westpa]] and develop your contribution in this separate fork. To adhere to the [[Stylistic Guidelines]], make sure you have [[pre-commit|https://pre-commit.com/]] configured and test your contribution locally using [[pytest|https://docs.pytest.org/en/stable]].

All [[GitHub Actions continuous integration (CI) tests]], including unit/functional tests and checks on coding style must pass before submitting your contribution. If any of the CI tests fail, you can find out why by clicking on the “failed” icon (red cross) and inspecting the build and test log. To avoid overuse and waste of this resource, please test your work locally before committing.

All documentation must build properly with Read the Docs. Please check code documentation before committing.

===3. Submit your contribution===
Submit your contribution by making a PR. If your contribution introduces a new feature or changes functionality, please explain in a PR comment. 

===4. Review process===
Reviewers (other developers and interested community members) will comment inline on your PR to help you improve its implementation, documentation, and style. Every single developer working on the project has their code reviewed with the intention of a friendly conversation from which we all learn to improve the quality of the project. 

To update your PR, make your changes on your fork, commit, run tests, and only if they succeed, push to your fork. As soon as those changes are pushed up (to the same branch as before) the PR will update automatically. The [[GitHub Actions CI services]] are triggered after each PR update. If you do not know how to fix the test failures, you may still push your changes and ask for help in a PR comment. 

A PR must be approved by at least one core WESTPA developer before merging. Approval means the core developer has carefully reviewed the changes, and the PR is ready for merging.

===5. Document changes===
Beyond changes to a functions docstring and possible description in the general documentation, if your change introduces any user-facing modifications they may need to be mentioned in the release notes. To add your change to the release notes, you need to create a short file with a summary and place it in CHANGELOG. The file README.rst details the format and filename conventions. If your change introduces a deprecation, make sure to discuss this first on [[GitHub|https://github.com/westpa/westpa/issues]].

===6. Cross referencing issues===
If the PR relates to any issues, you can add the text xref gh-xxxx where xxxx is the number of the issue to GitHub comments. Likewise, if the PR solves an issue, replace the xref with closes, fixes or any of the other flavors GitHub accepts. In the source code, be sure to preface any issue or PR reference with gh-xxxx.

