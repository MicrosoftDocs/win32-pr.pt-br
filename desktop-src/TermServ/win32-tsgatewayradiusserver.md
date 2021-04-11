---
title: Classe Win32_TSGatewayRADIUSServer
description: Descreve um servidor serviço RADIUS (RADIUS), que tem um conjunto de Serviços de Área de Trabalho Remota políticas de autorização de conexão (RD \ 160; CAPs).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayRADIUSServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayRADIUSServer classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455036"
---
# <a name="win32_tsgatewayradiusserver-class"></a><span data-ttu-id="b92bd-105">\_Classe Win32 TSGatewayRADIUSServer</span><span class="sxs-lookup"><span data-stu-id="b92bd-105">Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="b92bd-106">Descreve um servidor serviço RADIUS (RADIUS), que tem um conjunto de Serviços de Área de Trabalho Remota RD CAPs (políticas de autorização de conexão).</span><span class="sxs-lookup"><span data-stu-id="b92bd-106">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

<span data-ttu-id="b92bd-107">O RADIUS é um protocolo padrão da indústria que é usado para transmitir informações de autenticação, autorização e configuração entre um computador servidor e um servidor de autenticação, chamado de servidor RADIUS, com um banco de dados que armazena informações do usuário.</span><span class="sxs-lookup"><span data-stu-id="b92bd-107">RADIUS is an industry-standard protocol that is used to transmit authentication, authorization, and configuration information between a server computer and an authenticating server, called a RADIUS server, with a database that stores user information.</span></span> <span data-ttu-id="b92bd-108">Para obter mais informações, consulte [protocolo RADIUS](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="b92bd-108">For more information, see [RADIUS Protocol](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span></span>

## <a name="syntax"></a><span data-ttu-id="b92bd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b92bd-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a><span data-ttu-id="b92bd-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b92bd-110">Members</span></span>

<span data-ttu-id="b92bd-111">A classe **Win32 \_ TSGatewayRADIUSServer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b92bd-111">The **Win32\_TSGatewayRADIUSServer** class has these types of members:</span></span>

-   [<span data-ttu-id="b92bd-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b92bd-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b92bd-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b92bd-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b92bd-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b92bd-114">Methods</span></span>

<span data-ttu-id="b92bd-115">A classe **Win32 \_ TSGatewayRADIUSServer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b92bd-115">The **Win32\_TSGatewayRADIUSServer** class has these methods.</span></span>



| <span data-ttu-id="b92bd-116">Método</span><span class="sxs-lookup"><span data-stu-id="b92bd-116">Method</span></span>                                                                 | <span data-ttu-id="b92bd-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b92bd-117">Description</span></span>                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="b92bd-118">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="b92bd-118">**Add**</span></span>](win32-tsgatewayradiusserver-add.md)                         | <span data-ttu-id="b92bd-119">Adiciona um novo servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b92bd-119">Adds a new RADIUS server.</span></span><br/>                                         |
| [<span data-ttu-id="b92bd-120">**MoveDown**</span><span class="sxs-lookup"><span data-stu-id="b92bd-120">**MoveDown**</span></span>](movedown-win32-tsgatewayradiusserver.md)               | <span data-ttu-id="b92bd-121">Move esse servidor RADIUS uma posição para baixo na ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="b92bd-121">Moves this RADIUS server one position down in the priority order.</span></span><br/> |
| [<span data-ttu-id="b92bd-122">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="b92bd-122">**MoveUp**</span></span>](moveup-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="b92bd-123">Move este servidor RADIUS uma posição para cima na ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="b92bd-123">Moves this RADIUS server one position up in the priority order.</span></span><br/>   |
| [<span data-ttu-id="b92bd-124">**Remover**</span><span class="sxs-lookup"><span data-stu-id="b92bd-124">**Remove**</span></span>](win32-tsgatewayradiusserver-remove.md)                   | <span data-ttu-id="b92bd-125">Remove o servidor RADIUS atual.</span><span class="sxs-lookup"><span data-stu-id="b92bd-125">Removes the current RADIUS server.</span></span><br/>                                |
| [<span data-ttu-id="b92bd-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="b92bd-126">**SetName**</span></span>](setname-win32-tsgatewayradiusserver.md)                 | <span data-ttu-id="b92bd-127">Define a propriedade **Name** para este servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b92bd-127">Sets the **Name** property for this RADIUS server.</span></span><br/>                |
| [<span data-ttu-id="b92bd-128">**SetSharedSecret**</span><span class="sxs-lookup"><span data-stu-id="b92bd-128">**SetSharedSecret**</span></span>](setsharedsecret-win32-tsgatewayradiusserver.md) | <span data-ttu-id="b92bd-129">Define a propriedade **SharedSecret** para esse servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b92bd-129">Sets the **SharedSecret** property for this RADIUS server.</span></span><br/>        |
| [<span data-ttu-id="b92bd-130">**Cumulativo**</span><span class="sxs-lookup"><span data-stu-id="b92bd-130">**Update**</span></span>](update-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="b92bd-131">Atualiza o servidor RADIUS atual.</span><span class="sxs-lookup"><span data-stu-id="b92bd-131">Updates the current RADIUS server.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="b92bd-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b92bd-132">Properties</span></span>

<span data-ttu-id="b92bd-133">A classe **Win32 \_ TSGatewayRADIUSServer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b92bd-133">The **Win32\_TSGatewayRADIUSServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b92bd-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b92bd-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b92bd-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b92bd-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b92bd-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b92bd-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b92bd-137">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b92bd-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b92bd-138">Nome do servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b92bd-138">Name of the RADIUS server.</span></span> <span data-ttu-id="b92bd-139">Essa propriedade pode ser alterada com o método [**SetName**](setname-win32-tsgatewayradiusserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b92bd-139">This property can be changed with the [**SetName**](setname-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b92bd-140">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="b92bd-140">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b92bd-141">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b92bd-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b92bd-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b92bd-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b92bd-143">Prioridade do servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b92bd-143">Priority of the RADIUS server.</span></span> <span data-ttu-id="b92bd-144">O servidor de gateway de área de trabalho remota procura RD CAPs em servidores RADIUS com base na prioridade.</span><span class="sxs-lookup"><span data-stu-id="b92bd-144">The RD Gateway server looks for RD CAPs on RADIUS servers based on the priority.</span></span> <span data-ttu-id="b92bd-145">Essa propriedade pode ser alterada com os métodos [**moveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)e [**Remove**](win32-tsgatewayradiusserver-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="b92bd-145">This property can be changed with the [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md), and [**Remove**](win32-tsgatewayradiusserver-remove.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="b92bd-146">**SharedSecret**</span><span class="sxs-lookup"><span data-stu-id="b92bd-146">**SharedSecret**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b92bd-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b92bd-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b92bd-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b92bd-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b92bd-149">Segredo compartilhado para o servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b92bd-149">Shared secret for the RADIUS server.</span></span> <span data-ttu-id="b92bd-150">Essa propriedade pode ser alterada com o método [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b92bd-150">This property can be changed with the [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b92bd-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="b92bd-151">Remarks</span></span>

<span data-ttu-id="b92bd-152">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="b92bd-152">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="b92bd-153">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b92bd-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b92bd-154">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b92bd-154">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b92bd-155">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="b92bd-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b92bd-156">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b92bd-156">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b92bd-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b92bd-157">Requirements</span></span>



| <span data-ttu-id="b92bd-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="b92bd-158">Requirement</span></span> | <span data-ttu-id="b92bd-159">Valor</span><span class="sxs-lookup"><span data-stu-id="b92bd-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b92bd-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b92bd-160">Minimum supported client</span></span><br/> | <span data-ttu-id="b92bd-161">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b92bd-161">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b92bd-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b92bd-162">Minimum supported server</span></span><br/> | <span data-ttu-id="b92bd-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b92bd-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b92bd-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="b92bd-164">Namespace</span></span><br/>                | <span data-ttu-id="b92bd-165">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="b92bd-165">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b92bd-166">MOF</span><span class="sxs-lookup"><span data-stu-id="b92bd-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b92bd-167"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b92bd-167"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b92bd-168">DLL</span><span class="sxs-lookup"><span data-stu-id="b92bd-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b92bd-169"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b92bd-169"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b92bd-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="b92bd-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b92bd-171">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="b92bd-171">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="b92bd-172">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="b92bd-172">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="b92bd-173">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="b92bd-173">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="b92bd-174">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="b92bd-174">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="b92bd-175">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="b92bd-175">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="b92bd-176">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="b92bd-176">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

