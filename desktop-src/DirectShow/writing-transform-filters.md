---
description: Gravando filtros de transformação
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Gravando filtros de transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921918"
---
# <a name="writing-transform-filters"></a><span data-ttu-id="2d8fb-103">Gravando filtros de transformação</span><span class="sxs-lookup"><span data-stu-id="2d8fb-103">Writing Transform Filters</span></span>

<span data-ttu-id="2d8fb-104">Esta seção descreve como escrever um filtro de transformação, definido como um filtro que tem exatamente um PIN de entrada e um pino de saída.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-104">This section describes how to write a transform filter, defined as a filter that has exactly one input pin and one output pin.</span></span> <span data-ttu-id="2d8fb-105">Para ilustrar as etapas, esta seção descreve um filtro de transformação hipotético que gera vídeo de RLE (codificação de tamanho de execução).</span><span class="sxs-lookup"><span data-stu-id="2d8fb-105">To illustrate the steps, this section describes a hypothetical transform filter that outputs run-length encoded (RLE) video.</span></span> <span data-ttu-id="2d8fb-106">Ele não descreve o próprio algoritmo de codificação RLE, somente as tarefas específicas do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-106">It does not describe the RLE-encoding algorithm itself, only the tasks that are specific to DirectShow.</span></span> <span data-ttu-id="2d8fb-107">(O DirectShow já fornece um codec RLE por meio do filtro de [compressor AVI](avi-compressor-filter.md) .)</span><span class="sxs-lookup"><span data-stu-id="2d8fb-107">(DirectShow already provides an RLE codec through the [AVI Compressor](avi-compressor-filter.md) filter.)</span></span>

<span data-ttu-id="2d8fb-108">Esta seção pressupõe que você usará a biblioteca de classes base do DirectShow para criar filtros.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-108">This section assumes that you will use the DirectShow base class library to create filters.</span></span> <span data-ttu-id="2d8fb-109">Embora você possa escrever um filtro sem ele, a biblioteca de classes base é altamente recomendável.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-109">Although you can write a filter without it, the base class library is strongly recommended.</span></span>

> [!Note]  
> <span data-ttu-id="2d8fb-110">Antes de escrever um filtro de transformação, considere se um DMO (objeto de mídia do DirectX) atenderia às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-110">Before writing a transform filter, consider whether a DirectX Media Object (DMO) would fulfill your requirements.</span></span> <span data-ttu-id="2d8fb-111">O DMOs pode fazer muitas das mesmas coisas que os filtros, e o modelo de programação para DMOs é mais simples.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-111">DMOs can do many of the same things as filters, and the programming model for DMOs is simpler.</span></span> <span data-ttu-id="2d8fb-112">Os DMOs são hospedados no DirectShow por meio do filtro de [invólucro do DMO](dmo-wrapper-filter.md) , mas também podem ser usados fora do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-112">DMOs are hosted in DirectShow through the [DMO Wrapper](dmo-wrapper-filter.md) filter, but can also be used outside of DirectShow.</span></span> <span data-ttu-id="2d8fb-113">DMOs agora é a solução recomendada para codificadores e decodificadores.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-113">DMOs are now the recommended solution for encoders and decoders.</span></span>

 

<span data-ttu-id="2d8fb-114">Esta seção inclui os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="2d8fb-114">This section includes the following topics:</span></span>

-   [<span data-ttu-id="2d8fb-115">Etapa 1. Escolher uma classe base</span><span class="sxs-lookup"><span data-stu-id="2d8fb-115">Step 1. Choose a Base Class</span></span>](step-1--choose-a-base-class.md)
-   [<span data-ttu-id="2d8fb-116">Etapa 2. Declarar a classe de filtro</span><span class="sxs-lookup"><span data-stu-id="2d8fb-116">Step 2. Declare the Filter Class</span></span>](step-2--declare-the-filter-class.md)
-   [<span data-ttu-id="2d8fb-117">Etapa 3. Suporte à negociação de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="2d8fb-117">Step 3. Support Media Type Negotiation</span></span>](step-3--support-media-type-negotiation.md)
-   [<span data-ttu-id="2d8fb-118">Etapa 4. Definir propriedades de alocador</span><span class="sxs-lookup"><span data-stu-id="2d8fb-118">Step 4. Set Allocator Properties</span></span>](step-4--set-allocator-properties.md)
-   [<span data-ttu-id="2d8fb-119">Etapa 5. Transformar a imagem</span><span class="sxs-lookup"><span data-stu-id="2d8fb-119">Step 5. Transform the Image</span></span>](step-5--transform-the-image.md)
-   [<span data-ttu-id="2d8fb-120">Etapa 6. Adicionar suporte para COM</span><span class="sxs-lookup"><span data-stu-id="2d8fb-120">Step 6. Add Support for COM</span></span>](step-6--add-support-for-com.md)

## <a name="related-topics"></a><span data-ttu-id="2d8fb-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d8fb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d8fb-122">Criando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="2d8fb-122">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="2d8fb-123">Classes base do DirectShow</span><span class="sxs-lookup"><span data-stu-id="2d8fb-123">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="2d8fb-124">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="2d8fb-124">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



