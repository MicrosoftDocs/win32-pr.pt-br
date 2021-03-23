---
title: Ler dados por meio de um buffer
description: Para ler os dados da GPU (por exemplo, para capturar uma captura de tela), use um heap readback.
ms.assetid: 2F515B2C-3317-4AA8-81E1-7762ED895F77
ms.localizationpriority: high
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: 752d97d517a48a38adabc7c8fe51d11d47c1d8d3
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548285"
---
# <a name="read-back-data-via-a-buffer"></a>Ler dados por meio de um buffer

Para ler os dados da GPU (por exemplo, para capturar uma captura de tela), use um heap readback. Essa técnica está relacionada ao [carregamento de dados de textura por meio de um buffer](upload-and-readback-of-texture-data.md), com algumas diferenças.

- Para ler os dados, você cria um heap com o **D3D12_HEAP_TYPE** definido como [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type), em vez de **D3D12_HEAP_TYPE_UPLOAD**.
- O recurso no heap de leitura regressiva sempre deve ser um **D3D12_RESOURCE_DIMENSION_BUFFER**.
- Você usa um limite para detectar quando a GPU conclui o processamento de um quadro (quando terminar de gravar dados em seu buffer de saída). Isso é importante, porque o método [**ID3D12Resource:: map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) não é sincronizado com a GPU (por outro lado, o equivalente do Direct3D 11 *é* sincronizado). As chamadas de **mapa** do Direct3D 12 se comportam como se você chamasse o equivalente do Direct3D 11 com o sinalizador NO_OVERWRITE.
- Depois que os dados estiverem prontos (incluindo qualquer barreira de recurso necessária), chame [**ID3D12Resource:: map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) para tornar os dados do readback visíveis para a CPU.

## <a name="code-example"></a>Exemplo de código

O exemplo de código abaixo mostra a estrutura geral do processo de leitura de dados da GPU para a CPU por meio de um buffer.

```cppwinrt

// The output buffer (created below) is on a default heap, so only the GPU can access it.

D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
D3D12_RESOURCE_DESC outputBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize, D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS) };
winrt::com_ptr<::ID3D12Resource> outputBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &defaultHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &outputBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(outputBuffer),
    outputBuffer.put_void()));

// The readback buffer (created below) is on a readback heap, so that the CPU can access it.

D3D12_HEAP_PROPERTIES readbackHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_READBACK) };
D3D12_RESOURCE_DESC readbackBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize) };
winrt::com_ptr<::ID3D12Resource> readbackBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &readbackHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &readbackBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(readbackBuffer),
    readbackBuffer.put_void()));

{
    D3D12_RESOURCE_BARRIER outputBufferResourceBarrier
    {
        CD3DX12_RESOURCE_BARRIER::Transition(
            outputBuffer.get(),
            D3D12_RESOURCE_STATE_COPY_DEST,
            D3D12_RESOURCE_STATE_COPY_SOURCE)
    };
    commandList->ResourceBarrier(1, &outputBufferResourceBarrier);
}

commandList->CopyResource(readbackBuffer.get(), outputBuffer.get());

// Code goes here to close, execute (and optionally reset) the command list, and also
// to use a fence to wait for the command queue.

// The code below assumes that the GPU wrote FLOATs to the buffer.

D3D12_RANGE readbackBufferRange{ 0, outputBufferSize };
FLOAT * pReadbackBufferData{};
winrt::check_hresult(
    readbackBuffer->Map
    (
        0,
        &readbackBufferRange,
        reinterpret_cast<void**>(&pReadbackBufferData)
    )
);

// Code goes here to access the data via pReadbackBufferData.

D3D12_RANGE emptyRange{ 0, 0 };
readbackBuffer->Unmap
(
    0,
    &emptyRange
);
```

Para obter uma implementação completa de uma rotina de captura de tela que lê a textura de destino de renderização e a grava no disco como um arquivo, consulte *Kit de ferramentas do DirectX para* [Screengrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp)da dx12.

## <a name="related-topics"></a>Tópicos relacionados

* [Subalocação em um buffer](large-buffers.md)
