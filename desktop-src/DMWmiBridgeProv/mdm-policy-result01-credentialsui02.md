---
title: Classe MDM_Policy_Result01_CredentialsUI02
description: A \_ classe MDM Policy \_ Result01 \_ CredentialsUI02 representa as políticas de credenciais disponíveis.
ms.assetid: d50a4cc5-e87f-44a5-9345-744126615d04
keywords:
- Classe MDM_Policy_Result01_CredentialsUI02
- Classe MDM_Policy_Result01_CredentialsUI02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_CredentialsUI02
- MDM_Policy_Result01_CredentialsUI02.InstanceID
- MDM_Policy_Result01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e444e36f2602fa30ca51601e6cd08e7fa8e30c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454813"
---
# <a name="mdm_policy_result01_credentialsui02-class"></a><span data-ttu-id="7d785-105">\_Classe MDM \_ Result01 \_ CredentialsUI02</span><span class="sxs-lookup"><span data-stu-id="7d785-105">MDM\_Policy\_Result01\_CredentialsUI02 class</span></span>

<span data-ttu-id="7d785-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7d785-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7d785-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7d785-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7d785-108">A \_ classe MDM Policy \_ Result01 \_ CredentialsUI02 representa as políticas de credenciais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7d785-108">The MDM\_Policy\_Result01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="7d785-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7d785-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d785-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d785-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
  string EnumerateAdministrators;
};
```

## <a name="members"></a><span data-ttu-id="7d785-111">Membros</span><span class="sxs-lookup"><span data-stu-id="7d785-111">Members</span></span>

<span data-ttu-id="7d785-112">A **classe \_ \_ Result01 \_ CredentialsUI02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7d785-112">The **MDM\_Policy\_Result01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="7d785-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7d785-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d785-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7d785-114">Properties</span></span>

<span data-ttu-id="7d785-115">A **classe \_ \_ Result01 \_ CredentialsUI02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7d785-115">The **MDM\_Policy\_Result01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7d785-116">DisablePasswordReveal</span><span class="sxs-lookup"><span data-stu-id="7d785-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d785-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7d785-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d785-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7d785-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d785-119">EnumerateAdministrators</span><span class="sxs-lookup"><span data-stu-id="7d785-119">EnumerateAdministrators</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-enumerateadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d785-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7d785-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d785-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7d785-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d785-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7d785-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d785-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7d785-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d785-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d785-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d785-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7d785-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d785-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7d785-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d785-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7d785-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d785-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d785-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d785-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7d785-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d785-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d785-130">Requirements</span></span>



| <span data-ttu-id="7d785-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d785-131">Requirement</span></span> | <span data-ttu-id="7d785-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7d785-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d785-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d785-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7d785-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7d785-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d785-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d785-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7d785-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7d785-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7d785-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d785-137">Namespace</span></span><br/>                | <span data-ttu-id="7d785-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7d785-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7d785-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7d785-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d785-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d785-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d785-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7d785-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d785-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d785-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

