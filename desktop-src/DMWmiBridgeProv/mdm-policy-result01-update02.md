---
title: Classe MDM_Policy_Result01_Update02
description: A \_ classe MDM Policy \_ Result01 \_ Update02 representa as políticas de atualização disponíveis.
ms.assetid: 06604da6-5298-4273-a030-529491c2823c
keywords:
- Classe MDM_Policy_Result01_Update02
- Classe MDM_Policy_Result01_Update02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Update02
- MDM_Policy_Result01_Update02.InstanceID
- MDM_Policy_Result01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0be844bb4ef8fc20e7ab5bbc8b7709cdfde4034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918025"
---
# <a name="mdm_policy_result01_update02-class"></a><span data-ttu-id="1fa51-105">\_Classe MDM \_ Result01 \_ Update02</span><span class="sxs-lookup"><span data-stu-id="1fa51-105">MDM\_Policy\_Result01\_Update02 class</span></span>

<span data-ttu-id="1fa51-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="1fa51-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1fa51-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="1fa51-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1fa51-108">A classe **MDM \_ Policy \_ Result01 \_ Update02** representa as políticas de atualização disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1fa51-108">The **MDM\_Policy\_Result01\_Update02** class represents the update policies available.</span></span>

<span data-ttu-id="1fa51-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1fa51-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa51-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fa51-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Update02
{
  string InstanceID;
  string ParentID;
  sint32 RequireUpdateApproval;
  sint32 AllowAutoUpdate;
  sint32 AllowAutoWindowsUpdateDownloadOverMeteredNetwork;
  sint32 AllowMUUpdateService;
  sint32 ScheduledInstallDay;
  sint32 ScheduledInstallThirdWeek;
  sint32 ScheduledInstallSecondWeek;
  sint32 ScheduledInstallFourthWeek;
  sint32 ScheduledInstallFirstWeek;
  sint32 ScheduledInstallEveryWeek;
  sint32 ScheduledInstallTime;
  sint32 AllowUpdateService;
  sint32 DeferQualityUpdatesPeriodInDays;
  sint32 DeferFeatureUpdatesPeriodInDays;
  sint32 BranchReadinessLevel;
  string UpdateServiceUrl;
  sint32 SetEDURestart;
  sint32 AutoRestartDeadlinePeriodInDays;
  string UpdateServiceUrlAlternate;
  sint32 FillEmptyContentUrls;
  sint32 AllowNonMicrosoftSignedUpdate;
  sint32 RequireDeferUpgrade;
  sint32 PauseDeferrals;
  sint32 PauseQualityUpdates;
  sint32 PhoneUpdateRestrictions;
  string PauseQualityUpdatesStartTime;
  sint32 PauseFeatureUpdates;
  string PauseFeatureUpdatesStartTime;
  sint32 DeferUpgradePeriod;
  sint32 ExcludeWUDriversInQualityUpdate;
  sint32 IgnoreMOUpdateDownloadLimit;
  sint32 ManagePreviewBuilds;
  sint32 IgnoreMOAppDownloadLimit;
  sint32 DeferUpdatePeriod;
  sint32 ActiveHoursEnd;
  sint32 ActiveHoursStart;
  sint32 DetectionFrequency;
  sint32 DisableDualScan;
  sint32 EngagedRestartDeadline;
  sint32 EngagedRestartSnoozeSchedule;
  sint32 EngagedRestartTransitionSchedule;
  sint32 ScheduleImminentRestartWarning;
  sint32 ScheduleRestartWarning;
  sint32 SetAutoRestartNotificationDisable;
  sint32 AutoRestartNotificationSchedule;
  sint32 AutoRestartRequiredNotificationDismissal;
  sint32 ActiveHoursMaxRange;
};
```

## <a name="members"></a><span data-ttu-id="1fa51-111">Membros</span><span class="sxs-lookup"><span data-stu-id="1fa51-111">Members</span></span>

<span data-ttu-id="1fa51-112">A **classe \_ \_ Result01 \_ Update02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1fa51-112">The **MDM\_Policy\_Result01\_Update02** class has these types of members:</span></span>

-   [<span data-ttu-id="1fa51-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1fa51-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1fa51-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1fa51-114">Properties</span></span>

<span data-ttu-id="1fa51-115">A **classe \_ \_ Result01 \_ Update02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1fa51-115">The **MDM\_Policy\_Result01\_Update02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1fa51-116">ActiveHoursEnd</span><span class="sxs-lookup"><span data-stu-id="1fa51-116">ActiveHoursEnd</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-119">ActiveHoursMaxRange</span><span class="sxs-lookup"><span data-stu-id="1fa51-119">ActiveHoursMaxRange</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-122">ActiveHoursStart</span><span class="sxs-lookup"><span data-stu-id="1fa51-122">ActiveHoursStart</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-125">AllowAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="1fa51-125">AllowAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span><span class="sxs-lookup"><span data-stu-id="1fa51-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-131">AllowMUUpdateService</span><span class="sxs-lookup"><span data-stu-id="1fa51-131">AllowMUUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-134">AllowNonMicrosoftSignedUpdate</span><span class="sxs-lookup"><span data-stu-id="1fa51-134">AllowNonMicrosoftSignedUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-137">AllowUpdateService</span><span class="sxs-lookup"><span data-stu-id="1fa51-137">AllowUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-140">AutoRestartDeadlinePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1fa51-140">AutoRestartDeadlinePeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-143">AutoRestartNotificationSchedule</span><span class="sxs-lookup"><span data-stu-id="1fa51-143">AutoRestartNotificationSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-146">AutoRestartRequiredNotificationDismissal</span><span class="sxs-lookup"><span data-stu-id="1fa51-146">AutoRestartRequiredNotificationDismissal</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-149">BranchReadinessLevel</span><span class="sxs-lookup"><span data-stu-id="1fa51-149">BranchReadinessLevel</span></span>](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-152">DeferFeatureUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1fa51-152">DeferFeatureUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-153">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-155">DeferQualityUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1fa51-155">DeferQualityUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-156">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-158">DeferUpdatePeriod</span><span class="sxs-lookup"><span data-stu-id="1fa51-158">DeferUpdatePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-159">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-161">DeferUpgradePeriod</span><span class="sxs-lookup"><span data-stu-id="1fa51-161">DeferUpgradePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-162">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-164">DetectionFrequency</span><span class="sxs-lookup"><span data-stu-id="1fa51-164">DetectionFrequency</span></span>](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-165">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-167">DisableDualScan</span><span class="sxs-lookup"><span data-stu-id="1fa51-167">DisableDualScan</span></span>](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-168">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-170">EngagedRestartDeadline</span><span class="sxs-lookup"><span data-stu-id="1fa51-170">EngagedRestartDeadline</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-171">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-173">EngagedRestartSnoozeSchedule</span><span class="sxs-lookup"><span data-stu-id="1fa51-173">EngagedRestartSnoozeSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-174">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-176">EngagedRestartTransitionSchedule</span><span class="sxs-lookup"><span data-stu-id="1fa51-176">EngagedRestartTransitionSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-177">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-179">ExcludeWUDriversInQualityUpdate</span><span class="sxs-lookup"><span data-stu-id="1fa51-179">ExcludeWUDriversInQualityUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-180">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-182">FillEmptyContentUrls</span><span class="sxs-lookup"><span data-stu-id="1fa51-182">FillEmptyContentUrls</span></span>](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-183">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-185">IgnoreMOAppDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="1fa51-185">IgnoreMOAppDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-186">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-188">IgnoreMOUpdateDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="1fa51-188">IgnoreMOUpdateDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-189">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1fa51-191">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1fa51-191">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1fa51-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1fa51-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-194">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1fa51-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1fa51-195">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="1fa51-195">Identifies the name of the parent node.</span></span> <span data-ttu-id="1fa51-196">Para essa classe, a cadeia de caracteres é "Update"</span><span class="sxs-lookup"><span data-stu-id="1fa51-196">For this class, the string is "Update"</span></span>

</dd> <dt>

[<span data-ttu-id="1fa51-197">ManagePreviewBuilds</span><span class="sxs-lookup"><span data-stu-id="1fa51-197">ManagePreviewBuilds</span></span>](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-198">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1fa51-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1fa51-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1fa51-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1fa51-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-203">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1fa51-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1fa51-204">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="1fa51-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="1fa51-205">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="1fa51-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="1fa51-206">PauseDeferrals</span><span class="sxs-lookup"><span data-stu-id="1fa51-206">PauseDeferrals</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-207">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-209">PauseFeatureUpdates</span><span class="sxs-lookup"><span data-stu-id="1fa51-209">PauseFeatureUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-210">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-212">PauseFeatureUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="1fa51-212">PauseFeatureUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1fa51-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-215">PauseQualityUpdates</span><span class="sxs-lookup"><span data-stu-id="1fa51-215">PauseQualityUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-216">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-217">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-218">PauseQualityUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="1fa51-218">PauseQualityUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1fa51-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-221">PhoneUpdateRestrictions</span><span class="sxs-lookup"><span data-stu-id="1fa51-221">PhoneUpdateRestrictions</span></span>](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-222">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-224">RequireDeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="1fa51-224">RequireDeferUpgrade</span></span>](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-225">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-227">RequireUpdateApproval</span><span class="sxs-lookup"><span data-stu-id="1fa51-227">RequireUpdateApproval</span></span>](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-228">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-229">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-230">ScheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="1fa51-230">ScheduledInstallDay</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-231">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-232">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-233">ScheduledInstallEveryWeek</span><span class="sxs-lookup"><span data-stu-id="1fa51-233">ScheduledInstallEveryWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-234">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-234">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-235">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-236">ScheduledInstallFirstWeek</span><span class="sxs-lookup"><span data-stu-id="1fa51-236">ScheduledInstallFirstWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-237">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-237">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-238">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-239">ScheduledInstallFourthWeek</span><span class="sxs-lookup"><span data-stu-id="1fa51-239">ScheduledInstallFourthWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-240">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-240">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-241">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-242">ScheduledInstallSecondWeek</span><span class="sxs-lookup"><span data-stu-id="1fa51-242">ScheduledInstallSecondWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-243">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-244">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-245">ScheduledInstallThirdWeek</span><span class="sxs-lookup"><span data-stu-id="1fa51-245">ScheduledInstallThirdWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-246">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-246">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-247">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-248">ScheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="1fa51-248">ScheduledInstallTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-249">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-249">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-250">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-251">ScheduleImminentRestartWarning</span><span class="sxs-lookup"><span data-stu-id="1fa51-251">ScheduleImminentRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-252">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-252">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-253">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-254">ScheduleRestartWarning</span><span class="sxs-lookup"><span data-stu-id="1fa51-254">ScheduleRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-255">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-256">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-257">SetAutoRestartNotificationDisable</span><span class="sxs-lookup"><span data-stu-id="1fa51-257">SetAutoRestartNotificationDisable</span></span>](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-258">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-258">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-259">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-260">SetEDURestart</span><span class="sxs-lookup"><span data-stu-id="1fa51-260">SetEDURestart</span></span>](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-261">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fa51-261">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-262">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-263">UpdateServiceUrl</span><span class="sxs-lookup"><span data-stu-id="1fa51-263">UpdateServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1fa51-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-265">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fa51-266">UpdateServiceUrlAlternate</span><span class="sxs-lookup"><span data-stu-id="1fa51-266">UpdateServiceUrlAlternate</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa51-267">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1fa51-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa51-268">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1fa51-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fa51-269">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fa51-269">Requirements</span></span>



| <span data-ttu-id="1fa51-270">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fa51-270">Requirement</span></span> | <span data-ttu-id="1fa51-271">Valor</span><span class="sxs-lookup"><span data-stu-id="1fa51-271">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa51-272">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fa51-272">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa51-273">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1fa51-273">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1fa51-274">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fa51-274">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa51-275">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1fa51-275">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1fa51-276">Namespace</span><span class="sxs-lookup"><span data-stu-id="1fa51-276">Namespace</span></span><br/>                | <span data-ttu-id="1fa51-277">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="1fa51-277">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="1fa51-278">MOF</span><span class="sxs-lookup"><span data-stu-id="1fa51-278">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fa51-279"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fa51-279"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fa51-280">DLL</span><span class="sxs-lookup"><span data-stu-id="1fa51-280">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fa51-281"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fa51-281"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fa51-282">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fa51-282">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa51-283">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="1fa51-283">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

