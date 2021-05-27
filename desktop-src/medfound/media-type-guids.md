---
description: Principais tipos de mídia
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Principais tipos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56553ac635f0e767e43e057b2a468027dcefb730
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549571"
---
# <a name="major-media-types"></a><span data-ttu-id="d3585-103">Principais tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="d3585-103">Major Media Types</span></span>

<span data-ttu-id="d3585-104">Em um tipo de mídia, *o tipo principal* descreve a categoria geral dos dados, como áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="d3585-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="d3585-105">O *subtipo*, se presente, refina ainda mais o tipo principal.</span><span class="sxs-lookup"><span data-stu-id="d3585-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="d3585-106">Por exemplo, se o tipo principal for vídeo, o subtipo poderá ser um vídeo RGB de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d3585-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="d3585-107">Os subtipos também distinguem formatos codificados, como vídeo H.264, de formatos descompactados.</span><span class="sxs-lookup"><span data-stu-id="d3585-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="d3585-108">O tipo principal e o subtipo são identificados por GUIDs e armazenados nos seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="d3585-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="d3585-109">Atributo</span><span class="sxs-lookup"><span data-stu-id="d3585-109">Attribute</span></span>                                             | <span data-ttu-id="d3585-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3585-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="d3585-111">MF \_ MT \_ MAJOR \_ TYPE</span><span class="sxs-lookup"><span data-stu-id="d3585-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="d3585-112">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="d3585-112">Major type.</span></span> |
| [<span data-ttu-id="d3585-113">SUBTIPO \_ MF MT \_</span><span class="sxs-lookup"><span data-stu-id="d3585-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="d3585-114">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="d3585-114">Subtype.</span></span>    |



 

<span data-ttu-id="d3585-115">Os seguintes tipos principais são definidos.</span><span class="sxs-lookup"><span data-stu-id="d3585-115">The following major types are defined.</span></span>



| <span data-ttu-id="d3585-116">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="d3585-116">Major Type</span></span>                    | <span data-ttu-id="d3585-117">Description</span><span class="sxs-lookup"><span data-stu-id="d3585-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="d3585-118">Subtipos</span><span class="sxs-lookup"><span data-stu-id="d3585-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d3585-119">**Áudio MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="d3585-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="d3585-120">Áudio.</span><span class="sxs-lookup"><span data-stu-id="d3585-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="d3585-121">[GUIDs de subtipo de áudio.](audio-subtype-guids.md)</span><span class="sxs-lookup"><span data-stu-id="d3585-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="d3585-122">**Binário MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="d3585-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="d3585-123">Fluxo binário.</span><span class="sxs-lookup"><span data-stu-id="d3585-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="d3585-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d3585-124">None.</span></span>                                                |
| <span data-ttu-id="d3585-125">**Arquivo \_ MFMediaTypeTransfer**</span><span class="sxs-lookup"><span data-stu-id="d3585-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="d3585-126">Um fluxo que contém arquivos de dados.</span><span class="sxs-lookup"><span data-stu-id="d3585-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="d3585-127">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d3585-127">None.</span></span>                                                |
| <span data-ttu-id="d3585-128">**\_HTML MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d3585-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="d3585-129">Fluxo de HTML.</span><span class="sxs-lookup"><span data-stu-id="d3585-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="d3585-130">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d3585-130">None.</span></span>                                                |
| <span data-ttu-id="d3585-131">**\_Imagem MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d3585-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="d3585-132">Fluxo de imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="d3585-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="d3585-133">[GUIDs e CLSIDs do WIC](../wic/-wic-guids-clsids.md).</span><span class="sxs-lookup"><span data-stu-id="d3585-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="d3585-134">**Metadados do MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="d3585-134">**MFMediaType\_Metadata**</span></span>        | <span data-ttu-id="d3585-135">Fluxo de metadados.</span><span class="sxs-lookup"><span data-stu-id="d3585-135">Metadata stream.</span></span>                                                                                                                                        | <span data-ttu-id="d3585-136">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d3585-136">None.</span></span>       |
| <span data-ttu-id="d3585-137">**MFMediaType \_ protegido**</span><span class="sxs-lookup"><span data-stu-id="d3585-137">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="d3585-138">Mídia protegida.</span><span class="sxs-lookup"><span data-stu-id="d3585-138">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="d3585-139">O subtipo especifica o esquema de proteção de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d3585-139">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="d3585-140">**Percepção de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="d3585-140">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="d3585-141">Transmite de um sensor de câmera ou unidade de processamento por razões e compreende dados brutos de vídeo e fornece compreensão do ambiente ou dos seres humanos.</span><span class="sxs-lookup"><span data-stu-id="d3585-141">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="d3585-142">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d3585-142">None.</span></span>                                                |
| <span data-ttu-id="d3585-143">**Sami de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="d3585-143">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="d3585-144">Legendas de SAMI (intercâmbio de mídia acessível) sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="d3585-144">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="d3585-145">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d3585-145">None.</span></span>                                                |
| <span data-ttu-id="d3585-146">**\_Script MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d3585-146">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="d3585-147">Fluxo de script.</span><span class="sxs-lookup"><span data-stu-id="d3585-147">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="d3585-148">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d3585-148">None.</span></span>                                                |
| <span data-ttu-id="d3585-149">**Fluxo de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="d3585-149">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="d3585-150">Fluxo multiplexado ou fluxo elementar.</span><span class="sxs-lookup"><span data-stu-id="d3585-150">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="d3585-151">GUIDs de subtipo de fluxo</span><span class="sxs-lookup"><span data-stu-id="d3585-151">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="d3585-152">**Vídeo MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="d3585-152">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="d3585-153">Vídeo.</span><span class="sxs-lookup"><span data-stu-id="d3585-153">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="d3585-154">[GUIDs de subtipo de vídeo.](video-subtype-guids.md)</span><span class="sxs-lookup"><span data-stu-id="d3585-154">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="d3585-155">Componentes de terceiros podem definir novos tipos principais e novos subtipos.</span><span class="sxs-lookup"><span data-stu-id="d3585-155">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3585-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3585-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3585-157">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d3585-157">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="d3585-158">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="d3585-158">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
