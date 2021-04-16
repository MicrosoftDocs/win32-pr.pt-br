---
title: Classe MDM_VPNv2_DeviceCompliance02
description: Reservado para uso futuro. | Classe MDM_VPNv2_DeviceCompliance02
ms.assetid: f84f4812-3083-46c4-a60c-919ec92c844f
keywords:
- Classe MDM_VPNv2_DeviceCompliance02
- Classe MDM_VPNv2_DeviceCompliance02, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_DeviceCompliance02
- MDM_VPNv2_DeviceCompliance02.InstanceID
- MDM_VPNv2_DeviceCompliance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a454a5cce3a40066c7cf14a60bdeeb81dcabab9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105750546"
---
# <a name="mdm_vpnv2_devicecompliance02-class"></a><span data-ttu-id="685da-106">\_ \_ Classe DEVICECOMPLIANCE02 do MDM VPNv2</span><span class="sxs-lookup"><span data-stu-id="685da-106">MDM\_VPNv2\_DeviceCompliance02 class</span></span>

<span data-ttu-id="685da-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="685da-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="685da-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="685da-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="685da-109">Reservado para uso futuro</span><span class="sxs-lookup"><span data-stu-id="685da-109">Reserved for Future Use</span></span>

<span data-ttu-id="685da-110">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="685da-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="685da-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="685da-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DeviceCompliance02
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
};
```

## <a name="members"></a><span data-ttu-id="685da-112">Membros</span><span class="sxs-lookup"><span data-stu-id="685da-112">Members</span></span>

<span data-ttu-id="685da-113">A **classe \_ \_ DeviceCompliance02 de MDM VPNv2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="685da-113">The **MDM\_VPNv2\_DeviceCompliance02** class has these types of members:</span></span>

-   [<span data-ttu-id="685da-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="685da-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="685da-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="685da-115">Properties</span></span>

<span data-ttu-id="685da-116">A **classe \_ \_ DeviceCompliance02 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="685da-116">The **MDM\_VPNv2\_DeviceCompliance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="685da-117">Enabled</span><span class="sxs-lookup"><span data-stu-id="685da-117">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="685da-118">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="685da-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="685da-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="685da-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="685da-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="685da-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="685da-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="685da-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="685da-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="685da-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="685da-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="685da-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="685da-124">Adicionado no Windows 10, versão 1607.</span><span class="sxs-lookup"><span data-stu-id="685da-124">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="685da-125">Nós em DeviceCompliance podem ser usados para habilitar o acesso condicional baseado em AAD para VPN.</span><span class="sxs-lookup"><span data-stu-id="685da-125">Nodes under DeviceCompliance can be used to enable AAD-based Conditional Access for VPN.</span></span>

</dd> <dt>

<span data-ttu-id="685da-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="685da-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="685da-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="685da-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="685da-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="685da-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="685da-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="685da-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="685da-130">Adicionado no Windows 10, versão 1607.</span><span class="sxs-lookup"><span data-stu-id="685da-130">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="685da-131">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="685da-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="685da-132">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="685da-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="685da-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="685da-133">Requirements</span></span>



| <span data-ttu-id="685da-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="685da-134">Requirement</span></span> | <span data-ttu-id="685da-135">Valor</span><span class="sxs-lookup"><span data-stu-id="685da-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="685da-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="685da-136">Minimum supported client</span></span><br/> | <span data-ttu-id="685da-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="685da-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="685da-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="685da-138">Minimum supported server</span></span><br/> | <span data-ttu-id="685da-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="685da-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="685da-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="685da-140">Namespace</span></span><br/>                | <span data-ttu-id="685da-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="685da-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="685da-142">MOF</span><span class="sxs-lookup"><span data-stu-id="685da-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="685da-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="685da-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="685da-144">DLL</span><span class="sxs-lookup"><span data-stu-id="685da-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="685da-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="685da-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="685da-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="685da-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685da-147">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="685da-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

