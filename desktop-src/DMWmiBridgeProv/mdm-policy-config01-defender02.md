---
title: Classe MDM_Policy_Config01_Defender02
description: A política de MDM \_ \_ Config01 \_ Defender02class representa políticas relacionadas ao Windows Defender.
ms.assetid: 6d9d4edd-fcb6-45ea-bc5d-1bffb9cf8740
keywords:
- Classe MDM_Policy_Config01_Defender02
- Classe MDM_Policy_Config01_Defender02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Defender02
- MDM_Policy_Config01_Defender02.InstanceID
- MDM_Policy_Config01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b184008fc0ce7fc44dcb7106ceec3abc0e91450d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454913"
---
# <a name="mdm_policy_config01_defender02-class"></a><span data-ttu-id="cd8b8-105">\_Classe MDM \_ Config01 \_ Defender02</span><span class="sxs-lookup"><span data-stu-id="cd8b8-105">MDM\_Policy\_Config01\_Defender02 class</span></span>

<span data-ttu-id="cd8b8-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="cd8b8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cd8b8-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="cd8b8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cd8b8-108">A **classe \_ \_ Config01 \_ Defender02 de política de MDM** representa políticas relacionadas ao Windows Defender</span><span class="sxs-lookup"><span data-stu-id="cd8b8-108">The **MDM\_Policy\_Config01\_Defender02** class represents policies related to Windows Defender</span></span>

