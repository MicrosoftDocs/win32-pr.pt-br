---
description: O Win32 \_ NetworkProtocol&\# 8194; A classe WMI representa um protocolo e suas características de rede em um sistema de computador Win32.
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Classe Win32_NetworkProtocol
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457142"
---
# <a name="win32_networkprotocol-class"></a><span data-ttu-id="c2a28-103">\_Classe Win32 NetworkProtocol</span><span class="sxs-lookup"><span data-stu-id="c2a28-103">Win32\_NetworkProtocol class</span></span>

<span data-ttu-id="c2a28-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkProtocol do Win32** representa um protocolo e suas características de rede em um sistema de computador Win32.</span><span class="sxs-lookup"><span data-stu-id="c2a28-104">The **Win32\_NetworkProtocol** [WMI class](../wmisdk/retrieving-a-class.md) represents a protocol and its network characteristics on a Win32 computer system.</span></span>

<span data-ttu-id="c2a28-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c2a28-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c2a28-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="c2a28-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a28-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2a28-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a><span data-ttu-id="c2a28-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c2a28-108">Members</span></span>

<span data-ttu-id="c2a28-109">A classe **Win32 \_ NetworkProtocol** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c2a28-109">The **Win32\_NetworkProtocol** class has these types of members:</span></span>

