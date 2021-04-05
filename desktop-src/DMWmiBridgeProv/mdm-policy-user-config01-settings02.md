---
title: Classe MDM_Policy_User_Config01_Settings02
description: A \_ classe Config01 Settings02 do usuário da política de MDM \_ \_ \_ configura calendários adicionais na barra de tarefas.
ms.assetid: 66cfdb55-17a7-4586-86b3-70ba7dcd5637
keywords:
- Classe MDM_Policy_User_Config01_Settings02
- Classe MDM_Policy_User_Config01_Settings02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Settings02
- MDM_Policy_User_Config01_Settings02.InstanceID
- MDM_Policy_User_Config01_Settings02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8bd0099d19ec4535abf6b525a7487b810b39704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085617"
---
# <a name="mdm_policy_user_config01_settings02-class"></a><span data-ttu-id="cf28e-105">Config01 de usuário de política de MDM- \_ \_ \_ \_ classe Settings02</span><span class="sxs-lookup"><span data-stu-id="cf28e-105">MDM\_Policy\_User\_Config01\_Settings02 class</span></span>

<span data-ttu-id="cf28e-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="cf28e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cf28e-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="cf28e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cf28e-108">A \_ classe Config01 Settings02 do usuário da política de MDM \_ \_ \_ configura calendários adicionais na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="cf28e-108">The MDM\_Policy\_User\_Config01\_Settings02 class configures additional calendars in the taskbar.</span></span>

<span data-ttu-id="cf28e-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cf28e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf28e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf28e-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Settings02
{
  string InstanceID;
  string ParentID;
  sint32 ConfigureTaskbarCalendar;
};
```

## <a name="members"></a><span data-ttu-id="cf28e-111">Membros</span><span class="sxs-lookup"><span data-stu-id="cf28e-111">Members</span></span>

<span data-ttu-id="cf28e-112">A **classe \_ \_ \_ Config01 \_ Settings02 do usuário da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cf28e-112">The **MDM\_Policy\_User\_Config01\_Settings02** class has these types of members:</span></span>

-   [<span data-ttu-id="cf28e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cf28e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf28e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cf28e-114">Properties</span></span>

<span data-ttu-id="cf28e-115">A **classe \_ \_ \_ Config01 \_ Settings02 do usuário da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cf28e-115">The **MDM\_Policy\_User\_Config01\_Settings02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="cf28e-116">ConfigureTaskbarCalendar</span><span class="sxs-lookup"><span data-stu-id="cf28e-116">ConfigureTaskbarCalendar</span></span>](/windows/client-management/mdm/policy-csp-settings#settings-configuretaskbarcalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf28e-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cf28e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf28e-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cf28e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cf28e-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cf28e-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf28e-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf28e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf28e-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf28e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf28e-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cf28e-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cf28e-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cf28e-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf28e-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cf28e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf28e-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cf28e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf28e-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cf28e-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf28e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf28e-127">Requirements</span></span>



| <span data-ttu-id="cf28e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf28e-128">Requirement</span></span> | <span data-ttu-id="cf28e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="cf28e-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf28e-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf28e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cf28e-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cf28e-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf28e-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf28e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cf28e-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cf28e-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cf28e-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf28e-134">Namespace</span></span><br/>                | <span data-ttu-id="cf28e-135">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="cf28e-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cf28e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="cf28e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf28e-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf28e-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf28e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cf28e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf28e-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf28e-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

