---
title: Classe MDM_Policy_Result01_DeliveryOptimization02
description: A \_ classe MDM Policy \_ Result01 \_ DeliveryOptimization02 representa as políticas de otimização de entrega disponíveis.
ms.assetid: 0f8a6de1-0f6c-4ee2-9235-9b5dc855f8c4
keywords:
- Classe MDM_Policy_Result01_DeliveryOptimization02
- Classe MDM_Policy_Result01_DeliveryOptimization02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeliveryOptimization02
- MDM_Policy_Result01_DeliveryOptimization02.InstanceID
- MDM_Policy_Result01_DeliveryOptimization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69408228b2ed67c12de83575ddc524387498e91a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644446"
---
# <a name="mdm_policy_result01_deliveryoptimization02-class"></a><span data-ttu-id="0d339-105">\_Classe MDM \_ Result01 \_ DeliveryOptimization02</span><span class="sxs-lookup"><span data-stu-id="0d339-105">MDM\_Policy\_Result01\_DeliveryOptimization02 class</span></span>

<span data-ttu-id="0d339-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0d339-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0d339-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0d339-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0d339-108">A classe **MDM \_ Policy \_ Result01 \_ DeliveryOptimization02** representa as políticas de otimização de entrega disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0d339-108">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class represents the delivery optimization policies available.</span></span>

<span data-ttu-id="0d339-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0d339-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d339-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d339-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeliveryOptimization02
{
  string InstanceID;
  string ParentID;
  sint32 DOAbsoluteMaxCacheSize;
  sint32 DOAllowVPNPeerCaching;
  string DOCacheHost;
  string DOGroupID;
  sint32 DOMaxUploadBandwidth;
  sint32 DOPercentageMaxDownloadBandwidth;
  sint32 DOMonthlyUploadDataCap;
  string DOModifyCacheDrive;
  sint32 DOMinBackgroundQos;
  sint32 DOMinRAMAllowedToPeer;
  sint32 DOMinFileSizeToCache;
  sint32 DOMinDiskSizeAllowedToPeer;
  sint32 DOMinBatteryPercentageAllowedToUpload;
  sint32 DOMaxCacheSize;
  sint32 DOMaxDownloadBandwidth;
  sint32 DOMaxCacheAge;
  sint32 DODownloadMode;
};
```

## <a name="members"></a><span data-ttu-id="0d339-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0d339-111">Members</span></span>

<span data-ttu-id="0d339-112">A **classe \_ \_ Result01 \_ DeliveryOptimization02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0d339-112">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class has these types of members:</span></span>

-   [<span data-ttu-id="0d339-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d339-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d339-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d339-114">Properties</span></span>

<span data-ttu-id="0d339-115">A **classe \_ \_ Result01 \_ DeliveryOptimization02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d339-115">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0d339-116">DOAbsoluteMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="0d339-116">DOAbsoluteMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doabsolutemaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-119">DOAllowVPNPeerCaching</span><span class="sxs-lookup"><span data-stu-id="0d339-119">DOAllowVPNPeerCaching</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doallowvpnpeercaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-122">DOCacheHost</span><span class="sxs-lookup"><span data-stu-id="0d339-122">DOCacheHost</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d339-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-125">DODownloadMode</span><span class="sxs-lookup"><span data-stu-id="0d339-125">DODownloadMode</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-128">Dogroupid</span><span class="sxs-lookup"><span data-stu-id="0d339-128">DOGroupID</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dogroupid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d339-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-131">DOMaxCacheAge</span><span class="sxs-lookup"><span data-stu-id="0d339-131">DOMaxCacheAge</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcacheage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-134">DOMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="0d339-134">DOMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-137">DOMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="0d339-137">DOMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-138">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-140">DOMaxUploadBandwidth</span><span class="sxs-lookup"><span data-stu-id="0d339-140">DOMaxUploadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxuploadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-143">DOMinBackgroundQos</span><span class="sxs-lookup"><span data-stu-id="0d339-143">DOMinBackgroundQos</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbackgroundqos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-146">DOMinBatteryPercentageAllowedToUpload</span><span class="sxs-lookup"><span data-stu-id="0d339-146">DOMinBatteryPercentageAllowedToUpload</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbatterypercentageallowedtoupload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-149">DOMinDiskSizeAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="0d339-149">DOMinDiskSizeAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domindisksizeallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-152">DOMinFileSizeToCache</span><span class="sxs-lookup"><span data-stu-id="0d339-152">DOMinFileSizeToCache</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominfilesizetocache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-153">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-155">DOMinRAMAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="0d339-155">DOMinRAMAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominramallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-156">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-158">DOModifyCacheDrive</span><span class="sxs-lookup"><span data-stu-id="0d339-158">DOModifyCacheDrive</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domodifycachedrive)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d339-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-161">DOMonthlyUploadDataCap</span><span class="sxs-lookup"><span data-stu-id="0d339-161">DOMonthlyUploadDataCap</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domonthlyuploaddatacap)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-162">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0d339-164">DOPercentageMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="0d339-164">DOPercentageMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-165">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0d339-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d339-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0d339-167">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0d339-167">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d339-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d339-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d339-170">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0d339-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0d339-171">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="0d339-171">Identifies the name of the parent node.</span></span> <span data-ttu-id="0d339-172">Para essa classe, a cadeia de caracteres é "DeliveryOptimization".</span><span class="sxs-lookup"><span data-stu-id="0d339-172">For this class, the string is "DeliveryOptimization".</span></span>

</dd> <dt>

<span data-ttu-id="0d339-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0d339-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d339-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d339-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d339-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d339-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d339-176">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0d339-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0d339-177">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="0d339-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="0d339-178">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="0d339-178">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d339-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d339-179">Requirements</span></span>



| <span data-ttu-id="0d339-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d339-180">Requirement</span></span> | <span data-ttu-id="0d339-181">Valor</span><span class="sxs-lookup"><span data-stu-id="0d339-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d339-182">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d339-182">Minimum supported client</span></span><br/> | <span data-ttu-id="0d339-183">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0d339-183">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d339-184">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d339-184">Minimum supported server</span></span><br/> | <span data-ttu-id="0d339-185">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0d339-185">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0d339-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d339-186">Namespace</span></span><br/>                | <span data-ttu-id="0d339-187">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0d339-187">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="0d339-188">MOF</span><span class="sxs-lookup"><span data-stu-id="0d339-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d339-189"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d339-189"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d339-190">DLL</span><span class="sxs-lookup"><span data-stu-id="0d339-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d339-191"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d339-191"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d339-192">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d339-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d339-193">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="0d339-193">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

