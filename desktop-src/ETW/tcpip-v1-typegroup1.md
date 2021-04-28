---
description: Classe TcpIp_V1_TypeGroup1-essa classe é a classe de tipo de evento para eventos TCP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 1cde7e37-52da-4108-90ce-7647a5653f65
title: Classe TcpIp_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V1_TypeGroup1
- TcpIp_V1_TypeGroup1.PID
- TcpIp_V1_TypeGroup1.size
- TcpIp_V1_TypeGroup1.daddr
- TcpIp_V1_TypeGroup1.saddr
- TcpIp_V1_TypeGroup1.dport
- TcpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: 831dfdc228e2c8e128f328784046e833b0b45a39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105754"
---
# <a name="tcpip_v1_typegroup1-class"></a><span data-ttu-id="7daed-104">\_ \_ Classe TypeGroup1 tcpip v1</span><span class="sxs-lookup"><span data-stu-id="7daed-104">TcpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="7daed-105">Essa classe é a classe de tipo de evento para eventos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7daed-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="7daed-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="7daed-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7daed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7daed-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept", "Reconnect"}]
class TcpIp_V1_TypeGroup1 : TcpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="7daed-108">Membros</span><span class="sxs-lookup"><span data-stu-id="7daed-108">Members</span></span>

<span data-ttu-id="7daed-109">A classe **tcpip \_ v1 \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7daed-109">The **TcpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="7daed-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7daed-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7daed-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7daed-111">Properties</span></span>

<span data-ttu-id="7daed-112">A classe **tcpip \_ v1 \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7daed-112">The **TcpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7daed-113">daddr</span><span class="sxs-lookup"><span data-stu-id="7daed-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7daed-114">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="7daed-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7daed-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7daed-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7daed-116">Qualificadores: WmiDataId (3), extensão ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="7daed-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="7daed-117">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="7daed-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7daed-118">dport</span><span class="sxs-lookup"><span data-stu-id="7daed-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7daed-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="7daed-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7daed-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7daed-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7daed-121">Qualificadores: WmiDataId (5), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="7daed-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="7daed-122">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="7daed-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="7daed-123">PID</span><span class="sxs-lookup"><span data-stu-id="7daed-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7daed-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7daed-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7daed-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7daed-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7daed-126">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="7daed-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="7daed-127">Identificador do processo associado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="7daed-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="7daed-128">saddr</span><span class="sxs-lookup"><span data-stu-id="7daed-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7daed-129">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="7daed-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7daed-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7daed-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7daed-131">Qualificadores: WmiDataId (4), extensão ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="7daed-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="7daed-132">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="7daed-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7daed-133">tamanho</span><span class="sxs-lookup"><span data-stu-id="7daed-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7daed-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7daed-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7daed-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7daed-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7daed-136">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="7daed-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="7daed-137">Tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="7daed-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="7daed-138">esporte</span><span class="sxs-lookup"><span data-stu-id="7daed-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7daed-139">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="7daed-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7daed-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7daed-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7daed-141">Qualificadores: WmiDataId (6), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="7daed-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="7daed-142">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="7daed-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7daed-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7daed-143">Requirements</span></span>



| <span data-ttu-id="7daed-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="7daed-144">Requirement</span></span> | <span data-ttu-id="7daed-145">Valor</span><span class="sxs-lookup"><span data-stu-id="7daed-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7daed-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7daed-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7daed-147">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7daed-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7daed-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7daed-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7daed-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7daed-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7daed-150">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7daed-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7daed-151">**TcpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="7daed-151">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 




