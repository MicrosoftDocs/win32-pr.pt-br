---
title: Usando barreiras de recursos para sincronizar Estados de recursos no Direct3D 12
description: Para reduzir o uso geral da CPU e habilitar o pré-processamento e o pós-processamento do driver, o Direct3D 12 move a responsabilidade do gerenciamento de estado por recurso do driver de gráficos para o aplicativo.
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c766f18e85ab8acc2ed0afad8e680d566a723a68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104548309"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a><span data-ttu-id="1bbc5-103">Usando barreiras de recursos para sincronizar Estados de recursos no Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1bbc5-103">Using Resource Barriers to Synchronize Resource States in Direct3D 12</span></span>

<span data-ttu-id="1bbc5-104">Para reduzir o uso geral da CPU e habilitar o pré-processamento e o pós-processamento do driver, o Direct3D 12 move a responsabilidade do gerenciamento de estado por recurso do driver de gráficos para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-104">To reduce overall CPU usage and enable driver multi-threading and pre-processing, Direct3D 12 moves the responsibility of per-resource state management from the graphics driver to the application.</span></span> <span data-ttu-id="1bbc5-105">Um exemplo de estado por recurso é se um recurso de textura está sendo acessado no momento como por meio de um sombreador Modo de Exibição de Recursos ou como uma exibição de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-105">An example of per-resource state is whether a texture resource is currently being accessed as through a Shader Resource View or as a Render Target View.</span></span> <span data-ttu-id="1bbc5-106">No Direct3D 11, os drivers eram necessários para acompanhar esse estado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-106">In Direct3D 11, drivers were required to track this state in the background.</span></span> <span data-ttu-id="1bbc5-107">Isso é caro do ponto de vista da CPU e complica significativamente qualquer tipo de design multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-107">This is expensive from a CPU perspective and significantly complicates any sort of multi-threaded design.</span></span> <span data-ttu-id="1bbc5-108">No Microsoft Direct3D 12, a maioria dos Estados por recurso é gerenciada pelo aplicativo com uma única API, [**ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="1bbc5-108">In Microsoft Direct3D 12, most per-resource state is managed by the application with a single API, [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

-   [<span data-ttu-id="1bbc5-109">Usando a API ResourceBarrier para gerenciar o estado por recurso</span><span class="sxs-lookup"><span data-stu-id="1bbc5-109">Using the ResourceBarrier API to manage per-resource state</span></span>](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [<span data-ttu-id="1bbc5-110">Estados de recursos</span><span class="sxs-lookup"><span data-stu-id="1bbc5-110">Resource states</span></span>](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [<span data-ttu-id="1bbc5-111">Estados iniciais de recursos</span><span class="sxs-lookup"><span data-stu-id="1bbc5-111">Initial states for resources</span></span>](#initial-states-for-resources)
    -   [<span data-ttu-id="1bbc5-112">Restrições de estado do recurso de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1bbc5-112">Read/write resource state restrictions</span></span>](#readwrite-resource-state-restrictions)
    -   [<span data-ttu-id="1bbc5-113">Estados de recursos para apresentar buffers de fundo</span><span class="sxs-lookup"><span data-stu-id="1bbc5-113">Resource states for presenting back buffers</span></span>](#resource-states-for-presenting-back-buffers)
    -   [<span data-ttu-id="1bbc5-114">Descartando recursos</span><span class="sxs-lookup"><span data-stu-id="1bbc5-114">Discarding resources</span></span>](#discarding-resources)
-   [<span data-ttu-id="1bbc5-115">Transições de estado implícitas</span><span class="sxs-lookup"><span data-stu-id="1bbc5-115">Implicit State Transitions</span></span>](#implicit-state-transitions)
    -   [<span data-ttu-id="1bbc5-116">Promoção de Estado comum</span><span class="sxs-lookup"><span data-stu-id="1bbc5-116">Common state promotion</span></span>](#common-state-promotion)
    -   [<span data-ttu-id="1bbc5-117">Estado decaimento para comum</span><span class="sxs-lookup"><span data-stu-id="1bbc5-117">State decay to common</span></span>](#state-decay-to-common)
    -   [<span data-ttu-id="1bbc5-118">Implicações de desempenho</span><span class="sxs-lookup"><span data-stu-id="1bbc5-118">Performance implications</span></span>](#performance-implications)
-   [<span data-ttu-id="1bbc5-119">Barreiras de divisão</span><span class="sxs-lookup"><span data-stu-id="1bbc5-119">Split Barriers</span></span>](#split-barriers)
-   [<span data-ttu-id="1bbc5-120">Cenário de exemplo de barreira de recurso</span><span class="sxs-lookup"><span data-stu-id="1bbc5-120">Resource barrier example scenario</span></span>](#resource-barrier-example-scenario)
-   [<span data-ttu-id="1bbc5-121">Promoção de Estado comum e exemplo de decaimento</span><span class="sxs-lookup"><span data-stu-id="1bbc5-121">Common state promotion and decay sample</span></span>](#common-state-promotion-and-decay-sample)
-   [<span data-ttu-id="1bbc5-122">Exemplo de barreiras de divisão</span><span class="sxs-lookup"><span data-stu-id="1bbc5-122">Example of split barriers</span></span>](#example-of-split-barriers)
-   [<span data-ttu-id="1bbc5-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bbc5-123">Related topics</span></span>](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a><span data-ttu-id="1bbc5-124">Usando a API ResourceBarrier para gerenciar o estado por recurso</span><span class="sxs-lookup"><span data-stu-id="1bbc5-124">Using the ResourceBarrier API to manage per-resource state</span></span>

<span data-ttu-id="1bbc5-125">O [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifica o driver de gráficos de situações em que o driver pode precisar sincronizar vários acessos à memória na qual um recurso está armazenado.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-125">[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) notifies the graphics driver of situations in which the driver may need to synchronize multiple accesses to the memory in which a resource is stored.</span></span> <span data-ttu-id="1bbc5-126">O método é chamado com uma ou mais estruturas de descrição de barreira de recurso que indicam o tipo de barreira de recurso que está sendo declarado.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-126">The method is called with one or more resource barrier description structures indicating the type of resource barrier being declared.</span></span>

<span data-ttu-id="1bbc5-127">Há três tipos de barreiras de recursos:</span><span class="sxs-lookup"><span data-stu-id="1bbc5-127">There are three types of resource barriers:</span></span>

-   <span data-ttu-id="1bbc5-128">**Barreira de transição** – uma barreira de transição indica que um conjunto de subrecursos faz a transição entre diferentes usos.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-128">**Transition barrier** - A transition barrier indicates that a set of subresources transition between different usages.</span></span> <span data-ttu-id="1bbc5-129">Uma estrutura de [**barreira de \_ transição de recursos \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) é usada para especificar o subrecurso que está em transição, bem como os Estados de *antes* e *depois* do subrecurso.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-129">A [**D3D12\_RESOURCE\_TRANSITION\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier) structure is used to specify the subresource that is transitioning as well as the *before* and *after* states of the subresource.</span></span>

    <span data-ttu-id="1bbc5-130">O sistema verifica se as transições de subrecurso em uma lista de comandos são consistentes com as transições anteriores na mesma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-130">The system verifies that subresource transitions in a command list are consistent with previous transitions in the same command list.</span></span> <span data-ttu-id="1bbc5-131">A camada de depuração rastreia ainda mais o estado do subrecurso para encontrar outros erros, no entanto, essa validação é conservadora e não exaustiva.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-131">The debug layer further tracks subresource state to find other errors however this validation is conservative and not exhaustive.</span></span>

    <span data-ttu-id="1bbc5-132">Observe que você pode usar o \_ sinalizador D3D12 \_ de \_ todos os \_ subrecursos de barreira de recursos para especificar que todos os subrecursos em um recurso estão sendo transferidos.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-132">Note that you can use the D3D12\_RESOURCE\_BARRIER\_ALL\_SUBRESOURCES flag to specify that all subresources within a resource are being transitioned.</span></span>

-   <span data-ttu-id="1bbc5-133">**Barreira de alias** – uma barreira de alias indica uma transição entre os usos de dois recursos diferentes que têm mapeamentos sobrepostos no mesmo heap.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-133">**Aliasing barrier** - An aliasing barrier indicates a transition between usages of two different resources which have overlapping mappings into the same heap.</span></span> <span data-ttu-id="1bbc5-134">Isso se aplica a recursos reservados e colocados.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-134">This applies to both reserved and placed resources.</span></span> <span data-ttu-id="1bbc5-135">Uma estrutura de [**barreira de \_ alias de recursos \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) é usada para especificar o recurso *before* e o *After* .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-135">A [**D3D12\_RESOURCE\_ALIASING\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier) structure is used to specify both the *before* resource and the *after* resource.</span></span>

    <span data-ttu-id="1bbc5-136">Observe que um ou ambos os recursos podem ser nulos, o que indica que qualquer recurso de ladrilho pode causar alias.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-136">Note that one or both resources can be NULL, which indicates that any tiled resource could cause aliasing.</span></span> <span data-ttu-id="1bbc5-137">Para obter mais informações sobre o uso de recursos em ladrilho, consulte recursos de [lado](../direct3d11/tiled-resources.md) e de [volume](volume-tiled-resources.md).</span><span class="sxs-lookup"><span data-stu-id="1bbc5-137">For more information about using tiled resources, see [Tiled resources](../direct3d11/tiled-resources.md) and [Volume Tiled Resources](volume-tiled-resources.md).</span></span>

-   <span data-ttu-id="1bbc5-138">**Barreira de modo de exibição de acesso não ordenado (UAV)** -uma barreira UAV indica que todos os acessos de UAV, leitura ou gravação, a um recurso específico devem ser concluídos entre quaisquer acessos UAV futuros, leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-138">**Unordered access view (UAV) barrier** - A UAV barrier indicates that all UAV accesses, both read or write, to a particular resource must complete between any future UAV accesses, both read or write.</span></span> <span data-ttu-id="1bbc5-139">Não é necessário que um aplicativo Coloque uma barreira de UAV entre duas chamadas de desenho ou expedição que só lêem de um UAV.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-139">It's not necessary for an app to put a UAV barrier between two draw or dispatch calls that only read from a UAV.</span></span> <span data-ttu-id="1bbc5-140">Além disso, não é necessário colocar uma barreira UAV entre duas chamadas Draw ou Dispatch que gravam no mesmo UAV se o aplicativo sabe que é seguro executar o acesso de UAV em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-140">Also, it's not necessary to put a UAV barrier between two draw or dispatch calls that write to the same UAV if the application knows that it is safe to execute the UAV access in any order.</span></span> <span data-ttu-id="1bbc5-141">Uma estrutura de [**\_ barreira de \_ UAV \_ de recursos D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) é usada para especificar o recurso de UAV ao qual a barreira se aplica.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-141">A [**D3D12\_RESOURCE\_UAV\_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier) structure is used to specify the UAV resource to which the barrier applies.</span></span> <span data-ttu-id="1bbc5-142">O aplicativo pode especificar NULL para o UAV da barreira, o que indica que qualquer acesso UAV poderia exigir a barreira.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-142">The application can specify NULL for the barrier's UAV, which indicates that any UAV access could require the barrier.</span></span>

<span data-ttu-id="1bbc5-143">Quando [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) é chamado com uma matriz de descrições de barreira de recursos, a API se comporta como se fosse chamada uma vez para cada elemento, na ordem em que foram fornecidas.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-143">When [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) is called with an array of resource barrier descriptions, the API behaves as if it was called once for each element, in the order in which they were supplied.</span></span>

<span data-ttu-id="1bbc5-144">A qualquer momento, um subrecurso está em exatamente um estado, determinado pelo conjunto de sinalizadores de [**\_ \_ Estados de recursos D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) fornecidos para [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="1bbc5-144">At any given time, a subresource is in exactly one state, determined by the set of [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) flags supplied to [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span> <span data-ttu-id="1bbc5-145">O aplicativo deve garantir que os Estados de *antes* e *depois* de chamadas consecutivas para **ResourceBarrier** concordem.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-145">The application must ensure that the *before* and *after* states of consecutive calls to **ResourceBarrier** agree.</span></span>

> [!TIP]
>
> <span data-ttu-id="1bbc5-146">Os aplicativos devem fazer várias transições em lote em uma chamada à API sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-146">Applications should batch multiple transitions into one API call wherever possible.</span></span>

 

### <a name="resource-states"></a><span data-ttu-id="1bbc5-147">Estados de recursos</span><span class="sxs-lookup"><span data-stu-id="1bbc5-147">Resource states</span></span>

<span data-ttu-id="1bbc5-148">Para obter a lista completa de Estados de recursos em que um recurso pode fazer a transição, consulte o tópico de referência para a enumeração de [**\_ \_ Estados de recursos do D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-148">For the complete list of resource states that a resource can transition between, see the reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) enumeration.</span></span>

<span data-ttu-id="1bbc5-149">Para barreiras de recurso dividido, consulte também [**os \_ \_ \_ sinalizadores de barreira de recurso D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span><span class="sxs-lookup"><span data-stu-id="1bbc5-149">For split resource barriers, also refer to [**D3D12\_RESOURCE\_BARRIER\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags).</span></span>

### <a name="initial-states-for-resources"></a><span data-ttu-id="1bbc5-150">Estados iniciais de recursos</span><span class="sxs-lookup"><span data-stu-id="1bbc5-150">Initial states for resources</span></span>

<span data-ttu-id="1bbc5-151">Os recursos podem ser criados com qualquer estado inicial especificado pelo usuário (válido para a descrição do recurso), com as seguintes exceções:</span><span class="sxs-lookup"><span data-stu-id="1bbc5-151">Resources may be created with any user-specified initial state (valid for the resource description), with the following exceptions:</span></span>

-   <span data-ttu-id="1bbc5-152">Os heaps de carregamento devem começar no estado D3D12 de \_ recursos de estado de recurso \_ \_ \_ de leitura genérica, que é uma combinação de bits ou de:</span><span class="sxs-lookup"><span data-stu-id="1bbc5-152">Upload heaps must start out in the state D3D12\_RESOURCE\_STATE\_GENERIC\_READ which is a bitwise OR combination of:</span></span>
    -   <span data-ttu-id="1bbc5-153">\_Vértice do estado do recurso D3D12 \_ \_ \_ e buffer de \_ constante \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-153">D3D12\_RESOURCE\_STATE\_VERTEX\_AND\_CONSTANT\_BUFFER</span></span>
    -   <span data-ttu-id="1bbc5-154">\_Buffer de \_ índice de estado do recurso D3D12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-154">D3D12\_RESOURCE\_STATE\_INDEX\_BUFFER</span></span>
    -   <span data-ttu-id="1bbc5-155">\_Fonte de \_ cópia de estado do recurso D3D12 \_ \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-155">D3D12\_RESOURCE\_STATE\_COPY\_SOURCE</span></span>
    -   <span data-ttu-id="1bbc5-156">\_Recurso de \_ \_ \_ \_ sombreador não pixel \_ do estado do recurso D3D12</span><span class="sxs-lookup"><span data-stu-id="1bbc5-156">D3D12\_RESOURCE\_STATE\_NON\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="1bbc5-157">\_Recurso D3D12 \_ \_ \_ sombreador de pixel do estado do recurso \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-157">D3D12\_RESOURCE\_STATE\_PIXEL\_SHADER\_RESOURCE</span></span>
    -   <span data-ttu-id="1bbc5-158">\_ \_ \_ Argumento indireto de estado do recurso D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-158">D3D12\_RESOURCE\_STATE\_INDIRECT\_ARGUMENT</span></span>
-   <span data-ttu-id="1bbc5-159">Os heaps readback devem começar no estado de \_ destino da cópia de estado do recurso D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-159">Readback heaps must start out in the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span>
-   <span data-ttu-id="1bbc5-160">Buffers de back de cadeia de permuta iniciam automaticamente \_ no \_ estado comum do estado do recurso D3D12 \_ .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-160">Swap chain back buffers automatically start out in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span>

<span data-ttu-id="1bbc5-161">Antes que um heap possa ser o destino de uma operação de cópia de GPU, normalmente o heap deve primeiro ser transferido para o \_ estado de destino da cópia de estado do recurso D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-161">Before a heap can be the target of a GPU copy operation, normally the heap must first be transitioned to the D3D12\_RESOURCE\_STATE\_COPY\_DEST state.</span></span> <span data-ttu-id="1bbc5-162">No entanto, os recursos criados em heaps de carregamento devem começar no e não podem ser alterados a partir do \_ estado de leitura genérico, pois apenas a CPU estará escrevendo.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-162">However, resources created on UPLOAD heaps must start in and cannot change from the GENERIC\_READ state since only the CPU will be doing writing.</span></span> <span data-ttu-id="1bbc5-163">Por outro lado, os recursos confirmados criados em heaps READBACK devem começar no e não podem mudar a partir do estado de destino da cópia \_ .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-163">Conversely, committed resources created in READBACK heaps must start in and cannot change from the COPY\_DEST state.</span></span>

### <a name="readwrite-resource-state-restrictions"></a><span data-ttu-id="1bbc5-164">Restrições de estado do recurso de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1bbc5-164">Read/write resource state restrictions</span></span>

<span data-ttu-id="1bbc5-165">Os bits de uso de estado do recurso que são usados para descrever um estado de recurso são divididos em Estados somente leitura e de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-165">The resource state usage bits that are used to describe a resource state are divided into read-only and read/write states.</span></span> <span data-ttu-id="1bbc5-166">O tópico de referência para [**os \_ \_ Estados de recurso D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indica o nível de acesso de leitura/gravação para cada bit na enumeração.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-166">The reference topic for the [**D3D12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) indicates the read/write access level for each bit in the enumeration.</span></span>

<span data-ttu-id="1bbc5-167">No máximo, apenas um bit de leitura/gravação pode ser definido para qualquer recurso.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-167">At most, only one read/write bit can be set for any resource.</span></span> <span data-ttu-id="1bbc5-168">Se um bit de gravação for definido, nenhum bit somente leitura poderá ser definido para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-168">If a write bit is set, then no read-only bit may be set for that resource.</span></span> <span data-ttu-id="1bbc5-169">Se nenhum bit de gravação for definido, qualquer número de bits de leitura poderá ser definido.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-169">If no write bit is set, then any number of read bits may be set.</span></span>

### <a name="resource-states-for-presenting-back-buffers"></a><span data-ttu-id="1bbc5-170">Estados de recursos para apresentar buffers de fundo</span><span class="sxs-lookup"><span data-stu-id="1bbc5-170">Resource states for presenting back buffers</span></span>

<span data-ttu-id="1bbc5-171">Antes de um buffer de fundo ser apresentado, ele deve estar no \_ estado comum do estado do recurso D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-171">Before a back buffer is presented, it must be in the D3D12\_RESOURCE\_STATE\_COMMON state.</span></span> <span data-ttu-id="1bbc5-172">Observe que o estado do recurso D3D12 \_ Resource State \_ \_ presente é um sinônimo para o \_ estado do recurso D3D12 \_ \_ comum, e ambos têm um valor de 0.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-172">Note, the resource state D3D12\_RESOURCE\_STATE\_PRESENT is a synonym for D3D12\_RESOURCE\_STATE\_COMMON, and they both have a value of 0.</span></span> <span data-ttu-id="1bbc5-173">Se [**IDXGISwapChain::P reenviado**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (ou [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) for chamado em um recurso que não está atualmente nesse estado, um aviso de camada de depuração será emitido.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-173">If [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) (or [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) is called on a resource that is not currently in this state, a debug layer warning is emitted.</span></span>

### <a name="discarding-resources"></a><span data-ttu-id="1bbc5-174">Descartando recursos</span><span class="sxs-lookup"><span data-stu-id="1bbc5-174">Discarding resources</span></span>

<span data-ttu-id="1bbc5-175">Todos os subrecursos em um recurso devem estar no estado de destino de RENDERIZAÇÃO \_ ou no \_ estado de gravação de profundidade, para os recursos destinos de renderização/estêncil de profundidade, respectivamente, quando [**ID3D12GraphicsCommandList::D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) é chamado.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-175">All subresources in a resource must be in the RENDER\_TARGET state, or DEPTH\_WRITE state, for render targets/depth-stencil resources respectively, when [**ID3D12GraphicsCommandList::DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) is called.</span></span>

## <a name="implicit-state-transitions"></a><span data-ttu-id="1bbc5-176">Transições de estado implícitas</span><span class="sxs-lookup"><span data-stu-id="1bbc5-176">Implicit State Transitions</span></span>

<span data-ttu-id="1bbc5-177">Os recursos só podem ser "promovidos" fora do \_ estado de recurso D3D12 \_ \_ comum.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-177">Resources can only be "promoted" out of D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="1bbc5-178">Da mesma forma, os recursos só "decaimento" para o \_ estado do recurso D3D12 \_ \_ comum.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-178">Similarly, resources will only "decay" to D3D12\_RESOURCE\_STATE\_COMMON.</span></span>

### <a name="common-state-promotion"></a><span data-ttu-id="1bbc5-179">Promoção de Estado comum</span><span class="sxs-lookup"><span data-stu-id="1bbc5-179">Common state promotion</span></span>

<span data-ttu-id="1bbc5-180">Todos os recursos de buffer, bem como texturas com o \_ sinalizador de recurso D3D12 permitir o conjunto de \_ \_ \_ \_ sinalizadores de acesso simultâneo, são promovidos implicitamente do \_ estado do recurso D3D12 \_ \_ comum para o estado relevante no primeiro acesso à GPU, incluindo \_ leitura genérica para cobrir qualquer cenário de leitura.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-180">All buffer resources as well as textures with the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set are implicitly promoted from D3D12\_RESOURCE\_STATE\_COMMON to the relevant state on first GPU access, including GENERIC\_READ to cover any read scenario.</span></span> <span data-ttu-id="1bbc5-181">Qualquer recurso no estado comum pode ser acessado como se estivesse em um único estado com</span><span class="sxs-lookup"><span data-stu-id="1bbc5-181">Any resource in the COMMON state can be accessed as through it were in a single state with</span></span>

<dl> <span data-ttu-id="1bbc5-182">1 sinalizador de gravação ou</span><span class="sxs-lookup"><span data-stu-id="1bbc5-182">1 WRITE flag, or</span></span>  
<span data-ttu-id="1bbc5-183">1 ou mais sinalizadores de leitura</span><span class="sxs-lookup"><span data-stu-id="1bbc5-183">1 or more READ flags</span></span>  
</dl>

<span data-ttu-id="1bbc5-184">Os recursos podem ser promovidos do Estado comum com base na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="1bbc5-184">Resources can be promoted from the COMMON state based on the following table:</span></span>



| <span data-ttu-id="1bbc5-185">Sinalizador de estado</span><span class="sxs-lookup"><span data-stu-id="1bbc5-185">State flag</span></span>                    | <span data-ttu-id="1bbc5-186">Estado da promoçãotable</span><span class="sxs-lookup"><span data-stu-id="1bbc5-186">Promotable State</span></span>                             |                                      |
|-------------------------------|----------------------------------------------|--------------------------------------|
|                               | <span data-ttu-id="1bbc5-187">**Buffers e texturas de Simultaneous-Access**</span><span class="sxs-lookup"><span data-stu-id="1bbc5-187">**Buffers and Simultaneous-Access Textures**</span></span> | <span data-ttu-id="1bbc5-188">**Texturas de acesso não simultâneo**</span><span class="sxs-lookup"><span data-stu-id="1bbc5-188">**Non-Simultaneous-Access Textures**</span></span> |
| <span data-ttu-id="1bbc5-189">VÉRTICE \_ e \_ buffer de constantes \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-189">VERTEX\_AND\_CONSTANT\_BUFFER</span></span> | <span data-ttu-id="1bbc5-190">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-190">Yes</span></span>                                          | <span data-ttu-id="1bbc5-191">Não</span><span class="sxs-lookup"><span data-stu-id="1bbc5-191">No</span></span>                                   |
| <span data-ttu-id="1bbc5-192">BUFFER de índice \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-192">INDEX\_BUFFER</span></span>                 | <span data-ttu-id="1bbc5-193">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-193">Yes</span></span>                                          | <span data-ttu-id="1bbc5-194">Não</span><span class="sxs-lookup"><span data-stu-id="1bbc5-194">No</span></span>                                   |
| <span data-ttu-id="1bbc5-195">destino de RENDERIZAÇÃO \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-195">RENDER\_TARGET</span></span>                | <span data-ttu-id="1bbc5-196">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-196">Yes</span></span>                                          | <span data-ttu-id="1bbc5-197">Não</span><span class="sxs-lookup"><span data-stu-id="1bbc5-197">No</span></span>                                   |
| <span data-ttu-id="1bbc5-198">acesso não ordenado \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-198">UNORDERED\_ACCESS</span></span>             | <span data-ttu-id="1bbc5-199">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-199">Yes</span></span>                                          | <span data-ttu-id="1bbc5-200">Não</span><span class="sxs-lookup"><span data-stu-id="1bbc5-200">No</span></span>                                   |
| <span data-ttu-id="1bbc5-201">gravação de profundidade \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-201">DEPTH\_WRITE</span></span>                  | <span data-ttu-id="1bbc5-202">Não<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1bbc5-202">No<sup>\*</sup></span></span>                              | <span data-ttu-id="1bbc5-203">Não</span><span class="sxs-lookup"><span data-stu-id="1bbc5-203">No</span></span>                                   |
| <span data-ttu-id="1bbc5-204">leitura de profundidade \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-204">DEPTH\_READ</span></span>                   | <span data-ttu-id="1bbc5-205">Não<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1bbc5-205">No<sup>\*</sup></span></span>                              | <span data-ttu-id="1bbc5-206">Não</span><span class="sxs-lookup"><span data-stu-id="1bbc5-206">No</span></span>                                   |
| <span data-ttu-id="1bbc5-207">\_recurso de \_ sombreador não pixel \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-207">NON\_PIXEL\_SHADER\_RESOURCE</span></span>  | <span data-ttu-id="1bbc5-208">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-208">Yes</span></span>                                          | <span data-ttu-id="1bbc5-209">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-209">Yes</span></span>                                  |
| <span data-ttu-id="1bbc5-210">\_recurso sombreador de pixel \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-210">PIXEL\_SHADER\_RESOURCE</span></span>       | <span data-ttu-id="1bbc5-211">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-211">Yes</span></span>                                          | <span data-ttu-id="1bbc5-212">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-212">Yes</span></span>                                  |
| <span data-ttu-id="1bbc5-213">saída de fluxo \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-213">STREAM\_OUT</span></span>                   | <span data-ttu-id="1bbc5-214">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-214">Yes</span></span>                                          | <span data-ttu-id="1bbc5-215">Não</span><span class="sxs-lookup"><span data-stu-id="1bbc5-215">No</span></span>                                   |
| <span data-ttu-id="1bbc5-216">argumento indireto \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-216">INDIRECT\_ARGUMENT</span></span>            | <span data-ttu-id="1bbc5-217">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-217">Yes</span></span>                                          | <span data-ttu-id="1bbc5-218">Não</span><span class="sxs-lookup"><span data-stu-id="1bbc5-218">No</span></span>                                   |
| <span data-ttu-id="1bbc5-219">COPIAR \_ dest</span><span class="sxs-lookup"><span data-stu-id="1bbc5-219">COPY\_DEST</span></span>                    | <span data-ttu-id="1bbc5-220">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-220">Yes</span></span>                                          | <span data-ttu-id="1bbc5-221">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-221">Yes</span></span>                                  |
| <span data-ttu-id="1bbc5-222">origem da cópia \_</span><span class="sxs-lookup"><span data-stu-id="1bbc5-222">COPY\_SOURCE</span></span>                  | <span data-ttu-id="1bbc5-223">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-223">Yes</span></span>                                          | <span data-ttu-id="1bbc5-224">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-224">Yes</span></span>                                  |
| <span data-ttu-id="1bbc5-225">RESOLVER \_ dest</span><span class="sxs-lookup"><span data-stu-id="1bbc5-225">RESOLVE\_DEST</span></span>                 | <span data-ttu-id="1bbc5-226">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-226">Yes</span></span>                                          | <span data-ttu-id="1bbc5-227">Não</span><span class="sxs-lookup"><span data-stu-id="1bbc5-227">No</span></span>                                   |
| <span data-ttu-id="1bbc5-228">RESOLVER \_ origem</span><span class="sxs-lookup"><span data-stu-id="1bbc5-228">RESOLVE\_SOURCE</span></span>               | <span data-ttu-id="1bbc5-229">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-229">Yes</span></span>                                          | <span data-ttu-id="1bbc5-230">Não</span><span class="sxs-lookup"><span data-stu-id="1bbc5-230">No</span></span>                                   |
| <span data-ttu-id="1bbc5-231">PREDICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="1bbc5-231">PREDICATION</span></span>                   | <span data-ttu-id="1bbc5-232">Sim</span><span class="sxs-lookup"><span data-stu-id="1bbc5-232">Yes</span></span>                                          | <span data-ttu-id="1bbc5-233">Não</span><span class="sxs-lookup"><span data-stu-id="1bbc5-233">No</span></span>                                   |



 

<span data-ttu-id="1bbc5-234"><sup>\*</sup>Os recursos do estêncil de profundidade devem ser texturas de acesso não simultâneas e, portanto, nunca podem ser promovidas implicitamente.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-234"><sup>\*</sup>Depth-stencil resources must be non-simultaneous-access textures and thus can never be implicitly promoted.</span></span>

<span data-ttu-id="1bbc5-235">Quando esse acesso ocorre, a promoção age como uma barreira de recursos implícita.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-235">When this access occurs the promotion acts like an implicit resource barrier.</span></span> <span data-ttu-id="1bbc5-236">Para os acessos subsequentes, as barreiras de recursos serão necessárias para alterar o estado do recurso, se necessário.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-236">For subsequent accesses, resource barriers will be required to change the resource state if necessary.</span></span> <span data-ttu-id="1bbc5-237">Observe que a promoção de um estado de leitura promovido em vários Estados de leitura é válida, mas esse não é o caso para os Estados de gravação.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-237">Note that promotion from one promoted read state into multiple read state is valid, but this is not the case for write states.</span></span>  
<span data-ttu-id="1bbc5-238">Por exemplo, se um recurso no estado comum for promovido para recurso de \_ sombreador \_ de pixel em uma chamada de desenho, ele ainda poderá ser promovido para NON_PIXEL \_ recurso de sombreador \_ | \_ \_ Recurso de sombreador de pixel em outra chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-238">For example, if a resource in the common state is promoted to PIXEL\_SHADER\_RESOURCE in a Draw call, it can still be promoted to NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE in another Draw call.</span></span> <span data-ttu-id="1bbc5-239">No entanto, se ele for usado em uma operação de gravação, como um destino de cópia, uma barreira de transição de estado de recurso dos Estados de leitura promovidos combinados, aqui NON_PIXEL \_ recurso de sombreador \_ | O \_ \_ recurso de sombreador de pixel, para copiar \_ dest é necessário.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-239">However, if it is used in a write operation, such as a copy destination, a resource state transition barrier from the combined promoted read states, here NON_PIXEL\_SHADER\_RESOURCE | PIXEL\_SHADER\_RESOURCE, to COPY\_DEST is needed.</span></span>  
<span data-ttu-id="1bbc5-240">Da mesma forma, se for promovido de COMMON para COPY \_ dest, uma barreira ainda será necessária para fazer a transição do dest de cópia \_ para o destino de renderização \_ .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-240">Similarly, if promoted from COMMON to COPY\_DEST, a barrier is still required to transition from COPY\_DEST to RENDER\_TARGET.</span></span>

<span data-ttu-id="1bbc5-241">Observe que a promoção de Estado comum é "gratuita", pois não há necessidade de a GPU executar qualquer espera de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-241">Note that common state promotion is "free" in that there is no need for the GPU to perform any synchronization waits.</span></span> <span data-ttu-id="1bbc5-242">A promoção representa o fato de que os recursos no estado comum não devem exigir acompanhamento de driver ou trabalho de GPU adicional para dar suporte a determinados acessos.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-242">The promotion represents the fact that resources in the COMMON state should not require additional GPU work or driver tracking to support certain accesses.</span></span>

### <a name="state-decay-to-common"></a><span data-ttu-id="1bbc5-243">Estado decaimento para comum</span><span class="sxs-lookup"><span data-stu-id="1bbc5-243">State decay to common</span></span>

<span data-ttu-id="1bbc5-244">O lado do inverso da promoção de Estado comum é decaimento de volta para o \_ estado de recurso D3D12 \_ \_ comum.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-244">The flip-side of common state promotion is decay back to D3D12\_RESOURCE\_STATE\_COMMON.</span></span> <span data-ttu-id="1bbc5-245">Os recursos que atendem a determinados requisitos são considerados sem estado e efetivamente retornam ao Estado comum quando a GPU conclui a execução de uma operação [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-245">Resources that meet certain requirements are considered to be stateless and effectively return to the common state when the GPU finishes execution of an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation.</span></span> <span data-ttu-id="1bbc5-246">Decaimento não ocorre entre as listas de comandos executadas juntas na mesma chamada **ExecuteCommandLists** .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-246">Decay does not occur between command lists executed together in the same **ExecuteCommandLists** call.</span></span>

<span data-ttu-id="1bbc5-247">Os seguintes recursos serão decaimentodos quando uma operação [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) for concluída na GPU:</span><span class="sxs-lookup"><span data-stu-id="1bbc5-247">The following resources will decay when an [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) operation is completed on the GPU:</span></span>

-   <span data-ttu-id="1bbc5-248">Recursos que estão sendo acessados em uma fila de cópia *ou*</span><span class="sxs-lookup"><span data-stu-id="1bbc5-248">Resources being accessed on a Copy queue, *or*</span></span>
-   <span data-ttu-id="1bbc5-249">Recursos de buffer em qualquer tipo de fila *ou*</span><span class="sxs-lookup"><span data-stu-id="1bbc5-249">Buffer resources on any queue type, *or*</span></span>
-   <span data-ttu-id="1bbc5-250">Recursos de textura em qualquer tipo de fila que têm o \_ sinalizador de recurso D3D12 \_ \_ permitir conjunto de \_ \_ sinalizadores de acesso simultâneos *ou*</span><span class="sxs-lookup"><span data-stu-id="1bbc5-250">Texture resources on any queue type that have the D3D12\_RESOURCE\_FLAG\_ALLOW\_SIMULTANEOUS\_ACCESS flag set, *or*</span></span>
-   <span data-ttu-id="1bbc5-251">Qualquer recurso promovido implicitamente para um estado somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-251">Any resource implicitly promoted to a read-only state.</span></span>

<span data-ttu-id="1bbc5-252">Como a promoção de Estado comum, o decaimento é gratuito, pois nenhuma sincronização adicional é necessária.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-252">Like common state promotion, the decay is free in that no additional synchronization is needed.</span></span> <span data-ttu-id="1bbc5-253">A combinação de promoção de Estado comum e decaimento pode ajudar a eliminar muitas transições de [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-253">Combining common state promotion and decay can help to eliminate many unnecessary [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions.</span></span> <span data-ttu-id="1bbc5-254">Em alguns casos, isso pode fornecer melhorias significativas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-254">In some cases, this can provide significant performance improvements.</span></span>

<span data-ttu-id="1bbc5-255">Os buffers e Simultaneous-Access recursos decaimentoão o estado comum, independentemente de terem sido explicitamente transferidos usando barreiras de recursos ou promovidas implicitamente.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-255">Buffers and Simultaneous-Access resources will decay to the common state regardless of whether they were explicitly transitioned using resource barriers or implicitly promoted.</span></span>

### <a name="performance-implications"></a><span data-ttu-id="1bbc5-256">Implicações de desempenho</span><span class="sxs-lookup"><span data-stu-id="1bbc5-256">Performance implications</span></span>

<span data-ttu-id="1bbc5-257">Ao registrar transições [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explícitas em recursos no estado comum, é correto usar o estado do \_ recurso D3D12 \_ \_ comum ou qualquer estado de promotable como o valor *anterior* na estrutura de barreira de transição de recursos do D3D12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-257">When recording explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions on resources in the common state, it is correct to use either D3D12\_RESOURCE\_STATE\_COMMON or any promotable state as the *BeforeState* value in the D3D12\_RESOURCE\_TRANSITION\_BARRIER structure.</span></span> <span data-ttu-id="1bbc5-258">Isso permite o gerenciamento de estado tradicional que ignora o decaimento automático de buffers e texturas de acesso simultâneo.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-258">This allows traditional state management that ignores automatic decay of buffers and simultaneous-access textures.</span></span> <span data-ttu-id="1bbc5-259">No entanto, isso pode não ser desejável, pois evitar que chamadas de **ResourceBarrier** de transição com recursos conhecidos para estar no estado comum pode melhorar significativamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-259">This may not be desirable though, as avoiding transition **ResourceBarrier** calls with resources known to be in the common state can significantly improve performance.</span></span> <span data-ttu-id="1bbc5-260">As barreiras de recursos podem ser caras.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-260">Resource barriers can be expensive.</span></span> <span data-ttu-id="1bbc5-261">Elas são projetadas para forçar liberações de cache, alterações de layout de memória e outras sincronizações que podem não ser necessárias para os recursos que já estão no estado comum.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-261">They are designed to force cache flushes, memory layout changes and other synchronization that may not be necessary for resources already in the common state.</span></span> <span data-ttu-id="1bbc5-262">Uma lista de comandos que usa uma barreira de recurso de um estado não comum para outro Estado não comum em um recurso atualmente no estado comum pode introduzir muita sobrecarga desnecessária.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-262">A command list that uses a resource barrier from a non-common state to another non-common state on a resource currently in the common state can introduce a lot of unneeded overhead.</span></span>

<span data-ttu-id="1bbc5-263">Além disso, evite transições [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) explícitas \_ para \_ o estado do recurso D3D12 \_ comum, a menos que seja absolutamente necessário (por exemplo, o próximo acesso está em uma fila de comando de cópia que exige que os recursos comecem no estado comum).</span><span class="sxs-lookup"><span data-stu-id="1bbc5-263">Also, avoid explicit [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) transitions to D3D12\_RESOURCE\_STATE\_COMMON unless absolutely necessary (e.g. the next access is on a COPY command queue which requires a resources begin in the common state).</span></span> <span data-ttu-id="1bbc5-264">As transições excessivas para o estado comum podem reduzir drasticamente o desempenho da GPU.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-264">Excessive transitions to the common state can dramatically slow down GPU performance.</span></span>

<span data-ttu-id="1bbc5-265">Em resumo, tente contar com a promoção de Estado comum e decaimento sempre que sua semântica permitir que você saia sem emitir chamadas [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) .</span><span class="sxs-lookup"><span data-stu-id="1bbc5-265">In summary, try to rely on common state promotion and decay whenever its semantics let you get away without issuing [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) calls.</span></span>

## <a name="split-barriers"></a><span data-ttu-id="1bbc5-266">Barreiras de divisão</span><span class="sxs-lookup"><span data-stu-id="1bbc5-266">Split Barriers</span></span>

<span data-ttu-id="1bbc5-267">Uma barreira de transição de recurso com o sinalizador de barreira de D3D12 de \_ recursos \_ \_ \_ inicial \_ só começa uma barreira de divisão e a barreira de transição é considerada pendente.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-267">A resource transition barrier with the D3D12\_RESOURCE\_BARRIER\_FLAG\_BEGIN\_ONLY flag begins a split barrier and the transition barrier is said to be pending.</span></span> <span data-ttu-id="1bbc5-268">Embora a barreira esteja pendente, o recurso (sub) não pode ser lido ou gravado pela GPU.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-268">While the barrier is pending the (sub)resource cannot be read or written by the GPU.</span></span> <span data-ttu-id="1bbc5-269">A única barreira de transição legal que pode ser aplicada a um recurso (sub) com uma barreira pendente é uma com o mesmo estado *anterior* e *posterior* e o \_ sinalizador de finalização do sinalizador de barreira de recursos D3D12 \_ \_ \_ \_ , que a barreira conclui a transição pendente.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-269">The only legal transition barrier that can be applied to a (sub)resource with a pending barrier is one with the same *before* and *after* states and the D3D12\_RESOURCE\_BARRIER\_FLAG\_END\_ONLY flag, which barrier completes the pending transition.</span></span>

<span data-ttu-id="1bbc5-270">As barreiras de divisão fornecem dicas para a GPU em que um recurso no estado *a* seguir será usado no estado *B* , em algum momento depois.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-270">Split barriers provide hints to the GPU that a resource in state *A* will next be used in state *B* sometime later.</span></span> <span data-ttu-id="1bbc5-271">Isso dá à GPU a opção de otimizar a carga de trabalho de transição, possivelmente reduzindo ou eliminando as vagas de execução.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-271">This gives the GPU the option to optimize the transition workload, possibly reducing or eliminating execution stalls.</span></span> <span data-ttu-id="1bbc5-272">A emissão da barreira somente final garante que todo o trabalho de transição da GPU seja concluído antes de passar para o próximo comando.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-272">Issuing the end-only barrier guarantees that all GPU transition work is finished before moving onto the next command.</span></span>

<span data-ttu-id="1bbc5-273">O uso de barreiras de divisão pode ajudar a melhorar o desempenho, especialmente em cenários de vários mecanismos ou em que os recursos de leitura/gravação são transferidos de modo disperso em uma ou mais listas de comandos.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-273">Using split barriers can help to improve performance, especially in multi-engine scenarios or where resources are read/write transitioned sparsely throughout one or more command lists.</span></span>

## <a name="resource-barrier-example-scenario"></a><span data-ttu-id="1bbc5-274">Cenário de exemplo de barreira de recurso</span><span class="sxs-lookup"><span data-stu-id="1bbc5-274">Resource barrier example scenario</span></span>

<span data-ttu-id="1bbc5-275">Os trechos de código a seguir mostram o uso do método [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) em um exemplo de multithreading.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-275">The following snippets show the use of the [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) method in a multi-threading sample.</span></span>

<span data-ttu-id="1bbc5-276">Criando a exibição de estêncil de profundidade, fazendo a transição para um estado gravável.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-276">Creating the depth stencil view, transitioning it to a writeable state.</span></span>


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



<span data-ttu-id="1bbc5-277">Criando a exibição de buffer de vértice, primeiro alterando-a de um Estado comum para um destino e, em seguida, de um destino para um estado genérico legível.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-277">Creating the vertex buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


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



<span data-ttu-id="1bbc5-278">Criando a exibição do buffer de índice, primeiro alterando-a de um Estado comum para um destino e, em seguida, de um destino para um estado genérico legível.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-278">Creating the index buffer view, first changing it from a common state to a destination, then from a destination to a generic readable state.</span></span>


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



<span data-ttu-id="1bbc5-279">Criando texturas e exibições de recursos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-279">Creating textures and shader resource views.</span></span> <span data-ttu-id="1bbc5-280">A textura é alterada de um Estado comum para um destino e, em seguida, de um destino para um recurso de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-280">The texture is changed from a common state to a destination, and then from a destination to a pixel shader resource.</span></span>


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



<span data-ttu-id="1bbc5-281">Iniciando um quadro; Isso não apenas usa [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) para indicar que o BackBuffer deve ser usado como um destino de renderização, mas também Inicializa o recurso de quadro (que chama **ResourceBarrier** no buffer de estêncil de profundidade).</span><span class="sxs-lookup"><span data-stu-id="1bbc5-281">Beginning a frame; this not only uses [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to indicate that the backbuffer is to be used as a render target, but also initializes the frame resource (which calls **ResourceBarrier** on the depth stencil buffer).</span></span>


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



<span data-ttu-id="1bbc5-282">Finalizar um quadro, indicando que o buffer de fundo agora é usado para apresentar.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-282">Ending a frame, indicating the back buffer is now used to present.</span></span>


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



<span data-ttu-id="1bbc5-283">Inicializar um recurso de quadro, chamado quando inicia um quadro, faz a transição do buffer de estêncil de profundidade para gravável.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-283">Initializing a frame resource, called when beginning a frame, transitions the depth stencil buffer to writeable.</span></span>


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



<span data-ttu-id="1bbc5-284">As barreiras são permutadas em meio período, fazendo a transição do mapa de sombra de gravável para legível.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-284">Barriers are swapped mid-frame, transitioning the shadow map from writeable to readable.</span></span>


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



<span data-ttu-id="1bbc5-285">O término é chamado quando um quadro é finalizado, fazendo a transição do mapa de sombra para um Estado comum.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-285">Finish is called when a frame is ended, transitioning the shadow map to a common state.</span></span>


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a><span data-ttu-id="1bbc5-286">Promoção de Estado comum e exemplo de decaimento</span><span class="sxs-lookup"><span data-stu-id="1bbc5-286">Common state promotion and decay sample</span></span>

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

## <a name="example-of-split-barriers"></a><span data-ttu-id="1bbc5-287">Exemplo de barreiras de divisão</span><span class="sxs-lookup"><span data-stu-id="1bbc5-287">Example of split barriers</span></span>

<span data-ttu-id="1bbc5-288">O exemplo a seguir mostra como usar uma barreira de divisão para reduzir as interrupções de pipeline.</span><span class="sxs-lookup"><span data-stu-id="1bbc5-288">The following example shows how to use a split barrier to reduce pipeline stalls.</span></span> <span data-ttu-id="1bbc5-289">O código a seguir não usa barreiras de divisão:</span><span class="sxs-lookup"><span data-stu-id="1bbc5-289">The code that follows does not use split barriers:</span></span>

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

<span data-ttu-id="1bbc5-290">O código a seguir usa barreiras de divisão:</span><span class="sxs-lookup"><span data-stu-id="1bbc5-290">The following code uses split barriers:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1bbc5-291">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bbc5-291">Related topics</span></span>

[<span data-ttu-id="1bbc5-292">Tutoriais de vídeo do DirectX Advanced Learning: barreiras de recursos e acompanhamento de estado</span><span class="sxs-lookup"><span data-stu-id="1bbc5-292">DirectX advanced learning video tutorials : Resource Barriers and State Tracking</span></span>](https://www.youtube.com/watch?v=nmB2XMasz2o)

[<span data-ttu-id="1bbc5-293">Sincronização de vários mecanismos</span><span class="sxs-lookup"><span data-stu-id="1bbc5-293">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)

[<span data-ttu-id="1bbc5-294">Envio de trabalho no Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1bbc5-294">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)

[<span data-ttu-id="1bbc5-295">Uma olhada nas barreiras do estado do recurso D3D12</span><span class="sxs-lookup"><span data-stu-id="1bbc5-295">A Look Inside D3D12 Resource State Barriers</span></span>](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

