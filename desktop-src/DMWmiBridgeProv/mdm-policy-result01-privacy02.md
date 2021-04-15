---
title: Classe MDM_Policy_Result01_Privacy02
description: A \_ classe Result01 Privacy02 de política de MDM \_ \_ representa as políticas de pesquisa disponíveis.
ms.assetid: 40aa1b74-bdec-471d-a7d4-89e59bf8637c
keywords:
- Classe MDM_Policy_Result01_Privacy02
- Classe MDM_Policy_Result01_Privacy02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Privacy02
- MDM_Policy_Result01_Privacy02.InstanceID
- MDM_Policy_Result01_Privacy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bbe28d1c0bc1258ec3c9fb57fd592a97c96026
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454682"
---
# <a name="mdm_policy_result01_privacy02-class"></a><span data-ttu-id="9f8af-105">\_Classe MDM \_ Result01 \_ Privacy02</span><span class="sxs-lookup"><span data-stu-id="9f8af-105">MDM\_Policy\_Result01\_Privacy02 class</span></span>

<span data-ttu-id="9f8af-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="9f8af-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9f8af-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="9f8af-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9f8af-108">A **classe \_ \_ Result01 \_ Privacy02 de política de MDM** representa as políticas de pesquisa disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9f8af-108">The **MDM\_Policy\_Result01\_Privacy02** class represents the search policies available.</span></span>

<span data-ttu-id="9f8af-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9f8af-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f8af-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f8af-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Privacy02
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

## <a name="members"></a><span data-ttu-id="9f8af-111">Membros</span><span class="sxs-lookup"><span data-stu-id="9f8af-111">Members</span></span>

<span data-ttu-id="9f8af-112">A **classe \_ \_ Result01 \_ Privacy02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9f8af-112">The **MDM\_Policy\_Result01\_Privacy02** class has these types of members:</span></span>

