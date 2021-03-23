---
title: Predicação
description: Predicação é um recurso que habilita a GPU em vez da CPU para determinar não desenhar, copiar ou distribuir um objeto.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/20/2020
ms.locfileid: "104548293"
---
# <a name="predication"></a><span data-ttu-id="b15ae-103">Predicação</span><span class="sxs-lookup"><span data-stu-id="b15ae-103">Predication</span></span>

<span data-ttu-id="b15ae-104">Predicação é um recurso que habilita a GPU em vez da CPU para determinar não desenhar, copiar ou distribuir um objeto.</span><span class="sxs-lookup"><span data-stu-id="b15ae-104">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy, or dispatch an object.</span></span>

-   [<span data-ttu-id="b15ae-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b15ae-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="b15ae-106">SetPredication</span><span class="sxs-lookup"><span data-stu-id="b15ae-106">SetPredication</span></span>](#setpredication)
-   [<span data-ttu-id="b15ae-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b15ae-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="b15ae-108">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b15ae-108">Overview</span></span>

<span data-ttu-id="b15ae-109">O uso típico de predicação é com oclusão; se uma caixa delimitadora for desenhada e for obstruído, obviamente, não há nenhum ponto no desenho do objeto em si.</span><span class="sxs-lookup"><span data-stu-id="b15ae-109">The typical use of predication is with occlusion; if a bounding box is drawn and is occluded, there is obviously no point in drawing the object itself.</span></span> <span data-ttu-id="b15ae-110">Nessa situação, o desenho do objeto pode ser "predicado", permitindo a remoção do processamento real pela GPU.</span><span class="sxs-lookup"><span data-stu-id="b15ae-110">In this situation, the drawing of the object can be "predicated", enabling its removal from actual rendering by the GPU.</span></span>

<span data-ttu-id="b15ae-111">A princípio, isso pode parecer Redudant e acima do teste de profundidade padrão mais um passo de profundidade inicial.</span><span class="sxs-lookup"><span data-stu-id="b15ae-111">At first, this might seem redudant over and above the standard depth test plus an early depth pass.</span></span> <span data-ttu-id="b15ae-112">Mas predicação pode remover a sobrecarga do próprio estado do comando Draw, além da rasterização.</span><span class="sxs-lookup"><span data-stu-id="b15ae-112">But predication can remove the overhead of the draw command state itself, plus the rasterization.</span></span> <span data-ttu-id="b15ae-113">Embora uma passagem de profundidade inicial remova pixels desnecessários, ele ainda pode executar os sombreadores de vértice, envoltória, domínio e geometria e invocar o Assembler de entrada de função fixa, o tesselator e o rasterizador.</span><span class="sxs-lookup"><span data-stu-id="b15ae-113">While an early depth pass removes unnecessary pixels, it can still execute vertex, hull, domain, and geometry shaders, and invoke the fixed-function input assembler, tesselator, and rasterizer.</span></span> <span data-ttu-id="b15ae-114">Ao desenhar uma caixa delimitadora simples ou um volume delimitador semelhante &mdash; , que é mais simples de processar e rasterizar do que o modelo real &mdash; , você evita a rasterização e o processamento desnecessários.</span><span class="sxs-lookup"><span data-stu-id="b15ae-114">By drawing a simple bounding box or similar bounding volume&mdash;which is simpler to process and rasterize than the real model&mdash;you avoid unnecessary rasterization and processing.</span></span>

<span data-ttu-id="b15ae-115">Ao contrário do Direct3D 11, o predicação é dissociado de consultas e é expandido no Direct3D 12 para permitir que um aplicativo para objetos de predicado com base em qualquer motivo pelo qual o desenvolvedor do aplicativo possa decidir (não apenas oclusão).</span><span class="sxs-lookup"><span data-stu-id="b15ae-115">Unlike Direct3D 11, predication is decoupled from queries, and is expanded in Direct3D 12 to enable an application to predicate objects based on any reasoning the app developer may decide on (not just occlusion).</span></span>

## <a name="setpredication"></a><span data-ttu-id="b15ae-116">SetPredication</span><span class="sxs-lookup"><span data-stu-id="b15ae-116">SetPredication</span></span>

<span data-ttu-id="b15ae-117">Predicação pode ser definido com base no valor de 64 bits em um buffer (consulte [**D3D12 \_ predicação \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span><span class="sxs-lookup"><span data-stu-id="b15ae-117">Predication can be set based on the value of 64-bits within a buffer (refer to [**D3D12\_PREDICATION\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span></span>

<span data-ttu-id="b15ae-118">Quando a GPU executa um comando [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) , ele ajusta o valor no buffer.</span><span class="sxs-lookup"><span data-stu-id="b15ae-118">When the GPU executes a [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) command it snaps the value in the buffer.</span></span> <span data-ttu-id="b15ae-119">Alterações futuras nos dados no buffer não afetam retroativamente o estado predicação.</span><span class="sxs-lookup"><span data-stu-id="b15ae-119">Future changes to the data in the buffer do not retroactively affect the predication state.</span></span>

<span data-ttu-id="b15ae-120">Se o buffer de parâmetro de entrada for nulo, predicação será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b15ae-120">If the input parameter Buffer is NULL, then predication is disabled.</span></span>

<span data-ttu-id="b15ae-121">As dicas de predicação não estão presentes na API do Direct3D 12; e predicação é permitido em listas de comando direta, de computação e de cópia.</span><span class="sxs-lookup"><span data-stu-id="b15ae-121">Predication hints are not present in the Direct3D 12 API; and predication is allowed on direct, compute, and copy command lists.</span></span> <span data-ttu-id="b15ae-122">O buffer de origem pode estar em qualquer tipo de heap (padrão, carregar, readback, personalizado).</span><span class="sxs-lookup"><span data-stu-id="b15ae-122">The source buffer can be in any heap type (default, upload, readback, custom).</span></span>

<span data-ttu-id="b15ae-123">O tempo de execução principal validará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b15ae-123">The core runtime will validate the following:</span></span>

-   <span data-ttu-id="b15ae-124">*AlignedBufferOffset* é um múltiplo de 8 bytes</span><span class="sxs-lookup"><span data-stu-id="b15ae-124">*AlignedBufferOffset* is a multiple of 8 bytes</span></span>
-   <span data-ttu-id="b15ae-125">O recurso é um buffer</span><span class="sxs-lookup"><span data-stu-id="b15ae-125">The resource is a buffer</span></span>
-   <span data-ttu-id="b15ae-126">A operação é um membro válido da enumeração</span><span class="sxs-lookup"><span data-stu-id="b15ae-126">The operation is a valid member of the enumeration</span></span>
-   <span data-ttu-id="b15ae-127">[**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) não pode ser chamado de dentro de um pacote</span><span class="sxs-lookup"><span data-stu-id="b15ae-127">[**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) cannot be called from within a bundle</span></span>
-   <span data-ttu-id="b15ae-128">O tipo de lista de comandos dá suporte a predicação</span><span class="sxs-lookup"><span data-stu-id="b15ae-128">The command list type supports predication</span></span>
-   <span data-ttu-id="b15ae-129">O deslocamento não excede o tamanho do buffer</span><span class="sxs-lookup"><span data-stu-id="b15ae-129">The offset does not exceed the buffer size</span></span>

<span data-ttu-id="b15ae-130">A camada de depuração emitirá um erro se o buffer de origem não estiver na [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (que é a mesma do estado [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)e simplesmente um alias).</span><span class="sxs-lookup"><span data-stu-id="b15ae-130">The debug layer will issue an error if the source buffer is not in the [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (which is the same as [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states), and simply an alias) state.</span></span>

<span data-ttu-id="b15ae-131">O conjunto de operações que podem ser preparadas são:</span><span class="sxs-lookup"><span data-stu-id="b15ae-131">The set of operations which can be predicated are:</span></span>

-   [<span data-ttu-id="b15ae-132">**DrawInstanced**</span><span class="sxs-lookup"><span data-stu-id="b15ae-132">**DrawInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [<span data-ttu-id="b15ae-133">**DrawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="b15ae-133">**DrawIndexedInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [<span data-ttu-id="b15ae-134">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="b15ae-134">**Dispatch**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="b15ae-135">**CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="b15ae-135">**CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="b15ae-136">**CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="b15ae-136">**CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="b15ae-137">**CopyResource**</span><span class="sxs-lookup"><span data-stu-id="b15ae-137">**CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="b15ae-138">**CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="b15ae-138">**CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="b15ae-139">**ResolveSubresource**</span><span class="sxs-lookup"><span data-stu-id="b15ae-139">**ResolveSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [<span data-ttu-id="b15ae-140">**ClearDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="b15ae-140">**ClearDepthStencilView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [<span data-ttu-id="b15ae-141">**ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="b15ae-141">**ClearRenderTargetView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [<span data-ttu-id="b15ae-142">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="b15ae-142">**ClearUnorderedAccessViewUint**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="b15ae-143">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="b15ae-143">**ClearUnorderedAccessViewFloat**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="b15ae-144">**ExecuteIndirect**</span><span class="sxs-lookup"><span data-stu-id="b15ae-144">**ExecuteIndirect**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

<span data-ttu-id="b15ae-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) não é predicado.</span><span class="sxs-lookup"><span data-stu-id="b15ae-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) is not predicated itself.</span></span> <span data-ttu-id="b15ae-146">Em vez disso, as operações individuais da lista acima que estão contidas no lado do grupo são predicadas.</span><span class="sxs-lookup"><span data-stu-id="b15ae-146">Instead, individual operations from the list above which are contained in side of the bundle are predicated.</span></span>

<span data-ttu-id="b15ae-147">Os métodos ID3D12GraphicsCommandList [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) não são predicados.</span><span class="sxs-lookup"><span data-stu-id="b15ae-147">The ID3D12GraphicsCommandList methods [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) and [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) are not predicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b15ae-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b15ae-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b15ae-149">Contadores e consultas</span><span class="sxs-lookup"><span data-stu-id="b15ae-149">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="b15ae-150">Medição de desempenho</span><span class="sxs-lookup"><span data-stu-id="b15ae-150">Performance Measurement</span></span>](performance-measurement.md)
</dt> <dt>

[<span data-ttu-id="b15ae-151">Passo a passo de consultas do predicação</span><span class="sxs-lookup"><span data-stu-id="b15ae-151">Predication queries walk-through</span></span>](predication-queries.md)
</dt> </dl>

 

 




