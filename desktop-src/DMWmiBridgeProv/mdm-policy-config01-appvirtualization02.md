---
title: Classe MDM_Policy_Config01_AppVirtualization02
description: A \_ classe Config01 AppVirtualization02 de política de MDM \_ \_ configura as políticas de virtualização de aplicativo disponíveis.
ms.assetid: d270704c-8652-4f97-89f7-fcb6e68ee6fe
keywords:
- Classe MDM_Policy_Config01_AppVirtualization02
- Classe MDM_Policy_Config01_AppVirtualization02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_AppVirtualization02
- MDM_Policy_Config01_AppVirtualization02.InstanceID
- MDM_Policy_Config01_AppVirtualization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871d09b306cff2833601100d9a645cde5c59e33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085386"
---
# <a name="mdm_policy_config01_appvirtualization02-class"></a><span data-ttu-id="d1631-105">\_Classe MDM \_ Config01 \_ AppVirtualization02</span><span class="sxs-lookup"><span data-stu-id="d1631-105">MDM\_Policy\_Config01\_AppVirtualization02 class</span></span>

<span data-ttu-id="d1631-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="d1631-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d1631-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="d1631-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d1631-108">A \_ classe Config01 AppVirtualization02 de política de MDM \_ \_ configura as políticas de virtualização de aplicativo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d1631-108">The MDM\_Policy\_Config01\_AppVirtualization02 class configures the available app virtualization policies.</span></span>

