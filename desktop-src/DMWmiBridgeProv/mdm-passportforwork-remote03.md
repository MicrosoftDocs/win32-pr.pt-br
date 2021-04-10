---
title: Classe MDM_PassportForWork_Remote03
description: A \_ classe MDM PassportForWork \_ Remote03 define as configurações de política remota do Windows Hello para empresas.
ms.assetid: 221701be-944f-42cd-847e-553d41281749
keywords:
- Classe MDM_PassportForWork_Remote03
- Classe MDM_PassportForWork_Remote03, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Remote03
- MDM_PassportForWork_Remote03.InstanceID
- MDM_PassportForWork_Remote03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae111389ad0f7c46b1f0b217bffc016e451ca9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009184"
---
# <a name="mdm_passportforwork_remote03-class"></a><span data-ttu-id="dd357-105">\_ \_ Classe REMOTE03 do MDM PassportForWork</span><span class="sxs-lookup"><span data-stu-id="dd357-105">MDM\_PassportForWork\_Remote03 class</span></span>

<span data-ttu-id="dd357-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="dd357-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dd357-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="dd357-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dd357-108">A classe **MDM \_ PassportForWork \_ Remote03** define as configurações de política remota do Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="dd357-108">The **MDM\_PassportForWork\_Remote03** class defines the Windows Hello for Business remote policy settings.</span></span>

<span data-ttu-id="dd357-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="dd357-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd357-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd357-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Remote03
{
  string  InstanceID;
  string  ParentID;
  boolean UseRemotePassport;
};
```

## <a name="members"></a><span data-ttu-id="dd357-111">Membros</span><span class="sxs-lookup"><span data-stu-id="dd357-111">Members</span></span>

<span data-ttu-id="dd357-112">A **classe \_ \_ Remote03 de MDM PassportForWork** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dd357-112">The **MDM\_PassportForWork\_Remote03** class has these types of members:</span></span>

-   [<span data-ttu-id="dd357-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dd357-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd357-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dd357-114">Properties</span></span>

<span data-ttu-id="dd357-115">A **classe \_ \_ Remote03 do MDM PassportForWork** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dd357-115">The **MDM\_PassportForWork\_Remote03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd357-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dd357-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd357-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dd357-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd357-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd357-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd357-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd357-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd357-120">Nó interior para definir políticas remotas do Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="dd357-120">Interior node for defining remote Windows Hello for Business policies.</span></span> <span data-ttu-id="dd357-121">Esse nó foi adicionado no Windows 10, versão 1511.</span><span class="sxs-lookup"><span data-stu-id="dd357-121">This node was added in Windows 10, version 1511.</span></span>

</dd> <dt>

<span data-ttu-id="dd357-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dd357-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd357-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dd357-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd357-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dd357-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd357-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd357-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd357-126">Nó para definir as configurações de política do Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="dd357-126">Node for defining the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

[<span data-ttu-id="dd357-127">UseRemotePassport</span><span class="sxs-lookup"><span data-stu-id="dd357-127">UseRemotePassport</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd357-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dd357-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd357-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="dd357-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd357-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd357-130">Requirements</span></span>



| <span data-ttu-id="dd357-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd357-131">Requirement</span></span> | <span data-ttu-id="dd357-132">Valor</span><span class="sxs-lookup"><span data-stu-id="dd357-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd357-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd357-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dd357-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="dd357-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd357-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd357-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dd357-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dd357-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dd357-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd357-137">Namespace</span></span><br/>                | <span data-ttu-id="dd357-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="dd357-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dd357-139">MOF</span><span class="sxs-lookup"><span data-stu-id="dd357-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd357-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd357-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd357-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dd357-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd357-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd357-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd357-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd357-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd357-144">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="dd357-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