-   [<span data-ttu-id="c2a28-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c2a28-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2a28-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c2a28-111">Properties</span></span>

<span data-ttu-id="c2a28-112">A classe **Win32 \_ NetworkProtocol** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c2a28-112">The **Win32\_NetworkProtocol** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2a28-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c2a28-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2a28-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-116">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c2a28-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-117">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c2a28-117">A short textual description of the object.</span></span>

<span data-ttu-id="c2a28-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2a28-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-119">**ConnectionlessService**</span><span class="sxs-lookup"><span data-stu-id="c2a28-119">**ConnectionlessService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-120">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-122">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets de \| protocolo \_ informações \| dwServiceFlags \| XP1 sem \_ conexão")</span><span class="sxs-lookup"><span data-stu-id="c2a28-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP1\_CONNECTIONLESS")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-123">O protocolo oferece suporte ao serviço sem conexão.</span><span class="sxs-lookup"><span data-stu-id="c2a28-123">Protocol supports connectionless service.</span></span> <span data-ttu-id="c2a28-124">Um serviço sem conexão (datagrama) descreve um protocolo de comunicação ou transporte no qual os pacotes de dados são roteados independentemente um do outro e podem seguir rotas diferentes e chegam em uma ordem diferente da que foram enviados.</span><span class="sxs-lookup"><span data-stu-id="c2a28-124">A connectionless (datagram) service describes a communications protocol or transport in which data packets are routed independently of each other and may follow different routes and arrive in a different order from that in which they were sent.</span></span> <span data-ttu-id="c2a28-125">Por outro lado, um serviço orientado a conexão fornece um circuito virtual por meio do qual os pacotes de dados são recebidos na mesma ordem em que foram transmitidos.</span><span class="sxs-lookup"><span data-stu-id="c2a28-125">Conversely, a connection-oriented service provides a virtual circuit through which data packets are received in the same order they were transmitted.</span></span> <span data-ttu-id="c2a28-126">Se a conexão entre os computadores falhar, o aplicativo será notificado.</span><span class="sxs-lookup"><span data-stu-id="c2a28-126">If the connection between computers fails, the application is notified.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c2a28-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2a28-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-130">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="c2a28-130">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-131">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c2a28-131">A textual description of the object.</span></span>

<span data-ttu-id="c2a28-132">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2a28-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-133">**GuaranteesDelivery**</span><span class="sxs-lookup"><span data-stu-id="c2a28-133">**GuaranteesDelivery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-136">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ garantido \_ Delivery")</span><span class="sxs-lookup"><span data-stu-id="c2a28-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_DELIVERY")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-137">O protocolo oferece suporte à entrega de pacotes de dados.</span><span class="sxs-lookup"><span data-stu-id="c2a28-137">Protocol supports delivery of data packets.</span></span> <span data-ttu-id="c2a28-138">Se esse sinalizador for **false**, é incerteza que todos os dados enviados atingirão o destino pretendido.</span><span class="sxs-lookup"><span data-stu-id="c2a28-138">If this flag is **FALSE**, it is uncertain that all of the data sent will reach the intended destination.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-139">**GuaranteesSequencing**</span><span class="sxs-lookup"><span data-stu-id="c2a28-139">**GuaranteesSequencing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-140">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-142">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ asguaranteed \_ Order")</span><span class="sxs-lookup"><span data-stu-id="c2a28-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_ORDER")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-143">O protocolo garante que os dados chegarão na ordem em que foram enviados.</span><span class="sxs-lookup"><span data-stu-id="c2a28-143">Protocol ensures that data will arrive in the order in which it was sent.</span></span> <span data-ttu-id="c2a28-144">Lembre-se de que essa característica não garante a entrega dos dados, apenas sua ordem.</span><span class="sxs-lookup"><span data-stu-id="c2a28-144">Be aware that this characteristic does not ensure delivery of the data, only its order.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c2a28-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-146">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c2a28-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-148">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="c2a28-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-149">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="c2a28-149">Indicates when the object was installed.</span></span> <span data-ttu-id="c2a28-150">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="c2a28-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c2a28-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2a28-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-152">**MaximumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="c2a28-152">**MaximumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-153">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2a28-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-155">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| iMaxSockAddr"), [**Units**](../wmisdk/standard-qualifiers.md) ("characters")</span><span class="sxs-lookup"><span data-stu-id="c2a28-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMaxSockAddr"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-156">Comprimento máximo de um endereço de soquete com suporte pelo protocolo.</span><span class="sxs-lookup"><span data-stu-id="c2a28-156">Maximum length of a socket address supported by the protocol.</span></span> <span data-ttu-id="c2a28-157">Os endereços de soquete podem ser itens como uma URL ( `www.microsoft.com` ) ou um endereço IP ( `130.215.24.1` ).</span><span class="sxs-lookup"><span data-stu-id="c2a28-157">Socket addresses may be items such as a URL (`www.microsoft.com`) or an IP address (`130.215.24.1`).</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-158">**MaximumMessageSize**</span><span class="sxs-lookup"><span data-stu-id="c2a28-158">**MaximumMessageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-159">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2a28-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-161">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwMessageSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("characters")</span><span class="sxs-lookup"><span data-stu-id="c2a28-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwMessageSize"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-162">Tamanho máximo de mensagem suportado pelo protocolo.</span><span class="sxs-lookup"><span data-stu-id="c2a28-162">Maximum message size supported by the protocol.</span></span> <span data-ttu-id="c2a28-163">Esse é o tamanho máximo de uma mensagem que pode ser enviada ou recebida pelo host.</span><span class="sxs-lookup"><span data-stu-id="c2a28-163">This is the maximum size of a message that can be sent from or received by the host.</span></span> <span data-ttu-id="c2a28-164">Para protocolos que não dão suporte ao enquadramento de mensagens, o tamanho máximo real de uma mensagem que pode ser enviada para um determinado endereço pode ser menor que esse valor.</span><span class="sxs-lookup"><span data-stu-id="c2a28-164">For protocols that do not support message framing, the actual maximum size of a message that can be sent to a given address may be less than this value.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-165">**MessageOriented**</span><span class="sxs-lookup"><span data-stu-id="c2a28-165">**MessageOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-166">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-168">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 do \_ \| Windows Sockets \| Protocol \_ info do \| dwServiceFlags \| XP \_ \_ orientado a mensagens")</span><span class="sxs-lookup"><span data-stu-id="c2a28-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_MESSAGE\_ORIENTED")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-169">O protocolo é orientado a mensagens.</span><span class="sxs-lookup"><span data-stu-id="c2a28-169">Protocol is message-oriented.</span></span> <span data-ttu-id="c2a28-170">Um protocolo orientado a mensagens usa pacotes de dados para transferir informações.</span><span class="sxs-lookup"><span data-stu-id="c2a28-170">A message-oriented protocol uses packets of data to transfer information.</span></span> <span data-ttu-id="c2a28-171">Por outro lado, os protocolos orientados a fluxo transferem dados como um fluxo contínuo de bytes.</span><span class="sxs-lookup"><span data-stu-id="c2a28-171">Conversely, stream-oriented protocols transfer data as a continuous stream of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-172">**MinimumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="c2a28-172">**MinimumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-173">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2a28-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-175">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| iMinSockAddr"), [**Units**](../wmisdk/standard-qualifiers.md) ("characters")</span><span class="sxs-lookup"><span data-stu-id="c2a28-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMinSockAddr "), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-176">Comprimento mínimo de um endereço de soquete com suporte pelo protocolo.</span><span class="sxs-lookup"><span data-stu-id="c2a28-176">Minimum length of a socket address supported by the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-177">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c2a28-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2a28-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-180">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| lpProtocol")</span><span class="sxs-lookup"><span data-stu-id="c2a28-180">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|lpProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-181">Nome para o protocolo.</span><span class="sxs-lookup"><span data-stu-id="c2a28-181">Name for the protocol.</span></span>

