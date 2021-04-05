---
title: Classe MDM_Policy_Config01_LocalPoliciesSecurityOptions02
description: A política de MDM \_ \_ Config01 \_ LocalPoliciesSecurityOptions02 configura as opções de segurança de políticas locais.
ms.assetid: 07688109-f14a-4a04-91b2-ee928d8911b4
keywords:
- Classe MDM_Policy_Config01_LocalPoliciesSecurityOptions02
- Classe MDM_Policy_Config01_LocalPoliciesSecurityOptions02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02.InstanceID
- MDM_Policy_Config01_LocalPoliciesSecurityOptions02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf39e1db2f5d6f823667865054a8c72b18dc916f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009346"
---
# <a name="mdm_policy_config01_localpoliciessecurityoptions02-class"></a><span data-ttu-id="426dd-105">\_Classe MDM \_ Config01 \_ LocalPoliciesSecurityOptions02</span><span class="sxs-lookup"><span data-stu-id="426dd-105">MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02 class</span></span>

<span data-ttu-id="426dd-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="426dd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="426dd-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="426dd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="426dd-108">A política de MDM \_ \_ Config01 \_ LocalPoliciesSecurityOptions02 configura as opções de segurança de políticas locais.</span><span class="sxs-lookup"><span data-stu-id="426dd-108">The MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02 configures the local policies security options.</span></span>

<span data-ttu-id="426dd-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="426dd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="426dd-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="426dd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_LocalPoliciesSecurityOptions02
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

## <a name="members"></a><span data-ttu-id="426dd-111">Membros</span><span class="sxs-lookup"><span data-stu-id="426dd-111">Members</span></span>

<span data-ttu-id="426dd-112">A **classe \_ \_ Config01 \_ LocalPoliciesSecurityOptions02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="426dd-112">The **MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02** class has these types of members:</span></span>

