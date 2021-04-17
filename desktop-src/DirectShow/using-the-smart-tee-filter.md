---
description: Usando o filtro de "t inteligente"
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Usando o filtro de "t inteligente"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780550"
---
# <a name="using-the-smart-tee-filter"></a><span data-ttu-id="ae341-103">Usando o filtro de "t inteligente"</span><span class="sxs-lookup"><span data-stu-id="ae341-103">Using the Smart Tee Filter</span></span>

<span data-ttu-id="ae341-104">Se um filtro de captura tiver Pins de captura e de visualização separados, você poderá capturar de um durante a visualização do outro.</span><span class="sxs-lookup"><span data-stu-id="ae341-104">If a capture filter has separate capture and preview pins, you can capture from one while previewing from the other.</span></span> <span data-ttu-id="ae341-105">Mas se o filtro não tiver nenhum pino de visualização, você poderá fazer a mesma coisa, incluindo o filtro de " [t" inteligente](smart-tee-filter.md) no grafo.</span><span class="sxs-lookup"><span data-stu-id="ae341-105">But if the filter has no preview pin, you can do the same thing by including the [Smart Tee](smart-tee-filter.md) filter in the graph.</span></span> <span data-ttu-id="ae341-106">Esse filtro divide os dados do pino de captura em dois fluxos idênticos, um para captura e outro para visualização.</span><span class="sxs-lookup"><span data-stu-id="ae341-106">This filter splits data from the capture pin into two identical streams, one for capture and one for preview.</span></span> <span data-ttu-id="ae341-107">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="ae341-107">The following diagram illustrates this process.</span></span>

![capturar grafo com o filtro de "inteligente"](images/vidcap05.png)

<span data-ttu-id="ae341-109">O método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insere automaticamente o filtro de "t inteligente", se necessário.</span><span class="sxs-lookup"><span data-stu-id="ae341-109">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Smart Tee Filter if it is required.</span></span> <span data-ttu-id="ae341-110">No entanto, se você usar métodos **IGraphBuilder** para criar seu grafo, e não **RenderStream**, talvez seja necessário inserir o filtro de "t inteligente".</span><span class="sxs-lookup"><span data-stu-id="ae341-110">However, if you use **IGraphBuilder** methods to build your graph, and not **RenderStream**, you may need to insert the Smart Tee filter.</span></span>

<span data-ttu-id="ae341-111">Antes de renderizar Pins no filtro de captura, verifique se o filtro tem um PIN de visualização ou um PIN de porta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae341-111">Before you render pins on the capture filter, check whether the filter has a preview pin or a video port pin.</span></span> <span data-ttu-id="ae341-112">Se não tiver, e você quiser Visualizar, adicione o filtro de "t Smart" ao grafo e conecte-o ao PIN de captura no filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="ae341-112">If it does not, and you wish to preview, add the Smart Tee filter to the graph and connect it to the capture pin on the capture filter.</span></span>

> [!Note]  
> <span data-ttu-id="ae341-113">Você pode tratar um PIN de porta de vídeo (VP) como um tipo de pino de visualização, de modo que um filtro com um VP PIN não precisa de um filtro de monitoração inteligente.</span><span class="sxs-lookup"><span data-stu-id="ae341-113">You can treat a video port (VP) pin as a kind of preview pin, so a filter with a VP pin does not need a Smart Tee filter.</span></span> <span data-ttu-id="ae341-114">No entanto, o VP de Pins tem alguns outros requisitos especiais.</span><span class="sxs-lookup"><span data-stu-id="ae341-114">However, VP pins have some other special requirements.</span></span> <span data-ttu-id="ae341-115">Para obter mais informações, consulte [pinos de porta de vídeo](video-port-pins.md).</span><span class="sxs-lookup"><span data-stu-id="ae341-115">For more information, see [Video Port Pins](video-port-pins.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ae341-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae341-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae341-117">Tópicos de captura avançada</span><span class="sxs-lookup"><span data-stu-id="ae341-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="ae341-118">Combinando captura de vídeo e visualização</span><span class="sxs-lookup"><span data-stu-id="ae341-118">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="ae341-119">Trabalhando com categorias de PIN</span><span class="sxs-lookup"><span data-stu-id="ae341-119">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 



