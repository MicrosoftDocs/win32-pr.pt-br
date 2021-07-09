---
title: Carregando diferentes tipos de recursos
description: Mostra como usar um buffer para carregar dados de buffer constante e dados de buffer de vértice para a GPU e como sublocar e colocar corretamente os dados em buffers.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03d4755124bbadcdd255a6e99739b710845ab14
ms.sourcegitcommit: a30d0436a84986234df673c6def6694d5a8579f6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113563776"
---
# <a name="uploading-different-types-of-resources"></a>Carregando diferentes tipos de recursos

Mostra como usar um buffer para carregar dados de buffer constante e dados de buffer de vértice para a GPU e como sublocar e colocar corretamente os dados em buffers. O uso de um único buffer aumenta a flexibilidade de uso de memória e fornece aos aplicativos um controle mais rígido sobre o uso de memória. Também mostra as diferenças entre os modelos Direct3D 11 e Direct3D 12 para carregar diferentes tipos de recursos.

## <a name="upload-different-types-of-resources"></a>Upload tipos diferentes de recursos

No Direct3D 12, você cria um buffer para acomodar diferentes tipos de dados de recurso para upload e copia dados de recursos para o mesmo buffer de maneira semelhante para dados de recursos diferentes. As exibições individuais são criadas para vincular esses dados de recurso ao pipeline de gráficos no modelo de associação de recursos do Direct3D 12.

No Direct3D 11, você cria buffers separados para diferentes tipos de dados de recurso (observe os diferentes usados no código de exemplo do Direct3D 11 abaixo), vinculando explicitamente cada buffer de recursos ao pipeline de gráficos e atualiza os dados do recurso com métodos diferentes com base em diferentes tipos de `BindFlags` recursos.

No Direct3D 12 e no Direct3D 11, você deve usar os recursos de upload somente em que a CPU gravará os dados uma vez e a GPU os lerá uma vez.

Em alguns casos,
* a GPU lerá os dados várias vezes ou
* a GPU não lerá os dados linearmente ou
* a renderização já é significativamente limitada por GPU.

Nesses casos, a melhor opção pode ser usar [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) para copiar os dados do buffer de upload para um recurso padrão.

Um recurso padrão pode residir na memória de vídeo físico em GPUs discretas.

### <a name="code-example-direct3d-11"></a>Exemplo de código: Direct3D 11

```cpp
// Direct3D 11: Separate buffers for each resource type.

void main()
{
    // ...

    // Create a constant buffer.
    float constantBufferData[] = ...;

    D3D11_BUFFER_DESC constantBufferDesc = {0};  
    constantBufferDesc.ByteWidth = sizeof(constantBufferData);  
    constantBufferDesc.Usage = D3D11_USAGE_DYNAMIC;  
    constantBufferDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;  
    constantBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;  

    ComPtr<ID3D11Buffer> constantBuffer;
    d3dDevice->CreateBuffer(  
        &constantBufferDesc,  
        NULL,
        &constantBuffer  
        );

    // Create a vertex buffer.
    float vertexBufferData[] = ...;

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(vertexBufferData);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;

    ComPtr<ID3D11Buffer> vertexBuffer;
    d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        NULL,
        &vertexBuffer
        );

    // ...
}

void DrawFrame()
{
    // ...

    // Bind buffers to the graphics pipeline.
    d3dDeviceContext->VSSetConstantBuffers(0, 1, constantBuffer.Get());
    d3dDeviceContext->IASetVertexBuffers(0, 1, vertexBuffer.Get(), ...);

    // Update the constant buffer.
    D3D11_MAPPED_SUBRESOURCE mappedResource;  
    d3dDeviceContext->Map(
        constantBuffer.Get(),
        0, 
        D3D11_MAP_WRITE_DISCARD,
        0,
        &mappedResource
        );
    memcpy(mappedResource.pData, constantBufferData,
        sizeof(contatnBufferData));
    d3dDeviceContext->Unmap(constantBuffer.Get(), 0);  

    // Update the vertex buffer.
    d3dDeviceContext->UpdateSubresource(
        vertexBuffer.Get(),
        0,
        NULL,
        vertexBufferData,
        sizeof(vertexBufferData),
        0
    );

    // ...
}
```

