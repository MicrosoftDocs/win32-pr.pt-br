---
title: Classe MDM_Policy_Result01_Autoplay02
description: A \_ classe MDM Policy \_ Result01 \_ Autoplay02 representa as políticas de reprodução automática disponíveis.
ms.assetid: f116015d-f10e-4d17-9c0b-7253894e6c0f
keywords:
- Classe MDM_Policy_Result01_Autoplay02
- Classe MDM_Policy_Result01_Autoplay02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Autoplay02
- MDM_Policy_Result01_Autoplay02.InstanceID
- MDM_Policy_Result01_Autoplay02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abf48754cff1513d6d373c9addb34b8ec9acc26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086372"
---
# <a name="mdm_policy_result01_autoplay02-class"></a><span data-ttu-id="b4bd7-105">\_Classe MDM \_ Result01 \_ Autoplay02</span><span class="sxs-lookup"><span data-stu-id="b4bd7-105">MDM\_Policy\_Result01\_Autoplay02 class</span></span>

<span data-ttu-id="b4bd7-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="b4bd7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b4bd7-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="b4bd7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b4bd7-108">A \_ classe MDM Policy \_ Result01 \_ Autoplay02 representa as políticas de reprodução automática disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b4bd7-108">The MDM\_Policy\_Result01\_Autoplay02 class represents the available autoplay policies.</span></span>

<span data-ttu-id="b4bd7-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b4bd7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4bd7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4bd7-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Autoplay02
{
  string InstanceID;
  string ParentID;
  string DisallowAutoplayForNonVolumeDevices;
  string SetDefaultAutoRunBehavior;
  string TurnOffAutoPlay;
};
```

## <a name="members"></a><span data-ttu-id="b4bd7-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b4bd7-111">Members</span></span>

<span data-ttu-id="b4bd7-112">A **classe \_ \_ Result01 \_ Autoplay02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b4bd7-112">The **MDM\_Policy\_Result01\_Autoplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="b4bd7-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b4bd7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4bd7-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b4bd7-114">Properties</span></span>

<span data-ttu-id="b4bd7-115">A **classe \_ \_ Result01 \_ Autoplay02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b4bd7-115">The **MDM\_Policy\_Result01\_Autoplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b4bd7-116">DisallowAutoplayForNonVolumeDevices</span><span class="sxs-lookup"><span data-stu-id="b4bd7-116">DisallowAutoplayForNonVolumeDevices</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-disallowautoplayfornonvolumedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4bd7-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b4bd7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4bd7-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b4bd7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b4bd7-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b4bd7-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4bd7-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b4bd7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4bd7-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b4bd7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4bd7-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b4bd7-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b4bd7-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b4bd7-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4bd7-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b4bd7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4bd7-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b4bd7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4bd7-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b4bd7-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b4bd7-127">SetDefaultAutoRunBehavior</span><span class="sxs-lookup"><span data-stu-id="b4bd7-127">SetDefaultAutoRunBehavior</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-setdefaultautorunbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4bd7-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b4bd7-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4bd7-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b4bd7-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b4bd7-130">TurnOffAutoPlay</span><span class="sxs-lookup"><span data-stu-id="b4bd7-130">TurnOffAutoPlay</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-turnoffautoplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4bd7-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b4bd7-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4bd7-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b4bd7-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4bd7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4bd7-133">Requirements</span></span>



| <span data-ttu-id="b4bd7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4bd7-134">Requirement</span></span> | <span data-ttu-id="b4bd7-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b4bd7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4bd7-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4bd7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b4bd7-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b4bd7-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b4bd7-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4bd7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b4bd7-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b4bd7-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b4bd7-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4bd7-140">Namespace</span></span><br/>                | <span data-ttu-id="b4bd7-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b4bd7-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b4bd7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b4bd7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4bd7-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4bd7-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4bd7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b4bd7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4bd7-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4bd7-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

