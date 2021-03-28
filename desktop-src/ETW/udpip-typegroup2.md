---
description: Essa classe é a classe de tipo de evento para eventos UDP/IP IPv6 Send e Receive. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 059041f6-bf34-4bf8-8e1a-2dfbc6c30edc
title: Classe UdpIp_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup2
- UdpIp_TypeGroup2.PID
- UdpIp_TypeGroup2.size
- UdpIp_TypeGroup2.daddr
- UdpIp_TypeGroup2.saddr
- UdpIp_TypeGroup2.dport
- UdpIp_TypeGroup2.sport
- UdpIp_TypeGroup2.seqnum
- UdpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 88d9cb4935d005f3c25f1fb6c3c421328fb285bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967729"
---
# <a name="udpip_typegroup2-class"></a><span data-ttu-id="64edd-104">\_Classe UdpIp TypeGroup2</span><span class="sxs-lookup"><span data-stu-id="64edd-104">UdpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="64edd-105">Essa classe é a classe de tipo de evento para eventos UDP/IP IPv6 Send e Receive.</span><span class="sxs-lookup"><span data-stu-id="64edd-105">This class is the event type class for UDP/IP IPv6 send and receive events.</span></span>

<span data-ttu-id="64edd-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="64edd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="64edd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64edd-107">Syntax</span></span>

``` syntax
[EventType{26, 27}, EventTypeName{"SendIPV6", "RecvIPV6"}]
class UdpIp_TypeGroup2 : UdpIp
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

## <a name="members"></a><span data-ttu-id="64edd-108">Membros</span><span class="sxs-lookup"><span data-stu-id="64edd-108">Members</span></span>

<span data-ttu-id="64edd-109">A classe **UdpIp \_ TypeGroup2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="64edd-109">The **UdpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="64edd-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="64edd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64edd-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="64edd-111">Properties</span></span>

<span data-ttu-id="64edd-112">A classe **UdpIp \_ TypeGroup2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="64edd-112">The **UdpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64edd-113">CONNID</span><span class="sxs-lookup"><span data-stu-id="64edd-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64edd-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64edd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64edd-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64edd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64edd-116">Qualificadores: WmiDataId (8), ponteiro</span><span class="sxs-lookup"><span data-stu-id="64edd-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="64edd-117">Um identificador de conexão exclusivo para correlacionar eventos pertencentes à mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="64edd-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="64edd-118">daddr</span><span class="sxs-lookup"><span data-stu-id="64edd-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64edd-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="64edd-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="64edd-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64edd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64edd-121">Qualificadores: WmiDataId (3), extensão ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="64edd-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="64edd-122">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="64edd-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="64edd-123">dport</span><span class="sxs-lookup"><span data-stu-id="64edd-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64edd-124">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="64edd-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="64edd-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64edd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64edd-126">Qualificadores: WmiDataId (5), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="64edd-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="64edd-127">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="64edd-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="64edd-128">PID</span><span class="sxs-lookup"><span data-stu-id="64edd-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64edd-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64edd-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64edd-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64edd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64edd-131">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="64edd-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="64edd-132">Identificador do processo associado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="64edd-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="64edd-133">saddr</span><span class="sxs-lookup"><span data-stu-id="64edd-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64edd-134">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="64edd-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="64edd-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64edd-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64edd-136">Qualificadores: WmiDataId (4), extensão ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="64edd-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="64edd-137">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="64edd-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="64edd-138">seqnum</span><span class="sxs-lookup"><span data-stu-id="64edd-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64edd-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64edd-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64edd-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64edd-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64edd-141">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="64edd-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="64edd-142">Número de sequência.</span><span class="sxs-lookup"><span data-stu-id="64edd-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="64edd-143">tamanho</span><span class="sxs-lookup"><span data-stu-id="64edd-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64edd-144">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64edd-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64edd-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64edd-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64edd-146">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="64edd-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="64edd-147">Tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="64edd-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="64edd-148">esporte</span><span class="sxs-lookup"><span data-stu-id="64edd-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64edd-149">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="64edd-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="64edd-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64edd-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64edd-151">Qualificadores: WmiDataId (6), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="64edd-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="64edd-152">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="64edd-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64edd-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64edd-153">Requirements</span></span>



| <span data-ttu-id="64edd-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="64edd-154">Requirement</span></span> | <span data-ttu-id="64edd-155">Valor</span><span class="sxs-lookup"><span data-stu-id="64edd-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="64edd-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64edd-156">Minimum supported client</span></span><br/> | <span data-ttu-id="64edd-157">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64edd-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="64edd-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64edd-158">Minimum supported server</span></span><br/> | <span data-ttu-id="64edd-159">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="64edd-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64edd-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="64edd-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64edd-161">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="64edd-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




