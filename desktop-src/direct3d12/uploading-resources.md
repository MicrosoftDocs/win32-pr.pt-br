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
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="b249c-103">Carregando diferentes tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="b249c-103">Uploading Different Types of Resources</span></span>

<span data-ttu-id="b249c-104">Mostra como usar um buffer para carregar dados de buffer constante e dados de buffer de vértice para a GPU e como subalocar e posicionar corretamente os dados nos buffers.</span><span class="sxs-lookup"><span data-stu-id="b249c-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="b249c-105">O uso de um único buffer aumenta a flexibilidade do uso de memória e fornece aos aplicativos um controle mais rígido do uso de memória.</span><span class="sxs-lookup"><span data-stu-id="b249c-105">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="b249c-106">Também mostra as diferenças entre os modelos D3D11 e D3D12 para carregar diferentes tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="b249c-106">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span>

-   [<span data-ttu-id="b249c-107">Carregar diferentes tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="b249c-107">Upload Different Types of Resources</span></span>](#upload-different-types-of-resources)
    -   [<span data-ttu-id="b249c-108">Exemplo de código: D3D11</span><span class="sxs-lookup"><span data-stu-id="b249c-108">Code Example: D3D11</span></span>](#code-example-d3d11)
    -   [<span data-ttu-id="b249c-109">Exemplo de código: D3D12</span><span class="sxs-lookup"><span data-stu-id="b249c-109">Code Example: D3D12</span></span>](#code-example-d3d12)
-   [<span data-ttu-id="b249c-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="b249c-110">Constants</span></span>](#constants)
-   [<span data-ttu-id="b249c-111">Recursos</span><span class="sxs-lookup"><span data-stu-id="b249c-111">Resources</span></span>](#uploading-different-types-of-resources)
-   [<span data-ttu-id="b249c-112">Reflexo do tamanho do recurso</span><span class="sxs-lookup"><span data-stu-id="b249c-112">Resource size reflection</span></span>](#resource-size-reflection)
-   [<span data-ttu-id="b249c-113">Alinhamento do buffer</span><span class="sxs-lookup"><span data-stu-id="b249c-113">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="b249c-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b249c-114">Related topics</span></span>](#related-topics)

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="b249c-115">Carregar diferentes tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="b249c-115">Upload Different Types of Resources</span></span>

<span data-ttu-id="b249c-116">No D3D12, os aplicativos criam um buffer para acomodar diferentes tipos de dados de recursos para carregar e copiar dados de recursos para o mesmo buffer de forma semelhante para dados de recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="b249c-116">In D3D12, applications create one buffer to accommodate different types of resource data for uploading, and copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="b249c-117">As exibições individuais são então criadas para associar esses dados de recurso ao pipeline de gráficos no novo modelo de associação de recursos.</span><span class="sxs-lookup"><span data-stu-id="b249c-117">Individual views are then created to bind those resource data to the graphics pipeline in the new resource binding model.</span></span>

<span data-ttu-id="b249c-118">No D3D11, os aplicativos criam buffers separados para diferentes tipos de dados de recurso (Observe os diferentes `BindFlags` usados no código de exemplo D3D11 abaixo), ligando explicitamente cada buffer de recursos ao pipeline de gráficos e atualizando os dados de recursos com diferentes métodos com base em diferentes tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="b249c-118">In D3D11, applications create separate buffers for different types of resource data (note the different `BindFlags` used in the D3D11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="b249c-119">Em D3D12 e D3D11, os aplicativos só devem usar recursos de carregamento em que a CPU gravará os dados uma vez e a GPU o lerá uma vez.</span><span class="sxs-lookup"><span data-stu-id="b249c-119">In both D3D12 and D3D11, applications should only use upload resources where the CPU will write the data once and the GPU will read it once.</span></span> <span data-ttu-id="b249c-120">Se a GPU ler os dados várias vezes, a GPU não lerá os dados linearmente, ou a renderização ainda é muito limitada por GPU.</span><span class="sxs-lookup"><span data-stu-id="b249c-120">If the GPU will read the data multiple times, the GPU will not read the data linearly, or the rendering is significantly GPU-limited already.</span></span> <span data-ttu-id="b249c-121">A melhor opção pode ser usar [**ID3D12GraphicsCommandList:: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList:: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) para copiar os dados do buffer de carregamento para um recurso padrão.</span><span class="sxs-lookup"><span data-stu-id="b249c-121">The better option may be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span> <span data-ttu-id="b249c-122">Um recurso padrão pode residir em memória de vídeo física em GPUs discretas.</span><span class="sxs-lookup"><span data-stu-id="b249c-122">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-d3d11"></a><span data-ttu-id="b249c-123">Exemplo de código: D3D11</span><span class="sxs-lookup"><span data-stu-id="b249c-123">Code Example: D3D11</span></span>

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

### <a name="code-example-d3d12"></a><span data-ttu-id="b249c-124">Exemplo de código: D3D12</span><span class="sxs-lookup"><span data-stu-id="b249c-124">Code Example: D3D12</span></span>

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

<span data-ttu-id="b249c-125">Observe o uso das estruturas auxiliares [**CD3DX12 \_ heap \_ Properties**](cd3dx12-heap-properties.md) e [**CD3DX12 do \_ recurso \_ desc**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="b249c-125">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_RESOURCE\_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="b249c-126">Constantes</span><span class="sxs-lookup"><span data-stu-id="b249c-126">Constants</span></span>

<span data-ttu-id="b249c-127">Para definir constantes, vértices e índices em um heap de upload ou readback, use as seguintes APIs:</span><span class="sxs-lookup"><span data-stu-id="b249c-127">To set constants, vertices and indexes within an Upload or Readback heap, use the following APIs:</span></span>

-   [<span data-ttu-id="b249c-128">**ID3D12Device::CreateConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="b249c-128">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="b249c-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="b249c-129">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="b249c-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="b249c-130">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="b249c-131">Recursos</span><span class="sxs-lookup"><span data-stu-id="b249c-131">Resources</span></span>

<span data-ttu-id="b249c-132">Os recursos são o conceito de D3D que abstrai o uso da memória física da GPU.</span><span class="sxs-lookup"><span data-stu-id="b249c-132">Resources are the D3D concept which abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="b249c-133">Os recursos exigem o espaço de endereço virtual da GPU para acessar a memória física.</span><span class="sxs-lookup"><span data-stu-id="b249c-133">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="b249c-134">A criação de recursos é de segmento livre.</span><span class="sxs-lookup"><span data-stu-id="b249c-134">Resource creation is free-threaded.</span></span>

<span data-ttu-id="b249c-135">Há três tipos de recursos em relação à criação e à flexibilidade do endereço virtual no D3D12:</span><span class="sxs-lookup"><span data-stu-id="b249c-135">There are three types of resources with respect to virtual address creation and flexibility in D3D12:</span></span>

-   <span data-ttu-id="b249c-136">Recursos confirmados</span><span class="sxs-lookup"><span data-stu-id="b249c-136">Committed resources</span></span>

    <span data-ttu-id="b249c-137">Os recursos confirmados são a ideia mais comum de recursos do D3D nas gerações.</span><span class="sxs-lookup"><span data-stu-id="b249c-137">Committed resources are the most common idea of D3D resources over the generations.</span></span> <span data-ttu-id="b249c-138">A criação desse recurso aloca um intervalo de endereços virtuais, um heap implícito grande o suficiente para se ajustar a todo o recurso e confirma o intervalo de endereços virtuais para a memória física encapsulada pelo heap.</span><span class="sxs-lookup"><span data-stu-id="b249c-138">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="b249c-139">As propriedades implícitas de heap devem ser passadas para corresponder à paridade funcional com versões anteriores do D3D.</span><span class="sxs-lookup"><span data-stu-id="b249c-139">The implicit heap properties must be passed to match functional parity with previous D3D versions.</span></span> <span data-ttu-id="b249c-140">Consulte [**ID3D12Device:: CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="b249c-140">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

-   <span data-ttu-id="b249c-141">Recursos reservados</span><span class="sxs-lookup"><span data-stu-id="b249c-141">Reserved resources</span></span>

    <span data-ttu-id="b249c-142">Os recursos reservados são equivalentes a recursos de lado D3D11.</span><span class="sxs-lookup"><span data-stu-id="b249c-142">Reserved resources are equivalent to D3D11 tiled resources.</span></span> <span data-ttu-id="b249c-143">Na criação, apenas um intervalo de endereços virtuais é alocado e não mapeado para nenhum heap.</span><span class="sxs-lookup"><span data-stu-id="b249c-143">On their creation, only a virtual address range is allocated and not mapped to any heap.</span></span> <span data-ttu-id="b249c-144">O aplicativo irá mapear esses recursos para heaps mais tarde.</span><span class="sxs-lookup"><span data-stu-id="b249c-144">The application will map such resources to heaps later.</span></span> <span data-ttu-id="b249c-145">Os recursos desses recursos estão atualmente inalterados em D3D11, pois eles podem ser mapeados para um heap em uma granularidade de bloco de 64 KB com [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span><span class="sxs-lookup"><span data-stu-id="b249c-145">The capabilities of such resources are currently unchanged over D3D11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="b249c-146">Consulte [ **ID3D12Device:: CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span><span class="sxs-lookup"><span data-stu-id="b249c-146">Refer to [**ID3D12Device::CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)</span></span>

-   <span data-ttu-id="b249c-147">Recursos inseridos</span><span class="sxs-lookup"><span data-stu-id="b249c-147">Placed resources</span></span>

    <span data-ttu-id="b249c-148">Novo para D3D12, os aplicativos podem criar heaps separados dos recursos.</span><span class="sxs-lookup"><span data-stu-id="b249c-148">New for D3D12, applications may create heaps separate from resources.</span></span> <span data-ttu-id="b249c-149">Depois disso, o aplicativo pode localizar vários recursos em um único heap.</span><span class="sxs-lookup"><span data-stu-id="b249c-149">Afterward, the application may locate multiple resources within a single heap.</span></span> <span data-ttu-id="b249c-150">Isso pode ser feito sem criar recursos por lado ou reservados, habilitando os recursos para todos os tipos de recursos que podem ser criados diretamente por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b249c-150">This can be done without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by applications.</span></span> <span data-ttu-id="b249c-151">Vários recursos podem se sobrepor e o aplicativo deve usar o `TiledResourceBarrier` para reutilizar a memória física corretamente.</span><span class="sxs-lookup"><span data-stu-id="b249c-151">Multiple resources may overlap, and the application must use the `TiledResourceBarrier` to re-use physical memory correctly.</span></span> <span data-ttu-id="b249c-152">Consulte [ **ID3D12Device:: CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span><span class="sxs-lookup"><span data-stu-id="b249c-152">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="b249c-153">Reflexo do tamanho do recurso</span><span class="sxs-lookup"><span data-stu-id="b249c-153">Resource size reflection</span></span>

<span data-ttu-id="b249c-154">Os aplicativos devem usar a reflexão de tamanho do recurso para entender a quantidade de texturas de aparências desconhecidas que os layouts de textura são necessários em pilhas.</span><span class="sxs-lookup"><span data-stu-id="b249c-154">Applications must use resource size reflection to understand how much room textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="b249c-155">Os buffers também têm suporte, mas principalmente como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="b249c-155">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="b249c-156">Os aplicativos devem estar cientes das principais discrepâncias de alinhamento para ajudar a empacotar os recursos de forma mais densa.</span><span class="sxs-lookup"><span data-stu-id="b249c-156">Applications should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="b249c-157">Por exemplo, uma matriz de elemento único com um buffer de um byte retorna um tamanho de 64 KB e um alinhamento de 64 KB, pois os buffers atualmente só podem ser alinhados em 64 KB.</span><span class="sxs-lookup"><span data-stu-id="b249c-157">For example, a single-element array with a one-byte-buffer returns a Size of 64KB and an Alignment of 64KB, as buffers currently can only be 64KB aligned.</span></span>

<span data-ttu-id="b249c-158">Além disso, uma matriz de três elementos com duas texturas alinhadas em 64 KB de Texel e uma textura alinhada de 4MB de Texel único relatam tamanhos diferentes com base na ordem da matriz.</span><span class="sxs-lookup"><span data-stu-id="b249c-158">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="b249c-159">Se as texturas de 4MB alinhadas estiverem no meio, o tamanho resultante será 12 MB.</span><span class="sxs-lookup"><span data-stu-id="b249c-159">If the 4MB aligned textures is in the middle, the resulting Size is 12MB.</span></span> <span data-ttu-id="b249c-160">Caso contrário, o tamanho resultante será 8MB.</span><span class="sxs-lookup"><span data-stu-id="b249c-160">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="b249c-161">O alinhamento retornado sempre seria 4 MB, o super conjunto de todos os alinhamentos na matriz de recursos.</span><span class="sxs-lookup"><span data-stu-id="b249c-161">The Alignment returned would always be 4MB, the super-set of all alignments in the resource array.</span></span>

<span data-ttu-id="b249c-162">Referencie as seguintes APIs:</span><span class="sxs-lookup"><span data-stu-id="b249c-162">Reference the following APIs:</span></span>

-   [<span data-ttu-id="b249c-163">**\_Informações de \_ alocação de recursos do D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b249c-163">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
-   [<span data-ttu-id="b249c-164">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="b249c-164">**GetResourceAllocationInfo**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="b249c-165">Alinhamento do buffer</span><span class="sxs-lookup"><span data-stu-id="b249c-165">Buffer alignment</span></span>

<span data-ttu-id="b249c-166">As restrições de alinhamento de buffer não foram alteradas de D3D11, notavelmente:</span><span class="sxs-lookup"><span data-stu-id="b249c-166">Buffer alignment restrictions have not changed from D3D11, notably:</span></span>

-   <span data-ttu-id="b249c-167">4 MB para texturas com várias amostras.</span><span class="sxs-lookup"><span data-stu-id="b249c-167">4 MB for multi-sample textures.</span></span>
-   <span data-ttu-id="b249c-168">64 KB para texturas e buffers de amostra única.</span><span class="sxs-lookup"><span data-stu-id="b249c-168">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b249c-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b249c-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b249c-170">Subalocação em buffers</span><span class="sxs-lookup"><span data-stu-id="b249c-170">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




