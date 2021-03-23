---
title: Glossário do Direct3D 12
description: Esses termos são diferentes do Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548303"
---
# <a name="direct3d-12-glossary"></a><span data-ttu-id="1008e-103">Glossário do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1008e-103">Direct3D 12 glossary</span></span>

<span data-ttu-id="1008e-104">Esses termos são diferentes do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="1008e-104">These terms are distinctive of Direct3D 12.</span></span>

<dl> <dt>

<span data-ttu-id="1008e-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**vinculação**</span><span class="sxs-lookup"><span data-stu-id="1008e-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-106">O processo de anexar memória ao pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="1008e-106">The process of attaching memory to the graphics pipeline.</span></span> <span data-ttu-id="1008e-107">A associação de recursos, por exemplo, envolve a associação de um recurso, como uma textura ao pipeline, para uso na renderização de um objeto.</span><span class="sxs-lookup"><span data-stu-id="1008e-107">Resource binding, for example, involves the binding of a resource such as a texture to the pipeline, for use in rendering an object.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**completo**</span><span class="sxs-lookup"><span data-stu-id="1008e-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**buffer**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-109">Um tipo de recurso do D3D que é sinônimo de uma alocação de memória contígua.</span><span class="sxs-lookup"><span data-stu-id="1008e-109">A type of D3D resource that is synonymous with a contiguous memory allocation.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**Commons**</span><span class="sxs-lookup"><span data-stu-id="1008e-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**bundle**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-111">Um buffer de comando que a GPU (unidade de processamento gráfico) pode executar somente diretamente por meio de uma *lista de comandos diretas*.</span><span class="sxs-lookup"><span data-stu-id="1008e-111">A command buffer that the graphics processing unit (GPU) can execute only directly via a *direct command list*.</span></span> <span data-ttu-id="1008e-112">Um pacote herda todo o estado da GPU (exceto para o *objeto de estado de pipeline* definido e a topologia primitiva).</span><span class="sxs-lookup"><span data-stu-id="1008e-112">A bundle inherits all GPU state (except for the currently set *pipeline state object* and primitive topology).</span></span>

</dd> <dt>

<span data-ttu-id="1008e-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**alocador de comando**</span><span class="sxs-lookup"><span data-stu-id="1008e-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**command allocator**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-114">As alocações de memória subjacentes nas quais os comandos de GPU são armazenados.</span><span class="sxs-lookup"><span data-stu-id="1008e-114">The underlying memory allocations in which GPU commands are stored.</span></span> <span data-ttu-id="1008e-115">O objeto alocador de comando se aplica a *listas de comandos diretos* e *grupos*.</span><span class="sxs-lookup"><span data-stu-id="1008e-115">The command allocator object applies to both *direct command lists* and *bundles*.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**lista de comandos**</span><span class="sxs-lookup"><span data-stu-id="1008e-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**command list**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-117">Uma lista de comandos corresponde a um conjunto de comandos que a GPU executa.</span><span class="sxs-lookup"><span data-stu-id="1008e-117">A command list corresponds to a set of commands which the GPU executes.</span></span> <span data-ttu-id="1008e-118">Isso inclui comandos como definir estado, desenhar, limpar e copiar.</span><span class="sxs-lookup"><span data-stu-id="1008e-118">These include commands such as to set state, draw, clear, and copy.</span></span> <span data-ttu-id="1008e-119">A interface de lista de comandos D3D12 é significativamente diferente da interface de lista de comandos do D3D11.</span><span class="sxs-lookup"><span data-stu-id="1008e-119">The D3D12 command list interface is significantly different than the D3D11 command list interface.</span></span> <span data-ttu-id="1008e-120">A interface de lista de comandos D3D12 contém APIs semelhantes às APIs de renderização de contexto de dispositivo D3D11.</span><span class="sxs-lookup"><span data-stu-id="1008e-120">The D3D12 command list interface contains APIs similar to the D3D11 device context rendering APIs.</span></span>

<span data-ttu-id="1008e-121">Uma lista de comandos D3D12 não mapeia ou cancela recursos, altera mapeamentos de bloco, redimensiona pools de blocos, obtém dados de consulta, nem envia comandos implicitamente para a GPU para execução.</span><span class="sxs-lookup"><span data-stu-id="1008e-121">A D3D12 command list does not map or unmap resources, change tile mappings, resize tile pools, get query data, nor does it ever implicitly submit commands to the GPU for execution.</span></span>

