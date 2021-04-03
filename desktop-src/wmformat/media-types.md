---
title: Tipos de mídia
description: Tipos de mídia
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- SDK do Windows Media Format, tipos de mídia
- ASF (Advanced Systems Format), tipos de mídia
- ASF (formato de sistemas avançados), tipos de mídia
- tipos de mídia, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35005498e8b0625f404e9a54a51cddc65fbfd7bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084123"
---
# <a name="media-types"></a><span data-ttu-id="9c142-107">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="9c142-107">Media Types</span></span>

<span data-ttu-id="9c142-108">Os tipos de mídia identificam os diferentes tipos de mídia que podem ser usados pelo SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="9c142-108">Media types identify the different types of media that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="9c142-109">Todos os tipos de mídia são valores de GUID que foram atribuídos a constantes no SDK.</span><span class="sxs-lookup"><span data-stu-id="9c142-109">All media types are GUID values that have been assigned to constants in the SDK.</span></span> <span data-ttu-id="9c142-110">Os valores de GUID representados pelas constantes listadas nesta seção são listados na seção [identificadores de tipo de mídia](media-type-identifiers.md) desta referência.</span><span class="sxs-lookup"><span data-stu-id="9c142-110">The GUID values represented by the constants listed in this section are listed in the [Media Type Identifiers](media-type-identifiers.md) section of this reference.</span></span>

<span data-ttu-id="9c142-111">A tabela a seguir lista os principais tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="9c142-111">The following table lists major media types.</span></span> <span data-ttu-id="9c142-112">Essas constantes definem a classificação de alto nível de mídia digital com suporte no Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="9c142-112">These constants define the high level classification of digital media supported by the Windows Media Format SDK.</span></span>



| <span data-ttu-id="9c142-113">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="9c142-113">Major type</span></span>                | <span data-ttu-id="9c142-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c142-114">Description</span></span>                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c142-115">Vídeo do WMMEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="9c142-115">WMMEDIATYPE\_Video</span></span>        | <span data-ttu-id="9c142-116">Um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9c142-116">A video stream.</span></span>                                                                                         |
| <span data-ttu-id="9c142-117">\_Áudio WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="9c142-117">WMMEDIATYPE\_Audio</span></span>        | <span data-ttu-id="9c142-118">Um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="9c142-118">An audio stream.</span></span>                                                                                        |
| <span data-ttu-id="9c142-119">\_Script WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="9c142-119">WMMEDIATYPE\_Script</span></span>       | <span data-ttu-id="9c142-120">Um fluxo de script.</span><span class="sxs-lookup"><span data-stu-id="9c142-120">A script stream.</span></span>                                                                                        |
| <span data-ttu-id="9c142-121">WMMEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="9c142-121">WMMEDIATYPE\_FileTransfer</span></span> | <span data-ttu-id="9c142-122">Um fluxo que contém arquivos de dados.</span><span class="sxs-lookup"><span data-stu-id="9c142-122">A stream that contains data files.</span></span> <span data-ttu-id="9c142-123">Os fluxos da Web, que consistem em arquivos HTML, também têm esse tipo principal.</span><span class="sxs-lookup"><span data-stu-id="9c142-123">Web streams, which consist of HTML files, also have this major type.</span></span> |
| <span data-ttu-id="9c142-124">\_Imagem WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="9c142-124">WMMEDIATYPE\_Image</span></span>        | <span data-ttu-id="9c142-125">Um fluxo de imagem JPEG para um arquivo de áudio ilustrado (como em uma apresentação de slides).</span><span class="sxs-lookup"><span data-stu-id="9c142-125">A JPEG image stream for an illustrated audio file (as in a slide show).</span></span>                                 |
| <span data-ttu-id="9c142-126">\_Texto WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="9c142-126">WMMEDIATYPE\_Text</span></span>         | <span data-ttu-id="9c142-127">Um fluxo de texto.</span><span class="sxs-lookup"><span data-stu-id="9c142-127">A text stream.</span></span>                                                                                          |



 

<span data-ttu-id="9c142-128">Além dos principais tipos de mídia com suporte explícito, você pode criar seus próprios tipos de dados arbitrários.</span><span class="sxs-lookup"><span data-stu-id="9c142-128">In addition to the explicitly supported major media types, you can create your own arbitrary data types.</span></span> <span data-ttu-id="9c142-129">Para tipos de dados arbitrários personalizados, você deve garantir que o GUID usado não corresponda a um tipo principal existente.</span><span class="sxs-lookup"><span data-stu-id="9c142-129">For custom arbitrary data types, you must ensure that the GUID you use does not match an existing major type.</span></span>

<span data-ttu-id="9c142-130">Um fluxo de mídia geralmente terá um subtipo, além de seu tipo principal.</span><span class="sxs-lookup"><span data-stu-id="9c142-130">A media stream will often have a subtype in addition to its major type.</span></span> <span data-ttu-id="9c142-131">As seções a seguir listam os subtipos com suporte.</span><span class="sxs-lookup"><span data-stu-id="9c142-131">The following sections list the supported subtypes.</span></span>



| <span data-ttu-id="9c142-132">Seção</span><span class="sxs-lookup"><span data-stu-id="9c142-132">Section</span></span>                                                        | <span data-ttu-id="9c142-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c142-133">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c142-134">Subtipos de mídia descompactados</span><span class="sxs-lookup"><span data-stu-id="9c142-134">Uncompressed Media Subtypes</span></span>](uncompressed-media-subtypes.md) | <span data-ttu-id="9c142-135">Descreve os subtipos disponíveis para mídias não compactadas.</span><span class="sxs-lookup"><span data-stu-id="9c142-135">Describes the subtypes available for uncompressed media.</span></span> <span data-ttu-id="9c142-136">Esses são os tipos normalmente associados à mídia de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="9c142-136">These are the types typically associated with input or output media.</span></span>              |
| [<span data-ttu-id="9c142-137">Subtipos de mídia compactados</span><span class="sxs-lookup"><span data-stu-id="9c142-137">Compressed Media Subtypes</span></span>](compressed-media-subtypes.md)     | <span data-ttu-id="9c142-138">Descreve os subtipos disponíveis para mídia compactada.</span><span class="sxs-lookup"><span data-stu-id="9c142-138">Describes the subtypes available for compressed media.</span></span> <span data-ttu-id="9c142-139">Esses são os tipos normalmente associados à mídia em um fluxo dentro de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="9c142-139">These are the types typically associated with media in a stream within an ASF file.</span></span> |
| [<span data-ttu-id="9c142-140">Formatos de entrada de vídeo</span><span class="sxs-lookup"><span data-stu-id="9c142-140">Video Input Formats</span></span>](video-input-formats.md)                 | <span data-ttu-id="9c142-141">Lista os formatos de vídeo aceitos como entradas para o codec do Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="9c142-141">Lists the video formats accepted as inputs for the Windows Media Video 9 codec.</span></span>                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="9c142-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c142-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c142-143">**Identificadores de tipo de mídia**</span><span class="sxs-lookup"><span data-stu-id="9c142-143">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="9c142-144">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="9c142-144">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




