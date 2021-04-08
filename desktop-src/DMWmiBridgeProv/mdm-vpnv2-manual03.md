---
title: Classe MDM_VPNv2_Manual03
description: O MDM \_ VPNv2 \_ Manual03class é um nó opcional que contém as configurações manuais do servidor.
ms.assetid: c294c5a2-35e2-46ca-b7d8-9c63f9d3cdd6
keywords:
- Classe MDM_VPNv2_Manual03
- Classe MDM_VPNv2_Manual03, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Manual03
- MDM_VPNv2_Manual03.InstanceID
- MDM_VPNv2_Manual03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e36d9a048e3a5a523770b9a3987a346fe2283
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919012"
---
# <a name="mdm_vpnv2_manual03-class"></a><span data-ttu-id="bbeab-105">\_ \_ Classe MANUAL03 do MDM VPNv2</span><span class="sxs-lookup"><span data-stu-id="bbeab-105">MDM\_VPNv2\_Manual03 class</span></span>

<span data-ttu-id="bbeab-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="bbeab-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bbeab-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="bbeab-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bbeab-108">A classe **MDM \_ VPNv2 \_ Manual03** é um nó opcional que contém as configurações manuais do servidor.</span><span class="sxs-lookup"><span data-stu-id="bbeab-108">The **MDM\_VPNv2\_Manual03** class is an optional node containing the manual server settings.</span></span>

<span data-ttu-id="bbeab-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bbeab-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbeab-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbeab-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Manual03
{
  string InstanceID;
  string ParentID;
  string Server;
};
```

## <a name="members"></a><span data-ttu-id="bbeab-111">Membros</span><span class="sxs-lookup"><span data-stu-id="bbeab-111">Members</span></span>

<span data-ttu-id="bbeab-112">A **classe \_ \_ Manual03 de MDM VPNv2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bbeab-112">The **MDM\_VPNv2\_Manual03** class has these types of members:</span></span>

-   [<span data-ttu-id="bbeab-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bbeab-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bbeab-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bbeab-114">Properties</span></span>

<span data-ttu-id="bbeab-115">A **classe \_ \_ Manual03 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bbeab-115">The **MDM\_VPNv2\_Manual03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bbeab-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bbeab-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbeab-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bbeab-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbeab-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bbeab-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbeab-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bbeab-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bbeab-120">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="bbeab-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="bbeab-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bbeab-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbeab-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bbeab-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbeab-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bbeab-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbeab-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bbeab-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bbeab-125">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="bbeab-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="bbeab-126">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/proxy/"</span><span class="sxs-lookup"><span data-stu-id="bbeab-126">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/Proxy/"</span></span>

</dd> <dt>

[<span data-ttu-id="bbeab-127">Servidor</span><span class="sxs-lookup"><span data-stu-id="bbeab-127">Server</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-manual-server)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbeab-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bbeab-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbeab-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bbeab-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bbeab-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbeab-130">Requirements</span></span>



| <span data-ttu-id="bbeab-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbeab-131">Requirement</span></span> | <span data-ttu-id="bbeab-132">Valor</span><span class="sxs-lookup"><span data-stu-id="bbeab-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbeab-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbeab-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bbeab-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bbeab-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bbeab-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbeab-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bbeab-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bbeab-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bbeab-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="bbeab-137">Namespace</span></span><br/>                | <span data-ttu-id="bbeab-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="bbeab-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bbeab-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bbeab-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbeab-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbeab-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbeab-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bbeab-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbeab-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbeab-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbeab-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbeab-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbeab-144">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="bbeab-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

