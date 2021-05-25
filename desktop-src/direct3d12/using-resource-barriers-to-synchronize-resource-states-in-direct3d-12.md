---
title: Como usar barreiras de recursos para sincronizar estados de recursos no Direct3D 12
description: Para reduzir o uso geral da CPU e habilitar o multi-threading e o pré-processamento do driver, o Direct3D 12 move a responsabilidade do gerenciamento de estado por recurso do driver gráfico para o aplicativo.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df27e7997b4f3f56ae8e87688e5cc136dc7eb87d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343471"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a><span data-ttu-id="c524c-103">Como usar barreiras de recursos para sincronizar estados de recursos no Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c524c-103">Using Resource Barriers to Synchronize Resource States in Direct3D 12</span></span>

<span data-ttu-id="c524c-104">Para reduzir o uso geral da CPU e habilitar o multi-threading e o pré-processamento do driver, o Direct3D 12 move a responsabilidade do gerenciamento de estado por recurso do driver gráfico para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c524c-104">To reduce overall CPU usage and enable driver multi-threading and pre-processing, Direct3D 12 moves the responsibility of per-resource state management from the graphics driver to the application.</span></span> <span data-ttu-id="c524c-105">Um exemplo de estado por recurso é se um recurso de textura está sendo acessado no momento como por meio de um Modo de Exibição de Recursos sombreador ou como uma Exibição de Destino de Renderização.</span><span class="sxs-lookup"><span data-stu-id="c524c-105">An example of per-resource state is whether a texture resource is currently being accessed as through a Shader Resource View or as a Render Target View.</span></span> <span data-ttu-id="c524c-106">No Direct3D 11, os drivers eram necessários para acompanhar esse estado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="c524c-106">In Direct3D 11, drivers were required to track this state in the background.</span></span> <span data-ttu-id="c524c-107">Isso é caro da perspectiva da CPU e complica significativamente qualquer tipo de design multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="c524c-107">This is expensive from a CPU perspective and significantly complicates any sort of multi-threaded design.</span></span> <span data-ttu-id="c524c-108">No Microsoft Direct3D 12, a maioria dos estados por recurso é gerenciada pelo aplicativo com uma única API, [**ID3D12GraphicsCommandList::ResourceBa ltd.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)</span><span class="sxs-lookup"><span data-stu-id="c524c-108">In Microsoft Direct3D 12, most per-resource state is managed by the application with a single API, [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

