# TFEEL

> Personal project, does not represent Google

Short for Twitter Feeling... simple sentiment analyses over tweeter data for
specific terms using Google Cloud services:

* [Google Container Engine](https://cloud.google.com/container-engine/)
* [Google NLP API](https://cloud.google.com/natural-language/)
* [Google Dataflow](https://cloud.google.com/dataflow/)
* [Google Pub/Sub](https://cloud.google.com/pubsub/)

![tfeel data flow](/../master/images/tfeel-flow.png?raw=true "tfeel data flow")

> All GCP services used in this example can be run under the GCP Free Tier
plan. More more information see https://cloud.google.com/free/

## Configuration

Edit the `scripts/config.sh` file with your Twitter API info. Alternatively
define the following environment variables. Instractions how to configure your Twitter API access codes are found [here](http://docs.inboundnow.com/guide/create-twitter-application/):

```
# export T_CONSUMER_KEY=""
# export T_CONSUMER_SECRET=""
# export T_ACCESS_TOKEN=""
# export T_ACCESS_SECRET=""
```

## Dependencies

`tfeel` depends on a few GCP services. You can setup these servicesmanually followingthe commandsfound in the `scripts/setup.sh` file or just execute that script. This script will also configure a service account for the `tfeel`  application to run under.

## Run

Once all the necessary GC resources have been created (dependencies) you can execute the `tfeel` application using the `scripts/run.sh` script.

## Cleanup

The cleanup of all the resources created in this application can be accomplished by executing the `scripts/cleanup.sh` script.

### TODO

* Tests, yes please
* Minimize account service roles (currently, project editor)