<span data-ttu-id="d1631-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d1631-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1631-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1631-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_AppVirtualization02
{
  string InstanceID;
  string ParentID;
  string AllowAppVClient;
  string AllowDynamicVirtualization;
  string AllowPackageCleanup;
  string AllowPackageScripts;
  string AllowPublishingRefreshUX;
  string AllowReportingServer;
  string AllowRoamingFileExclusions;
  string AllowRoamingRegistryExclusions;
  string AllowStreamingAutoload;
  string ClientCoexistenceAllowMigrationmode;
  string IntegrationAllowRootGlobal;
  string IntegrationAllowRootUser;
  string PublishingAllowServer1;
  string PublishingAllowServer2;
  string PublishingAllowServer3;
  string PublishingAllowServer4;
  string PublishingAllowServer5;
  string StreamingAllowCertificateFilterForClient_SSL;
  string StreamingAllowHighCostLaunch;
  string StreamingAllowLocationProvider;
  string StreamingAllowPackageInstallationRoot;
  string StreamingAllowPackageSourceRoot;
  string StreamingAllowReestablishmentInterval;
  string StreamingAllowReestablishmentRetries;
  string StreamingSharedContentStoreMode;
  string StreamingSupportBranchCache;
  string StreamingVerifyCertificateRevocationList;
  string VirtualComponentsAllowList;
};
```

## <a name="members"></a><span data-ttu-id="d1631-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d1631-111">Members</span></span>

<span data-ttu-id="d1631-112">A **classe \_ \_ Config01 \_ AppVirtualization02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d1631-112">The **MDM\_Policy\_Config01\_AppVirtualization02** class has these types of members:</span></span>

-   [<span data-ttu-id="d1631-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1631-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1631-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1631-114">Properties</span></span>

<span data-ttu-id="d1631-115">A **classe \_ \_ Config01 \_ AppVirtualization02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1631-115">The **MDM\_Policy\_Config01\_AppVirtualization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d1631-116">AllowAppVClient</span><span class="sxs-lookup"><span data-stu-id="d1631-116">AllowAppVClient</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowappvclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-119">AllowDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="d1631-119">AllowDynamicVirtualization</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowdynamicvirtualization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-122">AllowPackageCleanup</span><span class="sxs-lookup"><span data-stu-id="d1631-122">AllowPackageCleanup</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagecleanup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-125">AllowPackageScripts</span><span class="sxs-lookup"><span data-stu-id="d1631-125">AllowPackageScripts</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagescripts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-128">AllowPublishingRefreshUX</span><span class="sxs-lookup"><span data-stu-id="d1631-128">AllowPublishingRefreshUX</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpublishingrefreshux)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-131">AllowReportingServer</span><span class="sxs-lookup"><span data-stu-id="d1631-131">AllowReportingServer</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowreportingserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-134">AllowRoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="d1631-134">AllowRoamingFileExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingfileexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-137">AllowRoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="d1631-137">AllowRoamingRegistryExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingregistryexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-140">AllowStreamingAutoload</span><span class="sxs-lookup"><span data-stu-id="d1631-140">AllowStreamingAutoload</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowstreamingautoload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-143">ClientCoexistenceAllowMigrationmode</span><span class="sxs-lookup"><span data-stu-id="d1631-143">ClientCoexistenceAllowMigrationmode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-clientcoexistenceallowmigrationmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d1631-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d1631-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1631-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1631-149">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d1631-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-150">IntegrationAllowRootGlobal</span><span class="sxs-lookup"><span data-stu-id="d1631-150">IntegrationAllowRootGlobal</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootglobal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-153">IntegrationAllowRootUser</span><span class="sxs-lookup"><span data-stu-id="d1631-153">IntegrationAllowRootUser</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootuser)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d1631-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d1631-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1631-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1631-159">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d1631-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-160">PublishingAllowServer1</span><span class="sxs-lookup"><span data-stu-id="d1631-160">PublishingAllowServer1</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver1)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-162">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-163">PublishingAllowServer2</span><span class="sxs-lookup"><span data-stu-id="d1631-163">PublishingAllowServer2</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver2)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-166">PublishingAllowServer3</span><span class="sxs-lookup"><span data-stu-id="d1631-166">PublishingAllowServer3</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-168">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-169">PublishingAllowServer4</span><span class="sxs-lookup"><span data-stu-id="d1631-169">PublishingAllowServer4</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-171">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-172">PublishingAllowServer5</span><span class="sxs-lookup"><span data-stu-id="d1631-172">PublishingAllowServer5</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver5)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-174">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-175">StreamingAllowCertificateFilterForClient \_ SSL</span><span class="sxs-lookup"><span data-stu-id="d1631-175">StreamingAllowCertificateFilterForClient\_SSL</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowcertificatefilterforclient-ssl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-177">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-177">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-178">StreamingAllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="d1631-178">StreamingAllowHighCostLaunch</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowhighcostlaunch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-180">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-180">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-181">StreamingAllowLocationProvider</span><span class="sxs-lookup"><span data-stu-id="d1631-181">StreamingAllowLocationProvider</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowlocationprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-183">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-183">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-184">StreamingAllowPackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="d1631-184">StreamingAllowPackageInstallationRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackageinstallationroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-186">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-186">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-187">StreamingAllowPackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="d1631-187">StreamingAllowPackageSourceRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackagesourceroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-189">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-190">StreamingAllowReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="d1631-190">StreamingAllowReestablishmentInterval</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-192">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-193">StreamingAllowReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="d1631-193">StreamingAllowReestablishmentRetries</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentretries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-195">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-196">StreamingSharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="d1631-196">StreamingSharedContentStoreMode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsharedcontentstoremode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-198">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-199">StreamingSupportBranchCache</span><span class="sxs-lookup"><span data-stu-id="d1631-199">StreamingSupportBranchCache</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsupportbranchcache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-201">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-202">StreamingVerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="d1631-202">StreamingVerifyCertificateRevocationList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingverifycertificaterevocationlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-204">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d1631-205">VirtualComponentsAllowList</span><span class="sxs-lookup"><span data-stu-id="d1631-205">VirtualComponentsAllowList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-virtualcomponentsallowlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1631-206">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d1631-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1631-207">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d1631-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1631-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1631-208">Requirements</span></span>



| <span data-ttu-id="d1631-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1631-209">Requirement</span></span> | <span data-ttu-id="d1631-210">Valor</span><span class="sxs-lookup"><span data-stu-id="d1631-210">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1631-211">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1631-211">Minimum supported client</span></span><br/> | <span data-ttu-id="d1631-212">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d1631-212">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1631-213">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1631-213">Minimum supported server</span></span><br/> | <span data-ttu-id="d1631-214">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d1631-214">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d1631-215">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1631-215">Namespace</span></span><br/>                | <span data-ttu-id="d1631-216">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="d1631-216">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d1631-217">MOF</span><span class="sxs-lookup"><span data-stu-id="d1631-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1631-218"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1631-218"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1631-219">DLL</span><span class="sxs-lookup"><span data-stu-id="d1631-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1631-220"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1631-220"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

