---
title: Classe MDM_Policy_Config01_Storage02
description: A \_ classe Config01 Storage02 de política de MDM \_ \_ configura as políticas de armazenamento.
ms.assetid: 5c58e6d4-dfc6-4467-9a86-08eb31ccf28d
keywords:
- Classe MDM_Policy_Config01_Storage02
- Classe MDM_Policy_Config01_Storage02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Storage02
- MDM_Policy_Config01_Storage02.InstanceID
- MDM_Policy_Config01_Storage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445c73158e032d888b5b1d0ec4496d2fd49c1ae1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085627"
---
# <a name="mdm_policy_config01_storage02-class"></a><span data-ttu-id="b292e-105">\_Classe MDM \_ Config01 \_ Storage02</span><span class="sxs-lookup"><span data-stu-id="b292e-105">MDM\_Policy\_Config01\_Storage02 class</span></span>

<span data-ttu-id="b292e-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="b292e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b292e-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="b292e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b292e-108">A \_ classe Config01 Storage02 de política de MDM \_ \_ configura as políticas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b292e-108">The MDM\_Policy\_Config01\_Storage02 class configures the storage policies.</span></span>

<span data-ttu-id="b292e-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b292e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b292e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b292e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Storage02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiskHealthModelUpdates;
  string EnhancedStorageDevices;
};
```

## <a name="members"></a><span data-ttu-id="b292e-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b292e-111">Members</span></span>

<span data-ttu-id="b292e-112">A **classe \_ \_ Config01 \_ Storage02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b292e-112">The **MDM\_Policy\_Config01\_Storage02** class has these types of members:</span></span>

-   [<span data-ttu-id="b292e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b292e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b292e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b292e-114">Properties</span></span>

<span data-ttu-id="b292e-115">A **classe \_ \_ Config01 \_ Storage02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b292e-115">The **MDM\_Policy\_Config01\_Storage02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b292e-116">AllowDiskHealthModelUpdates</span><span class="sxs-lookup"><span data-stu-id="b292e-116">AllowDiskHealthModelUpdates</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-allowdiskhealthmodelupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b292e-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b292e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b292e-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b292e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b292e-119">EnhancedStorageDevices</span><span class="sxs-lookup"><span data-stu-id="b292e-119">EnhancedStorageDevices</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-enhancedstoragedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b292e-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b292e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b292e-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b292e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b292e-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b292e-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b292e-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b292e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b292e-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b292e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b292e-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b292e-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b292e-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b292e-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b292e-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b292e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b292e-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b292e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b292e-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b292e-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b292e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b292e-130">Requirements</span></span>



| <span data-ttu-id="b292e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b292e-131">Requirement</span></span> | <span data-ttu-id="b292e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b292e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b292e-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b292e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b292e-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b292e-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b292e-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b292e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b292e-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b292e-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b292e-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b292e-137">Namespace</span></span><br/>                | <span data-ttu-id="b292e-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b292e-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b292e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b292e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b292e-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b292e-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b292e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b292e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b292e-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b292e-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

