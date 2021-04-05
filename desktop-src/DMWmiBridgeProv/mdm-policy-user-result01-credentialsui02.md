---
title: Classe MDM_Policy_User_Result01_CredentialsUI02
description: A \_ classe Result01 CredentialsUI02 do usuário da política de MDM \_ \_ \_ representa as políticas de credenciais disponíveis.
ms.assetid: e1df7798-676a-4846-89e5-2c05d0259086
keywords:
- Classe MDM_Policy_User_Result01_CredentialsUI02
- Classe MDM_Policy_User_Result01_CredentialsUI02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_CredentialsUI02
- MDM_Policy_User_Result01_CredentialsUI02.InstanceID
- MDM_Policy_User_Result01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7659990ee980872059bd26b0a8b553202e6cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009413"
---
# <a name="mdm_policy_user_result01_credentialsui02-class"></a><span data-ttu-id="de121-105">Result01 de usuário de política de MDM- \_ \_ \_ \_ classe CredentialsUI02</span><span class="sxs-lookup"><span data-stu-id="de121-105">MDM\_Policy\_User\_Result01\_CredentialsUI02 class</span></span>

<span data-ttu-id="de121-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="de121-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="de121-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="de121-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="de121-108">A \_ classe Result01 CredentialsUI02 do usuário da política de MDM \_ \_ \_ representa as políticas de credenciais disponíveis.</span><span class="sxs-lookup"><span data-stu-id="de121-108">The MDM\_Policy\_User\_Result01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="de121-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="de121-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de121-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de121-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
};
```

## <a name="members"></a><span data-ttu-id="de121-111">Membros</span><span class="sxs-lookup"><span data-stu-id="de121-111">Members</span></span>

<span data-ttu-id="de121-112">A **classe \_ \_ \_ Result01 \_ CredentialsUI02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="de121-112">The **MDM\_Policy\_User\_Result01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="de121-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de121-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de121-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de121-114">Properties</span></span>

<span data-ttu-id="de121-115">A **classe \_ \_ \_ Result01 \_ CredentialsUI02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="de121-115">The **MDM\_Policy\_User\_Result01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="de121-116">DisablePasswordReveal</span><span class="sxs-lookup"><span data-stu-id="de121-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de121-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de121-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de121-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="de121-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de121-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="de121-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de121-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de121-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de121-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de121-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de121-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de121-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de121-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="de121-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de121-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de121-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de121-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de121-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de121-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de121-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de121-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de121-127">Requirements</span></span>



| <span data-ttu-id="de121-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="de121-128">Requirement</span></span> | <span data-ttu-id="de121-129">Valor</span><span class="sxs-lookup"><span data-stu-id="de121-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de121-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de121-130">Minimum supported client</span></span><br/> | <span data-ttu-id="de121-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="de121-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de121-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de121-132">Minimum supported server</span></span><br/> | <span data-ttu-id="de121-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="de121-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="de121-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="de121-134">Namespace</span></span><br/>                | <span data-ttu-id="de121-135">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="de121-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="de121-136">MOF</span><span class="sxs-lookup"><span data-stu-id="de121-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de121-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de121-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="de121-138">DLL</span><span class="sxs-lookup"><span data-stu-id="de121-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de121-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de121-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

