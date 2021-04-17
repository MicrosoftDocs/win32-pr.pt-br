---
title: Tipos de mídia do Windows Media Format SDK
description: Saiba mais sobre os tipos de mídia que podem ser usados pelo Windows Media Format SDK. Os tipos de mídia são valores de GUID atribuídos a constantes no SDK.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- SDK do Windows Media Format, tipos de mídia
- ASF (Advanced Systems Format), tipos de mídia
- ASF (formato de sistemas avançados), tipos de mídia
- tipos de mídia, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187811"
---
# <a name="media-types-for-windows-media-format-sdk"></a><span data-ttu-id="7c163-108">Tipos de mídia do Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="7c163-108">Media Types for Windows Media Format SDK</span></span>

<span data-ttu-id="7c163-109">Os tipos de mídia identificam os diferentes tipos de mídia que podem ser usados pelo SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="7c163-109">Media types identify the different types of media that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="7c163-110">Todos os tipos de mídia são valores de GUID que foram atribuídos a constantes no SDK.</span><span class="sxs-lookup"><span data-stu-id="7c163-110">All media types are GUID values that have been assigned to constants in the SDK.</span></span> <span data-ttu-id="7c163-111">Os valores de GUID representados pelas constantes listadas nesta seção são listados na seção [identificadores de tipo de mídia](media-type-identifiers.md) desta referência.</span><span class="sxs-lookup"><span data-stu-id="7c163-111">The GUID values represented by the constants listed in this section are listed in the [Media Type Identifiers](media-type-identifiers.md) section of this reference.</span></span>

<span data-ttu-id="7c163-112">A tabela a seguir lista os principais tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="7c163-112">The following table lists major media types.</span></span> <span data-ttu-id="7c163-113">Essas constantes definem a classificação de alto nível de mídia digital com suporte no Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="7c163-113">These constants define the high level classification of digital media supported by the Windows Media Format SDK.</span></span>



| <span data-ttu-id="7c163-114">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="7c163-114">Major type</span></span>                | <span data-ttu-id="7c163-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c163-115">Description</span></span>                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c163-116">Vídeo do WMMEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="7c163-116">WMMEDIATYPE\_Video</span></span>        | <span data-ttu-id="7c163-117">Um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7c163-117">A video stream.</span></span>                                                                                         |
| <span data-ttu-id="7c163-118">\_Áudio WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="7c163-118">WMMEDIATYPE\_Audio</span></span>        | <span data-ttu-id="7c163-119">Um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="7c163-119">An audio stream.</span></span>                                                                                        |
| <span data-ttu-id="7c163-120">\_Script WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="7c163-120">WMMEDIATYPE\_Script</span></span>       | <span data-ttu-id="7c163-121">Um fluxo de script.</span><span class="sxs-lookup"><span data-stu-id="7c163-121">A script stream.</span></span>                                                                                        |
| <span data-ttu-id="7c163-122">WMMEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="7c163-122">WMMEDIATYPE\_FileTransfer</span></span> | <span data-ttu-id="7c163-123">Um fluxo que contém arquivos de dados.</span><span class="sxs-lookup"><span data-stu-id="7c163-123">A stream that contains data files.</span></span> <span data-ttu-id="7c163-124">Os fluxos da Web, que consistem em arquivos HTML, também têm esse tipo principal.</span><span class="sxs-lookup"><span data-stu-id="7c163-124">Web streams, which consist of HTML files, also have this major type.</span></span> |
| <span data-ttu-id="7c163-125">\_Imagem WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="7c163-125">WMMEDIATYPE\_Image</span></span>        | <span data-ttu-id="7c163-126">Um fluxo de imagem JPEG para um arquivo de áudio ilustrado (como em uma apresentação de slides).</span><span class="sxs-lookup"><span data-stu-id="7c163-126">A JPEG image stream for an illustrated audio file (as in a slide show).</span></span>                                 |
| <span data-ttu-id="7c163-127">\_Texto WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="7c163-127">WMMEDIATYPE\_Text</span></span>         | <span data-ttu-id="7c163-128">Um fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="7c163-128">A text stream.</span></span>                                                                                          |



 

<span data-ttu-id="7c163-129">Além dos principais tipos de mídia com suporte explícito, você pode criar seus próprios tipos de dados arbitrários.</span><span class="sxs-lookup"><span data-stu-id="7c163-129">In addition to the explicitly supported major media types, you can create your own arbitrary data types.</span></span> <span data-ttu-id="7c163-130">Para tipos de dados arbitrários personalizados, você deve garantir que o GUID usado não corresponda a um tipo principal existente.</span><span class="sxs-lookup"><span data-stu-id="7c163-130">For custom arbitrary data types, you must ensure that the GUID you use does not match an existing major type.</span></span>

<span data-ttu-id="7c163-131">Um fluxo de mídia geralmente terá um subtipo, além de seu tipo principal.</span><span class="sxs-lookup"><span data-stu-id="7c163-131">A media stream will often have a subtype in addition to its major type.</span></span> <span data-ttu-id="7c163-132">As seções a seguir listam os subtipos com suporte.</span><span class="sxs-lookup"><span data-stu-id="7c163-132">The following sections list the supported subtypes.</span></span>



| <span data-ttu-id="7c163-133">Seção</span><span class="sxs-lookup"><span data-stu-id="7c163-133">Section</span></span>                                                        | <span data-ttu-id="7c163-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c163-134">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c163-135">Subtipos de mídia descompactados</span><span class="sxs-lookup"><span data-stu-id="7c163-135">Uncompressed Media Subtypes</span></span>](uncompressed-media-subtypes.md) | <span data-ttu-id="7c163-136">Descreve os subtipos disponíveis para mídias não compactadas.</span><span class="sxs-lookup"><span data-stu-id="7c163-136">Describes the subtypes available for uncompressed media.</span></span> <span data-ttu-id="7c163-137">Esses são os tipos normalmente associados à mídia de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="7c163-137">These are the types typically associated with input or output media.</span></span>              |
| [<span data-ttu-id="7c163-138">Subtipos de mídia compactados</span><span class="sxs-lookup"><span data-stu-id="7c163-138">Compressed Media Subtypes</span></span>](compressed-media-subtypes.md)     | <span data-ttu-id="7c163-139">Descreve os subtipos disponíveis para mídia compactada.</span><span class="sxs-lookup"><span data-stu-id="7c163-139">Describes the subtypes available for compressed media.</span></span> <span data-ttu-id="7c163-140">Esses são os tipos normalmente associados à mídia em um fluxo dentro de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="7c163-140">These are the types typically associated with media in a stream within an ASF file.</span></span> |
| [<span data-ttu-id="7c163-141">Formatos de entrada de vídeo</span><span class="sxs-lookup"><span data-stu-id="7c163-141">Video Input Formats</span></span>](video-input-formats.md)                 | <span data-ttu-id="7c163-142">Lista os formatos de vídeo aceitos como entradas para o codec do Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="7c163-142">Lists the video formats accepted as inputs for the Windows Media Video 9 codec.</span></span>                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="7c163-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c163-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c163-144">**Identificadores de tipo de mídia**</span><span class="sxs-lookup"><span data-stu-id="7c163-144">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="7c163-145">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="7c163-145">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




