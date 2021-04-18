---
description: Para vários GUIDs de tipo de mídia MPEG-2, o DDK do Windows define nomes que diferem dos nomes usados no DirectShow. A tabela a seguir mostra os nomes do DirectShow (definidos em Ksuuids. h) e os nomes do modo kernel correspondentes (definidos em Ksmedia. h).
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: Tipos de mídia do kernel MPEG-2 (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b03e6d3cbc32c987110ceac98e6aeef6617d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813085"
---
# <a name="mpeg-2-kernel-media-types"></a><span data-ttu-id="da22a-104">Tipos de mídia de kernel MPEG-2</span><span class="sxs-lookup"><span data-stu-id="da22a-104">MPEG-2 Kernel Media Types</span></span>

<span data-ttu-id="da22a-105">Para vários GUIDs de tipo de mídia MPEG-2, o DDK do Windows define nomes que diferem dos nomes usados no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="da22a-105">For several MPEG-2 media type GUIDs, the Windows DDK defines names that differ from the names used in DirectShow.</span></span> <span data-ttu-id="da22a-106">A tabela a seguir mostra os nomes do DirectShow (definidos em Ksuuids. h) e os nomes do modo kernel correspondentes (definidos em Ksmedia. h).</span><span class="sxs-lookup"><span data-stu-id="da22a-106">The following table shows the DirectShow names (defined in Ksuuids.h) and the corresponding kernel-mode names (defined in Ksmedia.h).</span></span>



| <span data-ttu-id="da22a-107">Nome em Ksuuids. h</span><span class="sxs-lookup"><span data-stu-id="da22a-107">Name in Ksuuids.h</span></span>              | <span data-ttu-id="da22a-108">Nome em Ksmedia. h</span><span class="sxs-lookup"><span data-stu-id="da22a-108">Name in Ksmedia.h</span></span>                          |
|--------------------------------|--------------------------------------------|
| <span data-ttu-id="da22a-109">WaveFormatEx de formato \_</span><span class="sxs-lookup"><span data-stu-id="da22a-109">FORMAT\_WaveFormatEx</span></span>           | <span data-ttu-id="da22a-110">\_WAVEFORMATEX especificador KSDATAFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="da22a-110">KSDATAFORMAT\_SPECIFIER\_WAVEFORMATEX</span></span>      |
| <span data-ttu-id="da22a-111">MPEG2Video de formato \_</span><span class="sxs-lookup"><span data-stu-id="da22a-111">FORMAT\_MPEG2Video</span></span>             | <span data-ttu-id="da22a-112">\_Vídeo MPEG2 do especificador KSDATAFORMAT \_ \_</span><span class="sxs-lookup"><span data-stu-id="da22a-112">KSDATAFORMAT\_SPECIFIER\_MPEG2\_VIDEO</span></span>      |
| <span data-ttu-id="da22a-113">MEDIASUBTYPE \_ ATSC \_ si</span><span class="sxs-lookup"><span data-stu-id="da22a-113">MEDIASUBTYPE\_ATSC\_SI</span></span>         | <span data-ttu-id="da22a-114">KSDATAFORMAT \_ subtipo \_ ATSC \_ si</span><span class="sxs-lookup"><span data-stu-id="da22a-114">KSDATAFORMAT\_SUBTYPE\_ATSC\_SI</span></span>            |
| <span data-ttu-id="da22a-115">MEDIASUBTYPE \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="da22a-115">MEDIASUBTYPE\_DOLBY\_AC3</span></span>       | <span data-ttu-id="da22a-116">KSDATAFORMAT \_ subtipo \_ AC3 \_ áudio</span><span class="sxs-lookup"><span data-stu-id="da22a-116">KSDATAFORMAT\_SUBTYPE\_AC3\_AUDIO</span></span>          |
| <span data-ttu-id="da22a-117">\_si MEDIASUBTYPE DVB \_</span><span class="sxs-lookup"><span data-stu-id="da22a-117">MEDIASUBTYPE\_DVB\_SI</span></span>          | <span data-ttu-id="da22a-118">KSDATAFORMAT do \_ subtipo \_ DVB \_ si</span><span class="sxs-lookup"><span data-stu-id="da22a-118">KSDATAFORMAT\_SUBTYPE\_DVB\_SI</span></span>             |
| <span data-ttu-id="da22a-119">\_áudio MEDIASUBTYPE DVD \_ LPCM \_</span><span class="sxs-lookup"><span data-stu-id="da22a-119">MEDIASUBTYPE\_DVD\_LPCM\_AUDIO</span></span> | <span data-ttu-id="da22a-120">KSDATAFORMAT \_ subtipo \_ LPCM \_ áudio</span><span class="sxs-lookup"><span data-stu-id="da22a-120">KSDATAFORMAT\_SUBTYPE\_LPCM\_AUDIO</span></span>         |
| <span data-ttu-id="da22a-121">\_Áudio MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="da22a-121">MEDIASUBTYPE\_MPEG2\_AUDIO</span></span>     | <span data-ttu-id="da22a-122">\_Áudio MPEG2 do SUBTIPO KSDATAFORMAT \_ \_</span><span class="sxs-lookup"><span data-stu-id="da22a-122">KSDATAFORMAT\_SUBTYPE\_MPEG2\_AUDIO</span></span>        |
| <span data-ttu-id="da22a-123">\_Programa MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="da22a-123">MEDIASUBTYPE\_MPEG2\_PROGRAM</span></span>   | <span data-ttu-id="da22a-124">\_Programa KSDATAFORMAT estático \_ tipo \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="da22a-124">STATIC\_KSDATAFORMAT\_TYPE\_MPEG2\_PROGRAM</span></span> |
| <span data-ttu-id="da22a-125">\_Transporte MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="da22a-125">MEDIASUBTYPE\_MPEG2\_TRANSPORT</span></span> | <span data-ttu-id="da22a-126">KSDATAFORMAT \_ tipo \_ de \_ transporte MPEG2</span><span class="sxs-lookup"><span data-stu-id="da22a-126">KSDATAFORMAT\_TYPE\_MPEG2\_TRANSPORT</span></span>       |
| <span data-ttu-id="da22a-127">Vídeo do MEDIASUBTYPE \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="da22a-127">MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>     | <span data-ttu-id="da22a-128">Vídeo KSDATAFORMAT do \_ subtipo \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="da22a-128">KSDATAFORMAT\_SUBTYPE\_MPEG2\_VIDEO</span></span>        |
| <span data-ttu-id="da22a-129">Seções de MEDIATYPE \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="da22a-129">MEDIATYPE\_MPEG2\_SECTIONS</span></span>     | <span data-ttu-id="da22a-130">KSDATAFORMAT \_ seções do tipo \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="da22a-130">KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>        |
| <span data-ttu-id="da22a-131">Áudio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="da22a-131">MEDIATYPE\_Audio</span></span>               | <span data-ttu-id="da22a-132">\_áudio do tipo KSDATAFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="da22a-132">KSDATAFORMAT\_TYPE\_AUDIO</span></span>                  |
| <span data-ttu-id="da22a-133">MEDIATYPE \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="da22a-133">MEDIATYPE\_MPEG2\_PES</span></span>          | <span data-ttu-id="da22a-134">KSDATAFORMAT \_ tipo \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="da22a-134">KSDATAFORMAT\_TYPE\_MPEG2\_PES</span></span>             |
| <span data-ttu-id="da22a-135">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="da22a-135">MEDIATYPE\_Video</span></span>               | <span data-ttu-id="da22a-136">\_vídeo do tipo KSDATAFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="da22a-136">KSDATAFORMAT\_TYPE\_VIDEO</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="da22a-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da22a-137">Requirements</span></span>



| <span data-ttu-id="da22a-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="da22a-138">Requirement</span></span> | <span data-ttu-id="da22a-139">Valor</span><span class="sxs-lookup"><span data-stu-id="da22a-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da22a-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da22a-140">Header</span></span><br/> | <dl> <span data-ttu-id="da22a-141"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="da22a-141"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da22a-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="da22a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da22a-143">Tipos de mídia MPEG-2</span><span class="sxs-lookup"><span data-stu-id="da22a-143">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




