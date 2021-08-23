---
title: Gerenciamento de recursos baseados em limites
description: Mostra como gerenciar o tempo de vida dos dados de recurso acompanhando o progresso da GPU por meio de cercas. A memória pode ser efetivamente re usada com cercas que gerenciam cuidadosamente a disponibilidade de espaço livre na memória, como em uma implementação de buffer de anéis para um heap de Upload.
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cbfd9231e3013099c8382072049f1ae1478e28f00830e89fb4ecef1b835ce58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728850"
---
# <a name="fence-based-resource-management"></a>Gerenciamento de recursos baseados em limites

Mostra como gerenciar o tempo de vida dos dados de recurso acompanhando o progresso da GPU por meio de cercas. A memória pode ser efetivamente re usada com cercas que gerenciam cuidadosamente a disponibilidade de espaço livre na memória, como em uma implementação de buffer de anéis para um heap de Upload.

-   [Cenário de buffer de anéis](#ring-buffer-scenario)
-   [Exemplo de buffer de anéis](#ring-buffer-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="ring-buffer-scenario"></a>Cenário de buffer de anéis

A seguir está um exemplo no qual um aplicativo passa por uma demanda rara de carregamento de memória de heap.

Um buffer de anéis é uma maneira de gerenciar um heap de upload. O buffer de anéis contém os dados necessários para os próximos quadros. O aplicativo mantém um ponteiro de entrada de dados atual e uma fila de deslocamento de quadro para registrar cada quadro e o deslocamento inicial dos dados do recurso para esse quadro.

Um aplicativo cria um buffer de anéis com base em um buffer para carregar dados para a GPU de cada quadro. Atualmente, o quadro 2 foi renderizado, o buffer de anéis envolve os dados do quadro 4, todos os dados necessários para o quadro 5 estão presentes e um buffer constante grande necessário para o quadro 6 precisa ser sublocado.

**Figura 1:** o aplicativo tenta sublocar para o buffer constante, mas encontra memória livre insuficiente.

![memória livre insuficiente neste buffer de anéis](images/ring-buffer-1.png)

**Figura 2:** por meio da sondagem de cerca, o aplicativo descobre que o quadro 3 foi renderizado, a fila de deslocamento do quadro é atualizada e o estado atual do buffer de anéis segue - no entanto, a memória livre ainda não é grande o suficiente para acomodar o buffer constante.

![memória ainda insuficiente após o quadro 3 ter sido renderizado](images/ring-buffer-2.png)

**Figura 3:** dada a situação, a CPU se bloqueia (por meio de espera de cerca) até que o quadro 4 tenha sido renderizado, o que libera a memória sublocada para o quadro 4.

![renderização do quadro 4 libera mais do buffer de anéis](images/ring-buffer-3.png)

**Figura 4:** agora a memória livre é grande o suficiente para o buffer constante e a subatribuição é bem-sucedida; o aplicativo copia os dados de buffer de constante grande para a memória usada anteriormente pelos dados de recurso para os quadros 3 e 4. O ponteiro de entrada atual é finalmente atualizado.

![agora há espaço do quadro 6 no buffer de anéis](images/ring-buffer-4.png)

Se um aplicativo implementar um buffer de anéis, o buffer de anéis deverá ser grande o suficiente para lidar com o cenário pior dos tamanhos de dados de recurso.

## <a name="ring-buffer-sample"></a>Exemplo de buffer de anéis

O código de exemplo a seguir mostra como um buffer de anéis pode ser gerenciado, preste atenção à rotina de subatribuição que lida com sondagem de cerca e espera. Para simplificar, o exemplo usa NOT SUFFICIENT MEMORY para ocultar os detalhes de "memória livre insuficiente encontrada no heap", pois essa lógica (com base em \_ m \_ *\_ pDataCur* e deslocamentos dentro de *FrameOffsetQueue*) não está fortemente relacionada a heaps ou cercas. O exemplo é simplificado para simplificar a taxa de quadros em vez da utilização de memória.

Observe que o suporte a buffer de anéis deve ser um cenário popular; no entanto, o design do heap não impede outro uso, como parametrização e rea utilização da lista de comandos.

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

 

 




