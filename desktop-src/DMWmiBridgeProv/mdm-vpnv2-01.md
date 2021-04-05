---
title: Classe MDM_VPNv2_01
description: A \_ classe MDM VPNv2 \_ 01 permite a configuração do perfil VPN do dispositivo.
ms.assetid: cfef674b-880c-4c9f-a2c1-6c2cb03189da
keywords:
- Classe MDM_VPNv2_01
- Classe MDM_VPNv2_01, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_01
- MDM_VPNv2_01.InstanceID
- MDM_VPNv2_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3457220c438d0143db90c1955d48352353fee29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918609"
---
# <a name="mdm_vpnv2_01-class"></a><span data-ttu-id="5488a-105">\_Classe MDM VPNv2 \_ 01</span><span class="sxs-lookup"><span data-stu-id="5488a-105">MDM\_VPNv2\_01 class</span></span>

<span data-ttu-id="5488a-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="5488a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5488a-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="5488a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5488a-108">A classe **MDM \_ VPNv2 \_ 01** permite a configuração do perfil VPN do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5488a-108">The **MDM\_VPNv2\_01** class allows configuration of the VPN profile of the device.</span></span>

<span data-ttu-id="5488a-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5488a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5488a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5488a-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_01
{
  string  InstanceID;
  string  ParentID;
  string  EdpModeId;
  boolean RememberCredentials;
  boolean AlwaysOn;
  string  DnsSuffix;
  boolean ByPassForLocal;
  string  TrustedNetworkDetection;
  string  ProfileXML;
  boolean LockDown;
};
```

## <a name="members"></a><span data-ttu-id="5488a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5488a-111">Members</span></span>

<span data-ttu-id="5488a-112">A classe **MDM \_ VPNv2 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5488a-112">The **MDM\_VPNv2\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="5488a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5488a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5488a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5488a-114">Properties</span></span>

<span data-ttu-id="5488a-115">A classe **MDM \_ VPNv2 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5488a-115">The **MDM\_VPNv2\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5488a-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="5488a-116">AlwaysOn</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5488a-117">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5488a-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5488a-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5488a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5488a-119">ByPassForLocal</span><span class="sxs-lookup"><span data-stu-id="5488a-119">ByPassForLocal</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-bypassforlocal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5488a-120">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5488a-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5488a-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5488a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5488a-122">DnsSuffix</span><span class="sxs-lookup"><span data-stu-id="5488a-122">DnsSuffix</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-dnssuffix)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5488a-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5488a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5488a-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5488a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5488a-125">EdpModeId</span><span class="sxs-lookup"><span data-stu-id="5488a-125">EdpModeId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-edpmodeid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5488a-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5488a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5488a-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5488a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5488a-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5488a-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5488a-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5488a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5488a-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5488a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5488a-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5488a-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5488a-132">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="5488a-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="5488a-133">Para essa classe, a cadeia de caracteres é o nome do perfil de VPN.</span><span class="sxs-lookup"><span data-stu-id="5488a-133">For this class, the string is the VPN profile name.</span></span>

</dd> <dt>

[<span data-ttu-id="5488a-134">LockDown</span><span class="sxs-lookup"><span data-stu-id="5488a-134">LockDown</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-lockdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5488a-135">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5488a-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5488a-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5488a-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5488a-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5488a-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5488a-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5488a-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5488a-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5488a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5488a-140">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5488a-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5488a-141">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="5488a-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="5488a-142">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2"</span><span class="sxs-lookup"><span data-stu-id="5488a-142">For this class, the string is "./Vendor/MSFT/VPNv2"</span></span>

</dd> <dt>

[<span data-ttu-id="5488a-143">ProfileXML</span><span class="sxs-lookup"><span data-stu-id="5488a-143">ProfileXML</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-profilexml)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5488a-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5488a-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5488a-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5488a-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5488a-146">RememberCredentials</span><span class="sxs-lookup"><span data-stu-id="5488a-146">RememberCredentials</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-remembercredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5488a-147">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5488a-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5488a-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5488a-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5488a-149">TrustedNetworkDetection</span><span class="sxs-lookup"><span data-stu-id="5488a-149">TrustedNetworkDetection</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trustednetworkdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5488a-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5488a-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5488a-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5488a-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5488a-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5488a-152">Requirements</span></span>



| <span data-ttu-id="5488a-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="5488a-153">Requirement</span></span> | <span data-ttu-id="5488a-154">Valor</span><span class="sxs-lookup"><span data-stu-id="5488a-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5488a-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5488a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="5488a-156">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5488a-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5488a-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5488a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="5488a-158">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5488a-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5488a-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="5488a-159">Namespace</span></span><br/>                | <span data-ttu-id="5488a-160">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5488a-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5488a-161">MOF</span><span class="sxs-lookup"><span data-stu-id="5488a-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5488a-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5488a-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5488a-163">DLL</span><span class="sxs-lookup"><span data-stu-id="5488a-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5488a-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5488a-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5488a-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="5488a-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5488a-166">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="5488a-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