-   [<span data-ttu-id="426dd-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="426dd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="426dd-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="426dd-114">Properties</span></span>

<span data-ttu-id="426dd-115">A **classe \_ \_ Config01 \_ LocalPoliciesSecurityOptions02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="426dd-115">The **MDM\_Policy\_Config01\_LocalPoliciesSecurityOptions02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="426dd-116">BlockMicrosoftAccounts de contas \_</span><span class="sxs-lookup"><span data-stu-id="426dd-116">Accounts\_BlockMicrosoftAccounts</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-blockmicrosoftaccounts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="426dd-119">Accounts_EnableAdministratorAccountStatus</span><span class="sxs-lookup"><span data-stu-id="426dd-119">Accounts_EnableAdministratorAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="426dd-122">Accounts_EnableGuestAccountStatus</span><span class="sxs-lookup"><span data-stu-id="426dd-122">Accounts_EnableGuestAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-125">LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly de contas \_</span><span class="sxs-lookup"><span data-stu-id="426dd-125">Accounts\_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-limitlocalaccountuseofblankpasswordstoconsolelogononly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-128">RenameAdministratorAccount de contas \_</span><span class="sxs-lookup"><span data-stu-id="426dd-128">Accounts\_RenameAdministratorAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameadministratoraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426dd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-131">RenameGuestAccount de contas \_</span><span class="sxs-lookup"><span data-stu-id="426dd-131">Accounts\_RenameGuestAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameguestaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426dd-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-134">Dispositivos \_ AllowedToFormatAndEjectRemovableMedia</span><span class="sxs-lookup"><span data-stu-id="426dd-134">Devices\_AllowedToFormatAndEjectRemovableMedia</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowedtoformatandejectremovablemedia)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426dd-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-137">Dispositivos \_ AllowUndockWithoutHavingToLogon</span><span class="sxs-lookup"><span data-stu-id="426dd-137">Devices\_AllowUndockWithoutHavingToLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowundockwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-140">Dispositivos \_ PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span><span class="sxs-lookup"><span data-stu-id="426dd-140">Devices\_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-preventusersfrominstallingprinterdriverswhenconnectingtosharedprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-143">Dispositivos \_ RestrictCDROMAccessToLocallyLoggedOnUserOnly</span><span class="sxs-lookup"><span data-stu-id="426dd-143">Devices\_RestrictCDROMAccessToLocallyLoggedOnUserOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-restrictcdromaccesstolocallyloggedonuseronly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426dd-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="426dd-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="426dd-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426dd-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426dd-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="426dd-149">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="426dd-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-150">InteractiveLogon \_ DisplayUserInformationWhenTheSessionIsLocked</span><span class="sxs-lookup"><span data-stu-id="426dd-150">InteractiveLogon\_DisplayUserInformationWhenTheSessionIsLocked</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-displayuserinformationwhenthesessionislocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-151">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-153">Interactivelogon \_ DoNotDisplayLastSignedIn</span><span class="sxs-lookup"><span data-stu-id="426dd-153">Interactivelogon\_DoNotDisplayLastSignedIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplaylastsignedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-154">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-156">Interactivelogon \_ DoNotDisplayUsernameAtSignIn</span><span class="sxs-lookup"><span data-stu-id="426dd-156">Interactivelogon\_DoNotDisplayUsernameAtSignIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplayusernameatsignin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-157">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-159">Interactivelogon \_ DoNotRequireCTRLALTDEL</span><span class="sxs-lookup"><span data-stu-id="426dd-159">Interactivelogon\_DoNotRequireCTRLALTDEL</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotrequirectrlaltdel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-160">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-161">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-162">InteractiveLogon \_ MachineInactivityLimit</span><span class="sxs-lookup"><span data-stu-id="426dd-162">InteractiveLogon\_MachineInactivityLimit</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-machineinactivitylimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-163">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-164">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-165">InteractiveLogon \_ MessageTextForUsersAttemptingToLogOn</span><span class="sxs-lookup"><span data-stu-id="426dd-165">InteractiveLogon\_MessageTextForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetextforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426dd-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-167">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-168">InteractiveLogon \_ MessageTitleForUsersAttemptingToLogOn</span><span class="sxs-lookup"><span data-stu-id="426dd-168">InteractiveLogon\_MessageTitleForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetitleforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426dd-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-171">NetworkAccess \_ DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span><span class="sxs-lookup"><span data-stu-id="426dd-171">NetworkAccess\_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-donotallowanonymousenumerationofsamaccountsandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-172">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-174">NetworkAccess \_ RestrictAnonymousAccessToNamedPipesAndShares</span><span class="sxs-lookup"><span data-stu-id="426dd-174">NetworkAccess\_RestrictAnonymousAccessToNamedPipesAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictanonymousaccesstonamedpipesandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-175">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-176">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-177">NetworkAccess \_ RestrictClientsAllowedToMakeRemoteCallsToSAM</span><span class="sxs-lookup"><span data-stu-id="426dd-177">NetworkAccess\_RestrictClientsAllowedToMakeRemoteCallsToSAM</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictclientsallowedtomakeremotecallstosam)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426dd-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-179">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-180">NetworkSecurity \_ AllowPKU2UAuthenticationRequests</span><span class="sxs-lookup"><span data-stu-id="426dd-180">NetworkSecurity\_AllowPKU2UAuthenticationRequests</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networksecurity-allowpku2uauthenticationrequests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-181">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-182">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="426dd-183">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="426dd-183">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="426dd-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="426dd-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="426dd-186">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="426dd-186">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-187">RecoveryConsole \_ AllowAutomaticAdministrativeLogon</span><span class="sxs-lookup"><span data-stu-id="426dd-187">RecoveryConsole\_AllowAutomaticAdministrativeLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-recoveryconsole-allowautomaticadministrativelogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-188">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-188">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-189">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-190">Desligar \_ AllowSystemToBeShutDownWithoutHavingToLogOn</span><span class="sxs-lookup"><span data-stu-id="426dd-190">Shutdown\_AllowSystemToBeShutDownWithoutHavingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-allowsystemtobeshutdownwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-191">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-191">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-192">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-193">Desligar \_ ClearVirtualMemoryPageFile</span><span class="sxs-lookup"><span data-stu-id="426dd-193">Shutdown\_ClearVirtualMemoryPageFile</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-clearvirtualmemorypagefile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-194">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-194">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-195">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-196">AllowUIAccessApplicationsToPromptForElevation de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="426dd-196">UserAccountControl\_AllowUIAccessApplicationsToPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-allowuiaccessapplicationstopromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-197">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-197">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-198">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-199">BehaviorOfTheElevationPromptForAdministrators de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="426dd-199">UserAccountControl\_BehaviorOfTheElevationPromptForAdministrators</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-200">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-201">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-202">BehaviorOfTheElevationPromptForStandardUsers de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="426dd-202">UserAccountControl\_BehaviorOfTheElevationPromptForStandardUsers</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforstandardusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-203">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-203">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-204">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-205">DetectApplicationInstallationsAndPromptForElevation de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="426dd-205">UserAccountControl\_DetectApplicationInstallationsAndPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-detectapplicationinstallationsandpromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-206">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-206">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-207">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-208">OnlyElevateExecutableFilesThatAreSignedAndValidated de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="426dd-208">UserAccountControl\_OnlyElevateExecutableFilesThatAreSignedAndValidated</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateexecutablefilesthataresignedandvalidated)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-209">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-210">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-210">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-211">OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="426dd-211">UserAccountControl\_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateuiaccessapplicationsthatareinstalledinsecurelocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-212">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-212">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-213">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-213">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-214">RunAllAdministratorsInAdminApprovalMode de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="426dd-214">UserAccountControl\_RunAllAdministratorsInAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-runalladministratorsinadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-215">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-216">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-216">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-217">SwitchToTheSecureDesktopWhenPromptingForElevation de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="426dd-217">UserAccountControl\_SwitchToTheSecureDesktopWhenPromptingForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-switchtothesecuredesktopwhenpromptingforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-218">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-218">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-219">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-219">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-220">UseAdminApprovalMode de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="426dd-220">UserAccountControl\_UseAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-useadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-221">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-221">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-222">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-222">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="426dd-223">VirtualizeFileAndRegistryWriteFailuresToPerUserLocations de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="426dd-223">UserAccountControl\_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-virtualizefileandregistrywritefailurestoperuserlocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="426dd-224">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="426dd-224">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="426dd-225">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="426dd-225">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="426dd-226">Requisitos</span><span class="sxs-lookup"><span data-stu-id="426dd-226">Requirements</span></span>



| <span data-ttu-id="426dd-227">Requisito</span><span class="sxs-lookup"><span data-stu-id="426dd-227">Requirement</span></span> | <span data-ttu-id="426dd-228">Valor</span><span class="sxs-lookup"><span data-stu-id="426dd-228">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="426dd-229">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="426dd-229">Minimum supported client</span></span><br/> | <span data-ttu-id="426dd-230">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="426dd-230">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="426dd-231">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="426dd-231">Minimum supported server</span></span><br/> | <span data-ttu-id="426dd-232">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="426dd-232">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="426dd-233">Namespace</span><span class="sxs-lookup"><span data-stu-id="426dd-233">Namespace</span></span><br/>                | <span data-ttu-id="426dd-234">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="426dd-234">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="426dd-235">MOF</span><span class="sxs-lookup"><span data-stu-id="426dd-235">MOF</span></span><br/>                      | <dl> <span data-ttu-id="426dd-236"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="426dd-236"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="426dd-237">DLL</span><span class="sxs-lookup"><span data-stu-id="426dd-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="426dd-238"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="426dd-238"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

