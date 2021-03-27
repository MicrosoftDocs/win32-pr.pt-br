---
description: Essa classe é a classe de tipo de evento para eventos TCP/IP IPv4. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: ed835df8-6f53-46a3-abf2-c66a1f13f987
title: Classe TcpIp_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup1
- TcpIp_TypeGroup1.PID
- TcpIp_TypeGroup1.size
- TcpIp_TypeGroup1.daddr
- TcpIp_TypeGroup1.saddr
- TcpIp_TypeGroup1.dport
- TcpIp_TypeGroup1.sport
- TcpIp_TypeGroup1.seqnum
- TcpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 70ac95d3d3de5a9bcef610607f3b5a9046b63ea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967578"
---
# <a name="tcpip_typegroup1-class"></a><span data-ttu-id="da985-104">\_Classe tcpip TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="da985-104">TcpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="da985-105">Essa classe é a classe de tipo de evento para eventos TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="da985-105">This class is the event type class for IPv4 TCP/IP events.</span></span>

<span data-ttu-id="da985-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="da985-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="da985-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da985-107">Syntax</span></span>

``` syntax
[EventType{11, 13, 14, 16, 18}, EventTypeName{"RecvIPV4", "DisconnectIPV4", "RetransmitIPV4", "ReconnectIPV4", "TCPCopyIPV4"}]
class TcpIp_TypeGroup1 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="da985-108">Membros</span><span class="sxs-lookup"><span data-stu-id="da985-108">Members</span></span>

<span data-ttu-id="da985-109">A classe **tcpip \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="da985-109">The **TcpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="da985-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da985-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da985-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da985-111">Properties</span></span>

<span data-ttu-id="da985-112">A classe **tcpip \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="da985-112">The **TcpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da985-113">CONNID</span><span class="sxs-lookup"><span data-stu-id="da985-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da985-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da985-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da985-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da985-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da985-116">Qualificadores: WmiDataId (8), ponteiro</span><span class="sxs-lookup"><span data-stu-id="da985-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="da985-117">Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="da985-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="da985-118">daddr</span><span class="sxs-lookup"><span data-stu-id="da985-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da985-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="da985-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="da985-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da985-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da985-121">Qualificadores: WmiDataId (3), extensão ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="da985-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="da985-122">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="da985-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="da985-123">dport</span><span class="sxs-lookup"><span data-stu-id="da985-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da985-124">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="da985-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="da985-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da985-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da985-126">Qualificadores: WmiDataId (5), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="da985-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="da985-127">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="da985-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="da985-128">PID</span><span class="sxs-lookup"><span data-stu-id="da985-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da985-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da985-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da985-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da985-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da985-131">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="da985-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="da985-132">Identificador do processo associado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="da985-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="da985-133">saddr</span><span class="sxs-lookup"><span data-stu-id="da985-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da985-134">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="da985-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="da985-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da985-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da985-136">Qualificadores: WmiDataId (4), extensão ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="da985-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="da985-137">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="da985-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="da985-138">seqnum</span><span class="sxs-lookup"><span data-stu-id="da985-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da985-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da985-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da985-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da985-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da985-141">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="da985-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="da985-142">Número de sequência.</span><span class="sxs-lookup"><span data-stu-id="da985-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="da985-143">tamanho</span><span class="sxs-lookup"><span data-stu-id="da985-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da985-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da985-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da985-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da985-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da985-146">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="da985-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="da985-147">Tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="da985-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="da985-148">esporte</span><span class="sxs-lookup"><span data-stu-id="da985-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da985-149">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="da985-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="da985-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da985-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da985-151">Qualificadores: WmiDataId (6), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="da985-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="da985-152">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="da985-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da985-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da985-153">Requirements</span></span>



| <span data-ttu-id="da985-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="da985-154">Requirement</span></span> | <span data-ttu-id="da985-155">Valor</span><span class="sxs-lookup"><span data-stu-id="da985-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da985-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da985-156">Minimum supported client</span></span><br/> | <span data-ttu-id="da985-157">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da985-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da985-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da985-158">Minimum supported server</span></span><br/> | <span data-ttu-id="da985-159">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="da985-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da985-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="da985-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da985-161">**IP**</span><span class="sxs-lookup"><span data-stu-id="da985-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




