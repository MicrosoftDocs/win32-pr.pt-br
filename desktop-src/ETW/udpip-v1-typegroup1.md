---
description: Essa classe é a classe de tipo de evento para eventos UDP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: Classe UdpIp_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: 58f7506aefa79c3bc9136d2e3e76d662f545a921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967289"
---
# <a name="udpip_v1_typegroup1-class"></a><span data-ttu-id="fc222-104">\_Classe UdpIp v1 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="fc222-104">UdpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="fc222-105">Essa classe é a classe de tipo de evento para eventos UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="fc222-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="fc222-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="fc222-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc222-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc222-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="fc222-108">Membros</span><span class="sxs-lookup"><span data-stu-id="fc222-108">Members</span></span>

<span data-ttu-id="fc222-109">A **classe \_ \_ TypeGroup1 UdpIp v1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fc222-109">The **UdpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="fc222-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc222-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc222-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc222-111">Properties</span></span>

<span data-ttu-id="fc222-112">A **classe \_ \_ TypeGroup1 UdpIp v1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fc222-112">The **UdpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc222-113">daddr</span><span class="sxs-lookup"><span data-stu-id="fc222-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc222-114">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="fc222-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="fc222-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc222-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc222-116">Qualificadores: WmiDataId (3), extensão ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="fc222-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="fc222-117">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="fc222-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="fc222-118">dport</span><span class="sxs-lookup"><span data-stu-id="fc222-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc222-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="fc222-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="fc222-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc222-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc222-121">Qualificadores: WmiDataId (5), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="fc222-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="fc222-122">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="fc222-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="fc222-123">PID</span><span class="sxs-lookup"><span data-stu-id="fc222-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc222-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc222-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc222-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc222-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc222-126">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="fc222-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="fc222-127">Identificador do processo associado à solicitação.</span><span class="sxs-lookup"><span data-stu-id="fc222-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="fc222-128">saddr</span><span class="sxs-lookup"><span data-stu-id="fc222-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc222-129">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="fc222-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="fc222-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc222-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc222-131">Qualificadores: WmiDataId (4), extensão ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="fc222-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="fc222-132">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="fc222-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="fc222-133">tamanho</span><span class="sxs-lookup"><span data-stu-id="fc222-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc222-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc222-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc222-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc222-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc222-136">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="fc222-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="fc222-137">Tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="fc222-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="fc222-138">esporte</span><span class="sxs-lookup"><span data-stu-id="fc222-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc222-139">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="fc222-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="fc222-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc222-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc222-141">Qualificadores: WmiDataId (6), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="fc222-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="fc222-142">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="fc222-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc222-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc222-143">Requirements</span></span>



| <span data-ttu-id="fc222-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc222-144">Requirement</span></span> | <span data-ttu-id="fc222-145">Valor</span><span class="sxs-lookup"><span data-stu-id="fc222-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc222-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc222-146">Minimum supported client</span></span><br/> | <span data-ttu-id="fc222-147">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fc222-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fc222-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc222-148">Minimum supported server</span></span><br/> | <span data-ttu-id="fc222-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc222-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc222-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc222-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc222-151">**UdpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="fc222-151">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> <dt>

[<span data-ttu-id="fc222-152">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="fc222-152">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




