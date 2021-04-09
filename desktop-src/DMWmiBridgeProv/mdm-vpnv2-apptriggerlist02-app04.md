---
title: Classe MDM_VPNv2_AppTriggerList02_App04
description: A \_ classe MDM VPNv2AppTriggerList02 \_ App04 descreve uma lista de aplicativos definidos para disparar a VPN.
ms.assetid: d17ec7b9-8a66-47da-8373-81b56168b495
keywords:
- Classe MDM_VPNv2_AppTriggerList02_App04
- Classe MDM_VPNv2_AppTriggerList02_App04, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_AppTriggerList02_App04
- MDM_VPNv2_AppTriggerList02_App04.InstanceID
- MDM_VPNv2_AppTriggerList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62685ea94b99e843625e87e7c653a2ff19ab737d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085718"
---
# <a name="mdm_vpnv2_apptriggerlist02_app04-class"></a><span data-ttu-id="c6d6c-105">\_Classe App04 do MDM VPNv2 \_ AppTriggerList02 \_</span><span class="sxs-lookup"><span data-stu-id="c6d6c-105">MDM\_VPNv2\_AppTriggerList02\_App04 class</span></span>

<span data-ttu-id="c6d6c-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c6d6c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c6d6c-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c6d6c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c6d6c-108">A classe **MDM \_ VPNv2AppTriggerList02 \_ App04** descreve uma lista de aplicativos definidos para disparar a VPN.</span><span class="sxs-lookup"><span data-stu-id="c6d6c-108">The **MDM\_VPNv2AppTriggerList02\_App04** class describes a list of applications set to trigger the VPN.</span></span>

<span data-ttu-id="c6d6c-109">Se qualquer um desses aplicativos for iniciado e o perfil de VPN for o perfil ativo no momento, esse perfil de VPN será disparado para se conectar.</span><span class="sxs-lookup"><span data-stu-id="c6d6c-109">If any of these apps are launched and the VPN profile is currently the active profile, this VPN profile will be triggered to connect.</span></span>

<span data-ttu-id="c6d6c-110">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c6d6c-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d6c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6d6c-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_AppTriggerList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="c6d6c-112">Membros</span><span class="sxs-lookup"><span data-stu-id="c6d6c-112">Members</span></span>

<span data-ttu-id="c6d6c-113">A classe **App04 do MDM \_ VPNv2 \_ AppTriggerList02 \_** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c6d6c-113">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="c6d6c-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c6d6c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6d6c-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c6d6c-115">Properties</span></span>

<span data-ttu-id="c6d6c-116">A **classe \_ \_ \_ App04 AppTriggerList02 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c6d6c-116">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c6d6c-117">Id</span><span class="sxs-lookup"><span data-stu-id="c6d6c-117">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d6c-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c6d6c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6d6c-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c6d6c-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c6d6c-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c6d6c-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d6c-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c6d6c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6d6c-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c6d6c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6d6c-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c6d6c-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c6d6c-124">Nó de aplicativo sob a ID de linha.</span><span class="sxs-lookup"><span data-stu-id="c6d6c-124">App Node under the Row Id.</span></span>

</dd> <dt>

<span data-ttu-id="c6d6c-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c6d6c-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d6c-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c6d6c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6d6c-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c6d6c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6d6c-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c6d6c-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c6d6c-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="c6d6c-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="c6d6c-130">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"</span><span class="sxs-lookup"><span data-stu-id="c6d6c-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"</span></span>

</dd> <dt>

[<span data-ttu-id="c6d6c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6d6c-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6d6c-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c6d6c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6d6c-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c6d6c-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6d6c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6d6c-134">Requirements</span></span>



| <span data-ttu-id="c6d6c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6d6c-135">Requirement</span></span> | <span data-ttu-id="c6d6c-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c6d6c-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d6c-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6d6c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d6c-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c6d6c-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6d6c-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6d6c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d6c-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c6d6c-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c6d6c-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6d6c-141">Namespace</span></span><br/>                | <span data-ttu-id="c6d6c-142">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c6d6c-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c6d6c-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c6d6c-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6d6c-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6d6c-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6d6c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c6d6c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6d6c-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6d6c-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d6c-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6d6c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d6c-148">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="c6d6c-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

