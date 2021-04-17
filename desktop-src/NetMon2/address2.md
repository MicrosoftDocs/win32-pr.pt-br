---
description: Contém um único endereço de qualquer tipo de endereços com suporte.
ms.assetid: 3f840842-8992-4fab-8820-cbbfc63242b8
title: ENDEREÇO2 estrutura (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a8d66548aa683abf82b795d6a47e93fbdc03e08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780500"
---
# <a name="address2-structure"></a><span data-ttu-id="525ed-103">ENDEREÇO2 estrutura</span><span class="sxs-lookup"><span data-stu-id="525ed-103">ADDRESS2 structure</span></span>

<span data-ttu-id="525ed-104">A estrutura de **endereço** contém um único endereço de qualquer tipo de endereços com suporte.</span><span class="sxs-lookup"><span data-stu-id="525ed-104">The **ADDRESS** structure contains a single address of any type of supported addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="525ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="525ed-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IP6Address[IP6_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a><span data-ttu-id="525ed-106">Membros</span><span class="sxs-lookup"><span data-stu-id="525ed-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="525ed-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="525ed-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-108">Tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="525ed-108">Address type.</span></span> <span data-ttu-id="525ed-109">Pode conter um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="525ed-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="525ed-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="525ed-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="525ed-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="525ed-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="525ed-112">ADDRESS_TYPE_IP6</span><span class="sxs-lookup"><span data-stu-id="525ed-112">ADDRESS_TYPE_IP6</span></span></dd> <dd><span data-ttu-id="525ed-113">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="525ed-113">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="525ed-114">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="525ed-114">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="525ed-115">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="525ed-115">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="525ed-116">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="525ed-116">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="525ed-117">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="525ed-117">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="525ed-118">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="525ed-118">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="525ed-119">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="525ed-119">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="525ed-120">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="525ed-120">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="525ed-121">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="525ed-121">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="525ed-122">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="525ed-122">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="525ed-123">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="525ed-123">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="525ed-124">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="525ed-124">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-125">Exibição dos dados expressos como um endereço MAC bruto.</span><span class="sxs-lookup"><span data-stu-id="525ed-125">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-126">**EndereçoIP**</span><span class="sxs-lookup"><span data-stu-id="525ed-126">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-127">Exibição dos dados expressos como um endereço IP bruto.</span><span class="sxs-lookup"><span data-stu-id="525ed-127">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-128">**IP6Address**</span><span class="sxs-lookup"><span data-stu-id="525ed-128">**IP6Address**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-129">Exibição dos dados expressos como um endereço IP bruto versão 6.</span><span class="sxs-lookup"><span data-stu-id="525ed-129">View of the data expressed as a raw IP version 6 address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-130">**IPXRawAddress**</span><span class="sxs-lookup"><span data-stu-id="525ed-130">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-131">Exibição dos dados expressos como um Endereço IPX bruto.</span><span class="sxs-lookup"><span data-stu-id="525ed-131">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-132">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="525ed-132">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-133">Exibição dos dados expressos como um valor de Endereço IPX decodificado.</span><span class="sxs-lookup"><span data-stu-id="525ed-133">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-134">**VinesIPRawAddress**</span><span class="sxs-lookup"><span data-stu-id="525ed-134">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-135">Exibição dos dados expressos como um endereço IP de Vines brutos.</span><span class="sxs-lookup"><span data-stu-id="525ed-135">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-136">**VinesIPAddress**</span><span class="sxs-lookup"><span data-stu-id="525ed-136">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-137">Exibição dos dados expressos como um endereço IP de Vines decodificados.</span><span class="sxs-lookup"><span data-stu-id="525ed-137">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-138">**EthernetSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="525ed-138">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-139">Exibição dos dados expressos como um endereço de origem da Ethernet.</span><span class="sxs-lookup"><span data-stu-id="525ed-139">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-140">**EthernetDstAddress**</span><span class="sxs-lookup"><span data-stu-id="525ed-140">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-141">Exibição dos dados expressos como um endereço de destino de Ethernet.</span><span class="sxs-lookup"><span data-stu-id="525ed-141">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-142">**TokenringSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="525ed-142">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-143">Uma exibição dos dados como um endereço de origem do token ring.</span><span class="sxs-lookup"><span data-stu-id="525ed-143">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-144">**TokenringDstAddress**</span><span class="sxs-lookup"><span data-stu-id="525ed-144">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-145">Uma exibição dos dados como um endereço de destino do token ring.</span><span class="sxs-lookup"><span data-stu-id="525ed-145">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-146">**FddiSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="525ed-146">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-147">Exibição dos dados expressos como um endereço de origem FDDI.</span><span class="sxs-lookup"><span data-stu-id="525ed-147">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-148">**FddiDstAddress**</span><span class="sxs-lookup"><span data-stu-id="525ed-148">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="525ed-149">Exibição dos dados expressos como um endereço de destino FDDI.</span><span class="sxs-lookup"><span data-stu-id="525ed-149">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="525ed-150">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="525ed-150">**Flags**</span></span>
<span data-ttu-id="525ed-151"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="525ed-151"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="525ed-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="525ed-152">Requirements</span></span>



| <span data-ttu-id="525ed-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="525ed-153">Requirement</span></span> | <span data-ttu-id="525ed-154">Valor</span><span class="sxs-lookup"><span data-stu-id="525ed-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="525ed-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="525ed-155">Minimum supported client</span></span><br/> | <span data-ttu-id="525ed-156">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="525ed-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="525ed-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="525ed-157">Minimum supported server</span></span><br/> | <span data-ttu-id="525ed-158">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="525ed-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="525ed-159">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="525ed-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="525ed-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="525ed-160"><dt>Netmon.h</dt></span></span> </dl> |



 

 




