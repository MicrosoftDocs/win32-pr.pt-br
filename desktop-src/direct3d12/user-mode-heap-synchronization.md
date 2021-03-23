---
title: Sincronização de vários mecanismos
description: Este tópico discute a sincronização de acesso a vários mecanismos independentes encontrados na maioria das GPUs modernas.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d60704e411a1ba45dd4902ad9101a416391743dd
ms.sourcegitcommit: 622d149edf775af5a9633c2d12ccfddf7000b8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/31/2020
ms.locfileid: "104548201"
---
# <a name="multi-engine-synchronization"></a><span data-ttu-id="c59a1-103">Sincronização de vários mecanismos</span><span class="sxs-lookup"><span data-stu-id="c59a1-103">Multi-engine synchronization</span></span>

<span data-ttu-id="c59a1-104">A maioria das GPUs modernas contém vários mecanismos independentes que fornecem funcionalidade especializada.</span><span class="sxs-lookup"><span data-stu-id="c59a1-104">Most modern GPUs contain multiple independent engines that provide specialized functionality.</span></span> <span data-ttu-id="c59a1-105">Muitos têm um ou mais mecanismos de cópia dedicados e um mecanismo de computação, geralmente distinto do mecanismo 3D.</span><span class="sxs-lookup"><span data-stu-id="c59a1-105">Many have one or more dedicated copy engines, and a compute engine, usually distinct from the 3D engine.</span></span> <span data-ttu-id="c59a1-106">Cada um desses mecanismos pode executar comandos em paralelo entre si.</span><span class="sxs-lookup"><span data-stu-id="c59a1-106">Each of these engines can execute commands in parallel with each other.</span></span> <span data-ttu-id="c59a1-107">O Direct3D 12 fornece acesso refinado aos mecanismos 3D, de computação e de cópia, usando filas e listas de comandos.</span><span class="sxs-lookup"><span data-stu-id="c59a1-107">Direct3D 12 provides fine-grained access to the 3D, compute, and copy engines, using queues and command lists.</span></span>

## <a name="gpu-engines"></a><span data-ttu-id="c59a1-108">Mecanismos de GPU</span><span class="sxs-lookup"><span data-stu-id="c59a1-108">GPU engines</span></span>

<span data-ttu-id="c59a1-109">O diagrama a seguir mostra os threads de CPU de um título, cada um deles populando uma ou mais das filas de cópia, computação e 3D.</span><span class="sxs-lookup"><span data-stu-id="c59a1-109">The following diagram shows a title's CPU threads, each populating one or more of the copy, compute, and 3D queues.</span></span> <span data-ttu-id="c59a1-110">A fila 3D pode impulsionar todos os três mecanismos de GPU; a fila de computação pode impulsionar os mecanismos de computação e cópia; e a fila de cópia simplesmente o mecanismo de cópia.</span><span class="sxs-lookup"><span data-stu-id="c59a1-110">The 3D queue can drive all three GPU engines; the compute queue can drive the compute and copy engines; and the copy queue simply the copy engine.</span></span>

<span data-ttu-id="c59a1-111">Como os diferentes threads preenchem as filas, não pode haver nenhuma garantia simples da ordem de execução, portanto, a necessidade de mecanismos de sincronização &mdash; quando o título os exige.</span><span class="sxs-lookup"><span data-stu-id="c59a1-111">As the different threads populate the queues, there can be no simple guarantee of the order of execution, hence the need for synchronization mechanisms&mdash;when the title requires them.</span></span>

![quatro threads enviando comandos para três filas](images/gpu-engines.png)

<span data-ttu-id="c59a1-113">A imagem a seguir ilustra como um título pode agendar o trabalho entre vários mecanismos de GPU, incluindo a sincronização entre mecanismos, quando necessário: ele mostra as cargas de trabalhos por mecanismo com dependências entre mecanismos.</span><span class="sxs-lookup"><span data-stu-id="c59a1-113">The following image illustrate how a title might schedule work across multiple GPU engines, including inter-engine synchronization where necessary: it shows the per-engine workloads with inter-engine dependencies.</span></span> <span data-ttu-id="c59a1-114">Neste exemplo, o mecanismo de cópia primeiro copia algumas geometrias necessárias para a renderização.</span><span class="sxs-lookup"><span data-stu-id="c59a1-114">In this example, the copy engine first copies some geometry necessary for rendering.</span></span> <span data-ttu-id="c59a1-115">O mecanismo 3D aguarda que essas cópias sejam concluídas e renderiza uma passada sobre a geometria.</span><span class="sxs-lookup"><span data-stu-id="c59a1-115">The 3D engine waits for these copies to complete, and renders a pre-pass over the geometry.</span></span> <span data-ttu-id="c59a1-116">Isso é então consumido pelo mecanismo de computação.</span><span class="sxs-lookup"><span data-stu-id="c59a1-116">This is then consumed by the compute engine.</span></span> <span data-ttu-id="c59a1-117">Os resultados da [**expedição**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)do mecanismo de computação, juntamente com várias operações de cópia de textura no mecanismo de cópia, são consumidos pelo mecanismo 3D para a chamada de [**desenho**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) final.</span><span class="sxs-lookup"><span data-stu-id="c59a1-117">The results of the compute engine [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch), along with several texture copy operations on the copy engine, are consumed by the 3D engine for the final [**Draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) call.</span></span>

![comunicação, gráficos e mecanismos de computação se comunicando](images/gpu-sync.png)

