---
description: Fornecendo um redimensionador de vídeo personalizado
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Fornecendo um redimensionador de vídeo personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087468"
---
# <a name="providing-a-custom-video-resizer"></a><span data-ttu-id="41224-103">Fornecendo um redimensionador de vídeo personalizado</span><span class="sxs-lookup"><span data-stu-id="41224-103">Providing a Custom Video Resizer</span></span>

<span data-ttu-id="41224-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="41224-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

> [!Note]  
> <span data-ttu-id="41224-105">Este recurso requer o DirectX 9,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="41224-105">This feature requires DirectX 9.0 or later.</span></span>

 

<span data-ttu-id="41224-106">Quando os [serviços de edição do DirectShow](directshow-editing-services.md) (des) redimensionam um clipe de fonte de vídeo, o comportamento padrão é um *StretchBlt*, que é rápido, mas sem suavização de serrilhado.</span><span class="sxs-lookup"><span data-stu-id="41224-106">When [DirectShow Editing Services](directshow-editing-services.md) (DES) resizes a video source clip, the default behavior is a *StretchBlt*, which is fast but not anti-aliased.</span></span> <span data-ttu-id="41224-107">Você pode alterar o comportamento de redimensionamento implementando um redimensionador personalizado como um filtro de transformação do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="41224-107">You can change the resizing behavior by implementing a custom resizer as a DirectShow transform filter.</span></span> <span data-ttu-id="41224-108">O filtro deve expor a interface [**IResize**](iresize.md) , que permite que o des especifique o tamanho do vídeo de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="41224-108">The filter must expose the [**IResize**](iresize.md) interface, which enables DES to specify the input and output video size.</span></span> <span data-ttu-id="41224-109">Para obter informações sobre como escrever um filtro de transformação, consulte [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="41224-109">For information about writing a transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span> <span data-ttu-id="41224-110">A classe base **CTransformFilter** é recomendada como ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="41224-110">The **CTransformFilter** base class is recommended as the starting point.</span></span> <span data-ttu-id="41224-111">Ao implementar o filtro, observe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="41224-111">When you implement the filter, note the following:</span></span>

-   <span data-ttu-id="41224-112">Suporte à interface **IResize** no filtro (não nos Pins).</span><span class="sxs-lookup"><span data-stu-id="41224-112">Support the **IResize** interface on the filter (not the pins).</span></span>
-   <span data-ttu-id="41224-113">O filtro deve aceitar somente formatos [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (Format \_ VIDEOINFO).</span><span class="sxs-lookup"><span data-stu-id="41224-113">The filter should accept only [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) formats (FORMAT\_VideoInfo).</span></span> <span data-ttu-id="41224-114">Rejeite outros tipos de formato.</span><span class="sxs-lookup"><span data-stu-id="41224-114">Reject other format types.</span></span>
-   <span data-ttu-id="41224-115">O formato de vídeo de DES pode ser qualquer tipo RGB descompactado, incluindo o RGB de 32 bits com alfa (MEDIASUBTYPE \_ ARGB32).</span><span class="sxs-lookup"><span data-stu-id="41224-115">The video format from DES may be any uncompressed RGB type, including 32-bit RGB with alpha (MEDIASUBTYPE\_ARGB32).</span></span> <span data-ttu-id="41224-116">O filtro pode rejeitar com segurança formatos com a **altura** < 0.</span><span class="sxs-lookup"><span data-stu-id="41224-116">Your filter can safely reject formats with **biHeight** < 0.</span></span>
-   <span data-ttu-id="41224-117">Antes que o mecanismo de renderização Conecte o pino de saída do filtro, ele chama [**IResize::p UT \_ MediaType**](iresize-put-mediatype.md) para definir o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="41224-117">Before the Render Engine connects the filter's output pin, it calls [**IResize::put\_MediaType**](iresize-put-mediatype.md) to set the output type.</span></span> <span data-ttu-id="41224-118">Ele também pode chamar [**IResize::p UT \_ size**](iresize-put-size.md) para ajustar o tamanho da saída.</span><span class="sxs-lookup"><span data-stu-id="41224-118">It may also call [**IResize::put\_Size**](iresize-put-size.md) to adjust the output size.</span></span> <span data-ttu-id="41224-119">Ele pode chamar esses dois métodos em qualquer ordem, qualquer número de vezes, antes de conectar o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="41224-119">It can call these two methods in any order, any number of times, before it connects the output pin.</span></span>
-   <span data-ttu-id="41224-120">Depois que o mecanismo de renderização conecta o pino de saída, ele pode chamar **Put \_ size** novamente.</span><span class="sxs-lookup"><span data-stu-id="41224-120">After the Render Engine connects the output pin, it might call **put\_Size** again.</span></span> <span data-ttu-id="41224-121">O filtro de redimensionador deve reconectar seu pino de saída com o novo tamanho.</span><span class="sxs-lookup"><span data-stu-id="41224-121">The resizer filter should reconnect its output pin with the new size.</span></span>
-   <span data-ttu-id="41224-122">Dentro do método [**CTransformFilter:: Transform**](ctransformfilter-transform.md) do filtro, estique o vídeo de entrada para o tamanho de saída.</span><span class="sxs-lookup"><span data-stu-id="41224-122">Inside the filter's [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, stretch the input video to the output size.</span></span>
-   <span data-ttu-id="41224-123">O filtro nunca deve definir o sinalizador de discontinuidade no exemplo de saída ou anexar um tipo de mídia ao exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="41224-123">Your filter should never set the discontinuity flag on the output sample, or attach a media type to the output sample.</span></span>
-   <span data-ttu-id="41224-124">Para salvar o estado do filtro em um arquivo GraphEdit (. GRF), implemente a interface **IPersistStream** .</span><span class="sxs-lookup"><span data-stu-id="41224-124">To save the filter's state in a GraphEdit (.grf) file, implement the **IPersistStream** interface.</span></span> <span data-ttu-id="41224-125">(Isso é opcional, mas útil para teste.)</span><span class="sxs-lookup"><span data-stu-id="41224-125">(This is optional, but useful for testing.)</span></span>

<span data-ttu-id="41224-126">Para usar o filtro redimensionador, o filtro deve ser registrado como um objeto COM no sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="41224-126">To use the resizer filter, the filter must be registered as a COM object on the user's system.</span></span> <span data-ttu-id="41224-127">Antes de o aplicativo renderizar o projeto de vídeo, consulte o mecanismo de renderização para a interface [**IRenderEngine2**](irenderengine2.md) e chame [**IRenderEngine2:: SETRESIZERGUID**](irenderengine2-setresizerguid.md) com o CLSID do filtro de redimensionador.</span><span class="sxs-lookup"><span data-stu-id="41224-127">Before the application renders the video project, query the Render Engine for the [**IRenderEngine2**](irenderengine2.md) interface and call [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) with the CLSID of the resizer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41224-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41224-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41224-129">Renderizando um projeto</span><span class="sxs-lookup"><span data-stu-id="41224-129">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



