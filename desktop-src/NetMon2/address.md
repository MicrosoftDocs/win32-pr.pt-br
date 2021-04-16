---
description: É obsoleto e não deve ser usado.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: Estrutura de endereço (Netmon. h)
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
ms.openlocfilehash: c577758401bede53c79fd109caa6d8b9cb3d9163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750792"
---
# <a name="address-structure"></a><span data-ttu-id="06c7d-103">Estrutura de endereço</span><span class="sxs-lookup"><span data-stu-id="06c7d-103">ADDRESS structure</span></span>

<span data-ttu-id="06c7d-104">A estrutura de **endereço** está obsoleta e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="06c7d-104">The **ADDRESS** structure is obsolete and should not be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c7d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06c7d-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
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



## <a name="members"></a><span data-ttu-id="06c7d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="06c7d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="06c7d-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="06c7d-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-108">Tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="06c7d-108">Address type.</span></span> <span data-ttu-id="06c7d-109">Pode conter um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="06c7d-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="06c7d-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="06c7d-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="06c7d-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="06c7d-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="06c7d-112">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="06c7d-112">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="06c7d-113">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="06c7d-113">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="06c7d-114">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="06c7d-114">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="06c7d-115">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="06c7d-115">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="06c7d-116">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="06c7d-116">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="06c7d-117">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="06c7d-117">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="06c7d-118">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="06c7d-118">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="06c7d-119">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="06c7d-119">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="06c7d-120">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="06c7d-120">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="06c7d-121">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="06c7d-121">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="06c7d-122">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="06c7d-122">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="06c7d-123">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="06c7d-123">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-124">Exibição dos dados expressos como um endereço MAC bruto.</span><span class="sxs-lookup"><span data-stu-id="06c7d-124">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-125">**EndereçoIP**</span><span class="sxs-lookup"><span data-stu-id="06c7d-125">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-126">Exibição dos dados expressos como um endereço IP bruto.</span><span class="sxs-lookup"><span data-stu-id="06c7d-126">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-127">**IPXRawAddress**</span><span class="sxs-lookup"><span data-stu-id="06c7d-127">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-128">Exibição dos dados expressos como um Endereço IPX bruto.</span><span class="sxs-lookup"><span data-stu-id="06c7d-128">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-129">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="06c7d-129">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-130">Exibição dos dados expressos como um valor de Endereço IPX decodificado.</span><span class="sxs-lookup"><span data-stu-id="06c7d-130">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-131">**VinesIPRawAddress**</span><span class="sxs-lookup"><span data-stu-id="06c7d-131">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-132">Exibição dos dados expressos como um endereço IP de Vines brutos.</span><span class="sxs-lookup"><span data-stu-id="06c7d-132">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-133">**VinesIPAddress**</span><span class="sxs-lookup"><span data-stu-id="06c7d-133">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-134">Exibição dos dados expressos como um endereço IP de Vines decodificados.</span><span class="sxs-lookup"><span data-stu-id="06c7d-134">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-135">**EthernetSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="06c7d-135">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-136">Exibição dos dados expressos como um endereço de origem da Ethernet.</span><span class="sxs-lookup"><span data-stu-id="06c7d-136">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-137">**EthernetDstAddress**</span><span class="sxs-lookup"><span data-stu-id="06c7d-137">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-138">Exibição dos dados expressos como um endereço de destino de Ethernet.</span><span class="sxs-lookup"><span data-stu-id="06c7d-138">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-139">**TokenringSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="06c7d-139">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-140">Uma exibição dos dados como um endereço de origem do token ring.</span><span class="sxs-lookup"><span data-stu-id="06c7d-140">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-141">**TokenringDstAddress**</span><span class="sxs-lookup"><span data-stu-id="06c7d-141">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-142">Uma exibição dos dados como um endereço de destino do token ring.</span><span class="sxs-lookup"><span data-stu-id="06c7d-142">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-143">**FddiSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="06c7d-143">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-144">Exibição dos dados expressos como um endereço de origem FDDI.</span><span class="sxs-lookup"><span data-stu-id="06c7d-144">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-145">**FddiDstAddress**</span><span class="sxs-lookup"><span data-stu-id="06c7d-145">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-146">Exibição dos dados expressos como um endereço de destino FDDI.</span><span class="sxs-lookup"><span data-stu-id="06c7d-146">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="06c7d-147">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="06c7d-147">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="06c7d-148">Um conjunto de sinalizadores que modificam as propriedades de endereço.</span><span class="sxs-lookup"><span data-stu-id="06c7d-148">A set of flags that modify the address properties.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06c7d-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06c7d-149">Requirements</span></span>



| <span data-ttu-id="06c7d-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c7d-150">Requirement</span></span> | <span data-ttu-id="06c7d-151">Valor</span><span class="sxs-lookup"><span data-stu-id="06c7d-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="06c7d-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06c7d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="06c7d-153">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06c7d-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="06c7d-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06c7d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="06c7d-155">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06c7d-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="06c7d-156">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="06c7d-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c7d-157"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c7d-157"><dt>Netmon.h</dt></span></span> </dl> |



 

 