<span data-ttu-id="c59a1-119">O pseudocódigo a seguir ilustra como um título pode enviar tal carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c59a1-119">The following pseudo-code illustrates how a title might submit such a workload.</span></span>

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

<span data-ttu-id="c59a1-120">O pseudocódigo a seguir ilustra a sincronização entre a cópia e os mecanismos 3D para realizar a alocação de memória semelhante a heap por meio de um buffer de anéis.</span><span class="sxs-lookup"><span data-stu-id="c59a1-120">The following pseudo-code illustrates synchronization between the copy and 3D engines to accomplish heap-like memory allocation via a ring buffer.</span></span> <span data-ttu-id="c59a1-121">Os títulos têm a flexibilidade de escolher o equilíbrio certo entre maximizar o paralelismo (por meio de um buffer grande) e reduzir o consumo de memória e a latência (por meio de um buffer pequeno).</span><span class="sxs-lookup"><span data-stu-id="c59a1-121">Titles have the flexibility to choose the right balance between maximizing parallelism (via a large buffer) and reducing memory consumption and latency (via a small buffer).</span></span>

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a><span data-ttu-id="c59a1-122">Cenários de vários mecanismos</span><span class="sxs-lookup"><span data-stu-id="c59a1-122">Multi-engine scenarios</span></span>

<span data-ttu-id="c59a1-123">O Direct3D 12 permite que você evite a execução acidental em ineficiências causadas por atrasos de sincronização inesperados.</span><span class="sxs-lookup"><span data-stu-id="c59a1-123">Direct3D 12 allows you to avoid accidentally running into inefficiencies caused by unexpected synchronization delays.</span></span> <span data-ttu-id="c59a1-124">Ele também permite que você introduza a sincronização em um nível mais alto em que a sincronização necessária pode ser determinada com maior certeza.</span><span class="sxs-lookup"><span data-stu-id="c59a1-124">It also allows you to introduce synchronization at a higher level where the required synchronization can be determined with greater certainty.</span></span> <span data-ttu-id="c59a1-125">Um segundo problema que os endereços de vários mecanismos é tornar as operações caras mais explícitas, o que inclui transições entre 3D e vídeo tradicionalmente dispendioso devido à sincronização entre vários contextos de kernel.</span><span class="sxs-lookup"><span data-stu-id="c59a1-125">A second issue that multi-engine addresses is to make expensive operations more explicit, which includes transitions between 3D and video that were traditionally costly because of synchronization between multiple kernel contexts.</span></span>

<span data-ttu-id="c59a1-126">Em particular, os cenários a seguir podem ser abordados com o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="c59a1-126">In particular, the following scenarios can be addressed with Direct3D 12.</span></span>

-   <span data-ttu-id="c59a1-127">Trabalho de GPU de baixa prioridade e assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c59a1-127">Asynchronous and low priority GPU work.</span></span> <span data-ttu-id="c59a1-128">Isso permite a execução simultânea de trabalho de GPU de baixa prioridade e operações atômicas que permitem que um thread de GPU consuma os resultados de outro thread não sincronizado sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c59a1-128">This enables concurrent execution of low priority GPU work and atomic operations that enable one GPU thread to consume the results of another unsynchronized thread without blocking.</span></span>
-   <span data-ttu-id="c59a1-129">Trabalho de computação de alta prioridade.</span><span class="sxs-lookup"><span data-stu-id="c59a1-129">High priority compute work.</span></span> <span data-ttu-id="c59a1-130">Com a computação em segundo plano, é possível interromper a renderização 3D para fazer uma pequena quantidade de trabalho de computação de alta prioridade.</span><span class="sxs-lookup"><span data-stu-id="c59a1-130">With background compute it is possible to interrupt 3D rendering to do a small amount of high priority compute work.</span></span> <span data-ttu-id="c59a1-131">Os resultados desse trabalho podem ser obtidos antecipadamente para processamento adicional na CPU.</span><span class="sxs-lookup"><span data-stu-id="c59a1-131">The results of this work can be obtained early for additional processing on the CPU.</span></span>
-   <span data-ttu-id="c59a1-132">Trabalho de computação em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="c59a1-132">Background compute work.</span></span> <span data-ttu-id="c59a1-133">Uma fila de baixa prioridade separada para cargas de trabalho de computação permite que um aplicativo utilize ciclos de GPU sobressalentes para executar a computação em segundo plano sem impacto negativo nas tarefas de renderização primária (ou outras).</span><span class="sxs-lookup"><span data-stu-id="c59a1-133">A separate low priority queue for compute workloads allows an application to utilize spare GPU cycles to perform background computation without negative impact on the primary rendering (or other) tasks.</span></span> <span data-ttu-id="c59a1-134">As tarefas em segundo plano podem incluir descompactação de recursos ou atualização de simulações ou estruturas de aceleração.</span><span class="sxs-lookup"><span data-stu-id="c59a1-134">Background tasks may include decompression of resources or updating simulations or acceleration structures.</span></span> <span data-ttu-id="c59a1-135">As tarefas em segundo plano devem ser sincronizadas na CPU com pouca frequência (aproximadamente uma vez por quadro) para evitar interrupções ou lentidão no trabalho em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="c59a1-135">Background tasks should be synchronized on the CPU infrequently (approximately once per frame) to avoid stalling or slowing foreground work.</span></span>
-   <span data-ttu-id="c59a1-136">Streaming e carregamento de dados.</span><span class="sxs-lookup"><span data-stu-id="c59a1-136">Streaming and uploading data.</span></span> <span data-ttu-id="c59a1-137">Uma fila de cópia separada substitui os conceitos de D3D11 dos dados iniciais e os recursos de atualização.</span><span class="sxs-lookup"><span data-stu-id="c59a1-137">A separate copy queue replaces the D3D11 concepts of initial data and updating resources.</span></span> <span data-ttu-id="c59a1-138">Embora o aplicativo seja responsável por mais detalhes no modelo do Direct3D 12, essa responsabilidade vem com energia.</span><span class="sxs-lookup"><span data-stu-id="c59a1-138">Although the application is responsible for more details in the Direct3D 12 model, this responsibility comes with power.</span></span> <span data-ttu-id="c59a1-139">O aplicativo pode controlar a quantidade de memória do sistema dedicada ao armazenamento de dados de upload.</span><span class="sxs-lookup"><span data-stu-id="c59a1-139">The application can control how much system memory is devoted to buffering upload data.</span></span> <span data-ttu-id="c59a1-140">O aplicativo pode escolher quando e como (CPU vs GPU, bloquear vs. sem bloqueio) sincronizar e controlar o progresso e controlar a quantidade de trabalho na fila.</span><span class="sxs-lookup"><span data-stu-id="c59a1-140">The app can choose when and how (CPU vs GPU, blocking vs non-blocking) to synchronize, and can track progress and control the amount of queued work.</span></span>
-   <span data-ttu-id="c59a1-141">Maior paralelismo.</span><span class="sxs-lookup"><span data-stu-id="c59a1-141">Increased parallelism.</span></span> <span data-ttu-id="c59a1-142">Os aplicativos podem usar filas mais profundas para cargas de trabalho em segundo plano (por exemplo, decodificação de vídeo) quando têm filas separadas para trabalhos em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="c59a1-142">Applications can use deeper queues for background workloads (e.g. video decode) when they have separate queues for foreground work.</span></span>

