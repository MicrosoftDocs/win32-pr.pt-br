---
title: Classe MDM_Policy_Config01_RemoteAssistance02
description: A \_ classe Config01 RemoteAssistance02 de política de MDM \_ \_ configura as políticas de assistência remota.
ms.assetid: bcc6c570-66d9-4dcd-b7f2-2d03733c0bcb
keywords:
- Classe MDM_Policy_Config01_RemoteAssistance02
- Classe MDM_Policy_Config01_RemoteAssistance02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteAssistance02
- MDM_Policy_Config01_RemoteAssistance02.InstanceID
- MDM_Policy_Config01_RemoteAssistance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceadb2eb784e72e4e332cdd34df44d779c99e97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824392"
---
# <a name="mdm_policy_config01_remoteassistance02-class"></a><span data-ttu-id="481bd-105">\_Classe MDM \_ Config01 \_ RemoteAssistance02</span><span class="sxs-lookup"><span data-stu-id="481bd-105">MDM\_Policy\_Config01\_RemoteAssistance02 class</span></span>

<span data-ttu-id="481bd-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="481bd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="481bd-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="481bd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="481bd-108">A \_ classe Config01 RemoteAssistance02 de política de MDM \_ \_ configura as políticas de assistência remota.</span><span class="sxs-lookup"><span data-stu-id="481bd-108">The MDM\_Policy\_Config01\_RemoteAssistance02 class configures the remote assistance policies.</span></span>

<span data-ttu-id="481bd-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="481bd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="481bd-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="481bd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteAssistance02
{
  string InstanceID;
  string ParentID;
  string CustomizeWarningMessages;
  string SessionLogging;
  string SolicitedRemoteAssistance;
  string UnsolicitedRemoteAssistance;
};
```

## <a name="members"></a><span data-ttu-id="481bd-111">Membros</span><span class="sxs-lookup"><span data-stu-id="481bd-111">Members</span></span>

<span data-ttu-id="481bd-112">A **classe \_ \_ Config01 \_ RemoteAssistance02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="481bd-112">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these types of members:</span></span>

-   [<span data-ttu-id="481bd-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="481bd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="481bd-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="481bd-114">Properties</span></span>

<span data-ttu-id="481bd-115">A **classe \_ \_ Config01 \_ RemoteAssistance02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="481bd-115">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="481bd-116">CustomizeWarningMessages</span><span class="sxs-lookup"><span data-stu-id="481bd-116">CustomizeWarningMessages</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-customizewarningmessages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="481bd-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="481bd-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="481bd-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="481bd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="481bd-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="481bd-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="481bd-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="481bd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="481bd-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="481bd-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="481bd-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="481bd-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="481bd-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="481bd-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="481bd-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="481bd-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="481bd-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="481bd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="481bd-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="481bd-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="481bd-127">SessionLogging</span><span class="sxs-lookup"><span data-stu-id="481bd-127">SessionLogging</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-sessionlogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="481bd-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="481bd-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="481bd-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="481bd-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="481bd-130">SolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="481bd-130">SolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-solicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="481bd-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="481bd-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="481bd-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="481bd-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="481bd-133">UnsolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="481bd-133">UnsolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-unsolicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="481bd-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="481bd-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="481bd-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="481bd-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="481bd-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="481bd-136">Requirements</span></span>



| <span data-ttu-id="481bd-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="481bd-137">Requirement</span></span> | <span data-ttu-id="481bd-138">Valor</span><span class="sxs-lookup"><span data-stu-id="481bd-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="481bd-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="481bd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="481bd-140">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="481bd-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="481bd-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="481bd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="481bd-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="481bd-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="481bd-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="481bd-143">Namespace</span></span><br/>                | <span data-ttu-id="481bd-144">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="481bd-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="481bd-145">MOF</span><span class="sxs-lookup"><span data-stu-id="481bd-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="481bd-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="481bd-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="481bd-147">DLL</span><span class="sxs-lookup"><span data-stu-id="481bd-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="481bd-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="481bd-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

