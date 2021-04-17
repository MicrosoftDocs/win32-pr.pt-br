---
title: Classe Win32_RDMSVirtualDesktop
description: Representa uma área de trabalho virtual.
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSVirtualDesktop Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSVirtualDesktop classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787574"
---
# <a name="win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="11003-105">\_Classe Win32 RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="11003-105">Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="11003-106">Representa uma área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-106">Represents a virtual desktop.</span></span>

<span data-ttu-id="11003-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="11003-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11003-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11003-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a><span data-ttu-id="11003-109">Membros</span><span class="sxs-lookup"><span data-stu-id="11003-109">Members</span></span>

<span data-ttu-id="11003-110">A classe **Win32 \_ RDMSVirtualDesktop** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="11003-110">The **Win32\_RDMSVirtualDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="11003-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="11003-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="11003-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11003-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="11003-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="11003-113">Methods</span></span>

<span data-ttu-id="11003-114">A classe **Win32 \_ RDMSVirtualDesktop** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="11003-114">The **Win32\_RDMSVirtualDesktop** class has these methods.</span></span>



| <span data-ttu-id="11003-115">Método</span><span class="sxs-lookup"><span data-stu-id="11003-115">Method</span></span>                                                                                              | <span data-ttu-id="11003-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="11003-116">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11003-117">**GetUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="11003-117">**GetUserAssignment**</span></span>](getuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="11003-118">Recupera o nome de usuário e o domínio que é atribuído à área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-118">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span><br/> |
| [<span data-ttu-id="11003-119">**GetVirtualDesktopAssignedToUser**</span><span class="sxs-lookup"><span data-stu-id="11003-119">**GetVirtualDesktopAssignedToUser**</span></span>](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | <span data-ttu-id="11003-120">Recupera a área de trabalho virtual que é atribuída ao usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="11003-120">Retrieves the virtual desktop that is assigned to the specified user.</span></span><br/>                       |
| [<span data-ttu-id="11003-121">**GetVirtualDesktopDetails**</span><span class="sxs-lookup"><span data-stu-id="11003-121">**GetVirtualDesktopDetails**</span></span>](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | <span data-ttu-id="11003-122">Recupera as informações adicionais sobre a área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-122">Retrieves the additional information about the virtual desktop.</span></span><br/>                             |
| [<span data-ttu-id="11003-123">**GetVirtualDesktopState**</span><span class="sxs-lookup"><span data-stu-id="11003-123">**GetVirtualDesktopState**</span></span>](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="11003-124">Recupera o estado da área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-124">Retrieves the state of the virtual desktop.</span></span><br/>                                                 |
| [<span data-ttu-id="11003-125">**RemoveUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="11003-125">**RemoveUserAssignment**</span></span>](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | <span data-ttu-id="11003-126">Remove a atribuição de usuário da área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-126">Removes the user assignment from the virtual desktop.</span></span><br/>                                       |
| [<span data-ttu-id="11003-127">**SetUserAssignment**</span><span class="sxs-lookup"><span data-stu-id="11003-127">**SetUserAssignment**</span></span>](setuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="11003-128">Atribui uma área de trabalho virtual a um usuário.</span><span class="sxs-lookup"><span data-stu-id="11003-128">Assigns a virtual desktop to a user.</span></span><br/>                                                        |
| [<span data-ttu-id="11003-129">**SetVirtualDesktopState**</span><span class="sxs-lookup"><span data-stu-id="11003-129">**SetVirtualDesktopState**</span></span>](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="11003-130">Atualiza o estado da área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-130">Updates the state of the virtual desktop.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="11003-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="11003-131">Properties</span></span>

<span data-ttu-id="11003-132">A classe **Win32 \_ RDMSVirtualDesktop** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="11003-132">The **Win32\_RDMSVirtualDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11003-133">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="11003-133">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11003-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11003-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11003-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11003-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11003-136">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11003-136">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11003-137">Obtém o alias para a coleção de áreas de trabalho virtuais que gerencia a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-137">Gets the alias to the virtual desktop collection that manages the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="11003-138">**HostName**</span><span class="sxs-lookup"><span data-stu-id="11003-138">**HostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11003-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11003-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11003-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11003-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11003-141">Obtém o nome do computador que hospeda a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-141">Gets the name of the machine that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="11003-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="11003-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11003-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11003-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11003-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11003-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11003-145">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11003-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11003-146">Obtém o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-146">Gets the name of the of virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="11003-147">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="11003-147">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11003-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11003-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11003-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11003-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11003-150">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11003-150">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11003-151">Obtém o estado da sessão de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-151">Gets the state of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="11003-152">**SessionUserName**</span><span class="sxs-lookup"><span data-stu-id="11003-152">**SessionUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11003-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11003-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11003-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11003-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11003-155">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11003-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11003-156">Obtém o nome de usuário que está conectado à sessão de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-156">Gets the username of the user that is logged in to the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="11003-157">**Status**</span><span class="sxs-lookup"><span data-stu-id="11003-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11003-158">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11003-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11003-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11003-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11003-160">Obtém o status da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-160">Gets the status of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="11003-161">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="11003-161">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11003-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11003-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11003-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11003-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11003-164">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11003-164">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11003-165">Obtém o nome de domínio do usuário atribuído à área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-165">Gets the domain name of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="11003-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="11003-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11003-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="11003-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11003-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11003-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11003-169">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11003-169">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11003-170">Obtém o nome do usuário atribuído à área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-170">Gets the username of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="11003-171">**VMState**</span><span class="sxs-lookup"><span data-stu-id="11003-171">**VMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11003-172">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11003-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11003-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="11003-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11003-174">Obtém o estado da área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="11003-174">Gets the state of the virtual desktop.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11003-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11003-175">Requirements</span></span>



| <span data-ttu-id="11003-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="11003-176">Requirement</span></span> | <span data-ttu-id="11003-177">Valor</span><span class="sxs-lookup"><span data-stu-id="11003-177">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="11003-178">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11003-178">Minimum supported client</span></span><br/> | <span data-ttu-id="11003-179">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="11003-179">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="11003-180">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11003-180">Minimum supported server</span></span><br/> | <span data-ttu-id="11003-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11003-181">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="11003-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="11003-182">Namespace</span></span><br/>                | <span data-ttu-id="11003-183">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="11003-183">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="11003-184">MOF</span><span class="sxs-lookup"><span data-stu-id="11003-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11003-185"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11003-185"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="11003-186">DLL</span><span class="sxs-lookup"><span data-stu-id="11003-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11003-187"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11003-187"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="11003-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="11003-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11003-189">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="11003-189">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

