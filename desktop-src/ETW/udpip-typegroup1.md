---
description: Essa classe é a classe de tipo de evento para eventos de envio e recebimento IPv4 de UDP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: f04e0b4c-6a2b-4452-9bdf-38c08b487863
title: Classe UdpIp_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup1
- UdpIp_TypeGroup1.PID
- UdpIp_TypeGroup1.size
- UdpIp_TypeGroup1.daddr
- UdpIp_TypeGroup1.saddr
- UdpIp_TypeGroup1.dport
- UdpIp_TypeGroup1.sport
- UdpIp_TypeGroup1.seqnum
- UdpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d977841cbfe9a88d14056d77a9b943f4d5d4a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967730"
---
# <a name="udpip_typegroup1-class"></a><span data-ttu-id="0498a-104">\_Classe UdpIp TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="0498a-104">UdpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="0498a-105">Essa classe é a classe de tipo de evento para eventos de envio e recebimento IPv4 de UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="0498a-105">This class is the event type class for UDP/IP IPv4 send and receive events.</span></span>

<span data-ttu-id="0498a-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="0498a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0498a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0498a-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"SendIPV4", "RecvIPV4"}]
class UdpIp_TypeGroup1 : UdpIp
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

## <a name="members"></a><span data-ttu-id="0498a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0498a-108">Members</span></span>

<span data-ttu-id="0498a-109">A classe **UdpIp \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0498a-109">The **UdpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="0498a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0498a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0498a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0498a-111">Properties</span></span>

<span data-ttu-id="0498a-112">A classe **UdpIp \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0498a-112">The **UdpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0498a-113">CONNID</span><span class="sxs-lookup"><span data-stu-id="0498a-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0498a-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0498a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0498a-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0498a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0498a-116">Qualificadores: WmiDataId (8), ponteiro</span><span class="sxs-lookup"><span data-stu-id="0498a-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0498a-117">Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="0498a-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="0498a-118">daddr</span><span class="sxs-lookup"><span data-stu-id="0498a-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0498a-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="0498a-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0498a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0498a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0498a-121">Qualificadores: WmiDataId (3), extensão ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="0498a-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="0498a-122">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="0498a-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0498a-123">dport</span><span class="sxs-lookup"><span data-stu-id="0498a-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0498a-124">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="0498a-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0498a-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0498a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0498a-126">Qualificadores: WmiDataId (5), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="0498a-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="0498a-127">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="0498a-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="0498a-128">PID</span><span class="sxs-lookup"><span data-stu-id="0498a-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0498a-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0498a-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0498a-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0498a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0498a-131">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="0498a-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="0498a-132">Identificador do processo associado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="0498a-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="0498a-133">saddr</span><span class="sxs-lookup"><span data-stu-id="0498a-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0498a-134">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="0498a-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0498a-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0498a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0498a-136">Qualificadores: WmiDataId (4), extensão ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="0498a-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="0498a-137">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="0498a-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0498a-138">seqnum</span><span class="sxs-lookup"><span data-stu-id="0498a-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0498a-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0498a-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0498a-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0498a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0498a-141">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="0498a-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="0498a-142">Número de sequência.</span><span class="sxs-lookup"><span data-stu-id="0498a-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="0498a-143">tamanho</span><span class="sxs-lookup"><span data-stu-id="0498a-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0498a-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0498a-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0498a-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0498a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0498a-146">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="0498a-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="0498a-147">Tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="0498a-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="0498a-148">esporte</span><span class="sxs-lookup"><span data-stu-id="0498a-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0498a-149">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="0498a-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="0498a-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0498a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0498a-151">Qualificadores: WmiDataId (6), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="0498a-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="0498a-152">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="0498a-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0498a-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0498a-153">Requirements</span></span>



| <span data-ttu-id="0498a-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="0498a-154">Requirement</span></span> | <span data-ttu-id="0498a-155">Valor</span><span class="sxs-lookup"><span data-stu-id="0498a-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0498a-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0498a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="0498a-157">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0498a-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0498a-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0498a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="0498a-159">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0498a-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0498a-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="0498a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0498a-161">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="0498a-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




