---
description: O filtro de codificador AC-3 Microsoft codifica áudio PCM estéreo para um Dolby Digital fragmentado.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Codificador AC-3 da Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087605"
---
# <a name="microsoft-ac-3-encoder"></a><span data-ttu-id="eaf83-103">Codificador AC-3 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="eaf83-103">Microsoft AC-3 Encoder</span></span>

<span data-ttu-id="eaf83-104">O filtro de codificador AC-3 Microsoft codifica áudio PCM estéreo para um Dolby Digital fragmentado.</span><span class="sxs-lookup"><span data-stu-id="eaf83-104">The Microsoft AC-3 Encoder filter encodes stereo PCM audio to a Dolby Digital bitstream.</span></span>

> [!Note]  
> <span data-ttu-id="eaf83-105">A implementação da tecnologia Dolby Digital da Microsoft é restrita em termos do programa de licenciamento do Dolby Digital para uso pelos aplicativos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eaf83-105">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="eaf83-106">Não há suporte para esse filtro em plataformas baseadas em IA-64.</span><span class="sxs-lookup"><span data-stu-id="eaf83-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="eaf83-107">Informações de filtro</span><span class="sxs-lookup"><span data-stu-id="eaf83-107">Filter Information</span></span>

<span data-ttu-id="eaf83-108">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="eaf83-108">Filter Interfaces</span></span>

[<span data-ttu-id="eaf83-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="eaf83-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

<span data-ttu-id="eaf83-110">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="eaf83-110">Input Pin Media Types</span></span>

<span data-ttu-id="eaf83-111">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="eaf83-111">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span><br/> <span data-ttu-id="eaf83-112">O tipo de entrada deve ser estéreo de 48-kHz, 16 bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="eaf83-112">The input type must be 48-kHz stereo, 16 bits per sample.</span></span><br/>

<span data-ttu-id="eaf83-113">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="eaf83-113">Input Pin Interfaces</span></span>

[<span data-ttu-id="eaf83-114">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="eaf83-114">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="eaf83-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="eaf83-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="eaf83-116">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="eaf83-116">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="eaf83-117">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="eaf83-117">Output Pin Media Types</span></span>

<span data-ttu-id="eaf83-118">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="eaf83-118">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/> <span data-ttu-id="eaf83-119">**MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="eaf83-119">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/>

<span data-ttu-id="eaf83-120">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="eaf83-120">Output Pin Interfaces</span></span>

[<span data-ttu-id="eaf83-121">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="eaf83-121">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="eaf83-122">**IPin**</span><span class="sxs-lookup"><span data-stu-id="eaf83-122">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="eaf83-123">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="eaf83-123">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="eaf83-124">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="eaf83-124">Filter CLSID</span></span>

<span data-ttu-id="eaf83-125">**CLSID \_ do CMSAC3Enc** (declarado em wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="eaf83-125">**CLSID\_CMSAC3Enc** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="eaf83-126">Executável</span><span class="sxs-lookup"><span data-stu-id="eaf83-126">Executable</span></span>

<span data-ttu-id="eaf83-127">msac3enc.dll</span><span class="sxs-lookup"><span data-stu-id="eaf83-127">msac3enc.dll</span></span>

[<span data-ttu-id="eaf83-128">Núcleo</span><span class="sxs-lookup"><span data-stu-id="eaf83-128">Merit</span></span>](merit.md)

<span data-ttu-id="eaf83-129">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="eaf83-129">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="eaf83-130">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="eaf83-130">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="eaf83-131">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="eaf83-131">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="eaf83-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="eaf83-132">Remarks</span></span>

<span data-ttu-id="eaf83-133">Esse filtro não está disponível para uso por aplicativos de terceiros.</span><span class="sxs-lookup"><span data-stu-id="eaf83-133">This filter is not available for use by third-party applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf83-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaf83-134">Requirements</span></span>



| <span data-ttu-id="eaf83-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaf83-135">Requirement</span></span> | <span data-ttu-id="eaf83-136">Valor</span><span class="sxs-lookup"><span data-stu-id="eaf83-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf83-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaf83-137">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf83-138">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="eaf83-138">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="eaf83-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaf83-139">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf83-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eaf83-140">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="eaf83-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eaf83-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaf83-142"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaf83-142"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="eaf83-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="eaf83-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf83-144">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="eaf83-144">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




