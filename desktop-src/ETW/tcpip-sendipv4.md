---
description: Essa classe é a classe de tipo de evento para eventos de envio de TCP/IP IPv4. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 51a61257-fcbf-4724-80e4-12bdf45b359e
title: Classe TcpIp_SendIPV4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV4
- TcpIp_SendIPV4.PID
- TcpIp_SendIPV4.size
- TcpIp_SendIPV4.daddr
- TcpIp_SendIPV4.saddr
- TcpIp_SendIPV4.dport
- TcpIp_SendIPV4.sport
- TcpIp_SendIPV4.startime
- TcpIp_SendIPV4.endtime
- TcpIp_SendIPV4.seqnum
- TcpIp_SendIPV4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: a255c8a262c53e6dad4654946171fc19a43c6f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921263"
---
# <a name="tcpip_sendipv4-class"></a><span data-ttu-id="5030e-104">\_Classe tcpip SendIPV4</span><span class="sxs-lookup"><span data-stu-id="5030e-104">TcpIp\_SendIPV4 class</span></span>

<span data-ttu-id="5030e-105">Essa classe é a classe de tipo de evento para eventos de envio de TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="5030e-105">This class is the event type class for IPv4 TCP/IP send events.</span></span>

<span data-ttu-id="5030e-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="5030e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5030e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5030e-107">Syntax</span></span>

``` syntax
[EventType{10}, EventTypeName{"SendIPV4"}]
class TcpIp_SendIPV4 : TcpIp
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

## <a name="members"></a><span data-ttu-id="5030e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5030e-108">Members</span></span>

<span data-ttu-id="5030e-109">A classe **tcpip \_ SendIPV4** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5030e-109">The **TcpIp\_SendIPV4** class has these types of members:</span></span>

-   [<span data-ttu-id="5030e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5030e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5030e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5030e-111">Properties</span></span>

<span data-ttu-id="5030e-112">A classe **tcpip \_ SendIPV4** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5030e-112">The **TcpIp\_SendIPV4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5030e-113">CONNID</span><span class="sxs-lookup"><span data-stu-id="5030e-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5030e-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5030e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5030e-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5030e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5030e-116">Qualificadores: WmiDataId (10), ponteiro</span><span class="sxs-lookup"><span data-stu-id="5030e-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5030e-117">Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="5030e-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="5030e-118">daddr</span><span class="sxs-lookup"><span data-stu-id="5030e-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5030e-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="5030e-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5030e-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5030e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5030e-121">Qualificadores: WmiDataId (3), extensão ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="5030e-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="5030e-122">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="5030e-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5030e-123">dport</span><span class="sxs-lookup"><span data-stu-id="5030e-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5030e-124">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="5030e-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5030e-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5030e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5030e-126">Qualificadores: WmiDataId (5), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="5030e-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="5030e-127">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="5030e-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="5030e-128">**final**</span><span class="sxs-lookup"><span data-stu-id="5030e-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5030e-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5030e-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5030e-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5030e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5030e-131">Qualificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="5030e-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="5030e-132">Encerrar o tempo de solicitação de envio.</span><span class="sxs-lookup"><span data-stu-id="5030e-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="5030e-133">PID</span><span class="sxs-lookup"><span data-stu-id="5030e-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5030e-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5030e-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5030e-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5030e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5030e-136">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="5030e-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="5030e-137">Identificador do processo associado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="5030e-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="5030e-138">saddr</span><span class="sxs-lookup"><span data-stu-id="5030e-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5030e-139">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="5030e-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5030e-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5030e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5030e-141">Qualificadores: WmiDataId (4), extensão ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="5030e-141">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="5030e-142">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="5030e-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5030e-143">seqnum</span><span class="sxs-lookup"><span data-stu-id="5030e-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5030e-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5030e-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5030e-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5030e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5030e-146">Qualificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="5030e-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="5030e-147">Número de sequência.</span><span class="sxs-lookup"><span data-stu-id="5030e-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="5030e-148">tamanho</span><span class="sxs-lookup"><span data-stu-id="5030e-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5030e-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5030e-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5030e-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5030e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5030e-151">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="5030e-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="5030e-152">Tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="5030e-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="5030e-153">esporte</span><span class="sxs-lookup"><span data-stu-id="5030e-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5030e-154">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="5030e-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5030e-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5030e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5030e-156">Qualificadores: WmiDataId (6), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="5030e-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="5030e-157">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="5030e-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="5030e-158">**Startime**</span><span class="sxs-lookup"><span data-stu-id="5030e-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5030e-159">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5030e-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5030e-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5030e-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5030e-161">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="5030e-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="5030e-162">Comece a enviar o tempo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="5030e-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5030e-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5030e-163">Requirements</span></span>



| <span data-ttu-id="5030e-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="5030e-164">Requirement</span></span> | <span data-ttu-id="5030e-165">Valor</span><span class="sxs-lookup"><span data-stu-id="5030e-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5030e-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5030e-166">Minimum supported client</span></span><br/> | <span data-ttu-id="5030e-167">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5030e-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5030e-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5030e-168">Minimum supported server</span></span><br/> | <span data-ttu-id="5030e-169">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5030e-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5030e-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="5030e-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5030e-171">**IP**</span><span class="sxs-lookup"><span data-stu-id="5030e-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