<span data-ttu-id="1008e-122">Ao contrário dos contextos adiados do D3D11, as listas de comandos do D3D12 dão suporte apenas a dois níveis de indireção.</span><span class="sxs-lookup"><span data-stu-id="1008e-122">Unlike D3D11 deferred contexts, D3D12 command lists only support two levels of indirection.</span></span> <span data-ttu-id="1008e-123">Uma *lista de comandos diretas* corresponde a um buffer de comando que a GPU pode executar.</span><span class="sxs-lookup"><span data-stu-id="1008e-123">A *direct command list* corresponds to a command buffer which the GPU can execute.</span></span> <span data-ttu-id="1008e-124">Um *pacote* pode ser executado somente diretamente por meio de uma lista de comandos direto.</span><span class="sxs-lookup"><span data-stu-id="1008e-124">A *bundle* can be executed only directly via a direct command list.</span></span>

<span data-ttu-id="1008e-125">Uma lista de comandos diretas não herda nenhum estado de GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-125">A direct command list does not inherit any GPU state.</span></span> <span data-ttu-id="1008e-126">Um pacote herda todo o estado da GPU (exceto para o objeto de estado de pipeline definido e a topologia primitiva).</span><span class="sxs-lookup"><span data-stu-id="1008e-126">A bundle inherits all GPU state (except for the currently set pipeline state object and primitive topology).</span></span>

<span data-ttu-id="1008e-127">A memória para uma lista de comandos é definida pelo *alocador de comando*.</span><span class="sxs-lookup"><span data-stu-id="1008e-127">Memory for a command list is set by the *command allocator*.</span></span> <span data-ttu-id="1008e-128">A finalidade das listas de comandos é que elas podem ser enviadas a uma GPU como uma única solicitação de renderização.</span><span class="sxs-lookup"><span data-stu-id="1008e-128">The purpose of command lists is that they can be submitted to a GPU as a single rendering request.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**fila de comandos**</span><span class="sxs-lookup"><span data-stu-id="1008e-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**command queue**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-130">Uma fila de *listas de comandos* que a GPU executa sucessivamente.</span><span class="sxs-lookup"><span data-stu-id="1008e-130">A queue of *command lists* that the GPU executes in succession.</span></span> <span data-ttu-id="1008e-131">Os aplicativos devem enviar explicitamente as *listas de comandos* a uma fila de comandos para execução.</span><span class="sxs-lookup"><span data-stu-id="1008e-131">Applications must explicitly submit *command lists* to a command queue for execution.</span></span> <span data-ttu-id="1008e-132">Normalmente, há três filas de comando: gráficos 3D, computação e cópia, correspondentes ao pipeline de gráficos 3D, ao mecanismo de computação e a um ou mais mecanismos de cópia na GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-132">Typically there are three command queues: 3D graphics, compute and copy, corresponding to the 3D graphics pipeline, the compute engine, and one or more copy engines, on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**rasterização conservadora**</span><span class="sxs-lookup"><span data-stu-id="1008e-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**conservative rasterization**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-134">A rasterização conservadora é um modo de operação para o estágio rasterizador do pipeline de gráficos do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1008e-134">Conservative rasterization is a mode of operation for the rasterizer stage of the Direct3D graphics pipeline.</span></span> <span data-ttu-id="1008e-135">Ele desabilita a rasterização padrão baseada em amostra e, em vez disso, rasterizará um pixel coberto por qualquer valor por um primitivo.</span><span class="sxs-lookup"><span data-stu-id="1008e-135">It disables the standard sample-based rasterization, and will instead rasterize a pixel that is covered by any amount by a primitive.</span></span> <span data-ttu-id="1008e-136">Uma distinção importante é que, embora qualquer cobertura produza um pixel rasterizado, essa cobertura não pode ser caracterizada pelo hardware e, portanto, a cobertura sempre aparece em binário para um sombreador de pixel: totalmente coberta ou não coberto.</span><span class="sxs-lookup"><span data-stu-id="1008e-136">One important distinction is that, while any coverage at all produces a rasterized pixel, that coverage cannot be characterized by the hardware, so coverage always appears binary to a pixel shader: either fully covered or not covered.</span></span> <span data-ttu-id="1008e-137">Ele é deixado para o código do sombreador de pixel para determinar a cobertura real.</span><span class="sxs-lookup"><span data-stu-id="1008e-137">It is left to the pixel shader code to analytically determine the actual coverage.</span></span>