### <a name="code-example-direct3d-12"></a>Exemplo de código: Direct3D 12

```cpp
// Direct3D 12: One buffer to accommodate different types of resources

ComPtr<ID3D12Resource> m_spUploadBuffer;
UINT8* m_pDataBegin = nullptr;    // starting position of upload buffer
UINT8* m_pDataCur = nullptr;      // current position of upload buffer
UINT8* m_pDataEnd = nullptr;      // ending position of upload buffer

void main()
{
    //
    // Initialize an upload buffer
    //

    InitializeUploadBuffer(64 * 1024);

    // ...
}

void DrawFrame()
{
    // ...

    // Set vertices data to the upload buffer.

    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float),
            sizeof(float), 
            verticesOffset
            ));

    // Set constant data to the upload buffer.

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadBuffer(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT, 
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model.

    D3D12_VERTEX_BUFFER_VIEW vertexBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + verticesOffset,
        sizeof(vertices), // size
        sizeof(float) * 4,  // stride
    };

    commandList->IASetVertexBuffers( 
        0,
        1,
        &vertexBufferViewDesc,
        ));

    // Create constant buffer views for the new binding model.

    D3D12_CONSTANT_BUFFER_VIEW_DESC constantBufferViewDesc = {
        m_spUploadBuffer->GetGPUVirtualAddress() + constantsOffset,
        sizeof(constants) // size
         };

    d3dDevice->CreateConstantBufferView(
        &constantBufferViewDesc,
        ...
        ));

    // Continue command list building and execution ...
}

//
// Create an upload buffer and keep it always mapped.
//

HRESULT InitializeUploadBuffer(SIZE_T uSize)
{
    HRESULT hr = d3dDevice->CreateCommittedResource(
         &CD3DX12_HEAP_PROPERTIES( D3D12_HEAP_TYPE_UPLOAD ),    
               D3D12_HEAP_FLAG_NONE, 
               &CD3DX12_RESOURCE_DESC::Buffer( uSize ), 
               D3D12_RESOURCE_STATE_GENERIC_READ, nullptr,  
               IID_PPV_ARGS( &m_spUploadBuffer ) );

    if (SUCCEEDED(hr))
    {
        void* pData;
        //
        // No CPU reads will be done from the resource.
        //
        CD3DX12_RANGE readRange(0, 0);
        m_spUploadBuffer->Map( 0, &readRange, &pData ); 
        m_pDataCur = m_pDataBegin = reinterpret_cast< UINT8* >( pData );
        m_pDataEnd = m_pDataBegin + uSize;
    }
    return hr;
}

//
// Sub-allocate from the buffer, with offset aligned.
//

HRESULT SuballocateFromBuffer(SIZE_T uSize, UINT uAlign)
{
    m_pDataCur = reinterpret_cast< UINT8* >(
        Align(reinterpret_cast< SIZE_T >(m_pDataCur), uAlign)
        );

    return (m_pDataCur + uSize > m_pDataEnd) ? E_INVALIDARG : S_OK;
}

//
// Place and copy data to the upload buffer.
//

HRESULT SetDataToUploadBuffer(
    const void* pData, 
    UINT bytesPerData, 
    UINT dataCount, 
    UINT alignment, 
    UINT& byteOffset
    )
{
    SIZE_T byteSize = bytesPerData * dataCount;
    HRESULT hr = SuballocateFromBuffer(byteSize, alignment);
    if (SUCCEEDED(hr))
    {
        byteOffset = UINT(m_pDataCur - m_pDataBegin);
        memcpy(m_pDataCur, pData, byteSize); 
        m_pDataCur += byteSize;
    }
    return hr;
}

//
// Align uLocation to the next multiple of uAlign.
//

UINT Align(UINT uLocation, UINT uAlign)
{
    if ( (0 == uAlign) || (uAlign & (uAlign-1)) )
    {
        ThrowException("non-pow2 alignment");
    }

    return ( (uLocation + (uAlign-1)) & ~(uAlign-1) );
}
```

