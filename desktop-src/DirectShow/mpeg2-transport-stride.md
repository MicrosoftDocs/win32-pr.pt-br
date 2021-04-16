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
ms.openlocfilehash: 4a0cdc21bdd8c320728da0c0af8c0af023de68eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779325"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="7457e-103">\_Estrutura Stride de transporte MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="7457e-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="7457e-104">A `MPEG2_TRANSPORT_STRIDE` estrutura descreve o formato dos pacotes de transmissão de transporte MPEG-2 (TS).</span><span class="sxs-lookup"><span data-stu-id="7457e-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="7457e-105">Essa estrutura permite Transportações para fluxos nos quais os pacotes de transporte de 188 bytes não são contíguos.</span><span class="sxs-lookup"><span data-stu-id="7457e-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="7457e-106">Para a finalidade desta documentação, esses pacotes são chamados de *pacotes Stride*.</span><span class="sxs-lookup"><span data-stu-id="7457e-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="7457e-107">Os pacotes Stride são identificados pelo seguinte tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="7457e-107">Stride packets are identified by the following media type:</span></span>



|             |                                        |
|-------------|----------------------------------------|
| <span data-ttu-id="7457e-108">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="7457e-108">Major Type</span></span>  | <span data-ttu-id="7457e-109">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="7457e-109">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="7457e-110">Subtype</span><span class="sxs-lookup"><span data-stu-id="7457e-110">Subtype</span></span>     | <span data-ttu-id="7457e-111">\_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="7457e-111">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="7457e-112">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="7457e-112">Format Type</span></span> | <span data-ttu-id="7457e-113">Formatar \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="7457e-113">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="7457e-114">O bloco de formato (**pbFormat**) é opcional.</span><span class="sxs-lookup"><span data-stu-id="7457e-114">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="7457e-115">Se o bloco de formato for incluído, ele deverá começar com uma estrutura **\_ \_ Stride de transporte MPEG2** .</span><span class="sxs-lookup"><span data-stu-id="7457e-115">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="7457e-116">Essa estrutura define o layout do pacote de transporte dentro do pacote Stride.</span><span class="sxs-lookup"><span data-stu-id="7457e-116">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="7457e-117">Se o bloco de formato for **nulo**, os pacotes serão considerados para usar um conjunto de valores padrão; consulte a seção comentários para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="7457e-117">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="7457e-118">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7457e-118">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="7457e-119">Membros</span><span class="sxs-lookup"><span data-stu-id="7457e-119">Members</span></span>

<dl> <dt>

<span data-ttu-id="7457e-120">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="7457e-120">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7457e-121">Especifica o deslocamento, em bytes, desde o início do pacote até o primeiro byte do pacote de transporte inserido.</span><span class="sxs-lookup"><span data-stu-id="7457e-121">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="7457e-122">O valor deve variar de zero a `(dwStride - dwPacketLength)` , inclusive.</span><span class="sxs-lookup"><span data-stu-id="7457e-122">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="7457e-123">**dwPacketLength**</span><span class="sxs-lookup"><span data-stu-id="7457e-123">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="7457e-124">Especifica o comprimento do pacote de transporte inserido, em bytes.</span><span class="sxs-lookup"><span data-stu-id="7457e-124">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="7457e-125">Para pacotes de transporte MPEG-2 padrão, o valor deve ser 188 bytes.</span><span class="sxs-lookup"><span data-stu-id="7457e-125">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7457e-126">**dwStride**</span><span class="sxs-lookup"><span data-stu-id="7457e-126">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="7457e-127">Especifica o comprimento de todo o pacote Stride, em bytes.</span><span class="sxs-lookup"><span data-stu-id="7457e-127">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="7457e-128">O valor deve ser pelo menos `(dwOffset + dwPacketLength)` .</span><span class="sxs-lookup"><span data-stu-id="7457e-128">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7457e-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="7457e-129">Remarks</span></span>

<span data-ttu-id="7457e-130">O diagrama a seguir ilustra as relações entre os membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="7457e-130">The following diagram illustrates the relations between the structure members.</span></span>

![pacote de Stride MPEG-2](images/mpeg2-stride-packet.png)

<span data-ttu-id="7457e-132">Os buffers de entrada que contêm pacotes Stride multiplexados têm algumas restrições:</span><span class="sxs-lookup"><span data-stu-id="7457e-132">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="7457e-133">Os pacotes Stride devem ser empacotados de forma contígua no buffer.</span><span class="sxs-lookup"><span data-stu-id="7457e-133">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="7457e-134">Nenhum byte pode preceder o primeiro pacote Stride ou seguir o último pacote Stride.</span><span class="sxs-lookup"><span data-stu-id="7457e-134">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="7457e-135">Um número integral de pacotes Stride deve caber no buffer; ou seja, o comprimento do buffer% dwStride é igual a zero.</span><span class="sxs-lookup"><span data-stu-id="7457e-135">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="7457e-136">Não há nenhuma restrição quanto ao número de pacotes Stride por buffer.</span><span class="sxs-lookup"><span data-stu-id="7457e-136">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="7457e-137">Se o tipo de mídia não contiver um bloco de formato (**pbFormat** é **nulo**), os seguintes valores padrão serão usados:</span><span class="sxs-lookup"><span data-stu-id="7457e-137">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="7457e-138">**dwOffset**: 0</span><span class="sxs-lookup"><span data-stu-id="7457e-138">**dwOffset**: 0</span></span>
-   <span data-ttu-id="7457e-139">**dwPacketLength**: 188</span><span class="sxs-lookup"><span data-stu-id="7457e-139">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="7457e-140">**dwStride**: 188</span><span class="sxs-lookup"><span data-stu-id="7457e-140">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="7457e-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7457e-141">Requirements</span></span>



| <span data-ttu-id="7457e-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="7457e-142">Requirement</span></span> | <span data-ttu-id="7457e-143">Valor</span><span class="sxs-lookup"><span data-stu-id="7457e-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7457e-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7457e-144">Header</span></span><br/> | <dl> <span data-ttu-id="7457e-145"><dt>Bdatypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="7457e-145"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7457e-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="7457e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7457e-147">Estruturas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="7457e-147">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="7457e-148">Tipos de mídia MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7457e-148">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




