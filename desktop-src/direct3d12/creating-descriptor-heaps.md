---
title: Como criar heaps de descritores
description: Para criar e configurar um heap de descritor, você deve selecionar um tipo de heap de descritor, determinar quantos descritores ele contém e definir sinalizadores que indiquem se a CPU está visível e/ou sombreador visível.
ms.assetid: 58677023-692C-4BA4-90B7-D568F3DD3F73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d21d462dd393360e9ebfcb07ab5b35524b9d8d8c01c8ab1ef28ef90166eb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857986"
---
# <a name="creating-descriptor-heaps"></a>Como criar heaps de descritores

Para criar e configurar um heap de descritor, você deve selecionar um tipo de heap de descritor, determinar quantos descritores ele contém e definir sinalizadores que indiquem se a CPU está visível e/ou sombreador visível.

-   [Tipos de heap de descritores](#descriptor-heap-types)
-   [Propriedades do heap do descritor](#descriptor-heap-properties)
-   [Identificadores de descritor](#descriptor-handles)
-   [Métodos de heap de descritores](#descriptor-heap-methods)
-   [Wrapper de heap de descritor mínimo](#minimal-descriptor-heap-wrapper)
-   [Tópicos relacionados](#related-topics)

## <a name="descriptor-heap-types"></a>Tipos de heap de descritores

O tipo de heap é determinado por um membro da enumeração [**do \_ \_ \_ tipo de heap do descritor D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) :

``` syntax
typedef enum D3D12_DESCRIPTOR_HEAP_TYPE
{
    D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV,    // Constant buffer/Shader resource/Unordered access views
    D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER,        // Samplers
    D3D12_DESCRIPTOR_HEAP_TYPE_RTV,            // Render target view
    D3D12_DESCRIPTOR_HEAP_TYPE_DSV,            // Depth stencil view
    D3D12_DESCRIPTOR_HEAP_TYPE_NUM_TYPES       // Simply the number of descriptor heap types
} D3D12_DESCRIPTOR_HEAP_TYPE;
```

## <a name="descriptor-heap-properties"></a>Propriedades do heap do descritor

As propriedades de heap são definidas na estrutura [**\_ desc de \_ heap \_ do descritor D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) , que faz referência ao [**\_ tipo de \_ heap \_ do descritor D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type) e aos [**\_ sinalizadores de \_ heap \_ do descritor de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags) .

O sinalizador do sinalizador heap do descritor de D3D12 da bandeira \_ \_ \_ \_ \_ visível pode, opcionalmente, ser definido em um heap de descritor para indicar que ele está associado em uma lista de comandos para referência por sombreadores. Heaps de descritores criados *sem* esse sinalizador permitem aos aplicativos a opção de preparar os descritores na memória da CPU antes de copiá-los para um heap de descritor visível do sombreador, como uma conveniência. Mas também é bom para que os aplicativos criem descritores diretamente em heaps de descritores visíveis de sombreador sem nenhum requisito para preparar qualquer coisa na CPU.

Esse sinalizador só se aplica a CBV, SRV, UAV e amostras. Ele não se aplica a outros tipos de heap de descritor, pois os sombreadores não fazem referência direta a outros tipos.

Por exemplo, descreva e crie um heap de descritor de amostra.


```C++
// Describe and create a sampler descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC samplerHeapDesc = {};
samplerHeapDesc.NumDescriptors = 1;
samplerHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER;
samplerHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&samplerHeapDesc, IID_PPV_ARGS(&m_samplerHeap)));
```



Descrever e criar uma CBV (exibição de buffer constante), SRV (modo de exibição de recursos de sombreamento) e heap de descritor de UAV (exibição de acesso não ordenado).


```C++
// Describe and create a shader resource view (SRV) and unordered
// access view (UAV) descriptor heap.
D3D12_DESCRIPTOR_HEAP_DESC srvUavHeapDesc = {};
srvUavHeapDesc.NumDescriptors = DescriptorCount;
srvUavHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
srvUavHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;
ThrowIfFailed(m_device->CreateDescriptorHeap(&srvUavHeapDesc, IID_PPV_ARGS(&m_srvUavHeap)));

m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
m_srvUavDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV);
```



## <a name="descriptor-handles"></a>Identificadores de descritor

As estruturas do [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) e do [**\_ \_ descritor \_ de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) identificam descritores específicos em um heap de descritor. Um identificador é um pouco como um ponteiro, mas o aplicativo não deve desreferenciá-lo manualmente; caso contrário, o comportamento será indefinido. O uso dos identificadores deve passar pela API. Um identificador em si pode ser copiado livremente ou passado para APIs que operam nos descritores de/usam. Não há nenhuma contagem de referência, portanto, o aplicativo deve garantir que ele não use um identificador depois que o heap de descritor subjacente tiver sido excluído.

Os aplicativos podem descobrir o tamanho de incremento dos descritores para um determinado tipo de heap de descrição, para que eles possam gerar identificadores para qualquer local em um heap de descritor manualmente, começando do identificador até a base. Os aplicativos nunca devem codificar os tamanhos de incremento de identificador de descritor e devem sempre consultá-los para uma determinada instância de dispositivo; caso contrário, o comportamento será indefinido. Os aplicativos também não devem usar os tamanhos e os identificadores de incremento para fazer seu próprio exame ou manipulação de dados de heap de descritor, pois os resultados dessa tarefa são indefinidos. Os identificadores podem não ser realmente usados como ponteiros, mas também como proxies para ponteiros para evitar a desreferenciação acidental.

> [!Note]
>
> Há uma estrutura auxiliar, o \_ \_ identificador do descritor de GPU CD3DX12 \_ , definido no cabeçalho d3dx12. h, que herda a estrutura de [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) e fornece inicialização e outras operações úteis. Da mesma forma, a \_ \_ estrutura auxiliar do identificador do descritor de CPU CD3DX12 \_ é definida para a estrutura de [**\_ \_ \_ identificador do descritor de CPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)

 

Ambas as estruturas auxiliares são usadas ao preencher as listas de comandos.


```C++
// Fill the command list with all the render commands and dependent state.
void D3D12nBodyGravity::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated
    // command lists have finished execution on the GPU; apps should use
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocators[m_frameIndex]->Reset());

    // However, when ExecuteCommandList() is called on a particular command
    // list, that command list can then be reset at any time and must be before
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocators[m_frameIndex].Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetPipelineState(m_pipelineState.Get());
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

    m_commandList->SetGraphicsRootConstantBufferView(RootParameterCB, m_constantBufferGS->GetGPUVirtualAddress() + m_frameIndex * sizeof(ConstantBufferGS));

    ID3D12DescriptorHeap* ppHeaps[] = { m_srvUavHeap.Get() };
    m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_POINTLIST);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.0f, 0.1f, 0.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);

    // Render the particles.
    float viewportHeight = static_cast<float>(static_cast<UINT>(m_viewport.Height) / m_heightInstances);
    float viewportWidth = static_cast<float>(static_cast<UINT>(m_viewport.Width) / m_widthInstances);
    for (UINT n = 0; n < ThreadCount; n++)
    {
        const UINT srvIndex = n + (m_srvIndex[n] == 0 ? SrvParticlePosVelo0 : SrvParticlePosVelo1);

        D3D12_VIEWPORT viewport;
        viewport.TopLeftX = (n % m_widthInstances) * viewportWidth;
        viewport.TopLeftY = (n / m_widthInstances) * viewportHeight;
        viewport.Width = viewportWidth;
        viewport.Height = viewportHeight;
        viewport.MinDepth = D3D12_MIN_DEPTH;
        viewport.MaxDepth = D3D12_MAX_DEPTH;
        m_commandList->RSSetViewports(1, &viewport);

        CD3DX12_GPU_DESCRIPTOR_HANDLE srvHandle(m_srvUavHeap->GetGPUDescriptorHandleForHeapStart(), srvIndex, m_srvUavDescriptorSize);
        m_commandList->SetGraphicsRootDescriptorTable(RootParameterSRV, srvHandle);

        m_commandList->DrawInstanced(ParticleCount, 1, 0, 0);
    }

    m_commandList->RSSetViewports(1, &m_viewport);

    // Indicate that the back buffer will now be used to present.
    m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_commandList->Close());
}
```



## <a name="descriptor-heap-methods"></a>Métodos de heap de descritores

Heaps de descritores ([**ID3D12DescriptorHeap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap)) herdam de [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable). Isso impõe a responsabilidade do gerenciamento de residência de heaps de descritores em aplicativos, assim como heaps de recursos. Os métodos de gerenciamento de residência se aplicam somente a heaps visíveis do sombreador, já que os heaps visíveis sem sombreador não são visíveis diretamente para a GPU.

O método [**ID3D12Device:: GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize) permite que os aplicativos recompensem manualmente os identificadores em um heap (produzindo identificadores em qualquer lugar em um heap de descritor). O identificador do local de início do heap vem de [**ID3D12DescriptorHeap:: GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) / [**ID3D12DescriptorHeap:: GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart). O deslocamento é feito adicionando o tamanho de incremento que \* o número de descritores deve deslocar para o início do heap do descritor. Observe que o tamanho do incremento não pode ser considerado como um tamanho de byte, pois os aplicativos não devem desreferenciar identificadores como se fossem memória – a memória apontada tem um layout não padronizado e pode variar mesmo para um determinado dispositivo.

[**GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart) retorna um identificador de CPU para heaps de descritor visíveis da CPU. Ele retorna um identificador nulo (e a camada de depuração relatará um erro) se o heap do descritor não estiver visível para a CPU.

[**GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart) retorna um identificador de GPU para heaps de descritor visíveis do sombreador. Ele retorna um identificador nulo (e a camada de depuração relatará um erro) se o heap do descritor não estiver visível para o sombreador.

Por exemplo, criar exibições de destino de renderização para exibir texto D2D usando um dispositivo 11on12.


```C++
    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_d3d12Device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_d3d12Device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    
    }
```



## <a name="minimal-descriptor-heap-wrapper"></a>Wrapper de heap de descritor mínimo

Os desenvolvedores de aplicativos provavelmente desejarão criar seu próprio código auxiliar para gerenciar identificadores e heaps de descritores. Um exemplo básico é mostrado abaixo. Wrappers mais sofisticados poderiam, por exemplo, controlar quais tipos de descritores são onde estão em um heap e armazenar os argumentos de criação da descrição.

``` syntax
class CDescriptorHeapWrapper
{
public:
    CDescriptorHeapWrapper() { memset(this, 0, sizeof(*this)); }

    HRESULT Create(
        ID3D12Device* pDevice, 
        D3D12_DESCRIPTOR_HEAP_TYPE Type, 
        UINT NumDescriptors, 
        bool bShaderVisible = false)
    {
        D3D12_DESCRIPTOR_HEAP_DESC Desc;
        Desc.Type = Type;
        Desc.NumDescriptors = NumDescriptors;
        Desc.Flags = (bShaderVisible ? D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE : D3D12_DESCRIPTOR_HEAP_FLAG_NONE);
       
        HRESULT hr = pDevice->CreateDescriptorHeap(&Desc, 
                               __uuidof(ID3D12DescriptorHeap), 
                               (void**)&pDH);
        if (FAILED(hr)) return hr;

        hCPUHeapStart = pDH->GetCPUDescriptorHandleForHeapStart();
        hGPUHeapStart = pDH->GetGPUDescriptorHandleForHeapStart();

        HandleIncrementSize = pDevice->GetDescriptorHandleIncrementSize(Desc.Type);
        return hr;
    }
    operator ID3D12DescriptorHeap*() { return pDH; }

    D3D12_CPU_DESCRIPTOR_HANDLE hCPU(UINT index)
    {
        return hCPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_GPU_DESCRIPTOR_HANDLE hGPU(UINT index) 
    {
        assert(Desc.Flags&D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE); 
        return hGPUHeapStart.MakeOffsetted(index,HandleIncrementSize); 
    }
    D3D12_DESCRIPTOR_HEAP_DESC Desc;
    CComPtr<ID3D12DescriptorHeap> pDH;
    D3D12_CPU_DESCRIPTOR_HANDLE hCPUHeapStart;
    D3D12_GPU_DESCRIPTOR_HANDLE hGPUHeapStart;
    UINT HandleIncrementSize;
};
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> </dl>

 

 