<span data-ttu-id="c2a28-182">Exemplo: "TCP/IP"</span><span class="sxs-lookup"><span data-stu-id="c2a28-182">Example: "TCP/IP"</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-183">**PseudoStreamOriented**</span><span class="sxs-lookup"><span data-stu-id="c2a28-183">**PseudoStreamOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-184">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-186">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ pseudo \_ Stream")</span><span class="sxs-lookup"><span data-stu-id="c2a28-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_PSEUDO\_STREAM")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-187">O protocolo é um protocolo orientado a mensagens que pode receber pacotes de dados de comprimento variável ou dados transmitidos para todas as operações de recebimento.</span><span class="sxs-lookup"><span data-stu-id="c2a28-187">Protocol is a message-oriented protocol that can receive variable-length data packets or streamed data for all receive operations.</span></span> <span data-ttu-id="c2a28-188">Essa capacidade opcional é útil quando um aplicativo não quer o protocolo para enquadrar mensagens e requer características orientadas a fluxo.</span><span class="sxs-lookup"><span data-stu-id="c2a28-188">This optional ability is useful when an application does not want the protocol to frame messages, and requires stream-oriented characteristics.</span></span> <span data-ttu-id="c2a28-189">Se **for true**, o protocolo será orientado a um pseudo-fluxo.</span><span class="sxs-lookup"><span data-stu-id="c2a28-189">If **TRUE**, the protocol is pseudo stream-oriented.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-190">**Status**</span><span class="sxs-lookup"><span data-stu-id="c2a28-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c2a28-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-193">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="c2a28-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-194">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c2a28-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="c2a28-195">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="c2a28-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c2a28-196">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="c2a28-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c2a28-197">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="c2a28-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c2a28-198">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="c2a28-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c2a28-199">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="c2a28-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c2a28-200">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="c2a28-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c2a28-201">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2a28-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c2a28-202">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c2a28-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c2a28-203">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c2a28-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c2a28-204">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="c2a28-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c2a28-205">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c2a28-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c2a28-206">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c2a28-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c2a28-207">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c2a28-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c2a28-208">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c2a28-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c2a28-209">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="c2a28-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c2a28-210">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="c2a28-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c2a28-211">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="c2a28-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c2a28-212">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c2a28-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c2a28-213">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="c2a28-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c2a28-214">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="c2a28-214">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c2a28-215">**SupportsBroadcasting**</span><span class="sxs-lookup"><span data-stu-id="c2a28-215">**SupportsBroadcasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-216">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-218">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ suporta \_ Broadcast")</span><span class="sxs-lookup"><span data-stu-id="c2a28-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_BROADCAST")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-219">O protocolo dá suporte a um mecanismo de transmissão de mensagens pela rede.</span><span class="sxs-lookup"><span data-stu-id="c2a28-219">Protocol supports a mechanism for broadcasting messages across the network.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-220">**SupportsConnectData**</span><span class="sxs-lookup"><span data-stu-id="c2a28-220">**SupportsConnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-221">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-223">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ Connect \_ Data")</span><span class="sxs-lookup"><span data-stu-id="c2a28-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_CONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-224">O protocolo permite que os dados sejam conectados pela rede.</span><span class="sxs-lookup"><span data-stu-id="c2a28-224">Protocol allows data to be connected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-225">**SupportsDisconnectData**</span><span class="sxs-lookup"><span data-stu-id="c2a28-225">**SupportsDisconnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-226">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-228">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ Desconectar \_ dados")</span><span class="sxs-lookup"><span data-stu-id="c2a28-228">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_DISCONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-229">O protocolo permite que os dados sejam desconectados pela rede.</span><span class="sxs-lookup"><span data-stu-id="c2a28-229">Protocol allows data to be disconnected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-230">**SupportsEncryption**</span><span class="sxs-lookup"><span data-stu-id="c2a28-230">**SupportsEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-231">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-233">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets de \| protocolo \_ informações \| dwServiceFlags \| XP \_ criptografas")</span><span class="sxs-lookup"><span data-stu-id="c2a28-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_ENCRYPTS")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-234">O protocolo dá suporte à criptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="c2a28-234">Protocol supports data encryption.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-235">**SupportsExpeditedData**</span><span class="sxs-lookup"><span data-stu-id="c2a28-235">**SupportsExpeditedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-236">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-238">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ expedited \_ Data")</span><span class="sxs-lookup"><span data-stu-id="c2a28-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_EXPEDITED\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-239">O protocolo oferece suporte a dados emitidos (também conhecidos como dados urgentes) na rede.</span><span class="sxs-lookup"><span data-stu-id="c2a28-239">Protocol supports expedited data (also known as urgent data) across the network.</span></span> <span data-ttu-id="c2a28-240">Os dados acelerados podem ignorar o controle de fluxo e receber a prioridade sobre pacotes de dados normais.</span><span class="sxs-lookup"><span data-stu-id="c2a28-240">Expedited data can bypass flow control and receive priority over normal data packets.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-241">**SupportsFragmentation**</span><span class="sxs-lookup"><span data-stu-id="c2a28-241">**SupportsFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-242">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-244">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 do \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ Fragmentation")</span><span class="sxs-lookup"><span data-stu-id="c2a28-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_FRAGMENTATION")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-245">O protocolo dá suporte à transmissão de dados em fragmentos.</span><span class="sxs-lookup"><span data-stu-id="c2a28-245">Protocol supports transmitting the data in fragments.</span></span> <span data-ttu-id="c2a28-246">A unidade de transferência máxima (MTU) da rede física está oculta dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c2a28-246">Physical network maximum transfer unit (MTU) is hidden from applications.</span></span> <span data-ttu-id="c2a28-247">Cada tipo de mídia tem um tamanho de quadro máximo que não pode ser excedido.</span><span class="sxs-lookup"><span data-stu-id="c2a28-247">Each media type has a maximum frame size that cannot be exceeded.</span></span> <span data-ttu-id="c2a28-248">A camada de link descobre a MTU e a relata para os protocolos usados.</span><span class="sxs-lookup"><span data-stu-id="c2a28-248">The link layer discovers the MTU and reports it to the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-249">**SupportsGracefulClosing**</span><span class="sxs-lookup"><span data-stu-id="c2a28-249">**SupportsGracefulClosing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-250">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-252">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets \| Protocol \_ info \| dwServiceFlags \| XP \_ normal \_ Close")</span><span class="sxs-lookup"><span data-stu-id="c2a28-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GRACEFUL\_CLOSE")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-253">O protocolo dá suporte a operações de fechamento de duas fases, também conhecidas como "operações de fechamento normais".</span><span class="sxs-lookup"><span data-stu-id="c2a28-253">Protocol supports two-phase close operations, also known as "graceful close operations".</span></span> <span data-ttu-id="c2a28-254">Caso contrário, o protocolo oferece suporte apenas a operações de fechamento anuladas.</span><span class="sxs-lookup"><span data-stu-id="c2a28-254">If not, the protocol supports only abortive close operations.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-255">**SupportsGuaranteedBandwidth**</span><span class="sxs-lookup"><span data-stu-id="c2a28-255">**SupportsGuaranteedBandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-256">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-258">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API do Win32 \_ \| Windows Sockets de \| protocolo \_ informações de alocação de largura de \| \| banda dwServiceFlags XP \_ \_ ")</span><span class="sxs-lookup"><span data-stu-id="c2a28-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_BANDWIDTH\_ALLOCATION")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-259">O protocolo tem um mecanismo para estabelecer e manter uma largura de banda.</span><span class="sxs-lookup"><span data-stu-id="c2a28-259">Protocol has a mechanism to establish and maintain a bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-260">**SupportsMulticasting**</span><span class="sxs-lookup"><span data-stu-id="c2a28-260">**SupportsMulticasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-261">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-263">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("as \_ informações do protocolo de estruturas do Windows Sockets de API do Win32 \| \| \_ \| dwServiceFlags \| XP \_ dão suporte a \_ multicast")</span><span class="sxs-lookup"><span data-stu-id="c2a28-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_MULTICAST")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-264">O protocolo dá suporte a multicast.</span><span class="sxs-lookup"><span data-stu-id="c2a28-264">Protocol supports multicasting.</span></span>

