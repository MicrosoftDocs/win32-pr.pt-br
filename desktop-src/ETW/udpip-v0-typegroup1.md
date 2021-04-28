---
description: Classe UdpIp_V0_TypeGroup1-essa classe é a classe de tipo de evento para eventos UDP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: Classe UdpIp_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 78243a49e4504fd9e132407feebe98d9b48f7bdd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105494"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="92262-104">\_Classe UdpIp V0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="92262-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="92262-105">Essa classe é a classe de tipo de evento para eventos UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="92262-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="92262-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="92262-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="92262-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92262-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a><span data-ttu-id="92262-108">Membros</span><span class="sxs-lookup"><span data-stu-id="92262-108">Members</span></span>

<span data-ttu-id="92262-109">A classe **UdpIp \_ V0 \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="92262-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="92262-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="92262-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92262-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="92262-111">Properties</span></span>

<span data-ttu-id="92262-112">A classe **UdpIp \_ V0 \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="92262-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92262-113">contexto</span><span class="sxs-lookup"><span data-stu-id="92262-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92262-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92262-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92262-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92262-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92262-116">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="92262-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="92262-117">Identificador de processo para o objeto de endereço que fez ou recebeu a solicitação.</span><span class="sxs-lookup"><span data-stu-id="92262-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="92262-118">daddr</span><span class="sxs-lookup"><span data-stu-id="92262-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92262-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="92262-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="92262-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92262-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92262-121">Qualificadores: WmiDataId (5), extensão ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="92262-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="92262-122">Endereço IP de destino.</span><span class="sxs-lookup"><span data-stu-id="92262-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="92262-123">dport</span><span class="sxs-lookup"><span data-stu-id="92262-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92262-124">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="92262-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="92262-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92262-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92262-126">Qualificadores: WmiDataId (6), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="92262-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="92262-127">Número da porta de destino.</span><span class="sxs-lookup"><span data-stu-id="92262-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="92262-128">dsize</span><span class="sxs-lookup"><span data-stu-id="92262-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92262-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92262-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92262-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92262-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92262-131">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="92262-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="92262-132">Tamanho do pacote de destino.</span><span class="sxs-lookup"><span data-stu-id="92262-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="92262-133">saddr</span><span class="sxs-lookup"><span data-stu-id="92262-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92262-134">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="92262-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="92262-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92262-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92262-136">Qualificadores: WmiDataId (2), extensão ("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="92262-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="92262-137">Endereço IP de origem.</span><span class="sxs-lookup"><span data-stu-id="92262-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="92262-138">tamanho</span><span class="sxs-lookup"><span data-stu-id="92262-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92262-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92262-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92262-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92262-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92262-141">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="92262-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="92262-142">Tamanho do pacote de origem.</span><span class="sxs-lookup"><span data-stu-id="92262-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="92262-143">esporte</span><span class="sxs-lookup"><span data-stu-id="92262-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92262-144">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="92262-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="92262-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92262-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92262-146">Qualificadores: WmiDataId (3), extensão ("porta")</span><span class="sxs-lookup"><span data-stu-id="92262-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="92262-147">Número da porta de origem.</span><span class="sxs-lookup"><span data-stu-id="92262-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92262-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92262-148">Requirements</span></span>



| <span data-ttu-id="92262-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="92262-149">Requirement</span></span> | <span data-ttu-id="92262-150">Valor</span><span class="sxs-lookup"><span data-stu-id="92262-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="92262-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92262-151">Minimum supported client</span></span><br/> | <span data-ttu-id="92262-152">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="92262-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="92262-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92262-153">Minimum supported server</span></span><br/> | <span data-ttu-id="92262-154">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="92262-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="92262-155">Consulte também</span><span class="sxs-lookup"><span data-stu-id="92262-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92262-156">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="92262-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




