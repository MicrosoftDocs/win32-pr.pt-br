---
title: Contadores de saída de fluxo
description: A saída de fluxo é a capacidade da GPU de gravar vértices em um buffer. Os contadores de saída do fluxo monitoram o progresso.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103773"
---
# <a name="stream-output-counters"></a><span data-ttu-id="80350-104">Contadores de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="80350-104">Stream Output Counters</span></span>

<span data-ttu-id="80350-105">A saída de fluxo é a capacidade da GPU de gravar vértices em um buffer.</span><span class="sxs-lookup"><span data-stu-id="80350-105">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="80350-106">Os contadores de saída do fluxo monitoram o progresso.</span><span class="sxs-lookup"><span data-stu-id="80350-106">The stream output counters monitor progress.</span></span>

-   [<span data-ttu-id="80350-107">Diferenças nos contadores de fluxo do Direct3D 11 para o Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="80350-107">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [<span data-ttu-id="80350-108">BufferFilledSize</span><span class="sxs-lookup"><span data-stu-id="80350-108">BufferFilledSize</span></span>](#bufferfilledsize)
-   [<span data-ttu-id="80350-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80350-109">Related topics</span></span>](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="80350-110">Diferenças nos contadores de fluxo do Direct3D 11 para o Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="80350-110">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>

<span data-ttu-id="80350-111">Como parte do processo de saída de fluxo, a GPU precisa saber o local atual no buffer em que está gravando.</span><span class="sxs-lookup"><span data-stu-id="80350-111">As a part of the stream output process, the GPU has to know the current location in the buffer that it is writing to.</span></span> <span data-ttu-id="80350-112">No Direct3D 11, a memória para armazenar esse local é alocada pelo driver e a única maneira de os aplicativos manipular esse valor é por meio do método **SOSetTargets** .</span><span class="sxs-lookup"><span data-stu-id="80350-112">In Direct3D 11, memory to store this location is allocated by the driver and the only way for applications to manipulate this value is via the **SOSetTargets** method.</span></span> <span data-ttu-id="80350-113">No Direct3D 12, os aplicativos alocam memória para armazenar esse local atual.</span><span class="sxs-lookup"><span data-stu-id="80350-113">In Direct3D 12, apps allocate memory to store this current location.</span></span> <span data-ttu-id="80350-114">Não há maneiras especiais de manipular esse valor, e os aplicativos são livres para ler/gravar o valor com a CPU ou a GPU.</span><span class="sxs-lookup"><span data-stu-id="80350-114">There are no special ways to manipulate this value, and apps are free to read/write the value with the CPU or GPU.</span></span>

## <a name="bufferfilledsize"></a><span data-ttu-id="80350-115">BufferFilledSize</span><span class="sxs-lookup"><span data-stu-id="80350-115">BufferFilledSize</span></span>

<span data-ttu-id="80350-116">O aplicativo é responsável por alocar armazenamento para uma quantidade de 32 bits chamada *BufferFilledSize*.</span><span class="sxs-lookup"><span data-stu-id="80350-116">The application is responsible for allocating storage for a 32-bit quantity called the *BufferFilledSize*.</span></span> <span data-ttu-id="80350-117">Contém o número de bytes de dados no buffer de saída de fluxo.</span><span class="sxs-lookup"><span data-stu-id="80350-117">This contains the number of bytes of data in the stream-output buffer.</span></span> <span data-ttu-id="80350-118">Esse armazenamento pode ser colocado no mesmo recurso, ou em outro, como aquele que contém os dados de saída de fluxo.</span><span class="sxs-lookup"><span data-stu-id="80350-118">This storage can be placed in the same, or a different, resource as the one that contains the stream-output data.</span></span> <span data-ttu-id="80350-119">Esse valor é acessado pela GPU no estágio Stream-Output para determinar onde acrescentar novos dados de vértice no buffer.</span><span class="sxs-lookup"><span data-stu-id="80350-119">This value is accessed by the GPU in the stream-output stage to determine where to append new vertex data in the buffer.</span></span> <span data-ttu-id="80350-120">Além disso, esse valor é acessado pela GPU para determinar quando o estouro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="80350-120">Additionally, this value is accessed by the GPU to determine when overflow has occurred.</span></span>

<span data-ttu-id="80350-121">Consulte o D3D12 de [**saída de fluxo de estrutura \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span><span class="sxs-lookup"><span data-stu-id="80350-121">Refer to the structure [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span></span>

<span data-ttu-id="80350-122">A camada de depuração validará o seguinte em [**ID3D12GraphicsCommandList:: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span><span class="sxs-lookup"><span data-stu-id="80350-122">The debug layer will validate the following in [**ID3D12GraphicsCommandList::SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span></span>

-   <span data-ttu-id="80350-123">*BufferFilledSize* cai no intervalo implícito por {*OffsetInBytes*, *sizeInBytes*}, se um recurso não nulo for especificado.</span><span class="sxs-lookup"><span data-stu-id="80350-123">*BufferFilledSize* falls in the range implied by {*OffsetInBytes*, *SizeInBytes*}, if a non-NULL resource is specified.</span></span>
-   <span data-ttu-id="80350-124">*BufferFilledSizeOffsetInBytes* é um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="80350-124">*BufferFilledSizeOffsetInBytes* is a multiple of 4.</span></span>
-   <span data-ttu-id="80350-125">*BufferFilledSizeOffsetInBytes* está dentro do intervalo do recurso que o contém.</span><span class="sxs-lookup"><span data-stu-id="80350-125">*BufferFilledSizeOffsetInBytes* is within the range of the containing resource.</span></span>
-   <span data-ttu-id="80350-126">O recurso especificado é um buffer.</span><span class="sxs-lookup"><span data-stu-id="80350-126">The specified resource is a buffer.</span></span>

<span data-ttu-id="80350-127">O tempo de execução não validará o tipo de heap associado ao buffer de saída de fluxo, pois a saída de fluxo terá suporte em todos os tipos de heap.</span><span class="sxs-lookup"><span data-stu-id="80350-127">The runtime will not validate the heap type associated with the stream output buffer, as stream output is supported in all heap types.</span></span>

<span data-ttu-id="80350-128">As assinaturas raiz devem especificar se a saída do fluxo será usada usando os sinalizadores de [**\_ \_ \_ sinalizadores de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) .</span><span class="sxs-lookup"><span data-stu-id="80350-128">Root signatures must specify if stream output will be used, by using the [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags.</span></span>

<span data-ttu-id="80350-129">\_ \_ O sinalizador de assinatura raiz D3D12 \_ \_ permitirá que \_ \_ a saída de fluxo possa ser especificada para assinaturas raiz criadas em HLSL, de maneira semelhante a como os outros sinalizadores são especificados.</span><span class="sxs-lookup"><span data-stu-id="80350-129">D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT can be specified for root signatures authored in HLSL, in a manner similar to how the other flags are specified.</span></span>

<span data-ttu-id="80350-130">[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) falhará se o sombreador de geometria contiver Stream-output, mas a assinatura raiz não tiver o sinalizador de \_ assinatura raiz D3D12 \_ \_ \_ permitir \_ conjunto de sinalizadores de saída de fluxo \_ .</span><span class="sxs-lookup"><span data-stu-id="80350-130">[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) will fail if the geometry shader contains stream-output but the root signature does not have the D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT flag set.</span></span>

<span data-ttu-id="80350-131">Quando um recurso é usado como um destino de saída de fluxo, os recursos usados devem estar no \_ estado do fluxo de estado do recurso D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="80350-131">When a resource is used as a stream-output target, the resources used must be in the D3D12\_RESOURCE\_STATE\_STREAM\_OUT state.</span></span> <span data-ttu-id="80350-132">Isso se aplica aos dados de vértice e ao *BufferFilledSize* (que pode estar nos mesmos ou em recursos separados).</span><span class="sxs-lookup"><span data-stu-id="80350-132">This applies to both the vertex data and the *BufferFilledSize* (which can be in the same or separate resources).</span></span>

<span data-ttu-id="80350-133">Não há nenhuma API especial para definir deslocamentos de buffer de saída de fluxo porque os aplicativos podem gravar no *BufferFilledSize* com a CPU ou GPU diretamente.</span><span class="sxs-lookup"><span data-stu-id="80350-133">There are no special APIs to set stream-output buffer offsets because applications can write to the *BufferFilledSize* with the CPU or GPU directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80350-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80350-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80350-135">Contadores e consultas</span><span class="sxs-lookup"><span data-stu-id="80350-135">Counters and Queries</span></span>](counters-and-queries.md)
</dt> </dl>

 

 




