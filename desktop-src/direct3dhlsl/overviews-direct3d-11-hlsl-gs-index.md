---
title: Como indexar vários fluxos de saída
description: No sombreador modelo 5, um sombreador Geometry pode dar suporte a até quatro fluxos separados. Isso significa que um único sombreador pode gerar uma saída entre um e quatro fluxos de saída, dependendo do número de fluxos declarados.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8564917be9565e862043e370840f8ac7280f174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004991"
---
# <a name="how-to-index-multiple-output-streams"></a><span data-ttu-id="e59fe-104">Como: indexar vários fluxos de saída</span><span class="sxs-lookup"><span data-stu-id="e59fe-104">How To: Index Multiple Output Streams</span></span>

<span data-ttu-id="e59fe-105">No sombreador modelo 5, um sombreador Geometry pode dar suporte a até quatro fluxos separados.</span><span class="sxs-lookup"><span data-stu-id="e59fe-105">In shader model 5, a geometry shader can support up to 4 separate streams.</span></span> <span data-ttu-id="e59fe-106">Isso significa que um único sombreador pode gerar uma saída entre um e quatro fluxos de saída, dependendo do número de fluxos declarados.</span><span class="sxs-lookup"><span data-stu-id="e59fe-106">This means a single shader can output between one and four output streams, depending on the number of streams declared.</span></span>

<span data-ttu-id="e59fe-107">Para indexar vários fluxos de saída</span><span class="sxs-lookup"><span data-stu-id="e59fe-107">To index multiple output streams</span></span>

1.  <span data-ttu-id="e59fe-108">Defina um fluxo de dados usando um tipo de modelo de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e59fe-108">Define a data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  <span data-ttu-id="e59fe-109">Defina um segundo fluxo de dados usando um tipo de modelo de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e59fe-109">Define a second data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  <span data-ttu-id="e59fe-110">Dados de saída para (ou ambos) fluxos usando as funções intrínsecas do objeto de saída de fluxo (como Append ou RestartStrip).</span><span class="sxs-lookup"><span data-stu-id="e59fe-110">Output data to either (or both) streams using the stream output object intrinsic functions (such as Append or RestartStrip).</span></span>

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

<span data-ttu-id="e59fe-111">Ao usar um único fluxo de saída, você pode emitir faixas de triângulo, faixas de linha ou listas de pontos.</span><span class="sxs-lookup"><span data-stu-id="e59fe-111">When using a single output stream, you can emit triangle strips, line strips, or point lists.</span></span> <span data-ttu-id="e59fe-112">Quando você armazena as faixas de triângulo e de linha no buffer de saída de fluxo, elas são expandidas para listas de linhas e triângulos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e59fe-112">When you store triangle and line strips in the stream out buffer, they are expanded to triangle and line lists respectively.</span></span> <span data-ttu-id="e59fe-113">Você também pode rasterizar um fluxo e não enviá-lo para um buffer de memória.</span><span class="sxs-lookup"><span data-stu-id="e59fe-113">You can also rasterize one stream and not send it to a memory buffer.</span></span>

<span data-ttu-id="e59fe-114">Ao usar vários fluxos de saída, todos os fluxos devem conter pontos e até um fluxo de saída pode ser enviado para o rasterizador.</span><span class="sxs-lookup"><span data-stu-id="e59fe-114">When using multiple output streams, all streams must contain points, and up to one output stream can be sent to the rasterizer.</span></span> <span data-ttu-id="e59fe-115">Mais comumente, um aplicativo não rasterizará nenhum fluxo.</span><span class="sxs-lookup"><span data-stu-id="e59fe-115">More commonly, an application will not rasterize any stream.</span></span>

<span data-ttu-id="e59fe-116">Depois de transmitir dados para um buffer, você pode usar esses dados para renderizar qualquer tipo primitivo, não apenas o tipo primitivo que você usou para preencher o buffer.</span><span class="sxs-lookup"><span data-stu-id="e59fe-116">After you stream data to a buffer, you can use that data to render any primitive type, not just the primitive type that you used to fill the buffer.</span></span>

<span data-ttu-id="e59fe-117">A saída total do sombreador Geometry é limitada a 1024 escalares.</span><span class="sxs-lookup"><span data-stu-id="e59fe-117">The total output of the geometry shader is limited to 1024 scalars.</span></span> <span data-ttu-id="e59fe-118">Quando há vários fluxos, o número de escalares é computado do maior tipo de fluxo multiplicado pela contagem máxima de vértices.</span><span class="sxs-lookup"><span data-stu-id="e59fe-118">When multiple streams exist, the number of scalars is computed from the largest stream type multiplied by the maximum vertex count.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e59fe-119">Diferenças entre o modelo de sombreador 4 e o modelo de sombreador 5:</span><span class="sxs-lookup"><span data-stu-id="e59fe-119">Differences between shader model 4 and shader model 5:</span></span><br/> <span data-ttu-id="e59fe-120">Modelo do sombreador 4:</span><span class="sxs-lookup"><span data-stu-id="e59fe-120">Shader model 4:</span></span><br/>
<ul>
<li><span data-ttu-id="e59fe-121">O número máximo de escalares para a saída do fluxo é 64.</span><span class="sxs-lookup"><span data-stu-id="e59fe-121">Maximum number of scalars for stream output is 64.</span></span></li>
<li><span data-ttu-id="e59fe-122">A máscara de registro por componente deve corresponder ao intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="e59fe-122">The per-component register mask must match across the index range.</span></span></li>
</ul>
<span data-ttu-id="e59fe-123">Modelo do sombreador 5:</span><span class="sxs-lookup"><span data-stu-id="e59fe-123">Shader model 5:</span></span><br/>
<ul>
<li><span data-ttu-id="e59fe-124">O número máximo de escalares para a saída do fluxo é 128.</span><span class="sxs-lookup"><span data-stu-id="e59fe-124">Maximum number of scalars for stream output is 128.</span></span></li>
<li><span data-ttu-id="e59fe-125">A máscara de registro por componente não precisa corresponder ao intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="e59fe-125">The per-component register mask does not need to match across the index range.</span></span></li>
<li><span data-ttu-id="e59fe-126">A indexação dinâmica de saídas deve ser válida em todos os fluxos.</span><span class="sxs-lookup"><span data-stu-id="e59fe-126">Dynamic indexing of outputs must be legal across all streams.</span></span></li>
<li><span data-ttu-id="e59fe-127">Os modos de interpolação não precisam corresponder aos fluxos.</span><span class="sxs-lookup"><span data-stu-id="e59fe-127">Interpolation modes do not need to match for the streams.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e59fe-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e59fe-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e59fe-129">Recursos do sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="e59fe-129">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