<span data-ttu-id="1008e-138">A rasterização conservadora pode ajudar com problemas como colisão e detecção de ocorrências, compartimentalização e remoção de oclusão, em que a cor de um pixel é mais específica e os casos de borda podem ser eliminados.</span><span class="sxs-lookup"><span data-stu-id="1008e-138">Conservative rasterization can help with such problems as collision and hit detection, binning, and occlusion culling, where the color of a pixel is more certain and edge cases can be eliminated.</span></span> <span data-ttu-id="1008e-139">Consulte [rasterização conservadora](conservative-rasterization.md).</span><span class="sxs-lookup"><span data-stu-id="1008e-139">See [Conservative Rasterization](conservative-rasterization.md).</span></span>

</dd> <dt>

<span data-ttu-id="1008e-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Exibição de buffer constante (CBV)**</span><span class="sxs-lookup"><span data-stu-id="1008e-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Constant Buffer View (CBV)**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-141">Os buffers de constantes contêm dados de constante de sombreador, como uma exibição de câmera, matrizes de projeção e matrizes mundiais.</span><span class="sxs-lookup"><span data-stu-id="1008e-141">Constant buffers contain shader constant data, such as a camera view, projection matrices, and world matrices.</span></span> <span data-ttu-id="1008e-142">Uma "exibição de buffer constante" é a exibição específica do formato do buffer, como visto pelo pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="1008e-142">A "constant buffer view" is the format-specific view of the buffer as seen by the graphics pipeline.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**heap padrão**</span><span class="sxs-lookup"><span data-stu-id="1008e-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**default heap**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-144">Um heap de modo de usuário que se concentra no suporte a tipos de recursos de GPU persistentes, incluindo recursos escritos por GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-144">A user-mode heap that is focused on supporting persistent GPU resource types, including GPU-written resources.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**descritor**</span><span class="sxs-lookup"><span data-stu-id="1008e-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-146">Os descritores são a unidade primária de associação para um único recurso no D3D12.</span><span class="sxs-lookup"><span data-stu-id="1008e-146">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span> <span data-ttu-id="1008e-147">Um descritor é um bloco de dados relativamente pequeno que descreve totalmente um objeto para a GPU, em um formato específico de GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-147">A descriptor is a relatively small block of data that fully describes an object to the GPU, in a GPU specific format.</span></span> <span data-ttu-id="1008e-148">Há muitos tipos diferentes de descritores: SRVs (exibições de recursos de sombreador), UAVs (exibições de acesso não ordenadas), CBVs (exibições de buffer constante) e amostras são alguns exemplos.</span><span class="sxs-lookup"><span data-stu-id="1008e-148">There are many different types of descriptors: Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers are a few examples.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**heap de descritores**</span><span class="sxs-lookup"><span data-stu-id="1008e-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**descriptor heap**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-150">Um heap de descritor é uma coleção de alocações contíguas de descritores, uma alocação para cada descritor.</span><span class="sxs-lookup"><span data-stu-id="1008e-150">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span> <span data-ttu-id="1008e-151">O ponto principal de um heap de descritor é abranger a quantidade de alocação de memória necessária para armazenar as especificações de descritor dos tipos de objetos que os sombreadores fazem referência para o maior número possível de uma janela de renderização (idealmente, um quadro inteiro de renderização ou mais).</span><span class="sxs-lookup"><span data-stu-id="1008e-151">The primary point of a descriptor heap is to encompass the bulk of memory allocation required for storing the descriptor specifications of object types that shaders reference for as large of a window of rendering as possible (ideally an entire frame of rendering or more).</span></span>

</dd> <dt>

