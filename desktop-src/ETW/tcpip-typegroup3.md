---
description: Essa classe é a classe de tipo de evento para eventos TCP/IP IPv6. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: d24e667e-ec7f-492a-989e-a02ff4c8ac10
title: Classe TcpIp_TypeGroup3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup3
- TcpIp_TypeGroup3.PID
- TcpIp_TypeGroup3.size
- TcpIp_TypeGroup3.daddr
- TcpIp_TypeGroup3.saddr
- TcpIp_TypeGroup3.dport
- TcpIp_TypeGroup3.sport
- TcpIp_TypeGroup3.seqnum
- TcpIp_TypeGroup3.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 82aa119c0d770a26060b1e8d6ab74433146bb3c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967574"
---
# <a name="tcpip_typegroup3-class"></a><span data-ttu-id="3432d-104">\_Classe tcpip TypeGroup3</span><span class="sxs-lookup"><span data-stu-id="3432d-104">TcpIp\_TypeGroup3 class</span></span>

<span data-ttu-id="3432d-105">Essa classe é a classe de tipo de evento para eventos TCP/IP IPv6.</span><span class="sxs-lookup"><span data-stu-id="3432d-105">This class is the event type class for IPv6 TCP/IP events.</span></span>

<span data-ttu-id="3432d-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="3432d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3432d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3432d-107">Syntax</span></span>

``` syntax
[EventType{27, 29, 30, 32, 34}, EventTypeName{"RecvIPV6", "DisconnectIPV6", "RetransmitIPV6", "ReconnectIPV6", "TCPCopyIPV6"}]
class TcpIp_TypeGroup3 : TcpIp
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

## <a name="members"></a><span data-ttu-id="3432d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3432d-108">Members</span></span>

<span data-ttu-id="3432d-109">A classe **tcpip \_ TypeGroup3** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3432d-109">The **TcpIp\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="3432d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3432d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3432d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3432d-111">Properties</span></span>

<span data-ttu-id="3432d-112">A classe **tcpip \_ TypeGroup3** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3432d-112">The **TcpIp\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3432d-113">CONNID</span><span class="sxs-lookup"><span data-stu-id="3432d-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3432d-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3432d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3432d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3432d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3432d-116">Qualificadores: WmiDataId (6), ponteiro</span><span class="sxs-lookup"><span data-stu-id="3432d-116">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3432d-117">Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="3432d-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="3432d-118">daddr</span><span class="sxs-lookup"><span data-stu-id="3432d-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3432d-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="3432d-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="3432d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3432d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3432d-121">Qualificadores: WmiDataId (3), extensão ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="3432d-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="3432d-122">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="3432d-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3432d-123">dport</span><span class="sxs-lookup"><span data-stu-id="3432d-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3432d-124">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="3432d-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="3432d-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3432d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3432d-126">Qualificadores: WmiDataId (5), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="3432d-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="3432d-127">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="3432d-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="3432d-128">PID</span><span class="sxs-lookup"><span data-stu-id="3432d-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3432d-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3432d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3432d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3432d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3432d-131">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="3432d-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="3432d-132">Identificador do processo associado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="3432d-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="3432d-133">saddr</span><span class="sxs-lookup"><span data-stu-id="3432d-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3432d-134">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="3432d-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="3432d-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3432d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3432d-136">Qualificadores: WmiDataId (4), extensão ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="3432d-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="3432d-137">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="3432d-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3432d-138">seqnum</span><span class="sxs-lookup"><span data-stu-id="3432d-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3432d-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3432d-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3432d-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3432d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3432d-141">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="3432d-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="3432d-142">Número de sequência.</span><span class="sxs-lookup"><span data-stu-id="3432d-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="3432d-143">tamanho</span><span class="sxs-lookup"><span data-stu-id="3432d-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3432d-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3432d-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3432d-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3432d-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3432d-146">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="3432d-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="3432d-147">Tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="3432d-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="3432d-148">esporte</span><span class="sxs-lookup"><span data-stu-id="3432d-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3432d-149">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="3432d-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="3432d-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3432d-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3432d-151">Qualificadores: WmiDataId (6), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="3432d-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="3432d-152">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="3432d-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3432d-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3432d-153">Requirements</span></span>



| <span data-ttu-id="3432d-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="3432d-154">Requirement</span></span> | <span data-ttu-id="3432d-155">Valor</span><span class="sxs-lookup"><span data-stu-id="3432d-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3432d-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3432d-156">Minimum supported client</span></span><br/> | <span data-ttu-id="3432d-157">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3432d-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3432d-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3432d-158">Minimum supported server</span></span><br/> | <span data-ttu-id="3432d-159">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3432d-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3432d-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="3432d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3432d-161">**IP**</span><span class="sxs-lookup"><span data-stu-id="3432d-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




