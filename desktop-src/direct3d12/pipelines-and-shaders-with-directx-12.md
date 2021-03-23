---
title: Pipelines e sombreadores com o Direct3D 12
description: O pipeline programável do Direct3D 12 aumenta significativamente o desempenho de renderização em comparação com as interfaces de programação de gráficos de geração anteriores.
ms.assetid: 329882F5-D2A9-4D6D-AC3B-29F370D22C97
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2c392b3915443da2f287a5511f3959cbb7179f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104548239"
---
# <a name="pipelines-and-shaders-with-direct3d-12"></a><span data-ttu-id="9bd23-103">Pipelines e sombreadores com o Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9bd23-103">Pipelines and Shaders with Direct3D 12</span></span>

<span data-ttu-id="9bd23-104">O pipeline programável do Direct3D 12 aumenta significativamente o desempenho de renderização em comparação com as interfaces de programação de gráficos de geração anteriores.</span><span class="sxs-lookup"><span data-stu-id="9bd23-104">The Direct3D 12 programmable pipeline significantly increases rendering performance compared to previous generation graphics programming interfaces.</span></span>

-   [<span data-ttu-id="9bd23-105">Pipeline de gráficos do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9bd23-105">Direct3D 12 graphics pipeline</span></span>](#direct3d-12-graphics-pipeline)
-   [<span data-ttu-id="9bd23-106">Objetos de estado do pipeline</span><span class="sxs-lookup"><span data-stu-id="9bd23-106">Pipeline state objects</span></span>](#pipeline-state-objects)
-   [<span data-ttu-id="9bd23-107">Pipeline de computação do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9bd23-107">Direct3D 12 compute pipeline</span></span>](#direct3d-12-compute-pipeline)
-   [<span data-ttu-id="9bd23-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9bd23-108">Related topics</span></span>](#related-topics)

## <a name="direct3d-12-graphics-pipeline"></a><span data-ttu-id="9bd23-109">Pipeline de gráficos do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9bd23-109">Direct3D 12 graphics pipeline</span></span>

<span data-ttu-id="9bd23-110">O diagrama a seguir ilustra o pipeline de gráficos do Direct3D 12 e o estado.</span><span class="sxs-lookup"><span data-stu-id="9bd23-110">The following diagram illustrates the Direct3D 12 graphics pipeline and state.</span></span>

![diagrama que ilustra o pipeline e o estado do Direct3D 12](images/pipeline.png)

<span data-ttu-id="9bd23-112">Um pipeline de gráficos é o fluxo sequencial de entradas de dados e saídas à medida que a GPU renderiza quadros.</span><span class="sxs-lookup"><span data-stu-id="9bd23-112">A graphics pipeline is the sequential flow of data inputs and outputs as the GPU renders frames.</span></span> <span data-ttu-id="9bd23-113">Considerando o estado do pipeline e as entradas, a GPU executa uma série de operações para criar as imagens resultantes.</span><span class="sxs-lookup"><span data-stu-id="9bd23-113">Given the pipeline state and inputs, the GPU performs a series of operations to create the resulting images.</span></span> <span data-ttu-id="9bd23-114">Um pipeline de gráficos contém sombreadores, que executam efeitos de renderização programáveis e cálculos e operações de função fixas.</span><span class="sxs-lookup"><span data-stu-id="9bd23-114">A graphics pipeline contains shaders, which perform programmable rendering effects and calculations, and fixed function operations.</span></span>

<span data-ttu-id="9bd23-115">Observe o seguinte ao fazer referência ao diagrama de estado do pipeline:</span><span class="sxs-lookup"><span data-stu-id="9bd23-115">Note the following when referring to the pipeline state diagram:</span></span>

-   <span data-ttu-id="9bd23-116">As tabelas de descritores e os heaps podem ser organizados arbitrariamente: SRVs, CBVs e UAVs podem ser referenciados e alocados em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="9bd23-116">The descriptor tables and heaps can be arbitrarily arranged: SRVs, CBVs and UAVs can be referenced and allocated in any order.</span></span>
-   <span data-ttu-id="9bd23-117">Algumas operações do pipeline são configuráveis.</span><span class="sxs-lookup"><span data-stu-id="9bd23-117">Some operations of the pipeline are configurable.</span></span> <span data-ttu-id="9bd23-118">Por exemplo, a mesclagem de saída normalmente opera em uma base de leitura-modificação-gravação com as exibições de destino de renderização e estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="9bd23-118">For example, the output merger typically operates on a read-modify-write basis with the render target and depth stencil views.</span></span> <span data-ttu-id="9bd23-119">No entanto, o pipeline pode ser configurado para que qualquer uma dessas exibições seja somente leitura ou somente gravação.</span><span class="sxs-lookup"><span data-stu-id="9bd23-119">However the pipeline can be configured so that either of these views are read-only or write-only.</span></span>
-   <span data-ttu-id="9bd23-120">Os exemplos estáticos não fazem parte dos argumentos raiz, pois são estáticos.</span><span class="sxs-lookup"><span data-stu-id="9bd23-120">Static samplers are not part of the root arguments since they are static.</span></span>

## <a name="pipeline-state-objects"></a><span data-ttu-id="9bd23-121">Objetos de estado do pipeline</span><span class="sxs-lookup"><span data-stu-id="9bd23-121">Pipeline state objects</span></span>

<span data-ttu-id="9bd23-122">O Direct3D 12 apresenta o PSO (objeto de estado de pipeline).</span><span class="sxs-lookup"><span data-stu-id="9bd23-122">Direct3D 12 introduces the pipeline state object (PSO).</span></span> <span data-ttu-id="9bd23-123">Em vez de armazenar e representar o estado do pipeline em um grande número de objetos de alto nível, os Estados dos componentes de pipeline, como o Assembler de entrada, rasterizador, sombreador de pixel e a fusão de saída, são armazenados em um PSO.</span><span class="sxs-lookup"><span data-stu-id="9bd23-123">Rather than storing and representing pipeline state across a large number of high-level objects, the states of pipeline components like the input assembler, rasterizer, pixel shader, and output merger are stored in a PSO.</span></span> <span data-ttu-id="9bd23-124">Um PSO é um objeto de estado de pipeline unificado que é imutável após a criação.</span><span class="sxs-lookup"><span data-stu-id="9bd23-124">A PSO is a unified pipeline state object that is immutable after creation.</span></span> <span data-ttu-id="9bd23-125">O PSO selecionado no momento pode ser alterado de forma rápida e dinâmica, e o hardware e os drivers podem converter diretamente um PSO em instruções de hardware nativo e estado, preparando a GPU para o processamento de gráficos.</span><span class="sxs-lookup"><span data-stu-id="9bd23-125">The currently selected PSO can be changed quickly and dynamically, and the hardware and drivers can directly convert a PSO into native hardware instructions and state, readying the GPU for graphics processing.</span></span> <span data-ttu-id="9bd23-126">Para aplicar um PSO, o hardware copia uma quantidade mínima de Estado previamente computado diretamente nos registros de hardware.</span><span class="sxs-lookup"><span data-stu-id="9bd23-126">To apply a PSO, the hardware copies a minimal amount of pre-computed state directly to the hardware registers.</span></span> <span data-ttu-id="9bd23-127">Isso remove a sobrecarga causada pelo driver de gráficos recomputando continuamente o estado do hardware com base em todas as configurações de pipeline e renderização aplicáveis no momento.</span><span class="sxs-lookup"><span data-stu-id="9bd23-127">This removes the overhead caused by the graphics driver continually recomputing hardware state based on all currently applicable rendering and pipeline settings.</span></span> <span data-ttu-id="9bd23-128">O resultado é significativamente reduzido de forma significativa a sobrecarga de chamada, melhor desempenho e mais chamadas de desenho por quadro.</span><span class="sxs-lookup"><span data-stu-id="9bd23-128">The result is significantly reduced draw call overhead, increased performance, and more draw calls per frame.</span></span>

<span data-ttu-id="9bd23-129">O PSO aplicado atualmente define e conecta todos os sombreadores que estão sendo usados no pipeline de renderização.</span><span class="sxs-lookup"><span data-stu-id="9bd23-129">The currently applied PSO defines and connects all of the shaders being used in the rendering pipeline.</span></span> <span data-ttu-id="9bd23-130">A [HLSL (linguagem de sombreamento de alto nível) da Microsoft](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) é pré-compilado em objetos de sombreador, que são usados em tempo de execução como entrada para objetos de estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="9bd23-130">[Microsoft High Level Shader Language (HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) is pre-compiled into shader objects, which are then used at run time as input for pipeline state objects.</span></span> <span data-ttu-id="9bd23-131">Para obter mais informações sobre como as funções PSO no pipeline de gráficos, consulte [Gerenciando o estado do pipeline de gráficos no Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="9bd23-131">For more information about how the PSO functions within the graphics pipeline, see [Managing graphics pipeline state in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).</span></span>

## <a name="direct3d-12-compute-pipeline"></a><span data-ttu-id="9bd23-132">Pipeline de computação do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9bd23-132">Direct3D 12 compute pipeline</span></span>

<span data-ttu-id="9bd23-133">O diagrama a seguir ilustra o pipeline de computação do Direct3D 12 e o estado.</span><span class="sxs-lookup"><span data-stu-id="9bd23-133">The following diagram illustrates the Direct3D 12 compute pipeline and state.</span></span>

![Diagrama que mostra o pipeline de computação do Direct3D 12.](images/compute-pipeline.png)

<span data-ttu-id="9bd23-135">Não há unidades de função fixas nesse pipeline, no entanto, heaps de descritores, heaps de amostra e amostras estáticas ainda estão disponíveis em computação.</span><span class="sxs-lookup"><span data-stu-id="9bd23-135">There are no fixed function units in this pipeline, however descriptor heaps, sampler heaps and static samplers are still available in compute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bd23-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9bd23-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bd23-137">Envio de trabalho no Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9bd23-137">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)
</dt> </dl>

 

 