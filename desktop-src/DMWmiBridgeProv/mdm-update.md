---
title: Classe MDM_Update
description: A classe de atualização do MDM \_ é usada para gerenciar e controlar a distribuição de novas atualizações.
ms.assetid: 503884fd-190c-482d-b600-1a15363891f3
keywords:
- Classe MDM_Update
- Classe MDM_Update, descrita
topic_type:
- apiref
api_name:
- MDM_Update
- MDM_Update.InstanceID
- MDM_Update.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2735b5eaaef4abc468586cb7608be7969a1eab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824328"
---
# <a name="mdm_update-class"></a><span data-ttu-id="c668b-105">Classe de atualização do MDM \_</span><span class="sxs-lookup"><span data-stu-id="c668b-105">MDM\_Update class</span></span>

<span data-ttu-id="c668b-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c668b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c668b-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c668b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c668b-108">A classe de **\_ atualização do MDM** é usada para gerenciar e controlar a distribuição de novas atualizações.</span><span class="sxs-lookup"><span data-stu-id="c668b-108">The **MDM\_Update** class is used to manage and control the rollout of new updates.</span></span>

<span data-ttu-id="c668b-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c668b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c668b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c668b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update
{
  string   InstanceID;
  string   ParentID;
  datetime LastSuccessfulScanTime;
  sint32   DeferUpgrade;
};
```

## <a name="members"></a><span data-ttu-id="c668b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="c668b-111">Members</span></span>

<span data-ttu-id="c668b-112">A classe de **\_ atualização do MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c668b-112">The **MDM\_Update** class has these types of members:</span></span>

-   [<span data-ttu-id="c668b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c668b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c668b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c668b-114">Properties</span></span>

<span data-ttu-id="c668b-115">A classe de **\_ atualização do MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c668b-115">The **MDM\_Update** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c668b-116">DeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="c668b-116">DeferUpgrade</span></span>](/windows/client-management/mdm/update-csp#deferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c668b-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c668b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c668b-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c668b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c668b-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c668b-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c668b-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c668b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c668b-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c668b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c668b-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c668b-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c668b-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="c668b-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="c668b-124">Para essa classe, a cadeia de caracteres é "Update".</span><span class="sxs-lookup"><span data-stu-id="c668b-124">For this class, the string is "Update".</span></span>

</dd> <dt>

[<span data-ttu-id="c668b-125">LastSuccessfulScanTime</span><span class="sxs-lookup"><span data-stu-id="c668b-125">LastSuccessfulScanTime</span></span>](/windows/client-management/mdm/update-csp#lastsuccessfulscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c668b-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c668b-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c668b-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c668b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c668b-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c668b-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c668b-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c668b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c668b-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c668b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c668b-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c668b-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c668b-132">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="c668b-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="c668b-133">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="c668b-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c668b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c668b-134">Requirements</span></span>



| <span data-ttu-id="c668b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c668b-135">Requirement</span></span> | <span data-ttu-id="c668b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c668b-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c668b-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c668b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c668b-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c668b-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c668b-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c668b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c668b-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c668b-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="c668b-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="c668b-141">Namespace</span></span><br/>                | <span data-ttu-id="c668b-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c668b-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="c668b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c668b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c668b-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c668b-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="c668b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c668b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c668b-146"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="c668b-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

