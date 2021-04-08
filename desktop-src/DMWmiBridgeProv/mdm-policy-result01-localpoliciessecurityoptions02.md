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
# <a name="mdm_policy_result01_localpoliciessecurityoptions02-class"></a><span data-ttu-id="086ac-105">\_Classe MDM \_ Result01 \_ LocalPoliciesSecurityOptions02</span><span class="sxs-lookup"><span data-stu-id="086ac-105">MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02 class</span></span>

<span data-ttu-id="086ac-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="086ac-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="086ac-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="086ac-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="086ac-108">A \_ classe MDM Policy \_ Result01 \_ LocalPoliciesSecurityOptions02 representa as opções de segurança de políticas locais.</span><span class="sxs-lookup"><span data-stu-id="086ac-108">The MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02 class represents the local policies security options.</span></span>

<span data-ttu-id="086ac-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="086ac-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="086ac-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="086ac-110">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="086ac-111">Membros</span><span class="sxs-lookup"><span data-stu-id="086ac-111">Members</span></span>

<span data-ttu-id="086ac-112">A **classe \_ \_ Result01 \_ LocalPoliciesSecurityOptions02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="086ac-112">The **MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02** class has these types of members:</span></span>

-   [<span data-ttu-id="086ac-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="086ac-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="086ac-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="086ac-114">Properties</span></span>

<span data-ttu-id="086ac-115">A **classe \_ \_ Result01 \_ LocalPoliciesSecurityOptions02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="086ac-115">The **MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="086ac-116">BlockMicrosoftAccounts de contas \_</span><span class="sxs-lookup"><span data-stu-id="086ac-116">Accounts\_BlockMicrosoftAccounts</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-blockmicrosoftaccounts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="086ac-119">Accounts_EnableAdministratorAccountStatus</span><span class="sxs-lookup"><span data-stu-id="086ac-119">Accounts_EnableAdministratorAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="086ac-122">Accounts_EnableGuestAccountStatus</span><span class="sxs-lookup"><span data-stu-id="086ac-122">Accounts_EnableGuestAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-125">LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly de contas \_</span><span class="sxs-lookup"><span data-stu-id="086ac-125">Accounts\_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-limitlocalaccountuseofblankpasswordstoconsolelogononly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-128">RenameAdministratorAccount de contas \_</span><span class="sxs-lookup"><span data-stu-id="086ac-128">Accounts\_RenameAdministratorAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameadministratoraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="086ac-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-131">RenameGuestAccount de contas \_</span><span class="sxs-lookup"><span data-stu-id="086ac-131">Accounts\_RenameGuestAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameguestaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="086ac-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-134">Dispositivos \_ AllowedToFormatAndEjectRemovableMedia</span><span class="sxs-lookup"><span data-stu-id="086ac-134">Devices\_AllowedToFormatAndEjectRemovableMedia</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowedtoformatandejectremovablemedia)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="086ac-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-137">Dispositivos \_ AllowUndockWithoutHavingToLogon</span><span class="sxs-lookup"><span data-stu-id="086ac-137">Devices\_AllowUndockWithoutHavingToLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowundockwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-140">Dispositivos \_ PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span><span class="sxs-lookup"><span data-stu-id="086ac-140">Devices\_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-preventusersfrominstallingprinterdriverswhenconnectingtosharedprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-143">Dispositivos \_ RestrictCDROMAccessToLocallyLoggedOnUserOnly</span><span class="sxs-lookup"><span data-stu-id="086ac-143">Devices\_RestrictCDROMAccessToLocallyLoggedOnUserOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-restrictcdromaccesstolocallyloggedonuseronly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="086ac-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="086ac-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="086ac-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="086ac-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="086ac-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="086ac-149">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="086ac-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-150">InteractiveLogon \_ DisplayUserInformationWhenTheSessionIsLocked</span><span class="sxs-lookup"><span data-stu-id="086ac-150">InteractiveLogon\_DisplayUserInformationWhenTheSessionIsLocked</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-displayuserinformationwhenthesessionislocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-151">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-153">Interactivelogon \_ DoNotDisplayLastSignedIn</span><span class="sxs-lookup"><span data-stu-id="086ac-153">Interactivelogon\_DoNotDisplayLastSignedIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplaylastsignedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-154">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-156">Interactivelogon \_ DoNotDisplayUsernameAtSignIn</span><span class="sxs-lookup"><span data-stu-id="086ac-156">Interactivelogon\_DoNotDisplayUsernameAtSignIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplayusernameatsignin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-157">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-159">Interactivelogon \_ DoNotRequireCTRLALTDEL</span><span class="sxs-lookup"><span data-stu-id="086ac-159">Interactivelogon\_DoNotRequireCTRLALTDEL</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotrequirectrlaltdel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-160">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-161">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-162">InteractiveLogon \_ MachineInactivityLimit</span><span class="sxs-lookup"><span data-stu-id="086ac-162">InteractiveLogon\_MachineInactivityLimit</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-machineinactivitylimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-163">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-164">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-165">InteractiveLogon \_ MessageTextForUsersAttemptingToLogOn</span><span class="sxs-lookup"><span data-stu-id="086ac-165">InteractiveLogon\_MessageTextForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetextforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="086ac-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-167">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-168">InteractiveLogon \_ MessageTitleForUsersAttemptingToLogOn</span><span class="sxs-lookup"><span data-stu-id="086ac-168">InteractiveLogon\_MessageTitleForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetitleforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="086ac-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-171">NetworkAccess \_ DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span><span class="sxs-lookup"><span data-stu-id="086ac-171">NetworkAccess\_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-donotallowanonymousenumerationofsamaccountsandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-172">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-174">NetworkAccess \_ RestrictAnonymousAccessToNamedPipesAndShares</span><span class="sxs-lookup"><span data-stu-id="086ac-174">NetworkAccess\_RestrictAnonymousAccessToNamedPipesAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictanonymousaccesstonamedpipesandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-175">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-176">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-177">NetworkAccess \_ RestrictClientsAllowedToMakeRemoteCallsToSAM</span><span class="sxs-lookup"><span data-stu-id="086ac-177">NetworkAccess\_RestrictClientsAllowedToMakeRemoteCallsToSAM</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictclientsallowedtomakeremotecallstosam)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="086ac-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-179">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-180">NetworkSecurity \_ AllowPKU2UAuthenticationRequests</span><span class="sxs-lookup"><span data-stu-id="086ac-180">NetworkSecurity\_AllowPKU2UAuthenticationRequests</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networksecurity-allowpku2uauthenticationrequests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-181">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-182">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="086ac-183">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="086ac-183">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="086ac-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="086ac-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="086ac-186">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="086ac-186">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-187">RecoveryConsole \_ AllowAutomaticAdministrativeLogon</span><span class="sxs-lookup"><span data-stu-id="086ac-187">RecoveryConsole\_AllowAutomaticAdministrativeLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-recoveryconsole-allowautomaticadministrativelogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-188">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-188">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-189">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-190">Desligar \_ AllowSystemToBeShutDownWithoutHavingToLogOn</span><span class="sxs-lookup"><span data-stu-id="086ac-190">Shutdown\_AllowSystemToBeShutDownWithoutHavingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-allowsystemtobeshutdownwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-191">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-191">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-192">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-193">Desligar \_ ClearVirtualMemoryPageFile</span><span class="sxs-lookup"><span data-stu-id="086ac-193">Shutdown\_ClearVirtualMemoryPageFile</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-clearvirtualmemorypagefile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-194">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-194">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-195">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-196">AllowUIAccessApplicationsToPromptForElevation de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="086ac-196">UserAccountControl\_AllowUIAccessApplicationsToPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-allowuiaccessapplicationstopromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-197">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-197">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-198">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-199">BehaviorOfTheElevationPromptForAdministrators de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="086ac-199">UserAccountControl\_BehaviorOfTheElevationPromptForAdministrators</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-200">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-201">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-202">BehaviorOfTheElevationPromptForStandardUsers de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="086ac-202">UserAccountControl\_BehaviorOfTheElevationPromptForStandardUsers</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforstandardusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-203">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-203">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-204">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-205">DetectApplicationInstallationsAndPromptForElevation de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="086ac-205">UserAccountControl\_DetectApplicationInstallationsAndPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-detectapplicationinstallationsandpromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-206">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-206">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-207">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-208">OnlyElevateExecutableFilesThatAreSignedAndValidated de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="086ac-208">UserAccountControl\_OnlyElevateExecutableFilesThatAreSignedAndValidated</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateexecutablefilesthataresignedandvalidated)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-209">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-210">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-210">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-211">OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="086ac-211">UserAccountControl\_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateuiaccessapplicationsthatareinstalledinsecurelocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-212">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-212">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-213">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-213">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-214">RunAllAdministratorsInAdminApprovalMode de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="086ac-214">UserAccountControl\_RunAllAdministratorsInAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-runalladministratorsinadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-215">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-216">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-216">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-217">SwitchToTheSecureDesktopWhenPromptingForElevation de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="086ac-217">UserAccountControl\_SwitchToTheSecureDesktopWhenPromptingForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-switchtothesecuredesktopwhenpromptingforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-218">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-218">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-219">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-219">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-220">UseAdminApprovalMode de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="086ac-220">UserAccountControl\_UseAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-useadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-221">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-221">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-222">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-222">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="086ac-223">VirtualizeFileAndRegistryWriteFailuresToPerUserLocations de UserAccountControl \_</span><span class="sxs-lookup"><span data-stu-id="086ac-223">UserAccountControl\_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-virtualizefileandregistrywritefailurestoperuserlocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="086ac-224">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="086ac-224">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="086ac-225">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="086ac-225">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="086ac-226">Requisitos</span><span class="sxs-lookup"><span data-stu-id="086ac-226">Requirements</span></span>



| <span data-ttu-id="086ac-227">Requisito</span><span class="sxs-lookup"><span data-stu-id="086ac-227">Requirement</span></span> | <span data-ttu-id="086ac-228">Valor</span><span class="sxs-lookup"><span data-stu-id="086ac-228">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="086ac-229">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="086ac-229">Minimum supported client</span></span><br/> | <span data-ttu-id="086ac-230">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="086ac-230">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="086ac-231">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="086ac-231">Minimum supported server</span></span><br/> | <span data-ttu-id="086ac-232">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="086ac-232">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="086ac-233">Namespace</span><span class="sxs-lookup"><span data-stu-id="086ac-233">Namespace</span></span><br/>                | <span data-ttu-id="086ac-234">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="086ac-234">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="086ac-235">MOF</span><span class="sxs-lookup"><span data-stu-id="086ac-235">MOF</span></span><br/>                      | <dl> <span data-ttu-id="086ac-236"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="086ac-236"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="086ac-237">DLL</span><span class="sxs-lookup"><span data-stu-id="086ac-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="086ac-238"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="086ac-238"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

