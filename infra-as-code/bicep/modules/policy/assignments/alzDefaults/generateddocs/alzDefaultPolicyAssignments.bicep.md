# ALZ Bicep - Default Policy Assignments

Assigns ALZ Default Policies to the Management Group hierarchy

## Parameters

Parameter name | Required | Description
-------------- | -------- | -----------
parTopLevelManagementGroupPrefix | No       | Prefix for the management group hierarchy.
parTopLevelManagementGroupSuffix | No       | Optional suffix for management group names/IDs. Include a dash if needed.
parTopLevelPolicyAssignmentSovereigntyGlobal | No       | Object used to assign SovrBL - Global Policies to the intermediate root MG.'  - `parTopLevelSovereignGlobalPoliciesEnable` - enable/disable deployment of the SovrBL. - `parListOfAllowedLocations` - The list of allowed locations. - `parPolicyEffect` - The effect type.  
parPolicyAssignmentSovereigntyConfidential | No       | Object used to assign SovrBL - Confidential Policies to the confidential landing zone management groups.'  - `parAllowedResourceTypes` - The list of Azure resource types approved for usage. - `parListOfAllowedLocations` - The list of allowed locations. - `parallowedVirtualMachineSKUs` - The list of VM SKUs approved approved for usage. - `parPolicyEffect` - The effect type.  
parPlatformMgAlzDefaultsEnable | No       | Toggle to apply platform policies to the Platform group or child groups.
parLandingZoneChildrenMgAlzDefaultsEnable | No       | Toggle to assign policies to Corp & Online Management Groups under Landing Zones.
parLandingZoneMgConfidentialEnable | No       | Toggle to assign policies to Confidential Corp and Online groups under Landing Zones.
parLogAnalyticsWorkSpaceAndAutomationAccountLocation | No       | Location of Log Analytics Workspace & Automation Account.
parLogAnalyticsWorkspaceResourceId | No       | Resource ID of Log Analytics Workspace.
parDataCollectionRuleVMInsightsResourceId | No       | Resource ID for VM Insights Data Collection Rule.
parDataCollectionRuleChangeTrackingResourceId | No       | Resource ID for Change Tracking Data Collection Rule.
parDataCollectionRuleMDFCSQLResourceId | No       | Resource ID for MDFC SQL Data Collection Rule.
parUserAssignedManagedIdentityResourceId | No       | Resource ID for User Assigned Managed Identity.
parLogAnalyticsWorkspaceLogRetentionInDays | No       | Number of days to retain logs in Log Analytics Workspace.
parAutomationAccountName | No       | Name of the Automation Account.
parMsDefenderForCloudEmailSecurityContact | No       | Email address for Microsoft Defender for Cloud alerts.
parDdosEnabled | No       | enable/disable DDoS Network Protection deployment
parDdosProtectionPlanId | No       | Resource ID of the DDoS Protection Plan
parPrivateDnsResourceGroupId | No       | Resource ID of the Resource Group containing Private DNS Zones.
parPrivateDnsZonesNamesToAuditInCorp | No       | List of Private DNS Zones to audit if deployed in Subscriptions under the Corp Management Group.
parDisableAlzDefaultPolicies | No       | Set Enforcement Mode of all default Pol Asss to Do Not Enforce.
parDisableSlzDefaultPolicies | No       | Set Enforcement Mode of all default sovereign Pol Asss to Do Not Enforce.
parVmBackupExclusionTagName | No       | Tag name for excluding VMs from this policy’s scope.
parVmBackupExclusionTagValue | No       | Tag value for excluding VMs from this policy’s scope
parExcludedPolicyAssignments | No       | Add assignment definition names to exclude specific policies.
parTelemetryOptOut | No       | Set to true to opt out of deployment telemetry.

### parTopLevelManagementGroupPrefix

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Prefix for the management group hierarchy.

- Default value: `alz`

### parTopLevelManagementGroupSuffix

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Optional suffix for management group names/IDs. Include a dash if needed.

### parTopLevelPolicyAssignmentSovereigntyGlobal

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Object used to assign SovrBL - Global Policies to the intermediate root MG.'

- `parTopLevelSovereignGlobalPoliciesEnable` - enable/disable deployment of the SovrBL.
- `parListOfAllowedLocations` - The list of allowed locations.
- `parPolicyEffect` - The effect type.



- Default value: `@{parTopLevelSovereigntyGlobalPoliciesEnable=False; parListOfAllowedLocations=System.Object[]; parPolicyEffect=Deny}`

### parPolicyAssignmentSovereigntyConfidential

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Object used to assign SovrBL - Confidential Policies to the confidential landing zone management groups.'

- `parAllowedResourceTypes` - The list of Azure resource types approved for usage.
- `parListOfAllowedLocations` - The list of allowed locations.
- `parallowedVirtualMachineSKUs` - The list of VM SKUs approved approved for usage.
- `parPolicyEffect` - The effect type.



- Default value: `@{parAllowedResourceTypes=System.Object[]; parListOfAllowedLocations=System.Object[]; parAllowedVirtualMachineSKUs=System.Object[]; parPolicyEffect=Deny}`

### parPlatformMgAlzDefaultsEnable

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Toggle to apply platform policies to the Platform group or child groups.

- Default value: `True`

### parLandingZoneChildrenMgAlzDefaultsEnable

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Toggle to assign policies to Corp & Online Management Groups under Landing Zones.

