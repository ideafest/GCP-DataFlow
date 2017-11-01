# GCP-DataFlow

# Compile Locally
mvn compile -e exec:java \
 -Dexec.mainClass=com.example.pipelinesrus.dfp.StarterPipeline
 
 
#Run on Cloud 
mvn compile -e exec:java \
 -Dexec.mainClass=com.example.pipelinesrus.dfp.StarterPipeline \
      -Dexec.args="--project=my-kubernetes-codelab-184319 \
      --stagingLocation=gs://dfp-data-pipeline/staging/ \
      --tempLocation=gs://dfp-data-pipeline/staging/ \
      --runner=DataflowPipelineRunner"
