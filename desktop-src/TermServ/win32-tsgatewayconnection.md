---
title: Classe Win32_TSGatewayConnection
description: Representa uma conexão de um computador cliente com um servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 6e76ae25-409d-436a-8eef-8f047194c29c
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayConnection Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayConnection classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection
- Win32_TSGatewayConnection.ConnectionKey
- Win32_TSGatewayConnection.TunnelId
- Win32_TSGatewayConnection.ChannelId
- Win32_TSGatewayConnection.UserName
- Win32_TSGatewayConnection.FullUserName
- Win32_TSGatewayConnection.ClientAddress
- Win32_TSGatewayConnection.ConnectedTime
- Win32_TSGatewayConnection.IdleTime
- Win32_TSGatewayConnection.ConnectedResource
- Win32_TSGatewayConnection.ProtocolName
- Win32_TSGatewayConnection.ConnectedPort
- Win32_TSGatewayConnection.NumberOfKilobytesSent
- Win32_TSGatewayConnection.NumberOfKilobytesReceived
- Win32_TSGatewayConnection.ConnectionDuration
- Win32_TSGatewayConnection.TransportProtocol
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dbaa79213282a70b2f29e6bee9f94901700dddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086273"
---
# <a name="win32_tsgatewayconnection-class"></a><span data-ttu-id="60fe6-105">\_Classe Win32 TSGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="60fe6-105">Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="60fe6-106">Representa uma conexão de um computador cliente com um servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="60fe6-106">Represents a connection from a client computer to a Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="60fe6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60fe6-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnection
{
  string ConnectionKey;
  uint64 TunnelId;
  uint32 ChannelId;
  string UserName;
  string FullUserName;
  string ClientAddress;
  string ConnectedTime;
  string IdleTime;
  string ConnectedResource;
  string ProtocolName;
  uint32 ConnectedPort;
  uint64 NumberOfKilobytesSent;
  uint64 NumberOfKilobytesReceived;
  string ConnectionDuration;
  uint32 TransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="60fe6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="60fe6-108">Members</span></span>

<span data-ttu-id="60fe6-109">A classe **Win32 \_ TSGatewayConnection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="60fe6-109">The **Win32\_TSGatewayConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="60fe6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="60fe6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="60fe6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="60fe6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="60fe6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="60fe6-112">Methods</span></span>

<span data-ttu-id="60fe6-113">A classe **Win32 \_ TSGatewayConnection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="60fe6-113">The **Win32\_TSGatewayConnection** class has these methods.</span></span>



| <span data-ttu-id="60fe6-114">Método</span><span class="sxs-lookup"><span data-stu-id="60fe6-114">Method</span></span>                                                                     | <span data-ttu-id="60fe6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="60fe6-115">Description</span></span>                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60fe6-116">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="60fe6-116">**CheckStatus**</span></span>](checkstatus-win32-tsgatewayconnection.md)               | <span data-ttu-id="60fe6-117">Verifica o status de uma conexão de servidor de gateway de área de trabalho remota e se o servidor de destino está configurado para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="60fe6-117">Checks the status of an RD Gateway server connection, and whether the target server is configured for load balancing.</span></span><br/> |
| [<span data-ttu-id="60fe6-118">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="60fe6-118">**Disconnect**</span></span>](disconnect-win32-tsgatewayconnection.md)                 | <span data-ttu-id="60fe6-119">Encerra a conexão.</span><span class="sxs-lookup"><span data-stu-id="60fe6-119">Ends the connection.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="60fe6-120">**DisconnectProtocol**</span><span class="sxs-lookup"><span data-stu-id="60fe6-120">**DisconnectProtocol**</span></span>](disconnectprotocol-win32-tsgatewayconnection.md) | <span data-ttu-id="60fe6-121">Encerra todas as conexões que usam o protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="60fe6-121">Ends all connections that use the specified protocol.</span></span><br/>                                                                 |
| [<span data-ttu-id="60fe6-122">**DisconnectUser**</span><span class="sxs-lookup"><span data-stu-id="60fe6-122">**DisconnectUser**</span></span>](disconnectuser-win32-tsgatewayconnection.md)         | <span data-ttu-id="60fe6-123">Encerra todas as conexões do usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="60fe6-123">Ends all connections of the specified user.</span></span><br/>                                                                           |



 

