---
title: Classe Win32_SessionBrokerTarget
description: Define a consulta para um destino de agente de sessão.
ms.assetid: 35de25da-cb89-4836-be14-9544b1264248
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionBrokerTarget Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionBrokerTarget classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTarget
- Win32_SessionBrokerTarget.PluginName
- Win32_SessionBrokerTarget.TargetName
- Win32_SessionBrokerTarget.FarmName
- Win32_SessionBrokerTarget.Guid
- Win32_SessionBrokerTarget.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ceca0df64eeb9cd285737fee7c6ca6fa3a2e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824773"
---
# <a name="win32_sessionbrokertarget-class"></a><span data-ttu-id="4a00e-105">\_Classe Win32 SessionBrokerTarget</span><span class="sxs-lookup"><span data-stu-id="4a00e-105">Win32\_SessionBrokerTarget class</span></span>

<span data-ttu-id="4a00e-106">Define a consulta para um destino de agente de sessão.</span><span class="sxs-lookup"><span data-stu-id="4a00e-106">Defines the query for a session broker target.</span></span>

<span data-ttu-id="4a00e-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4a00e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a00e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a00e-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERTARGET_Prov"), AMENDMENT]
class Win32_SessionBrokerTarget
{
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="4a00e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4a00e-109">Members</span></span>

<span data-ttu-id="4a00e-110">A classe **Win32 \_ SessionBrokerTarget** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4a00e-110">The **Win32\_SessionBrokerTarget** class has these types of members:</span></span>

-   [<span data-ttu-id="4a00e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4a00e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a00e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4a00e-112">Properties</span></span>

<span data-ttu-id="4a00e-113">A classe **Win32 \_ SessionBrokerTarget** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4a00e-113">The **Win32\_SessionBrokerTarget** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4a00e-114">**Ambiente**</span><span class="sxs-lookup"><span data-stu-id="4a00e-114">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00e-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4a00e-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a00e-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4a00e-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a00e-117">O nome do ambiente.</span><span class="sxs-lookup"><span data-stu-id="4a00e-117">The environment name.</span></span> <span data-ttu-id="4a00e-118">No caso de um destino de máquina virtual (VM), esse pode ser o nome do host da VM.</span><span class="sxs-lookup"><span data-stu-id="4a00e-118">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

</dd> <dt>

<span data-ttu-id="4a00e-119">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="4a00e-119">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00e-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4a00e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a00e-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4a00e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a00e-122">O nome do farm ao qual o destino pertence.</span><span class="sxs-lookup"><span data-stu-id="4a00e-122">The name of the farm the target belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="4a00e-123">**Volume**</span><span class="sxs-lookup"><span data-stu-id="4a00e-123">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00e-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4a00e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a00e-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4a00e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a00e-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4a00e-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4a00e-127">O GUID (se houver) do destino.</span><span class="sxs-lookup"><span data-stu-id="4a00e-127">The GUID (if any) of the target.</span></span>

</dd> <dt>

<span data-ttu-id="4a00e-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="4a00e-128">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00e-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4a00e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a00e-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4a00e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a00e-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4a00e-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4a00e-132">O nome do plug-in.</span><span class="sxs-lookup"><span data-stu-id="4a00e-132">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="4a00e-133">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="4a00e-133">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a00e-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4a00e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a00e-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4a00e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a00e-136">O nome do destino.</span><span class="sxs-lookup"><span data-stu-id="4a00e-136">The name of the target.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4a00e-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4a00e-137">Examples</span></span>

<span data-ttu-id="4a00e-138">A cadeia de caracteres de consulta a seguir demonstra como a \_ classe SessionBrokerTarget do Win32 é usada em uma consulta.</span><span class="sxs-lookup"><span data-stu-id="4a00e-138">The following query string demonstrates how the Win32\_SessionBrokerTarget class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerTarget WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="4a00e-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a00e-139">Requirements</span></span>



| <span data-ttu-id="4a00e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a00e-140">Requirement</span></span> | <span data-ttu-id="4a00e-141">Valor</span><span class="sxs-lookup"><span data-stu-id="4a00e-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a00e-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a00e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4a00e-143">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4a00e-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4a00e-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a00e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4a00e-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4a00e-145">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="4a00e-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a00e-146">Namespace</span></span><br/>                | <span data-ttu-id="4a00e-147">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="4a00e-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="4a00e-148">MOF</span><span class="sxs-lookup"><span data-stu-id="4a00e-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a00e-149"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a00e-149"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a00e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="4a00e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a00e-151"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a00e-151"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

