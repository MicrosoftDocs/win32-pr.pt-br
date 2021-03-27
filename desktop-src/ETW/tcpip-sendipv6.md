---
description: Essa classe é a classe de tipo de evento para eventos de envio de TCP/IP IPv6. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 231ef62f-e3a5-497d-b10a-79449dc73c71
title: Classe TcpIp_SendIPV6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV6
- TcpIp_SendIPV6.PID
- TcpIp_SendIPV6.size
- TcpIp_SendIPV6.daddr
- TcpIp_SendIPV6.saddr
- TcpIp_SendIPV6.dport
- TcpIp_SendIPV6.sport
- TcpIp_SendIPV6.startime
- TcpIp_SendIPV6.endtime
- TcpIp_SendIPV6.seqnum
- TcpIp_SendIPV6.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 190b7d4fc64660b1e12240b6461e73066102b6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967577"
---
# <a name="tcpip_sendipv6-class"></a><span data-ttu-id="51cd2-104">\_Classe tcpip SendIPV6</span><span class="sxs-lookup"><span data-stu-id="51cd2-104">TcpIp\_SendIPV6 class</span></span>

<span data-ttu-id="51cd2-105">Essa classe é a classe de tipo de evento para eventos de envio de TCP/IP IPv6.</span><span class="sxs-lookup"><span data-stu-id="51cd2-105">This class is the event type class for IPv6 TCP/IP send events.</span></span>

<span data-ttu-id="51cd2-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="51cd2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="51cd2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51cd2-107">Syntax</span></span>

``` syntax
[EventType{26}, EventTypeName{"SendIPV6"}]
class TcpIp_SendIPV6 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 startime;
  uint32 endtime;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="51cd2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="51cd2-108">Members</span></span>

<span data-ttu-id="51cd2-109">A classe **tcpip \_ SendIPV6** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="51cd2-109">The **TcpIp\_SendIPV6** class has these types of members:</span></span>

-   [<span data-ttu-id="51cd2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="51cd2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51cd2-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="51cd2-111">Properties</span></span>

<span data-ttu-id="51cd2-112">A classe **tcpip \_ SendIPV6** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="51cd2-112">The **TcpIp\_SendIPV6** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51cd2-113">CONNID</span><span class="sxs-lookup"><span data-stu-id="51cd2-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51cd2-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51cd2-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51cd2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-116">Qualificadores: WmiDataId (10), ponteiro</span><span class="sxs-lookup"><span data-stu-id="51cd2-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="51cd2-117">Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="51cd2-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="51cd2-118">daddr</span><span class="sxs-lookup"><span data-stu-id="51cd2-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51cd2-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="51cd2-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51cd2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-121">Qualificadores: WmiDataId (3), extensão ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="51cd2-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="51cd2-122">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="51cd2-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="51cd2-123">dport</span><span class="sxs-lookup"><span data-stu-id="51cd2-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51cd2-124">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="51cd2-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51cd2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-126">Qualificadores: WmiDataId (5), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="51cd2-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="51cd2-127">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="51cd2-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="51cd2-128">**final**</span><span class="sxs-lookup"><span data-stu-id="51cd2-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51cd2-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51cd2-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51cd2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-131">Qualificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="51cd2-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="51cd2-132">Encerrar o tempo de solicitação de envio.</span><span class="sxs-lookup"><span data-stu-id="51cd2-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="51cd2-133">PID</span><span class="sxs-lookup"><span data-stu-id="51cd2-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51cd2-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51cd2-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51cd2-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-136">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="51cd2-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="51cd2-137">Identificador do processo associado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="51cd2-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="51cd2-138">saddr</span><span class="sxs-lookup"><span data-stu-id="51cd2-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51cd2-139">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="51cd2-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51cd2-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-141">Qualificadores: WmiDataId (4), extensão ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="51cd2-141">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="51cd2-142">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="51cd2-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="51cd2-143">seqnum</span><span class="sxs-lookup"><span data-stu-id="51cd2-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51cd2-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51cd2-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51cd2-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-146">Qualificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="51cd2-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="51cd2-147">Número de sequência.</span><span class="sxs-lookup"><span data-stu-id="51cd2-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="51cd2-148">tamanho</span><span class="sxs-lookup"><span data-stu-id="51cd2-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51cd2-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51cd2-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51cd2-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-151">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="51cd2-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="51cd2-152">Tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="51cd2-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="51cd2-153">esporte</span><span class="sxs-lookup"><span data-stu-id="51cd2-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51cd2-154">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="51cd2-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51cd2-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-156">Qualificadores: WmiDataId (6), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="51cd2-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="51cd2-157">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="51cd2-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="51cd2-158">**Startime**</span><span class="sxs-lookup"><span data-stu-id="51cd2-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51cd2-159">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="51cd2-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="51cd2-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51cd2-161">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="51cd2-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="51cd2-162">Comece a enviar o tempo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="51cd2-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51cd2-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51cd2-163">Requirements</span></span>



| <span data-ttu-id="51cd2-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="51cd2-164">Requirement</span></span> | <span data-ttu-id="51cd2-165">Valor</span><span class="sxs-lookup"><span data-stu-id="51cd2-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51cd2-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51cd2-166">Minimum supported client</span></span><br/> | <span data-ttu-id="51cd2-167">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51cd2-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="51cd2-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51cd2-168">Minimum supported server</span></span><br/> | <span data-ttu-id="51cd2-169">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="51cd2-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51cd2-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="51cd2-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51cd2-171">**IP**</span><span class="sxs-lookup"><span data-stu-id="51cd2-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