<span data-ttu-id="cd8b8-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cd8b8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd8b8-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd8b8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Defender02
{
  string InstanceID;
  string ParentID;
  sint32 AllowArchiveScanning;
  sint32 AllowBehaviorMonitoring;
  sint32 AllowCloudProtection;
  sint32 AllowEmailScanning;
  sint32 AllowFullScanOnMappedNetworkDrives;
  sint32 AllowFullScanRemovableDriveScanning;
  sint32 AllowIntrusionPreventionSystem;
  sint32 AllowIOAVProtection;
  sint32 AllowOnAccessProtection;
  sint32 AllowRealtimeMonitoring;
  sint32 AllowScanningNetworkFiles;
  sint32 AllowScriptScanning;
  sint32 AllowUserUIAccess;
  string AttackSurfaceReductionRules;
  string AttackSurfaceReductionOnlyExclusions;
  sint32 AVGCPULoadFactor;
  sint32 CloudExtendedTimeout;
  string ControlledFolderAccessProtectedFolders;
  string ControlledFolderAccessAllowedApplications;
  sint32 CloudBlockLevel;
  sint32 DaysToRetainCleanedMalware;
  sint32 EnableControlledFolderAccess;
  sint32 EnableNetworkProtection;
  sint32 PUAProtection;
  string ExcludedProcesses;
  string ExcludedPaths;
  string ExcludedExtensions;
  sint32 RealTimeScanDirection;
  sint32 ScanParameter;
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
};
```

## <a name="members"></a><span data-ttu-id="cd8b8-111">Membros</span><span class="sxs-lookup"><span data-stu-id="cd8b8-111">Members</span></span>

<span data-ttu-id="cd8b8-112">A **classe \_ \_ Config01 \_ Defender02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cd8b8-112">The **MDM\_Policy\_Config01\_Defender02** class has these types of members:</span></span>

-   [<span data-ttu-id="cd8b8-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd8b8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd8b8-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd8b8-114">Properties</span></span>

<span data-ttu-id="cd8b8-115">A **classe \_ \_ Config01 \_ Defender02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cd8b8-115">The **MDM\_Policy\_Config01\_Defender02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="cd8b8-116">AllowArchiveScanning</span><span class="sxs-lookup"><span data-stu-id="cd8b8-116">AllowArchiveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-119">AllowBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="cd8b8-119">AllowBehaviorMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-122">AllowCloudProtection</span><span class="sxs-lookup"><span data-stu-id="cd8b8-122">AllowCloudProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-125">AllowEmailScanning</span><span class="sxs-lookup"><span data-stu-id="cd8b8-125">AllowEmailScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-128">AllowFullScanOnMappedNetworkDrives</span><span class="sxs-lookup"><span data-stu-id="cd8b8-128">AllowFullScanOnMappedNetworkDrives</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-131">AllowFullScanRemovableDriveScanning</span><span class="sxs-lookup"><span data-stu-id="cd8b8-131">AllowFullScanRemovableDriveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-134">AllowIntrusionPreventionSystem</span><span class="sxs-lookup"><span data-stu-id="cd8b8-134">AllowIntrusionPreventionSystem</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-137">AllowIOAVProtection</span><span class="sxs-lookup"><span data-stu-id="cd8b8-137">AllowIOAVProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-140">AllowOnAccessProtection</span><span class="sxs-lookup"><span data-stu-id="cd8b8-140">AllowOnAccessProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-143">AllowRealtimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="cd8b8-143">AllowRealtimeMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-146">AllowScanningNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="cd8b8-146">AllowScanningNetworkFiles</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-149">AllowScriptScanning</span><span class="sxs-lookup"><span data-stu-id="cd8b8-149">AllowScriptScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-152">AllowUserUIAccess</span><span class="sxs-lookup"><span data-stu-id="cd8b8-152">AllowUserUIAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-153">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-155">AttackSurfaceReductionOnlyExclusions</span><span class="sxs-lookup"><span data-stu-id="cd8b8-155">AttackSurfaceReductionOnlyExclusions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-158">AttackSurfaceReductionRules</span><span class="sxs-lookup"><span data-stu-id="cd8b8-158">AttackSurfaceReductionRules</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-161">AVGCPULoadFactor</span><span class="sxs-lookup"><span data-stu-id="cd8b8-161">AVGCPULoadFactor</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-162">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-164">CloudBlockLevel</span><span class="sxs-lookup"><span data-stu-id="cd8b8-164">CloudBlockLevel</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-165">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-167">CloudExtendedTimeout</span><span class="sxs-lookup"><span data-stu-id="cd8b8-167">CloudExtendedTimeout</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-168">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-170">ControlledFolderAccessAllowedApplications</span><span class="sxs-lookup"><span data-stu-id="cd8b8-170">ControlledFolderAccessAllowedApplications</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-173">ControlledFolderAccessProtectedFolders</span><span class="sxs-lookup"><span data-stu-id="cd8b8-173">ControlledFolderAccessProtectedFolders</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-175">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-176">DaysToRetainCleanedMalware</span><span class="sxs-lookup"><span data-stu-id="cd8b8-176">DaysToRetainCleanedMalware</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-177">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-179">EnableControlledFolderAccess</span><span class="sxs-lookup"><span data-stu-id="cd8b8-179">EnableControlledFolderAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-180">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-182">EnableNetworkProtection</span><span class="sxs-lookup"><span data-stu-id="cd8b8-182">EnableNetworkProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-183">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-185">ExcludedExtensions</span><span class="sxs-lookup"><span data-stu-id="cd8b8-185">ExcludedExtensions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-187">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-188">ExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="cd8b8-188">ExcludedPaths</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-191">ExcludedProcesses</span><span class="sxs-lookup"><span data-stu-id="cd8b8-191">ExcludedProcesses</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-193">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cd8b8-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd8b8-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-197">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cd8b8-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cd8b8-198">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="cd8b8-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="cd8b8-199">Para essa classe, a cadeia de caracteres é "defender".</span><span class="sxs-lookup"><span data-stu-id="cd8b8-199">For this class, the string is "Defender".</span></span>

</dd> <dt>

<span data-ttu-id="cd8b8-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd8b8-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-203">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cd8b8-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cd8b8-204">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="cd8b8-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="cd8b8-205">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="cd8b8-205">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="cd8b8-206">PUAProtection</span><span class="sxs-lookup"><span data-stu-id="cd8b8-206">PUAProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-207">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-209">RealTimeScanDirection</span><span class="sxs-lookup"><span data-stu-id="cd8b8-209">RealTimeScanDirection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-210">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-211">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-212">ScanParameter</span><span class="sxs-lookup"><span data-stu-id="cd8b8-212">ScanParameter</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-213">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-214">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-215">ScheduleQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="cd8b8-215">ScheduleQuickScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-216">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-217">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-218">ScheduleScanDay</span><span class="sxs-lookup"><span data-stu-id="cd8b8-218">ScheduleScanDay</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-219">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-220">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-221">ScheduleScanTime</span><span class="sxs-lookup"><span data-stu-id="cd8b8-221">ScheduleScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-222">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-223">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-224">SignatureUpdateInterval</span><span class="sxs-lookup"><span data-stu-id="cd8b8-224">SignatureUpdateInterval</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-225">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-227">SubmitSamplesConsent</span><span class="sxs-lookup"><span data-stu-id="cd8b8-227">SubmitSamplesConsent</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-228">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-229">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cd8b8-230">ThreatSeverityDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd8b8-230">ThreatSeverityDefaultAction</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd8b8-231">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd8b8-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd8b8-232">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cd8b8-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd8b8-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd8b8-233">Requirements</span></span>



| <span data-ttu-id="cd8b8-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd8b8-234">Requirement</span></span> | <span data-ttu-id="cd8b8-235">Valor</span><span class="sxs-lookup"><span data-stu-id="cd8b8-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd8b8-236">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd8b8-236">Minimum supported client</span></span><br/> | <span data-ttu-id="cd8b8-237">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cd8b8-237">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd8b8-238">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd8b8-238">Minimum supported server</span></span><br/> | <span data-ttu-id="cd8b8-239">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cd8b8-239">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cd8b8-240">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd8b8-240">Namespace</span></span><br/>                | <span data-ttu-id="cd8b8-241">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="cd8b8-241">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="cd8b8-242">MOF</span><span class="sxs-lookup"><span data-stu-id="cd8b8-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd8b8-243"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd8b8-243"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd8b8-244">DLL</span><span class="sxs-lookup"><span data-stu-id="cd8b8-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd8b8-245"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd8b8-245"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd8b8-246">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd8b8-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd8b8-247">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="cd8b8-247">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

