---
title: Classe Win32_VirtualDesktopSession
description: Gerencia uma sessão de área de trabalho virtual.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Classe de Win32_VirtualDesktopSession Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_VirtualDesktopSession classe, descrita
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f343c1dc022dcb4759f813de956ade27e1aff213
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454724"
---
# <a name="win32_virtualdesktopsession-class"></a><span data-ttu-id="f30c1-105">\_Classe Win32 VirtualDesktopSession</span><span class="sxs-lookup"><span data-stu-id="f30c1-105">Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="f30c1-106">Gerencia uma sessão de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="f30c1-106">Manages a virtual desktop session.</span></span>

<span data-ttu-id="f30c1-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f30c1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f30c1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f30c1-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a><span data-ttu-id="f30c1-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f30c1-109">Members</span></span>

<span data-ttu-id="f30c1-110">A classe **Win32 \_ VirtualDesktopSession** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f30c1-110">The **Win32\_VirtualDesktopSession** class has these types of members:</span></span>

-   [<span data-ttu-id="f30c1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f30c1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f30c1-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f30c1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f30c1-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f30c1-113">Methods</span></span>

<span data-ttu-id="f30c1-114">A classe **Win32 \_ VirtualDesktopSession** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f30c1-114">The **Win32\_VirtualDesktopSession** class has these methods.</span></span>



| <span data-ttu-id="f30c1-115">Método</span><span class="sxs-lookup"><span data-stu-id="f30c1-115">Method</span></span>                                                         | <span data-ttu-id="f30c1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f30c1-116">Description</span></span>                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="f30c1-117">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="f30c1-117">**Disconnect**</span></span>](disconnect-win32-virtualdesktopsession.md)   | <span data-ttu-id="f30c1-118">Desconecta a sessão de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="f30c1-118">Disconnects the virtual desktop session.</span></span><br/>                        |
| [<span data-ttu-id="f30c1-119">**Verbos**</span><span class="sxs-lookup"><span data-stu-id="f30c1-119">**Logoff**</span></span>](logoff-win32-virtualdesktopsession.md)           | <span data-ttu-id="f30c1-120">Faz logoff do usuário da sessão de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="f30c1-120">Logs off the user from the virtual desktop session.</span></span><br/>             |
| [<span data-ttu-id="f30c1-121">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="f30c1-121">**SendMessage**</span></span>](sendmessage-win32-virtualdesktopsession.md) | <span data-ttu-id="f30c1-122">Envie uma mensagem para o usuário por meio da sessão de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="f30c1-122">Send a message to the user through the virtual desktop session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f30c1-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f30c1-123">Properties</span></span>

<span data-ttu-id="f30c1-124">A classe **Win32 \_ VirtualDesktopSession** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f30c1-124">The **Win32\_VirtualDesktopSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f30c1-125">**ClientMachineName**</span><span class="sxs-lookup"><span data-stu-id="f30c1-125">**ClientMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f30c1-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f30c1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f30c1-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f30c1-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f30c1-128">Obtém o nome do computador cliente que está conectado à sessão.</span><span class="sxs-lookup"><span data-stu-id="f30c1-128">Gets the name of the client machine that is connected to the session.</span></span>

</dd> <dt>

<span data-ttu-id="f30c1-129">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="f30c1-129">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f30c1-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f30c1-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f30c1-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f30c1-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f30c1-132">Obtém o nome da coleção de áreas de trabalho virtuais que hospeda a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f30c1-132">Gets the name of the virtual desktop collection that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="f30c1-133">**Connectstate**</span><span class="sxs-lookup"><span data-stu-id="f30c1-133">**ConnectState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f30c1-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f30c1-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f30c1-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f30c1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f30c1-136">Obtém o estado da conexão com a sessão.</span><span class="sxs-lookup"><span data-stu-id="f30c1-136">Gets the state of the connection to the session.</span></span>

</dd> <dt>

<span data-ttu-id="f30c1-137">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="f30c1-137">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f30c1-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f30c1-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f30c1-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f30c1-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f30c1-140">Obtém o nome de domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="f30c1-140">Gets the domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="f30c1-141">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="f30c1-141">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f30c1-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f30c1-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f30c1-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f30c1-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f30c1-144">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f30c1-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f30c1-145">Obtém a ID da sessão de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="f30c1-145">Gets the ID of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="f30c1-146">**UserName**</span><span class="sxs-lookup"><span data-stu-id="f30c1-146">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f30c1-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f30c1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f30c1-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f30c1-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f30c1-149">Obtém o nome da conta de usuário que é atribuída à sessão.</span><span class="sxs-lookup"><span data-stu-id="f30c1-149">Gets the name of the user account that is assigned to the session.</span></span>

</dd> <dt>

<span data-ttu-id="f30c1-150">**VMHostName**</span><span class="sxs-lookup"><span data-stu-id="f30c1-150">**VMHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f30c1-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f30c1-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f30c1-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f30c1-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f30c1-153">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f30c1-153">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f30c1-154">Obtém o nome do servidor host de virtualização Área de Trabalho Remota que hospeda a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f30c1-154">Gets the name of the Remote Desktop virtualization host server that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="f30c1-155">**VMName**</span><span class="sxs-lookup"><span data-stu-id="f30c1-155">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f30c1-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f30c1-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f30c1-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f30c1-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f30c1-158">Obtém o nome da máquina virtual que é atribuída à sessão.</span><span class="sxs-lookup"><span data-stu-id="f30c1-158">Gets the name of the virtual machine that is assigned to the session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f30c1-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f30c1-159">Requirements</span></span>



| <span data-ttu-id="f30c1-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="f30c1-160">Requirement</span></span> | <span data-ttu-id="f30c1-161">Valor</span><span class="sxs-lookup"><span data-stu-id="f30c1-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f30c1-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f30c1-162">Minimum supported client</span></span><br/> | <span data-ttu-id="f30c1-163">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f30c1-163">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f30c1-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f30c1-164">Minimum supported server</span></span><br/> | <span data-ttu-id="f30c1-165">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f30c1-165">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f30c1-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="f30c1-166">Namespace</span></span><br/>                | <span data-ttu-id="f30c1-167">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="f30c1-167">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f30c1-168">MOF</span><span class="sxs-lookup"><span data-stu-id="f30c1-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f30c1-169"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f30c1-169"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f30c1-170">DLL</span><span class="sxs-lookup"><span data-stu-id="f30c1-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f30c1-171"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f30c1-171"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f30c1-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="f30c1-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f30c1-173">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="f30c1-173">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

