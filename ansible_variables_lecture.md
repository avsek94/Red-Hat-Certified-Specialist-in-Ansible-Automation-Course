# Variable and Facts

#### What is ansible Variables
* Review on naming convention
  * letter number and underscore only
* where can we declare variable
  * vars, var_files and vars_prompt
  * Command line using -e flag
  * Roles, blocks and inventories

* Essentials variable ise:
  * ```cmd -debug:msg="Look! I'm using my variable{{myvar}}" ```

* A note on quote:
  * ```name:"{{package}}"```

#### Dictionary Variables:
  * keyvalue pairs
    * Only can be done with yaml formarting
    * two ways to access a Dictionary varibles are :

        * ``` employee['name']```
        * ``` employee.name ```


#### Magic Variables

Example of a magic varible is hostvar which can be used to look at facts about the another hosts
Also, there is a group variables that provides a inventory informations.

jinja2 filters can be useful in manipulating text formats.

  ## Make sure to look-up more for jinja2 filters!!!
