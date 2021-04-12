---
title: Classe MDM_Policy_Result01_Maps02
description: A \_ classe Result01 Maps02 de política de MDM \_ \_ representa as políticas de mapa disponíveis.
ms.assetid: 09a2755c-1d2c-4c34-a5e7-d8fc07b55ad8
keywords:
- Classe MDM_Policy_Result01_Maps02
- Classe MDM_Policy_Result01_Maps02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Maps02
- MDM_Policy_Result01_Maps02.InstanceID
- MDM_Policy_Result01_Maps02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7bc3676a8c2900cba6afcbeff20839153ec3320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454997"
---
# <a name="mdm_policy_result01_maps02-class"></a><span data-ttu-id="ed65b-105">\_Classe MDM \_ Result01 \_ Maps02</span><span class="sxs-lookup"><span data-stu-id="ed65b-105">MDM\_Policy\_Result01\_Maps02 class</span></span>

<span data-ttu-id="ed65b-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="ed65b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ed65b-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="ed65b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ed65b-108">A **classe \_ \_ Result01 \_ Maps02 de política de MDM** representa as políticas de mapa disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ed65b-108">The **MDM\_Policy\_Result01\_Maps02** class represents the map policies available.</span></span>

<span data-ttu-id="ed65b-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ed65b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed65b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed65b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Maps02
{
  string InstanceID;
  string ParentID;
  sint32 AllowOfflineMapsDownloadOverMeteredConnection;
  sint32 EnableOfflineMapsAutoUpdate;
};
```

## <a name="members"></a><span data-ttu-id="ed65b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="ed65b-111">Members</span></span>

<span data-ttu-id="ed65b-112">A **classe \_ \_ Result01 \_ Maps02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ed65b-112">The **MDM\_Policy\_Result01\_Maps02** class has these types of members:</span></span>

-   [<span data-ttu-id="ed65b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ed65b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed65b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ed65b-114">Properties</span></span>

<span data-ttu-id="ed65b-115">A **classe \_ \_ Result01 \_ Maps02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ed65b-115">The **MDM\_Policy\_Result01\_Maps02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ed65b-116">AllowOfflineMapsDownloadOverMeteredConnection</span><span class="sxs-lookup"><span data-stu-id="ed65b-116">AllowOfflineMapsDownloadOverMeteredConnection</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-allowofflinemapsdownloadovermeteredconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed65b-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed65b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed65b-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ed65b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed65b-119">EnableOfflineMapsAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="ed65b-119">EnableOfflineMapsAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-enableofflinemapsautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed65b-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed65b-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed65b-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ed65b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ed65b-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ed65b-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed65b-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ed65b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed65b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ed65b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed65b-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed65b-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed65b-126">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="ed65b-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="ed65b-127">Para essa classe, a cadeia de caracteres é "Maps".</span><span class="sxs-lookup"><span data-stu-id="ed65b-127">For this class, the string is "Maps".</span></span>

</dd> <dt>

<span data-ttu-id="ed65b-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ed65b-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed65b-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ed65b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed65b-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ed65b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed65b-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed65b-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed65b-132">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="ed65b-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="ed65b-133">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="ed65b-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed65b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed65b-134">Requirements</span></span>



| <span data-ttu-id="ed65b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed65b-135">Requirement</span></span> | <span data-ttu-id="ed65b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="ed65b-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed65b-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed65b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ed65b-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ed65b-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ed65b-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed65b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ed65b-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ed65b-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="ed65b-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed65b-141">Namespace</span></span><br/>                | <span data-ttu-id="ed65b-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="ed65b-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="ed65b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="ed65b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed65b-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed65b-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="ed65b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ed65b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed65b-146"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="ed65b-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

