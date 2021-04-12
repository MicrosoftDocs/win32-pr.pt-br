---
title: Classe MDM_VPNv2_Proxy02
description: A \_ classe MDM VPNv2 \_ Proxy02 define um objeto de configuração para habilitar um suporte de proxy pós-conexão para VPN.
ms.assetid: 243f0824-4951-41c4-b8b4-b5c39aefd8ff
keywords:
- Classe MDM_VPNv2_Proxy02
- Classe MDM_VPNv2_Proxy02, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Proxy02
- MDM_VPNv2_Proxy02.InstanceID
- MDM_VPNv2_Proxy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf8197379f5b1ff69433baa845af2cd53bb9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455163"
---
# <a name="mdm_vpnv2_proxy02-class"></a><span data-ttu-id="b38e8-105">\_ \_ Classe PROXY02 do MDM VPNv2</span><span class="sxs-lookup"><span data-stu-id="b38e8-105">MDM\_VPNv2\_Proxy02 class</span></span>

<span data-ttu-id="b38e8-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="b38e8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b38e8-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="b38e8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b38e8-108">A classe **MDM \_ VPNv2 \_ Proxy02** define um objeto de configuração para habilitar um suporte de proxy pós-conexão para VPN.</span><span class="sxs-lookup"><span data-stu-id="b38e8-108">The **MDM\_VPNv2\_Proxy02** class defines a configuration object to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="b38e8-109">O proxy definido para esse perfil é aplicado quando esse perfil está ativo e conectado.</span><span class="sxs-lookup"><span data-stu-id="b38e8-109">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

<span data-ttu-id="b38e8-110">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b38e8-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b38e8-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b38e8-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Proxy02
{
  string InstanceID;
  string ParentID;
  string AutoConfigUrl;
};
```

## <a name="members"></a><span data-ttu-id="b38e8-112">Membros</span><span class="sxs-lookup"><span data-stu-id="b38e8-112">Members</span></span>

<span data-ttu-id="b38e8-113">A **classe \_ \_ Proxy02 de MDM VPNv2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b38e8-113">The **MDM\_VPNv2\_Proxy02** class has these types of members:</span></span>

-   [<span data-ttu-id="b38e8-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b38e8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b38e8-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b38e8-115">Properties</span></span>

<span data-ttu-id="b38e8-116">A **classe \_ \_ Proxy02 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b38e8-116">The **MDM\_VPNv2\_Proxy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b38e8-117">AutoConfigUrl</span><span class="sxs-lookup"><span data-stu-id="b38e8-117">AutoConfigUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-autoconfigurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b38e8-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b38e8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b38e8-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b38e8-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b38e8-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b38e8-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b38e8-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b38e8-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b38e8-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b38e8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b38e8-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b38e8-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b38e8-124">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="b38e8-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="b38e8-125">Uma coleção de objetos de configuração para habilitar um suporte de proxy pós-conexão para VPN.</span><span class="sxs-lookup"><span data-stu-id="b38e8-125">A collection of configuration objects to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="b38e8-126">O proxy definido para esse perfil é aplicado quando esse perfil está ativo e conectado.</span><span class="sxs-lookup"><span data-stu-id="b38e8-126">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

</dd> <dt>

<span data-ttu-id="b38e8-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b38e8-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b38e8-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b38e8-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b38e8-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b38e8-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b38e8-130">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b38e8-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b38e8-131">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="b38e8-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="b38e8-132">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="b38e8-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b38e8-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b38e8-133">Requirements</span></span>



| <span data-ttu-id="b38e8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b38e8-134">Requirement</span></span> | <span data-ttu-id="b38e8-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b38e8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b38e8-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b38e8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b38e8-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b38e8-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b38e8-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b38e8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b38e8-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b38e8-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b38e8-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="b38e8-140">Namespace</span></span><br/>                | <span data-ttu-id="b38e8-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b38e8-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b38e8-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b38e8-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b38e8-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b38e8-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b38e8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b38e8-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b38e8-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b38e8-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b38e8-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="b38e8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b38e8-147">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="b38e8-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

