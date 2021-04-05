---
title: Classe Win32_SessionDirectoryVMMPlugin
description: Representa um plug-in do VMM (Virtual Machine Manager) registrado com um agente de sessão.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionDirectoryVMMPlugin Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionDirectoryVMMPlugin classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5fc6b899eaa264357527eb107e11ad5a40ad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918130"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="c4eac-105">\_Classe Win32 SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="c4eac-105">Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="c4eac-106">Representa um plug-in do VMM (Virtual Machine Manager) registrado com um agente de sessão.</span><span class="sxs-lookup"><span data-stu-id="c4eac-106">Represents a virtual machine manager (VMM) plug-in registered with a session broker.</span></span>

<span data-ttu-id="c4eac-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c4eac-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4eac-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4eac-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="c4eac-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c4eac-109">Members</span></span>

<span data-ttu-id="c4eac-110">A classe **Win32 \_ SessionDirectoryVMMPlugin** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c4eac-110">The **Win32\_SessionDirectoryVMMPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="c4eac-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c4eac-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="c4eac-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c4eac-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c4eac-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c4eac-113">Methods</span></span>

<span data-ttu-id="c4eac-114">A classe **Win32 \_ SessionDirectoryVMMPlugin** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c4eac-114">The **Win32\_SessionDirectoryVMMPlugin** class has these methods.</span></span>



