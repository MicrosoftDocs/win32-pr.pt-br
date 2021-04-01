---
title: Classe MDM_Policy_User_Config01_Printers02
description: A \_ classe Config01 Printers02 do usuário da política de MDM \_ \_ \_ representa as políticas de impressora disponíveis.
ms.assetid: 9faeaa04-92b4-43b0-be17-0f85f2eb493c
keywords:
- Classe MDM_Policy_User_Config01_Printers02
- Classe MDM_Policy_User_Config01_Printers02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Printers02
- MDM_Policy_User_Config01_Printers02.InstanceID
- MDM_Policy_User_Config01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04be571473f05d93242c77d02052cf84c335caf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644689"
---
# <a name="mdm_policy_user_config01_printers02-class"></a><span data-ttu-id="5f5ce-105">Config01 de usuário de política de MDM- \_ \_ \_ \_ classe Printers02</span><span class="sxs-lookup"><span data-stu-id="5f5ce-105">MDM\_Policy\_User\_Config01\_Printers02 class</span></span>

<span data-ttu-id="5f5ce-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5f5ce-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="5f5ce-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5f5ce-108">A \_ classe Config01 Printers02 do usuário da política de MDM \_ \_ \_ representa as políticas de impressora disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-108">The MDM\_Policy\_User\_Config01\_Printers02 class represents the available printer policies.</span></span>

<span data-ttu-id="5f5ce-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f5ce-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f5ce-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions_User;
};
```

## <a name="members"></a><span data-ttu-id="5f5ce-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5f5ce-111">Members</span></span>

<span data-ttu-id="5f5ce-112">A **classe \_ \_ \_ Config01 \_ Printers02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5f5ce-112">The **MDM\_Policy\_User\_Config01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="5f5ce-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f5ce-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f5ce-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f5ce-114">Properties</span></span>

<span data-ttu-id="5f5ce-115">A **classe \_ \_ \_ Config01 \_ Printers02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5f5ce-115">The **MDM\_Policy\_User\_Config01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f5ce-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5f5ce-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f5ce-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f5ce-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f5ce-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f5ce-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f5ce-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f5ce-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5f5ce-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5f5ce-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f5ce-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f5ce-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f5ce-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f5ce-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f5ce-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f5ce-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f5ce-124">\_Usuário PointAndPrintRestrictions</span><span class="sxs-lookup"><span data-stu-id="5f5ce-124">PointAndPrintRestrictions\_User</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions-user)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f5ce-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f5ce-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f5ce-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5f5ce-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f5ce-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f5ce-127">Requirements</span></span>



| <span data-ttu-id="5f5ce-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f5ce-128">Requirement</span></span> | <span data-ttu-id="5f5ce-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5f5ce-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5ce-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f5ce-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5f5ce-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5f5ce-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f5ce-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f5ce-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5f5ce-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5f5ce-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5f5ce-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f5ce-134">Namespace</span></span><br/>                | <span data-ttu-id="5f5ce-135">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5f5ce-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5f5ce-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5f5ce-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f5ce-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f5ce-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f5ce-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5f5ce-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f5ce-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f5ce-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