-   [<span data-ttu-id="c524c-109">Usando a API ResourceBa fox para gerenciar o estado por recurso</span><span class="sxs-lookup"><span data-stu-id="c524c-109">Using the ResourceBarrier API to manage per-resource state</span></span>](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [<span data-ttu-id="c524c-110">Estados de recurso</span><span class="sxs-lookup"><span data-stu-id="c524c-110">Resource states</span></span>](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [<span data-ttu-id="c524c-111">Estados iniciais para recursos</span><span class="sxs-lookup"><span data-stu-id="c524c-111">Initial states for resources</span></span>](#initial-states-for-resources)
    -   [<span data-ttu-id="c524c-112">Restrições de estado de recurso de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c524c-112">Read/write resource state restrictions</span></span>](#readwrite-resource-state-restrictions)
    -   [<span data-ttu-id="c524c-113">Estados de recurso para apresentar buffers de volta</span><span class="sxs-lookup"><span data-stu-id="c524c-113">Resource states for presenting back buffers</span></span>](#resource-states-for-presenting-back-buffers)
    -   [<span data-ttu-id="c524c-114">Descartando recursos</span><span class="sxs-lookup"><span data-stu-id="c524c-114">Discarding resources</span></span>](#discarding-resources)
-   [<span data-ttu-id="c524c-115">Transições de estado implícitas</span><span class="sxs-lookup"><span data-stu-id="c524c-115">Implicit State Transitions</span></span>](#implicit-state-transitions)
    -   [<span data-ttu-id="c524c-116">Promoção de estado comum</span><span class="sxs-lookup"><span data-stu-id="c524c-116">Common state promotion</span></span>](#common-state-promotion)
    -   [<span data-ttu-id="c524c-117">Decaimento de estado para comum</span><span class="sxs-lookup"><span data-stu-id="c524c-117">State decay to common</span></span>](#state-decay-to-common)
    -   [<span data-ttu-id="c524c-118">Implicações de desempenho</span><span class="sxs-lookup"><span data-stu-id="c524c-118">Performance implications</span></span>](#performance-implications)
-   [<span data-ttu-id="c524c-119">Barreiras de divisão</span><span class="sxs-lookup"><span data-stu-id="c524c-119">Split Barriers</span></span>](#split-barriers)
-   [<span data-ttu-id="c524c-120">Cenário de exemplo de barreira de recursos</span><span class="sxs-lookup"><span data-stu-id="c524c-120">Resource barrier example scenario</span></span>](#resource-barrier-example-scenario)
-   [<span data-ttu-id="c524c-121">Exemplo comum de promoção de estado e decaimento</span><span class="sxs-lookup"><span data-stu-id="c524c-121">Common state promotion and decay sample</span></span>](#common-state-promotion-and-decay-sample)
-   [<span data-ttu-id="c524c-122">Exemplo de barreiras de divisão</span><span class="sxs-lookup"><span data-stu-id="c524c-122">Example of split barriers</span></span>](#example-of-split-barriers)
-   [<span data-ttu-id="c524c-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c524c-123">Related topics</span></span>](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a><span data-ttu-id="c524c-124">Usando a API ResourceBa fox para gerenciar o estado por recurso</span><span class="sxs-lookup"><span data-stu-id="c524c-124">Using the ResourceBarrier API to manage per-resource state</span></span>

<span data-ttu-id="c524c-125">O [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifica o driver de gráficos de situações em que o driver pode precisar sincronizar vários acessos à memória na qual um recurso está armazenado.</span><span class="sxs-lookup"><span data-stu-id="c524c-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifies the graphics driver of situations in which the driver may need to synchronize multiple accesses to the memory in which a resource is stored.</span></span> <span data-ttu-id="c524c-126">O método é chamado com uma ou mais estruturas de descrição de barreira de recurso que indicam o tipo de barreira de recurso que está sendo declarado.</span><span class="sxs-lookup"><span data-stu-id="c524c-126">The method is called with one or more resource barrier description structures indicating the type of resource barrier being declared.</span></span>

<span data-ttu-id="c524c-127">Há três tipos de barreiras de recursos:</span><span class="sxs-lookup"><span data-stu-id="c524c-127">There are three types of resource barriers:</span></span>

-   <span data-ttu-id="c524c-128">**Barreira de transição** – uma barreira de transição indica que um conjunto de subrecursos faz a transição entre diferentes usos.</span><span class="sxs-lookup"><span data-stu-id="c524c-128">**Transition barrier** - A transition barrier indicates that a set of subresources transition between different usages.</span></span> <span data-ttu-id="c524c-129">Uma estrutura de [**barreira de \_ transição de recursos \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) é usada para especificar o subrecurso que está em transição, bem como os Estados de *antes* e *depois* do subrecurso.</span><span class="sxs-lookup"><span data-stu-id="c524c-129">A [**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) structure is used to specify the subresource that is transitioning as well as the *before* and *after* states of the subresource.</span></span>

    <span data-ttu-id="c524c-130">O sistema verifica se as transições de subrecurso em uma lista de comandos são consistentes com as transições anteriores na mesma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="c524c-130">The system verifies that subresource transitions in a command list are consistent with previous transitions in the same command list.</span></span> <span data-ttu-id="c524c-131">A camada de depuração rastreia ainda mais o estado do subrecurso para encontrar outros erros, no entanto, essa validação é conservadora e não exaustiva.</span><span class="sxs-lookup"><span data-stu-id="c524c-131">The debug layer further tracks subresource state to find other errors however this validation is conservative and not exhaustive.</span></span>

    <span data-ttu-id="c524c-132">Observe que você pode usar o \_ sinalizador D3D12 \_ de \_ todos os \_ subrecursos de barreira de recursos para especificar que todos os subrecursos em um recurso estão sendo transferidos.</span><span class="sxs-lookup"><span data-stu-id="c524c-132">Note that you can use the D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES flag to specify that all subresources within a resource are being transitioned.</span></span>

-   <span data-ttu-id="c524c-133">**Barreira de alias** – uma barreira de alias indica uma transição entre os usos de dois recursos diferentes que têm mapeamentos sobrepostos no mesmo heap.</span><span class="sxs-lookup"><span data-stu-id="c524c-133">**Aliasing barrier** - An aliasing barrier indicates a transition between usages of two different resources which have overlapping mappings into the same heap.</span></span> <span data-ttu-id="c524c-134">Isso se aplica a recursos reservados e colocados.</span><span class="sxs-lookup"><span data-stu-id="c524c-134">This applies to both reserved and placed resources.</span></span> <span data-ttu-id="c524c-135">Uma estrutura de [**barreira de \_ alias de recursos \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) é usada para especificar o recurso *before* e o *After* .</span><span class="sxs-lookup"><span data-stu-id="c524c-135">A [**D3D12\_RESOURCE\_ALIASING\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) structure is used to specify both the *before* resource and the *after* resource.</span></span>

    <span data-ttu-id="c524c-136">Observe que um ou ambos os recursos podem ser nulos, o que indica que qualquer recurso de ladrilho pode causar alias.</span><span class="sxs-lookup"><span data-stu-id="c524c-136">Note that one or both resources can be NULL, which indicates that any tiled resource could cause aliasing.</span></span> <span data-ttu-id="c524c-137">Para obter mais informações sobre o uso de recursos em ladrilho, consulte recursos de [lado](../direct3d11/tiled-resources.md) e de [volume](volume-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="c524c-137">For more information about using tiled resources, see [Tiled resources](../direct3d11/tiled-resources.md) and [Volume Tiled Resources](volume-tiled-resources.md).</span></span>

-   <span data-ttu-id="c524c-138">**Barreira de modo de exibição de acesso não ordenado (UAV)** -uma barreira UAV indica que todos os acessos de UAV, leitura ou gravação, a um recurso específico devem ser concluídos entre quaisquer acessos UAV futuros, leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="c524c-138">**Unordered access view (UAV) barrier** - A UAV barrier indicates that all UAV accesses, both read or write, to a particular resource must complete between any future UAV accesses, both read or write.</span></span> <span data-ttu-id="c524c-139">Não é necessário que um aplicativo coloque uma barreira de UAV entre duas chamadas de desenho ou expedição que somente leem de um UAV.</span><span class="sxs-lookup"><span data-stu-id="c524c-139">It's not necessary for an app to put a UAV barrier between two draw or dispatch calls that only read from a UAV.</span></span> <span data-ttu-id="c524c-140">Além disso, não é necessário colocar uma barreira de UAV entre duas chamadas de desenho ou expedição que são escritas no mesmo UAV se o aplicativo souber que é seguro executar o acesso UAV em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="c524c-140">Also, it's not necessary to put a UAV barrier between two draw or dispatch calls that write to the same UAV if the application knows that it is safe to execute the UAV access in any order.</span></span> <span data-ttu-id="c524c-141">Uma [**estrutura D3D12 \_ RESOURCE \_ UAV \_ BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) é usada para especificar o recurso UAV ao qual a barreira se aplica.</span><span class="sxs-lookup"><span data-stu-id="c524c-141">A [**D3D12\_RESOURCE\_UAV\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) structure is used to specify the UAV resource to which the barrier applies.</span></span> <span data-ttu-id="c524c-142">O aplicativo pode especificar NULL para o UAV da barreira, o que indica que qualquer acesso UAV pode exigir a barreira.</span><span class="sxs-lookup"><span data-stu-id="c524c-142">The application can specify NULL for the barrier's UAV, which indicates that any UAV access could require the barrier.</span></span>

<span data-ttu-id="c524c-143">Quando [**ResourceBa array**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) é chamado com uma matriz de descrições de barreira de recursos, a API se comporta como se tivesse sido chamada uma vez para cada elemento, na ordem em que foram fornecidas.</span><span class="sxs-lookup"><span data-stu-id="c524c-143">When [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) is called with an array of resource barrier descriptions, the API behaves as if it was called once for each element, in the order in which they were supplied.</span></span>

<span data-ttu-id="c524c-144">A qualquer momento, uma sub-fonte está exatamente em um estado, determinado pelo conjunto de sinalizadores [**D3D12 \_ RESOURCE \_ STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) fornecidos para [**ResourceBa ltda.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)</span><span class="sxs-lookup"><span data-stu-id="c524c-144">At any given time, a subresource is in exactly one state, determined by the set of [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) flags supplied to [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span> <span data-ttu-id="c524c-145">O aplicativo deve garantir que os *estados antes* e *depois* de chamadas consecutivas para **ResourceBarrier concordem.**</span><span class="sxs-lookup"><span data-stu-id="c524c-145">The application must ensure that the *before* and *after* states of consecutive calls to **ResourceBarrier** agree.</span></span>

> [!TIP]
>
> <span data-ttu-id="c524c-146">Os aplicativos devem fazer várias transições em lote em uma chamada à API sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="c524c-146">Applications should batch multiple transitions into one API call wherever possible.</span></span>

 

### <a name="resource-states"></a><span data-ttu-id="c524c-147">Estados de recurso</span><span class="sxs-lookup"><span data-stu-id="c524c-147">Resource states</span></span>

<span data-ttu-id="c524c-148">Para ver a lista completa de estados de recurso entre os que um recurso pode fazer a transição, consulte o tópico de referência para a enumeração [**D3D12 \_ RESOURCE \_ STATES.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="c524c-148">For the complete list of resource states that a resource can transition between, see the reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeration.</span></span>

<span data-ttu-id="c524c-149">Para dividir as barreiras de recursos, consulte também [**D3D12 \_ RESOURCE \_ BARRIER \_ FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span><span class="sxs-lookup"><span data-stu-id="c524c-149">For split resource barriers, also refer to [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span></span>

### <a name="initial-states-for-resources"></a><span data-ttu-id="c524c-150">Estados iniciais para recursos</span><span class="sxs-lookup"><span data-stu-id="c524c-150">Initial states for resources</span></span>

<span data-ttu-id="c524c-151">Os recursos podem ser criados com qualquer estado inicial especificado pelo usuário (válido para a descrição do recurso), com as seguintes exceções:</span><span class="sxs-lookup"><span data-stu-id="c524c-151">Resources may be created with any user-specified initial state (valid for the resource description), with the following exceptions:</span></span>

-   <span data-ttu-id="c524c-152">O carregamento de heaps deve começar no estado D3D12 RESOURCE STATE GENERIC READ, que é uma combinação \_ OR bit a bit \_ \_ \_ de:</span><span class="sxs-lookup"><span data-stu-id="c524c-152">Upload heaps must start out in the state D3D12\_RESOURCE\_STATE\_GENERIC\_READ which is a bitwise OR combination of:</span></span>
    -   <span data-ttu-id="c524c-153">VÉRTICE DE ESTADO DO RECURSO D3D12 \_ \_ E BUFFER \_ \_ \_ CONSTANTE \_</span><span class="sxs-lookup"><span data-stu-id="c524c-153">D3D12\_RESOURCE\_STATE\_VERTEX\_AND\_CONSTANT\_BUFFER</span></span>
    -   <span data-ttu-id="c524c-154">D3D12 \_ RESOURCE \_ STATE \_ INDEX \_ BUFFER</span><span class="sxs-lookup"><span data-stu-id="c524c-154">D3D12\_RESOURCE\_STATE\_INDEX\_BUFFER</span></span>
    -   <span data-ttu-id="c524c-155">D3D12 \_ RESOURCE \_ STATE \_ COPY \_ SOURCE</span><span class="sxs-lookup"><span data-stu-id="c524c-155">D3D12\_RESOURCE\_STATE\_COPY\_SOURCE</span></span>
    -   <span data-ttu-id="c524c-156">RECURSO D3D12 \_ RESOURCE STATE NON PIXEL \_ \_ \_ \_ \_ SHADER</span><span class="sxs-lookup"><span data-stu-id="c524c-156">D3D12\_RESOURCE\_STATE\_NON\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="c524c-157">\_Recurso D3D12 \_ \_ \_ sombreador de pixel do estado do recurso \_</span><span class="sxs-lookup"><span data-stu-id="c524c-157">D3D12\_RESOURCE\_STATE\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="c524c-158">\_ \_ \_ Argumento indireto de estado do recurso D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="c524c-158">D3D12\_RESOURCE\_STATE\_INDIRECT\_ARGUMENT</span></span>
-   <span data-ttu-id="c524c-159">Os heaps readback devem começar no estado de \_ destino da cópia de estado do recurso D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c524c-159">Readback heaps must start out in the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span>
-   <span data-ttu-id="c524c-160">Buffers de back de cadeia de permuta iniciam automaticamente \_ no \_ estado comum do estado do recurso D3D12 \_ .</span><span class="sxs-lookup"><span data-stu-id="c524c-160">Swap chain back buffers automatically start out in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span>

<span data-ttu-id="c524c-161">Antes que um heap possa ser o destino de uma operação de cópia de GPU, normalmente o heap deve primeiro ser transferido para o \_ estado de destino da cópia de estado do recurso D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c524c-161">Before a heap can be the target of a GPU copy operation, normally the heap must first be transitioned to the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span> <span data-ttu-id="c524c-162">No entanto, os recursos criados em heaps de carregamento devem começar no e não podem ser alterados a partir do \_ estado de leitura genérico, pois apenas a CPU estará escrevendo.</span><span class="sxs-lookup"><span data-stu-id="c524c-162">However, resources created on UPLOAD heaps must start in and cannot change from the GENERIC\_READ state since only the CPU will be doing writing.</span></span> <span data-ttu-id="c524c-163">Por outro lado, os recursos confirmados criados em heaps READBACK devem começar no e não podem mudar a partir do estado de destino da cópia \_ .</span><span class="sxs-lookup"><span data-stu-id="c524c-163">Conversely, committed resources created in READBACK heaps must start in and cannot change from the COPY\_DEST state.</span></span>

### <a name="readwrite-resource-state-restrictions"></a><span data-ttu-id="c524c-164">Restrições de estado do recurso de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c524c-164">Read/write resource state restrictions</span></span>

<span data-ttu-id="c524c-165">Os bits de uso de estado do recurso que são usados para descrever um estado de recurso são divididos em Estados somente leitura e de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c524c-165">The resource state usage bits that are used to describe a resource state are divided into read-only and read/write states.</span></span> <span data-ttu-id="c524c-166">O tópico de referência para [**os \_ \_ Estados de recurso D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indica o nível de acesso de leitura/gravação para cada bit na enumeração.</span><span class="sxs-lookup"><span data-stu-id="c524c-166">The reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indicates the read/write access level for each bit in the enumeration.</span></span>

<span data-ttu-id="c524c-167">No máximo, apenas um bit de leitura/gravação pode ser definido para qualquer recurso.</span><span class="sxs-lookup"><span data-stu-id="c524c-167">At most, only one read/write bit can be set for any resource.</span></span> <span data-ttu-id="c524c-168">Se um bit de gravação for definido, nenhum bit somente leitura poderá ser definido para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="c524c-168">If a write bit is set, then no read-only bit may be set for that resource.</span></span> <span data-ttu-id="c524c-169">Se nenhum bit de gravação for definido, qualquer número de bits de leitura poderá ser definido.</span><span class="sxs-lookup"><span data-stu-id="c524c-169">If no write bit is set, then any number of read bits may be set.</span></span>

### <a name="resource-states-for-presenting-back-buffers"></a><span data-ttu-id="c524c-170">Estados de recursos para apresentar buffers de fundo</span><span class="sxs-lookup"><span data-stu-id="c524c-170">Resource states for presenting back buffers</span></span>

<span data-ttu-id="c524c-171">Antes de um buffer de fundo ser apresentado, ele deve estar no \_ estado comum do estado do recurso D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c524c-171">Before a back buffer is presented, it must be in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span> <span data-ttu-id="c524c-172">Observe que o estado do recurso D3D12 \_ Resource State \_ \_ presente é um sinônimo para o \_ estado do recurso D3D12 \_ \_ comum, e ambos têm um valor de 0.</span><span class="sxs-lookup"><span data-stu-id="c524c-172">Note, the resource state D3D12\_RESOURCE\_STATE\_PRESENT is a synonym for D3D12\_RESOURCE\_STATE\_COMMON, and they both have a value of 0.</span></span> <span data-ttu-id="c524c-173">Se [**IDXGISwapChain::P reenviado**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (ou [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) for chamado em um recurso que não está atualmente nesse estado, um aviso de camada de depuração será emitido.</span><span class="sxs-lookup"><span data-stu-id="c524c-173">If [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (or [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) is called on a resource that is not currently in this state, a debug layer warning is emitted.</span></span>

### <a name="discarding-resources"></a><span data-ttu-id="c524c-174">Descartando recursos</span><span class="sxs-lookup"><span data-stu-id="c524c-174">Discarding resources</span></span>

<span data-ttu-id="c524c-175">Todas as sub-fontes em um recurso devem estar no estado RENDER TARGET ou no estado DEPTH WRITE para recursos de \_ \_ destino/profundidade/estêncil de renderização, respectivamente, quando [**ID3D12GraphicsCommandList::D iscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) é chamado.</span><span class="sxs-lookup"><span data-stu-id="c524c-175">All subresources in a resource must be in the RENDER\_TARGET state, or DEPTH\_WRITE state, for render targets/depth-stencil resources respectively, when [**ID3D12GraphicsCommandList::DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) is called.</span></span>

## <a name="implicit-state-transitions"></a><span data-ttu-id="c524c-176">Transições de estado implícitas</span><span class="sxs-lookup"><span data-stu-id="c524c-176">Implicit State Transitions</span></span>

<span data-ttu-id="c524c-177">Os recursos só podem ser "promovidos" de D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="c524c-177">Resources can only be "promoted" out of D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="c524c-178">Da mesma forma, os recursos só serão "decair" para D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="c524c-178">Similarly, resources will only "decay" to D3D12\_RESOURCE\_STATE\_COMMON.</span></span>

### <a name="common-state-promotion"></a><span data-ttu-id="c524c-179">Promoção de estado comum</span><span class="sxs-lookup"><span data-stu-id="c524c-179">Common state promotion</span></span>

<span data-ttu-id="c524c-180">Todos os recursos de buffer, bem como texturas com o sinalizador D3D12 RESOURCE FLAG ALLOW SIMULTANEOUS ACCESS definido são promovidos implicitamente de \_ \_ \_ \_ \_ D3D12 RESOURCE STATE \_ COMMON \_ \_ \_ para o estado relevante no primeiro acesso à GPU, incluindo LEITURA GENÉRICA para abranger qualquer cenário de leitura.</span><span class="sxs-lookup"><span data-stu-id="c524c-180">All buffer resources as well as textures with the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set are implicitly promoted from D3D12\_RESOURCE\_STATE\_COMMON to the relevant state on first GPU access, including GENERIC\_READ to cover any read scenario.</span></span> <span data-ttu-id="c524c-181">Qualquer recurso no estado COMMON pode ser acessado como por meio dele estava em um único estado com</span><span class="sxs-lookup"><span data-stu-id="c524c-181">Any resource in the COMMON state can be accessed as through it were in a single state with</span></span>

<dl> <span data-ttu-id="c524c-182">1 sinalizador WRITE ou</span><span class="sxs-lookup"><span data-stu-id="c524c-182">1 WRITE flag, or</span></span>  
<span data-ttu-id="c524c-183">1 ou mais sinalizadores READ</span><span class="sxs-lookup"><span data-stu-id="c524c-183">1 or more READ flags</span></span>  
</dl>

<span data-ttu-id="c524c-184">Os recursos podem ser promovidos do estado COMMON com base na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="c524c-184">Resources can be promoted from the COMMON state based on the following table:</span></span>



| <span data-ttu-id="c524c-185">Sinalizador de estado</span><span class="sxs-lookup"><span data-stu-id="c524c-185">State flag</span></span>                    | <span data-ttu-id="c524c-186">Buffers e Simultaneous-Access texturas</span><span class="sxs-lookup"><span data-stu-id="c524c-186">Buffers and Simultaneous-Access Textures</span></span>                             | <span data-ttu-id="c524c-187">Texturas sem acesso simultâneo</span><span class="sxs-lookup"><span data-stu-id="c524c-187">Non-Simultaneous-Access Textures</span></span>                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| <span data-ttu-id="c524c-188">VÉRTICE \_ E \_ BUFFER \_ CONSTANTE</span><span class="sxs-lookup"><span data-stu-id="c524c-188">VERTEX\_AND\_CONSTANT\_BUFFER</span></span> | <span data-ttu-id="c524c-189">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-189">Yes</span></span>                                          | <span data-ttu-id="c524c-190">Não</span><span class="sxs-lookup"><span data-stu-id="c524c-190">No</span></span>                                   |
| <span data-ttu-id="c524c-191">BUFFER DE \_ ÍNDICE</span><span class="sxs-lookup"><span data-stu-id="c524c-191">INDEX\_BUFFER</span></span>                 | <span data-ttu-id="c524c-192">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-192">Yes</span></span>                                          | <span data-ttu-id="c524c-193">Não</span><span class="sxs-lookup"><span data-stu-id="c524c-193">No</span></span>                                   |
| <span data-ttu-id="c524c-194">DESTINO \_ DE RENDERIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="c524c-194">RENDER\_TARGET</span></span>                | <span data-ttu-id="c524c-195">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-195">Yes</span></span>                                          | <span data-ttu-id="c524c-196">Não</span><span class="sxs-lookup"><span data-stu-id="c524c-196">No</span></span>                                   |
| <span data-ttu-id="c524c-197">ACESSO NÃO \_ ORGANIZADO</span><span class="sxs-lookup"><span data-stu-id="c524c-197">UNORDERED\_ACCESS</span></span>             | <span data-ttu-id="c524c-198">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-198">Yes</span></span>                                          | <span data-ttu-id="c524c-199">Não</span><span class="sxs-lookup"><span data-stu-id="c524c-199">No</span></span>                                   |
| <span data-ttu-id="c524c-200">GRAVAÇÃO \_ DE PROFUNDIDADE</span><span class="sxs-lookup"><span data-stu-id="c524c-200">DEPTH\_WRITE</span></span>                  | <span data-ttu-id="c524c-201">Não<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c524c-201">No<sup>\*</sup></span></span>                              | <span data-ttu-id="c524c-202">Não</span><span class="sxs-lookup"><span data-stu-id="c524c-202">No</span></span>                                   |
| <span data-ttu-id="c524c-203">LEITURA DE \_ PROFUNDIDADE</span><span class="sxs-lookup"><span data-stu-id="c524c-203">DEPTH\_READ</span></span>                   | <span data-ttu-id="c524c-204">Não<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="c524c-204">No<sup>\*</sup></span></span>                              | <span data-ttu-id="c524c-205">Não</span><span class="sxs-lookup"><span data-stu-id="c524c-205">No</span></span>                                   |
| <span data-ttu-id="c524c-206">\_recurso de \_ sombreador não pixel \_</span><span class="sxs-lookup"><span data-stu-id="c524c-206">NON\_PIXEL\_SHADER\_RESOURCE</span></span>  | <span data-ttu-id="c524c-207">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-207">Yes</span></span>                                          | <span data-ttu-id="c524c-208">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-208">Yes</span></span>                                  |
| <span data-ttu-id="c524c-209">\_recurso sombreador de pixel \_</span><span class="sxs-lookup"><span data-stu-id="c524c-209">PIXEL\_SHADER\_RESOURCE</span></span>       | <span data-ttu-id="c524c-210">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-210">Yes</span></span>                                          | <span data-ttu-id="c524c-211">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-211">Yes</span></span>                                  |
| <span data-ttu-id="c524c-212">saída de fluxo \_</span><span class="sxs-lookup"><span data-stu-id="c524c-212">STREAM\_OUT</span></span>                   | <span data-ttu-id="c524c-213">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-213">Yes</span></span>                                          | <span data-ttu-id="c524c-214">Não</span><span class="sxs-lookup"><span data-stu-id="c524c-214">No</span></span>                                   |
| <span data-ttu-id="c524c-215">argumento indireto \_</span><span class="sxs-lookup"><span data-stu-id="c524c-215">INDIRECT\_ARGUMENT</span></span>            | <span data-ttu-id="c524c-216">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-216">Yes</span></span>                                          | <span data-ttu-id="c524c-217">Não</span><span class="sxs-lookup"><span data-stu-id="c524c-217">No</span></span>                                   |
| <span data-ttu-id="c524c-218">COPIAR \_ dest</span><span class="sxs-lookup"><span data-stu-id="c524c-218">COPY\_DEST</span></span>                    | <span data-ttu-id="c524c-219">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-219">Yes</span></span>                                          | <span data-ttu-id="c524c-220">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-220">Yes</span></span>                                  |
| <span data-ttu-id="c524c-221">origem da cópia \_</span><span class="sxs-lookup"><span data-stu-id="c524c-221">COPY\_SOURCE</span></span>                  | <span data-ttu-id="c524c-222">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-222">Yes</span></span>                                          | <span data-ttu-id="c524c-223">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-223">Yes</span></span>                                  |
| <span data-ttu-id="c524c-224">RESOLVER \_ dest</span><span class="sxs-lookup"><span data-stu-id="c524c-224">RESOLVE\_DEST</span></span>                 | <span data-ttu-id="c524c-225">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-225">Yes</span></span>                                          | <span data-ttu-id="c524c-226">Não</span><span class="sxs-lookup"><span data-stu-id="c524c-226">No</span></span>                                   |
| <span data-ttu-id="c524c-227">RESOLVER \_ origem</span><span class="sxs-lookup"><span data-stu-id="c524c-227">RESOLVE\_SOURCE</span></span>               | <span data-ttu-id="c524c-228">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-228">Yes</span></span>                                          | <span data-ttu-id="c524c-229">Não</span><span class="sxs-lookup"><span data-stu-id="c524c-229">No</span></span>                                   |
| <span data-ttu-id="c524c-230">PREDICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="c524c-230">PREDICATION</span></span>                   | <span data-ttu-id="c524c-231">Sim</span><span class="sxs-lookup"><span data-stu-id="c524c-231">Yes</span></span>                                          | <span data-ttu-id="c524c-232">Não</span><span class="sxs-lookup"><span data-stu-id="c524c-232">No</span></span>                                   |



 

<span data-ttu-id="c524c-233"><sup>\*</sup>Os recursos do estêncil de profundidade devem ser texturas de acesso não simultâneas e, portanto, nunca podem ser promovidas implicitamente.</span><span class="sxs-lookup"><span data-stu-id="c524c-233"><sup>\*</sup>Depth-stencil resources must be non-simultaneous-access textures and thus can never be implicitly promoted.</span></span>

<span data-ttu-id="c524c-234">Quando esse acesso ocorre, a promoção age como uma barreira de recursos implícita.</span><span class="sxs-lookup"><span data-stu-id="c524c-234">When this access occurs the promotion acts like an implicit resource barrier.</span></span> <span data-ttu-id="c524c-235">Para os acessos subsequentes, as barreiras de recursos serão necessárias para alterar o estado do recurso, se necessário.</span><span class="sxs-lookup"><span data-stu-id="c524c-235">For subsequent accesses, resource barriers will be required to change the resource state if necessary.</span></span> <span data-ttu-id="c524c-236">Observe que a promoção de um estado de leitura promovido em vários Estados de leitura é válida, mas esse não é o caso para os Estados de gravação.</span><span class="sxs-lookup"><span data-stu-id="c524c-236">Note that promotion from one promoted read state into multiple read state is valid, but this is not the case for write states.</span></span>  
<span data-ttu-id="c524c-237">Por exemplo, se um recurso no estado comum for promovido para recurso de \_ sombreador \_ de pixel em uma chamada de desenho, ele ainda poderá ser promovido para NON_PIXEL \_ recurso de sombreador \_ | \_ \_ Recurso de sombreador de pixel em outra chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="c524c-237">For example, if a resource in the common state is promoted to PIXEL\_SHADER\_RESOURCE in a Draw call, it can still be promoted to NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE in another Draw call.</span></span> <span data-ttu-id="c524c-238">No entanto, se ele for usado em uma operação de gravação, como um destino de cópia, uma barreira de transição de estado de recurso dos Estados de leitura promovidos combinados, aqui NON_PIXEL \_ recurso de sombreador \_ | O \_ \_ recurso de sombreador de pixel, para copiar \_ dest é necessário.</span><span class="sxs-lookup"><span data-stu-id="c524c-238">However, if it is used in a write operation, such as a copy destination, a resource state transition barrier from the combined promoted read states, here NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE, to COPY\_DEST is needed.</span></span>  
<span data-ttu-id="c524c-239">Da mesma forma, se for promovido de COMMON para COPY \_ dest, uma barreira ainda será necessária para fazer a transição do dest de cópia \_ para o destino de renderização \_ .</span><span class="sxs-lookup"><span data-stu-id="c524c-239">Similarly, if promoted from COMMON to COPY\_DEST, a barrier is still required to transition from COPY\_DEST to RENDER\_TARGET.</span></span>

<span data-ttu-id="c524c-240">Observe que a promoção de Estado comum é "gratuita", pois não há necessidade de a GPU executar qualquer espera de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c524c-240">Note that common state promotion is "free" in that there is no need for the GPU to perform any synchronization waits.</span></span> <span data-ttu-id="c524c-241">A promoção representa o fato de que os recursos no estado comum não devem exigir acompanhamento de driver ou trabalho de GPU adicional para dar suporte a determinados acessos.</span><span class="sxs-lookup"><span data-stu-id="c524c-241">The promotion represents the fact that resources in the COMMON state should not require additional GPU work or driver tracking to support certain accesses.</span></span>

### <a name="state-decay-to-common"></a><span data-ttu-id="c524c-242">Estado decaimento para comum</span><span class="sxs-lookup"><span data-stu-id="c524c-242">State decay to common</span></span>

<span data-ttu-id="c524c-243">O outro lado da promoção de estado comum é decair de volta para D3D12 \_ RESOURCE \_ STATE \_ COMMON.</span><span class="sxs-lookup"><span data-stu-id="c524c-243">The flip-side of common state promotion is decay back to D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="c524c-244">Os recursos que atendem a determinados requisitos são considerados sem estado e retornam efetivamente ao estado comum quando a GPU termina a execução de [**uma operação ExecuteCommandLists.**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)</span><span class="sxs-lookup"><span data-stu-id="c524c-244">Resources that meet certain requirements are considered to be stateless and effectively return to the common state when the GPU finishes execution of an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation.</span></span> <span data-ttu-id="c524c-245">O decaimento não ocorre entre listas de comandos executadas juntas na mesma **chamada ExecuteCommandLists.**</span><span class="sxs-lookup"><span data-stu-id="c524c-245">Decay does not occur between command lists executed together in the same **ExecuteCommandLists** call.</span></span>

<span data-ttu-id="c524c-246">Os seguintes recursos serão decair [**quando uma operação ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) for concluída na GPU:</span><span class="sxs-lookup"><span data-stu-id="c524c-246">The following resources will decay when an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation is completed on the GPU:</span></span>

-   <span data-ttu-id="c524c-247">Recursos que estão sendo acessados em uma fila de cópia *ou*</span><span class="sxs-lookup"><span data-stu-id="c524c-247">Resources being accessed on a Copy queue, *or*</span></span>
-   <span data-ttu-id="c524c-248">Recursos de buffer em qualquer tipo de fila *ou*</span><span class="sxs-lookup"><span data-stu-id="c524c-248">Buffer resources on any queue type, *or*</span></span>
-   <span data-ttu-id="c524c-249">Recursos de textura em qualquer tipo de fila que tenha o sinalizador D3D12 \_ RESOURCE FLAG ALLOW SIMULTANEOUS ACCESS definido \_ \_ \_ \_ *ou*</span><span class="sxs-lookup"><span data-stu-id="c524c-249">Texture resources on any queue type that have the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set, *or*</span></span>
-   <span data-ttu-id="c524c-250">Qualquer recurso promovido implicitamente para um estado somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c524c-250">Any resource implicitly promoted to a read-only state.</span></span>

<span data-ttu-id="c524c-251">Assim como a promoção de estado comum, o decaimento é gratuito, já que nenhuma sincronização adicional é necessária.</span><span class="sxs-lookup"><span data-stu-id="c524c-251">Like common state promotion, the decay is free in that no additional synchronization is needed.</span></span> <span data-ttu-id="c524c-252">Combinar promoção de estado comum e decaimento pode ajudar a eliminar muitas transições [**desnecessárias do ResourceBa ltda.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)</span><span class="sxs-lookup"><span data-stu-id="c524c-252">Combining common state promotion and decay can help to eliminate many unnecessary [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions.</span></span> <span data-ttu-id="c524c-253">Em alguns casos, isso pode fornecer melhorias significativas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="c524c-253">In some cases, this can provide significant performance improvements.</span></span>

<span data-ttu-id="c524c-254">Buffers e Simultaneous-Access recursos serão decair para o estado comum, independentemente de eles ter sido explicitamente transições usando barreiras de recursos ou promovidos implicitamente.</span><span class="sxs-lookup"><span data-stu-id="c524c-254">Buffers and Simultaneous-Access resources will decay to the common state regardless of whether they were explicitly transitioned using resource barriers or implicitly promoted.</span></span>

### <a name="performance-implications"></a><span data-ttu-id="c524c-255">Implicações de desempenho</span><span class="sxs-lookup"><span data-stu-id="c524c-255">Performance implications</span></span>

<span data-ttu-id="c524c-256">Ao registrar transições explícitas de [**ResourceBastate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) em recursos no estado comum, é correto usar D3D12 RESOURCE STATE COMMON ou qualquer estado promovendo como o valor BeforeState na estrutura \_ \_ \_ D3D12 RESOURCE TRANSITION  \_ \_ \_ BARRIER.</span><span class="sxs-lookup"><span data-stu-id="c524c-256">When recording explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions on resources in the common state, it is correct to use either D3D12\_RESOURCE\_STATE\_COMMON or any promotable state as the *BeforeState* value in the D3D12\_RESOURCE\_TRANSITION\_BARRIER structure.</span></span> <span data-ttu-id="c524c-257">Isso permite o gerenciamento de estado tradicional que ignora o decaimento automático de buffers e texturas de acesso simultâneo.</span><span class="sxs-lookup"><span data-stu-id="c524c-257">This allows traditional state management that ignores automatic decay of buffers and simultaneous-access textures.</span></span> <span data-ttu-id="c524c-258">No entanto, isso pode não ser desejável, pois evitar chamadas de transição **do ResourceBa ltda** com recursos conhecidos por estar no estado comum pode melhorar significativamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="c524c-258">This may not be desirable though, as avoiding transition **ResourceBarrier** calls with resources known to be in the common state can significantly improve performance.</span></span> <span data-ttu-id="c524c-259">As barreiras de recursos podem ser caras.</span><span class="sxs-lookup"><span data-stu-id="c524c-259">Resource barriers can be expensive.</span></span> <span data-ttu-id="c524c-260">Elas são projetadas para forçar liberações de cache, alterações de layout de memória e outras sincronizações que podem não ser necessárias para os recursos que já estão no estado comum.</span><span class="sxs-lookup"><span data-stu-id="c524c-260">They are designed to force cache flushes, memory layout changes and other synchronization that may not be necessary for resources already in the common state.</span></span> <span data-ttu-id="c524c-261">Uma lista de comandos que usa uma barreira de recurso de um estado não comum para outro Estado não comum em um recurso atualmente no estado comum pode introduzir muita sobrecarga desnecessária.</span><span class="sxs-lookup"><span data-stu-id="c524c-261">A command list that uses a resource barrier from a non-common state to another non-common state on a resource currently in the common state can introduce a lot of unneeded overhead.</span></span>

<span data-ttu-id="c524c-262">Além disso, evite transições [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explícitas \_ para \_ o estado do recurso D3D12 \_ comum, a menos que seja absolutamente necessário (por exemplo, o próximo acesso está em uma fila de comando de cópia que exige que os recursos comecem no estado comum).</span><span class="sxs-lookup"><span data-stu-id="c524c-262">Also, avoid explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions to D3D12\_RESOURCE\_STATE\_COMMON unless absolutely necessary (e.g. the next access is on a COPY command queue which requires a resources begin in the common state).</span></span> <span data-ttu-id="c524c-263">As transições excessivas para o estado comum podem reduzir drasticamente o desempenho da GPU.</span><span class="sxs-lookup"><span data-stu-id="c524c-263">Excessive transitions to the common state can dramatically slow down GPU performance.</span></span>

<span data-ttu-id="c524c-264">Em resumo, tente contar com a promoção de Estado comum e decaimento sempre que sua semântica permitir que você saia sem emitir chamadas [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .</span><span class="sxs-lookup"><span data-stu-id="c524c-264">In summary, try to rely on common state promotion and decay whenever its semantics let you get away without issuing [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) calls.</span></span>

## <a name="split-barriers"></a><span data-ttu-id="c524c-265">Barreiras de divisão</span><span class="sxs-lookup"><span data-stu-id="c524c-265">Split Barriers</span></span>

<span data-ttu-id="c524c-266">Uma barreira de transição de recurso com o sinalizador de barreira de D3D12 de \_ recursos \_ \_ \_ inicial \_ só começa uma barreira de divisão e a barreira de transição é considerada pendente.</span><span class="sxs-lookup"><span data-stu-id="c524c-266">A resource transition barrier with the D3D12\_RESOURCE\_BARRIER\_FLAG\_BEGIN\_ONLY flag begins a split barrier and the transition barrier is said to be pending.</span></span> <span data-ttu-id="c524c-267">Embora a barreira esteja pendente, o recurso (sub) não pode ser lido ou gravado pela GPU.</span><span class="sxs-lookup"><span data-stu-id="c524c-267">While the barrier is pending the (sub)resource cannot be read or written by the GPU.</span></span> <span data-ttu-id="c524c-268">A única barreira de transição legal que pode ser aplicada a um recurso (sub) com uma barreira pendente é uma com o mesmo estado *anterior* e *posterior* e o \_ sinalizador de finalização do sinalizador de barreira de recursos D3D12 \_ \_ \_ \_ , que a barreira conclui a transição pendente.</span><span class="sxs-lookup"><span data-stu-id="c524c-268">The only legal transition barrier that can be applied to a (sub)resource with a pending barrier is one with the same *before* and *after* states and the D3D12\_RESOURCE\_BARRIER\_FLAG\_END\_ONLY flag, which barrier completes the pending transition.</span></span>

<span data-ttu-id="c524c-269">As barreiras de divisão fornecem dicas para a GPU em que um recurso no estado *a* seguir será usado no estado *B* , em algum momento depois.</span><span class="sxs-lookup"><span data-stu-id="c524c-269">Split barriers provide hints to the GPU that a resource in state *A* will next be used in state *B* sometime later.</span></span> <span data-ttu-id="c524c-270">Isso dá à GPU a opção de otimizar a carga de trabalho de transição, possivelmente reduzindo ou eliminando as vagas de execução.</span><span class="sxs-lookup"><span data-stu-id="c524c-270">This gives the GPU the option to optimize the transition workload, possibly reducing or eliminating execution stalls.</span></span> <span data-ttu-id="c524c-271">A emissão da barreira somente final garante que todo o trabalho de transição da GPU seja concluído antes de passar para o próximo comando.</span><span class="sxs-lookup"><span data-stu-id="c524c-271">Issuing the end-only barrier guarantees that all GPU transition work is finished before moving onto the next command.</span></span>

<span data-ttu-id="c524c-272">O uso de barreiras de divisão pode ajudar a melhorar o desempenho, especialmente em cenários de vários mecanismos ou em que os recursos de leitura/gravação são transferidos de modo disperso em uma ou mais listas de comandos.</span><span class="sxs-lookup"><span data-stu-id="c524c-272">Using split barriers can help to improve performance, especially in multi-engine scenarios or where resources are read/write transitioned sparsely throughout one or more command lists.</span></span>

## <a name="resource-barrier-example-scenario"></a><span data-ttu-id="c524c-273">Cenário de exemplo de barreira de recurso</span><span class="sxs-lookup"><span data-stu-id="c524c-273">Resource barrier example scenario</span></span>

<span data-ttu-id="c524c-274">Os snippets a seguir mostram o uso do [**método ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) em um exemplo de multi-threading.</span><span class="sxs-lookup"><span data-stu-id="c524c-274">The following snippets show the use of the [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) method in a multi-threading sample.</span></span>

<span data-ttu-id="c524c-275">Criando a exibição de estêncil de profundidade, fazendo a transição dela para um estado grave.</span><span class="sxs-lookup"><span data-stu-id="c524c-275">Creating the depth stencil view, transitioning it to a writeable state.</span></span>


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



<span data-ttu-id="c524c-276">Criando a exibição de buffer de vértice, primeiro alterando-a de um estado comum para um destino e, em seguida, de um destino para um estado acessível genérico.</span><span class="sxs-lookup"><span data-stu-id="c524c-276">Creating the vertex buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



<span data-ttu-id="c524c-277">Criando a exibição de buffer de índice, primeiro alterando-a de um estado comum para um destino e, em seguida, de um destino para um estado acessível genérico.</span><span class="sxs-lookup"><span data-stu-id="c524c-277">Creating the index buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



<span data-ttu-id="c524c-278">Criando texturas e exibições de recursos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c524c-278">Creating textures and shader resource views.</span></span> <span data-ttu-id="c524c-279">A textura é alterada de um estado comum para um destino e, em seguida, de um destino para um recurso de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="c524c-279">The texture is changed from a common state to a destination, and then from a destination to a pixel shader resource.</span></span>


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



<span data-ttu-id="c524c-280">Iniciando um quadro; isso não só usa [**ResourceBa widget para**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) indicar que o backbuffer deve ser usado como um destino de renderização, mas também inicializa o recurso de quadro (que chama **ResourceBa widget** no buffer de estêncil de profundidade).</span><span class="sxs-lookup"><span data-stu-id="c524c-280">Beginning a frame; this not only uses [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to indicate that the backbuffer is to be used as a render target, but also initializes the frame resource (which calls **ResourceBarrier** on the depth stencil buffer).</span></span>


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



<span data-ttu-id="c524c-281">Encerrando um quadro, indicando que o buffer de fundo agora é usado para apresentar.</span><span class="sxs-lookup"><span data-stu-id="c524c-281">Ending a frame, indicating the back buffer is now used to present.</span></span>


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



<span data-ttu-id="c524c-282">Inicializar um recurso de quadro, chamado ao iniciar um quadro, faz a transição do buffer de estêncil de profundidade para write-able.</span><span class="sxs-lookup"><span data-stu-id="c524c-282">Initializing a frame resource, called when beginning a frame, transitions the depth stencil buffer to writeable.</span></span>


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



<span data-ttu-id="c524c-283">As barreiras são trocadas no meio do quadro, fazendo a transição do mapa de sombra de writeable para leitura.</span><span class="sxs-lookup"><span data-stu-id="c524c-283">Barriers are swapped mid-frame, transitioning the shadow map from writeable to readable.</span></span>


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



<span data-ttu-id="c524c-284">Concluir é chamado quando um quadro é encerrado, fazendo a transição do mapa de sombra para um estado comum.</span><span class="sxs-lookup"><span data-stu-id="c524c-284">Finish is called when a frame is ended, transitioning the shadow map to a common state.</span></span>


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a><span data-ttu-id="c524c-285">Exemplo comum de promoção de estado e decaimento</span><span class="sxs-lookup"><span data-stu-id="c524c-285">Common state promotion and decay sample</span></span>

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a><span data-ttu-id="c524c-286">Exemplo de barreiras de divisão</span><span class="sxs-lookup"><span data-stu-id="c524c-286">Example of split barriers</span></span>

<span data-ttu-id="c524c-287">O exemplo a seguir mostra como usar uma barreira de divisão para reduzir as paralisações de pipeline.</span><span class="sxs-lookup"><span data-stu-id="c524c-287">The following example shows how to use a split barrier to reduce pipeline stalls.</span></span> <span data-ttu-id="c524c-288">O código a seguir não usa barreiras de divisão:</span><span class="sxs-lookup"><span data-stu-id="c524c-288">The code that follows does not use split barriers:</span></span>

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

<span data-ttu-id="c524c-289">O código a seguir usa barreiras de divisão:</span><span class="sxs-lookup"><span data-stu-id="c524c-289">The following code uses split barriers:</span></span>

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a><span data-ttu-id="c524c-290">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c524c-290">Related topics</span></span>

[<span data-ttu-id="c524c-291">Tutoriais de vídeo de aprendizado avançado do DirectX: Barreiras de recursos e acompanhamento de estado</span><span class="sxs-lookup"><span data-stu-id="c524c-291">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</span></span>](https://www.youtube.com/watch?v=nmB2XMasz2o)

[<span data-ttu-id="c524c-292">Sincronização de vários mecanismos</span><span class="sxs-lookup"><span data-stu-id="c524c-292">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)

[<span data-ttu-id="c524c-293">Envio de trabalho no Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c524c-293">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)

[<span data-ttu-id="c524c-294">Uma olhada dentro das barreiras de estado do recurso D3D12</span><span class="sxs-lookup"><span data-stu-id="c524c-294">A Look Inside D3D12 Resource State Barriers</span></span>](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

