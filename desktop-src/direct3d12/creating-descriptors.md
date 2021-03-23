---
title: Criando descritores
description: Descreve e mostra exemplos de como criar exibições de índice, vértice e buffer constante; recurso de sombreador, destino de renderização, acesso não ordenado, saída de fluxo e exibições de estêncil de profundidade; e amostras. Todos os métodos para criar descritores são threads livres.
ms.assetid: 0D360A7C-8A2F-49E1-A5CC-98C958B59D1C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac9aab5dde0f5ca0864fcc1627ade984c6b6ccf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548245"
---
# <a name="creating-descriptors"></a>Criando descritores

Descreve e mostra exemplos de como criar exibições de índice, vértice e buffer constante; recurso de sombreador, destino de renderização, acesso não ordenado, saída de fluxo e exibições de estêncil de profundidade; e amostras. Todos os métodos para criar descritores são threads livres.

-   [Exibição do buffer de índice](#index-buffer-view)
-   [Exibição do buffer de vértice](#vertex-buffer-view)
-   [Modo de Exibição de Recursos do sombreador](#shader-resource-view)
-   [Exibição do buffer de constantes](#constant-buffer-view)
-   [Exemplo](#sampler)
-   [Modo de exibição de acesso não ordenado](#unordered-access-view)
-   [Exibição de saída de fluxo](#stream-output-view)
-   [Renderizar exibição de destino](#render-target-view)
-   [Exibição de estêncil de profundidade](#depth-stencil-view)
-   [Tópicos relacionados](#related-topics)

## <a name="index-buffer-view"></a>Exibição do buffer de índice

Para criar uma exibição de buffer de índice, preencha uma estrutura de [**\_ exibição de \_ buffer \_ de índice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view) :

``` syntax
typedef struct D3D12_INDEX_BUFFER_VIEW
{
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
    UINT SizeInBytes;
    DXGI_FORMAT Format;
}   D3D12_INDEX_BUFFER_VIEW;
```

Defina o local (Call [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) e o tamanho do buffer, observando que \_ \_ o endereço virtual da GPU D3D12 \_ é definido como:

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

Consulte a enumeração [**de \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) . Normalmente, para um buffer de índice, o seguinte definir pode ser usado:

`const DXGI_FORMAT StandardIndexFormat = DXGI_FORMAT_R32_UINT;`

Finalmente, chame [**ID3D12GraphicsCommandList:: IASetIndexBuffer**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer).

Por exemplo,


```C++
// Initialize the index buffer view.
m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
```



## <a name="vertex-buffer-view"></a>Exibição do buffer de vértice

Para criar uma exibição de buffer de vértice, preencha uma estrutura de [**\_ exibição de \_ buffer \_ de vértice D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view) :

``` syntax
typedef struct D3D12_VERTEX_BUFFER_VIEW {
    D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;  
    UINT SizeInBytes;  
    UINT StrideInBytes;  
} D3D12_VERTEX_BUFFER_VIEW;
```

Defina o local (Call [**GetGPUVirtualAddress**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)) e o tamanho do buffer, observando que \_ \_ o endereço virtual da GPU D3D12 \_ é definido como:

`typedef UINT64 D3D12_GPU_VIRTUAL_ADDRESS;`

O stride normalmente é o tamanho de uma única estrutura de dados de vértice, como `sizeof(Vertex);` , em seguida, chamar [**ID3D12GraphicsCommandList:: IASetVertexBuffers**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers).

Por exemplo,


```C++
// Initialize the vertex buffer view.
m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
m_vertexBufferView.SizeInBytes = SampleAssets::VertexDataSize;
m_vertexBufferView.StrideInBytes = SampleAssets::StandardVertexStride;
```



## <a name="shader-resource-view"></a>Modo de Exibição de Recursos do sombreador

Para criar um modo de exibição de recurso de sombreador, preencha uma estrutura [**desc de exibição de \_ recursos do sombreador \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) :

``` syntax
typedef struct D3D12_SHADER_RESOURCE_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_SRV_DIMENSION ViewDimension;  
    UINT Shader4ComponentMapping;  
    union   
        {  
        D3D12_BUFFER_SRV Buffer;  
        D3D12_TEX1D_SRV Texture1D;  
        D3D12_TEX1D_ARRAY_SRV Texture1DArray;  
        D3D12_TEX2D_SRV Texture2D;  
        D3D12_TEX2D_ARRAY_SRV Texture2DArray;  
        D3D12_TEX2DMS_SRV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_SRV Texture2DMSArray;  
        D3D12_TEX3D_SRV Texture3D;  
        D3D12_TEXCUBE_SRV TextureCube;  
        D3D12_TEXCUBE_ARRAY_SRV TextureCubeArray;  
        }   ;  
    }   D3D12_SHADER_RESOURCE_VIEW_DESC; 
```

O `ViewDimension` campo é definido como zero ou um valor da enumeração de [**\_ \_ \_ sinalizadores SRV do buffer D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags) .

As enumerações e estruturas referenciadas [**pela \_ exibição de recursos do sombreador D3D12 \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc) são:

-   [**\_formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 do \_ buffer do \_ servidor**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv)
-   [**D3D12 \_ TEX1D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv)
-   [**D3D12 \_ TEX1D \_ matriz \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv)
-   [**D3D12 \_ TEX2D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv)
-   [**D3D12 \_ TEX2D \_ matriz \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv)
-   [**D3D12 \_ TEX2DMS \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv)
-   [**D3D12 \_ TEX2DMS \_ matriz \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv)
-   [**D3D12 \_ TEX3D \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv)
-   [**D3D12 \_ TEXCUBE \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv)
-   [**D3D12 \_ TEXCUBE \_ matriz \_ SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv)

Observe abaixo que float foi `ResourceMinLODClamp` adicionado a SRVs para Tex1D/2D/3D/Cube. No D3D11, era uma propriedade de um recurso, mas isso não correspondia a como ele foi implementado no hardware. `StructureByteStride` foi adicionado ao buffer SRVs, em que em D3D11 era uma propriedade do recurso. Se o stride for diferente de zero, que indica uma exibição de buffer estruturada, e o formato deverá ser definido como \_ formato dxgi \_ desconhecido.

Por fim, para criar a exibição de recursos do sombreador, chame [**ID3D12Device:: CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview).

Por exemplo,


```C++
// Describe and create an SRV.
D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
srvDesc.Format = tex.Format;
srvDesc.Texture2D.MipLevels = tex.MipLevels;
srvDesc.Texture2D.MostDetailedMip = 0;
srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);
```



## <a name="constant-buffer-view"></a>Exibição do buffer de constantes

Para criar uma exibição de buffer constante, preencha uma [**estrutura \_ \_ desc de \_ exibição \_ de buffer de constante D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc) :

``` syntax
typedef struct D3D12_CONSTANT_BUFFER_VIEW_DESC {
  D3D12_GPU_VIRTUAL_ADDRESS BufferLocation;
  UINT   SizeInBytes;
} D3D12_CONSTANT_BUFFER_VIEW_DESC;
```

Em seguida, chame [**ID3D12Device:: CreateConstantBufferView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview).

Por exemplo,


```C++
// Describe and create a constant buffer view.
D3D12_CONSTANT_BUFFER_VIEW_DESC cbvDesc = {};
cbvDesc.BufferLocation = m_constantBuffer->GetGPUVirtualAddress();
cbvDesc.SizeInBytes = (sizeof(ConstantBuffer) + 255) & ~255;    // CB size is required to be 256-byte aligned.
m_device->CreateConstantBufferView(&cbvDesc, m_cbvHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="sampler"></a>Exemplo

Para criar um exemplo, preencha uma estrutura [**\_ \_ desc de amostra de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc) :

``` syntax
typedef struct D3D12_SAMPLER_DESC
{
    D3D12_FILTER Filter;
    D3D12_TEXTURE_ADDRESS_MODE AddressU;
    D3D12_TEXTURE_ADDRESS_MODE AddressV;
    D3D12_TEXTURE_ADDRESS_MODE AddressW;
    FLOAT MipLODBias;
    UINT MaxAnisotropy;
    D3D12_COMPARISON_FUNC ComparisonFunc;
    FLOAT BorderColor[4]; // RGBA
    FLOAT MinLOD;
    FLOAT MaxLOD;
} D3D12_SAMPLER_DESC;
```

Para preencher essa estrutura, consulte as seguintes enumerações:

-   [**Filtro de D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)
-   [**\_Tipo de filtro D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_type)
-   [**\_Tipo de \_ redução do filtro D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter_reduction_type)
-   [**\_Modo de \_ endereço de textura D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode)
-   [**\_Funcde de comparação de D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func)

Por fim, chame [**ID3D12Device:: Createsampler**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createsampler).

Por exemplo,


```C++
// Describe and create a sampler.
D3D12_SAMPLER_DESC samplerDesc = {};
samplerDesc.Filter = D3D12_FILTER_MIN_MAG_MIP_LINEAR;
samplerDesc.AddressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.AddressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.AddressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP;
samplerDesc.MinLOD = 0;
samplerDesc.MaxLOD = D3D12_FLOAT32_MAX;
samplerDesc.MipLODBias = 0.0f;
samplerDesc.MaxAnisotropy = 1;
samplerDesc.ComparisonFunc = D3D12_COMPARISON_FUNC_ALWAYS;
m_device->CreateSampler(&samplerDesc, m_samplerHeap->GetCPUDescriptorHandleForHeapStart());
```



## <a name="unordered-access-view"></a>Modo de exibição de acesso não ordenado

Para criar uma exibição de acesso não ordenado, preencha uma estrutura [**\_ desc de exibição de \_ acesso \_ \_ não ordenado D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc) :

``` syntax
typedef struct D3D12_UNORDERED_ACCESS_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_UAV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_UAV Buffer;
        D3D12_TEX1D_UAV Texture1D;
        D3D12_TEX1D_ARRAY_UAV Texture1DArray;
        D3D12_TEX2D_UAV Texture2D;
        D3D12_TEX2D_ARRAY_UAV Texture2DArray;
        D3D12_TEX3D_UAV Texture3D;
    };
} D3D12_UNORDERED_ACCESS_VIEW_DESC;
```

O `ViewDimension` campo é definido como zero ou um valor da enumeração [**D3D12 do \_ buffer \_ UAV \_ flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) .

Consulte as seguintes enumerações e estruturas:

-   [**\_formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav)
-   [**D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav)
-   [**\_Matriz D3D12 \_ TEX1D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav)
-   [**D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav)
-   [**\_Matriz D3D12 \_ TEX2D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav)
-   [**D3D12 \_ TEX3D \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav)

`StructureByteStride` foi adicionado ao buffer UAVs, em que em D3D11 era uma propriedade do recurso. Se o stride for diferente de zero, que indica uma exibição de buffer estruturada, e o formato deverá ser definido como \_ formato dxgi \_ desconhecido.

Finalmente, chame [**ID3D12Device:: CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).

Por exemplo,


```C++
// Create the unordered access views (UAVs) that store the results of the compute work.
CD3DX12_CPU_DESCRIPTOR_HANDLE processedCommandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), ProcessedCommandsOffset, m_cbvSrvUavDescriptorSize);
for (UINT frame = 0; frame < FrameCount; frame++)
{
    // Allocate a buffer large enough to hold all of the indirect commands
    // for a single frame as well as a UAV counter.
    commandBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(CommandBufferSizePerFrame + sizeof(UINT), D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS);
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &commandBufferDesc,
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_processedCommandBuffers[frame])));

    D3D12_UNORDERED_ACCESS_VIEW_DESC uavDesc = {};
    uavDesc.Format = DXGI_FORMAT_UNKNOWN;
    uavDesc.ViewDimension = D3D12_UAV_DIMENSION_BUFFER;
    uavDesc.Buffer.FirstElement = 0;
    uavDesc.Buffer.NumElements = TriangleCount;
    uavDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
    uavDesc.Buffer.CounterOffsetInBytes = CommandBufferSizePerFrame;
    uavDesc.Buffer.Flags = D3D12_BUFFER_UAV_FLAG_NONE;

    m_device->CreateUnorderedAccessView(            
        m_processedCommandBuffers[frame].Get(),
        m_processedCommandBuffers[frame].Get(),
        &uavDesc,
        processedCommandsHandle);

    processedCommandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
}

// Allocate a buffer that can be used to reset the UAV counters and initialize it to 0.
ThrowIfFailed(m_device->CreateCommittedResource(
    &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
    D3D12_HEAP_FLAG_NONE,
    &CD3DX12_RESOURCE_DESC::Buffer(sizeof(UINT)),
    D3D12_RESOURCE_STATE_GENERIC_READ,
    
    nullptr,
    IID_PPV_ARGS(&m_processedCommandBufferCounterReset)));

UINT8* pMappedCounterReset = nullptr;
CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
ThrowIfFailed(m_processedCommandBufferCounterReset->Map(0, &readRange, reinterpret_cast<void**>(&pMappedCounterReset)));
ZeroMemory(pMappedCounterReset, sizeof(UINT));
m_processedCommandBufferCounterReset->Unmap(0, nullptr);
```



## <a name="stream-output-view"></a>Exibição de saída de fluxo

Para criar uma exibição de saída de fluxo, preencha uma estrutura [**desc de saída de fluxo de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .

``` syntax
typedef struct D3D12_STREAM_OUTPUT_DESC  
    {  
    _Field_size_full_(NumEntries)  const D3D12_SO_DECLARATION_ENTRY *pSODeclaration;  
    UINT NumEntries;  
    _Field_size_full_(NumStrides)  const UINT *pBufferStrides;  
    UINT NumStrides;  
    UINT RasterizedStream;  
    }   D3D12_STREAM_OUTPUT_DESC;  
```

Em seguida, chame [**ID3D12GraphicsCommandList:: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets).

## <a name="render-target-view"></a>Renderizar exibição de destino

Para criar uma exibição de destino de renderização, preencha uma estrutura [**desc de exibição de destino de D3D12 \_ render \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc) .

``` syntax
typedef struct D3D12_RENDER_TARGET_VIEW_DESC
{
    DXGI_FORMAT Format;
    D3D12_RTV_DIMENSION ViewDimension;

    union
    {
        D3D12_BUFFER_RTV Buffer;
        D3D12_TEX1D_RTV Texture1D;
        D3D12_TEX1D_ARRAY_RTV Texture1DArray;
        D3D12_TEX2D_RTV Texture2D;
        D3D12_TEX2D_ARRAY_RTV Texture2DArray;
        D3D12_TEX2DMS_RTV Texture2DMS;
        D3D12_TEX2DMS_ARRAY_RTV Texture2DMSArray;
        D3D12_TEX3D_RTV Texture3D;
    };
} D3D12_RENDER_TARGET_VIEW_DESC;
```

O `ViewDimension` campo é definido como zero ou um valor da enumeração de [**\_ \_ dimensão D3D12 RTV**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_rtv_dimension) .

Consulte as seguintes enumerações e estruturas:

-   [**\_formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**D3D12 \_ buffer \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv)
-   [**D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv)
-   [**\_Matriz D3D12 \_ TEX1D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv)
-   [**D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv)
-   [**D3D12 \_ TEX2DMS \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv)
-   [**\_Matriz D3D12 \_ TEX2D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv)
-   [**\_Matriz D3D12 \_ TEX2DMS \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv)
-   [**D3D12 \_ TEX3D \_ RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv)

Por fim, chame [**ID3D12Device:: CreateRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview).

Por exemplo,

```C++
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
```



## <a name="depth-stencil-view"></a>Exibição de estêncil de profundidade

Para criar uma exibição de estêncil de profundidade, preencha uma estrutura [**desc de exibição de estêncil de profundidade de D3D12 \_ \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc) :

``` syntax
typedef struct D3D12_DEPTH_STENCIL_VIEW_DESC  
    {  
    DXGI_FORMAT Format;  
    D3D12_DSV_DIMENSION ViewDimension;  
    D3D12_DSV_FLAGS Flags;  
    union   
        {  
        D3D12_TEX1D_DSV Texture1D;  
        D3D12_TEX1D_ARRAY_DSV Texture1DArray;  
        D3D12_TEX2D_DSV Texture2D;  
        D3D12_TEX2D_ARRAY_DSV Texture2DArray;  
        D3D12_TEX2DMS_DSV Texture2DMS;  
        D3D12_TEX2DMS_ARRAY_DSV Texture2DMSArray;  
        }   ;  
    }   D3D12_DEPTH_STENCIL_VIEW_DESC;  
```

O `ViewDimension` campo é definido como zero ou um valor da enumeração de [**\_ \_ dimensão DSV D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_dimension) . Consulte a enumeração [**de \_ \_ sinalizadores DSV D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_dsv_flags) para as configurações de sinalizador.

Consulte as seguintes enumerações e estruturas:

-   [**\_formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
-   [**\_DSV D3D12 TEX1D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv)
-   [**\_DSV de \_ matriz D3D12 TEX1D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv)
-   [**\_DSV D3D12 TEX2D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv)
-   [**\_DSV de \_ matriz D3D12 TEX2D \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv)
-   [**\_DSV D3D12 TEX2DMS \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv)
-   [**\_DSV de \_ matriz D3D12 TEX2DMS \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv)

Por fim, chame [**ID3D12Device:: CreateDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview).

Por exemplo,


```C++
// Create the depth stencil view.
{
    D3D12_DEPTH_STENCIL_VIEW_DESC depthStencilDesc = {};
    depthStencilDesc.Format = DXGI_FORMAT_D32_FLOAT;
    depthStencilDesc.ViewDimension = D3D12_DSV_DIMENSION_TEXTURE2D;
    depthStencilDesc.Flags = D3D12_DSV_FLAG_NONE;

    D3D12_CLEAR_VALUE depthOptimizedClearValue = {};
    depthOptimizedClearValue.Format = DXGI_FORMAT_D32_FLOAT;
    depthOptimizedClearValue.DepthStencil.Depth = 1.0f;
    depthOptimizedClearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Tex2D(DXGI_FORMAT_D32_FLOAT, m_width, m_height, 1, 0, 1, 0, D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL),
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &depthOptimizedClearValue,
        IID_PPV_ARGS(&m_depthStencil)
        ));

    m_device->CreateDepthStencilView(m_depthStencil.Get(), &depthStencilDesc, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Descritores](descriptors.md)
</dt> <dt>

[Heaps de descritores](descriptor-heaps.md)
</dt> </dl>

 

 