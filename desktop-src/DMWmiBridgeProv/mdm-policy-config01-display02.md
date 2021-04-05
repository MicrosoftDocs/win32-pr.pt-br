---
title: Classe MDM_Policy_Config01_Display02
description: A \_ classe Config01 Display02 de política de MDM \_ \_ configura as políticas de exibição.
ms.assetid: 106eecc5-ede0-4d66-ba51-967a8f7bcb66
keywords:
- Classe MDM_Policy_Config01_Display02
- Classe MDM_Policy_Config01_Display02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Display02
- MDM_Policy_Config01_Display02.InstanceID
- MDM_Policy_Config01_Display02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e79861a911d03f1d9174053dc8ec7c62824fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085376"
---
# <a name="mdm_policy_config01_display02-class"></a><span data-ttu-id="c50d7-105">\_Classe MDM \_ Config01 \_ Display02</span><span class="sxs-lookup"><span data-stu-id="c50d7-105">MDM\_Policy\_Config01\_Display02 class</span></span>

<span data-ttu-id="c50d7-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c50d7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c50d7-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c50d7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c50d7-108">A \_ classe Config01 Display02 de política de MDM \_ \_ configura as políticas de exibição.</span><span class="sxs-lookup"><span data-stu-id="c50d7-108">The MDM\_Policy\_Config01\_Display02 class configures the display policies.</span></span>

<span data-ttu-id="c50d7-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c50d7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50d7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c50d7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Display02
{
  string InstanceID;
  string ParentID;
  string TurnOffGdiDPIScalingForApps;
  string TurnOnGdiDPIScalingForApps;
};
```

## <a name="members"></a><span data-ttu-id="c50d7-111">Membros</span><span class="sxs-lookup"><span data-stu-id="c50d7-111">Members</span></span>

<span data-ttu-id="c50d7-112">A **classe \_ \_ Config01 \_ Display02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c50d7-112">The **MDM\_Policy\_Config01\_Display02** class has these types of members:</span></span>

-   [<span data-ttu-id="c50d7-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c50d7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c50d7-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c50d7-114">Properties</span></span>

<span data-ttu-id="c50d7-115">A **classe \_ \_ Config01 \_ Display02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c50d7-115">The **MDM\_Policy\_Config01\_Display02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c50d7-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c50d7-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c50d7-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c50d7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c50d7-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c50d7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c50d7-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c50d7-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c50d7-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c50d7-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c50d7-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c50d7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c50d7-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c50d7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c50d7-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c50d7-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c50d7-124">TurnOffGdiDPIScalingForApps</span><span class="sxs-lookup"><span data-stu-id="c50d7-124">TurnOffGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnoffgdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c50d7-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c50d7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c50d7-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c50d7-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c50d7-127">TurnOnGdiDPIScalingForApps</span><span class="sxs-lookup"><span data-stu-id="c50d7-127">TurnOnGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnongdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c50d7-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c50d7-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c50d7-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c50d7-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c50d7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c50d7-130">Requirements</span></span>



| <span data-ttu-id="c50d7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c50d7-131">Requirement</span></span> | <span data-ttu-id="c50d7-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c50d7-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c50d7-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c50d7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c50d7-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c50d7-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c50d7-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c50d7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c50d7-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c50d7-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c50d7-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="c50d7-137">Namespace</span></span><br/>                | <span data-ttu-id="c50d7-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c50d7-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c50d7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c50d7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c50d7-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c50d7-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c50d7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c50d7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c50d7-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c50d7-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

