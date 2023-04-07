To run this, a number of paths need to be modified:
 - all the hardcoded paths in config.yml, including the rundir, notebook dir, and catalog json path
 - in the catalog .json file, the path to the .csv file
 
 Two environments also need to be installed, as specified by:
 - nbscuid-basic-demo-env1.yml
 - nbscuid-basic-demo-env2.yml
 
 Following this, the collection can be run by activating an environment with nbscuid installed and running nbscuid-run config.yml.