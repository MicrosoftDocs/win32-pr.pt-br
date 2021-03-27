---
description: Essa classe é a classe de tipo de evento para eventos TCP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 007f0744-8b74-4c57-85bc-f6bdb20bffa7
title: Classe TcpIp_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V0_TypeGroup1
- TcpIp_V0_TypeGroup1.daddr
- TcpIp_V0_TypeGroup1.saddr
- TcpIp_V0_TypeGroup1.dport
- TcpIp_V0_TypeGroup1.sport
- TcpIp_V0_TypeGroup1.size
- TcpIp_V0_TypeGroup1.PID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c21025990fe3e21cd5322b651e543472fa8d48c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296559"
---
# <a name="tcpip_v0_typegroup1-class"></a><span data-ttu-id="bd684-104">\_Classe tcpip V0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="bd684-104">TcpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="bd684-105">Essa classe é a classe de tipo de evento para eventos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="bd684-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="bd684-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="bd684-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd684-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd684-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept"}]
class TcpIp_V0_TypeGroup1 : TcpIp_V0
{
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 size;
  uint32 PID;
};
```

## <a name="members"></a><span data-ttu-id="bd684-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bd684-108">Members</span></span>

<span data-ttu-id="bd684-109">A classe **tcpip \_ V0 \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bd684-109">The **TcpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="bd684-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bd684-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd684-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bd684-111">Properties</span></span>

<span data-ttu-id="bd684-112">A classe **tcpip \_ V0 \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bd684-112">The **TcpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd684-113">daddr</span><span class="sxs-lookup"><span data-stu-id="bd684-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd684-114">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="bd684-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="bd684-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd684-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd684-116">Qualificadores: WmiDataId (1), extensão ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="bd684-116">Qualifiers: WmiDataId(1), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="bd684-117">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="bd684-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="bd684-118">dport</span><span class="sxs-lookup"><span data-stu-id="bd684-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd684-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="bd684-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="bd684-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd684-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd684-121">Qualificadores: WmiDataId (3), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="bd684-121">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="bd684-122">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="bd684-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="bd684-123">PID</span><span class="sxs-lookup"><span data-stu-id="bd684-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd684-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd684-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd684-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd684-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd684-126">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="bd684-126">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="bd684-127">Identificador do processo associado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="bd684-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="bd684-128">saddr</span><span class="sxs-lookup"><span data-stu-id="bd684-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd684-129">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="bd684-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="bd684-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd684-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd684-131">Qualificadores: WmiDataId (2), extensão ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="bd684-131">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="bd684-132">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="bd684-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="bd684-133">tamanho</span><span class="sxs-lookup"><span data-stu-id="bd684-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd684-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd684-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd684-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd684-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd684-136">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="bd684-136">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="bd684-137">Tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="bd684-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="bd684-138">esporte</span><span class="sxs-lookup"><span data-stu-id="bd684-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd684-139">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="bd684-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="bd684-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd684-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd684-141">Qualificadores: WmiDataId (4), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="bd684-141">Qualifiers: WmiDataId(4), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="bd684-142">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="bd684-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd684-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd684-143">Requirements</span></span>



| <span data-ttu-id="bd684-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd684-144">Requirement</span></span> | <span data-ttu-id="bd684-145">Valor</span><span class="sxs-lookup"><span data-stu-id="bd684-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="bd684-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd684-146">Minimum supported client</span></span><br/> | <span data-ttu-id="bd684-147">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bd684-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bd684-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd684-148">Minimum supported server</span></span><br/> | <span data-ttu-id="bd684-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bd684-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="bd684-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd684-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd684-151">**\_V0 tcpip**</span><span class="sxs-lookup"><span data-stu-id="bd684-151">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> </dl>

 

 




