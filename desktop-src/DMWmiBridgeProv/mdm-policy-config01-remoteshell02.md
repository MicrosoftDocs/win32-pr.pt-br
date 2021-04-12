---
title: Classe MDM_Policy_Config01_RemoteShell02
description: A \_ classe Config01 RemoteShell02 de política de MDM \_ \_ configura as políticas de shell remoto.
ms.assetid: 7026fadb-ec6a-4696-a24c-1b1e071b94b0
keywords:
- Classe MDM_Policy_Config01_RemoteShell02
- Classe MDM_Policy_Config01_RemoteShell02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteShell02
- MDM_Policy_Config01_RemoteShell02.InstanceID
- MDM_Policy_Config01_RemoteShell02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c318b0c6f23e92d90091495fdc25993d6958ca56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455219"
---
# <a name="mdm_policy_config01_remoteshell02-class"></a><span data-ttu-id="0e389-105">\_Classe MDM \_ Config01 \_ RemoteShell02</span><span class="sxs-lookup"><span data-stu-id="0e389-105">MDM\_Policy\_Config01\_RemoteShell02 class</span></span>

<span data-ttu-id="0e389-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0e389-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0e389-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0e389-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0e389-108">A \_ classe Config01 RemoteShell02 de política de MDM \_ \_ configura as políticas de shell remoto.</span><span class="sxs-lookup"><span data-stu-id="0e389-108">The MDM\_Policy\_Config01\_RemoteShell02 class configures the remote shell policies.</span></span>

<span data-ttu-id="0e389-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0e389-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e389-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e389-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteShell02
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

## <a name="members"></a><span data-ttu-id="0e389-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0e389-111">Members</span></span>

<span data-ttu-id="0e389-112">A **classe \_ \_ Config01 \_ RemoteShell02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0e389-112">The **MDM\_Policy\_Config01\_RemoteShell02** class has these types of members:</span></span>

-   [<span data-ttu-id="0e389-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0e389-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e389-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0e389-114">Properties</span></span>

<span data-ttu-id="0e389-115">A **classe \_ \_ Config01 \_ RemoteShell02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0e389-115">The **MDM\_Policy\_Config01\_RemoteShell02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0e389-116">AllowRemoteShellAccess</span><span class="sxs-lookup"><span data-stu-id="0e389-116">AllowRemoteShellAccess</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-allowremoteshellaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e389-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0e389-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e389-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0e389-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0e389-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0e389-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e389-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0e389-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e389-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0e389-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e389-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0e389-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0e389-123">MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="0e389-123">MaxConcurrentUsers</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-maxconcurrentusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e389-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0e389-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e389-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0e389-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0e389-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0e389-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e389-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0e389-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e389-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0e389-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e389-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0e389-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0e389-130">SpecifyIdleTimeout</span><span class="sxs-lookup"><span data-stu-id="0e389-130">SpecifyIdleTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyidletimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e389-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0e389-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e389-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0e389-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0e389-133">SpecifyMaxMemory</span><span class="sxs-lookup"><span data-stu-id="0e389-133">SpecifyMaxMemory</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxmemory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e389-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0e389-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e389-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0e389-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0e389-136">SpecifyMaxProcesses</span><span class="sxs-lookup"><span data-stu-id="0e389-136">SpecifyMaxProcesses</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e389-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0e389-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e389-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0e389-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0e389-139">SpecifyMaxRemoteShells</span><span class="sxs-lookup"><span data-stu-id="0e389-139">SpecifyMaxRemoteShells</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxremoteshells)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e389-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0e389-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e389-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0e389-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0e389-142">SpecifyShellTimeout</span><span class="sxs-lookup"><span data-stu-id="0e389-142">SpecifyShellTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyshelltimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e389-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0e389-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e389-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0e389-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e389-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e389-145">Requirements</span></span>



| <span data-ttu-id="0e389-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e389-146">Requirement</span></span> | <span data-ttu-id="0e389-147">Valor</span><span class="sxs-lookup"><span data-stu-id="0e389-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e389-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e389-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0e389-149">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0e389-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0e389-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e389-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0e389-151">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0e389-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0e389-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e389-152">Namespace</span></span><br/>                | <span data-ttu-id="0e389-153">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0e389-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0e389-154">MOF</span><span class="sxs-lookup"><span data-stu-id="0e389-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e389-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e389-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e389-156">DLL</span><span class="sxs-lookup"><span data-stu-id="0e389-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e389-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e389-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