</dd> <dt>

<span data-ttu-id="c2a28-265">**SupportsQualityofService**</span><span class="sxs-lookup"><span data-stu-id="c2a28-265">**SupportsQualityofService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2a28-266">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c2a28-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c2a28-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2a28-268">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets estruturas \| WSAPROTOCOL \_ info \| dwServiceFlags1 \| XP1 \_ QoS \_ supported")</span><span class="sxs-lookup"><span data-stu-id="c2a28-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|WSAPROTOCOL\_INFO\|dwServiceFlags1\|XP1\_QOS\_SUPPORTED")</span></span>
</dt> </dl>

<span data-ttu-id="c2a28-269">O protocolo é capaz de dar suporte à qualidade de serviço (QoS) pelo provedor de serviços em camadas subjacente ou pela operadora de transporte.</span><span class="sxs-lookup"><span data-stu-id="c2a28-269">Protocol is capable of Quality of Service (QoS) support by the underlying layered service provider or transport carrier.</span></span> <span data-ttu-id="c2a28-270">QoS é uma coleção de componentes que habilitam a diferenciação e o tratamento preferencial para subconjuntos de dados transmitidos pela rede.</span><span class="sxs-lookup"><span data-stu-id="c2a28-270">QoS is a collection of components that enable differentiation and preferential treatment for subsets of data transmitted over the network.</span></span> <span data-ttu-id="c2a28-271">QoS significa que os subconjuntos de dados recebem maior prioridade ou serviço garantido ao atravessar uma rede.</span><span class="sxs-lookup"><span data-stu-id="c2a28-271">QoS means subsets of data get higher priority or guaranteed service when traversing a network.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2a28-272">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2a28-272">Remarks</span></span>