<span data-ttu-id="1008e-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**tabela de descritores**</span><span class="sxs-lookup"><span data-stu-id="1008e-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**descriptor table**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-153">Uma tabela de descritores é logicamente uma matriz de descritores.</span><span class="sxs-lookup"><span data-stu-id="1008e-153">A descriptor table is logically an array of descriptors.</span></span> <span data-ttu-id="1008e-154">Cada tabela de descritores armazena os descritores de um ou mais tipos, incluindo SRVs, UAVe, CBVs e amostras.</span><span class="sxs-lookup"><span data-stu-id="1008e-154">Each descriptor table stores descriptors of one or more types, including SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="1008e-155">Uma tabela de descritores não é uma alocação de memória; ela é simplesmente um deslocamento e um comprimento em um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="1008e-155">A descriptor table is not an allocation of memory, it is simply an offset and length into a descriptor heap.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**lista de comandos diretos**</span><span class="sxs-lookup"><span data-stu-id="1008e-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**direct command list**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-157">Um buffer de comando que a GPU pode executar.</span><span class="sxs-lookup"><span data-stu-id="1008e-157">A command buffer that the GPU can execute.</span></span> <span data-ttu-id="1008e-158">Uma lista de comandos diretas não herda nenhum estado de GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-158">A direct command list doesn't inherit any GPU state.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**ondula**</span><span class="sxs-lookup"><span data-stu-id="1008e-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**fence**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-160">Um mecanismo para sincronizar a GPU e a CPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-160">A mechanism to synchronize the GPU and CPU.</span></span> <span data-ttu-id="1008e-161">A GPU e a CPU podem ser instruídas a aguardar em um limite, esperando em vigor para o outro processador acompanhar.</span><span class="sxs-lookup"><span data-stu-id="1008e-161">Both the GPU and CPU can be instructed to wait at a fence, waiting in effect for the other processor to catch up.</span></span> <span data-ttu-id="1008e-162">Consulte [sincronização de vários mecanismos](./user-mode-heap-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="1008e-162">See [Multi-engine synchronization](./user-mode-heap-synchronization.md).</span></span>

</dd> <dt>

<span data-ttu-id="1008e-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**risco, controle de riscos**</span><span class="sxs-lookup"><span data-stu-id="1008e-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**hazard, hazard tracking**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-164">Um risco ocorre quando um recurso foi usado para uma finalidade e o aplicativo pretende reutilizá-lo para outra finalidade.</span><span class="sxs-lookup"><span data-stu-id="1008e-164">A hazard occurs when a resource has been used for one purpose, and the app intends to reuse it for another purpose.</span></span> <span data-ttu-id="1008e-165">Para usar o recurso novamente, os caches intermediários precisarão ser liberados ou invalidados, os requisitos de compactação precisarão ser consistentes com o segundo uso e o recurso deverá estar no estado necessário para evitar a leitura do recurso depois que ele tiver sido gravado e invalidado para a finalidade pretendida.</span><span class="sxs-lookup"><span data-stu-id="1008e-165">In order to use the resource again, intermediate caches will need to be flushed or invalidated, compression requirements will need to be consistent with the second use, and the resource should be in the required state to avoid reading the resource after it has been written to and invalidated for the intended purpose.</span></span>

