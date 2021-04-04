---
title: Classe MDM_Policy_Result01_RemoteShell02
description: A \_ classe MDM Policy \_ Result01 \_ RemoteShell02 representa as políticas de shell remoto.
ms.assetid: d005b2e6-e838-4bda-9ba4-bd49c092f951
keywords:
- Classe MDM_Policy_Result01_RemoteShell02
- Classe MDM_Policy_Result01_RemoteShell02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteShell02
- MDM_Policy_Result01_RemoteShell02.InstanceID
- MDM_Policy_Result01_RemoteShell02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babd602823d0cc2e98a6855c3803aea240627e37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824240"
---
# <a name="mdm_policy_result01_remoteshell02-class"></a><span data-ttu-id="0b2bb-105">\_Classe MDM \_ Result01 \_ RemoteShell02</span><span class="sxs-lookup"><span data-stu-id="0b2bb-105">MDM\_Policy\_Result01\_RemoteShell02 class</span></span>

<span data-ttu-id="0b2bb-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0b2bb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0b2bb-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0b2bb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0b2bb-108">A \_ classe MDM Policy \_ Result01 \_ RemoteShell02 representa as políticas de shell remoto.</span><span class="sxs-lookup"><span data-stu-id="0b2bb-108">The MDM\_Policy\_Result01\_RemoteShell02 class represents the remote shell policies.</span></span>

<span data-ttu-id="0b2bb-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0b2bb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b2bb-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b2bb-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteShell02
{
  string InstanceID;
  string ParentID;
  string AllowRemoteShellAccess;
  string MaxConcurrentUsers;
  string SpecifyIdleTimeout;
  string SpecifyMaxMemory;
  string SpecifyMaxProcesses;
  string SpecifyMaxRemoteShells;
  string SpecifyShellTimeout;
};
```

## <a name="members"></a><span data-ttu-id="0b2bb-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0b2bb-111">Members</span></span>

<span data-ttu-id="0b2bb-112">A **classe \_ \_ Result01 \_ RemoteShell02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b2bb-112">The **MDM\_Policy\_Result01\_RemoteShell02** class has these types of members:</span></span>

-   [<span data-ttu-id="0b2bb-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b2bb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b2bb-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b2bb-114">Properties</span></span>

<span data-ttu-id="0b2bb-115">A **classe \_ \_ Result01 \_ RemoteShell02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b2bb-115">The **MDM\_Policy\_Result01\_RemoteShell02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0b2bb-116">AllowRemoteShellAccess</span><span class="sxs-lookup"><span data-stu-id="0b2bb-116">AllowRemoteShellAccess</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-allowremoteshellaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b2bb-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b2bb-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b2bb-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b2bb-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b2bb-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b2bb-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b2bb-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b2bb-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b2bb-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b2bb-123">MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="0b2bb-123">MaxConcurrentUsers</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-maxconcurrentusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b2bb-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b2bb-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b2bb-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b2bb-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b2bb-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b2bb-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b2bb-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b2bb-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b2bb-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b2bb-130">SpecifyIdleTimeout</span><span class="sxs-lookup"><span data-stu-id="0b2bb-130">SpecifyIdleTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyidletimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b2bb-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b2bb-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b2bb-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b2bb-133">SpecifyMaxMemory</span><span class="sxs-lookup"><span data-stu-id="0b2bb-133">SpecifyMaxMemory</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxmemory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b2bb-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b2bb-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b2bb-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b2bb-136">SpecifyMaxProcesses</span><span class="sxs-lookup"><span data-stu-id="0b2bb-136">SpecifyMaxProcesses</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b2bb-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b2bb-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b2bb-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b2bb-139">SpecifyMaxRemoteShells</span><span class="sxs-lookup"><span data-stu-id="0b2bb-139">SpecifyMaxRemoteShells</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxremoteshells)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b2bb-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b2bb-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b2bb-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b2bb-142">SpecifyShellTimeout</span><span class="sxs-lookup"><span data-stu-id="0b2bb-142">SpecifyShellTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyshelltimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b2bb-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b2bb-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b2bb-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0b2bb-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b2bb-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b2bb-145">Requirements</span></span>



| <span data-ttu-id="0b2bb-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b2bb-146">Requirement</span></span> | <span data-ttu-id="0b2bb-147">Valor</span><span class="sxs-lookup"><span data-stu-id="0b2bb-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b2bb-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b2bb-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0b2bb-149">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0b2bb-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b2bb-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b2bb-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0b2bb-151">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0b2bb-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0b2bb-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b2bb-152">Namespace</span></span><br/>                | <span data-ttu-id="0b2bb-153">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0b2bb-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0b2bb-154">MOF</span><span class="sxs-lookup"><span data-stu-id="0b2bb-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b2bb-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b2bb-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b2bb-156">DLL</span><span class="sxs-lookup"><span data-stu-id="0b2bb-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b2bb-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b2bb-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

