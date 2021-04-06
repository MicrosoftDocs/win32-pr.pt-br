---
title: Classe MDM_VPNv2_TrafficFilterList02_App04
description: A \_ classe MDM TrafficFilterList02 \_ App04 fornece a configuração dos aplicativos que são permitidos pela interface VPN.
ms.assetid: a56d004b-8fe3-4187-8aad-962f1cab8f7f
keywords:
- Classe MDM_VPNv2_TrafficFilterList02_App04
- Classe MDM_VPNv2_TrafficFilterList02_App04, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_App04
- MDM_VPNv2_TrafficFilterList02_App04.InstanceID
- MDM_VPNv2_TrafficFilterList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b1cd3edbfec5fa270f8404983af57dba4fad31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085980"
---
# <a name="mdm_vpnv2_trafficfilterlist02_app04-class"></a><span data-ttu-id="82c5e-105">\_Classe App04 do MDM VPNv2 \_ TrafficFilterList02 \_</span><span class="sxs-lookup"><span data-stu-id="82c5e-105">MDM\_VPNv2\_TrafficFilterList02\_App04 class</span></span>

<span data-ttu-id="82c5e-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="82c5e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="82c5e-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="82c5e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="82c5e-108">A classe **MDM \_ TrafficFilterList02 \_ App04** fornece a configuração dos aplicativos que são permitidos pela interface VPN.</span><span class="sxs-lookup"><span data-stu-id="82c5e-108">The **MDM\_TrafficFilterList02\_App04** class provides configuration of the apps that are allowed over the VPN interface.</span></span>

<span data-ttu-id="82c5e-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="82c5e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82c5e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82c5e-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="82c5e-111">Membros</span><span class="sxs-lookup"><span data-stu-id="82c5e-111">Members</span></span>

<span data-ttu-id="82c5e-112">A classe **App04 do MDM \_ VPNv2 \_ TrafficFilterList02 \_** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="82c5e-112">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="82c5e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82c5e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82c5e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="82c5e-114">Properties</span></span>

<span data-ttu-id="82c5e-115">A **classe \_ \_ \_ App04 TrafficFilterList02 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="82c5e-115">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="82c5e-116">Id</span><span class="sxs-lookup"><span data-stu-id="82c5e-116">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82c5e-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="82c5e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82c5e-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="82c5e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="82c5e-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="82c5e-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82c5e-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="82c5e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82c5e-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82c5e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82c5e-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="82c5e-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="82c5e-123">Regra de VPN por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="82c5e-123">Per app VPN rule.</span></span> <span data-ttu-id="82c5e-124">Isso permitirá que somente os aplicativos especificados sejam permitidos pela interface VPN.</span><span class="sxs-lookup"><span data-stu-id="82c5e-124">This will allow only the apps specified to be allowed over the VPN interface.</span></span> <span data-ttu-id="82c5e-125">Para essa classe, a cadeia de caracteres é "aplicativo"</span><span class="sxs-lookup"><span data-stu-id="82c5e-125">For this class, the string is "App"</span></span>

</dd> <dt>

<span data-ttu-id="82c5e-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="82c5e-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82c5e-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="82c5e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82c5e-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82c5e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82c5e-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="82c5e-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="82c5e-130">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="82c5e-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="82c5e-131">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*"</span><span class="sxs-lookup"><span data-stu-id="82c5e-131">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*"</span></span>

</dd> <dt>

[<span data-ttu-id="82c5e-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="82c5e-132">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="82c5e-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="82c5e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82c5e-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="82c5e-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82c5e-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82c5e-135">Requirements</span></span>



| <span data-ttu-id="82c5e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="82c5e-136">Requirement</span></span> | <span data-ttu-id="82c5e-137">Valor</span><span class="sxs-lookup"><span data-stu-id="82c5e-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82c5e-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82c5e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="82c5e-139">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="82c5e-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82c5e-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82c5e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="82c5e-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="82c5e-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="82c5e-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="82c5e-142">Namespace</span></span><br/>                | <span data-ttu-id="82c5e-143">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="82c5e-143">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="82c5e-144">MOF</span><span class="sxs-lookup"><span data-stu-id="82c5e-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82c5e-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82c5e-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="82c5e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="82c5e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82c5e-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82c5e-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82c5e-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="82c5e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82c5e-149">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="82c5e-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

