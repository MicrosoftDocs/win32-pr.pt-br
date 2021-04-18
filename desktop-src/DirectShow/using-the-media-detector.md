---
description: Usando o detector de mídia
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Usando o detector de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105778461"
---
# <a name="using-the-media-detector"></a><span data-ttu-id="1b7d1-103">Usando o detector de mídia</span><span class="sxs-lookup"><span data-stu-id="1b7d1-103">Using the Media Detector</span></span>

<span data-ttu-id="1b7d1-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="1b7d1-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="1b7d1-105">O detector de mídia é um objeto auxiliar que pode recuperar informações sobre um arquivo, como o número de fluxos, seu tipo e sua duração.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-105">The media detector is a helper object that can retrieve information about a file, such as the number of streams, their type, and their duration.</span></span> <span data-ttu-id="1b7d1-106">Ele também contém métodos para recuperar quadros de pôster de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-106">It also contains methods for retrieving poster frames from a video stream.</span></span> <span data-ttu-id="1b7d1-107">Ele expõe a interface [**IMediaDet**](imediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="1b7d1-107">It exposes the [**IMediaDet**](imediadet.md) interface.</span></span>

<span data-ttu-id="1b7d1-108">O detector de mídia opera em um dos dois modos.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-108">The media detector operates in one of two modes.</span></span> <span data-ttu-id="1b7d1-109">Quando você cria uma instância do detector de mídia, ela não é anexada a um arquivo de origem específico.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-109">When you create an instance of the media detector, it is not attached to a particular source file.</span></span> <span data-ttu-id="1b7d1-110">Nesse modo, você pode recuperar informações de fluxo de vários arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-110">In this mode, you can retrieve stream information from multiple source files.</span></span> <span data-ttu-id="1b7d1-111">No entanto, depois de usar o detector de mídia para obter um quadro de pôster, ele alterna para o *modo de captura de bitmap*.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-111">However, once you use the media detector to obtain a poster frame, it switches to *bitmap grab mode*.</span></span> <span data-ttu-id="1b7d1-112">No modo de captura de bitmap, o detector de mídia é anexado a um fluxo de vídeo específico e os métodos de informações de fluxo não funcionam mais.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-112">In bitmap grab mode, the media detector is attached to a specific video stream, and the stream information methods no longer work.</span></span> <span data-ttu-id="1b7d1-113">Além disso, não há como mudar o detector de mídia para seu modo de início.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-113">Moreover, there is no way to switch the media detector back to its starting mode.</span></span> <span data-ttu-id="1b7d1-114">Portanto, obtenha as informações de fluxo necessárias antes de recuperar os quadros de pôster ou crie novas instâncias do detector de mídia para cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-114">Therefore, obtain any stream information you need before retrieving poster frames, or else create new instances of the media detector for each stream.</span></span>

<span data-ttu-id="1b7d1-115">Para obter informações de fluxo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b7d1-115">To obtain stream information, do the following:</span></span>

1.  <span data-ttu-id="1b7d1-116">Chame [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) com o nome do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-116">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) with the name of the source file.</span></span>
2.  <span data-ttu-id="1b7d1-117">Chame [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) para obter o número de fluxos na origem.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-117">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of streams in the source.</span></span>
3.  <span data-ttu-id="1b7d1-118">Especifique um número de fluxo com [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="1b7d1-118">Specify a stream number with [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span> <span data-ttu-id="1b7d1-119">Em seguida, chame um ou mais dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="1b7d1-119">Then call one or more of the following methods:</span></span>
    -   <span data-ttu-id="1b7d1-120">[**IMediaDet:: get \_ Streamtype**](imediadet-get-streamtype.md): recupera o tipo de mídia do fluxo.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-120">[**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md): Retrieves the stream's media type.</span></span>
    -   <span data-ttu-id="1b7d1-121">[**IMediaDet:: get \_ StreamLength**](imediadet-get-streamlength.md): recupera a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-121">[**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md): Retrieves the duration of the stream.</span></span>
    -   <span data-ttu-id="1b7d1-122">[**IMediaDet:: get \_**](imediadet-get-framerate.md)Faixa de quadros: recupera a taxa de quadros de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-122">[**IMediaDet::get\_FrameRate**](imediadet-get-framerate.md): Retrieves a video stream's frame rate.</span></span>

<span data-ttu-id="1b7d1-123">Para obter um quadro de cartaz, especifique o número do fluxo, como na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-123">To obtain a poster frame, specify the stream number, as in the previous step.</span></span> <span data-ttu-id="1b7d1-124">Em seguida, chame [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md), que copia um quadro de pôster em um buffer, ou [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md), que salva um quadro de pôster em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="1b7d1-124">Then call either [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md), which copies a poster frame into a buffer, or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md), which saves a poster frame to a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b7d1-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b7d1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b7d1-126">Trabalhando com fontes</span><span class="sxs-lookup"><span data-stu-id="1b7d1-126">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



