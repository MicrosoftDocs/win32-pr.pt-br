---
title: Classe MDM_Policy_Config01_Privacy02
description: A \_ classe Config01 Privacy02 de política de MDM \_ \_ representa as políticas de pesquisa disponíveis.
ms.assetid: 202213b9-5301-4c55-bbc6-6ce3daf705ad
keywords:
- Classe MDM_Policy_Config01_Privacy02
- Classe MDM_Policy_Config01_Privacy02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Privacy02
- MDM_Policy_Config01_Privacy02.InstanceID
- MDM_Policy_Config01_Privacy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca714dc17db60982e5ba047690886bc88aa79853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918428"
---
# <a name="mdm_policy_config01_privacy02-class"></a><span data-ttu-id="2e399-105">\_Classe MDM \_ Config01 \_ Privacy02</span><span class="sxs-lookup"><span data-stu-id="2e399-105">MDM\_Policy\_Config01\_Privacy02 class</span></span>

<span data-ttu-id="2e399-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2e399-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2e399-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="2e399-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2e399-108">A **classe \_ \_ Config01 \_ Privacy02 de política de MDM** representa as políticas de pesquisa disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2e399-108">The **MDM\_Policy\_Config01\_Privacy02** class represents the search policies available.</span></span>

<span data-ttu-id="2e399-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2e399-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e399-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e399-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Privacy02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAutoAcceptPairingAndPrivacyConsentPrompts;
  sint32 AllowInputPersonalization;
  string LetAppsSyncWithDevices_UserInControlOfTheseApps;
  sint32 PublishUserActivities;
  string LetAppsSyncWithDevices_ForceDenyTheseApps;
  string LetAppsSyncWithDevices_ForceAllowTheseApps;
  sint32 LetAppsSyncWithDevices;
  string LetAppsAccessTrustedDevices_UserInControlOfTheseApps;
  string LetAppsRunInBackground_UserInControlOfTheseApps;
  string LetAppsRunInBackground_ForceDenyTheseApps;
  string LetAppsRunInBackground_ForceAllowTheseApps;
  sint32 LetAppsRunInBackground;
  string LetAppsGetDiagnosticInfo_UserInControlOfTheseApps;
  string LetAppsGetDiagnosticInfo_ForceDenyTheseApps;
  string LetAppsGetDiagnosticInfo_ForceAllowTheseApps;
  sint32 LetAppsGetDiagnosticInfo;
  string LetAppsAccessTrustedDevices_ForceDenyTheseApps;
  string LetAppsAccessTrustedDevices_ForceAllowTheseApps;
  sint32 LetAppsAccessTrustedDevices;
  string LetAppsAccessRadios_UserInControlOfTheseApps;
  string LetAppsAccessTasks_UserInControlOfTheseApps;
  string LetAppsAccessTasks_ForceDenyTheseApps;
  string LetAppsAccessTasks_ForceAllowTheseApps;
  sint32 LetAppsAccessTasks;
  string LetAppsAccessRadios_ForceDenyTheseApps;
  string LetAppsAccessRadios_ForceAllowTheseApps;
  sint32 LetAppsAccessRadios;
  string LetAppsAccessPhone_UserInControlOfTheseApps;
  string LetAppsAccessPhone_ForceDenyTheseApps;
  string LetAppsAccessPhone_ForceAllowTheseApps;
  sint32 LetAppsAccessPhone;
  string LetAppsAccessMotion_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_ForceDenyTheseApps;
  string LetAppsAccessNotifications_ForceAllowTheseApps;
  sint32 LetAppsAccessNotifications;
  string LetAppsAccessMotion_ForceDenyTheseApps;
  string LetAppsAccessMotion_ForceAllowTheseApps;
  sint32 LetAppsAccessMotion;
  string LetAppsAccessMicrophone_UserInControlOfTheseApps;
  string LetAppsAccessMicrophone_ForceDenyTheseApps;
  string LetAppsAccessMicrophone_ForceAllowTheseApps;
  sint32 LetAppsAccessMicrophone;
  string LetAppsAccessMessaging_UserInControlOfTheseApps;
  string LetAppsAccessMessaging_ForceDenyTheseApps;
  string LetAppsAccessMessaging_ForceAllowTheseApps;
  sint32 LetAppsAccessMessaging;
  string LetAppsAccessLocation_UserInControlOfTheseApps;
  string LetAppsAccessLocation_ForceDenyTheseApps;
  string LetAppsAccessLocation_ForceAllowTheseApps;
  sint32 LetAppsAccessLocation;
  string LetAppsAccessEmail_UserInControlOfTheseApps;
  string LetAppsAccessEmail_ForceDenyTheseApps;
  string LetAppsAccessEmail_ForceAllowTheseApps;
  sint32 LetAppsAccessEmail;
  string LetAppsAccessContacts_UserInControlOfTheseApps;
  string LetAppsAccessContacts_ForceDenyTheseApps;
  string LetAppsAccessContacts_ForceAllowTheseApps;
  sint32 LetAppsAccessContacts;
  string LetAppsAccessCamera_UserInControlOfTheseApps;
  string LetAppsAccessCamera_ForceDenyTheseApps;
  string LetAppsAccessCamera_ForceAllowTheseApps;
  sint32 LetAppsAccessCamera;
  string LetAppsAccessCallHistory_UserInControlOfTheseApps;
  string LetAppsAccessCallHistory_ForceDenyTheseApps;
  string LetAppsAccessCallHistory_ForceAllowTheseApps;
  sint32 LetAppsAccessCallHistory;
  string LetAppsAccessCalendar_UserInControlOfTheseApps;
  string LetAppsAccessCalendar_ForceDenyTheseApps;
  string LetAppsAccessCalendar_ForceAllowTheseApps;
  sint32 LetAppsAccessCalendar;
  string LetAppsAccessAccountInfo_UserInControlOfTheseApps;
  string LetAppsAccessAccountInfo_ForceDenyTheseApps;
  string LetAppsAccessAccountInfo_ForceAllowTheseApps;
  sint32 LetAppsAccessAccountInfo;
  sint32 DisableAdvertisingId;
  sint32 EnableActivityFeed;
};
```

## <a name="members"></a><span data-ttu-id="2e399-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2e399-111">Members</span></span>

<span data-ttu-id="2e399-112">A **classe \_ \_ Config01 \_ Privacy02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2e399-112">The **MDM\_Policy\_Config01\_Privacy02** class has these types of members:</span></span>

-   [<span data-ttu-id="2e399-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2e399-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e399-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2e399-114">Properties</span></span>

<span data-ttu-id="2e399-115">A **classe \_ \_ Config01 \_ Privacy02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2e399-115">The **MDM\_Policy\_Config01\_Privacy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2e399-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span><span class="sxs-lookup"><span data-stu-id="2e399-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowautoacceptpairingandprivacyconsentprompts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-119">AllowInputPersonalization</span><span class="sxs-lookup"><span data-stu-id="2e399-119">AllowInputPersonalization</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowinputpersonalization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-122">DisableAdvertisingId</span><span class="sxs-lookup"><span data-stu-id="2e399-122">DisableAdvertisingId</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-disableadvertisingid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-125">EnableActivityFeed</span><span class="sxs-lookup"><span data-stu-id="2e399-125">EnableActivityFeed</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-enableactivityfeed)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2e399-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2e399-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e399-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e399-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2e399-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2e399-132">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="2e399-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="2e399-133">Para essa classe, a cadeia de caracteres é "privacidade".</span><span class="sxs-lookup"><span data-stu-id="2e399-133">For this class, the string is "Privacy".</span></span>

</dd> <dt>

[<span data-ttu-id="2e399-134">LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="2e399-134">LetAppsAccessAccountInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-137">LetAppsAccessAccountInfo \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-137">LetAppsAccessAccountInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-140">LetAppsAccessAccountInfo \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-140">LetAppsAccessAccountInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-143">LetAppsAccessAccountInfo \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-143">LetAppsAccessAccountInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-146">LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="2e399-146">LetAppsAccessCalendar</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-149">LetAppsAccessCalendar \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-149">LetAppsAccessCalendar\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-152">LetAppsAccessCalendar \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-152">LetAppsAccessCalendar\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-155">LetAppsAccessCalendar \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-155">LetAppsAccessCalendar\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-158">LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="2e399-158">LetAppsAccessCallHistory</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-159">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-161">LetAppsAccessCallHistory \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-161">LetAppsAccessCallHistory\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-164">LetAppsAccessCallHistory \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-164">LetAppsAccessCallHistory\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-167">LetAppsAccessCallHistory \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-167">LetAppsAccessCallHistory\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-170">LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="2e399-170">LetAppsAccessCamera</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-171">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-173">LetAppsAccessCamera \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-173">LetAppsAccessCamera\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-176">LetAppsAccessCamera \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-176">LetAppsAccessCamera\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-179">LetAppsAccessCamera \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-179">LetAppsAccessCamera\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-182">LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="2e399-182">LetAppsAccessContacts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-183">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-185">LetAppsAccessContacts \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-185">LetAppsAccessContacts\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-188">LetAppsAccessContacts \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-188">LetAppsAccessContacts\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-191">LetAppsAccessContacts \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-191">LetAppsAccessContacts\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-193">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-194">LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="2e399-194">LetAppsAccessEmail</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-195">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-195">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-196">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-197">LetAppsAccessEmail \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-197">LetAppsAccessEmail\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-200">LetAppsAccessEmail \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-200">LetAppsAccessEmail\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-203">LetAppsAccessEmail \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-203">LetAppsAccessEmail\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-205">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-206">LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="2e399-206">LetAppsAccessLocation</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-207">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-209">LetAppsAccessLocation \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-209">LetAppsAccessLocation\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-212">LetAppsAccessLocation \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-212">LetAppsAccessLocation\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-215">LetAppsAccessLocation \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-215">LetAppsAccessLocation\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-217">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-218">LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="2e399-218">LetAppsAccessMessaging</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-219">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-221">LetAppsAccessMessaging \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-221">LetAppsAccessMessaging\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-224">LetAppsAccessMessaging \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-224">LetAppsAccessMessaging\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-227">LetAppsAccessMessaging \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-227">LetAppsAccessMessaging\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-229">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-230">LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="2e399-230">LetAppsAccessMicrophone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-231">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-232">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-233">LetAppsAccessMicrophone \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-233">LetAppsAccessMicrophone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-235">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-236">LetAppsAccessMicrophone \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-236">LetAppsAccessMicrophone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-238">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-239">LetAppsAccessMicrophone \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-239">LetAppsAccessMicrophone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-241">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-242">LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="2e399-242">LetAppsAccessMotion</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-243">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-244">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-245">LetAppsAccessMotion \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-245">LetAppsAccessMotion\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-247">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-248">LetAppsAccessMotion \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-248">LetAppsAccessMotion\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-250">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-251">LetAppsAccessMotion \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-251">LetAppsAccessMotion\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-253">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-254">LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="2e399-254">LetAppsAccessNotifications</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-255">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-256">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-257">LetAppsAccessNotifications \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-257">LetAppsAccessNotifications\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-259">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-260">LetAppsAccessNotifications \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-260">LetAppsAccessNotifications\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-262">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-263">LetAppsAccessNotifications \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-263">LetAppsAccessNotifications\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-265">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-266">LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="2e399-266">LetAppsAccessPhone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-267">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-267">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-268">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-269">LetAppsAccessPhone \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-269">LetAppsAccessPhone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-270">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-271">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-272">LetAppsAccessPhone \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-272">LetAppsAccessPhone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-274">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-275">LetAppsAccessPhone \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-275">LetAppsAccessPhone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-276">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-277">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-278">LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="2e399-278">LetAppsAccessRadios</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-279">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-279">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-280">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-281">LetAppsAccessRadios \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-281">LetAppsAccessRadios\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-283">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-283">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-284">LetAppsAccessRadios \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-284">LetAppsAccessRadios\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-285">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-286">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-286">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-287">LetAppsAccessRadios \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-287">LetAppsAccessRadios\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-289">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-289">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-290">LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="2e399-290">LetAppsAccessTasks</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-291">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-291">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-292">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-292">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-293">LetAppsAccessTasks \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-293">LetAppsAccessTasks\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-294">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-295">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-295">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-296">LetAppsAccessTasks \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-296">LetAppsAccessTasks\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-298">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-298">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-299">LetAppsAccessTasks \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-299">LetAppsAccessTasks\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-301">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-301">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-302">LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="2e399-302">LetAppsAccessTrustedDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-303">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-303">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-304">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-304">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-305">LetAppsAccessTrustedDevices \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-305">LetAppsAccessTrustedDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-306">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-307">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-307">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-308">LetAppsAccessTrustedDevices \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-308">LetAppsAccessTrustedDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-310">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-310">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-311">LetAppsAccessTrustedDevices \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-311">LetAppsAccessTrustedDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-312">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-313">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-313">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-314">LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="2e399-314">LetAppsGetDiagnosticInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-315">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-315">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-316">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-316">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-317">LetAppsGetDiagnosticInfo \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-317">LetAppsGetDiagnosticInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-318">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-319">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-319">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-320">LetAppsGetDiagnosticInfo \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-320">LetAppsGetDiagnosticInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-322">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-322">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-323">LetAppsGetDiagnosticInfo \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-323">LetAppsGetDiagnosticInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-325">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-325">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-326">LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="2e399-326">LetAppsRunInBackground</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-327">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-327">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-328">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-328">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-329">LetAppsRunInBackground \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-329">LetAppsRunInBackground\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-330">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-331">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-331">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-332">LetAppsRunInBackground \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-332">LetAppsRunInBackground\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-334">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-334">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-335">LetAppsRunInBackground \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-335">LetAppsRunInBackground\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-337">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-337">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-338">LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="2e399-338">LetAppsSyncWithDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-339">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-340">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-340">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-341">LetAppsSyncWithDevices \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-341">LetAppsSyncWithDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-343">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-343">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-344">LetAppsSyncWithDevices \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-344">LetAppsSyncWithDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-346">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-346">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2e399-347">LetAppsSyncWithDevices \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="2e399-347">LetAppsSyncWithDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-348">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-349">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-349">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2e399-350">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2e399-350">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-351">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e399-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e399-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e399-353">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2e399-353">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2e399-354">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="2e399-354">Describes the full path to the parent node.</span></span> <span data-ttu-id="2e399-355">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="2e399-355">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="2e399-356">PublishUserActivities</span><span class="sxs-lookup"><span data-stu-id="2e399-356">PublishUserActivities</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-publishuseractivities)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e399-357">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2e399-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e399-358">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2e399-358">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e399-359">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e399-359">Requirements</span></span>



| <span data-ttu-id="2e399-360">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e399-360">Requirement</span></span> | <span data-ttu-id="2e399-361">Valor</span><span class="sxs-lookup"><span data-stu-id="2e399-361">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e399-362">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e399-362">Minimum supported client</span></span><br/> | <span data-ttu-id="2e399-363">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2e399-363">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e399-364">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e399-364">Minimum supported server</span></span><br/> | <span data-ttu-id="2e399-365">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2e399-365">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2e399-366">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e399-366">Namespace</span></span><br/>                | <span data-ttu-id="2e399-367">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="2e399-367">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2e399-368">MOF</span><span class="sxs-lookup"><span data-stu-id="2e399-368">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e399-369"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e399-369"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e399-370">DLL</span><span class="sxs-lookup"><span data-stu-id="2e399-370">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e399-371"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e399-371"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e399-372">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e399-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e399-373">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="2e399-373">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