<span data-ttu-id="c59a1-143">No Direct3D 12, o conceito de uma fila de comandos é a representação de API de uma sequência de trabalho aproximadamente serial enviada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c59a1-143">In Direct3D 12 the concept of a command queue is the API representation of a roughly serial sequence of work submitted by the application.</span></span> <span data-ttu-id="c59a1-144">As barreiras e outras técnicas permitem que esse trabalho seja executado em um pipeline ou fora de ordem, mas o aplicativo vê apenas uma linha do tempo de conclusão única.</span><span class="sxs-lookup"><span data-stu-id="c59a1-144">Barriers and other techniques allow this work to be executed in a pipeline or out of order, but the application only sees a single completion timeline.</span></span> <span data-ttu-id="c59a1-145">Isso corresponde ao contexto imediato no D3D11.</span><span class="sxs-lookup"><span data-stu-id="c59a1-145">This corresponds to the immediate context in D3D11.</span></span>

## <a name="synchronization-apis"></a><span data-ttu-id="c59a1-146">APIs de sincronização</span><span class="sxs-lookup"><span data-stu-id="c59a1-146">Synchronization APIs</span></span>

### <a name="devices-and-queues"></a><span data-ttu-id="c59a1-147">Dispositivos e filas</span><span class="sxs-lookup"><span data-stu-id="c59a1-147">Devices and queues</span></span>

<span data-ttu-id="c59a1-148">O dispositivo Direct3D 12 tem métodos para criar e recuperar filas de comandos de diferentes tipos e prioridades.</span><span class="sxs-lookup"><span data-stu-id="c59a1-148">The Direct3D 12 device has methods to create and retrieve command queues of different types and priorities.</span></span> <span data-ttu-id="c59a1-149">A maioria dos aplicativos deve usar as filas de comando padrão, pois elas permitem o uso compartilhado por outros componentes.</span><span class="sxs-lookup"><span data-stu-id="c59a1-149">Most applications should use the default command queues because these allow for shared usage by other components.</span></span> <span data-ttu-id="c59a1-150">Aplicativos com requisitos de simultaneidade adicionais podem criar filas adicionais.</span><span class="sxs-lookup"><span data-stu-id="c59a1-150">Applications with additional concurrency requirements can create additional queues.</span></span> <span data-ttu-id="c59a1-151">As filas são especificadas pelo tipo de lista de comandos que elas consomem.</span><span class="sxs-lookup"><span data-stu-id="c59a1-151">Queues are specified by the command list type that they consume.</span></span>

