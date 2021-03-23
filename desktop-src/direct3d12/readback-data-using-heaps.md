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
# <a name="read-back-data-via-a-buffer"></a><span data-ttu-id="7c62c-103">Ler dados por meio de um buffer</span><span class="sxs-lookup"><span data-stu-id="7c62c-103">Read back data via a buffer</span></span>

<span data-ttu-id="7c62c-104">Para ler os dados da GPU (por exemplo, para capturar uma captura de tela), use um heap readback.</span><span class="sxs-lookup"><span data-stu-id="7c62c-104">To read back data from the GPU (for example, to capture a screen shot), you use a readback heap.</span></span> <span data-ttu-id="7c62c-105">Essa técnica está relacionada ao [carregamento de dados de textura por meio de um buffer](upload-and-readback-of-texture-data.md), com algumas diferenças.</span><span class="sxs-lookup"><span data-stu-id="7c62c-105">This technique is related to [Uploading texture data via a buffer](upload-and-readback-of-texture-data.md), with a few differences.</span></span>

- <span data-ttu-id="7c62c-106">Para ler os dados, você cria um heap com o **D3D12_HEAP_TYPE** definido como [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type), em vez de **D3D12_HEAP_TYPE_UPLOAD**.</span><span class="sxs-lookup"><span data-stu-id="7c62c-106">To read back data, you create a heap with the **D3D12_HEAP_TYPE** set to [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type), instead of **D3D12_HEAP_TYPE_UPLOAD**.</span></span>
- <span data-ttu-id="7c62c-107">O recurso no heap de leitura regressiva sempre deve ser um **D3D12_RESOURCE_DIMENSION_BUFFER**.</span><span class="sxs-lookup"><span data-stu-id="7c62c-107">The resource on the read-back heap must always be a **D3D12_RESOURCE_DIMENSION_BUFFER**.</span></span>
- <span data-ttu-id="7c62c-108">Você usa um limite para detectar quando a GPU conclui o processamento de um quadro (quando terminar de gravar dados em seu buffer de saída).</span><span class="sxs-lookup"><span data-stu-id="7c62c-108">You use a fence to detect when the GPU completes processing a frame (when it is done writing data into your output buffer).</span></span> <span data-ttu-id="7c62c-109">Isso é importante, porque o método [**ID3D12Resource:: map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) não é sincronizado com a GPU (por outro lado, o equivalente do Direct3D 11 *é* sincronizado).</span><span class="sxs-lookup"><span data-stu-id="7c62c-109">This is important, because the [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) method doesn't synchronize with the GPU (conversely, the Direct3D 11 equivalent *does* synchronize).</span></span> <span data-ttu-id="7c62c-110">As chamadas de **mapa** do Direct3D 12 se comportam como se você chamasse o equivalente do Direct3D 11 com o sinalizador NO_OVERWRITE.</span><span class="sxs-lookup"><span data-stu-id="7c62c-110">Direct3D 12 **Map** calls behave as if you called the Direct3D 11 equivalent with the NO_OVERWRITE flag.</span></span>
- <span data-ttu-id="7c62c-111">Depois que os dados estiverem prontos (incluindo qualquer barreira de recurso necessária), chame [**ID3D12Resource:: map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) para tornar os dados do readback visíveis para a CPU.</span><span class="sxs-lookup"><span data-stu-id="7c62c-111">After the data is ready (including any necessary resource barrier), call [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) to make the readback data visible to the CPU.</span></span>

## <a name="code-example"></a><span data-ttu-id="7c62c-112">Exemplo de código</span><span class="sxs-lookup"><span data-stu-id="7c62c-112">Code example</span></span>

<span data-ttu-id="7c62c-113">O exemplo de código abaixo mostra a estrutura geral do processo de leitura de dados da GPU para a CPU por meio de um buffer.</span><span class="sxs-lookup"><span data-stu-id="7c62c-113">The code example below shows the general outline of the process of reading back data from the GPU to the CPU via a buffer.</span></span>

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

<span data-ttu-id="7c62c-114">Para obter uma implementação completa de uma rotina de captura de tela que lê a textura de destino de renderização e a grava no disco como um arquivo, consulte *Kit de ferramentas do DirectX para* [Screengrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp)da dx12.</span><span class="sxs-lookup"><span data-stu-id="7c62c-114">For a full implementation of a screenshot routine that reads the render target texture, and writes it to disk as a file, see *DirectX Tool Kit for DX12*'s [ScreenGrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c62c-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c62c-115">Related topics</span></span>

* [<span data-ttu-id="7c62c-116">Subalocação em um buffer</span><span class="sxs-lookup"><span data-stu-id="7c62c-116">Suballocation within a buffer</span></span>](large-buffers.md)
