### How to use this image
~~~~
VSTS account name:
https://{VSTS_ACCOUNT}.visualstudio.com
~~~~

~~~~
docker run \
  -e VSTS_ACCOUNT=<name> \
  -e VSTS_TOKEN=<pat> \
  -e VSTS_TOKEN=<token with "Agent Pools (read, manage)" scope> \
  -e VSTS_AGENT=<agent name>
  -e VSTS_POOL=<pool name> \
  -e VSTS_WORK='/var/vsts/$VSTS_AGENT' \
  -v /var/vsts:/var/vsts \
  -d atlemann/vsts-fsharp
~~~~