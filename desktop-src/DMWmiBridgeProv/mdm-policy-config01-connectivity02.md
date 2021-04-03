---
title: Classe MDM_Policy_Config01_Connectivity02
description: A \_ classe MDM Policy \_ Config01 \_ Connectivity02 representa as políticas de conexão disponíveis.
ms.assetid: 670e48c2-1af1-45e9-81c6-cdf3a310240f
keywords:
- Classe MDM_Policy_Config01_Connectivity02
- Classe MDM_Policy_Config01_Connectivity02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Connectivity02
- MDM_Policy_Config01_Connectivity02.InstanceID
- MDM_Policy_Config01_Connectivity02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b39b897998bf47c5f5411456ccae7fcb6927aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644516"
---
# <a name="mdm_policy_config01_connectivity02-class"></a><span data-ttu-id="4ec02-105">\_Classe MDM \_ Config01 \_ Connectivity02</span><span class="sxs-lookup"><span data-stu-id="4ec02-105">MDM\_Policy\_Config01\_Connectivity02 class</span></span>

<span data-ttu-id="4ec02-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="4ec02-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4ec02-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="4ec02-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4ec02-108">A classe **MDM \_ Policy \_ Config01 \_ Connectivity02** representa as políticas de conexão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4ec02-108">The **MDM\_Policy\_Config01\_Connectivity02** class represents the connection policies available.</span></span>

<span data-ttu-id="4ec02-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4ec02-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec02-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ec02-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Connectivity02
{
  string InstanceID;
  string ParentID;
  sint32 AllowBluetooth;
  sint32 AllowCellularData;
  sint32 AllowCellularDataRoaming;
  sint32 AllowVPNOverCellular;
  sint32 AllowVPNRoamingOverCellular;
  string DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards;
  string DisableDownloadingOfPrintDriversOverHTTP;
  string DiablePrintingOverHTTP;
  string HardenedUNCPaths;
  string ProhibitInstallationAndConfigurationOfNetworkBridge;
  sint32 DisallowNetworkConnectivityActiveTests;
  sint32 AllowConnectedDevices;
};
```

## <a name="members"></a><span data-ttu-id="4ec02-111">Membros</span><span class="sxs-lookup"><span data-stu-id="4ec02-111">Members</span></span>

<span data-ttu-id="4ec02-112">A **classe \_ \_ Config01 \_ Connectivity02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4ec02-112">The **MDM\_Policy\_Config01\_Connectivity02** class has these types of members:</span></span>

-   [<span data-ttu-id="4ec02-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4ec02-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ec02-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4ec02-114">Properties</span></span>

<span data-ttu-id="4ec02-115">A **classe \_ \_ Config01 \_ Connectivity02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4ec02-115">The **MDM\_Policy\_Config01\_Connectivity02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4ec02-116">AllowBluetooth</span><span class="sxs-lookup"><span data-stu-id="4ec02-116">AllowBluetooth</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4ec02-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4ec02-119">AllowCellularData</span><span class="sxs-lookup"><span data-stu-id="4ec02-119">AllowCellularData</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4ec02-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4ec02-122">AllowCellularDataRoaming</span><span class="sxs-lookup"><span data-stu-id="4ec02-122">AllowCellularDataRoaming</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardataroaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4ec02-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4ec02-125">AllowConnectedDevices</span><span class="sxs-lookup"><span data-stu-id="4ec02-125">AllowConnectedDevices</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowconnecteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4ec02-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4ec02-128">AllowVPNOverCellular</span><span class="sxs-lookup"><span data-stu-id="4ec02-128">AllowVPNOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4ec02-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4ec02-131">AllowVPNRoamingOverCellular</span><span class="sxs-lookup"><span data-stu-id="4ec02-131">AllowVPNRoamingOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnroamingovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4ec02-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4ec02-134">DiablePrintingOverHTTP</span><span class="sxs-lookup"><span data-stu-id="4ec02-134">DiablePrintingOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-diableprintingoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ec02-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4ec02-137">DisableDownloadingOfPrintDriversOverHTTP</span><span class="sxs-lookup"><span data-stu-id="4ec02-137">DisableDownloadingOfPrintDriversOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disabledownloadingofprintdriversoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ec02-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4ec02-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span><span class="sxs-lookup"><span data-stu-id="4ec02-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disableinternetdownloadforwebpublishingandonlineorderingwizards)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ec02-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4ec02-143">DisallowNetworkConnectivityActiveTests</span><span class="sxs-lookup"><span data-stu-id="4ec02-143">DisallowNetworkConnectivityActiveTests</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disallownetworkconnectivityactivetests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4ec02-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4ec02-146">HardenedUNCPaths</span><span class="sxs-lookup"><span data-stu-id="4ec02-146">HardenedUNCPaths</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-hardeneduncpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ec02-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4ec02-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4ec02-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ec02-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ec02-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-152">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4ec02-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4ec02-153">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="4ec02-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="4ec02-154">Para essa classe, a cadeia de caracteres é "conectividade".</span><span class="sxs-lookup"><span data-stu-id="4ec02-154">For this class, the string is "Connectivity".</span></span>

</dd> <dt>

<span data-ttu-id="4ec02-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4ec02-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ec02-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ec02-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-158">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4ec02-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4ec02-159">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="4ec02-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="4ec02-160">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="4ec02-160">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="4ec02-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span><span class="sxs-lookup"><span data-stu-id="4ec02-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-prohibitinstallationandconfigurationofnetworkbridge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec02-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ec02-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ec02-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4ec02-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ec02-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ec02-164">Requirements</span></span>



| <span data-ttu-id="4ec02-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ec02-165">Requirement</span></span> | <span data-ttu-id="4ec02-166">Valor</span><span class="sxs-lookup"><span data-stu-id="4ec02-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec02-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ec02-167">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec02-168">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4ec02-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ec02-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ec02-169">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec02-170">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4ec02-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4ec02-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ec02-171">Namespace</span></span><br/>                | <span data-ttu-id="4ec02-172">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="4ec02-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="4ec02-173">MOF</span><span class="sxs-lookup"><span data-stu-id="4ec02-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ec02-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ec02-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ec02-175">DLL</span><span class="sxs-lookup"><span data-stu-id="4ec02-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ec02-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ec02-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ec02-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ec02-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec02-178">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="4ec02-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

