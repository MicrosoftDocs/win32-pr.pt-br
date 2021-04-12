---
title: Classe MDM_Policy_Config01_CredentialProviders02
description: A \_ classe Config01 CredentialProviders02 de política de MDM \_ \_ configura as políticas de provedor de credenciais disponíveis.
ms.assetid: 84a44fef-1481-4d1d-9531-f2ff6f3b36e6
keywords:
- Classe MDM_Policy_Config01_CredentialProviders02
- Classe MDM_Policy_Config01_CredentialProviders02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialProviders02
- MDM_Policy_Config01_CredentialProviders02.InstanceID
- MDM_Policy_Config01_CredentialProviders02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f77a4ec63a37c71353be43836dd307d5f5293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454916"
---
# <a name="mdm_policy_config01_credentialproviders02-class"></a><span data-ttu-id="d2776-105">\_Classe MDM \_ Config01 \_ CredentialProviders02</span><span class="sxs-lookup"><span data-stu-id="d2776-105">MDM\_Policy\_Config01\_CredentialProviders02 class</span></span>

<span data-ttu-id="d2776-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="d2776-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d2776-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="d2776-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d2776-108">A \_ classe Config01 CredentialProviders02 de política de MDM \_ \_ configura as políticas de provedor de credenciais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d2776-108">The MDM\_Policy\_Config01\_CredentialProviders02 class configures the available credential provider policies.</span></span>

<span data-ttu-id="d2776-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d2776-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2776-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2776-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialProviders02
{
  string InstanceID;
  string ParentID;
  string AllowPINLogon;
  string BlockPicturePassword;
  sint32 DisableAutomaticReDeploymentCredentials;
};
```

## <a name="members"></a><span data-ttu-id="d2776-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d2776-111">Members</span></span>

<span data-ttu-id="d2776-112">A **classe \_ \_ Config01 \_ CredentialProviders02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d2776-112">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these types of members:</span></span>

-   [<span data-ttu-id="d2776-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d2776-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2776-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d2776-114">Properties</span></span>

<span data-ttu-id="d2776-115">A **classe \_ \_ Config01 \_ CredentialProviders02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d2776-115">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d2776-116">AllowPINLogon</span><span class="sxs-lookup"><span data-stu-id="d2776-116">AllowPINLogon</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-allowpinlogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2776-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d2776-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2776-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d2776-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2776-119">BlockPicturePassword</span><span class="sxs-lookup"><span data-stu-id="d2776-119">BlockPicturePassword</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-blockpicturepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2776-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d2776-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2776-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d2776-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2776-122">DisableAutomaticReDeploymentCredentials</span><span class="sxs-lookup"><span data-stu-id="d2776-122">DisableAutomaticReDeploymentCredentials</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-disableautomaticredeploymentcredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2776-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d2776-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2776-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d2776-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2776-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d2776-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2776-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d2776-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2776-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d2776-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2776-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d2776-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2776-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d2776-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2776-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d2776-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2776-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d2776-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2776-132">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d2776-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2776-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2776-133">Requirements</span></span>



| <span data-ttu-id="d2776-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2776-134">Requirement</span></span> | <span data-ttu-id="d2776-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d2776-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2776-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2776-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d2776-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d2776-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2776-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2776-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d2776-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d2776-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d2776-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2776-140">Namespace</span></span><br/>                | <span data-ttu-id="d2776-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="d2776-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d2776-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d2776-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2776-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2776-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2776-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d2776-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2776-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2776-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

