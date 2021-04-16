---
title: Classe MDM_Policy_User_Config01_AttachmentManager02
description: A \_ classe Config01 AttachmentManager02 do usuário da política de MDM \_ \_ \_ representa as políticas do Gerenciador de anexos disponíveis.
ms.assetid: b20ec516-cdc9-4aeb-802d-97cd8423eceb
keywords:
- Classe MDM_Policy_User_Config01_AttachmentManager02
- Classe MDM_Policy_User_Config01_AttachmentManager02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_AttachmentManager02
- MDM_Policy_User_Config01_AttachmentManager02.InstanceID
- MDM_Policy_User_Config01_AttachmentManager02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d127fc3770f6ba605bd8e1efdd82314231ab27f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499592"
---
# <a name="mdm_policy_user_config01_attachmentmanager02-class"></a><span data-ttu-id="6f6bc-105">Config01 de usuário de política de MDM- \_ \_ \_ \_ classe AttachmentManager02</span><span class="sxs-lookup"><span data-stu-id="6f6bc-105">MDM\_Policy\_User\_Config01\_AttachmentManager02 class</span></span>

<span data-ttu-id="6f6bc-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="6f6bc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6f6bc-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="6f6bc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6f6bc-108">A \_ classe Config01 AttachmentManager02 do usuário da política de MDM \_ \_ \_ representa as políticas do Gerenciador de anexos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6f6bc-108">The MDM\_Policy\_User\_Config01\_AttachmentManager02 class represents the available attachment manager policies.</span></span>

<span data-ttu-id="6f6bc-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6f6bc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f6bc-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f6bc-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_AttachmentManager02
{
  string InstanceID;
  string ParentID;
  string DoNotPreserveZoneInformation;
  string HideZoneInfoMechanism;
  string NotifyAntivirusPrograms;
};
```

## <a name="members"></a><span data-ttu-id="6f6bc-111">Membros</span><span class="sxs-lookup"><span data-stu-id="6f6bc-111">Members</span></span>

<span data-ttu-id="6f6bc-112">A **classe \_ \_ \_ Config01 \_ AttachmentManager02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6f6bc-112">The **MDM\_Policy\_User\_Config01\_AttachmentManager02** class has these types of members:</span></span>

-   [<span data-ttu-id="6f6bc-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f6bc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f6bc-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f6bc-114">Properties</span></span>

<span data-ttu-id="6f6bc-115">A **classe \_ \_ \_ Config01 \_ AttachmentManager02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6f6bc-115">The **MDM\_Policy\_User\_Config01\_AttachmentManager02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6f6bc-116">DoNotPreserveZoneInformation</span><span class="sxs-lookup"><span data-stu-id="6f6bc-116">DoNotPreserveZoneInformation</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-donotpreservezoneinformation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f6bc-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f6bc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f6bc-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6f6bc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6f6bc-119">HideZoneInfoMechanism</span><span class="sxs-lookup"><span data-stu-id="6f6bc-119">HideZoneInfoMechanism</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-hidezoneinfomechanism)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f6bc-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f6bc-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f6bc-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6f6bc-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f6bc-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6f6bc-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f6bc-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f6bc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f6bc-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f6bc-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f6bc-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6f6bc-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6f6bc-126">NotifyAntivirusPrograms</span><span class="sxs-lookup"><span data-stu-id="6f6bc-126">NotifyAntivirusPrograms</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-notifyantivirusprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f6bc-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f6bc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f6bc-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6f6bc-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f6bc-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6f6bc-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f6bc-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6f6bc-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f6bc-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f6bc-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f6bc-132">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6f6bc-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f6bc-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f6bc-133">Requirements</span></span>



| <span data-ttu-id="6f6bc-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f6bc-134">Requirement</span></span> | <span data-ttu-id="6f6bc-135">Valor</span><span class="sxs-lookup"><span data-stu-id="6f6bc-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f6bc-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f6bc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6f6bc-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6f6bc-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f6bc-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f6bc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6f6bc-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6f6bc-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6f6bc-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f6bc-140">Namespace</span></span><br/>                | <span data-ttu-id="6f6bc-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="6f6bc-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6f6bc-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6f6bc-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f6bc-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f6bc-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f6bc-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6f6bc-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f6bc-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f6bc-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