<span data-ttu-id="1008e-166">O processo de manutenção de recursos e de evitar esses problemas de sincronização é conhecido como controle de risco.</span><span class="sxs-lookup"><span data-stu-id="1008e-166">The process of maintaining resources and avoiding these sync issues is known as hazard tracking.</span></span> <span data-ttu-id="1008e-167">Se não houver nenhum controle de risco pelo driver, o aplicativo será responsável por isso.</span><span class="sxs-lookup"><span data-stu-id="1008e-167">If there is no hazard tracking by the driver, then the app is responsible for this.</span></span> <span data-ttu-id="1008e-168">Na maioria das versões anteriores do DirectX, o controle de riscos foi manipulado pelo driver.</span><span class="sxs-lookup"><span data-stu-id="1008e-168">In most earlier versions of DirectX, hazard tracking was handled by the driver.</span></span> <span data-ttu-id="1008e-169">Para melhorar o desempenho, os métodos sem controle de risco estão disponíveis no DirectX 12.</span><span class="sxs-lookup"><span data-stu-id="1008e-169">To improve performance, methods without hazard tracking are available in DirectX 12.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**Linguagem de sombreamento de alto nível (HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1008e-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level Shader Language (HLSL)**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-171">Uma linguagem de computador, semelhante, mas distinta de várias maneiras, que é usada para escrever código de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1008e-171">A computer language, similar but distinct in many ways from C, that is used to write shader code.</span></span> <span data-ttu-id="1008e-172">Os sombreadores de vértice, pixel, geometria, computação, domínio e envoltória são todos escritos usando HLSL.</span><span class="sxs-lookup"><span data-stu-id="1008e-172">Vertex, pixel, geometry, compute, domain, and hull shaders are all written using HLSL.</span></span> <span data-ttu-id="1008e-173">Um compilador converte a origem HLSL em um formato binário para consumir a GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-173">A compiler converts the HLSL source into a binary format for the GPU to consume.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**</span><span class="sxs-lookup"><span data-stu-id="1008e-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-175">As diferentes instâncias e tipos de mecanismos em uma única GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-175">The different instances and types of engines in a single GPU.</span></span> <span data-ttu-id="1008e-176">Os tipos de mecanismos incluem: gráficos, computação e cópia.</span><span class="sxs-lookup"><span data-stu-id="1008e-176">The types of engines include: graphics, compute, and copy.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span><span class="sxs-lookup"><span data-stu-id="1008e-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-178">Uma configuração de hardware onde há mais de um adaptador gráfico.</span><span class="sxs-lookup"><span data-stu-id="1008e-178">A hardware configuration where there is more than one graphics adapter.</span></span> <span data-ttu-id="1008e-179">Os adaptadores separados, às vezes, são chamados de nós.</span><span class="sxs-lookup"><span data-stu-id="1008e-179">The separate adapters are sometimes referred to as nodes.</span></span> <span data-ttu-id="1008e-180">Ter várias GPUs pode tornar a tarefa de sincronizá-las com a CPU e outra, consideravelmente mais complexa do que com uma única GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-180">Having multiple GPUs can make the task of synchronizing them with the CPU, and each other, considerably more complex than with a single GPU.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Objeto de estado de pipeline (PSO)**</span><span class="sxs-lookup"><span data-stu-id="1008e-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Pipeline State object (PSO)**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-182">Uma parte significativa do estado da GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-182">A significant portion of the state of the GPU.</span></span> <span data-ttu-id="1008e-183">Esse estado inclui todos os sombreadores definidos atualmente e determinados objetos de estado de função fixa.</span><span class="sxs-lookup"><span data-stu-id="1008e-183">This state includes all currently set shaders and certain fixed-function state objects.</span></span> <span data-ttu-id="1008e-184">A única maneira de alterar os Estados contidos no objeto de pipeline é alterar o objeto de pipeline vinculado no momento.</span><span class="sxs-lookup"><span data-stu-id="1008e-184">The only way to change states contained within the pipeline object is to change the currently bound pipeline object.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predicação**</span><span class="sxs-lookup"><span data-stu-id="1008e-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predication**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-186">Predicação é um recurso que habilita a GPU em vez da CPU para determinar não desenhar, copiar ou distribuir um objeto.</span><span class="sxs-lookup"><span data-stu-id="1008e-186">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span> <span data-ttu-id="1008e-187">Por exemplo, se uma caixa delimitadora de um objeto for totalmente obstruído por outro objeto ou a perspectiva tiver reduzido o objeto para menos do que o tamanho de um pixel, pode não haver nenhum ponto na tentativa de desenhar o objeto oculto.</span><span class="sxs-lookup"><span data-stu-id="1008e-187">For example, if a bounding box of an object is totally occluded by another object or perspective has reduced the object to less than the size of a pixel, there may be no point in attempting to draw the hidden object at all.</span></span> <span data-ttu-id="1008e-188">Consulte [predicação](predication.md).</span><span class="sxs-lookup"><span data-stu-id="1008e-188">See [Predication](predication.md).</span></span>

</dd> <dt>

<span data-ttu-id="1008e-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Exibição de ordem do rasterizador (ROV)**</span><span class="sxs-lookup"><span data-stu-id="1008e-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Rasterizer Order View (ROV)**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-190">Pipelines gráficos padrão podem ter problemas para compor corretamente várias texturas que contêm transparência.</span><span class="sxs-lookup"><span data-stu-id="1008e-190">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="1008e-191">Objetos como isolamentos de fio, fumaça, fogo, vegetação e transparência de uso de vidro colorido para obter o efeito desejado.</span><span class="sxs-lookup"><span data-stu-id="1008e-191">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="1008e-192">Os problemas surgem quando várias texturas que contêm transparência estão alinhadas umas com as outras (fumaça na frente de uma cerca na frente de um prédio contendo vegetação, como um exemplo).</span><span class="sxs-lookup"><span data-stu-id="1008e-192">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="1008e-193">As exibições ordenadas do rasterizador (ROVs) habilitam os algoritmos de OIT (transparência independente de ordem subjacente) para usar os recursos do hardware para tentar resolver a ordem de transparência corretamente.</span><span class="sxs-lookup"><span data-stu-id="1008e-193">Rasterizer ordered views (ROVs) enable the underlying Order Independent Transparency (OIT) algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="1008e-194">A transparência é manipulada pelo sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="1008e-194">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="1008e-195">As exibições ordenadas do rasterizador (ROVs) permitem que o código do sombreador de pixel marque associações de UAV (exibição de acesso não ordenado) com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para UAVs.</span><span class="sxs-lookup"><span data-stu-id="1008e-195">Rasterizer Ordered Views (ROVs) allow pixel shader code to mark Unordered Access View (UAV) bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**heap de readback**</span><span class="sxs-lookup"><span data-stu-id="1008e-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**readback heap**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-197">Um heap de modo de usuário que se concentra na transferência de dados da GPU de volta para a CPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-197">A user-mode heap that is focused on data transfer from the GPU back to the CPU.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**Kit**</span><span class="sxs-lookup"><span data-stu-id="1008e-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**resource**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-199">Uma entidade que fornece dados para o pipeline e define o que é processado durante sua cena.</span><span class="sxs-lookup"><span data-stu-id="1008e-199">An entity that provides data to the pipeline and defines what is rendered during your scene.</span></span> <span data-ttu-id="1008e-200">Os recursos podem ser carregados a partir da mídia de jogo ou criados dinamicamente no momento de execução.</span><span class="sxs-lookup"><span data-stu-id="1008e-200">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="1008e-201">Normalmente, os recursos incluem dados de textura, dados de vértice e dados de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1008e-201">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="1008e-202">A maioria dos aplicativos do Direct3D cria e destrói recursos extensivamente durante seu ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="1008e-202">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**barreira de recurso**</span><span class="sxs-lookup"><span data-stu-id="1008e-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**resource barrier**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-204">Uma barreira de recurso notifica o driver de que a sincronização de vários acessos a um único recurso pode ser necessária, por exemplo, leitura e gravação na mesma textura.</span><span class="sxs-lookup"><span data-stu-id="1008e-204">A resource barrier notifies the driver that synchronization of multiple accesses to a single resource may be required, for example, reading and writing to the same texture.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**Associação de recursos**</span><span class="sxs-lookup"><span data-stu-id="1008e-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**resource binding**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-206">A associação de recursos é o processo de vinculação de recursos (texturas, buffers de vértice, buffers de índice e assim por diante) ao pipeline de gráficos, permitindo que os sombreadores do pipeline processem o recurso correto.</span><span class="sxs-lookup"><span data-stu-id="1008e-206">Resource binding is the process of linking resources (textures, vertex buffers, index buffers, and so on), to the graphics pipeline, enabling the shaders of the pipeline to process the correct resource.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**heaps de recursos**</span><span class="sxs-lookup"><span data-stu-id="1008e-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**resource heaps**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-208">Heaps de recursos é um termo genérico para os heaps que são buffers de memória separados para manter recursos à medida que são transferidos para e da GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-208">Resource heaps is a generic term for the heaps that are memory buffers set aside to hold resources as they are transferred to and from the GPU.</span></span> <span data-ttu-id="1008e-209">Uma transferência para a GPU requer um heap de carregamento, da GPU para a CPU requer um heap readback e um heap persistente para a GPU a ser mantido em vários quadros de renderização é chamado de heap padrão.</span><span class="sxs-lookup"><span data-stu-id="1008e-209">A transfer to the GPU requires an Upload Heap, from the GPU to the CPU requires a Readback Heap, and a persistent heap for the GPU to maintain over multiple rendering frames is called a Default Heap.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**assinatura de raiz**</span><span class="sxs-lookup"><span data-stu-id="1008e-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**root signature**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-211">As assinaturas raiz definem todos os recursos que devem ser associados aos pipelines de gráficos ou de computação.</span><span class="sxs-lookup"><span data-stu-id="1008e-211">Root signatures define all the resources that are to be bound to the graphics, or compute, pipelines.</span></span> <span data-ttu-id="1008e-212">Uma assinatura de raiz é configurada pelas listas de comandos de aplicativo e links para os recursos que os sombreadores exigem normalmente, há um gráfico e uma assinatura raiz de computação por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1008e-212">A root signature is configured by the app and links command lists to the resources that the shaders require Typically, there is one graphics and one compute root signature per app.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**cores**</span><span class="sxs-lookup"><span data-stu-id="1008e-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**sampler**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-214">Um amostra é o código que lê de uma textura.</span><span class="sxs-lookup"><span data-stu-id="1008e-214">A sampler is code that reads from a texture.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Modo de Exibição de Recursos do sombreador (SRV)**</span><span class="sxs-lookup"><span data-stu-id="1008e-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader Resource View (SRV)**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-216">Uma maneira específica de formato de examinar os dados em um recurso de sombreador, como uma textura.</span><span class="sxs-lookup"><span data-stu-id="1008e-216">A format-specific way to look at the data in a shader resource, such as a texture.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**heap estático**</span><span class="sxs-lookup"><span data-stu-id="1008e-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**static heap**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-218">Um heap de modo de usuário que se concentra em vários recursos somente leitura de GPU que normalmente são usados ao mesmo tempo e não são alterados com frequência.</span><span class="sxs-lookup"><span data-stu-id="1008e-218">A user-mode heap that is focused on multiple GPU-read-only resources that are typically used at the same time and are not changed frequently.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**Cadeia de permuta**</span><span class="sxs-lookup"><span data-stu-id="1008e-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-220">As cadeias de permuta controlam a rotação do buffer de fundo, formando a base da animação de gráficos.</span><span class="sxs-lookup"><span data-stu-id="1008e-220">Swap chains control the back buffer rotation, forming the basis of graphics animation.</span></span> <span data-ttu-id="1008e-221">As cadeias de permuta são manipuladas pelo conjunto de APIs de nível baixo DXGI (consulte [visão geral do dxgi](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span><span class="sxs-lookup"><span data-stu-id="1008e-221">Swap chains are handled by the low level API set DXGI (see [DXGI Overview](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1008e-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span><span class="sxs-lookup"><span data-stu-id="1008e-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-223">Uma técnica de localizar dados multidimensionais na memória, de modo que os dados da dimensionalidade próxima tendem a ter endereços próximos.</span><span class="sxs-lookup"><span data-stu-id="1008e-223">A technique of locating multidimensional data in memory such that data of nearby dimensionality tends to have nearby addresses.</span></span> <span data-ttu-id="1008e-224">Em particular, todos os dados de uma linha não estão localizados de forma contígua antes dos dados da próxima linha.</span><span class="sxs-lookup"><span data-stu-id="1008e-224">In particular, all the data for one row is not located contiguously before the data for the next row.</span></span> <span data-ttu-id="1008e-225">Um "swizzle com parâmetros" descreve uma maneira padronizada para descrever os padrões de swizzle.</span><span class="sxs-lookup"><span data-stu-id="1008e-225">A "Parameterized Swizzle" describes a standardized way to describe swizzle patterns.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**textura**</span><span class="sxs-lookup"><span data-stu-id="1008e-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**texture**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-227">Um tipo de recurso do D3D que é multidimensional e tem um layout de memória que é otimizado para acesso multidimensional da GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-227">A type of D3D resource that is multi-dimensional and has a memory layout that is optimized for multi-dimensional access from the GPU.</span></span> <span data-ttu-id="1008e-228">As texturas geralmente contêm a imagem bruta necessária para renderizar em uma superfície, antes que a iluminação e a mesclagem ocorram, mas possam conter outras formas de dados, como gradientes de cores e cores de referência.</span><span class="sxs-lookup"><span data-stu-id="1008e-228">Textures often contain the raw image required to render onto a surface, before lighting and blending takes place, but can contain other forms of data such as color gradients and reference colors.</span></span> <span data-ttu-id="1008e-229">O Direct3D 12 dá suporte a uma, duas e três texturas dimensionais.</span><span class="sxs-lookup"><span data-stu-id="1008e-229">Direct3D 12 supports one, two, and three dimensional textures.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**bloco**</span><span class="sxs-lookup"><span data-stu-id="1008e-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**tile**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-231">Uma página de memória de vídeo, semelhante a uma página de CPU/sistema de memória.</span><span class="sxs-lookup"><span data-stu-id="1008e-231">A page of video memory, similar to a CPU/System page of memory.</span></span> <span data-ttu-id="1008e-232">A notação de bloco ajuda a distinguir o subsistema de memória virtual da GPU do subsistema de memória virtual da CPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-232">The tile notation helps to distinguish the GPU virtual memory subsystem from the CPU virtual memory subsystem.</span></span> <span data-ttu-id="1008e-233">As GPUs fornecem recursos de memória virtual semelhantes à memória virtual do sistema.</span><span class="sxs-lookup"><span data-stu-id="1008e-233">GPUs provide similar virtual memory capabilities as system virtual memory.</span></span> <span data-ttu-id="1008e-234">Algumas GPUs têm recursos de memória virtual compartilhados, que permitem o compartilhamento de algumas páginas do subsistema de memória virtual com a CPU e a GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-234">Some GPUs have shared virtual memory capabilities, which allow for the sharing of some pages of the virtual memory subsystem with both the CPU and GPU.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**recursos em ladrilho**</span><span class="sxs-lookup"><span data-stu-id="1008e-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-236">Os recursos do lado do ladrilho são necessários, portanto, menos memória da GPU é desperdiçada, armazenando regiões de superfícies que o aplicativo sabe que não será acessado, e o hardware pode entender como filtrar por blocos adjacentes.</span><span class="sxs-lookup"><span data-stu-id="1008e-236">Tiled resources are needed so less GPU memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span> <span data-ttu-id="1008e-237">Os recursos em ladrilho são grandes recursos lógicos, mas exigem pequenas quantidades de memória física.</span><span class="sxs-lookup"><span data-stu-id="1008e-237">Tiled resources are large logical resources, but requiring small amounts of physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Modo de exibição de acesso não ordenado (UAV)**</span><span class="sxs-lookup"><span data-stu-id="1008e-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unordered Access View (UAV)**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-239">Uma exibição de acesso não ordenada em um recurso (que inclui buffers, texturas e matrizes de textura, sem várias amostras), permite acesso de leitura/gravação não ordenado de forma temporal de vários threads.</span><span class="sxs-lookup"><span data-stu-id="1008e-239">An unordered access view into a resource (which includes buffers, textures, and texture arrays - without multi-sampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="1008e-240">Isso significa que esse tipo de recurso pode ser lido/gravado simultaneamente por vários threads sem gerar conflitos de memória.</span><span class="sxs-lookup"><span data-stu-id="1008e-240">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**carregar heap**</span><span class="sxs-lookup"><span data-stu-id="1008e-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**upload heap**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-242">Um heap de modo de usuário que se concentra na transferência de dados da CPU para a GPU.</span><span class="sxs-lookup"><span data-stu-id="1008e-242">A user-mode heap that is focused on data transfer from the CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**heap de modo de usuário**</span><span class="sxs-lookup"><span data-stu-id="1008e-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**user-mode heap**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-244">Uma coleção de alocações de memória grandes e contíguas que são recicladas sem reconhecimento de qualquer componente de kernel: os métodos de alocação e destruição não chamam métodos de alocação e destruição de kernel durante o estado Steady.</span><span class="sxs-lookup"><span data-stu-id="1008e-244">A collection of large, contiguous memory allocations that are recycled without any kernel component's awareness: the allocation and destruction methods do not call kernel allocation and destruction methods during steady state.</span></span> <span data-ttu-id="1008e-245">Upload, readback e heaps padrão são variantes de heaps de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="1008e-245">Upload, Readback, and Default heaps are variants of user mode heaps.</span></span>

</dd> <dt>

<span data-ttu-id="1008e-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**recursos de sublado do volume**</span><span class="sxs-lookup"><span data-stu-id="1008e-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**volume tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="1008e-247">[Recursos de lado](/windows)triplo tridimensionais.</span><span class="sxs-lookup"><span data-stu-id="1008e-247">Three-dimensional [tiled resources](/windows).</span></span>

</dd> </dl>

 

 