### <a name="properties"></a><span data-ttu-id="60fe6-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="60fe6-124">Properties</span></span>

<span data-ttu-id="60fe6-125">A classe **Win32 \_ TSGatewayConnection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="60fe6-125">The **Win32\_TSGatewayConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60fe6-126">**ChannelId**</span><span class="sxs-lookup"><span data-stu-id="60fe6-126">**ChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-127">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60fe6-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-129">Identificador do canal.</span><span class="sxs-lookup"><span data-stu-id="60fe6-129">Channel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-130">**ClientAddress**</span><span class="sxs-lookup"><span data-stu-id="60fe6-130">**ClientAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60fe6-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-133">Endereço IP do cliente.</span><span class="sxs-lookup"><span data-stu-id="60fe6-133">Client IP address.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-134">**ConnectedPort**</span><span class="sxs-lookup"><span data-stu-id="60fe6-134">**ConnectedPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60fe6-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-137">Porta no recurso conectado ao qual o usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="60fe6-137">Port on the connected resource to which the user is connected.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-138">**ConnectedResource**</span><span class="sxs-lookup"><span data-stu-id="60fe6-138">**ConnectedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60fe6-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-141">Nome do computador (ou cluster) ao qual o cliente está conectado.</span><span class="sxs-lookup"><span data-stu-id="60fe6-141">Name of the computer (or cluster) to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-142">**Conectadotime**</span><span class="sxs-lookup"><span data-stu-id="60fe6-142">**ConnectedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60fe6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-145">O carimbo de data/hora para quando a conexão foi estabelecida.</span><span class="sxs-lookup"><span data-stu-id="60fe6-145">The time stamp for when the connection was established.</span></span> <span data-ttu-id="60fe6-146">Esse tempo é redefinido quando a conexão é redefinida, mesmo se ela for reconectada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="60fe6-146">This time is reset when the connection is reset, even if it is automatically reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-147">**ConnectionDuration**</span><span class="sxs-lookup"><span data-stu-id="60fe6-147">**ConnectionDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60fe6-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-150">O tempo decorrido desde a hora conectada.</span><span class="sxs-lookup"><span data-stu-id="60fe6-150">The time that has elapsed since the connected time.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-151">**ConnectionKey**</span><span class="sxs-lookup"><span data-stu-id="60fe6-151">**ConnectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60fe6-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-154">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="60fe6-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-155">Identificador de conexão no formato "tunnelid: channelId".</span><span class="sxs-lookup"><span data-stu-id="60fe6-155">Connection identifier in the format "tunnelId:channelID".</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-156">**FullUserName**</span><span class="sxs-lookup"><span data-stu-id="60fe6-156">**FullUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60fe6-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-159">Nome de usuário completo do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="60fe6-159">Full user name of the connected user.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-160">**Tempo ocioso**</span><span class="sxs-lookup"><span data-stu-id="60fe6-160">**IdleTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60fe6-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-163">Tempo ocioso da conexão.</span><span class="sxs-lookup"><span data-stu-id="60fe6-163">Idle time of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-164">**NumberOfKilobytesReceived**</span><span class="sxs-lookup"><span data-stu-id="60fe6-164">**NumberOfKilobytesReceived**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-165">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60fe6-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-167">Número de kilobytes recebidos do computador cliente pelo servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="60fe6-167">Number of kilobytes received from the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-168">**NumberOfKilobytesSent**</span><span class="sxs-lookup"><span data-stu-id="60fe6-168">**NumberOfKilobytesSent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-169">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60fe6-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-171">Número de kilobytes enviados ao computador cliente pelo servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="60fe6-171">Number of kilobytes sent to the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-172">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="60fe6-172">**ProtocolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60fe6-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-175">Protocolo usado para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="60fe6-175">Protocol that is used to connect to the RD Gateway server.</span></span>

