---
title: Classe MDM_Policy_Result01_LocalPoliciesSecurityOptions02
description: A \_ classe MDM Policy \_ Result01 \_ LocalPoliciesSecurityOptions02 representa as opções de segurança de políticas locais.
ms.assetid: 75ac4789-781f-4722-8b0a-33e53b307296
keywords:
- Classe MDM_Policy_Result01_LocalPoliciesSecurityOptions02
- Classe MDM_Policy_Result01_LocalPoliciesSecurityOptions02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02.InstanceID
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f1ece3790bf5a6a6ac51310d04661366bbe9e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009252"
---
# <a name="mdm_policy_result01_localpoliciessecurityoptions02-class"></a>\_Classe MDM \_ Result01 \_ LocalPoliciesSecurityOptions02

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A \_ classe MDM Policy \_ Result01 \_ LocalPoliciesSecurityOptions02 representa as opções de segurança de políticas locais.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LocalPoliciesSecurityOptions02
{
  string InstanceID;
  string ParentID;
  sint32 Accounts_BlockMicrosoftAccounts;
  sint32 Accounts_EnableGuestAccountStatus;
  sint32 Accounts_EnableAdministratorAccountStatus;
  sint32 Accounts_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly;
  string Accounts_RenameAdministratorAccount;
  string Accounts_RenameGuestAccount;
  string Devices_RestrictCDROMAccessToLocallyLoggedOnUserOnly;
  sint32 Devices_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters;
  sint32 Devices_AllowUndockWithoutHavingToLogon;
  string Devices_AllowedToFormatAndEjectRemovableMedia;
  sint32 InteractiveLogon_DisplayUserInformationWhenTheSessionIsLocked;
  sint32 Interactivelogon_DoNotDisplayLastSignedIn;
  sint32 Interactivelogon_DoNotDisplayUsernameAtSignIn;
  sint32 Interactivelogon_DoNotRequireCTRLALTDEL;
  sint32 InteractiveLogon_MachineInactivityLimit;
  string InteractiveLogon_MessageTextForUsersAttemptingToLogOn;
  string InteractiveLogon_MessageTitleForUsersAttemptingToLogOn;
  sint32 NetworkAccess_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares;
  sint32 NetworkAccess_RestrictAnonymousAccessToNamedPipesAndShares;
  string NetworkAccess_RestrictClientsAllowedToMakeRemoteCallsToSAM;
  sint32 NetworkSecurity_AllowPKU2UAuthenticationRequests;
  sint32 RecoveryConsole_AllowAutomaticAdministrativeLogon;
  sint32 Shutdown_AllowSystemToBeShutDownWithoutHavingToLogOn;
  sint32 Shutdown_ClearVirtualMemoryPageFile;
  sint32 UserAccountControl_AllowUIAccessApplicationsToPromptForElevation;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForAdministrators;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForStandardUsers;
  sint32 UserAccountControl_DetectApplicationInstallationsAndPromptForElevation;
  sint32 UserAccountControl_OnlyElevateExecutableFilesThatAreSignedAndValidated;
  sint32 UserAccountControl_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations;
  sint32 UserAccountControl_RunAllAdministratorsInAdminApprovalMode;
  sint32 UserAccountControl_SwitchToTheSecureDesktopWhenPromptingForElevation;
  sint32 UserAccountControl_UseAdminApprovalMode;
  sint32 UserAccountControl_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations;
};
```

## <a name="members"></a>Membros

A **classe \_ \_ Result01 \_ LocalPoliciesSecurityOptions02 da política MDM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ \_ Result01 \_ LocalPoliciesSecurityOptions02 da política MDM** tem essas propriedades.

<dl> <dt>

[BlockMicrosoftAccounts de contas \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-blockmicrosoftaccounts)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

Accounts_EnableAdministratorAccountStatus
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

Accounts_EnableGuestAccountStatus
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly de contas \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-limitlocalaccountuseofblankpasswordstoconsolelogononly)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[RenameAdministratorAccount de contas \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameadministratoraccount)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[RenameGuestAccount de contas \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameguestaccount)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[Dispositivos \_ AllowedToFormatAndEjectRemovableMedia](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowedtoformatandejectremovablemedia)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[Dispositivos \_ AllowUndockWithoutHavingToLogon](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowundockwithouthavingtologon)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[Dispositivos \_ PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-preventusersfrominstallingprinterdriverswhenconnectingtosharedprinters)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[Dispositivos \_ RestrictCDROMAccessToLocallyLoggedOnUserOnly](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-restrictcdromaccesstolocallyloggedonuseronly)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[InteractiveLogon \_ DisplayUserInformationWhenTheSessionIsLocked](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-displayuserinformationwhenthesessionislocked)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[Interactivelogon \_ DoNotDisplayLastSignedIn](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplaylastsignedin)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[Interactivelogon \_ DoNotDisplayUsernameAtSignIn](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplayusernameatsignin)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[Interactivelogon \_ DoNotRequireCTRLALTDEL](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotrequirectrlaltdel)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[InteractiveLogon \_ MachineInactivityLimit](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-machineinactivitylimit)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[InteractiveLogon \_ MessageTextForUsersAttemptingToLogOn](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetextforusersattemptingtologon)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[InteractiveLogon \_ MessageTitleForUsersAttemptingToLogOn](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetitleforusersattemptingtologon)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[NetworkAccess \_ DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-donotallowanonymousenumerationofsamaccountsandshares)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[NetworkAccess \_ RestrictAnonymousAccessToNamedPipesAndShares](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictanonymousaccesstonamedpipesandshares)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[NetworkAccess \_ RestrictClientsAllowedToMakeRemoteCallsToSAM](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictclientsallowedtomakeremotecallstosam)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[NetworkSecurity \_ AllowPKU2UAuthenticationRequests](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networksecurity-allowpku2uauthenticationrequests)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[RecoveryConsole \_ AllowAutomaticAdministrativeLogon](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-recoveryconsole-allowautomaticadministrativelogon)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[Desligar \_ AllowSystemToBeShutDownWithoutHavingToLogOn](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-allowsystemtobeshutdownwithouthavingtologon)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[Desligar \_ ClearVirtualMemoryPageFile](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-clearvirtualmemorypagefile)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[AllowUIAccessApplicationsToPromptForElevation de UserAccountControl \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-allowuiaccessapplicationstopromptforelevation)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[BehaviorOfTheElevationPromptForAdministrators de UserAccountControl \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforadministrators)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[BehaviorOfTheElevationPromptForStandardUsers de UserAccountControl \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforstandardusers)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[DetectApplicationInstallationsAndPromptForElevation de UserAccountControl \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-detectapplicationinstallationsandpromptforelevation)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[OnlyElevateExecutableFilesThatAreSignedAndValidated de UserAccountControl \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateexecutablefilesthataresignedandvalidated)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations de UserAccountControl \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateuiaccessapplicationsthatareinstalledinsecurelocations)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[RunAllAdministratorsInAdminApprovalMode de UserAccountControl \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-runalladministratorsinadminapprovalmode)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[SwitchToTheSecureDesktopWhenPromptingForElevation de UserAccountControl \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-switchtothesecuredesktopwhenpromptingforelevation)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[UseAdminApprovalMode de UserAccountControl \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-useadminapprovalmode)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[VirtualizeFileAndRegistryWriteFailuresToPerUserLocations de UserAccountControl \_](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-virtualizefileandregistrywritefailurestoperuserlocations)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

