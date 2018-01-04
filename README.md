# datapipes-examples

## What is DataPipes?
DataPipes is a lightweight cross-platform app specifically built to orchestrate the flow of data between systems on commodity hardware, which is becoming ever more vital in today’s modern data architecture. This includes the ability to interact with multiple data sources, such as collecting structured or unstructured data from systems that use a variety of data extraction procedures and protocols as well as loading data into disparate systems. DataPipes captures additional activity metrics and metadata during execution to provide lineage and visibility over the flow of data. A common application of DataPipes is to enable the flow of data from on-premise systems and/or cloud services to a data lake repository such as Actio’s FlowHUB. DataPipes can then subsequently be used to cleanse, aggregate, transform and load the data into disparate systems to support the intended business use case.

## How dows DataPipes work?
DataPipes is written in Scala and runs on the JVM, allowing for it to be deployed on Windows, Linux and macOS systems. PipeScript is a human readable DSL (domain specific language) that captures how to orchestrate the flow of data between systems. DataPipes interprets and executes PipeScript. It can read PipeScript instances from your local file system or retrieve up-to-date instructions via an API call.

## Command Line Interface
The command line options for DataPipes are as follows:

```shell
$ ./run
    [-c <configName.conf>]
    [-p <pipeName>]
    [-s] 
    -Dkey1=val1 -Dkey2=val2 ...
```
* -c, --config 
    This is used to specify the configuration file to execute. The default is application.conf.
* -p, --pipe 
    This is used to specify which pipe to execute in the configuration file. The default is the startup pipe specified in the configuration file.
* -s, --service
    The parameter will run DataPipes as a long running service, listening on a predefined port specified in the configuration file.



## Hello World

To run the Hello World example, run the following command:

```shell
$ ./run -c ./examples/helloworld.conf
```

Once DataPipes completes, view the file output.txt