---
description: Descreve o conteúdo de um fluxo elementar dentro de um fluxo de transporte MPEG-2. Essa enumeração é usada na interface IMPEG2PIDMap, que é implementada nos pinos de saída do demultiplexador MPEG-2.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: Enumeração de MEDIA_SAMPLE_CONTENT (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SAMPLE_CONTENT
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 9065f2af948ff28d181b24842673b086882837bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757009"
---
# <a name="media_sample_content-enumeration"></a><span data-ttu-id="2262d-104">Enumeração de conteúdo de \_ exemplo de mídia \_</span><span class="sxs-lookup"><span data-stu-id="2262d-104">MEDIA\_SAMPLE\_CONTENT enumeration</span></span>

<span data-ttu-id="2262d-105">Descreve o conteúdo de um fluxo elementar dentro de um fluxo de transporte MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="2262d-105">Describes the contents of an elementary stream within an MPEG-2 transport stream.</span></span> <span data-ttu-id="2262d-106">Essa enumeração é usada na interface [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) , que é implementada nos pinos de saída do [demultiplexador MPEG-2](mpeg-2-demultiplexer.md).</span><span class="sxs-lookup"><span data-stu-id="2262d-106">This enumeration is used in the [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) interface, which is implemented on the output pins of the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2262d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2262d-107">Syntax</span></span>


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a><span data-ttu-id="2262d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="2262d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2262d-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**\_pacote de transporte de mídia \_**</span><span class="sxs-lookup"><span data-stu-id="2262d-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**MEDIA\_TRANSPORT\_PACKET**</span></span>
</dt> <dd>

<span data-ttu-id="2262d-110">Especifica um pacote de fluxo de transporte completo a ser passado sem processamento.</span><span class="sxs-lookup"><span data-stu-id="2262d-110">Specifies a complete transport stream packet to be passed through without processing.</span></span>

</dd> <dt>

<span data-ttu-id="2262d-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**\_fluxo elementar mídia \_**</span><span class="sxs-lookup"><span data-stu-id="2262d-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**MEDIA\_ELEMENTARY\_STREAM**</span></span>
</dt> <dd>

<span data-ttu-id="2262d-112">Especifica uma carga de áudio/vídeo PES.</span><span class="sxs-lookup"><span data-stu-id="2262d-112">Specifies an audio or video PES payload.</span></span>

</dd> <dt>

<span data-ttu-id="2262d-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MPEG2 de mídia \_ \_ psi**</span><span class="sxs-lookup"><span data-stu-id="2262d-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA\_MPEG2\_PSI**</span></span>
</dt> <dd>

<span data-ttu-id="2262d-114">Especifica um fluxo de dados PAT, pgto, CAT ou Private.</span><span class="sxs-lookup"><span data-stu-id="2262d-114">Specifies a PAT, PMT, CAT, or Private data stream.</span></span> <span data-ttu-id="2262d-115">Essas são seções completas do PSI que não precisam ser remontadas.</span><span class="sxs-lookup"><span data-stu-id="2262d-115">These are complete PSI sections which do not need to be reassembled.</span></span>

</dd> <dt>

<span data-ttu-id="2262d-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**\_carga de transporte de mídia \_**</span><span class="sxs-lookup"><span data-stu-id="2262d-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**MEDIA\_TRANSPORT\_PAYLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="2262d-117">Especifica cargas de pacotes TS coletadas, como pacotes PES.</span><span class="sxs-lookup"><span data-stu-id="2262d-117">Specifies gathered TS packet payloads, such as PES packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2262d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2262d-118">Requirements</span></span>



| <span data-ttu-id="2262d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2262d-119">Requirement</span></span> | <span data-ttu-id="2262d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2262d-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2262d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2262d-121">Header</span></span><br/> | <dl> <span data-ttu-id="2262d-122"><dt>Bdatypes. h (incluir Bdaiface. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2262d-122"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2262d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2262d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2262d-124">Tipos enumerados do DirectShow</span><span class="sxs-lookup"><span data-stu-id="2262d-124">DirectShow Enumerated Types</span></span>](directshow-enumerated-types.md)
</dt> </dl>

 

 