<span data-ttu-id="c2a28-273">A classe **Win32 \_ NetworkProtocol** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c2a28-273">The **Win32\_NetworkProtocol** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c2a28-274">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c2a28-274">Examples</span></span>

<span data-ttu-id="c2a28-275">O exemplo de código VBScript a seguir demonstra como recuperar uma lista de serviços em execução de instâncias do **Win32 \_ NetworkProtocol**.</span><span class="sxs-lookup"><span data-stu-id="c2a28-275">The following VBScript code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



<span data-ttu-id="c2a28-276">O exemplo de código Perl a seguir demonstra como recuperar uma lista de serviços em execução de instâncias do **Win32 \_ NetworkProtocol**.</span><span class="sxs-lookup"><span data-stu-id="c2a28-276">The following Perl code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="c2a28-277">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2a28-277">Requirements</span></span>



| <span data-ttu-id="c2a28-278">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2a28-278">Requirement</span></span> | <span data-ttu-id="c2a28-279">Valor</span><span class="sxs-lookup"><span data-stu-id="c2a28-279">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a28-280">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2a28-280">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a28-281">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2a28-281">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2a28-282">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2a28-282">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a28-283">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2a28-283">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2a28-284">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2a28-284">Namespace</span></span><br/>                | <span data-ttu-id="c2a28-285">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c2a28-285">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c2a28-286">MOF</span><span class="sxs-lookup"><span data-stu-id="c2a28-286">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2a28-287"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2a28-287"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2a28-288">DLL</span><span class="sxs-lookup"><span data-stu-id="c2a28-288">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2a28-289"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2a28-289"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2a28-290">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2a28-290">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a28-291">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="c2a28-291">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="c2a28-292">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="c2a28-292">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
