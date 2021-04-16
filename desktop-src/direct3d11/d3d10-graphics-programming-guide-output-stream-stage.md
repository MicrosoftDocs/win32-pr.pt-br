---
title: Estágio de Stream-Output
description: A finalidade do estágio Stream-output é gerar continuamente (ou transmitir) dados de vértice do estágio Geometry-Shader (ou o estágio Vertex-Shader se o estágio Geometry-Shader estiver inativo) em um ou mais buffers na memória (consulte Introdução com o estágio Stream-Output).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- estágio de saída de fluxo (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0879cde2ba2f1bb3ed9cc6121aaf378cd4af312
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104454468"
---
# <a name="stream-output-stage"></a><span data-ttu-id="6933d-104">Estágio de Stream-Output</span><span class="sxs-lookup"><span data-stu-id="6933d-104">Stream-Output Stage</span></span>

<span data-ttu-id="6933d-105">A finalidade do estágio Stream-output é gerar continuamente (ou transmitir) dados de vértice do estágio Geometry-Shader (ou o estágio Vertex-Shader se o estágio Geometry-Shader estiver inativo) em um ou mais buffers na memória (consulte [introdução com o estágio Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span><span class="sxs-lookup"><span data-stu-id="6933d-105">The purpose of the stream-output stage is to continuously output (or stream) vertex data from the geometry-shader stage (or the vertex-shader stage if the geometry-shader stage is inactive) to one or more buffers in memory (see [Getting Started with the Stream-Output Stage](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span></span>

<span data-ttu-id="6933d-106">O estágio Stream-Output (por isso) está localizado no pipeline logo após o estágio Geometry-Shader e logo antes do estágio de rasterização, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="6933d-106">The stream-output stage (SO) is located in the pipeline right after the geometry-shader stage and just before the rasterization stage, as shown in the following diagram.</span></span>

![diagrama da localização do estágio de saída de fluxo no pipeline](images/d3d10-pipeline-stages-so.png)

<span data-ttu-id="6933d-108">Os dados transmitidos para a memória podem ser lidos de volta no pipeline em uma passagem de renderização subsequente, ou podem ser copiados para um recurso de preparo (para que possam ser lidos pela CPU).</span><span class="sxs-lookup"><span data-stu-id="6933d-108">Data streamed out to memory can be read back into the pipeline in a subsequent rendering pass, or can be copied to a staging resource (so it can be read by the CPU).</span></span> <span data-ttu-id="6933d-109">A quantidade de dados transmitidos pode variar; a API [**ID3D11DeviceContext::D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) foi projetada para lidar com os dados sem a necessidade de consultar (a GPU) sobre a quantidade de dados gravados.</span><span class="sxs-lookup"><span data-stu-id="6933d-109">The amount of data streamed out can vary; the [**ID3D11DeviceContext::DrawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) API is designed to handle the data without the need to query (the GPU) about the amount of data written.</span></span>

<span data-ttu-id="6933d-110">Quando um triângulo ou uma faixa de linha está associado ao estágio de Assembler de entrada, cada faixa é convertida em uma lista antes de ser transmitida. Os vértices são sempre escritos como primitivos completos (por exemplo, três vértices por vez para triângulos); primitivos incompletos nunca são transmitidos. Tipos primitivos com adjacência descartam os dados de adjacência antes de transmitir os dados.</span><span class="sxs-lookup"><span data-stu-id="6933d-110">When a triangle or line strip is bound to the input-assembler stage, each strip is converted into a list before they are streamed out. Vertices are always written out as complete primitives (for example, 3 vertices at a time for triangles); incomplete primitives are never streamed out. Primitive types with adjacency discard the adjacency data before streaming data out.</span></span>

<span data-ttu-id="6933d-111">Há duas maneiras de fornecer dados de saída de fluxo para o pipeline:</span><span class="sxs-lookup"><span data-stu-id="6933d-111">There are two ways to feed stream-output data into the pipeline:</span></span>

-   <span data-ttu-id="6933d-112">Os dados de saída de fluxo podem ser devolvidos para o estágio de Assembler de entrada.</span><span class="sxs-lookup"><span data-stu-id="6933d-112">Stream-output data can be fed back into the input-assembler stage.</span></span>
-   <span data-ttu-id="6933d-113">Os dados de saída de fluxo podem ser lidos por sombreadores programáveis usando funções de carga (como [carga](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span><span class="sxs-lookup"><span data-stu-id="6933d-113">Stream-output data can be read by programmable shaders using load functions (such as [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span></span>

<span data-ttu-id="6933d-114">Para usar um buffer como um recurso de saída de fluxo, crie o buffer com o sinalizador de [**\_ saída do \_ fluxo \_ de associação D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="6933d-114">To use a buffer as a stream-output resource, create the buffer with the [**D3D11\_BIND\_STREAM\_OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) flag.</span></span> <span data-ttu-id="6933d-115">O estágio de saída de fluxo dá suporte a até 4 buffers simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="6933d-115">The stream-output stage supports up to 4 buffers simultaneously.</span></span>

-   <span data-ttu-id="6933d-116">Se você estiver transmitindo dados em vários buffers, cada buffer pode capturar apenas um único elemento (até 4 componentes) de dados por vértice, com uma distância de dados implícita igual à largura do elemento em cada buffer (compatível com a maneira como os buffers de elemento único podem ser vinculados para a entrada em estágios de sombreador).</span><span class="sxs-lookup"><span data-stu-id="6933d-116">If you are streaming data into multiple buffers, each buffer can only capture a single element (up to 4 components) of per-vertex data, with an implied data stride equal to the element width in each buffer (compatible with the way single element buffers can be bound for input into shader stages).</span></span> <span data-ttu-id="6933d-117">Além disso, se os buffers tiverem tamanhos diferentes, a escrita é interrompida assim que qualquer um dos buffers estiver cheio.</span><span class="sxs-lookup"><span data-stu-id="6933d-117">Furthermore, if the buffers have different sizes, writing stops as soon as any one of the buffers is full.</span></span>
-   <span data-ttu-id="6933d-118">Se você estiver transmitindo dados em um único buffer, o buffer pode capturar até 64 componentes escalares de dados por vértice (256 bytes ou menos) ou a distância de vértice pode ser de até 2048 bytes.</span><span class="sxs-lookup"><span data-stu-id="6933d-118">If you are streaming data into a single buffer, the buffer can capture up to 64 scalar components of per-vertex data (256 bytes or less) or the vertex stride can be up to 2048 bytes.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="6933d-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6933d-119">In this section</span></span>



| <span data-ttu-id="6933d-120">Tópico</span><span class="sxs-lookup"><span data-stu-id="6933d-120">Topic</span></span>                                                                                                                               | <span data-ttu-id="6933d-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="6933d-121">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6933d-122">Introdução com o estágio de Stream-Output</span><span class="sxs-lookup"><span data-stu-id="6933d-122">Getting Started with the Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | <span data-ttu-id="6933d-123">Esta seção descreve como usar um sombreador de geometria com o estágio de saída de fluxo.</span><span class="sxs-lookup"><span data-stu-id="6933d-123">This section describes how to use a geometry shader with the stream output stage.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="6933d-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6933d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6933d-125">Pipeline de gráficos</span><span class="sxs-lookup"><span data-stu-id="6933d-125">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="6933d-126">Estágios de pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="6933d-126">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

