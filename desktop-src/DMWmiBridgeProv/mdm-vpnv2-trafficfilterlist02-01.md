---
title: Classe MDM_VPNv2_TrafficFilterList02_01
description: A \_ classe MDM VPNv2 \_ TrafficFilterList02 \_ 01 contém uma lista opcional de regras. Apenas o tráfego que corresponde a essas regras pode ser enviado por meio da Interface VPN.
ms.assetid: 3cffe96d-7454-43a1-aa5b-33e820369e7e
keywords:
- Classe MDM_VPNv2_TrafficFilterList02_01
- Classe MDM_VPNv2_TrafficFilterList02_01, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_01
- MDM_VPNv2_TrafficFilterList02_01.InstanceID
- MDM_VPNv2_TrafficFilterList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3005026a85aa118a4122e073579fcb06389a9fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085981"
---
# <a name="mdm_vpnv2_trafficfilterlist02_01-class"></a><span data-ttu-id="27015-106">\_Classe MDM VPNv2 \_ TrafficFilterList02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="27015-106">MDM\_VPNv2\_TrafficFilterList02\_01 class</span></span>

<span data-ttu-id="27015-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="27015-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="27015-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="27015-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="27015-109">A classe **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** contém uma lista opcional de regras.</span><span class="sxs-lookup"><span data-stu-id="27015-109">The **MDM\_VPNv2\_TrafficFilterList02\_01** class contains an optional list of rules.</span></span> <span data-ttu-id="27015-110">Apenas o tráfego que corresponde a essas regras pode ser enviado por meio da Interface VPN.</span><span class="sxs-lookup"><span data-stu-id="27015-110">Only traffic that matches these rules can be sent via the VPN Interface.</span></span>

<span data-ttu-id="27015-111">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="27015-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="27015-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27015-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_01
{
  string InstanceID;
  string ParentID;
  string Claims;
  sint32 Protocol;
  string LocalPortRanges;
  string RemotePortRanges;
  string LocalAddressRanges;
  string RemoteAddressRanges;
  string RoutingPolicyType;
};
```

## <a name="members"></a><span data-ttu-id="27015-113">Membros</span><span class="sxs-lookup"><span data-stu-id="27015-113">Members</span></span>

<span data-ttu-id="27015-114">A classe **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="27015-114">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="27015-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="27015-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27015-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="27015-116">Properties</span></span>

<span data-ttu-id="27015-117">A classe **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="27015-117">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="27015-118">Declarações</span><span class="sxs-lookup"><span data-stu-id="27015-118">Claims</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-claims)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27015-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="27015-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27015-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="27015-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="27015-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="27015-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27015-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="27015-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27015-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="27015-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27015-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="27015-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="27015-125">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="27015-125">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="27015-126">LocalAddressRanges</span><span class="sxs-lookup"><span data-stu-id="27015-126">LocalAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27015-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="27015-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27015-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="27015-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="27015-129">LocalPortRanges</span><span class="sxs-lookup"><span data-stu-id="27015-129">LocalPortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27015-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="27015-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27015-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="27015-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="27015-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="27015-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27015-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="27015-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27015-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="27015-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27015-135">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="27015-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="27015-136">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="27015-136">Describes the full path to the parent node.</span></span> <span data-ttu-id="27015-137">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList"</span><span class="sxs-lookup"><span data-stu-id="27015-137">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList"</span></span>

</dd> <dt>

[<span data-ttu-id="27015-138">Protocolo</span><span class="sxs-lookup"><span data-stu-id="27015-138">Protocol</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27015-139">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="27015-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27015-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="27015-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="27015-141">RemoteAddressRanges</span><span class="sxs-lookup"><span data-stu-id="27015-141">RemoteAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27015-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="27015-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27015-143">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="27015-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="27015-144">RemotePortRanges</span><span class="sxs-lookup"><span data-stu-id="27015-144">RemotePortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27015-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="27015-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27015-146">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="27015-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="27015-147">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="27015-147">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="27015-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="27015-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27015-149">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="27015-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27015-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27015-150">Requirements</span></span>



| <span data-ttu-id="27015-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="27015-151">Requirement</span></span> | <span data-ttu-id="27015-152">Valor</span><span class="sxs-lookup"><span data-stu-id="27015-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27015-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27015-153">Minimum supported client</span></span><br/> | <span data-ttu-id="27015-154">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="27015-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27015-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27015-155">Minimum supported server</span></span><br/> | <span data-ttu-id="27015-156">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="27015-156">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="27015-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="27015-157">Namespace</span></span><br/>                | <span data-ttu-id="27015-158">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="27015-158">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="27015-159">MOF</span><span class="sxs-lookup"><span data-stu-id="27015-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27015-160"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27015-160"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="27015-161">DLL</span><span class="sxs-lookup"><span data-stu-id="27015-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27015-162"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27015-162"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27015-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="27015-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27015-164">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="27015-164">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

