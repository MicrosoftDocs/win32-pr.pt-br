---
description: As funções a seguir pertencem a objetos de tipo de mídia.
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: Funções auxiliares de tipo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e5edb9748bad8ee16903eb9ff1ada50c1c043b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506353"
---
# <a name="media-type-helper-functions"></a><span data-ttu-id="92725-103">Funções auxiliares de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="92725-103">Media Type Helper Functions</span></span>

<span data-ttu-id="92725-104">As funções a seguir pertencem a objetos de tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="92725-104">The following functions pertain to media type objects.</span></span>



| <span data-ttu-id="92725-105">Função</span><span class="sxs-lookup"><span data-stu-id="92725-105">Function</span></span>                                                                     | <span data-ttu-id="92725-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="92725-106">Description</span></span>                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="92725-107">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="92725-107">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="92725-108">Calcula a taxa de quadros a partir da duração média de um quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="92725-108">Calculates the frame rate from the average duration of a video frame.</span></span> |
| [<span data-ttu-id="92725-109">**MFCalculateImageSize**</span><span class="sxs-lookup"><span data-stu-id="92725-109">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="92725-110">Recupera o tamanho da imagem para um formato de vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="92725-110">Retrieves the image size for an uncompressed video format.</span></span>            |
| [<span data-ttu-id="92725-111">**MFCompareFullToPartialMediaType**</span><span class="sxs-lookup"><span data-stu-id="92725-111">**MFCompareFullToPartialMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | <span data-ttu-id="92725-112">Compara um tipo de mídia completa com um tipo de mídia parcial.</span><span class="sxs-lookup"><span data-stu-id="92725-112">Compares a full media type to a partial media type.</span></span>                   |
| [<span data-ttu-id="92725-113">**MFCreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="92725-113">**MFCreateMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | <span data-ttu-id="92725-114">Cria um tipo de mídia vazio.</span><span class="sxs-lookup"><span data-stu-id="92725-114">Creates an empty media type.</span></span>                                          |
| [<span data-ttu-id="92725-115">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="92725-115">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="92725-116">Converte uma taxa de quadros de vídeo em uma duração de quadro.</span><span class="sxs-lookup"><span data-stu-id="92725-116">Converts a video frame rate into a frame duration.</span></span>                    |
| [<span data-ttu-id="92725-117">**MFGetStrideForBitmapInfoHeader**</span><span class="sxs-lookup"><span data-stu-id="92725-117">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="92725-118">Recupera o stride de superfície mínimo para um formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="92725-118">Retrieves the minimum surface stride for a video format.</span></span>              |
| [<span data-ttu-id="92725-119">**MFIsFormatYUV**</span><span class="sxs-lookup"><span data-stu-id="92725-119">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="92725-120">Consulta se um código FOURCC ou um valor **D3DFORMAT** é um formato YUV.</span><span class="sxs-lookup"><span data-stu-id="92725-120">Queries whether a FOURCC code or **D3DFORMAT** value is a YUV format.</span></span> |
| [<span data-ttu-id="92725-121">**MFValidateMediaTypeSize**</span><span class="sxs-lookup"><span data-stu-id="92725-121">**MFValidateMediaTypeSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | <span data-ttu-id="92725-122">Valida o tamanho de um buffer para um bloco de formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="92725-122">Validates the size of a buffer for a video format block.</span></span>              |
| [<span data-ttu-id="92725-123">**MFWrapMediaType**</span><span class="sxs-lookup"><span data-stu-id="92725-123">**MFWrapMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | <span data-ttu-id="92725-124">Cria um tipo de mídia que encapsula outro tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="92725-124">Creates a media type that wraps another media type.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="92725-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92725-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92725-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="92725-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="92725-127">Conversões de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="92725-127">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="92725-128">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="92725-128">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