-   [<span data-ttu-id="9f8af-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9f8af-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f8af-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9f8af-114">Properties</span></span>

<span data-ttu-id="9f8af-115">A **classe \_ \_ Result01 \_ Privacy02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9f8af-115">The **MDM\_Policy\_Result01\_Privacy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9f8af-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span><span class="sxs-lookup"><span data-stu-id="9f8af-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowautoacceptpairingandprivacyconsentprompts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-119">AllowInputPersonalization</span><span class="sxs-lookup"><span data-stu-id="9f8af-119">AllowInputPersonalization</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowinputpersonalization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-122">DisableAdvertisingId</span><span class="sxs-lookup"><span data-stu-id="9f8af-122">DisableAdvertisingId</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-disableadvertisingid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-125">EnableActivityFeed</span><span class="sxs-lookup"><span data-stu-id="9f8af-125">EnableActivityFeed</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-enableactivityfeed)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f8af-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9f8af-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f8af-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f8af-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f8af-132">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="9f8af-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="9f8af-133">Para essa classe, a cadeia de caracteres é "privacidade".</span><span class="sxs-lookup"><span data-stu-id="9f8af-133">For this class, the string is "Privacy".</span></span>

</dd> <dt>

[<span data-ttu-id="9f8af-134">LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="9f8af-134">LetAppsAccessAccountInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-137">LetAppsAccessAccountInfo \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-137">LetAppsAccessAccountInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-140">LetAppsAccessAccountInfo \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-140">LetAppsAccessAccountInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-143">LetAppsAccessAccountInfo \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-143">LetAppsAccessAccountInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-146">LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="9f8af-146">LetAppsAccessCalendar</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-149">LetAppsAccessCalendar \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-149">LetAppsAccessCalendar\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-152">LetAppsAccessCalendar \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-152">LetAppsAccessCalendar\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-155">LetAppsAccessCalendar \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-155">LetAppsAccessCalendar\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-158">LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="9f8af-158">LetAppsAccessCallHistory</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-159">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-161">LetAppsAccessCallHistory \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-161">LetAppsAccessCallHistory\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-164">LetAppsAccessCallHistory \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-164">LetAppsAccessCallHistory\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-167">LetAppsAccessCallHistory \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-167">LetAppsAccessCallHistory\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-170">LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="9f8af-170">LetAppsAccessCamera</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-171">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-173">LetAppsAccessCamera \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-173">LetAppsAccessCamera\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-176">LetAppsAccessCamera \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-176">LetAppsAccessCamera\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-179">LetAppsAccessCamera \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-179">LetAppsAccessCamera\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-182">LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="9f8af-182">LetAppsAccessContacts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-183">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-185">LetAppsAccessContacts \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-185">LetAppsAccessContacts\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-188">LetAppsAccessContacts \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-188">LetAppsAccessContacts\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-191">LetAppsAccessContacts \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-191">LetAppsAccessContacts\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-193">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-194">LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="9f8af-194">LetAppsAccessEmail</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-195">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-195">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-196">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-197">LetAppsAccessEmail \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-197">LetAppsAccessEmail\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-200">LetAppsAccessEmail \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-200">LetAppsAccessEmail\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-202">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-203">LetAppsAccessEmail \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-203">LetAppsAccessEmail\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-205">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-206">LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="9f8af-206">LetAppsAccessLocation</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-207">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-209">LetAppsAccessLocation \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-209">LetAppsAccessLocation\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-212">LetAppsAccessLocation \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-212">LetAppsAccessLocation\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-215">LetAppsAccessLocation \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-215">LetAppsAccessLocation\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-217">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-218">LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="9f8af-218">LetAppsAccessMessaging</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-219">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-221">LetAppsAccessMessaging \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-221">LetAppsAccessMessaging\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-224">LetAppsAccessMessaging \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-224">LetAppsAccessMessaging\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-227">LetAppsAccessMessaging \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-227">LetAppsAccessMessaging\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-228">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-229">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-230">LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="9f8af-230">LetAppsAccessMicrophone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-231">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-232">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-233">LetAppsAccessMicrophone \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-233">LetAppsAccessMicrophone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-235">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-236">LetAppsAccessMicrophone \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-236">LetAppsAccessMicrophone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-238">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-239">LetAppsAccessMicrophone \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-239">LetAppsAccessMicrophone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-241">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-242">LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="9f8af-242">LetAppsAccessMotion</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-243">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-244">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-245">LetAppsAccessMotion \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-245">LetAppsAccessMotion\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-246">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-247">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-248">LetAppsAccessMotion \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-248">LetAppsAccessMotion\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-250">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-251">LetAppsAccessMotion \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-251">LetAppsAccessMotion\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-253">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-254">LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="9f8af-254">LetAppsAccessNotifications</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-255">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-256">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-257">LetAppsAccessNotifications \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-257">LetAppsAccessNotifications\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-259">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-260">LetAppsAccessNotifications \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-260">LetAppsAccessNotifications\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-262">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-263">LetAppsAccessNotifications \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-263">LetAppsAccessNotifications\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-265">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-266">LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="9f8af-266">LetAppsAccessPhone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-267">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-267">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-268">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-269">LetAppsAccessPhone \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-269">LetAppsAccessPhone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-270">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-271">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-272">LetAppsAccessPhone \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-272">LetAppsAccessPhone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-274">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-275">LetAppsAccessPhone \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-275">LetAppsAccessPhone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-276">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-277">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-278">LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="9f8af-278">LetAppsAccessRadios</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-279">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-279">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-280">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-281">LetAppsAccessRadios \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-281">LetAppsAccessRadios\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-283">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-283">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-284">LetAppsAccessRadios \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-284">LetAppsAccessRadios\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-285">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-286">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-286">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-287">LetAppsAccessRadios \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-287">LetAppsAccessRadios\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-289">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-289">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-290">LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="9f8af-290">LetAppsAccessTasks</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-291">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-291">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-292">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-292">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-293">LetAppsAccessTasks \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-293">LetAppsAccessTasks\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-294">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-295">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-295">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-296">LetAppsAccessTasks \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-296">LetAppsAccessTasks\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-298">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-298">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-299">LetAppsAccessTasks \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-299">LetAppsAccessTasks\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-301">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-301">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-302">LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="9f8af-302">LetAppsAccessTrustedDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-303">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-303">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-304">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-304">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-305">LetAppsAccessTrustedDevices \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-305">LetAppsAccessTrustedDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-306">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-307">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-307">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-308">LetAppsAccessTrustedDevices \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-308">LetAppsAccessTrustedDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-310">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-310">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-311">LetAppsAccessTrustedDevices \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-311">LetAppsAccessTrustedDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-312">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-313">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-313">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-314">LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="9f8af-314">LetAppsGetDiagnosticInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-315">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-315">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-316">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-316">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-317">LetAppsGetDiagnosticInfo \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-317">LetAppsGetDiagnosticInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-318">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-319">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-319">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-320">LetAppsGetDiagnosticInfo \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-320">LetAppsGetDiagnosticInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-322">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-322">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-323">LetAppsGetDiagnosticInfo \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-323">LetAppsGetDiagnosticInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-325">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-325">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-326">LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="9f8af-326">LetAppsRunInBackground</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-327">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-327">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-328">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-328">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-329">LetAppsRunInBackground \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-329">LetAppsRunInBackground\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-330">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-331">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-331">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-332">LetAppsRunInBackground \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-332">LetAppsRunInBackground\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-334">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-334">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-335">LetAppsRunInBackground \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-335">LetAppsRunInBackground\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-337">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-337">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-338">LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="9f8af-338">LetAppsSyncWithDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-339">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-340">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-340">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-341">LetAppsSyncWithDevices \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-341">LetAppsSyncWithDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-343">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-343">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-344">LetAppsSyncWithDevices \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-344">LetAppsSyncWithDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-346">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-346">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f8af-347">LetAppsSyncWithDevices \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="9f8af-347">LetAppsSyncWithDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-348">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-349">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-349">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f8af-350">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9f8af-350">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-351">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f8af-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f8af-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-353">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f8af-353">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f8af-354">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="9f8af-354">Describes the full path to the parent node.</span></span> <span data-ttu-id="9f8af-355">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="9f8af-355">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="9f8af-356">PublishUserActivities</span><span class="sxs-lookup"><span data-stu-id="9f8af-356">PublishUserActivities</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-publishuseractivities)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f8af-357">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9f8af-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f8af-358">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9f8af-358">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f8af-359">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f8af-359">Requirements</span></span>



| <span data-ttu-id="9f8af-360">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f8af-360">Requirement</span></span> | <span data-ttu-id="9f8af-361">Valor</span><span class="sxs-lookup"><span data-stu-id="9f8af-361">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f8af-362">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f8af-362">Minimum supported client</span></span><br/> | <span data-ttu-id="9f8af-363">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9f8af-363">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f8af-364">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f8af-364">Minimum supported server</span></span><br/> | <span data-ttu-id="9f8af-365">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9f8af-365">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9f8af-366">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f8af-366">Namespace</span></span><br/>                | <span data-ttu-id="9f8af-367">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="9f8af-367">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9f8af-368">MOF</span><span class="sxs-lookup"><span data-stu-id="9f8af-368">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f8af-369"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f8af-369"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f8af-370">DLL</span><span class="sxs-lookup"><span data-stu-id="9f8af-370">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f8af-371"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f8af-371"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f8af-372">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f8af-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f8af-373">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="9f8af-373">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

