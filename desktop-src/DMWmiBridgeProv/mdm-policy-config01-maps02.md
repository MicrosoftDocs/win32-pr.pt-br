---
title: Classe MDM_Policy_Config01_Maps02
description: A \_ classe Config01 Maps02 de política de MDM \_ \_ representa as políticas de mapa disponíveis.
ms.assetid: d2965f1f-a858-4b43-9c46-17ba718291b1
keywords:
- Classe MDM_Policy_Config01_Maps02
- Classe MDM_Policy_Config01_Maps02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Maps02
- MDM_Policy_Config01_Maps02.InstanceID
- MDM_Policy_Config01_Maps02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090c8d077b3df4446054d29a8100a32923932736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085532"
---
# <a name="mdm_policy_config01_maps02-class"></a><span data-ttu-id="88d85-105">\_Classe MDM \_ Config01 \_ Maps02</span><span class="sxs-lookup"><span data-stu-id="88d85-105">MDM\_Policy\_Config01\_Maps02 class</span></span>

<span data-ttu-id="88d85-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="88d85-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="88d85-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="88d85-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="88d85-108">A **classe \_ \_ Config01 \_ Maps02 de política de MDM** representa as políticas de mapa disponíveis.</span><span class="sxs-lookup"><span data-stu-id="88d85-108">The **MDM\_Policy\_Config01\_Maps02** class represents the map policies available.</span></span>

<span data-ttu-id="88d85-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="88d85-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="88d85-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88d85-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Maps02
{
  string InstanceID;
  string ParentID;
  sint32 AllowOfflineMapsDownloadOverMeteredConnection;
  sint32 EnableOfflineMapsAutoUpdate;
};
```

## <a name="members"></a><span data-ttu-id="88d85-111">Membros</span><span class="sxs-lookup"><span data-stu-id="88d85-111">Members</span></span>

<span data-ttu-id="88d85-112">A **classe \_ \_ Config01 \_ Maps02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="88d85-112">The **MDM\_Policy\_Config01\_Maps02** class has these types of members:</span></span>

-   [<span data-ttu-id="88d85-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="88d85-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88d85-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="88d85-114">Properties</span></span>

<span data-ttu-id="88d85-115">A **classe \_ \_ Config01 \_ Maps02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="88d85-115">The **MDM\_Policy\_Config01\_Maps02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="88d85-116">AllowOfflineMapsDownloadOverMeteredConnection</span><span class="sxs-lookup"><span data-stu-id="88d85-116">AllowOfflineMapsDownloadOverMeteredConnection</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-allowofflinemapsdownloadovermeteredconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="88d85-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="88d85-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="88d85-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="88d85-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="88d85-119">EnableOfflineMapsAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="88d85-119">EnableOfflineMapsAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-enableofflinemapsautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="88d85-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="88d85-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="88d85-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="88d85-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="88d85-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="88d85-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88d85-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="88d85-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88d85-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88d85-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88d85-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="88d85-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="88d85-126">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="88d85-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="88d85-127">Para essa classe, a cadeia de caracteres é "Maps".</span><span class="sxs-lookup"><span data-stu-id="88d85-127">For this class, the string is "Maps".</span></span>

</dd> <dt>

<span data-ttu-id="88d85-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="88d85-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88d85-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="88d85-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88d85-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88d85-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88d85-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="88d85-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="88d85-132">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="88d85-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="88d85-133">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="88d85-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88d85-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88d85-134">Requirements</span></span>



| <span data-ttu-id="88d85-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="88d85-135">Requirement</span></span> | <span data-ttu-id="88d85-136">Valor</span><span class="sxs-lookup"><span data-stu-id="88d85-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88d85-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88d85-137">Minimum supported client</span></span><br/> | <span data-ttu-id="88d85-138">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="88d85-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="88d85-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88d85-139">Minimum supported server</span></span><br/> | <span data-ttu-id="88d85-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="88d85-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="88d85-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="88d85-141">Namespace</span></span><br/>                | <span data-ttu-id="88d85-142">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="88d85-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="88d85-143">MOF</span><span class="sxs-lookup"><span data-stu-id="88d85-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88d85-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88d85-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="88d85-145">DLL</span><span class="sxs-lookup"><span data-stu-id="88d85-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88d85-146"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="88d85-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

