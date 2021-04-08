---
title: Classe MDM_Policy_Config01_CredentialsUI02
description: A \_ classe Config01 CredentialsUI02 de política de MDM \_ \_ configura as políticas de provedor de credenciais disponíveis.
ms.assetid: 508b8dc8-cc89-4260-9346-30deeac606fd
keywords:
- Classe MDM_Policy_Config01_CredentialsUI02
- Classe MDM_Policy_Config01_CredentialsUI02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialsUI02
- MDM_Policy_Config01_CredentialsUI02.InstanceID
- MDM_Policy_Config01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e0fcb9b736adfabbf2b3de12d576ef76652e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009173"
---
# <a name="mdm_policy_config01_credentialsui02-class"></a><span data-ttu-id="5d62c-105">\_Classe MDM \_ Config01 \_ CredentialsUI02</span><span class="sxs-lookup"><span data-stu-id="5d62c-105">MDM\_Policy\_Config01\_CredentialsUI02 class</span></span>

<span data-ttu-id="5d62c-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="5d62c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5d62c-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="5d62c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5d62c-108">A \_ classe Config01 CredentialsUI02 de política de MDM \_ \_ configura as políticas de provedor de credenciais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5d62c-108">The MDM\_Policy\_Config01\_CredentialsUI02 class configures the available credential provider policies.</span></span>

<span data-ttu-id="5d62c-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5d62c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d62c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d62c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
  string EnumerateAdministrators;
};
```

## <a name="members"></a><span data-ttu-id="5d62c-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5d62c-111">Members</span></span>

<span data-ttu-id="5d62c-112">A **classe \_ \_ Config01 \_ CredentialsUI02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5d62c-112">The **MDM\_Policy\_Config01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="5d62c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d62c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d62c-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d62c-114">Properties</span></span>

<span data-ttu-id="5d62c-115">A **classe \_ \_ Config01 \_ CredentialsUI02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5d62c-115">The **MDM\_Policy\_Config01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5d62c-116">DisablePasswordReveal</span><span class="sxs-lookup"><span data-stu-id="5d62c-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d62c-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d62c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d62c-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5d62c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5d62c-119">EnumerateAdministrators</span><span class="sxs-lookup"><span data-stu-id="5d62c-119">EnumerateAdministrators</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-enumerateadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d62c-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d62c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d62c-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5d62c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5d62c-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5d62c-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d62c-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d62c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d62c-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d62c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d62c-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5d62c-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5d62c-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5d62c-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d62c-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d62c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d62c-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d62c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d62c-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5d62c-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d62c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d62c-130">Requirements</span></span>



| <span data-ttu-id="5d62c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d62c-131">Requirement</span></span> | <span data-ttu-id="5d62c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5d62c-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d62c-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d62c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5d62c-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5d62c-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5d62c-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d62c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5d62c-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5d62c-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5d62c-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d62c-137">Namespace</span></span><br/>                | <span data-ttu-id="5d62c-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5d62c-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5d62c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5d62c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d62c-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d62c-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d62c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5d62c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d62c-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d62c-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