Observe o uso das estruturas auxiliares [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) e [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).

## <a name="constants"></a>Constantes

Para definir constantes, vértices e índices em um heap de upload ou readback, use as APIs a seguir.

-   [**ID3D12Device::CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [**ID3D12GraphicsCommandList::IASetIndexBuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a>Recursos

Recursos são o conceito direct3D que abstrai o uso da memória física da GPU. Os recursos exigem espaço de endereço virtual de GPU para acessar a memória física. A criação de recursos é de thread livre.

Há três tipos de recursos em relação à criação de endereço virtual e flexibilidade no Direct3D 12.

### <a name="committed-resources"></a>Recursos comprometidos

Os recursos comprometidos são a ideia mais comum de recursos direct3D ao longo das gerações. A criação desse recurso aloca o intervalo de endereços virtuais, um heap implícito grande o suficiente para se ajustar a todo o recurso e confirma o intervalo de endereços virtuais para a memória física encapsulada pelo heap. As propriedades de heap implícitas devem ser passadas para corresponder a paridade funcional com versões anteriores do Direct3D. Consulte [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

### <a name="reserved-resources"></a>Recursos reservados

Os recursos reservados são equivalentes aos recursos lado a lado do Direct3D 11. Na criação, somente um intervalo de endereços virtuais é alocado e não mapeado para nenhum heap. O aplicativo mapeará esses recursos para heaps posteriormente. Atualmente, os recursos desses recursos são inalterados do Direct3D 11, pois eles podem ser mapeados para um heap em uma granularidade de bloco de 64KB com [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings). Consulte [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).

### <a name="placed-resources"></a>Recursos colocados

Novo para o Direct3D 12, você pode criar heaps separados dos recursos. Posteriormente, você pode localizar vários recursos em um único heap. Você pode fazer isso sem criar recursos reservados ou lado a lado, permitindo que os recursos de todos os tipos de recursos possam ser criados diretamente pelo seu aplicativo. Vários recursos podem se sobrepor e você deve usar [**o ID3D12GraphicsCommandList::ResourceBagraphic**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) para re-usar a memória física corretamente. Consulte [**ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).

## <a name="resource-size-reflection"></a>Reflexão do tamanho do recurso

Você deve usar a reflexão de tamanho do recurso para entender quanto texturas de espaço com layouts de textura desconhecidos exigem em heaps. Buffers também têm suporte, mas principalmente como uma conveniência.

Você deve estar ciente das principais discrepâncias de alinhamento para ajudar a empacotar recursos mais densamente.

Por exemplo, uma matriz de elemento único com um  buffer de um byte  retorna um Tamanho de 64KB e um Alinhamento de 64KB, porque os buffers podem ser alinhados apenas a 64KB.

Além disso, uma matriz de três elementos com duas texturas alinhadas de 64KB de single-texel e uma textura alinhada de 4 MB de um único texel relata tamanhos diferentes com base na ordem da matriz. Se as texturas alinhadas de 4 MB estão no meio, o *Tamanho* resultante é de 12 MB. Caso contrário, o Tamanho resultante será de 8 MB. O Alinhamento retornado sempre seria de 4 MB, o superconjunto de todos os alinhamentos na matriz de recursos.

Consulte as APIs a seguir.

- [**D3D12 \_ INFORMAÇÕES DE \_ ALOCAÇÃO DE \_ RECURSOS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [**GetResourceAllocationInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a>Alinhamento do buffer

As restrições de alinhamento do buffer não foram alteradas do Direct3D 11, principalmente:

- 4 MB para texturas de várias amostras.
- 64 KB para texturas e buffers de amostra única.

## <a name="related-topics"></a>Tópicos relacionados

* [Sublocação em buffers](large-buffers.md)