- Default value: `True`

### parLandingZoneMgConfidentialEnable

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Toggle to assign policies to Confidential Corp and Online groups under Landing Zones.

- Default value: `False`

### parLogAnalyticsWorkSpaceAndAutomationAccountLocation

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Location of Log Analytics Workspace & Automation Account.

- Default value: `eastus`

### parLogAnalyticsWorkspaceResourceId

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Resource ID of Log Analytics Workspace.

### parDataCollectionRuleVMInsightsResourceId

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Resource ID for VM Insights Data Collection Rule.

### parDataCollectionRuleChangeTrackingResourceId

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Resource ID for Change Tracking Data Collection Rule.

### parDataCollectionRuleMDFCSQLResourceId

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Resource ID for MDFC SQL Data Collection Rule.

### parUserAssignedManagedIdentityResourceId

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Resource ID for User Assigned Managed Identity.

### parLogAnalyticsWorkspaceLogRetentionInDays

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Number of days to retain logs in Log Analytics Workspace.

- Default value: `365`

### parAutomationAccountName

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Name of the Automation Account.

- Default value: `alz-automation-account`

### parMsDefenderForCloudEmailSecurityContact

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Email address for Microsoft Defender for Cloud alerts.

- Default value: `security_contact@replace_me.com`

### parDdosEnabled

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

enable/disable DDoS Network Protection deployment

- Default value: `True`

### parDdosProtectionPlanId

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Resource ID of the DDoS Protection Plan

### parPrivateDnsResourceGroupId

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Resource ID of the Resource Group containing Private DNS Zones.

### parPrivateDnsZonesNamesToAuditInCorp

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

List of Private DNS Zones to audit if deployed in Subscriptions under the Corp Management Group.

### parDisableAlzDefaultPolicies

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Set Enforcement Mode of all default Pol Asss to Do Not Enforce.

- Default value: `False`

### parDisableSlzDefaultPolicies

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Set Enforcement Mode of all default sovereign Pol Asss to Do Not Enforce.

- Default value: `False`

### parVmBackupExclusionTagName

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Tag name for excluding VMs from this policy’s scope.

### parVmBackupExclusionTagValue

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Tag value for excluding VMs from this policy’s scope

### parExcludedPolicyAssignments

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Add assignment definition names to exclude specific policies.

### parTelemetryOptOut

![Parameter Setting](https://img.shields.io/badge/parameter-optional-green?style=flat-square)

Set to true to opt out of deployment telemetry.

- Default value: `False`

## Snippets

### Parameter file

```json
{
    "$schema": "https://schema.management.azure.com/schemas/2015-01-01/deploymentParameters.json#",
    "contentVersion": "1.0.0.0",
    "metadata": {
        "template": "infra-as-code/bicep/modules/policy/assignments/alzDefaults/alzDefaultPolicyAssignments.json"
    },
    "parameters": {
        "parTopLevelManagementGroupPrefix": {
            "value": "alz"
        },
        "parTopLevelManagementGroupSuffix": {
            "value": ""
        },
        "parTopLevelPolicyAssignmentSovereigntyGlobal": {
            "value": {
                "parTopLevelSovereigntyGlobalPoliciesEnable": false,
                "parListOfAllowedLocations": [],
                "parPolicyEffect": "Deny"
            }
        },
        "parPolicyAssignmentSovereigntyConfidential": {
            "value": {
                "parAllowedResourceTypes": [],
                "parListOfAllowedLocations": [],
                "parAllowedVirtualMachineSKUs": [],
                "parPolicyEffect": "Deny"
            }
        },
        "parPlatformMgAlzDefaultsEnable": {
            "value": true
        },
        "parLandingZoneChildrenMgAlzDefaultsEnable": {
            "value": true
        },
        "parLandingZoneMgConfidentialEnable": {
            "value": false
        },
        "parLogAnalyticsWorkSpaceAndAutomationAccountLocation": {
            "value": "eastus"
        },
        "parLogAnalyticsWorkspaceResourceId": {
            "value": ""
        },
        "parDataCollectionRuleVMInsightsResourceId": {
            "value": ""
        },
        "parDataCollectionRuleChangeTrackingResourceId": {
            "value": ""
        },
        "parDataCollectionRuleMDFCSQLResourceId": {
            "value": ""
        },
        "parUserAssignedManagedIdentityResourceId": {
            "value": ""
        },
        "parLogAnalyticsWorkspaceLogRetentionInDays": {
            "value": "365"
        },
        "parAutomationAccountName": {
            "value": "alz-automation-account"
        },
        "parMsDefenderForCloudEmailSecurityContact": {
            "value": "security_contact@replace_me.com"
        },
        "parDdosEnabled": {
            "value": true
        },
        "parDdosProtectionPlanId": {
            "value": ""
        },
        "parPrivateDnsResourceGroupId": {
            "value": ""
        },
        "parPrivateDnsZonesNamesToAuditInCorp": {
            "value": []
        },
        "parDisableAlzDefaultPolicies": {
            "value": false
        },
        "parDisableSlzDefaultPolicies": {
            "value": false
        },
        "parVmBackupExclusionTagName": {
            "value": ""
        },
        "parVmBackupExclusionTagValue": {
            "value": []
        },
        "parExcludedPolicyAssignments": {
            "value": []
        },
        "parTelemetryOptOut": {
            "value": false
        }
    }
}
```
