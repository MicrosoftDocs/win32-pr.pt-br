---
description: Tipos de mídia principais
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Tipos de mídia principais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a93a1aa430a720ff4b2f3591071d0bc8b178d6a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930182"
---
# <a name="major-media-types"></a><span data-ttu-id="4509f-103">Tipos de mídia principais</span><span class="sxs-lookup"><span data-stu-id="4509f-103">Major Media Types</span></span>

<span data-ttu-id="4509f-104">Em um tipo de mídia, o *tipo principal* descreve a categoria geral dos dados, como áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="4509f-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="4509f-105">O *subtipo*, se presente, refinará o tipo principal.</span><span class="sxs-lookup"><span data-stu-id="4509f-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="4509f-106">Por exemplo, se o tipo principal for vídeo, o subtipo poderá ser um vídeo RGB de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4509f-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="4509f-107">Os subtipos também distinguem os formatos codificados, como o vídeo H. 264, de formatos descompactados.</span><span class="sxs-lookup"><span data-stu-id="4509f-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="4509f-108">O tipo principal e o subtipo são identificados por GUIDs e armazenados nos seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="4509f-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="4509f-109">Atributo</span><span class="sxs-lookup"><span data-stu-id="4509f-109">Attribute</span></span>                                             | <span data-ttu-id="4509f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4509f-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="4509f-111">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="4509f-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="4509f-112">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="4509f-112">Major type.</span></span> |
| [<span data-ttu-id="4509f-113">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="4509f-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="4509f-114">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="4509f-114">Subtype.</span></span>    |



 

<span data-ttu-id="4509f-115">Os seguintes tipos principais são definidos.</span><span class="sxs-lookup"><span data-stu-id="4509f-115">The following major types are defined.</span></span>



| <span data-ttu-id="4509f-116">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="4509f-116">Major Type</span></span>                    | <span data-ttu-id="4509f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="4509f-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="4509f-118">Subtipos</span><span class="sxs-lookup"><span data-stu-id="4509f-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4509f-119">**\_Áudio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4509f-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="4509f-120">Sonoro.</span><span class="sxs-lookup"><span data-stu-id="4509f-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="4509f-121">[GUIDs de subtipo de áudio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="4509f-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="4509f-122">**MFMediaType \_ binário**</span><span class="sxs-lookup"><span data-stu-id="4509f-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="4509f-123">Fluxo binário.</span><span class="sxs-lookup"><span data-stu-id="4509f-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="4509f-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4509f-124">None.</span></span>                                                |
| <span data-ttu-id="4509f-125">**MFMediaType \_ FileTransfer**</span><span class="sxs-lookup"><span data-stu-id="4509f-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="4509f-126">Um fluxo que contém arquivos de dados.</span><span class="sxs-lookup"><span data-stu-id="4509f-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="4509f-127">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4509f-127">None.</span></span>                                                |
| <span data-ttu-id="4509f-128">**\_HTML MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4509f-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="4509f-129">Fluxo de HTML.</span><span class="sxs-lookup"><span data-stu-id="4509f-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="4509f-130">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4509f-130">None.</span></span>                                                |
| <span data-ttu-id="4509f-131">**\_Imagem MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4509f-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="4509f-132">Fluxo de imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="4509f-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="4509f-133">[GUIDs e CLSIDs do WIC](../wic/-wic-guids-clsids.md).</span><span class="sxs-lookup"><span data-stu-id="4509f-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="4509f-134">**MFMediaType \_ protegido**</span><span class="sxs-lookup"><span data-stu-id="4509f-134">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="4509f-135">Mídia protegida.</span><span class="sxs-lookup"><span data-stu-id="4509f-135">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="4509f-136">O subtipo especifica o esquema de proteção de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4509f-136">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="4509f-137">**Percepção de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="4509f-137">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="4509f-138">Transmite de um sensor de câmera ou unidade de processamento por razões e compreende dados brutos de vídeo e fornece compreensão do ambiente ou dos seres humanos.</span><span class="sxs-lookup"><span data-stu-id="4509f-138">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="4509f-139">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4509f-139">None.</span></span>                                                |
| <span data-ttu-id="4509f-140">**Sami de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="4509f-140">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="4509f-141">Legendas de SAMI (intercâmbio de mídia acessível) sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="4509f-141">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="4509f-142">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4509f-142">None.</span></span>                                                |
| <span data-ttu-id="4509f-143">**\_Script MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4509f-143">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="4509f-144">Fluxo de script.</span><span class="sxs-lookup"><span data-stu-id="4509f-144">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="4509f-145">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4509f-145">None.</span></span>                                                |
| <span data-ttu-id="4509f-146">**Fluxo de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="4509f-146">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="4509f-147">Fluxo multiplexado ou fluxo elementar.</span><span class="sxs-lookup"><span data-stu-id="4509f-147">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="4509f-148">GUIDs de subtipo de fluxo</span><span class="sxs-lookup"><span data-stu-id="4509f-148">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="4509f-149">**Vídeo do MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="4509f-149">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="4509f-150">Vídeo.</span><span class="sxs-lookup"><span data-stu-id="4509f-150">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="4509f-151">[GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="4509f-151">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="4509f-152">Os componentes de terceiros podem definir novos tipos principais e novos subtipos.</span><span class="sxs-lookup"><span data-stu-id="4509f-152">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4509f-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4509f-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4509f-154">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4509f-154">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="4509f-155">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="4509f-155">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
