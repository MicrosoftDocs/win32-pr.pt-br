---
title: Criando e gravando listas de comandos e pacotes
description: Este tópico descreve a gravação de listas de comandos e pacotes em aplicativos Direct3D 12. As listas de comandos e os pacotes permitem que os aplicativos registrem chamadas de desenho ou alteração de estado para execução posterior na GPU (unidade de processamento gráfico).
ms.assetid: 0074B796-33A4-4AA1-A4E7-48A2A63F25B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480819cbd421b30cbf54a58578c02056d37d7e36bf2ead845c19e438df54cbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850703"
---
# <a name="creating-and-recording-command-lists-and-bundles"></a>Criando e gravando listas de comandos e pacotes

Este tópico descreve a gravação de listas de comandos e pacotes em aplicativos Direct3D 12. As listas de comandos e os pacotes permitem que os aplicativos registrem chamadas de desenho ou alteração de estado para execução posterior na GPU (unidade de processamento gráfico).

Além das listas de comandos, a API explora a funcionalidade presente no hardware de GPU adicionando um segundo nível de listas de comandos, que são conhecidas como *grupos*. A finalidade dos pacotes é permitir que os aplicativos agrupem um pequeno número de comandos de API juntos para execução posterior. No momento da criação do pacote, o driver executará o máximo de pré-processamento possível para torná-los baratos para serem executados posteriormente. Os grupos são projetados para serem usados e reutilizados várias vezes. As listas de comandos, por outro lado, normalmente são executadas apenas uma vez. No entanto, uma lista de comandos *pode* ser executada várias vezes (contanto que o aplicativo garanta que as execuções anteriores foram concluídas antes de enviar novas execuções).

Normalmente, a compilação de chamadas de API em pacotes, chamadas de API e pacotes em listas de comandos e listas de comandos em um único quadro, é mostrada no diagrama a seguir, observando a reutilização do **pacote 1** na **lista de comandos 1** e da **lista de comandos 2**, e que os nomes do método de API no diagrama são apenas exemplos, muitas chamadas de API diferentes podem ser usadas.

![Criando comandos, pacotes e listas de comandos em quadros](images/gpu-workitems.png)

Há diferentes restrições para criar e executar pacotes e listas de comandos diretos, e essas diferenças são indicadas ao longo deste tópico.

## <a name="creating-command-lists"></a>Criando listas de comandos

Os grupos e as listas de comandos diretos são criados chamando [**ID3D12Device:: Createcommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) ou [**ID3D12Device4:: CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1).

Use [**ID3D12Device4:: CreateCommandList1**](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommandlist1) para criar uma lista de comandos fechados, em vez de criar uma nova lista e fechá-la imediatamente. Isso evita a ineficiência da criação de uma lista com um alocador e um PSO, mas não para usá-las.

[**ID3D12Device:: Createcommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) usa os seguintes parâmetros como entrada:

### <a name="d3d12_command_list_type"></a>\_Tipo de \_ lista de comandos D3D12 \_

A enumeração do [**\_ tipo de \_ lista \_ de comandos D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) indica o tipo de lista de comandos que está sendo criada. Pode ser uma lista de comandos diretas, um pacote, uma lista de comandos de computação ou uma lista de comandos de cópia.

### <a name="id3d12commandallocator"></a>ID3D12CommandAllocator

Um alocador de comando permite que o aplicativo gerencie a memória alocada para listas de comandos. O alocador de comando é criado chamando [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator). Ao criar uma lista de comandos, o tipo de lista de comandos do alocador, especificado pelo [**\_ tipo de \_ lista \_ de comandos D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type), deve corresponder ao tipo de lista de comandos que está sendo criado. Um determinado alocador pode ser associado a não mais de uma lista de comandos de *gravação* por vez, embora um alocador de comando possa ser usado para criar qualquer número de objetos [**GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) .

Para recuperar a memória alocada por um alocador de comando, um aplicativo chama [**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset). Isso permite que o alocador seja reutilizado para novos comandos, mas não reduzirá seu tamanho subjacente. Mas antes de fazer isso, o aplicativo deve verificar se a GPU não está mais executando nenhuma lista de comandos associada ao alocador; caso contrário, a chamada falhará. Além disso, observe que essa API não tem threads livres e, portanto, não pode ser chamada no mesmo alocador ao mesmo tempo de vários threads.

