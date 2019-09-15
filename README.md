# needless-prod-file-removal/interface

An interface that defines some common configuration options for composer-plugins that remove files that are not needed for production.

The idea is to have the possibility for every library maintainer to define files that are needed in a production environment apart from the files in the directories defined in the `autoload` section of the libraries `composer.json`

In a prodution environment only files from the `autoload`-directory should be left over. Everything else is just a possible threat to the server. But sometimes files from other locations are relevant for the code of the library to execute correctly. Those locations can then be defined in the libraries `composer.json` file according to the schema defined here. Those files will then stay in a production environment also.

