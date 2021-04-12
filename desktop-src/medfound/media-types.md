---
description: Tipos de mídia
ms.assetid: 690fda6e-dcbd-44dc-968d-cc949126da81
title: Tipos de mídia (Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acbfb1b637eef6acb664d3d95a0488f155c6916
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297973"
---
# <a name="media-types-media-foundation"></a><span data-ttu-id="7ceb7-103">Tipos de mídia (Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="7ceb7-103">Media Types (Media Foundation)</span></span>

<span data-ttu-id="7ceb7-104">Um *tipo de mídia* é uma maneira de descrever o formato de um fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-104">A *media type* is a way to describe the format of a media stream.</span></span> <span data-ttu-id="7ceb7-105">No Media Foundation, os tipos de mídia são representados pela interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="7ceb7-105">In Media Foundation, media types are represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="7ceb7-106">Os aplicativos usam tipos de mídia para descobrir o formato de um arquivo de mídia ou fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-106">Applications use media types to discover the format of a media file or media stream.</span></span> <span data-ttu-id="7ceb7-107">Os objetos no pipeline de Media Foundation usam tipos de mídia para negociar os formatos que serão entregues ou recebidos.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-107">Objects in the Media Foundation pipeline use media types to negotiate the formats they will deliver or receive.</span></span>

<span data-ttu-id="7ceb7-108">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-108">This section contains the following topics.</span></span>



| <span data-ttu-id="7ceb7-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="7ceb7-109">Topic</span></span>                                                                    | <span data-ttu-id="7ceb7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ceb7-110">Description</span></span>                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="7ceb7-111">Sobre os tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="7ceb7-111">About Media Types</span></span>](about-media-types.md)                               | <span data-ttu-id="7ceb7-112">Visão geral dos tipos de mídia no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-112">General overview of media types in Media Foundation.</span></span>                             |
| [<span data-ttu-id="7ceb7-113">GUIDs de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="7ceb7-113">Media Type GUIDs</span></span>](media-type-guids.md)                                 | <span data-ttu-id="7ceb7-114">Lista os GUIDs definidos para tipos e subtipos principais.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-114">Lists the defined GUIDs for major types and subtypes.</span></span>                            |
| [<span data-ttu-id="7ceb7-115">Tipos de mídia de áudio</span><span class="sxs-lookup"><span data-stu-id="7ceb7-115">Audio Media Types</span></span>](audio-media-types.md)                               | <span data-ttu-id="7ceb7-116">Como criar tipos de mídia para formatos de áudio.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-116">How to create media types for audio formats.</span></span>                                     |
| [<span data-ttu-id="7ceb7-117">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="7ceb7-117">Video Media Types</span></span>](video-media-types.md)                               | <span data-ttu-id="7ceb7-118">Como criar tipos de mídia para formatos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-118">How to create media types for video formats.</span></span>                                     |
| [<span data-ttu-id="7ceb7-119">Tipos de mídia completos e parciais</span><span class="sxs-lookup"><span data-stu-id="7ceb7-119">Complete and Partial Media Types</span></span>](complete-and-partial-media-types.md) | <span data-ttu-id="7ceb7-120">Descreve a diferença entre os tipos de mídia completa e os tipos de mídia parcial.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-120">Describes the difference between complete media types and partial media types.</span></span>   |
| [<span data-ttu-id="7ceb7-121">Conversões de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="7ceb7-121">Media Type Conversions</span></span>](media-type-conversions.md)                     | <span data-ttu-id="7ceb7-122">Como converter entre Media Foundation tipos de mídia e estruturas de formato mais antigas.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-122">How to convert between Media Foundation media types and older format structures.</span></span> |
| [<span data-ttu-id="7ceb7-123">Funções auxiliares de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="7ceb7-123">Media Type Helper Functions</span></span>](media-type-helper-functions.md)           | <span data-ttu-id="7ceb7-124">Uma lista de funções que manipulam ou obtêm informações de um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-124">A list of functions that manipulate or get information from a media type.</span></span>        |
| [<span data-ttu-id="7ceb7-125">Código de depuração do tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="7ceb7-125">Media Type Debugging Code</span></span>](media-type-debugging-code.md)               | <span data-ttu-id="7ceb7-126">Código de exemplo que mostra como exibir um tipo de mídia durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="7ceb7-126">Example code that shows how to view a media type while debugging.</span></span>                |



 

## <a name="related-topics"></a><span data-ttu-id="7ceb7-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ceb7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ceb7-128">Primitivos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7ceb7-128">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> <dt>

[<span data-ttu-id="7ceb7-129">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="7ceb7-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 



