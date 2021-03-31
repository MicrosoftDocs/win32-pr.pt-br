---
title: Classe MDM_PassportForWork_Policies02
description: A \_ classe MDM PassportForWork \_ Policies02 provisiona o Windows Hello para empresas.
ms.assetid: 362fe819-a68a-4433-8b43-201d9678a8da
keywords:
- Classe MDM_PassportForWork_Policies02
- Classe MDM_PassportForWork_Policies02, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Policies02
- MDM_PassportForWork_Policies02.InstanceID
- MDM_PassportForWork_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdf407289f93f5ecff0e57ebf7b7fa8d9844183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918255"
---
# <a name="mdm_passportforwork_policies02-class"></a><span data-ttu-id="1a45b-105">\_ \_ Classe POLICIES02 do MDM PassportForWork</span><span class="sxs-lookup"><span data-stu-id="1a45b-105">MDM\_PassportForWork\_Policies02 class</span></span>

<span data-ttu-id="1a45b-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="1a45b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1a45b-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="1a45b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1a45b-108">A classe **MDM \_ PassportForWork \_ Policies02** provisiona o Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="1a45b-108">The **MDM\_PassportForWork\_Policies02** class provisions Windows Hello for Business.</span></span>

<span data-ttu-id="1a45b-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1a45b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a45b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a45b-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UsePassportForWork;
  boolean RequireSecurityDevice;
};
```

## <a name="members"></a><span data-ttu-id="1a45b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="1a45b-111">Members</span></span>

<span data-ttu-id="1a45b-112">A **classe \_ \_ Policies02 de MDM PassportForWork** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1a45b-112">The **MDM\_PassportForWork\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="1a45b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a45b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a45b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a45b-114">Properties</span></span>

<span data-ttu-id="1a45b-115">A **classe \_ \_ Policies02 do MDM PassportForWork** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1a45b-115">The **MDM\_PassportForWork\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a45b-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1a45b-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a45b-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a45b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a45b-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a45b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a45b-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a45b-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1a45b-120">Nó raiz para as políticas do Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="1a45b-120">Root node for Windows Hello for Business policies.</span></span>

</dd> <dt>

<span data-ttu-id="1a45b-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1a45b-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a45b-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a45b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a45b-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a45b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a45b-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a45b-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1a45b-125">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="1a45b-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="1a45b-126">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/PassPortForWork/*tenantid*"</span><span class="sxs-lookup"><span data-stu-id="1a45b-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*"</span></span>

</dd> <dt>

[<span data-ttu-id="1a45b-127">RequireSecurityDevice</span><span class="sxs-lookup"><span data-stu-id="1a45b-127">RequireSecurityDevice</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-requiresecuritydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a45b-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1a45b-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1a45b-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1a45b-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1a45b-130">UsePassportForWork</span><span class="sxs-lookup"><span data-stu-id="1a45b-130">UsePassportForWork</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-usepassportforwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a45b-131">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1a45b-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1a45b-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1a45b-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a45b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a45b-133">Requirements</span></span>



| <span data-ttu-id="1a45b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a45b-134">Requirement</span></span> | <span data-ttu-id="1a45b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="1a45b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a45b-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a45b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1a45b-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1a45b-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1a45b-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a45b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1a45b-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1a45b-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1a45b-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a45b-140">Namespace</span></span><br/>                | <span data-ttu-id="1a45b-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="1a45b-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1a45b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1a45b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a45b-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a45b-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a45b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1a45b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a45b-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a45b-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a45b-146">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1a45b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a45b-147">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="1a45b-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

