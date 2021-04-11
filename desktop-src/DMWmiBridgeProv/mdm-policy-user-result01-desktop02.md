---
title: Classe MDM_Policy_User_Result01_Desktop02
description: A \_ classe Result01 Desktop02 do usuário da política de MDM \_ \_ \_ representa as políticas de perfil de pasta disponíveis.
ms.assetid: dab89ac4-b857-474e-8fe5-6822fe06ac91
keywords:
- Classe MDM_Policy_User_Result01_Desktop02
- Classe MDM_Policy_User_Result01_Desktop02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Desktop02
- MDM_Policy_User_Result01_Desktop02.InstanceID
- MDM_Policy_User_Result01_Desktop02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da6504176140b9e775c7b7f83e0f9835ce25b42c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009412"
---
# <a name="mdm_policy_user_result01_desktop02-class"></a><span data-ttu-id="c1cc6-105">Result01 de usuário de política de MDM- \_ \_ \_ \_ classe Desktop02</span><span class="sxs-lookup"><span data-stu-id="c1cc6-105">MDM\_Policy\_User\_Result01\_Desktop02 class</span></span>

<span data-ttu-id="c1cc6-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c1cc6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c1cc6-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c1cc6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c1cc6-108">A \_ classe Result01 Desktop02 do usuário da política de MDM \_ \_ \_ representa as políticas de perfil de pasta disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c1cc6-108">The MDM\_Policy\_User\_Result01\_Desktop02 class represents the available folder profile policies.</span></span>

<span data-ttu-id="c1cc6-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c1cc6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1cc6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1cc6-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Desktop02
{
  string InstanceID;
  string ParentID;
  string PreventUserRedirectionOfProfileFolders;
};
```

## <a name="members"></a><span data-ttu-id="c1cc6-111">Membros</span><span class="sxs-lookup"><span data-stu-id="c1cc6-111">Members</span></span>

<span data-ttu-id="c1cc6-112">A **classe \_ \_ \_ Result01 \_ Desktop02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c1cc6-112">The **MDM\_Policy\_User\_Result01\_Desktop02** class has these types of members:</span></span>

-   [<span data-ttu-id="c1cc6-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1cc6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1cc6-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1cc6-114">Properties</span></span>

<span data-ttu-id="c1cc6-115">A **classe \_ \_ \_ Result01 \_ Desktop02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c1cc6-115">The **MDM\_Policy\_User\_Result01\_Desktop02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1cc6-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c1cc6-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1cc6-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1cc6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1cc6-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1cc6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1cc6-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c1cc6-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c1cc6-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c1cc6-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1cc6-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1cc6-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1cc6-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1cc6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c1cc6-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c1cc6-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c1cc6-124">PreventUserRedirectionOfProfileFolders</span><span class="sxs-lookup"><span data-stu-id="c1cc6-124">PreventUserRedirectionOfProfileFolders</span></span>](/windows/client-management/mdm/policy-csp-desktop#desktop-preventuserredirectionofprofilefolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1cc6-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c1cc6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1cc6-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c1cc6-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1cc6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1cc6-127">Requirements</span></span>



| <span data-ttu-id="c1cc6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1cc6-128">Requirement</span></span> | <span data-ttu-id="c1cc6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="c1cc6-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cc6-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1cc6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c1cc6-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c1cc6-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1cc6-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1cc6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c1cc6-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c1cc6-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c1cc6-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1cc6-134">Namespace</span></span><br/>                | <span data-ttu-id="c1cc6-135">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c1cc6-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c1cc6-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c1cc6-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1cc6-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1cc6-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1cc6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c1cc6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1cc6-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1cc6-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

