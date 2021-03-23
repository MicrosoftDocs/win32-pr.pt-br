---
title: Carregando diferentes tipos de recursos
description: Mostra como usar um buffer para carregar dados de buffer constante e dados de buffer de vértice para a GPU e como subalocar e posicionar corretamente os dados nos buffers.
ms.assetid: 255B0482-21D6-4276-8009-3F3891879CA1
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2edca2cd9f4d3becf5036056a89f91c50f2c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104203"
---
# <a name="uploading-different-types-of-resources"></a>Carregando diferentes tipos de recursos

Mostra como usar um buffer para carregar dados de buffer constante e dados de buffer de vértice para a GPU e como subalocar e posicionar corretamente os dados nos buffers. O uso de um único buffer aumenta a flexibilidade do uso de memória e fornece aos aplicativos um controle mais rígido do uso de memória. Também mostra as diferenças entre os modelos D3D11 e D3D12 para carregar diferentes tipos de recursos.

-   [Carregar diferentes tipos de recursos](#upload-different-types-of-resources)
    -   [Exemplo de código: D3D11](#code-example-d3d11)
    -   [Exemplo de código: D3D12](#code-example-d3d12)
-   [Constantes](#constants)
-   [Recursos](#uploading-different-types-of-resources)
-   [Reflexo do tamanho do recurso](#resource-size-reflection)
-   [Alinhamento do buffer](#buffer-alignment)
-   [Tópicos relacionados](#related-topics)

## <a name="upload-different-types-of-resources"></a>Carregar diferentes tipos de recursos

No D3D12, os aplicativos criam um buffer para acomodar diferentes tipos de dados de recursos para carregar e copiar dados de recursos para o mesmo buffer de forma semelhante para dados de recursos diferentes. As exibições individuais são então criadas para associar esses dados de recurso ao pipeline de gráficos no novo modelo de associação de recursos.

No D3D11, os aplicativos criam buffers separados para diferentes tipos de dados de recurso (Observe os diferentes `BindFlags` usados no código de exemplo D3D11 abaixo), ligando explicitamente cada buffer de recursos ao pipeline de gráficos e atualizando os dados de recursos com diferentes métodos com base em diferentes tipos de recursos.

Em D3D12 e D3D11, os aplicativos só devem usar recursos de carregamento em que a CPU gravará os dados uma vez e a GPU o lerá uma vez. Se a GPU ler os dados várias vezes, a GPU não lerá os dados linearmente, ou a renderização ainda é muito limitada por GPU. A melhor opção pode ser usar [**ID3D12GraphicsCommandList:: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList:: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) para copiar os dados do buffer de carregamento para um recurso padrão. Um recurso padrão pode residir em memória de vídeo física em GPUs discretas.

### <a name="code-example-d3d11"></a>Exemplo de código: D3D11

``` syntax
// D3D11: Separate buffers for each resource type.

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

### <a name="code-example-d3d12"></a>Exemplo de código: D3D12

``` syntax
// D3D12: One buffer to accommodate different types of resources

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

Observe o uso das estruturas auxiliares [**CD3DX12 \_ heap \_ Properties**](cd3dx12-heap-properties.md) e [**CD3DX12 do \_ recurso \_ desc**](cd3dx12-resource-desc.md).

## <a name="constants"></a>Constantes

Para definir constantes, vértices e índices em um heap de upload ou readback, use as seguintes APIs:

-   [**ID3D12Device::CreateConstantBufferView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [**ID3D12GraphicsCommandList::IASetIndexBuffer**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a>Recursos

Os recursos são o conceito de D3D que abstrai o uso da memória física da GPU. Os recursos exigem o espaço de endereço virtual da GPU para acessar a memória física. A criação de recursos é de segmento livre.

Há três tipos de recursos em relação à criação e à flexibilidade do endereço virtual no D3D12:

-   Recursos confirmados

    Os recursos confirmados são a ideia mais comum de recursos do D3D nas gerações. A criação desse recurso aloca um intervalo de endereços virtuais, um heap implícito grande o suficiente para se ajustar a todo o recurso e confirma o intervalo de endereços virtuais para a memória física encapsulada pelo heap. As propriedades implícitas de heap devem ser passadas para corresponder à paridade funcional com versões anteriores do D3D. Consulte [**ID3D12Device:: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

-   Recursos reservados

    Os recursos reservados são equivalentes a recursos de lado D3D11. Na criação, apenas um intervalo de endereços virtuais é alocado e não mapeado para nenhum heap. O aplicativo irá mapear esses recursos para heaps mais tarde. Os recursos desses recursos estão atualmente inalterados em D3D11, pois eles podem ser mapeados para um heap em uma granularidade de bloco de 64 KB com [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings). Consulte [ **ID3D12Device:: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)

-   Recursos inseridos

    Novo para D3D12, os aplicativos podem criar heaps separados dos recursos. Depois disso, o aplicativo pode localizar vários recursos em um único heap. Isso pode ser feito sem criar recursos por lado ou reservados, habilitando os recursos para todos os tipos de recursos que podem ser criados diretamente por aplicativos. Vários recursos podem se sobrepor e o aplicativo deve usar o `TiledResourceBarrier` para reutilizar a memória física corretamente. Consulte [ **ID3D12Device:: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)

## <a name="resource-size-reflection"></a>Reflexo do tamanho do recurso

Os aplicativos devem usar a reflexão de tamanho do recurso para entender a quantidade de texturas de aparências desconhecidas que os layouts de textura são necessários em pilhas. Os buffers também têm suporte, mas principalmente como uma conveniência.

Os aplicativos devem estar cientes das principais discrepâncias de alinhamento para ajudar a empacotar os recursos de forma mais densa.

Por exemplo, uma matriz de elemento único com um buffer de um byte retorna um tamanho de 64 KB e um alinhamento de 64 KB, pois os buffers atualmente só podem ser alinhados em 64 KB.

Além disso, uma matriz de três elementos com duas texturas alinhadas em 64 KB de Texel e uma textura alinhada de 4MB de Texel único relatam tamanhos diferentes com base na ordem da matriz. Se as texturas de 4MB alinhadas estiverem no meio, o tamanho resultante será 12 MB. Caso contrário, o tamanho resultante será 8MB. O alinhamento retornado sempre seria 4 MB, o super conjunto de todos os alinhamentos na matriz de recursos.

Referencie as seguintes APIs:

-   [**\_Informações de \_ alocação de recursos do D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [**GetResourceAllocationInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a>Alinhamento do buffer

As restrições de alinhamento de buffer não foram alteradas de D3D11, notavelmente:

-   4 MB para texturas com várias amostras.
-   64 KB para texturas e buffers de amostra única.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Subalocação em buffers](large-buffers.md)
</dt> </dl>

 

 




