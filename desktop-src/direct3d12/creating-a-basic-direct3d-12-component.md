---
title: Criando um componente básico do Direct3D 12
description: Este tópico descreve o fluxo de chamadas para criar um componente básico do Direct3D 12.
ms.assetid: A0FB108B-15C1-42AD-9277-D5CB63FA8329
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: d0c7ead9ce67ee23a0668304a006d6cd67fb3d67
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "104758856"
---
# <a name="creating-a-basic-direct3d-12-component"></a>Criando um componente básico do Direct3D 12

> [!NOTE]
> Consulte o repositório [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) para exemplos de gráficos do DirectX 12 que demonstram como criar aplicativos com uso intensivo de gráficos para o Windows 10.

Este tópico descreve o fluxo de chamadas para criar um componente básico do Direct3D 12.

-   [Fluxo de código para um aplicativo simples](#code-flow-for-a-simple-app)
    -   [Inicializar](#initialize)
    -   [Atualizar](#update)
    -   [Render](#render)
    -   [Destruir](#destroy)
-   [Exemplo de código para um aplicativo simples](#code-example-for-a-simple-app)
    -   [D3D12HelloTriangle de classe](#class-d3d12hellotriangle)
    -   [OnInit ()](#oninit)
    -   [LoadPipe ()](#loadpipeline)
    -   [Loadassets ()](#loadassets)
    -   [OnUpdate ()](#onupdate)
    -   [OnRender ()](#onrender)
    -   [PopulateCommandList()](#populatecommandlist)
    -   [WaitForPreviousFrame()](#waitforpreviousframe)
    -   [OnDestroy ()](#ondestroy)
-   [Tópicos relacionados](#related-topics)

## <a name="code-flow-for-a-simple-app"></a>Fluxo de código para um aplicativo simples

O loop mais externo de um programa do D3D 12 segue um processo gráfico muito padrão:

> [!TIP]
> Os recursos novos para o Direct3D 12 são seguidos de uma observação.

-   [Inicializar](#initialize)
-   **Pete**
    -   [Atualizar](#update)
    -   [Render](#render)
-   [Destruir](#destroy)

### <a name="initialize"></a>Inicializar

A inicialização envolve primeiro a configuração das variáveis e das classes globais, e uma função de inicialização deve preparar o pipeline e os ativos.

-   Inicialize o pipeline.
    -   Habilite a camada de depuração.
    -   Crie o dispositivo.
    -   Crie a fila de comandos.
    -   Crie a cadeia de permuta.
    -   Criar um heap de descritor de RTV (exibição de destino de renderização).
        > [!Note]  
        > Um [heap de descritor](descriptor-heaps.md) pode ser considerado como uma matriz [de descritores.](descriptors.md) Onde cada descritor descreve totalmente um objeto para a GPU.

    -   Crie recursos de quadro (uma exibição de destino de renderização para cada quadro).
    -   Crie um alocador de comando.
        > [!Note]  
        > Um alocador de comando gerencia o armazenamento subjacente para [listas de comandos e pacotes](recording-command-lists-and-bundles.md).
         
-   Inicialize os ativos.
    -   Crie uma assinatura raiz vazia.
        > [!Note]  
        > Uma [assinatura raiz](root-signatures.md) gráfica define quais recursos estão associados ao pipeline de gráficos.

    -   Compile os sombreadores.
    -   Crie o layout de entrada do vértice.
    -   Crie uma descrição de [objeto de estado de pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) e crie o objeto.
        > [!Note]  
        > Um objeto de estado de pipeline mantém o estado de todos os sombreadores definidos atualmente, bem como determinados objetos de estado de função fixa (como o *Assembler de entrada*, *tesselator*, *rasterizador* e *mesclagem de saída*).

    -   Crie a lista de comandos.
    -   Feche a lista de comandos.
    -   Crie e carregue os buffers de vértice.
    -   Crie as exibições do buffer de vértice.
    -   Criar uma cerca.
        > [!Note]  
        > Uma cerca é usada para sincronizar a CPU com a GPU (consulte [sincronização de vários mecanismos](./user-mode-heap-synchronization.md)).

    -   Crie um identificador de evento.
    -   Aguarde a conclusão da GPU.
        > [!Note]  
        > Verifique o limite.

Consulte a [classe D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [Loadcanalization](#loadpipeline) e [loadassets](#loadassets).

### <a name="update"></a>Atualizar

Atualizar tudo o que deve ser alterado desde o último quadro.

-   Modifique a constante, o vértice, os buffers de índice e todo o resto, conforme necessário.

Consulte [OnUpdate](#onupdate).

### <a name="render"></a>Renderizar

Desenhe o novo mundo.

-   Preencha a lista de comandos.
    -   Redefina o alocador de lista de comandos.
        > [!Note]  
        > Use novamente a memória associada ao alocador de comando.

         

    -   Redefina a lista de comandos.
    -   Defina a assinatura raiz de gráficos.
        > [!Note]  
        > Define a assinatura raiz de gráficos a ser usada para a lista de comandos atual.

         

    -   Defina os retângulos de visor e de mola.
    -   Defina uma barreira de recurso, indicando que o buffer de fundo deve ser usado como um destino de renderização.
        > [!Note]  
        > As barreiras de recursos são usadas para gerenciar transições de recursos.

         

    -   Grave os comandos na lista de comandos.
    -   Indique que o buffer de fundo será usado para apresentar após a execução da lista de comandos.
        > [!Note]  
        > Outra chamada para definir uma barreira de recurso.

         

    -   Feche a lista de comandos para gravar mais.
-   Execute a lista de comandos.
-   Apresente o quadro.
-   Aguarde a conclusão da GPU.
    > [!Note]  
    > Continue atualizando e verificando a cerca.

Consulte [OnRender](#onrender).

### <a name="destroy"></a>Destruir

Fechar o aplicativo corretamente.

-   Aguarde a conclusão da GPU.
    > [!Note]  
    > Verificação final da cerca.

-   Feche o identificador de evento.

Consulte [OnDestroy](#ondestroy).

## <a name="code-example-for-a-simple-app"></a>Exemplo de código para um aplicativo simples

O seguinte expande o fluxo de código acima para incluir o código necessário para um exemplo básico.

### <a name="class-d3d12hellotriangle"></a>D3D12HelloTriangle de classe

Primeiro, defina a classe em um arquivo de cabeçalho, incluindo um visor, um retângulo de recorte e um buffer de vértice usando as estruturas:

-   [**\_Visor D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [**D3D12 \_ Rect**](d3d12-rect.md)
-   [**\_Exibição do \_ buffer de vértice D3D12 \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

```cpp
#include "DXSample.h"

using namespace DirectX;
using namespace Microsoft::WRL;

class D3D12HelloTriangle : public DXSample
{
public:
    D3D12HelloTriangle(UINT width, UINT height, std::wstring name);

    virtual void OnInit();
    virtual void OnUpdate();
    virtual void OnRender();
    virtual void OnDestroy();

private:
    static const UINT FrameCount = 2;

    struct Vertex
    {
        XMFLOAT3 position;
        XMFLOAT4 color;
    };

    // Pipeline objects.
    D3D12_VIEWPORT m_viewport;
    D3D12_RECT m_scissorRect;
    ComPtr<IDXGISwapChain3> m_swapChain;
    ComPtr<ID3D12Device> m_device;
    ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
    ComPtr<ID3D12CommandAllocator> m_commandAllocator;
    ComPtr<ID3D12CommandQueue> m_commandQueue;
    ComPtr<ID3D12RootSignature> m_rootSignature;
    ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
    ComPtr<ID3D12PipelineState> m_pipelineState;
    ComPtr<ID3D12GraphicsCommandList> m_commandList;
    UINT m_rtvDescriptorSize;

    // App resources.
    ComPtr<ID3D12Resource> m_vertexBuffer;
    D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;

    // Synchronization objects.
    UINT m_frameIndex;
    HANDLE m_fenceEvent;
    ComPtr<ID3D12Fence> m_fence;
    UINT64 m_fenceValue;

    void LoadPipeline();
    void LoadAssets();
    void PopulateCommandList();
    void WaitForPreviousFrame();
};
```

### <a name="oninit"></a>OnInit ()

No arquivo de origem principal dos projetos, comece inicializando os objetos:

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a>LoadPipe ()

O código a seguir cria as noções básicas para um pipeline de gráficos. O processo de criação de dispositivos e cadeias de troca é muito semelhante ao Direct3D 11.

-   Habilite a camada de depuração, com chamadas para:<dl>

[**D3D12GetDebugInterface**](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [**ID3D12Debug::EnableDebugLayer**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   Crie o dispositivo:<dl>

[**CreateDXGIFactory1**](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   Preencha uma descrição da fila de comandos e crie a fila de comandos:<dl>

[**D3D12 \_ de \_ fila de comando \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [**ID3D12Device::CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   Preencha uma descrição de SwapChain e crie a cadeia de permuta: <dl>

[**\_desc de \_ cadeia de permuta dxgi \_**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [**IDXGIFactory::CreateSwapChain**](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   Preencha uma descrição de heap. em seguida, crie um heap de descritor: <dl>

[**D3D12 de \_ heap de descritor \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [**ID3D12Device::CreateDescriptorHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   Criar o modo de exibição de destino de renderização: <dl>

[**\_Identificador do \_ descritor de CPU CD3DX12 \_**](cd3dx12-cpu-descriptor-handle.md)  
    [**GetCPUDescriptorHandleForHeapStart**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**IDXGISwapChain::GetBuffer**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [**ID3D12Device::CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   Crie o alocador de comando: [**ID3D12Device:: CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).

Em etapas posteriores, as listas de comandos são obtidas do alocador de comandos e enviadas à fila de comandos.

Carregue as dependências do pipeline de renderização (Observe que a criação de um dispositivo de detorção de software é totalmente opcional).


```cpp
void D3D12HelloTriangle::LoadPipeline()
{
#if defined(_DEBUG)
    // Enable the D3D12 debug layer.
    {
        
        ComPtr<ID3D12Debug> debugController;
        if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&debugController))))
        {
            debugController->EnableDebugLayer();
        }
    }
#endif

    ComPtr<IDXGIFactory4> factory;
    ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&factory)));

    if (m_useWarpDevice)
    {
        ComPtr<IDXGIAdapter> warpAdapter;
        ThrowIfFailed(factory->EnumWarpAdapter(IID_PPV_ARGS(&warpAdapter)));

        ThrowIfFailed(D3D12CreateDevice(
            warpAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }
    else
    {
        ComPtr<IDXGIAdapter1> hardwareAdapter;
        GetHardwareAdapter(factory.Get(), &hardwareAdapter);

        ThrowIfFailed(D3D12CreateDevice(
            hardwareAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }

    // Describe and create the command queue.
    D3D12_COMMAND_QUEUE_DESC queueDesc = {};
    queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
    queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

    ThrowIfFailed(m_device->CreateCommandQueue(&queueDesc, IID_PPV_ARGS(&m_commandQueue)));

    // Describe and create the swap chain.
    DXGI_SWAP_CHAIN_DESC swapChainDesc = {};
    swapChainDesc.BufferCount = FrameCount;
    swapChainDesc.BufferDesc.Width = m_width;
    swapChainDesc.BufferDesc.Height = m_height;
    swapChainDesc.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
    swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
    swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_DISCARD;
    swapChainDesc.OutputWindow = Win32Application::GetHwnd();
    swapChainDesc.SampleDesc.Count = 1;
    swapChainDesc.Windowed = TRUE;

    ComPtr<IDXGISwapChain> swapChain;
    ThrowIfFailed(factory->CreateSwapChain(
        m_commandQueue.Get(),        // Swap chain needs the queue so that it can force a flush on it.
        &swapChainDesc,
        &swapChain
        ));

    ThrowIfFailed(swapChain.As(&m_swapChain));

    // This sample does not support fullscreen transitions.
    ThrowIfFailed(factory->MakeWindowAssociation(Win32Application::GetHwnd(), DXGI_MWA_NO_ALT_ENTER));

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();

    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
            rtvHandle.Offset(1, m_rtvDescriptorSize);
        }
    }

    ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
}
```



### <a name="loadassets"></a>Loadassets ()

O carregamento e a preparação de ativos é um processo longo. Muitos desses estágios são semelhantes ao D3D 11, embora alguns sejam novos no D3D 12.

No Direct3D 12, o estado de pipeline necessário é anexado a uma lista de comandos por meio de um PSO ( [objeto de estado de pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) ). Este exemplo mostra como criar um PSO. Você pode armazenar o PSO como uma variável de membro e reutilizá-lo quantas vezes forem necessárias.

Um heap de descritores define as exibições e como acessar recursos (por exemplo, uma exibição de destino de renderização).

Com a lista de comandos alocador e PSO, você pode criar a lista de comandos real, que será executada posteriormente.

As seguintes APIs e processos são chamados sucessivamente.

-   Crie uma assinatura raiz vazia usando a estrutura auxiliar disponível: <dl>

[**Desc. de \_ assinatura raiz CD3DX12 \_ \_**](cd3dx12-root-signature-desc.md)  
    [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [**ID3D12Device::CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   Carregue e compile os sombreadores: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).
-   Crie o layout de entrada do vértice: [**\_ elemento de entrada D3D12 \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).
-   Preencha uma descrição do estado do pipeline, usando as estruturas auxiliares disponíveis e, em seguida, crie o estado do pipeline de gráficos: <dl>

[**Desc. de estado do pipeline de \_ gráficos D3D12 \_ \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [**CD3DX12 do \_ rasterizador \_ desc**](cd3dx12-rasterizer-desc.md)  
    [**CD3DX12 de \_ combinação \_ desc**](cd3dx12-blend-desc.md)  
    [**ID3D12Device::CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   Criar e fechar uma lista de comandos: <dl>

[**ID3D12Device:: createcommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [**ID3D12GraphicsCommandList:: fechar**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   Crie o buffer de vértice: [**ID3D12Device:: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).
-   Copie os dados de vértice para o buffer de vértice:<dl>

[**ID3D12Resource:: map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [**ID3D12Resource:: mapeamento**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   Inicialize a exibição do buffer de vértice: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).
-   Crie e inicialize a cerca: [**ID3D12Device:: createfence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).
-   Crie um identificador de evento para usar com a sincronização de quadros.
-   Aguarde a conclusão da GPU.


```cpp
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
        CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_UPLOAD);
        auto desc = CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize);
        ThrowIfFailed(m_device->CreateCommittedResource(
            &heapProps,
            D3D12_HEAP_FLAG_NONE,
            &desc,
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



### <a name="onupdate"></a>OnUpdate ()

Para um exemplo simples, nada é atualizado.


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a>OnRender ()

Durante a configuração, a variável de membro **m \_ commandlist** foi usada para registrar e executar todos os comandos set up. Agora você pode reutilizar esse membro no loop de renderização principal.

A renderização envolve uma chamada para popular a lista de comandos e, em seguida, a lista de comandos pode ser executada e o próximo buffer na cadeia de troca apresentada:

-   Preencha a lista de comandos.
-   Execute a lista de comandos: [**ID3D12CommandQueue:: ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).
-   [**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) o quadro.
-   Aguarde a conclusão da GPU.


```cpp
void D3D12HelloTriangle::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(1, 0));

    WaitForPreviousFrame();
}
```



### <a name="populatecommandlist"></a>PopulateCommandList()

Você deve redefinir o alocador de lista de comandos e a própria lista de comandos antes de poder reutilizá-los. Em cenários mais avançados, pode fazer sentido redefinir o alocador a cada vários quadros. A memória é associada ao alocador que não pode ser liberado imediatamente após a execução de uma lista de comandos. Este exemplo mostra como redefinir o alocador após cada quadro.

Agora, reutilize a lista de comandos para o quadro atual. Reanexe o visor à lista de comandos (que deve ser feito sempre que uma lista de comandos for redefinida e antes da execução da lista de comandos), indique que o recurso estará em uso como um destino de renderização, registre comandos e, em seguida, indique que o destino de renderização será usado para apresentar quando a execução da lista de comandos for concluída.

A população de listas de comandos chama os seguintes métodos e processos por sua vez:

-   Redefina o alocador de comando e a lista de comandos: <dl>

[**ID3D12CommandAllocator:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [**ID3D12GraphicsCommandList:: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   Defina os retângulos de assinatura raiz, visor e tesoura: <dl>

[**ID3D12GraphicsCommandList::SetGraphicsRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [**ID3D12GraphicsCommandList::RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [**ID3D12GraphicsCommandList::RSSetScissorRects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   Indique que o buffer de fundo deve ser usado como um destino de renderização: <dl>

[**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   Registre os comandos:<dl>

[**ID3D12GraphicsCommandList::ClearRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [**ID3D12GraphicsCommandList::IASetPrimitiveTopology**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [**ID3D12GraphicsCommandList::D rawInstanced**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   Indique que o buffer de fundo agora será usado para apresentar: [**ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).
-   Feche a lista de comandos: [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).


```cpp
void D3D12HelloTriangle::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocator->Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
    m_commandList->RSSetViewports(1, &m_viewport);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
    m_commandList->ResourceBarrier(1, &barrier);

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->DrawInstanced(3, 1, 0, 0);

    // Indicate that the back buffer will now be used to present.
    barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
    m_commandList->ResourceBarrier(1, &barrier);

    ThrowIfFailed(m_commandList->Close());
}
```



### <a name="waitforpreviousframe"></a>WaitForPreviousFrame()

O código a seguir mostra um uso supersimplificado de limites.

> [!Note]  
> Aguardar a conclusão de um quadro é muito ineficiente para a maioria dos aplicativos.

 

As seguintes APIs e processos são chamados na ordem:

-   [**ID3D12CommandQueue:: Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [**ID3D12Fence:: getcompletedvalue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [**ID3D12Fence::SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   Aguarde o evento.
-   Atualize o índice do quadro: [**IDXGISwapChain3:: GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).


```cpp
void D3D12HelloTriangle::WaitForPreviousFrame()
{
    // WAITING FOR THE FRAME TO COMPLETE BEFORE CONTINUING IS NOT BEST PRACTICE.
    // This is code implemented as such for simplicity. More advanced samples 
    // illustrate how to use fences for efficient resource usage.

    // Signal and increment the fence value.
    const UINT64 fence = m_fenceValue;
    ThrowIfFailed(m_commandQueue->Signal(m_fence.Get(), fence));
    m_fenceValue++;

    // Wait until the previous frame is finished.
    if (m_fence->GetCompletedValue() < fence)
    {
        ThrowIfFailed(m_fence->SetEventOnCompletion(fence, m_fenceEvent));
        WaitForSingleObject(m_fenceEvent, INFINITE);
    }

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();
}
```



### <a name="ondestroy"></a>OnDestroy ()

Fechar o aplicativo corretamente.

-   Aguarde a conclusão da GPU.
-   Feche o evento.


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Entendendo o Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Exemplos de trabalho](working-samples.md)
</dt> </dl>

 

 
