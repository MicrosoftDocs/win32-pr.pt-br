---
title: Classe Win32_TSGatewayLoadBalancer
description: Descreve um conjunto de servidores de balanceamento de carga de gateway de Área de Trabalho Remota (gateway de área de trabalho remota). Eles são usados para balancear a carga de conexões de gateway de área de trabalho remota em vários servidores.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayLoadBalancer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayLoadBalancer classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4956ed4dc9536ff6f7e3263071a2a477cb0f515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644587"
---
# <a name="win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="f9c55-106">\_Classe Win32 TSGatewayLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9c55-106">Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="f9c55-107">Descreve um conjunto de servidores de balanceamento de carga de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="f9c55-107">Describes a set of Remote Desktop Gateway (RD Gateway) load-balancing servers.</span></span> <span data-ttu-id="f9c55-108">Eles são usados para balancear a carga de conexões de gateway de área de trabalho remota em vários servidores.</span><span class="sxs-lookup"><span data-stu-id="f9c55-108">These are used to load balance RD Gateway connections across multiple servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c55-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9c55-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a><span data-ttu-id="f9c55-110">Membros</span><span class="sxs-lookup"><span data-stu-id="f9c55-110">Members</span></span>

<span data-ttu-id="f9c55-111">A classe **Win32 \_ TSGatewayLoadBalancer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f9c55-111">The **Win32\_TSGatewayLoadBalancer** class has these types of members:</span></span>

-   [<span data-ttu-id="f9c55-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f9c55-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f9c55-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f9c55-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f9c55-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="f9c55-114">Methods</span></span>

<span data-ttu-id="f9c55-115">A classe **Win32 \_ TSGatewayLoadBalancer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f9c55-115">The **Win32\_TSGatewayLoadBalancer** class has these methods.</span></span>



| <span data-ttu-id="f9c55-116">Método</span><span class="sxs-lookup"><span data-stu-id="f9c55-116">Method</span></span>                                                                             | <span data-ttu-id="f9c55-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9c55-117">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9c55-118">**Addservers**</span><span class="sxs-lookup"><span data-stu-id="f9c55-118">**AddServers**</span></span>](addservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="f9c55-119">Adiciona servidores à propriedade **servidores** .</span><span class="sxs-lookup"><span data-stu-id="f9c55-119">Adds servers to the **Servers** property.</span></span><br/>                                                             |
| [<span data-ttu-id="f9c55-120">**DeleteAllServers**</span><span class="sxs-lookup"><span data-stu-id="f9c55-120">**DeleteAllServers**</span></span>](deleteallservers-win32-tsgatewayloadbalancer.md)           | <span data-ttu-id="f9c55-121">Exclui todos os servidores de balanceamento de carga do gateway de área de trabalho remota que participam do farm de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="f9c55-121">Deletes all RD Gateway load-balancing servers participating in the load-balancing farm.</span></span><br/>               |
| [<span data-ttu-id="f9c55-122">**DeleteServers**</span><span class="sxs-lookup"><span data-stu-id="f9c55-122">**DeleteServers**</span></span>](deleteservers-win32-tsgatewayloadbalancer.md)                 | <span data-ttu-id="f9c55-123">Exclui servidores da propriedade **servidores** .</span><span class="sxs-lookup"><span data-stu-id="f9c55-123">Deletes servers from the **Servers** property.</span></span><br/>                                                        |
| [<span data-ttu-id="f9c55-124">**IsLoadBalancingServer**</span><span class="sxs-lookup"><span data-stu-id="f9c55-124">**IsLoadBalancingServer**</span></span>](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | <span data-ttu-id="f9c55-125">Determina se o servidor pode executar o balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="f9c55-125">Determines whether the server can perform load balancing.</span></span><br/>                                             |
| [<span data-ttu-id="f9c55-126">**Setservers**</span><span class="sxs-lookup"><span data-stu-id="f9c55-126">**SetServers**</span></span>](setservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="f9c55-127">Define a propriedade **Servers** com a lista separada por ponto e vírgula dos servidores de balanceamento de carga do gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="f9c55-127">Sets the **Servers** property with the semicolon-separated list of RD Gateway load-balancing servers.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f9c55-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f9c55-128">Properties</span></span>

<span data-ttu-id="f9c55-129">A classe **Win32 \_ TSGatewayLoadBalancer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f9c55-129">The **Win32\_TSGatewayLoadBalancer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9c55-130">**Servidores**</span><span class="sxs-lookup"><span data-stu-id="f9c55-130">**Servers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9c55-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f9c55-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9c55-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f9c55-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9c55-133">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f9c55-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f9c55-134">Lista separada por ponto e vírgula dos servidores de balanceamento de carga do gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="f9c55-134">Semicolon-separated list of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="f9c55-135">Essa propriedade pode ser alterada com os métodos [**Setservers**](setservers-win32-tsgatewayloadbalancer.md), [**addservers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)e [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) .</span><span class="sxs-lookup"><span data-stu-id="f9c55-135">This property can be changed with the [**SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md), and [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9c55-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9c55-136">Remarks</span></span>

<span data-ttu-id="f9c55-137">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="f9c55-137">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="f9c55-138">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f9c55-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f9c55-139">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f9c55-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f9c55-140">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f9c55-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f9c55-141">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f9c55-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c55-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9c55-142">Requirements</span></span>



| <span data-ttu-id="f9c55-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9c55-143">Requirement</span></span> | <span data-ttu-id="f9c55-144">Valor</span><span class="sxs-lookup"><span data-stu-id="f9c55-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c55-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9c55-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c55-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f9c55-146">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f9c55-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9c55-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c55-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9c55-148">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f9c55-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9c55-149">Namespace</span></span><br/>                | <span data-ttu-id="f9c55-150">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f9c55-150">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f9c55-151">MOF</span><span class="sxs-lookup"><span data-stu-id="f9c55-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9c55-152"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9c55-152"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9c55-153">DLL</span><span class="sxs-lookup"><span data-stu-id="f9c55-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9c55-154"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9c55-154"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f9c55-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9c55-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c55-156">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="f9c55-156">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="f9c55-157">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="f9c55-157">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="f9c55-158">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="f9c55-158">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="f9c55-159">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="f9c55-159">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="f9c55-160">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="f9c55-160">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="f9c55-161">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="f9c55-161">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

