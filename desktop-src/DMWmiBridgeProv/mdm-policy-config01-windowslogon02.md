---
title: Classe MDM_Policy_Config01_WindowsLogon02
description: A \_ classe Config01 WindowsLogon02 de política de MDM \_ \_ configura a tela de bloqueio e a interface do usuário da rede no logon.
ms.assetid: eb155cf8-628d-4325-8b39-f193733d4c87
keywords:
- Classe MDM_Policy_Config01_WindowsLogon02
- Classe MDM_Policy_Config01_WindowsLogon02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsLogon02
- MDM_Policy_Config01_WindowsLogon02.InstanceID
- MDM_Policy_Config01_WindowsLogon02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf723729f8b90974b1ecaf5a0d8ee08eba0a3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824442"
---
# <a name="mdm_policy_config01_windowslogon02-class"></a><span data-ttu-id="7b921-105">\_Classe MDM \_ Config01 \_ WindowsLogon02</span><span class="sxs-lookup"><span data-stu-id="7b921-105">MDM\_Policy\_Config01\_WindowsLogon02 class</span></span>

<span data-ttu-id="7b921-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7b921-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7b921-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7b921-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7b921-108">A \_ classe Config01 WindowsLogon02 de política de MDM \_ \_ configura a tela de bloqueio e a interface do usuário da rede no logon.</span><span class="sxs-lookup"><span data-stu-id="7b921-108">The MDM\_Policy\_Config01\_WindowsLogon02 class configures the lock screen and network user interface at logon.</span></span>

<span data-ttu-id="7b921-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7b921-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b921-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b921-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsLogon02
{
  string InstanceID;
  string ParentID;
  string DontDisplayNetworkSelectionUI;
  string DisableLockScreenAppNotifications;
  sint32 HideFastUserSwitching;
};
```

## <a name="members"></a><span data-ttu-id="7b921-111">Membros</span><span class="sxs-lookup"><span data-stu-id="7b921-111">Members</span></span>

<span data-ttu-id="7b921-112">A **classe \_ \_ Config01 \_ WindowsLogon02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7b921-112">The **MDM\_Policy\_Config01\_WindowsLogon02** class has these types of members:</span></span>

-   [<span data-ttu-id="7b921-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7b921-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b921-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7b921-114">Properties</span></span>

<span data-ttu-id="7b921-115">A **classe \_ \_ Config01 \_ WindowsLogon02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7b921-115">The **MDM\_Policy\_Config01\_WindowsLogon02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7b921-116">DisableLockScreenAppNotifications</span><span class="sxs-lookup"><span data-stu-id="7b921-116">DisableLockScreenAppNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-disablelockscreenappnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b921-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b921-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b921-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7b921-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7b921-119">DontDisplayNetworkSelectionUI</span><span class="sxs-lookup"><span data-stu-id="7b921-119">DontDisplayNetworkSelectionUI</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-dontdisplaynetworkselectionui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b921-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b921-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b921-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7b921-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7b921-122">HideFastUserSwitching</span><span class="sxs-lookup"><span data-stu-id="7b921-122">HideFastUserSwitching</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-hidefastuserswitching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b921-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7b921-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b921-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7b921-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b921-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7b921-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b921-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b921-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b921-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b921-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b921-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b921-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7b921-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7b921-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b921-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b921-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b921-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b921-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b921-132">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b921-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b921-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b921-133">Requirements</span></span>



| <span data-ttu-id="7b921-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b921-134">Requirement</span></span> | <span data-ttu-id="7b921-135">Valor</span><span class="sxs-lookup"><span data-stu-id="7b921-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b921-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b921-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7b921-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7b921-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b921-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b921-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7b921-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7b921-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7b921-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b921-140">Namespace</span></span><br/>                | <span data-ttu-id="7b921-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7b921-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7b921-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7b921-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b921-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b921-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b921-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7b921-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b921-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b921-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

