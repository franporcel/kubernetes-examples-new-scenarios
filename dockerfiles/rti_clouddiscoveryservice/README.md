## Locate RTI Cloud Discovery Service and its dependant libraries at your current directory
`$ cp -rf $NDDSHOME/resource/app/lib/x64Linux2.6gcc4.4.5 ./lib`

`$ cp -rf $NDDSHOME/resource/app/bin/x64Linux2.6gcc4.4.5/rticlouddiscoveryservice .`

## Build a Docker image
`$ docker build -t rti-clouddiscoveryservice`

## Run a Docker container with your custom XML configuration file
`$ docker run -tdi -v $PWD/rti_license.dat:/app/rti_license.dat -v $PWD/your_config.xml:/app/config.xml -e "ARGS=-cfgName your_config_name" rti-clouddiscoveryservice`
