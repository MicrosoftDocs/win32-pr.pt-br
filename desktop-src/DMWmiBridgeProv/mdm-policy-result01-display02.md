---
title: Classe MDM_Policy_Result01_Display02
description: A \_ classe Result01 Display02 de política de MDM \_ \_ representa as políticas de exibição.
ms.assetid: 9f8675d6-1fd7-4269-8059-9159622f03cb
keywords:
- Classe MDM_Policy_Result01_Display02
- Classe MDM_Policy_Result01_Display02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Display02
- MDM_Policy_Result01_Display02.InstanceID
- MDM_Policy_Result01_Display02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b8097d943e92343250802d63c4dfa2e5c77920
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455210"
---
# <a name="mdm_policy_result01_display02-class"></a><span data-ttu-id="16976-105">\_Classe MDM \_ Result01 \_ Display02</span><span class="sxs-lookup"><span data-stu-id="16976-105">MDM\_Policy\_Result01\_Display02 class</span></span>

<span data-ttu-id="16976-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="16976-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="16976-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="16976-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="16976-108">A \_ classe Result01 Display02 de política de MDM \_ \_ representa as políticas de exibição.</span><span class="sxs-lookup"><span data-stu-id="16976-108">The MDM\_Policy\_Result01\_Display02 class represents the display policies.</span></span>

<span data-ttu-id="16976-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="16976-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="16976-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16976-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Display02
{
  string InstanceID;
  string ParentID;
  string TurnOffGdiDPIScalingForApps;
  string TurnOnGdiDPIScalingForApps;
};
```

## <a name="members"></a><span data-ttu-id="16976-111">Membros</span><span class="sxs-lookup"><span data-stu-id="16976-111">Members</span></span>

<span data-ttu-id="16976-112">A **classe \_ \_ Result01 \_ Display02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="16976-112">The **MDM\_Policy\_Result01\_Display02** class has these types of members:</span></span>

-   [<span data-ttu-id="16976-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16976-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16976-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16976-114">Properties</span></span>

<span data-ttu-id="16976-115">A **classe \_ \_ Result01 \_ Display02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="16976-115">The **MDM\_Policy\_Result01\_Display02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16976-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="16976-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16976-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="16976-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16976-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16976-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16976-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="16976-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="16976-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="16976-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16976-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="16976-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16976-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16976-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16976-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="16976-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="16976-124">TurnOffGdiDPIScalingForApps</span><span class="sxs-lookup"><span data-stu-id="16976-124">TurnOffGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnoffgdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="16976-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="16976-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16976-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="16976-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="16976-127">TurnOnGdiDPIScalingForApps</span><span class="sxs-lookup"><span data-stu-id="16976-127">TurnOnGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnongdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="16976-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="16976-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16976-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="16976-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16976-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16976-130">Requirements</span></span>



| <span data-ttu-id="16976-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="16976-131">Requirement</span></span> | <span data-ttu-id="16976-132">Valor</span><span class="sxs-lookup"><span data-stu-id="16976-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16976-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16976-133">Minimum supported client</span></span><br/> | <span data-ttu-id="16976-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="16976-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="16976-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16976-135">Minimum supported server</span></span><br/> | <span data-ttu-id="16976-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="16976-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="16976-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="16976-137">Namespace</span></span><br/>                | <span data-ttu-id="16976-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="16976-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="16976-139">MOF</span><span class="sxs-lookup"><span data-stu-id="16976-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16976-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16976-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="16976-141">DLL</span><span class="sxs-lookup"><span data-stu-id="16976-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16976-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16976-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

