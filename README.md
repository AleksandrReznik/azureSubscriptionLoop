# azureSubscriptionLoop
Template/building block for looping through Azure subscriptions. Can be used to perform certain operations in defined set of subscriptions. Can loop all subscriptions or defined set of them (comma separated list).
As an example it performs simple VM inventory. Get VM name, running status, SKU resource group, subscriptionID and save it to CSV file.

.SYNOPSIS
  Looping through selected Azure subscriptions template. Also can be used as example of VM inventory
.DESCRIPTION
  Template/building block for looping through Azure subscriptions. 
  Can be used to perform certain operations in defined set of subscriptions. 
  Can loop all subscriptions or defined set of them (comma separated list).
  As an example makes inventory of all VMs with sizes, running statuses. resource groups
.PARAMETER $tenantID_param
    Tenant ID within which we looping subscriptons through
.PARAMETER $subID_Param
    "" means - loop through all subscriptions you have access to in the tennant specified
    if comma separated list of subscription ID is specified - will traverse only these subscriptions
    if just one subscription ID is specified - will use only this subscription 
.PARAMETER $pathToSaveFiles
    folder where to save csv files, by default (if not specified) will use same folder the script is run from
.INPUTS
  None
.OUTPUTS
  save sample VM data from looped subscription to this file. Name of the file is in 
    <yyyyMMdd-HHmmss>_<tenantID>_VMs.csv
  form.
