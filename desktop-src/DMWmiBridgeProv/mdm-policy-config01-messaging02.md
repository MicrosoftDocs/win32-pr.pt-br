---
title: Classe MDM_Policy_Config01_Messaging02
description: A \_ classe MDM \_ Config01 \_ Messaging02 permite o backup e a restauração de mensagens de texto em qualquer lugar. Essa política permite que uma organização Desabilite esses recursos para evitar que informações sejam armazenadas em servidores fora de seu controle.
ms.assetid: 179ece8a-d3f4-449c-8392-ca8a35e44a31
keywords:
- Classe MDM_Policy_Config01_Messaging02
- Classe MDM_Policy_Config01_Messaging02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Messaging02
- MDM_Policy_Config01_Messaging02.InstanceID
- MDM_Policy_Config01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137d9c36a822cd93d6cfd0c7cd83197204fb8f97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499360"
---
# <a name="mdm_policy_config01_messaging02-class"></a><span data-ttu-id="ad5e9-106">\_Classe MDM \_ Config01 \_ Messaging02</span><span class="sxs-lookup"><span data-stu-id="ad5e9-106">MDM\_Policy\_Config01\_Messaging02 class</span></span>

<span data-ttu-id="ad5e9-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="ad5e9-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ad5e9-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="ad5e9-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ad5e9-109">A \_ classe MDM \_ Config01 \_ Messaging02 permite o backup e a restauração de mensagens de texto em qualquer lugar.</span><span class="sxs-lookup"><span data-stu-id="ad5e9-109">The MDM\_Policy\_Config01\_Messaging02 class enables text message back up and restore and Messaging Everywhere.</span></span> <span data-ttu-id="ad5e9-110">Essa política permite que uma organização Desabilite esses recursos para evitar que informações sejam armazenadas em servidores fora de seu controle.</span><span class="sxs-lookup"><span data-stu-id="ad5e9-110">This policy allows an organization to disable these features to avoid information being stored on servers outside of their control.</span></span>

<span data-ttu-id="ad5e9-111">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ad5e9-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad5e9-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad5e9-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a><span data-ttu-id="ad5e9-113">Membros</span><span class="sxs-lookup"><span data-stu-id="ad5e9-113">Members</span></span>

<span data-ttu-id="ad5e9-114">A **classe \_ \_ Config01 \_ Messaging02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ad5e9-114">The **MDM\_Policy\_Config01\_Messaging02** class has these types of members:</span></span>

-   [<span data-ttu-id="ad5e9-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ad5e9-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad5e9-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ad5e9-116">Properties</span></span>

<span data-ttu-id="ad5e9-117">A **classe \_ \_ Config01 \_ Messaging02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ad5e9-117">The **MDM\_Policy\_Config01\_Messaging02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ad5e9-118">AllowMessageSync</span><span class="sxs-lookup"><span data-stu-id="ad5e9-118">AllowMessageSync</span></span>](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad5e9-119">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad5e9-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad5e9-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ad5e9-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ad5e9-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ad5e9-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad5e9-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ad5e9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad5e9-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ad5e9-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad5e9-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad5e9-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ad5e9-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ad5e9-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad5e9-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ad5e9-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad5e9-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ad5e9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad5e9-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad5e9-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad5e9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad5e9-129">Requirements</span></span>



| <span data-ttu-id="ad5e9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad5e9-130">Requirement</span></span> | <span data-ttu-id="ad5e9-131">Valor</span><span class="sxs-lookup"><span data-stu-id="ad5e9-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad5e9-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad5e9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ad5e9-133">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ad5e9-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad5e9-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad5e9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ad5e9-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ad5e9-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ad5e9-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad5e9-136">Namespace</span></span><br/>                | <span data-ttu-id="ad5e9-137">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="ad5e9-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ad5e9-138">MOF</span><span class="sxs-lookup"><span data-stu-id="ad5e9-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad5e9-139"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad5e9-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad5e9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ad5e9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad5e9-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad5e9-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

