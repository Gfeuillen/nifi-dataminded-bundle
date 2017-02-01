# A collection of customized processors for Apache Nifi

## Installation

`mvn clean install` and copy the `nifi-dataminded-processors-nar-1.0-SNAPSHOT.nar` to the `lib` folder of your Nifi installation.

## Processors
### SimpleTriggeredProcessExecutor

Modified version of `ExecuteProcess`. This processor allows input and you can use expression language on the parameters. The attributes from the incoming FlowFile can be used as arguments of the external tool that you want to call

### ExecuteOracleSQL
Modified version of `ExecuteSQL`. This processor handles Oracle's `NUMBER` type. It will make an educated guess if the content of a `NUMBER` field is either an `Integer`, `Long`, `Float` or `Double` instead of converting it to `String`