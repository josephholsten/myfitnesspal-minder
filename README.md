# myfitnesspal-minder

Add a beeminder data point every day you enter a meal in myfitnesspal.

## The Simplest Thing that Could Possible Work

Create a new "Do More" goal at https://www.beeminder.com/new

```
# Install Dependencies
scripts/bootstrap
# Set MyFitnessPal username in environment variable:
export MFP_USERNAME=...
# set MyFitnessPal password in system keyring
myfitnesspal store-password $MFP_USERNAME
# set Beeminder username in environment variable: 
export BM_USERNAME=...
# set Beeminder auth token in system keyring:
keyring set beeminder $BM_USERNAME
# set Beeminder goal name with environment variable:
export BM_GOAL=myfitnesspal
# Run!
bin/myfitnesspal-minder
```

## Thanks

Derived from katrielalex's script: https://gist.github.com/katrielalex/6302010eaf3fb5d25359
