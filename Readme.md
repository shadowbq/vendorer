Vendorer keeps your vendor files up to date.

 - updateable AND documented dependencies
 - copy-paste-free
 - no unwanted/accidental updates

Install
=======
Install curl and git, then:

    sudo gem install vendorer

Usage
=====
Add a Vendorfile to your project root:

    file 'public/javascripts/jquery.min.js' => 'http://code.jquery.com/jquery-latest.min.js'
    folder 'vendor/plugins/parallel_tests' => 'https://github.com/grosser/parallel_tests.git'

Call `vendorer`

If you added something new: `vendorer`

If you want to update all dependencies: `vendorer update`

If you want to update one dependencies: `vendorer update public/javasctips/jquery.min.js`


TODO
====
 - git branch/commit support
 - `folder 'vendor' do` which will remove everything that is not vendored via Vendorfile on `vendorer update` or `vendorer update vendor`
 - nice error message when no Vendorfile was found
 - block support `folder(....){|folder| `rm -rf "#{folder}/.gitignore"` }`
 - syntax change to `file a, b` + `folder a, b`  

Author
======
[Michael Grosser](http://grosser.it)<br/>
michael@grosser.it<br/>
License: MIT<br/>
[![Build Status](https://secure.travis-ci.org/grosser/vendorer.png)](http://travis-ci.org/grosser/vendorer)