<dt>

<span data-ttu-id="60fe6-176">RDP</span><span class="sxs-lookup"><span data-stu-id="60fe6-176">"RDP"</span></span>
</dt> <dd>

<span data-ttu-id="60fe6-177">O protocolo para o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="60fe6-177">The protocol for the RD Gateway server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="60fe6-178">**TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="60fe6-178">**TransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-179">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60fe6-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-181">Especifica o tipo de transporte para a conexão.</span><span class="sxs-lookup"><span data-stu-id="60fe6-181">Specifies the transport type for the connection.</span></span> <span data-ttu-id="60fe6-182">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="60fe6-182">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="60fe6-183">0</span><span class="sxs-lookup"><span data-stu-id="60fe6-183">0</span></span>
</dt> <dd>

<span data-ttu-id="60fe6-184">RPC sobre transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="60fe6-184">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-185">1</span><span class="sxs-lookup"><span data-stu-id="60fe6-185">1</span></span>
</dt> <dd>

<span data-ttu-id="60fe6-186">Transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="60fe6-186">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-187">2</span><span class="sxs-lookup"><span data-stu-id="60fe6-187">2</span></span>
</dt> <dd>

<span data-ttu-id="60fe6-188">Transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="60fe6-188">UDP transport.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="60fe6-189">**Túnelid**</span><span class="sxs-lookup"><span data-stu-id="60fe6-189">**TunnelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-190">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60fe6-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-192">Identificador de túnel.</span><span class="sxs-lookup"><span data-stu-id="60fe6-192">Tunnel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="60fe6-193">**UserName**</span><span class="sxs-lookup"><span data-stu-id="60fe6-193">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60fe6-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="60fe6-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60fe6-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="60fe6-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60fe6-196">Nome de usuário conectado ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="60fe6-196">User name connected to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60fe6-197">Comentários</span><span class="sxs-lookup"><span data-stu-id="60fe6-197">Remarks</span></span>

<span data-ttu-id="60fe6-198">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="60fe6-198">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="60fe6-199">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="60fe6-199">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60fe6-200">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="60fe6-200">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="60fe6-201">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="60fe6-201">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60fe6-202">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="60fe6-202">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="60fe6-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60fe6-203">Requirements</span></span>



| <span data-ttu-id="60fe6-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="60fe6-204">Requirement</span></span> | <span data-ttu-id="60fe6-205">Valor</span><span class="sxs-lookup"><span data-stu-id="60fe6-205">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60fe6-206">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60fe6-206">Minimum supported client</span></span><br/> | <span data-ttu-id="60fe6-207">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="60fe6-207">None supported</span></span><br/>                                                                |
| <span data-ttu-id="60fe6-208">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60fe6-208">Minimum supported server</span></span><br/> | <span data-ttu-id="60fe6-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60fe6-209">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="60fe6-210">Namespace</span><span class="sxs-lookup"><span data-stu-id="60fe6-210">Namespace</span></span><br/>                | <span data-ttu-id="60fe6-211">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="60fe6-211">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="60fe6-212">MOF</span><span class="sxs-lookup"><span data-stu-id="60fe6-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60fe6-213"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60fe6-213"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="60fe6-214">DLL</span><span class="sxs-lookup"><span data-stu-id="60fe6-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60fe6-215"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60fe6-215"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="60fe6-216">Confira também</span><span class="sxs-lookup"><span data-stu-id="60fe6-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60fe6-217">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="60fe6-217">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="60fe6-218">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="60fe6-218">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="60fe6-219">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="60fe6-219">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="60fe6-220">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="60fe6-220">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="60fe6-221">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="60fe6-221">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="60fe6-222">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="60fe6-222">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

