# Rancher AWS host cleanup

### Info
This template contains a single alpine based image that runs a check every minute to remove terminiated AWS instances from the Rancher environment.

An AWS key and secret are required with permissions to describe instances in order for it to validate the host status.
An assumption is made that the hostname of the host to be checked is the private DNS name assigned by Amazon. The second element of the DNS name would then be the region that the host belongs to.
If this name is different then the host will not be removed from Rancher. Hosts from other providers will generate an error in the log but will be otherwise untouched.

Please try this in a test environment first, whilst it has been tested there may well be a use case that has not been tried.

The source code is available at [https://www.github.com/chrisurwin/rancher-aws-host-cleanup] (https://www.github.com/chrisurwin/rancher-aws-host-cleanup)

