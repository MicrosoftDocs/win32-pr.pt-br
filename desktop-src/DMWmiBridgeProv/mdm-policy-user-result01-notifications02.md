---
title: Classe MDM_Policy_User_Result01_Notifications02
description: A \_ classe Result01 Notifications02 do usuário da política de MDM \_ \_ \_ representa as políticas de notificação disponíveis.
ms.assetid: a2da74f3-2585-4c8c-abab-751ba4c708a1
keywords:
- Classe MDM_Policy_User_Result01_Notifications02
- Classe MDM_Policy_User_Result01_Notifications02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Notifications02
- MDM_Policy_User_Result01_Notifications02.InstanceID
- MDM_Policy_User_Result01_Notifications02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c917e42ef568783b1c804ce17d52474a86359e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008908"
---
# <a name="mdm_policy_user_result01_notifications02-class"></a><span data-ttu-id="37391-105">Result01 de usuário de política de MDM- \_ \_ \_ \_ classe Notifications02</span><span class="sxs-lookup"><span data-stu-id="37391-105">MDM\_Policy\_User\_Result01\_Notifications02 class</span></span>

<span data-ttu-id="37391-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="37391-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="37391-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="37391-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="37391-108">A **classe \_ \_ \_ Result01 \_ Notifications02 do usuário da política de MDM** representa as políticas de notificação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="37391-108">The **MDM\_Policy\_User\_Result01\_Notifications02** class represents the notification policies available.</span></span>

<span data-ttu-id="37391-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="37391-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37391-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37391-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Notifications02
{
  string InstanceID;
  string ParentID;
  sint32 DisallowNotificationMirroring;
};
```

## <a name="members"></a><span data-ttu-id="37391-111">Membros</span><span class="sxs-lookup"><span data-stu-id="37391-111">Members</span></span>

<span data-ttu-id="37391-112">A **classe \_ \_ \_ Result01 \_ Notifications02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="37391-112">The **MDM\_Policy\_User\_Result01\_Notifications02** class has these types of members:</span></span>

-   [<span data-ttu-id="37391-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="37391-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37391-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="37391-114">Properties</span></span>

<span data-ttu-id="37391-115">A **classe \_ \_ \_ Result01 \_ Notifications02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="37391-115">The **MDM\_Policy\_User\_Result01\_Notifications02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="37391-116">DisallowNotificationMirroring</span><span class="sxs-lookup"><span data-stu-id="37391-116">DisallowNotificationMirroring</span></span>](/windows/client-management/mdm/policy-csp-notifications#notifications-disallownotificationmirroring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="37391-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="37391-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="37391-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="37391-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37391-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="37391-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37391-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="37391-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37391-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="37391-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37391-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37391-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="37391-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="37391-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="37391-124">Para essa classe, a cadeia de caracteres é "notificações".</span><span class="sxs-lookup"><span data-stu-id="37391-124">For this class, the string is "Notifications".</span></span>

</dd> <dt>

<span data-ttu-id="37391-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="37391-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37391-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="37391-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37391-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="37391-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37391-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37391-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="37391-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="37391-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="37391-130">Para essa classe, a cadeia de caracteres é "./User/Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="37391-130">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37391-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37391-131">Requirements</span></span>



| <span data-ttu-id="37391-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="37391-132">Requirement</span></span> | <span data-ttu-id="37391-133">Valor</span><span class="sxs-lookup"><span data-stu-id="37391-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37391-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37391-134">Minimum supported client</span></span><br/> | <span data-ttu-id="37391-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="37391-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="37391-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37391-136">Minimum supported server</span></span><br/> | <span data-ttu-id="37391-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="37391-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="37391-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="37391-138">Namespace</span></span><br/>                | <span data-ttu-id="37391-139">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="37391-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="37391-140">MOF</span><span class="sxs-lookup"><span data-stu-id="37391-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37391-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37391-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="37391-142">DLL</span><span class="sxs-lookup"><span data-stu-id="37391-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37391-143"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="37391-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

