---
title: Gerenciamento de recursos do Fence-Based
description: Mostra como gerenciar o tempo de vida de dados de recursos rastreando o progresso da GPU por meio de limites. A memória pode ser efetivamente reutilizada com limites que gerenciam cuidadosamente a disponibilidade de espaço livre na memória, como em uma implementação de buffer de anéis para um heap de carregamento.
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba8afd66f8a50a54b699c6a314ba148ebcef023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103610"
---
# <a name="fence-based-resource-management"></a><span data-ttu-id="6b2e5-104">Gerenciamento de recursos do Fence-Based</span><span class="sxs-lookup"><span data-stu-id="6b2e5-104">Fence-Based Resource Management</span></span>

<span data-ttu-id="6b2e5-105">Mostra como gerenciar o tempo de vida de dados de recursos rastreando o progresso da GPU por meio de limites.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-105">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="6b2e5-106">A memória pode ser efetivamente reutilizada com limites que gerenciam cuidadosamente a disponibilidade de espaço livre na memória, como em uma implementação de buffer de anéis para um heap de carregamento.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-106">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span>

-   [<span data-ttu-id="6b2e5-107">Cenário de buffer de anéis</span><span class="sxs-lookup"><span data-stu-id="6b2e5-107">Ring buffer scenario</span></span>](#ring-buffer-scenario)
-   [<span data-ttu-id="6b2e5-108">Amostra de buffer de anel</span><span class="sxs-lookup"><span data-stu-id="6b2e5-108">Ring buffer sample</span></span>](#ring-buffer-sample)
-   [<span data-ttu-id="6b2e5-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b2e5-109">Related topics</span></span>](#related-topics)

## <a name="ring-buffer-scenario"></a><span data-ttu-id="6b2e5-110">Cenário de buffer de anéis</span><span class="sxs-lookup"><span data-stu-id="6b2e5-110">Ring buffer scenario</span></span>

<span data-ttu-id="6b2e5-111">Veja a seguir um exemplo em que um aplicativo passa por uma demanda rara para carregar a memória do heap.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-111">The following is an example in which an app experiences a rare demand for upload heap memory.</span></span>

<span data-ttu-id="6b2e5-112">Um buffer de anéis é uma maneira de gerenciar um heap de carregamento.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-112">A ring buffer is one way to manage an upload heap.</span></span> <span data-ttu-id="6b2e5-113">O buffer de anéis armazena os dados necessários para os próximos quadros.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-113">The ring buffer holds data required for the next few frames.</span></span> <span data-ttu-id="6b2e5-114">O aplicativo mantém um ponteiro de entrada de dados atual e uma fila de deslocamento de quadro para registrar cada quadro e iniciar o deslocamento dos dados de recurso para esse quadro.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-114">The app maintains a current data input pointer, and a frame offset queue to record each frame and starting offset of resource data for that frame.</span></span>

<span data-ttu-id="6b2e5-115">Um aplicativo cria um buffer de anéis com base em um buffer para carregar dados para a GPU de cada quadro.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-115">An app creates a ring-buffer based upon a buffer to upload data to the GPU for each frame.</span></span> <span data-ttu-id="6b2e5-116">Atualmente, o quadro 2 foi renderizado, o buffer de anéis encapsula os dados do quadro 4, todos os dados necessários para o quadro 5 estão presentes e um buffer de constante grande necessário para o quadro 6 precisa ser subalocado.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-116">Currently frame 2 has been rendered, the ring buffer wraps around the data for frame 4, all the data required for frame 5 is present, and a large constant buffer required for frame 6 needs to be sub-allocated.</span></span>

<span data-ttu-id="6b2e5-117">**Figura 1** : o aplicativo tenta subalocar para o buffer de constantes, mas localiza memória livre insuficiente.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-117">**Figure 1** : the app tries to sub-allocate for the constant buffer, but finds insufficient free memory.</span></span>

![memória livre insuficiente neste buffer de anéis](images/ring-buffer-1.png)

<span data-ttu-id="6b2e5-119">**Figura 2** : por meio da sondagem de cerca, o aplicativo descobre que o quadro 3 foi renderizado, a fila de deslocamento de quadros é atualizada e o estado atual do buffer de anéis segue-no entanto, a memória livre ainda não é grande o suficiente para acomodar o buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-119">**Figure 2** : through fence polling, the app discovers that frame 3 has been rendered, the frame offset queue is then updated, and the current state of the ring buffer follows - however, free memory is still not large enough to accommodate the constant buffer.</span></span>

![Ainda não há memória suficiente após o quadro 3 ter processado](images/ring-buffer-2.png)

<span data-ttu-id="6b2e5-121">**Figura 3** : dada a situação, a CPU bloqueia a si mesma (por meio de espera de cerca) até que o quadro 4 tenha sido renderizado, liberando a memória alocada para o quadro 4.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-121">**Figure 3** : given the situation, the CPU blocks itself (via fence waiting) until frame 4 has been rendered, which frees up the memory sub-allocated for frame 4.</span></span>

![o quadro de renderização 4 libera mais do que o buffer de anéis](images/ring-buffer-3.png)

<span data-ttu-id="6b2e5-123">**Figura 4** : agora a memória livre é grande o suficiente para o buffer de constantes e a subalocação é realizada com sucesso; o aplicativo copia os dados de buffer de grande constante para a memória usada anteriormente pelos dados de recurso para os dois quadros 3 e 4.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-123">**Figure 4** : now free memory is large enough for the constant buffer, and sub-allocation succeeds; the app copies the big constant buffer data to memory previously used by resource data for both frames 3 and 4.</span></span> <span data-ttu-id="6b2e5-124">O ponteiro de entrada atual é finalmente atualizado.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-124">The current input pointer is finally updated.</span></span>

![Agora há espaço do quadro 6 no buffer de anéis](images/ring-buffer-4.png)

<span data-ttu-id="6b2e5-126">Se um aplicativo implementa um buffer de anéis, o buffer de anéis deve ser grande o suficiente para lidar com o cenário de pior caso dos tamanhos dos dados do recurso.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-126">If an app implements a ring buffer, the ring buffer must be large enough to cope with the worse-case scenario of the sizes of resource data.</span></span>

## <a name="ring-buffer-sample"></a><span data-ttu-id="6b2e5-127">Amostra de buffer de anel</span><span class="sxs-lookup"><span data-stu-id="6b2e5-127">Ring buffer sample</span></span>

<span data-ttu-id="6b2e5-128">O código de exemplo a seguir mostra como um buffer de anéis pode ser gerenciado, prestando atenção à rotina de subalocação que lida com a sondagem de cerca e espera.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-128">The following sample code shows how a ring buffer can be managed, paying attention to the sub-allocation routine that handles fence polling and waiting.</span></span> <span data-ttu-id="6b2e5-129">Para simplificar, o exemplo usa \_ memória insuficiente \_ para ocultar os detalhes de "memória livre insuficiente encontrada no heap", pois essa lógica (com base em *m \_ pDataCur* e deslocamentos dentro de *FrameOffsetQueue*) não está estreitamente relacionada a heaps ou limites.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-129">For simplicity, the sample uses NOT\_SUFFICIENT\_MEMORY to hide the details of “not sufficient free memory found in the heap” since that logic (based on *m\_pDataCur* and offsets inside *FrameOffsetQueue*) is not tightly related to heaps or fences.</span></span> <span data-ttu-id="6b2e5-130">O exemplo é simplificado para sacrificar a taxa de quadros em vez da utilização de memória.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-130">The sample is simplified to sacrifice frame rate instead of memory utilization.</span></span>

<span data-ttu-id="6b2e5-131">Observe que o suporte ao buffer de anéis deve ser um cenário popular; no entanto, o design de heap não impede outro uso, como parametrização de lista de comandos e reutilização.</span><span class="sxs-lookup"><span data-stu-id="6b2e5-131">Note that, ring-buffer support is expected to be a popular scenario; however, the heap design does not preclude other usage, such as command list parameterization and re-use.</span></span>

``` syntax
struct FrameResourceOffset
{
    UINT frameIndex;
    UINT8* pResourceOffset;
};
std::queue<FrameResourceOffset> frameOffsetQueue;

void DrawFrame()
{
    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float), 
            4, // Max alignment requirement for vertex data is 4 bytes.
            verticesOffset
            ));

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT,
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model. 
    // Create constant buffer views for the new binding model. 
    // ...

    commandQueue->Execute(commandList);
    commandQueue->AdvanceFence();
}

HRESULT SuballocateFromHeap(SIZE_T uSize, UINT uAlign)
{
    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Free up resources for frames processed by GPU; see Figure 2.
        UINT lastCompletedFrame = commandQueue->GetLastCompletedFence();
        FreeUpMemoryUntilFrame( lastCompletedFrame );

        while ( NOT_SUFFICIENT_MEMORY(uSize, uAlign)
            && !frameOffsetQueue.empty() )
        {
            // Block until a new frame is processed by GPU, then free up more memory; see Figure 3.
            UINT nextGPUFrame = frameOffsetQueue.front().frameIndex;
            commandQueue->SetEventOnFenceCompletion(nextGPUFrame, hEvent);
            WaitForSingleObject(hEvent, INFINITE);
            FreeUpMemoryUntilFrame( nextGPUFrame );
        }
    }

    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Apps need to create a new Heap that is large enough for this resource.
        return E_HEAPNOTLARGEENOUGH;
    }
    else
    {
        // Update current data pointer for the new resource.
        m_pDataCur = reinterpret_cast<UINT8*>(
            Align(reinterpret_cast<SIZE_T>(m_pHDataCur), uAlign)
            );

        // Update frame offset queue if this is the first resource for a new frame; see Figure 4.
        UINT currentFrame = commandQueue->GetCurrentFence();
        if ( frameOffsetQueue.empty()
            || frameOffsetQueue.back().frameIndex < currentFrame )
        {
            FrameResourceOffset offset = {currentFrame, m_pDataCur};
            frameOffsetQueue.push(offset);
        }

        return S_OK;
    }
}

void FreeUpMemoryUntilFrame(UINT lastCompletedFrame)
{
    while ( !frameOffsetQueue.empty() 
        && frameOffsetQueue.first().frameIndex <= lastCompletedFrame )
    {
        frameOffsetQueue.pop();
    }
}
```

## <a name="related-topics"></a><span data-ttu-id="6b2e5-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b2e5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b2e5-133">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="6b2e5-133">**ID3D12Fence**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[<span data-ttu-id="6b2e5-134">Subalocação em buffers</span><span class="sxs-lookup"><span data-stu-id="6b2e5-134">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




