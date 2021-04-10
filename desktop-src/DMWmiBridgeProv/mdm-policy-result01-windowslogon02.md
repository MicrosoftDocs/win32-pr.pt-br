---
title: Classe MDM_Policy_Result01_WindowsLogon02
description: A \_ classe Result01 WindowsLogon02 da política de MDM \_ \_ Obtém as configurações da tela de bloqueio e da interface do usuário da rede no logon.
ms.assetid: 4c710e3d-e7d5-4e6e-ad99-b3c7d1813599
keywords:
- Classe MDM_Policy_Result01_WindowsLogon02
- Classe MDM_Policy_Result01_WindowsLogon02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsLogon02
- MDM_Policy_Result01_WindowsLogon02.InstanceID
- MDM_Policy_Result01_WindowsLogon02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8e9c0e2ebc2e82d5daef174ce9322b5b4b5ec7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085207"
---
# <a name="mdm_policy_result01_windowslogon02-class"></a><span data-ttu-id="f50d3-105">\_Classe MDM \_ Result01 \_ WindowsLogon02</span><span class="sxs-lookup"><span data-stu-id="f50d3-105">MDM\_Policy\_Result01\_WindowsLogon02 class</span></span>

<span data-ttu-id="f50d3-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="f50d3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f50d3-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="f50d3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f50d3-108">A \_ classe Result01 WindowsLogon02 da política de MDM \_ \_ Obtém as configurações da tela de bloqueio e da interface do usuário da rede no logon.</span><span class="sxs-lookup"><span data-stu-id="f50d3-108">The MDM\_Policy\_Result01\_WindowsLogon02 class gets the settings of the lock screen and network user interface at logon.</span></span>

<span data-ttu-id="f50d3-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f50d3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f50d3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f50d3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsLogon02
{
  string InstanceID;
  string ParentID;
  string DontDisplayNetworkSelectionUI;
  string DisableLockScreenAppNotifications;
  sint32 HideFastUserSwitching;
};
```

## <a name="members"></a><span data-ttu-id="f50d3-111">Membros</span><span class="sxs-lookup"><span data-stu-id="f50d3-111">Members</span></span>

<span data-ttu-id="f50d3-112">A **classe \_ \_ Result01 \_ WindowsLogon02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f50d3-112">The **MDM\_Policy\_Result01\_WindowsLogon02** class has these types of members:</span></span>

-   [<span data-ttu-id="f50d3-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f50d3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f50d3-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f50d3-114">Properties</span></span>

<span data-ttu-id="f50d3-115">A **classe \_ \_ Result01 \_ WindowsLogon02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f50d3-115">The **MDM\_Policy\_Result01\_WindowsLogon02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f50d3-116">DisableLockScreenAppNotifications</span><span class="sxs-lookup"><span data-stu-id="f50d3-116">DisableLockScreenAppNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-disablelockscreenappnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f50d3-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f50d3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f50d3-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f50d3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f50d3-119">DontDisplayNetworkSelectionUI</span><span class="sxs-lookup"><span data-stu-id="f50d3-119">DontDisplayNetworkSelectionUI</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-dontdisplaynetworkselectionui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f50d3-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f50d3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f50d3-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f50d3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f50d3-122">HideFastUserSwitching</span><span class="sxs-lookup"><span data-stu-id="f50d3-122">HideFastUserSwitching</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-hidefastuserswitching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f50d3-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f50d3-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f50d3-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f50d3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f50d3-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f50d3-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f50d3-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f50d3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f50d3-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f50d3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f50d3-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f50d3-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f50d3-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f50d3-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f50d3-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f50d3-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f50d3-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f50d3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f50d3-132">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f50d3-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f50d3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f50d3-133">Requirements</span></span>



| <span data-ttu-id="f50d3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f50d3-134">Requirement</span></span> | <span data-ttu-id="f50d3-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f50d3-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f50d3-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f50d3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f50d3-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f50d3-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f50d3-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f50d3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f50d3-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f50d3-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f50d3-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="f50d3-140">Namespace</span></span><br/>                | <span data-ttu-id="f50d3-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="f50d3-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f50d3-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f50d3-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f50d3-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f50d3-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f50d3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f50d3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f50d3-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f50d3-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

