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
# <a name="fence-based-resource-management"></a>Gerenciamento de recursos do Fence-Based

Mostra como gerenciar o tempo de vida de dados de recursos rastreando o progresso da GPU por meio de limites. A memória pode ser efetivamente reutilizada com limites que gerenciam cuidadosamente a disponibilidade de espaço livre na memória, como em uma implementação de buffer de anéis para um heap de carregamento.

-   [Cenário de buffer de anéis](#ring-buffer-scenario)
-   [Amostra de buffer de anel](#ring-buffer-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="ring-buffer-scenario"></a>Cenário de buffer de anéis

Veja a seguir um exemplo em que um aplicativo passa por uma demanda rara para carregar a memória do heap.

Um buffer de anéis é uma maneira de gerenciar um heap de carregamento. O buffer de anéis armazena os dados necessários para os próximos quadros. O aplicativo mantém um ponteiro de entrada de dados atual e uma fila de deslocamento de quadro para registrar cada quadro e iniciar o deslocamento dos dados de recurso para esse quadro.

Um aplicativo cria um buffer de anéis com base em um buffer para carregar dados para a GPU de cada quadro. Atualmente, o quadro 2 foi renderizado, o buffer de anéis encapsula os dados do quadro 4, todos os dados necessários para o quadro 5 estão presentes e um buffer de constante grande necessário para o quadro 6 precisa ser subalocado.

**Figura 1** : o aplicativo tenta subalocar para o buffer de constantes, mas localiza memória livre insuficiente.

![memória livre insuficiente neste buffer de anéis](images/ring-buffer-1.png)

**Figura 2** : por meio da sondagem de cerca, o aplicativo descobre que o quadro 3 foi renderizado, a fila de deslocamento de quadros é atualizada e o estado atual do buffer de anéis segue-no entanto, a memória livre ainda não é grande o suficiente para acomodar o buffer de constantes.

![Ainda não há memória suficiente após o quadro 3 ter processado](images/ring-buffer-2.png)

**Figura 3** : dada a situação, a CPU bloqueia a si mesma (por meio de espera de cerca) até que o quadro 4 tenha sido renderizado, liberando a memória alocada para o quadro 4.

![o quadro de renderização 4 libera mais do que o buffer de anéis](images/ring-buffer-3.png)

**Figura 4** : agora a memória livre é grande o suficiente para o buffer de constantes e a subalocação é realizada com sucesso; o aplicativo copia os dados de buffer de grande constante para a memória usada anteriormente pelos dados de recurso para os dois quadros 3 e 4. O ponteiro de entrada atual é finalmente atualizado.

![Agora há espaço do quadro 6 no buffer de anéis](images/ring-buffer-4.png)

Se um aplicativo implementa um buffer de anéis, o buffer de anéis deve ser grande o suficiente para lidar com o cenário de pior caso dos tamanhos dos dados do recurso.

## <a name="ring-buffer-sample"></a>Amostra de buffer de anel

O código de exemplo a seguir mostra como um buffer de anéis pode ser gerenciado, prestando atenção à rotina de subalocação que lida com a sondagem de cerca e espera. Para simplificar, o exemplo usa \_ memória insuficiente \_ para ocultar os detalhes de "memória livre insuficiente encontrada no heap", pois essa lógica (com base em *m \_ pDataCur* e deslocamentos dentro de *FrameOffsetQueue*) não está estreitamente relacionada a heaps ou limites. O exemplo é simplificado para sacrificar a taxa de quadros em vez da utilização de memória.

Observe que o suporte ao buffer de anéis deve ser um cenário popular; no entanto, o design de heap não impede outro uso, como parametrização de lista de comandos e reutilização.

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

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[Subalocação em buffers](large-buffers.md)
</dt> </dl>

 

 




