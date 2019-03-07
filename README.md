# Get-AccessToken
## Description

The purpose of the script is to retrieve an AcceesToken from AzureAD. There script supports several flows.

## Requirements
# A registered application in AzureAD
# ADAL library installed

## Parameters

### -UserPrincipalName

Username to prepopulate when using ADAL

### -ADALPath

Path to Microsoft.IdentityModel.Clients.ActiveDirectory DLL

### -ClientId

Application ID of the registered app

### -Resource

The resource you want the AccessToken for. It is also known as the audience(aud) of a token.

### -RedirectUri

This can be used for entering either "Sign-On URL" for "Web app/API" or "Redirect URI" for "Native" application.

### -PromptBehavior

The ADAL's PromptBehavior. Always, Auto, Never or RefreshSession are valid values. Default is Auto.

### -TokenForResourceExists

Switch to check whether a token for specific resource exists in your ADAL cache.

### -Certificate

The certificate, which is used for Client Credentials flow.

### -Credential

PS credential object for acquiring a token.

### -ClientSecret

The secret, which is used for Client Credentials flow.

### -ClientIdOBO

Application ID of the registered app in the On-Behalf-Of flow.

### -ClientSecretOBO

The secret, which is used in the On-Behalf-Of flow.

### -ResourceOBO

The resource/audience in the On-Behalf-Of flow.

### -Authority

The authority from where you get the token.

### -ClearTokenCache

Clear ADAL cache in order to retrieve a new token. ADAL checks whether you have a token or not before acquiring a new one. This can be helpful for debugging.

### -UseImplicitFlow

Switch for implicit flow.

### -UseAuthCodeFlow

Switch for AuthCode flow.

### -UseOnBehalfOfFlow

Switch for OBO flow.

### -AuthPrompt

When using either Implicit or AuthCode flow, you can set the prompt. login, select_account, consent, admin_consent and none are valid values. Default is none.

### -ParseToken

Switch for parsing the AccessToken.

### -Tenant

Required when using Implicit or AuthCode flow.

### -AccessToken

If you want to parse an existing AccessToken, just provide the value of the token to this parameter.

## Links

### https://docs.microsoft.com/en-us/azure/active-directory/develop/
### https://techcommunity.microsoft.com/t5/Azure-Active-Directory-Identity/Simplifying-our-Azure-AD-Authentication-Flows/ba-p/243928
### https://docs.microsoft.com/en-us/azure/architecture/multitenant-identity/client-assertion
### https://developer.microsoft.com/en-us/graph/docs/concepts/auth_v2_user
### https://tools.ietf.org/rfc/rfc6749.txt
### https://blogs.msdn.microsoft.com/aaddevsup/2018/04/18/query-string-is-not-allowed-in-redirect_uri-for-azure-ad/
### https://tools.ietf.org/html/rfc6819#section-5.2.3.5