<span data-ttu-id="c59a1-152">Consulte os métodos de criação a seguir de [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="c59a1-152">Refer to the following creation methods of [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span></span>

-   <span data-ttu-id="c59a1-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : cria uma fila de comando com base em informações em uma estrutura [**desc de fila de comando do Direct3D 12 \_ \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .</span><span class="sxs-lookup"><span data-stu-id="c59a1-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : creates a command queue based on information in a [**Direct3D 12\_COMMAND\_QUEUE\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) structure.</span></span>
-   <span data-ttu-id="c59a1-154">[**Createcommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : cria uma lista de comandos do tipo [**tipo de \_ \_ lista \_ de comandos do Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span><span class="sxs-lookup"><span data-stu-id="c59a1-154">[**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : creates a command list of type [**Direct3D 12\_COMMAND\_LIST\_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>
-   <span data-ttu-id="c59a1-155">[**Createfence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : cria uma cerca, observando os sinalizadores nos [**sinalizadores de \_ cerca do \_ Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span><span class="sxs-lookup"><span data-stu-id="c59a1-155">[**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : creates a fence, noting the flags in [**Direct3D 12\_FENCE\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span></span> <span data-ttu-id="c59a1-156">Os limites são usados para sincronizar filas.</span><span class="sxs-lookup"><span data-stu-id="c59a1-156">Fences are used to synchronize queues.</span></span>

<span data-ttu-id="c59a1-157">Filas de todos os tipos (3D, computação e cópia) compartilham a mesma interface e são todas baseadas na lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="c59a1-157">Queues of all types (3D, compute and copy) share the same interface and are all command-list based.</span></span>

<span data-ttu-id="c59a1-158">Consulte os seguintes métodos de [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span><span class="sxs-lookup"><span data-stu-id="c59a1-158">Refer to the following methods of [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span></span>

-   <span data-ttu-id="c59a1-159">[**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : envia uma matriz de listas de comandos para execução.</span><span class="sxs-lookup"><span data-stu-id="c59a1-159">[**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : submits an array of command lists for execution.</span></span> <span data-ttu-id="c59a1-160">Cada lista de comandos está sendo definida por [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span><span class="sxs-lookup"><span data-stu-id="c59a1-160">Each command list being defined by [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>
-   <span data-ttu-id="c59a1-161">[**Sinal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : define um valor de limite quando a fila (em execução na GPU) atinge um determinado ponto.</span><span class="sxs-lookup"><span data-stu-id="c59a1-161">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : sets a fence value when the queue (running on the GPU) reaches a certain point.</span></span>
-   <span data-ttu-id="c59a1-162">[**Aguardar**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : a fila aguarda até que a cerca especificada atinja o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c59a1-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : the queue waits until the specified fence reaches the specified value.</span></span>

<span data-ttu-id="c59a1-163">Observe que os grupos não são consumidos por nenhuma fila e, portanto, esse tipo não pode ser usado para criar uma fila.</span><span class="sxs-lookup"><span data-stu-id="c59a1-163">Note that bundles are not consumed by any queues and therefore this type cannot be used to create a queue.</span></span>

### <a name="fences"></a><span data-ttu-id="c59a1-164">Limites</span><span class="sxs-lookup"><span data-stu-id="c59a1-164">Fences</span></span>

<span data-ttu-id="c59a1-165">A API de vários mecanismos fornece APIs explícitas para criar e sincronizar usando limites.</span><span class="sxs-lookup"><span data-stu-id="c59a1-165">The multi-engine API provides explicit APIs to create and synchronize using fences.</span></span> <span data-ttu-id="c59a1-166">Um limite é uma construção de sincronização controlada por um valor UINT64.</span><span class="sxs-lookup"><span data-stu-id="c59a1-166">A fence is a synchronization construct controlled by a UINT64 value.</span></span> <span data-ttu-id="c59a1-167">Os valores de limite são definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c59a1-167">Fence values are set by the application.</span></span> <span data-ttu-id="c59a1-168">Uma operação de sinal modifica o valor de limite e uma operação de espera até que a cerca tenha atingido o valor solicitado ou maior.</span><span class="sxs-lookup"><span data-stu-id="c59a1-168">A signal operation modifies the fence value and a wait operation blocks until the fence has reached the requested value or greater.</span></span> <span data-ttu-id="c59a1-169">Um evento pode ser acionado quando uma cerca atinge um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="c59a1-169">An event can be fired when a fence reaches a certain value.</span></span>

<span data-ttu-id="c59a1-170">Consulte os métodos da interface [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) .</span><span class="sxs-lookup"><span data-stu-id="c59a1-170">Refer to the methods of the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface.</span></span>

-   <span data-ttu-id="c59a1-171">[**Getcompletedvalue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : retorna o valor atual da cerca.</span><span class="sxs-lookup"><span data-stu-id="c59a1-171">[**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : returns the current value of the fence.</span></span>
-   <span data-ttu-id="c59a1-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : faz com que um evento seja acionado quando a cerca atinge um determinado valor.</span><span class="sxs-lookup"><span data-stu-id="c59a1-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : causes an event to fire when the fence reaches a given value.</span></span>
-   <span data-ttu-id="c59a1-173">[**Sinal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : define a cerca para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="c59a1-173">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : sets the fence to the given value.</span></span>

<span data-ttu-id="c59a1-174">Os limites permitem acesso de CPU ao valor de limite atual e esperas e sinais de CPU.</span><span class="sxs-lookup"><span data-stu-id="c59a1-174">Fences allow CPU access to the current fence value, and CPU waits and signals.</span></span>

<span data-ttu-id="c59a1-175">O método [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) na interface [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) atualiza um limite do lado da CPU.</span><span class="sxs-lookup"><span data-stu-id="c59a1-175">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) method on the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface updates a fence from the CPU side.</span></span> <span data-ttu-id="c59a1-176">Essa atualização ocorre imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c59a1-176">This update occurs immediately.</span></span> <span data-ttu-id="c59a1-177">O método [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) em [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) atualiza um limite do lado da GPU.</span><span class="sxs-lookup"><span data-stu-id="c59a1-177">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) method on [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) updates a fence from the GPU side.</span></span> <span data-ttu-id="c59a1-178">Essa atualização ocorre depois que todas as outras operações na fila de comandos tiverem sido concluídas.</span><span class="sxs-lookup"><span data-stu-id="c59a1-178">This update occurs after all other operations on the command queue have been completed.</span></span>

<span data-ttu-id="c59a1-179">Todos os nós em uma instalação de vários mecanismos podem ler e reagir a qualquer limite que atinja o valor correto.</span><span class="sxs-lookup"><span data-stu-id="c59a1-179">All nodes in a multi-engine setup can read and react to any fence reaching the right value.</span></span>

<span data-ttu-id="c59a1-180">Os aplicativos definem seus próprios valores de limite, um bom ponto de partida pode estar aumentando um limite uma vez por quadro.</span><span class="sxs-lookup"><span data-stu-id="c59a1-180">Applications set their own fence values, a good starting point might be increasing a fence once per frame.</span></span>

<span data-ttu-id="c59a1-181">Um limite *pode* ser *rebobinado*.</span><span class="sxs-lookup"><span data-stu-id="c59a1-181">A fence *may* be *rewound*.</span></span> <span data-ttu-id="c59a1-182">Isso significa que o valor de isolamento não precisa ser incrementado exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="c59a1-182">This means that the fence value does not need to solely increment.</span></span> <span data-ttu-id="c59a1-183">Se uma operação de **sinal** for enfileirada em duas filas de comandos diferentes ou se dois threads de CPU estiverem chamando o **sinal** em uma cerca, poderá haver uma corrida para determinar qual **sinal** é concluído por último e, portanto, qual valor de limite é aquele que permanecerá.</span><span class="sxs-lookup"><span data-stu-id="c59a1-183">If a **Signal** operation is enqueued on two different command queues, or if two CPU threads are both calling **Signal** on a fence, there may be a race to determine which **Signal** completes last, and therefore which fence value is the one which will remain.</span></span> <span data-ttu-id="c59a1-184">Se uma cerca for rebobinada, quaisquer novas esperas (incluindo solicitações **SetEventOnCompletion** ) serão comparadas com o novo valor de limite inferior e, portanto, talvez não sejam satisfeitas, mesmo se o valor de limite tiver sido alto o suficiente para atender a elas.</span><span class="sxs-lookup"><span data-stu-id="c59a1-184">If a fence is rewound, any new waits (including **SetEventOnCompletion** requests) will be compared against the new lower fence value, and therefore may not be satisfied, even if the fence value had previously been high enough to satisfy them.</span></span> <span data-ttu-id="c59a1-185">Se ocorrer uma corrida, entre um valor que atenderá a uma espera pendente e um valor mais baixo que não será, a espera *será* satisfeita, independentemente de qual valor permanecer depois.</span><span class="sxs-lookup"><span data-stu-id="c59a1-185">If a race does occur, between a value which will satisfy an outstanding wait, and a lower value which will not, the wait *will* be satisfied regardless of which value remains afterwards.</span></span>

<span data-ttu-id="c59a1-186">As APIs de isolamento fornecem uma funcionalidade de sincronização poderosa, mas podem criar problemas potencialmente difíceis de depurar.</span><span class="sxs-lookup"><span data-stu-id="c59a1-186">The fence APIs provide powerful synchronization functionality but can create potentially difficult to debug issues.</span></span> <span data-ttu-id="c59a1-187">É recomendável que cada cerca seja usada apenas para indicar o progresso em uma linha do tempo para evitar corridas entre os signalrs.</span><span class="sxs-lookup"><span data-stu-id="c59a1-187">It is recommended that each fence only be used to indicate progress on one timeline to prevent races between signalers.</span></span>

### <a name="copy-and-compute-command-lists"></a><span data-ttu-id="c59a1-188">Listas de comandos copiar e computar</span><span class="sxs-lookup"><span data-stu-id="c59a1-188">Copy and compute command lists</span></span>

<span data-ttu-id="c59a1-189">Todos os três tipos de lista de comandos usam a interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ; no entanto, apenas um subconjunto dos métodos tem suporte para cópia e computação.</span><span class="sxs-lookup"><span data-stu-id="c59a1-189">All three types of command list use the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface, however only a subset of the methods are supported for copy and compute.</span></span>

<span data-ttu-id="c59a1-190">As listas de comandos Copy e Compute podem usar os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c59a1-190">Copy and compute command lists can use the following methods.</span></span>

-   [<span data-ttu-id="c59a1-191">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="c59a1-191">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [<span data-ttu-id="c59a1-192">**CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="c59a1-192">**CopyBufferRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="c59a1-193">**CopyResource**</span><span class="sxs-lookup"><span data-stu-id="c59a1-193">**CopyResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="c59a1-194">**CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="c59a1-194">**CopyTextureRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="c59a1-195">**CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="c59a1-195">**CopyTiles**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="c59a1-196">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="c59a1-196">**Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [<span data-ttu-id="c59a1-197">**ResourceBarrier**</span><span class="sxs-lookup"><span data-stu-id="c59a1-197">**ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

<span data-ttu-id="c59a1-198">As listas de comandos de computação também podem usar os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c59a1-198">Compute command lists can also use the following methods.</span></span>

-   [<span data-ttu-id="c59a1-199">**Clearstate**</span><span class="sxs-lookup"><span data-stu-id="c59a1-199">**ClearState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [<span data-ttu-id="c59a1-200">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="c59a1-200">**ClearUnorderedAccessViewFloat**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="c59a1-201">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="c59a1-201">**ClearUnorderedAccessViewUint**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="c59a1-202">**DiscardResource**</span><span class="sxs-lookup"><span data-stu-id="c59a1-202">**DiscardResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [<span data-ttu-id="c59a1-203">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="c59a1-203">**Dispatch**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="c59a1-204">**ExecuteIndirect**</span><span class="sxs-lookup"><span data-stu-id="c59a1-204">**ExecuteIndirect**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [<span data-ttu-id="c59a1-205">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="c59a1-205">**SetComputeRoot32BitConstant**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="c59a1-206">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="c59a1-206">**SetComputeRoot32BitConstants**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [<span data-ttu-id="c59a1-207">**SetComputeRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="c59a1-207">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="c59a1-208">**SetComputeRootDescriptorTable**</span><span class="sxs-lookup"><span data-stu-id="c59a1-208">**SetComputeRootDescriptorTable**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [<span data-ttu-id="c59a1-209">**SetComputeRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="c59a1-209">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="c59a1-210">**SetComputeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="c59a1-210">**SetComputeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [<span data-ttu-id="c59a1-211">**SetComputeRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="c59a1-211">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="c59a1-212">**SetDescriptorHeaps**</span><span class="sxs-lookup"><span data-stu-id="c59a1-212">**SetDescriptorHeaps**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [<span data-ttu-id="c59a1-213">**Setpipelinestate**</span><span class="sxs-lookup"><span data-stu-id="c59a1-213">**SetPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [<span data-ttu-id="c59a1-214">**SetPredication**</span><span class="sxs-lookup"><span data-stu-id="c59a1-214">**SetPredication**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

<span data-ttu-id="c59a1-215">As listas de comandos de computação devem definir um PSO de computação ao chamar [**Setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span><span class="sxs-lookup"><span data-stu-id="c59a1-215">Compute command lists must set a compute PSO when calling [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span></span>

<span data-ttu-id="c59a1-216">Os grupos não podem ser usados com listas de comandos ou filas de computação ou cópia.</span><span class="sxs-lookup"><span data-stu-id="c59a1-216">Bundles cannot be used with compute or copy command lists or queues.</span></span>

## <a name="pipelined-compute-and-graphics-example"></a><span data-ttu-id="c59a1-217">Exemplo de computação e gráficos em pipeline</span><span class="sxs-lookup"><span data-stu-id="c59a1-217">Pipelined compute and graphics example</span></span>

<span data-ttu-id="c59a1-218">Este exemplo mostra como a sincronização de isolamento pode ser usada para criar um pipeline de trabalho de computação em uma fila (referenciada por `pComputeQueue` ) que é consumida por gráficos funcionam na fila `pGraphicsQueue` .</span><span class="sxs-lookup"><span data-stu-id="c59a1-218">This example shows how fence synchronization can be used to create a pipeline of compute work on a queue (referenced by `pComputeQueue`) that's consumed by graphics work on queue `pGraphicsQueue`.</span></span> <span data-ttu-id="c59a1-219">O trabalho de computação e gráficos é canalizado com a fila de gráficos que consome o resultado do trabalho de computação de vários quadros de volta e um evento de CPU é usado para limitar o total de trabalhos na fila geral.</span><span class="sxs-lookup"><span data-stu-id="c59a1-219">The compute and graphics work is pipelined with the graphics queue consuming the result of compute work from several frames back, and a CPU event is used to throttle the total work queued overall.</span></span>

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

<span data-ttu-id="c59a1-220">Para dar suporte a esse pipeline, deve haver um buffer de `ComputeGraphicsLatency+1` cópias diferentes dos dados que passam da fila de computação para a fila de gráficos.</span><span class="sxs-lookup"><span data-stu-id="c59a1-220">To support this pipelining, there must be a buffer of `ComputeGraphicsLatency+1` different copies of the data passing from the compute queue to the graphics queue.</span></span> <span data-ttu-id="c59a1-221">As listas de comandos devem usar UAVs e indireção para ler e gravar a partir da "versão" apropriada dos dados no buffer.</span><span class="sxs-lookup"><span data-stu-id="c59a1-221">The command lists must use UAVs and indirection to read and write from the appropriate “version” of the data in the buffer.</span></span> <span data-ttu-id="c59a1-222">A fila de computação deve aguardar até que a fila de gráficos termine de ler os dados do quadro N antes que ele possa gravar o quadro `N+ComputeGraphicsLatency` .</span><span class="sxs-lookup"><span data-stu-id="c59a1-222">The compute queue must wait until the graphics queue has finished reading from the data for frame N before it can write frame `N+ComputeGraphicsLatency`.</span></span>

<span data-ttu-id="c59a1-223">Observe que a quantidade de filas de computação trabalhadas em relação à CPU não depende diretamente da quantidade de buffer necessária, no entanto, o trabalho da GPU de enfileiramento além da quantidade de espaço disponível no buffer é menos valioso.</span><span class="sxs-lookup"><span data-stu-id="c59a1-223">Note that the amount of compute queue worked relative to the CPU does not depend directly on the amount of buffering required, however, queuing GPU work beyond the amount of buffer space available is less valuable.</span></span>

<span data-ttu-id="c59a1-224">Um mecanismo alternativo para evitar o indireção seria criar várias listas de comandos correspondentes a cada uma das versões "renomeadas" dos dados.</span><span class="sxs-lookup"><span data-stu-id="c59a1-224">An alternative mechanism to avoid indirection would be to create multiple command lists corresponding to each of the “renamed” versions of the data.</span></span> <span data-ttu-id="c59a1-225">O exemplo a seguir usa essa técnica enquanto estende o exemplo anterior para permitir que as filas de computação e gráficos sejam executadas de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c59a1-225">The next example uses this technique while extending the previous example to allow the compute and graphics queues to run more asynchronously.</span></span>

## <a name="asynchronous-compute-and-graphics-example"></a><span data-ttu-id="c59a1-226">Exemplo de computação assíncrona e gráficos</span><span class="sxs-lookup"><span data-stu-id="c59a1-226">Asynchronous compute and graphics example</span></span>

<span data-ttu-id="c59a1-227">Este exemplo a seguir permite que os gráficos sejam renderizados de forma assíncrona da fila de computação.</span><span class="sxs-lookup"><span data-stu-id="c59a1-227">This next example allows graphics to render asynchronously from the compute queue.</span></span> <span data-ttu-id="c59a1-228">Ainda há uma quantidade fixa de dados armazenados em buffer entre os dois estágios; no entanto, agora o trabalho gráfico funciona de forma independente e usa o resultado mais atualizado do estágio de computação como conhecido na CPU quando o trabalho de gráficos é colocado na fila.</span><span class="sxs-lookup"><span data-stu-id="c59a1-228">There is still a fixed amount of buffered data between the two stages, however now graphics work proceeds independently and uses the most up-to-date result of the compute stage as known on the CPU when the graphics work is queued.</span></span> <span data-ttu-id="c59a1-229">Isso seria útil se o trabalho de gráficos estivesse sendo atualizado por outra fonte, por exemplo, entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="c59a1-229">This would be useful if the graphics work was being updated by another source, for example user input.</span></span> <span data-ttu-id="c59a1-230">Deve haver várias listas de comandos para permitir que os `ComputeGraphicsLatency` quadros de trabalho de gráficos estejam em trânsito por vez e a função `UpdateGraphicsCommandList` represente a atualização da lista de comandos para incluir os dados de entrada mais recentes e ler os dados de computação do buffer apropriado.</span><span class="sxs-lookup"><span data-stu-id="c59a1-230">There must be multiple command lists to allow the `ComputeGraphicsLatency` frames of graphics work to be in flight at a time, and the function `UpdateGraphicsCommandList` represents updating the command list to include the most recent input data and read from the compute data from the appropriate buffer.</span></span>

<span data-ttu-id="c59a1-231">A fila de computação ainda deve aguardar a conclusão da fila de gráficos com os buffers de pipe, mas uma terceira cerca ( `pGraphicsComputeFence` ) é introduzida para que o progresso dos gráficos de leitura do trabalho de computação versus o progresso de gráficos em geral possa ser acompanhado.</span><span class="sxs-lookup"><span data-stu-id="c59a1-231">The compute queue must still wait for the graphics queue to finish with the pipe buffers, but a third fence (`pGraphicsComputeFence`) is introduced so that the progress of graphics reading compute work versus graphics progress in general can be tracked.</span></span> <span data-ttu-id="c59a1-232">Isso reflete o fato de que agora quadros gráficos consecutivos podiam ler do mesmo resultado de computação ou podem ignorar um resultado de computação.</span><span class="sxs-lookup"><span data-stu-id="c59a1-232">This reflects the fact that now consecutive graphics frames could read from the same compute result or could skip a compute result.</span></span> <span data-ttu-id="c59a1-233">Um design mais eficiente, mas ligeiramente mais complicado, usaria apenas a única cerca de gráficos e armazenaria um mapeamento para os quadros de computação usados por cada quadro de gráficos.</span><span class="sxs-lookup"><span data-stu-id="c59a1-233">A more efficient but slightly more complicated design would use just the single graphics fence and store a mapping to the compute frames used by each graphics frame.</span></span>

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a><span data-ttu-id="c59a1-234">Acesso a recursos de várias filas</span><span class="sxs-lookup"><span data-stu-id="c59a1-234">Multi-queue resource access</span></span>

<span data-ttu-id="c59a1-235">Para acessar um recurso em mais de uma fila, um aplicativo deve aderir às regras a seguir.</span><span class="sxs-lookup"><span data-stu-id="c59a1-235">To access a resource on more than one queue an application must adhere to the following rules.</span></span>

-   <span data-ttu-id="c59a1-236">O acesso aos recursos (consulte os [**\_ \_ Estados de recursos do Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) é determinado pelo objeto classe tipo fila não fila.</span><span class="sxs-lookup"><span data-stu-id="c59a1-236">Resource access (refer to [**Direct3D 12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) is determined by queue type class not queue object.</span></span> <span data-ttu-id="c59a1-237">Há duas classes de tipo de fila: a fila de computação/3D é de uma classe de tipo, a cópia é uma segunda classe de tipo.</span><span class="sxs-lookup"><span data-stu-id="c59a1-237">There are two type classes of queue: Compute/3D queue is one type class, Copy is a second type class.</span></span> <span data-ttu-id="c59a1-238">Portanto, um recurso que tem uma barreira para o \_ \_ estado do recurso de sombreador não pixel \_ em uma fila 3D pode ser usado nesse estado em qualquer fila 3D ou de computação, sujeito aos requisitos de sincronização que exigem a serialização da maioria das gravações.</span><span class="sxs-lookup"><span data-stu-id="c59a1-238">So a resource that has a barrier to the NON\_PIXEL\_SHADER\_RESOURCE state on one 3D queue can be used in that state on any 3D or Compute queue, subject to synchronization requirements which require most writes to be serialized.</span></span> <span data-ttu-id="c59a1-239">Os Estados de recursos que são compartilhados entre as duas classes de tipo ( \_ origem de cópia e destino de cópia \_ ) são considerados Estados diferentes para cada classe de tipo.</span><span class="sxs-lookup"><span data-stu-id="c59a1-239">The resource states that are shared between the two type classes (COPY\_SOURCE and COPY\_DEST) are considered different states for each type class.</span></span> <span data-ttu-id="c59a1-240">Portanto, se um recurso fizer a transição para o dest de cópia \_ em uma fila de cópia, ele não poderá ser acessado como um destino de cópia de filas 3D ou de computação e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="c59a1-240">So that if a resource transitions to COPY\_DEST on a Copy queue it is not accessible as a copy destination from 3D or Compute queues and vice versa.</span></span>

    <span data-ttu-id="c59a1-241">Para resumir.</span><span class="sxs-lookup"><span data-stu-id="c59a1-241">To summarize.</span></span>

    -   <span data-ttu-id="c59a1-242">Uma fila "Object" é qualquer fila única.</span><span class="sxs-lookup"><span data-stu-id="c59a1-242">A queue "object" is any single queue.</span></span>
    -   <span data-ttu-id="c59a1-243">Uma fila "tipo" é qualquer uma destas três: Compute, 3D e Copy.</span><span class="sxs-lookup"><span data-stu-id="c59a1-243">A queue "type" is any one of these three: Compute, 3D, and Copy.</span></span>
    -   <span data-ttu-id="c59a1-244">Uma fila "tipo classe" é qualquer uma destas duas: Compute/3D e Copy.</span><span class="sxs-lookup"><span data-stu-id="c59a1-244">A queue "type class" is any one of these two: Compute/3D and Copy.</span></span>

-   <span data-ttu-id="c59a1-245">Os sinalizadores de cópia ( \_ destino de cópia e \_ origem da cópia) usados como Estados iniciais representam Estados na classe do tipo 3D/computação.</span><span class="sxs-lookup"><span data-stu-id="c59a1-245">The COPY flags (COPY\_DEST and COPY\_SOURCE) used as initial states represent states in the 3D/Compute type class.</span></span> <span data-ttu-id="c59a1-246">Para usar um recurso inicialmente em uma fila de cópia, ele deve iniciar no estado comum.</span><span class="sxs-lookup"><span data-stu-id="c59a1-246">To use a resource initially on a Copy queue it should start in the COMMON state.</span></span> <span data-ttu-id="c59a1-247">O estado comum pode ser usado para todos os usos em uma fila de cópia usando as transições de estado implícitas.</span><span class="sxs-lookup"><span data-stu-id="c59a1-247">The COMMON state can be used for all usages on a Copy queue using the implicit state transitions.</span></span> 
-   <span data-ttu-id="c59a1-248">Embora o estado do recurso seja compartilhado entre todas as filas de computação e 3D, não é permitido gravar no recurso simultaneamente em filas diferentes.</span><span class="sxs-lookup"><span data-stu-id="c59a1-248">Although resource state is shared across all Compute and 3D queues, it is not permitted to write to the resource simultaneously on different queues.</span></span> <span data-ttu-id="c59a1-249">"Simultaneamente" aqui significa não sincronizado, não é possível observar a execução não sincronizada em alguns hardwares.</span><span class="sxs-lookup"><span data-stu-id="c59a1-249">"Simultaneously" here means unsynchronized, noting unsynchronized execution is not possible on some hardware.</span></span> <span data-ttu-id="c59a1-250">As regras a seguir se aplicam.</span><span class="sxs-lookup"><span data-stu-id="c59a1-250">The following rules apply.</span></span>

    -   <span data-ttu-id="c59a1-251">Apenas uma fila pode gravar em um recurso por vez.</span><span class="sxs-lookup"><span data-stu-id="c59a1-251">Only one queue can write to a resource at a time.</span></span>
    -   <span data-ttu-id="c59a1-252">Várias filas podem ler do recurso contanto que eles não leiam os bytes que estão sendo modificados pelo gravador (os bytes de leitura que estão sendo gravados simultaneamente produzem resultados indefinidos).</span><span class="sxs-lookup"><span data-stu-id="c59a1-252">Multiple queues can read from the resource as long as they don’t read the bytes being modified by the writer (reading bytes being simultaneously written produces undefined results).</span></span>
    -   <span data-ttu-id="c59a1-253">Um limite deve ser usado para sincronizar após a gravação antes que outra fila possa ler os bytes gravados ou fazer qualquer acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="c59a1-253">A fence must be used to synchronize after writing before another queue can read the written bytes or make any write access.</span></span>

-   <span data-ttu-id="c59a1-254">Os buffers de fundo que estão sendo apresentados devem estar \_ no \_ estado comum do estado do recurso do Direct3D 12 \_ .</span><span class="sxs-lookup"><span data-stu-id="c59a1-254">Back buffers being presented must be in the Direct3D 12\_RESOURCE\_STATE\_COMMON state.</span></span> 

## <a name="related-topics"></a><span data-ttu-id="c59a1-255">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c59a1-255">Related topics</span></span>

[<span data-ttu-id="c59a1-256">Guia de programação do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c59a1-256">Direct3D 12 programming guide</span></span>](directx-12-programming-guide.md)

[<span data-ttu-id="c59a1-257">Usando barreiras de recursos para sincronizar Estados de recursos no Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c59a1-257">Using resource barriers to synchronize resource states in Direct3D 12</span></span>](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[<span data-ttu-id="c59a1-258">Gerenciamento de memória no Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c59a1-258">Memory management in Direct3D 12</span></span>](memory-management.md)