| <span data-ttu-id="c4eac-115">Método</span><span class="sxs-lookup"><span data-stu-id="c4eac-115">Method</span></span>                                                                             | <span data-ttu-id="c4eac-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4eac-116">Description</span></span>                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="c4eac-117">**GetCurrentVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="c4eac-117">**GetCurrentVMMPlugin**</span></span>](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="c4eac-118">Obtém o plug-in de prioridade mais alta que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c4eac-118">Gets the highest priority plug-in that is enabled.</span></span><br/> |
| [<span data-ttu-id="c4eac-119">**RegisterVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="c4eac-119">**RegisterVMMPlugin**</span></span>](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | <span data-ttu-id="c4eac-120">Registra um novo plug-in do VMM.</span><span class="sxs-lookup"><span data-stu-id="c4eac-120">Registers a new VMM plug-in.</span></span><br/>                       |
| [<span data-ttu-id="c4eac-121">**Sethabilitado**</span><span class="sxs-lookup"><span data-stu-id="c4eac-121">**SetEnabled**</span></span>](setenabled-win32-sessiondirectoryvmmplugin.md)                   | <span data-ttu-id="c4eac-122">Habilita ou desabilita o plug-in.</span><span class="sxs-lookup"><span data-stu-id="c4eac-122">Enables or disables the plug-in.</span></span><br/>                   |
| [<span data-ttu-id="c4eac-123">**SetName**</span><span class="sxs-lookup"><span data-stu-id="c4eac-123">**SetName**</span></span>](setname-win32-sessiondirectoryvmmplugin.md)                         | <span data-ttu-id="c4eac-124">Define o nome do plug-in.</span><span class="sxs-lookup"><span data-stu-id="c4eac-124">Sets the name of the plug-in.</span></span><br/>                      |
| [<span data-ttu-id="c4eac-125">**Setanteriority**</span><span class="sxs-lookup"><span data-stu-id="c4eac-125">**SetPriority**</span></span>](setpriority-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="c4eac-126">Define a prioridade do plug-in.</span><span class="sxs-lookup"><span data-stu-id="c4eac-126">Sets the priority of the plug-in.</span></span><br/>                  |
| [<span data-ttu-id="c4eac-127">**Setfornecedor**</span><span class="sxs-lookup"><span data-stu-id="c4eac-127">**SetProvider**</span></span>](setprovider-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="c4eac-128">Define o nome do provedor do plug-in.</span><span class="sxs-lookup"><span data-stu-id="c4eac-128">Sets the provider name of the plug-in.</span></span><br/>             |
| [<span data-ttu-id="c4eac-129">**SetServiceLocation**</span><span class="sxs-lookup"><span data-stu-id="c4eac-129">**SetServiceLocation**</span></span>](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | <span data-ttu-id="c4eac-130">Define o local do serviço do plug-in.</span><span class="sxs-lookup"><span data-stu-id="c4eac-130">Sets the service location of the plug-in.</span></span><br/>          |
| [<span data-ttu-id="c4eac-131">**UnregisterVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="c4eac-131">**UnregisterVMMPlugin**</span></span>](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="c4eac-132">Cancela o registro do plug-in.</span><span class="sxs-lookup"><span data-stu-id="c4eac-132">Unregisters the plug-in.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="c4eac-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c4eac-133">Properties</span></span>

<span data-ttu-id="c4eac-134">A classe **Win32 \_ SessionDirectoryVMMPlugin** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c4eac-134">The **Win32\_SessionDirectoryVMMPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4eac-135">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="c4eac-135">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eac-136">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c4eac-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4eac-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4eac-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4eac-138">Indica se o plug-in está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c4eac-138">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="c4eac-139">**True** se o plug-in estiver habilitado ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c4eac-139">**True** if the plug-in is enabled or **false** otherwise.</span></span> <span data-ttu-id="c4eac-140">O plug-in está desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="c4eac-140">The plug-in is disabled by default.</span></span>

</dd> <dt>

<span data-ttu-id="c4eac-141">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="c4eac-141">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eac-142">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c4eac-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4eac-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4eac-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4eac-144">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c4eac-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c4eac-145">A prioridade do plug-in.</span><span class="sxs-lookup"><span data-stu-id="c4eac-145">The priority of the plug-in.</span></span> <span data-ttu-id="c4eac-146">Quanto maior o valor, maior a prioridade do plug-in.</span><span class="sxs-lookup"><span data-stu-id="c4eac-146">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="c4eac-147">A prioridade é zero por padrão.</span><span class="sxs-lookup"><span data-stu-id="c4eac-147">The priority is zero by default.</span></span>

</dd> <dt>

<span data-ttu-id="c4eac-148">**sClassID**</span><span class="sxs-lookup"><span data-stu-id="c4eac-148">**sClassID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eac-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c4eac-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4eac-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4eac-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4eac-151">O identificador de classe do plug-in.</span><span class="sxs-lookup"><span data-stu-id="c4eac-151">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="c4eac-152">**sName**</span><span class="sxs-lookup"><span data-stu-id="c4eac-152">**sName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eac-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c4eac-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4eac-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4eac-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4eac-155">O nome do plug-in.</span><span class="sxs-lookup"><span data-stu-id="c4eac-155">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="c4eac-156">**sProvider**</span><span class="sxs-lookup"><span data-stu-id="c4eac-156">**sProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eac-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c4eac-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4eac-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4eac-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4eac-159">O nome do provedor de plug-in.</span><span class="sxs-lookup"><span data-stu-id="c4eac-159">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="c4eac-160">**sServiceLocation**</span><span class="sxs-lookup"><span data-stu-id="c4eac-160">**sServiceLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eac-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c4eac-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4eac-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c4eac-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4eac-163">O local do serviço que o plug-in deve contatar.</span><span class="sxs-lookup"><span data-stu-id="c4eac-163">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4eac-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4eac-164">Requirements</span></span>



| <span data-ttu-id="c4eac-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4eac-165">Requirement</span></span> | <span data-ttu-id="c4eac-166">Valor</span><span class="sxs-lookup"><span data-stu-id="c4eac-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4eac-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4eac-167">Minimum supported client</span></span><br/> | <span data-ttu-id="c4eac-168">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c4eac-168">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c4eac-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4eac-169">Minimum supported server</span></span><br/> | <span data-ttu-id="c4eac-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4eac-170">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="c4eac-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4eac-171">Namespace</span></span><br/>                | <span data-ttu-id="c4eac-172">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="c4eac-172">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="c4eac-173">MOF</span><span class="sxs-lookup"><span data-stu-id="c4eac-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4eac-174"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4eac-174"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4eac-175">DLL</span><span class="sxs-lookup"><span data-stu-id="c4eac-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4eac-176"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4eac-176"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

