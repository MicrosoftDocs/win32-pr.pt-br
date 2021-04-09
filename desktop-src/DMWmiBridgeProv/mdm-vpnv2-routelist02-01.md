---
title: Classe MDM_VPNv2_RouteList02_01
description: A \_ classe MDM VPNv2 \_ RouteList02 \_ 01 contém uma lista opcional de rotas a serem adicionadas à tabela de roteamento para a interface VPN.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- Classe MDM_VPNv2_RouteList02_01
- Classe MDM_VPNv2_RouteList02_01, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebc274bb3efd2bc78850dd37c95b25db35c4cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009587"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a><span data-ttu-id="5f8b7-105">\_Classe MDM VPNv2 \_ RouteList02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="5f8b7-105">MDM\_VPNv2\_RouteList02\_01 class</span></span>

<span data-ttu-id="5f8b7-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5f8b7-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="5f8b7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5f8b7-108">A classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** contém uma lista opcional de rotas a serem adicionadas à tabela de roteamento para a interface VPN.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-108">The **MDM\_VPNv2\_RouteList02\_01** class contains an optional list of routes to be added to the routing table for the VPN interface.</span></span>

<span data-ttu-id="5f8b7-109">Isso é necessário para o caso de túnel dividido em que o site do servidor VPN tem mais sub-redes que a sub-rede padrão com base no IP atribuído à interface.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-109">This is required for split tunneling case where the VPN server site has more subnets that the default subnet based on the IP assigned to the interface.</span></span>

<span data-ttu-id="5f8b7-110">Cada computador que executa TCP/IP toma decisões de roteamento.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-110">Every computer that runs TCP/IP makes routing decisions.</span></span> <span data-ttu-id="5f8b7-111">Essas decisões são controladas pela tabela de roteamento de IP.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-111">These decisions are controlled by the IP routing table.</span></span> <span data-ttu-id="5f8b7-112">A adição de valores sob esse nó atualiza a tabela de roteamento com rotas para a interface VPN post Connection.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-112">Adding values under this node updates the routing table with routes for the VPN interface post connection.</span></span> <span data-ttu-id="5f8b7-113">Os valores sob esse nó representam o prefixo de destino das rotas de IP.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-113">The values under this node represent the destination prefix of IP routes.</span></span> <span data-ttu-id="5f8b7-114">Um prefixo de destino consiste em um prefixo de endereço IP e um comprimento de prefixo.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-114">A destination prefix consists of an IP address prefix and a prefix length.</span></span>

<span data-ttu-id="5f8b7-115">Adicionar uma rota aqui permite que a pilha de rede identifique o tráfego que precisa passar pela interface VPN para VPN de túnel dividido.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-115">Adding a route here allows the networking stack to identify the traffic that needs to go over the VPN interface for split tunnel VPN.</span></span> <span data-ttu-id="5f8b7-116">Alguns servidores VPN podem configurar isso durante a negociação de conexão e não precisam dessas informações no perfil de VPN.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-116">Some VPN servers can configure this during connect negotiation and do not need this information in the VPN Profile.</span></span> <span data-ttu-id="5f8b7-117">Consulte o administrador do servidor VPN para determinar se você precisa dessas informações no perfil VPN.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-117">Please check with your VPN server administrator to determine whether you need this information in the VPN profile.</span></span>

<span data-ttu-id="5f8b7-118">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-118">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8b7-119">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f8b7-119">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a><span data-ttu-id="5f8b7-120">Membros</span><span class="sxs-lookup"><span data-stu-id="5f8b7-120">Members</span></span>

<span data-ttu-id="5f8b7-121">A classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5f8b7-121">The **MDM\_VPNv2\_RouteList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="5f8b7-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f8b7-122">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f8b7-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f8b7-123">Properties</span></span>

<span data-ttu-id="5f8b7-124">A classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-124">The **MDM\_VPNv2\_RouteList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5f8b7-125">Endereço</span><span class="sxs-lookup"><span data-stu-id="5f8b7-125">Address</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f8b7-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f8b7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f8b7-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5f8b7-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5f8b7-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5f8b7-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f8b7-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f8b7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f8b7-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f8b7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f8b7-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f8b7-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5f8b7-132">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-132">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="5f8b7-133">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5f8b7-133">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f8b7-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f8b7-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f8b7-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f8b7-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f8b7-136">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f8b7-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5f8b7-137">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="5f8b7-137">Describes the full path to the parent node.</span></span> <span data-ttu-id="5f8b7-138">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"</span><span class="sxs-lookup"><span data-stu-id="5f8b7-138">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"</span></span>

</dd> <dt>

[<span data-ttu-id="5f8b7-139">PrefixSize</span><span class="sxs-lookup"><span data-stu-id="5f8b7-139">PrefixSize</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f8b7-140">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f8b7-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f8b7-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5f8b7-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f8b7-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f8b7-142">Requirements</span></span>



| <span data-ttu-id="5f8b7-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f8b7-143">Requirement</span></span> | <span data-ttu-id="5f8b7-144">Valor</span><span class="sxs-lookup"><span data-stu-id="5f8b7-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8b7-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f8b7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5f8b7-146">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5f8b7-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f8b7-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f8b7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5f8b7-148">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5f8b7-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5f8b7-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f8b7-149">Namespace</span></span><br/>                | <span data-ttu-id="5f8b7-150">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5f8b7-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5f8b7-151">MOF</span><span class="sxs-lookup"><span data-stu-id="5f8b7-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f8b7-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f8b7-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f8b7-153">DLL</span><span class="sxs-lookup"><span data-stu-id="5f8b7-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f8b7-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f8b7-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f8b7-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f8b7-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8b7-156">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="5f8b7-156">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

