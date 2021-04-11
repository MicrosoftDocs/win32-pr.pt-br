---
description: O pipeline de gráficos do Direct3D 10 representa uma mudança fundamental na arquitetura, recriada a partir do início em hardware e software para capacitar a próxima geração de jogos e de aplicativos multimídia 3D.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Recursos de API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab12285509441bb429c78d995e68ed1753ceb5bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163963"
---
# <a name="api-features-direct3d-10"></a><span data-ttu-id="d7b4c-103">Recursos de API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d7b4c-103">API Features (Direct3D 10)</span></span>

<span data-ttu-id="d7b4c-104">O pipeline de gráficos do Direct3D 10 representa uma mudança fundamental na arquitetura, recriada a partir do início em hardware e software para capacitar a próxima geração de jogos e de aplicativos multimídia 3D.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-104">The Direct3D 10 graphics pipeline represents a fundamental architecture change, rebuilt from the ground-up in hardware and software to power the next-generation of games and 3D multimedia applications.</span></span> <span data-ttu-id="d7b4c-105">Ele usa o WDDM (modelo de driver de vídeo) do Windows, que permite aprimoramentos de desempenho e comportamento, como a memória da GPU virtual.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-105">It uses the Windows Display Driver Model (WDDM), which enables performance and behavioral enhancements such as virtual GPU memory.</span></span>

<span data-ttu-id="d7b4c-106">Os desenvolvedores familiarizados com o Direct3D 9 descobrirão uma série de aprimoramentos funcionais e melhorias de desempenho no Direct3D 10, incluindo:</span><span class="sxs-lookup"><span data-stu-id="d7b4c-106">Developers familiar with Direct3D 9 will discover a series of functional enhancements and performance improvements in Direct3D 10, including:</span></span>

-   <span data-ttu-id="d7b4c-107">A capacidade de processar primitivos inteiros no novo [estágio Geometry-Shader](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d7b4c-107">The ability to process entire primitives in the new [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span>
-   <span data-ttu-id="d7b4c-108">A capacidade de produzir dados de vértice gerados por pipeline para a memória usando o [estágio Stream-output](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span><span class="sxs-lookup"><span data-stu-id="d7b4c-108">The ability to output pipeline-generated vertex data to memory using the [stream-output stage](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span></span>
-   <span data-ttu-id="d7b4c-109">Organização do estado do pipeline em 5 [objetos de estado](d3d10-graphics-programming-guide-api-features-state-objects.md)imutáveis, permitindo a configuração rápida do pipeline.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-109">Organization of pipeline state into 5 immutable [state objects](d3d10-graphics-programming-guide-api-features-state-objects.md), enabling fast configuration of the pipeline.</span></span>
-   <span data-ttu-id="d7b4c-110">Organização de constantes de sombreador em [buffers constantes](d3d10-graphics-programming-guide-resources-types.md), minimizando a sobrecarga de largura de banda para fornecer dados de sombreador-constante.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-110">Organization of shader constants into [constant buffers](d3d10-graphics-programming-guide-resources-types.md), minimizing bandwidth overhead for supplying shader-constant data.</span></span>
-   <span data-ttu-id="d7b4c-111">A capacidade de executar a troca de material por primitivo e a configuração usando um sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-111">The ability to perform per-primitive material swapping and setup using a geometry shader.</span></span>
-   <span data-ttu-id="d7b4c-112">Novos [tipos de recursos](d3d10-graphics-programming-guide-resources-types.md) (incluindo matrizes de textura que podem ser indexados de sombreadores) e formatos de recurso.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-112">New [resource types](d3d10-graphics-programming-guide-resources-types.md) (including texture arrays that can be indexed from shaders) and resource formats.</span></span>
-   <span data-ttu-id="d7b4c-113">Maior generalização de acesso a recursos usando uma [exibição](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="d7b4c-113">Increased generalization of resource access using a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>
-   <span data-ttu-id="d7b4c-114">Os bits de capacidade de hardware herdados (CAPS) foram removidos em favor de um conjunto avançado de funcionalidade garantida, que tem como alvo o hardware de classe Direct3D 10 (mínimo).</span><span class="sxs-lookup"><span data-stu-id="d7b4c-114">Legacy hardware capability bits (caps) have been removed in favor of a rich set of guaranteed functionality, which targets Direct3D 10-class hardware (minimum).</span></span>
-   <span data-ttu-id="d7b4c-115">[Tempo de execução em camadas](d3d10-graphics-programming-guide-api-features-layers.md) – a API do Direct3D 10 é construída com camadas, começando com a funcionalidade básica no núcleo e compilando a funcionalidade opcional e auxiliar de desenvolvedor (Debug, etc.) em camadas externas.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-115">[Layered Runtime](d3d10-graphics-programming-guide-api-features-layers.md) - The Direct3D 10 API is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality (debug, etc.) in outer layers.</span></span>
-   <span data-ttu-id="d7b4c-116">Integração total do HLSL-todos os sombreadores do Direct3D 10 são escritos em HLSL e implementados com o [núcleo do sombreador comum](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span><span class="sxs-lookup"><span data-stu-id="d7b4c-116">Full HLSL integration - All Direct3D 10 shaders are written in HLSL and implemented with the [common-shader core](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span></span>
-   <span data-ttu-id="d7b4c-117">Um aumento no número de destinos de renderização, texturas e amostras.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-117">An increase in the number of render targets, textures, and samplers.</span></span> <span data-ttu-id="d7b4c-118">Também não há nenhum limite de comprimento de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-118">There is also no shader length limit.</span></span>
-   <span data-ttu-id="d7b4c-119">Operações de sombreador de inteiros e de bits.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-119">Integer and bitwise shader operations.</span></span>
-   <span data-ttu-id="d7b4c-120">Readback de uma superfície de profundidade/estêncil ou um recurso de uma amostra, uma vez que ele não está mais associado como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-120">Readback of a depth/stencil surface or a multisampled resource, once it is no longer bound as a render target.</span></span>
-   <span data-ttu-id="d7b4c-121">Suporte de Alpha-to-Coverage com uma amostra.</span><span class="sxs-lookup"><span data-stu-id="d7b4c-121">Multisampled alpha-to-coverage support.</span></span>

<span data-ttu-id="d7b4c-122">Há diferenças de comportamento adicionais que os desenvolvedores do Direct3D 9 também devem conhecer (consulte [considerações do Direct3D 9 para o Direct3D 10](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span><span class="sxs-lookup"><span data-stu-id="d7b4c-122">There are additional behavioral differences that Direct3D 9 developers should also be aware of (see [Direct3D 9 to Direct3D 10 Considerations](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span></span>

<span data-ttu-id="d7b4c-123">Aqui está uma lista de recursos do Direct3D 9 que não têm mais suporte ou que foram revisados no Direct3D 10 (consulte [recursos preteridos](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span><span class="sxs-lookup"><span data-stu-id="d7b4c-123">Here is a list of Direct3D 9 features that either are no longer supported, or have been revised in Direct3D 10 (see [Deprecated Features](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7b4c-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7b4c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7b4c-125">Guia de programação para Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="d7b4c-125">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