### <a name="id3d12pipelinestate"></a>ID3D12PipelineState

O estado inicial do pipeline para a lista de comandos. No Microsoft Direct3D 12, a maioria dos Estados de pipeline de gráficos é definida dentro de uma lista de comandos usando o objeto [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) . Um aplicativo criará um grande número deles, normalmente durante a inicialização do aplicativo e, em seguida, o estado será atualizado alterando o objeto de estado atualmente associado usando [**ID3D12GraphicsCommandList:: Setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate). Para obter mais informações sobre objetos de estado do pipeline, consulte [Gerenciando o estado do pipeline de gráficos no Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

Observe que os grupos não herdam o estado do pipeline definido por chamadas anteriores nas listas de comandos diretos que são seus pais.

Se esse parâmetro for NULL, um estado padrão será usado.

## <a name="recording-command-lists"></a>Registrando listas de comandos

Imediatamente após a criação, as listas de comandos estão no estado de gravação. Você também pode usar novamente uma lista de comandos existente chamando I [**D3D12GraphicsCommandList:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset), que também deixa a lista de comandos no estado de gravação. Ao contrário de [**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset), você pode chamar **Reset** enquanto a lista de comandos ainda está sendo executada. Um padrão típico é enviar uma lista de comandos e redefini-la imediatamente para reutilizar a memória alocada para outra lista de comandos. Observe que apenas uma lista de comandos associada a cada alocador de comando pode estar em um estado de gravação ao mesmo tempo.

Quando uma lista de comandos está no estado de gravação, basta chamar métodos da interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) para adicionar comandos à lista. Muitos desses métodos habilitam a funcionalidade Direct3D comum que será familiar para os desenvolvedores do Microsoft Direct3D 11; outras APIs são novas para o Direct3D 12.

Depois de adicionar comandos à lista de comandos, você faz a transição da lista de comandos para fora do estado de gravação chamando [**Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).

Os alocadores de comando podem crescer, mas não reduzir o pool e reutilizar os alocadores devem ser considerados para maximizá a eficiência do seu aplicativo. Você pode gravar várias listas no mesmo alocador antes que ele seja redefinido, desde que apenas uma lista esteja gravando em um determinado alocador ao mesmo tempo. Você pode visualizar cada lista como proprietária de uma parte do alocador que indica o que [**ID3D12CommandQueue:: ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) será executado.

Uma estratégia de pooling de alocador simples deve ser direcionada para aproximadamente `numCommandLists * MaxFrameLatency` alocadores. Por exemplo, se você registrar 6 listas e permitir até três quadros latentes, poderá esperar 18-20 alocadores. Uma estratégia de Pooling mais avançada, que reutiliza os alocadores para várias listas no mesmo thread, pode visar `numRecordingThreads * MaxFrameLatency` alocadores. Usando o exemplo anterior, se duas listas tiverem sido registradas no thread A, 2 no thread B, 1 no thread C e 1 no thread D, você poderá direcionar Realistamente para os alocadores 12-14.

Use uma cerca para determinar quando um determinado alocador pode ser reutilizado.

