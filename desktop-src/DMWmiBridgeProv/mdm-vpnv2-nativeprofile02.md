---
title: Classe MDM_VPNv2_NativeProfile02
description: A \_ classe MDM VPNv2 \_ NativeProfile2 define informações de perfil ao usar um protocolo de VPN da caixa de entrada do Windows (IKEV2, PPTP, L2TP).
ms.assetid: 50c4adc6-baef-437c-8223-9aeaaec813af
keywords:
- Classe MDM_VPNv2_NativeProfile02
- Classe MDM_VPNv2_NativeProfile02, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_NativeProfile02
- MDM_VPNv2_NativeProfile02.InstanceID
- MDM_VPNv2_NativeProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8573975c488df6e5c759e719d5c687f6a71c505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824704"
---
# <a name="mdm_vpnv2_nativeprofile02-class"></a><span data-ttu-id="674ae-105">\_ \_ Classe NATIVEPROFILE02 do MDM VPNv2</span><span class="sxs-lookup"><span data-stu-id="674ae-105">MDM\_VPNv2\_NativeProfile02 class</span></span>

<span data-ttu-id="674ae-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="674ae-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="674ae-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="674ae-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="674ae-108">A classe **MDM \_ VPNv2 \_ NativeProfile2** define informações de perfil ao usar um protocolo de VPN da caixa de entrada do Windows (IKEV2, PPTP, L2TP).</span><span class="sxs-lookup"><span data-stu-id="674ae-108">The **MDM\_VPNv2\_NativeProfile2** class defines profile information when using a Windows Inbox VPN Protocol (IKEv2, PPTP, L2TP).</span></span>

<span data-ttu-id="674ae-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="674ae-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="674ae-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="674ae-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_NativeProfile02
{
  string InstanceID;
  string ParentID;
  string Servers;
  string RoutingPolicyType;
  string NativeProtocolType;
  string L2tpPsk;
};
```

## <a name="members"></a><span data-ttu-id="674ae-111">Membros</span><span class="sxs-lookup"><span data-stu-id="674ae-111">Members</span></span>

<span data-ttu-id="674ae-112">A **classe \_ \_ NativeProfile02 de MDM VPNv2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="674ae-112">The **MDM\_VPNv2\_NativeProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="674ae-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="674ae-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="674ae-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="674ae-114">Properties</span></span>

<span data-ttu-id="674ae-115">A **classe \_ \_ NativeProfile02 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="674ae-115">The **MDM\_VPNv2\_NativeProfile02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="674ae-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="674ae-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="674ae-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="674ae-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="674ae-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="674ae-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="674ae-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="674ae-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="674ae-120">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="674ae-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="674ae-121">L2tpPsk</span><span class="sxs-lookup"><span data-stu-id="674ae-121">L2tpPsk</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-l2tppsk)
</dt> <dd> <dl> <dt>

<span data-ttu-id="674ae-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="674ae-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="674ae-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="674ae-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="674ae-124">NativeProtocolType</span><span class="sxs-lookup"><span data-stu-id="674ae-124">NativeProtocolType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-nativeprotocoltype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="674ae-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="674ae-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="674ae-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="674ae-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="674ae-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="674ae-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="674ae-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="674ae-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="674ae-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="674ae-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="674ae-130">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="674ae-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="674ae-131">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="674ae-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="674ae-132">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="674ae-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="674ae-133">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="674ae-133">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="674ae-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="674ae-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="674ae-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="674ae-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="674ae-136">Servidores</span><span class="sxs-lookup"><span data-stu-id="674ae-136">Servers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-servers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="674ae-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="674ae-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="674ae-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="674ae-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="674ae-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="674ae-139">Requirements</span></span>



| <span data-ttu-id="674ae-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="674ae-140">Requirement</span></span> | <span data-ttu-id="674ae-141">Valor</span><span class="sxs-lookup"><span data-stu-id="674ae-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="674ae-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="674ae-142">Minimum supported client</span></span><br/> | <span data-ttu-id="674ae-143">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="674ae-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="674ae-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="674ae-144">Minimum supported server</span></span><br/> | <span data-ttu-id="674ae-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="674ae-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="674ae-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="674ae-146">Namespace</span></span><br/>                | <span data-ttu-id="674ae-147">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="674ae-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="674ae-148">MOF</span><span class="sxs-lookup"><span data-stu-id="674ae-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="674ae-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="674ae-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="674ae-150">DLL</span><span class="sxs-lookup"><span data-stu-id="674ae-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="674ae-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="674ae-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="674ae-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="674ae-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="674ae-153">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="674ae-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

