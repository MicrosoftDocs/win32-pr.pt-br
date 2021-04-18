---
description: Trabalhando com quadros de vídeo
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Trabalhando com quadros de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812968"
---
# <a name="working-with-video-frames"></a><span data-ttu-id="28fb3-103">Trabalhando com quadros de vídeo</span><span class="sxs-lookup"><span data-stu-id="28fb3-103">Working with Video Frames</span></span>

<span data-ttu-id="28fb3-104">O vídeo descompactado é uma sequência de bitmaps reproduzidos em uma rápida sucessão, normalmente a uma taxa de aproximadamente 30 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="28fb3-104">Uncompressed video is a sequence of bitmaps played in rapid succession, typically at a rate of about 30 frames per second.</span></span> <span data-ttu-id="28fb3-105">Como a maioria do vídeo entra em um grafo de filtro do DirectShow em um formato compactado, o fluxo de vídeo geralmente passa por um decodificador para descompactação.</span><span class="sxs-lookup"><span data-stu-id="28fb3-105">Because most video enters a DirectShow filter graph in a compressed format, the video stream generally goes through a decoder for decompression.</span></span> <span data-ttu-id="28fb3-106">Muitos decodificadores geram dados em um formato YUV e deixam a conversão final em RGB para o hardware de vídeo logo antes da renderização.</span><span class="sxs-lookup"><span data-stu-id="28fb3-106">Many decoders output data in a YUV format and leave the final conversion to RGB for the video hardware just prior to rendering.</span></span> <span data-ttu-id="28fb3-107">Se um decodificador usar a aceleração de vídeo do DirectX, o hardware de vídeo executará um trabalho adicional para decodificar a imagem.</span><span class="sxs-lookup"><span data-stu-id="28fb3-107">If a decoder uses DirectX Video Acceleration, the video hardware performs additional work to decode the image.</span></span> <span data-ttu-id="28fb3-108">Assim, a descompactação final dos bitmaps pode não ser executada até que os dados cheguem ao hardware de vídeo.</span><span class="sxs-lookup"><span data-stu-id="28fb3-108">Thus, final decompression of the bitmaps may not be performed until the data reaches the video hardware.</span></span>

<span data-ttu-id="28fb3-109">Mas, para executar muitos tipos de análise de vídeo, processamento ou edição, geralmente é necessário trabalhar em bitmaps não compactados em algum tipo de formato RGB ou YUV antes de serem renderizados ou gravados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="28fb3-109">But to perform many types of video analysis, processing, or editing, it is often necessary to work on uncompressed bitmaps in some type of RGB or YUV format before they are rendered or written to file.</span></span> <span data-ttu-id="28fb3-110">Normalmente, esse trabalho é feito dentro de um filtro de transformação baseado na classe base [**CTransformFilter**](ctransformfilter.md) , especificamente no método **Transform** .</span><span class="sxs-lookup"><span data-stu-id="28fb3-110">This work is typically done within a transform filter based on the [**CTransformFilter**](ctransformfilter.md) base class, specifically in the **Transform** method.</span></span> <span data-ttu-id="28fb3-111">Esse método recebe um ponteiro para um objeto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) que encapsula os dados de vídeo.</span><span class="sxs-lookup"><span data-stu-id="28fb3-111">This method receives a pointer to an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) object that encapsulates the video data.</span></span> <span data-ttu-id="28fb3-112">O método **IMediaSample:: Getpointr** retorna um ponteiro para o primeiro byte dos dados brutos.</span><span class="sxs-lookup"><span data-stu-id="28fb3-112">The **IMediaSample::GetPointer** method returns a pointer to the first byte of the raw data.</span></span> <span data-ttu-id="28fb3-113">Para quadros não compactados, esses dados consistem em pixels que podem ser acessados ou modificados diretamente pelo filtro.</span><span class="sxs-lookup"><span data-stu-id="28fb3-113">For uncompressed frames, this data consists of pixels that can be accessed or modified directly by the filter.</span></span> <span data-ttu-id="28fb3-114">As seções a seguir fornecem informações básicas que o ajudarão a trabalhar efetivamente com dados DIB dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="28fb3-114">The following sections provide background information that will help you work effectively with DIB data in this manner.</span></span>

> [!Note]  
> <span data-ttu-id="28fb3-115">Você também pode modificar os bits usando as funções GDI, GDI+, DirectDraw ou Direct3D, mas essas técnicas estão além do escopo deste artigo.</span><span class="sxs-lookup"><span data-stu-id="28fb3-115">You can also modify the bits by using GDI, GDI+, DirectDraw or Direct3D functions, but these techniques are beyond the scope of this article.</span></span>

 

<span data-ttu-id="28fb3-116">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="28fb3-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="28fb3-117">Cima para baixo versus Bottom-Up DIBs</span><span class="sxs-lookup"><span data-stu-id="28fb3-117">Top-Down vs. Bottom-Up DIBs</span></span>](top-down-vs--bottom-up-dibs.md)
-   [<span data-ttu-id="28fb3-118">Trabalhando com RGB de 16 bits</span><span class="sxs-lookup"><span data-stu-id="28fb3-118">Working with 16-bit RGB</span></span>](working-with-16-bit-rgb.md)

 

 