Como as listas de comandos podem ser imediatamente redefinidas após a execução, elas podem ser agrupadas de forma trivial, adicionando-as de volta ao pool após cada chamada para [**ID3D12CommandQueue:: ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

## <a name="example"></a>Exemplo

Os trechos de código a seguir ilustram a criação e a gravação de uma lista de comandos. Observe que este exemplo inclui os seguintes recursos do Direct3D 12:

-   Objetos de estado do pipeline-são usados para definir a maioria dos parâmetros de estado do pipeline de renderização de dentro de uma lista de comandos. Para obter mais informações, consulte [Gerenciando o estado do pipeline de gráficos no Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).
-   Heap de descritores-os aplicativos usam heaps de descritor para gerenciar a associação de pipeline para recursos de memória.
-   Barreira de recursos – é usada para gerenciar a transição de recursos de um estado para outro, como de uma exibição de destino de renderização para uma exibição de recurso de sombreador. Para obter mais informações, consulte [usando barreiras de recursos para sincronizar Estados de recursos](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

Por exemplo,


```C++
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



Depois que uma lista de comandos tiver sido criada e registrada, ela poderá ser executada usando uma fila de comandos. Para obter mais informações, consulte [executando e sincronizando listas de comandos](executing-and-synchronizing-command-lists.md).

## <a name="reference-counting"></a>Contagem de referência

A maioria das APIs D3D12 continuam a usar a contagem de referência seguindo as convenções COM. Uma exceção notável a isso são as APIs da lista de comandos do D3D12 Graphics. Todas as APIs em [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) não mantêm referências aos objetos passados para essas APIs. Isso significa que os aplicativos são responsáveis por garantir que uma lista de comandos nunca seja enviada para execução que faça referência a um recurso destruído.

## <a name="command-list-errors"></a>Erros de lista de comandos

A maioria das APIs em [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) não retorna erros. Erros encontrados durante a criação da lista de comandos são adiados até [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close). A única exceção é o \_ \_ dispositivo de erro dxgi \_ removido, o que é adiado ainda mais. Observe que isso é diferente de D3D11, em que muitos erros de validação de parâmetro são silenciosamente descartados e nunca retornados ao chamador.

Os aplicativos podem esperar ver \_ erros removidos do dispositivo dxgi \_ nas seguintes chamadas à API:

-   Qualquer método de criação de recursos
-   [**ID3D12Resource:: map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)
-   [**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**GetDeviceRemovedReason**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)

## <a name="command-list-api-restrictions"></a>Restrições de API da lista de comandos

Algumas APIs de lista de comandos só podem ser chamadas em determinados tipos de listas de comandos. A tabela a seguir mostra quais APIs de lista de comandos são válidas para chamar em cada tipo de lista de comandos. Ele também mostra quais APIs são válidas para chamar em uma [**passagem de renderização D3D12**](./direct3d-12-render-passes.md). 

| Nome da API                                         | Gráficos | Computação | Copiar | Pacote | Em processamento aprovado |
|--------------------------------------------------|:--------:|:-------:|:----:|:------:|:--------------:|
| AtomicCopyBufferUINT                             | ✓        | ✓       | ✓    |        |                |
| AtomicCopyBufferUINT64                           | ✓        | ✓       | ✓    |        |                |
| BeginQuery                                       | ✓        |         |      |        | ✓              |
| BeginRenderPass                                  | ✓        |         |      |        |                |
| BuildRaytracingAccelerationStructure             | ✓        | ✓       |      |        |                |
| ClearDepthStencilView                            | ✓        |         |      |        |                |
| ClearRenderTargetView                            | ✓        |         |      |        |                |
| ClearState                                       | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewFloat                    | ✓        | ✓       |      |        |                |
| ClearUnorderedAccessViewUint                     | ✓        | ✓       |      |        |                |
| CopyBufferRegion                                 | ✓        | ✓       | ✓    |        |                |
| CopyRaytracingAccelerationStructure              | ✓        | ✓       |      |        |                |
| CopyResource                                     | ✓        | ✓       | ✓    |        |                |
| CopyTextureRegion                                | ✓        | ✓       | ✓    |        |                |
| CopyTiles                                        | ✓        | ✓       | ✓    |        |                |
| DiscardResource                                  | ✓        | ✓       |      |        |                |
| Dispatch                                         | ✓        | ✓       |      | ✓      |                |
| DispatchRays                                     | ✓        | ✓       |      | ✓      |                |
| DrawIndexedInstanced                             | ✓        |         |      | ✓      | ✓              |
| DrawInstanced                                    | ✓        |         |      | ✓      | ✓              |
| EmitRaytracingAccelerationStructurePostbuildInfo | ✓        | ✓       |      |        |                |
| EndQuery                                         | ✓        | ✓       | ✓    |        | ✓              |
| EndRenderPass                                    | ✓        |         |      |        | ✓              |
| ExecuteBundle                                    | ✓        |         |      |        | ✓              |
| ExecuteIndirect                                  | ✓        | ✓       |      | ✓      | ✓              |
| ExecuteMetaCommand                               | ✓        | ✓       |      |        |                |
| IASetIndexBuffer                                 | ✓        |         |      | ✓      | ✓              |
| IASetPrimitiveTopology                           | ✓        |         |      | ✓      | ✓              |
| IASetVertexBuffers                               | ✓        |         |      | ✓      | ✓              |
| InitializeMetaCommand                            | ✓        | ✓       |      |        |                |
| OMSetBlendFactor                                 | ✓        |         |      | ✓      | ✓              |
| OMSetDepthBounds                                 | ✓        |         |      | ✓      | ✓              |
| OMSetRenderTargets                               | ✓        |         |      |        |                |
| OMSetStencilRef                                  | ✓        |         |      | ✓      | ✓              |
| ResolveQueryData                                 | ✓        | ✓       | ✓    |        |                |
| ResolveSubresource                               | ✓        |         |      |        |                |
| ResolveSubresourceRegion                         | ✓        |         |      |        |                |
| ResourceBarrier                                  | ✓        | ✓       | ✓    |        | ✓              |
| RSSetScissorRects                                | ✓        |         |      |        | ✓              |
| RSSetShadingRate                                 | ✓        |         |      | ✓      | ✓              |
| RSSetShadingRateImage                            | ✓        |         |      | ✓      | ✓              |
| RSSetViewports                                   | ✓        |         |      |        | ✓              |
| SetComputeRoot32BitConstant                      | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRoot32BitConstants                     | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootConstantBufferView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootDescriptorTable                    | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootShaderResourceView                 | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootSignature                          | ✓        | ✓       |      | ✓      | ✓              |
| SetComputeRootUnorderedAccessView                | ✓        | ✓       |      | ✓      | ✓              |
| SetDescriptorHeaps                               | ✓        | ✓       |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstant                     | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRoot32BitConstants                    | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootConstantBufferView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootDescriptorTable                   | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootShaderResourceView                | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootSignature                         | ✓        |         |      | ✓      | ✓              |
| SetGraphicsRootUnorderedAccessView               | ✓        |         |      | ✓      | ✓              |
| SetPipelineState                                 | ✓        | ✓       |      | ✓      | ✓              |
| SetPipelineState1                                | ✓        | ✓       |      | ✓      |                |
| SetPredication                                   | ✓        | ✓       |      |        | ✓              |
| SetProtectedResourceSession                      | ✓        | ✓       | ✓    |        |                |
| SetSamplePositions                               | ✓        |         |      | ✓      | ✓              |
| SetViewInstanceMask                              | ✓        |         |      | ✓      | ✓              |
| SOSetTargets                                     | ✓        |         |      |        | ✓              |
| WriteBufferImmediate                             | ✓        | ✓       | ✓    | ✓      | ✓              |

## <a name="bundle-restrictions"></a>Restrições de pacote

As restrições permitem que os drivers do Direct3D 12 façam a maior parte do trabalho associado aos pacotes no momento do registro, permitindo que a API do [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) seja executada com baixa sobrecarga. Todos os objetos de estado de pipeline referenciados por um pacote devem ter os mesmos formatos de destino de renderização, formato de buffer de profundidade e descrições de exemplo.

As seguintes chamadas à API de lista de comandos não são permitidas em listas de comandos criadas com o tipo: D3D12 \_ grupo de tipos de lista de comando \_ \_ \_ :

-   Qualquer método claro
-   Qualquer método de cópia
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
-   [**ResolveSubresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)
-   [**BeginQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
-   [**EndQuery**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
-   [**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)
-   [**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
-   [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)
-   [**RSSetScissorRects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)

[**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) pode ser chamado em um pacote, mas os heaps do descritor de pacote devem corresponder ao heap do descritor de lista de comandos de chamada.

Se qualquer uma dessas APIs for chamada em um pacote, o tempo de execução descartará a chamada. A camada de depuração emitirá um erro sempre que isso ocorrer.

## <a name="related-topics"></a>Tópicos relacionados

[Envio de trabalho no Direct3D 12](command-queues-and-command-lists.md)