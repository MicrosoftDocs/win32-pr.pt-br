---
description: A \_ estrutura Stride de transporte do MPEG2 \_ descreve o formato dos pacotes TS-2 Transport Stream.
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: Estrutura de MPEG2_TRANSPORT_STRIDE (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 5153f6f79c2807634149222a126a7256a65ffe8a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908484"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="44eb6-103">\_Estrutura Stride de transporte MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="44eb6-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="44eb6-104">A `MPEG2_TRANSPORT_STRIDE` estrutura descreve o formato dos pacotes de transmissão de transporte MPEG-2 (TS).</span><span class="sxs-lookup"><span data-stu-id="44eb6-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="44eb6-105">Essa estrutura permite Transportações para fluxos nos quais os pacotes de transporte de 188 bytes não são contíguos.</span><span class="sxs-lookup"><span data-stu-id="44eb6-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="44eb6-106">Para a finalidade desta documentação, esses pacotes são chamados de *pacotes Stride*.</span><span class="sxs-lookup"><span data-stu-id="44eb6-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="44eb6-107">Os pacotes Stride são identificados pelo seguinte tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="44eb6-107">Stride packets are identified by the following media type:</span></span>



| <span data-ttu-id="44eb6-108">Label</span><span class="sxs-lookup"><span data-stu-id="44eb6-108">Label</span></span> | <span data-ttu-id="44eb6-109">Valor</span><span class="sxs-lookup"><span data-stu-id="44eb6-109">Value</span></span> |
|-------------|----------------------------------------|
| <span data-ttu-id="44eb6-110">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="44eb6-110">Major Type</span></span>  | <span data-ttu-id="44eb6-111">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="44eb6-111">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="44eb6-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="44eb6-112">Subtype</span></span>     | <span data-ttu-id="44eb6-113">\_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="44eb6-113">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="44eb6-114">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="44eb6-114">Format Type</span></span> | <span data-ttu-id="44eb6-115">Formatar \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="44eb6-115">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="44eb6-116">O bloco de formato (**pbFormat**) é opcional.</span><span class="sxs-lookup"><span data-stu-id="44eb6-116">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="44eb6-117">Se o bloco de formato for incluído, ele deverá começar com uma estrutura **\_ \_ Stride de transporte MPEG2** .</span><span class="sxs-lookup"><span data-stu-id="44eb6-117">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="44eb6-118">Essa estrutura define o layout do pacote de transporte dentro do pacote Stride.</span><span class="sxs-lookup"><span data-stu-id="44eb6-118">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="44eb6-119">Se o bloco de formato for **nulo**, os pacotes serão considerados para usar um conjunto de valores padrão; consulte a seção comentários para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="44eb6-119">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="44eb6-120">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44eb6-120">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="44eb6-121">Membros</span><span class="sxs-lookup"><span data-stu-id="44eb6-121">Members</span></span>

<dl> <dt>

<span data-ttu-id="44eb6-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="44eb6-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="44eb6-123">Especifica o deslocamento, em bytes, desde o início do pacote até o primeiro byte do pacote de transporte inserido.</span><span class="sxs-lookup"><span data-stu-id="44eb6-123">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="44eb6-124">O valor deve variar de zero a `(dwStride - dwPacketLength)` , inclusive.</span><span class="sxs-lookup"><span data-stu-id="44eb6-124">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="44eb6-125">**dwPacketLength**</span><span class="sxs-lookup"><span data-stu-id="44eb6-125">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="44eb6-126">Especifica o comprimento do pacote de transporte inserido, em bytes.</span><span class="sxs-lookup"><span data-stu-id="44eb6-126">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="44eb6-127">Para pacotes de transporte MPEG-2 padrão, o valor deve ser 188 bytes.</span><span class="sxs-lookup"><span data-stu-id="44eb6-127">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="44eb6-128">**dwStride**</span><span class="sxs-lookup"><span data-stu-id="44eb6-128">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="44eb6-129">Especifica o comprimento de todo o pacote Stride, em bytes.</span><span class="sxs-lookup"><span data-stu-id="44eb6-129">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="44eb6-130">O valor deve ser pelo menos `(dwOffset + dwPacketLength)` .</span><span class="sxs-lookup"><span data-stu-id="44eb6-130">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44eb6-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="44eb6-131">Remarks</span></span>

<span data-ttu-id="44eb6-132">O diagrama a seguir ilustra as relações entre os membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="44eb6-132">The following diagram illustrates the relations between the structure members.</span></span>

![pacote de Stride MPEG-2](images/mpeg2-stride-packet.png)

<span data-ttu-id="44eb6-134">Os buffers de entrada que contêm pacotes Stride multiplexados têm algumas restrições:</span><span class="sxs-lookup"><span data-stu-id="44eb6-134">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="44eb6-135">Os pacotes Stride devem ser empacotados de forma contígua no buffer.</span><span class="sxs-lookup"><span data-stu-id="44eb6-135">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="44eb6-136">Nenhum byte pode preceder o primeiro pacote Stride ou seguir o último pacote Stride.</span><span class="sxs-lookup"><span data-stu-id="44eb6-136">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="44eb6-137">Um número integral de pacotes Stride deve caber no buffer; ou seja, o comprimento do buffer% dwStride é igual a zero.</span><span class="sxs-lookup"><span data-stu-id="44eb6-137">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="44eb6-138">Não há nenhuma restrição quanto ao número de pacotes Stride por buffer.</span><span class="sxs-lookup"><span data-stu-id="44eb6-138">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="44eb6-139">Se o tipo de mídia não contiver um bloco de formato (**pbFormat** é **nulo**), os seguintes valores padrão serão usados:</span><span class="sxs-lookup"><span data-stu-id="44eb6-139">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="44eb6-140">**dwOffset**: 0</span><span class="sxs-lookup"><span data-stu-id="44eb6-140">**dwOffset**: 0</span></span>
-   <span data-ttu-id="44eb6-141">**dwPacketLength**: 188</span><span class="sxs-lookup"><span data-stu-id="44eb6-141">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="44eb6-142">**dwStride**: 188</span><span class="sxs-lookup"><span data-stu-id="44eb6-142">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="44eb6-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44eb6-143">Requirements</span></span>



| <span data-ttu-id="44eb6-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="44eb6-144">Requirement</span></span> | <span data-ttu-id="44eb6-145">Valor</span><span class="sxs-lookup"><span data-stu-id="44eb6-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44eb6-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44eb6-146">Header</span></span><br/> | <dl> <span data-ttu-id="44eb6-147"><dt>Bdatypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="44eb6-147"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44eb6-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="44eb6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44eb6-149">Estruturas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="44eb6-149">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="44eb6-150">Tipos de mídia MPEG-2</span><span class="sxs-lookup"><span data-stu-id="44eb6-150">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




