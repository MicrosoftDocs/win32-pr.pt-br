---
title: Classe MDM_Policy_Config01_WiFi02
description: A \_ classe MDM Policy \_ Config01 \_ WiFi02 representa as políticas de Wi-Fi disponíveis.
ms.assetid: 68CFBB5E-F365-4D1A-8EF1-CC070E9A7982
keywords:
- Classe MDM_Policy_Config01_WiFi02
- Classe MDM_Policy_Config01_WiFi02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WiFi02
- MDM_Policy_Config01_WiFi02.InstanceID
- MDM_Policy_Config01_WiFi02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00848613f1f0e9fd4ab6db9dc4afdabe54ce538c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824444"
---
# <a name="mdm_policy_config01_wifi02-class"></a><span data-ttu-id="3b61c-105">\_Classe MDM \_ Config01 \_ WiFi02</span><span class="sxs-lookup"><span data-stu-id="3b61c-105">MDM\_Policy\_Config01\_WiFi02 class</span></span>

<span data-ttu-id="3b61c-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="3b61c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3b61c-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="3b61c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3b61c-108">A classe **MDM \_ Policy \_ Config01 \_ WiFi02** representa as políticas de Wi-Fi disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3b61c-108">The **MDM\_Policy\_Config01\_WiFi02** class represents the Wi-Fi policies available.</span></span> <span data-ttu-id="3b61c-109">Essas políticas determinam Wi-Fi configurações permitidas.</span><span class="sxs-lookup"><span data-stu-id="3b61c-109">These policies determine Wi-Fi configurations that are allowed.</span></span>

<span data-ttu-id="3b61c-110">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3b61c-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b61c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b61c-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WiFi02
{
  string InstanceID;
  string ParentID;
  sint32 AllowInternetSharing;
  sint32 AllowWiFi;
  sint32 AllowWiFiDirect;
  sint32 AllowManualWiFiConfiguration;
  sint32 AllowAutoConnectToWiFiSenseHotspots;
  sint32 WLANScanMode;
};
```

## <a name="members"></a><span data-ttu-id="3b61c-112">Membros</span><span class="sxs-lookup"><span data-stu-id="3b61c-112">Members</span></span>

<span data-ttu-id="3b61c-113">A **classe \_ \_ Config01 \_ WiFi02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3b61c-113">The **MDM\_Policy\_Config01\_WiFi02** class has these types of members:</span></span>

-   [<span data-ttu-id="3b61c-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3b61c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b61c-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3b61c-115">Properties</span></span>

<span data-ttu-id="3b61c-116">A **classe \_ \_ Config01 \_ WiFi02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3b61c-116">The **MDM\_Policy\_Config01\_WiFi02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3b61c-117">AllowAutoConnectToWiFiSenseHotspots</span><span class="sxs-lookup"><span data-stu-id="3b61c-117">AllowAutoConnectToWiFiSenseHotspots</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowautoconnecttowifisensehotspots)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b61c-118">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b61c-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b61c-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b61c-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b61c-120">AllowInternetSharing</span><span class="sxs-lookup"><span data-stu-id="3b61c-120">AllowInternetSharing</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowinternetsharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b61c-121">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b61c-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b61c-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b61c-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b61c-123">AllowManualWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b61c-123">AllowManualWiFiConfiguration</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b61c-124">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b61c-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b61c-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b61c-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b61c-126">AllowWiFi</span><span class="sxs-lookup"><span data-stu-id="3b61c-126">AllowWiFi</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b61c-127">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b61c-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b61c-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b61c-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b61c-129">AllowWiFiDirect</span><span class="sxs-lookup"><span data-stu-id="3b61c-129">AllowWiFiDirect</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifidirect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b61c-130">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b61c-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b61c-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b61c-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b61c-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3b61c-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b61c-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3b61c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b61c-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b61c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b61c-135">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b61c-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3b61c-136">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="3b61c-136">Identifies the name of the parent node.</span></span> <span data-ttu-id="3b61c-137">Para essa classe, a cadeia de caracteres é "WiFi".</span><span class="sxs-lookup"><span data-stu-id="3b61c-137">For this class, the string is "WiFi".</span></span>

</dd> <dt>

<span data-ttu-id="3b61c-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3b61c-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b61c-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3b61c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b61c-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b61c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b61c-141">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b61c-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3b61c-142">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="3b61c-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="3b61c-143">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="3b61c-143">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="3b61c-144">WLANScanMode</span><span class="sxs-lookup"><span data-stu-id="3b61c-144">WLANScanMode</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-wlanscanmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b61c-145">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b61c-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b61c-146">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3b61c-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b61c-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b61c-147">Requirements</span></span>



| <span data-ttu-id="3b61c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b61c-148">Requirement</span></span> | <span data-ttu-id="3b61c-149">Valor</span><span class="sxs-lookup"><span data-stu-id="3b61c-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b61c-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b61c-150">Minimum supported client</span></span><br/> | <span data-ttu-id="3b61c-151">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3b61c-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b61c-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b61c-152">Minimum supported server</span></span><br/> | <span data-ttu-id="3b61c-153">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3b61c-153">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3b61c-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b61c-154">Namespace</span></span><br/>                | <span data-ttu-id="3b61c-155">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="3b61c-155">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="3b61c-156">MOF</span><span class="sxs-lookup"><span data-stu-id="3b61c-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b61c-157"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b61c-157"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b61c-158">DLL</span><span class="sxs-lookup"><span data-stu-id="3b61c-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b61c-159"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b61c-159"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b61c-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b61c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b61c-161">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="3b61c-161">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

