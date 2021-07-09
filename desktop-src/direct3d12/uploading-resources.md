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
# <a name="uploading-different-types-of-resources"></a><span data-ttu-id="0d9ef-103">Carregando diferentes tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="0d9ef-103">Uploading different types of resources</span></span>

<span data-ttu-id="0d9ef-104">Mostra como usar um buffer para carregar dados de buffer constante e dados de buffer de vértice para a GPU e como sublocar e colocar corretamente os dados em buffers.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-104">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="0d9ef-105">O uso de um único buffer aumenta a flexibilidade de uso de memória e fornece aos aplicativos um controle mais rígido sobre o uso de memória.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-105">The use of a single buffer increases memory usage flexibility, and provides applications with tighter control over memory usage.</span></span> <span data-ttu-id="0d9ef-106">Também mostra as diferenças entre os modelos Direct3D 11 e Direct3D 12 para carregar diferentes tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-106">Also shows the differences between the Direct3D 11 and Direct3D 12 models for uploading different types of resources.</span></span>

## <a name="upload-different-types-of-resources"></a><span data-ttu-id="0d9ef-107">Upload tipos diferentes de recursos</span><span class="sxs-lookup"><span data-stu-id="0d9ef-107">Upload different types of resources</span></span>

<span data-ttu-id="0d9ef-108">No Direct3D 12, você cria um buffer para acomodar diferentes tipos de dados de recurso para upload e copia dados de recursos para o mesmo buffer de maneira semelhante para dados de recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-108">In Direct3D 12, you create one buffer to accommodate different types of resource data for uploading, and you copy resource data to the same buffer in a similar way for different resource data.</span></span> <span data-ttu-id="0d9ef-109">As exibições individuais são criadas para vincular esses dados de recurso ao pipeline de gráficos no modelo de associação de recursos do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-109">Individual views are then created to bind those resource data to the graphics pipeline in the Direct3D 12 resource binding model.</span></span>

<span data-ttu-id="0d9ef-110">No Direct3D 11, você cria buffers separados para diferentes tipos de dados de recurso (observe os diferentes usados no código de exemplo do Direct3D 11 abaixo), vinculando explicitamente cada buffer de recursos ao pipeline de gráficos e atualiza os dados do recurso com métodos diferentes com base em diferentes tipos de `BindFlags` recursos.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-110">In Direct3D 11, you create separate buffers for different types of resource data (note the different `BindFlags` used in the Direct3D 11 sample code below), explicitly binding each resource buffer to the graphics pipeline, and update the resource data with different methods based on different resource types.</span></span>

<span data-ttu-id="0d9ef-111">No Direct3D 12 e no Direct3D 11, você deve usar os recursos de upload somente em que a CPU gravará os dados uma vez e a GPU os lerá uma vez.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-111">In both Direct3D 12 and Direct3D 11, you should use upload resources only where the CPU will write the data once, and the GPU will read it once.</span></span>

<span data-ttu-id="0d9ef-112">Em alguns casos,</span><span class="sxs-lookup"><span data-stu-id="0d9ef-112">In some cases,</span></span>
* <span data-ttu-id="0d9ef-113">a GPU lerá os dados várias vezes ou</span><span class="sxs-lookup"><span data-stu-id="0d9ef-113">the GPU will read the data multiple times, or</span></span>
* <span data-ttu-id="0d9ef-114">a GPU não lerá os dados linearmente ou</span><span class="sxs-lookup"><span data-stu-id="0d9ef-114">the GPU won't read the data linearly, or</span></span>
* <span data-ttu-id="0d9ef-115">a renderização já é significativamente limitada por GPU.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-115">the rendering is significantly GPU-limited already.</span></span>

<span data-ttu-id="0d9ef-116">Nesses casos, a melhor opção pode ser usar [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) para copiar os dados do buffer de upload para um recurso padrão.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-116">In those cases, the better option might be to use [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) to copy the upload buffer data to a default resource.</span></span>

<span data-ttu-id="0d9ef-117">Um recurso padrão pode residir na memória de vídeo físico em GPUs discretas.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-117">A default resource can reside in physical video memory on discrete GPUs.</span></span>

### <a name="code-example-direct3d-11"></a><span data-ttu-id="0d9ef-118">Exemplo de código: Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="0d9ef-118">Code Example: Direct3D 11</span></span>

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

### <a name="code-example-direct3d-12"></a><span data-ttu-id="0d9ef-119">Exemplo de código: Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0d9ef-119">Code Example: Direct3D 12</span></span>

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

<span data-ttu-id="0d9ef-120">Observe o uso das estruturas auxiliares [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) e [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span><span class="sxs-lookup"><span data-stu-id="0d9ef-120">Note the use of the helper structures [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md).</span></span>

## <a name="constants"></a><span data-ttu-id="0d9ef-121">Constantes</span><span class="sxs-lookup"><span data-stu-id="0d9ef-121">Constants</span></span>

<span data-ttu-id="0d9ef-122">Para definir constantes, vértices e índices em um heap de upload ou readback, use as APIs a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-122">To set constants, vertices, and indexes within an upload or readback heap, use the following APIs.</span></span>

-   [<span data-ttu-id="0d9ef-123">**ID3D12Device::CreateConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="0d9ef-123">**ID3D12Device::CreateConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [<span data-ttu-id="0d9ef-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="0d9ef-124">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)
-   [<span data-ttu-id="0d9ef-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="0d9ef-125">**ID3D12GraphicsCommandList::IASetIndexBuffer**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)

## <a name="resources"></a><span data-ttu-id="0d9ef-126">Recursos</span><span class="sxs-lookup"><span data-stu-id="0d9ef-126">Resources</span></span>

<span data-ttu-id="0d9ef-127">Recursos são o conceito direct3D que abstrai o uso da memória física da GPU.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-127">Resources are the Direct3D concept that abstracts the usage of GPU physical memory.</span></span> <span data-ttu-id="0d9ef-128">Os recursos exigem espaço de endereço virtual de GPU para acessar a memória física.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-128">Resources require GPU virtual address space to access physical memory.</span></span> <span data-ttu-id="0d9ef-129">A criação de recursos é de thread livre.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-129">Resource creation is free-threaded.</span></span>

<span data-ttu-id="0d9ef-130">Há três tipos de recursos em relação à criação de endereço virtual e flexibilidade no Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-130">There are three types of resources with respect to virtual address creation and flexibility in Direct3D 12.</span></span>

### <a name="committed-resources"></a><span data-ttu-id="0d9ef-131">Recursos comprometidos</span><span class="sxs-lookup"><span data-stu-id="0d9ef-131">Committed resources</span></span>

<span data-ttu-id="0d9ef-132">Os recursos comprometidos são a ideia mais comum de recursos direct3D ao longo das gerações.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-132">Committed resources are the most common idea of Direct3D resources over the generations.</span></span> <span data-ttu-id="0d9ef-133">A criação desse recurso aloca o intervalo de endereços virtuais, um heap implícito grande o suficiente para se ajustar a todo o recurso e confirma o intervalo de endereços virtuais para a memória física encapsulada pelo heap.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-133">Creating such a resource allocates virtual address range, an implicit heap large enough to fit the whole resource, and commits the virtual address range to the physical memory encapsulated by the heap.</span></span> <span data-ttu-id="0d9ef-134">As propriedades de heap implícitas devem ser passadas para corresponder a paridade funcional com versões anteriores do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-134">The implicit heap properties must be passed to match functional parity with previous Direct3D versions.</span></span> <span data-ttu-id="0d9ef-135">Consulte [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="0d9ef-135">Refer to [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>

### <a name="reserved-resources"></a><span data-ttu-id="0d9ef-136">Recursos reservados</span><span class="sxs-lookup"><span data-stu-id="0d9ef-136">Reserved resources</span></span>

<span data-ttu-id="0d9ef-137">Os recursos reservados são equivalentes aos recursos lado a lado do Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-137">Reserved resources are equivalent to Direct3D 11 tiled resources.</span></span> <span data-ttu-id="0d9ef-138">Na criação, somente um intervalo de endereços virtuais é alocado e não mapeado para nenhum heap.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-138">On their creation, only a virtual address range is allocated, and not mapped to any heap.</span></span> <span data-ttu-id="0d9ef-139">O aplicativo mapeará esses recursos para heaps posteriormente.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-139">The application will map such resources to heaps later.</span></span> <span data-ttu-id="0d9ef-140">Atualmente, os recursos desses recursos são inalterados do Direct3D 11, pois eles podem ser mapeados para um heap em uma granularidade de bloco de 64KB com [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span><span class="sxs-lookup"><span data-stu-id="0d9ef-140">The capabilities of such resources are currently unchanged from Direct3D 11, as they can be mapped to a heap at a 64KB tile granularity with [**UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings).</span></span> <span data-ttu-id="0d9ef-141">Consulte [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span><span class="sxs-lookup"><span data-stu-id="0d9ef-141">Refer to [**ID3D12Device::CreateReservedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource).</span></span>

### <a name="placed-resources"></a><span data-ttu-id="0d9ef-142">Recursos colocados</span><span class="sxs-lookup"><span data-stu-id="0d9ef-142">Placed resources</span></span>

<span data-ttu-id="0d9ef-143">Novo para o Direct3D 12, você pode criar heaps separados dos recursos.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-143">New for Direct3D 12, you can create heaps separate from resources.</span></span> <span data-ttu-id="0d9ef-144">Posteriormente, você pode localizar vários recursos em um único heap.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-144">Afterward, you can locate multiple resources within a single heap.</span></span> <span data-ttu-id="0d9ef-145">Você pode fazer isso sem criar recursos reservados ou lado a lado, permitindo que os recursos de todos os tipos de recursos possam ser criados diretamente pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-145">You can do that without creating tiled or reserved resources, enabling the capabilities for all resource types able to be created directly by your application.</span></span> <span data-ttu-id="0d9ef-146">Vários recursos podem se sobrepor e você deve usar [**o ID3D12GraphicsCommandList::ResourceBagraphic**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) para re-usar a memória física corretamente.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-146">Multiple resources might overlap, and you must use the [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) to re-use physical memory correctly.</span></span> <span data-ttu-id="0d9ef-147">Consulte [**ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span><span class="sxs-lookup"><span data-stu-id="0d9ef-147">Refer to [**ID3D12Device::CreatePlacedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource).</span></span>

## <a name="resource-size-reflection"></a><span data-ttu-id="0d9ef-148">Reflexão do tamanho do recurso</span><span class="sxs-lookup"><span data-stu-id="0d9ef-148">Resource size reflection</span></span>

<span data-ttu-id="0d9ef-149">Você deve usar a reflexão de tamanho do recurso para entender quanto texturas de espaço com layouts de textura desconhecidos exigem em heaps.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-149">You must use resource size reflection to understand how much space textures with unknown texture layouts require in heaps.</span></span> <span data-ttu-id="0d9ef-150">Buffers também têm suporte, mas principalmente como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-150">Buffers are also supported, but mostly as a convenience.</span></span>

<span data-ttu-id="0d9ef-151">Você deve estar ciente das principais discrepâncias de alinhamento para ajudar a empacotar recursos mais densamente.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-151">You should be aware of major alignment discrepancies, to help pack resources more densely.</span></span>

<span data-ttu-id="0d9ef-152">Por exemplo, uma matriz de elemento único com um  buffer de um byte  retorna um Tamanho de 64KB e um Alinhamento de 64KB, porque os buffers podem ser alinhados apenas a 64KB.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-152">For example, a single-element array with a one-byte-buffer returns a *Size* of 64KB, and an *Alignment* of 64KB, because buffers can be only 64KB-aligned.</span></span>

<span data-ttu-id="0d9ef-153">Além disso, uma matriz de três elementos com duas texturas alinhadas de 64KB de single-texel e uma textura alinhada de 4 MB de um único texel relata tamanhos diferentes com base na ordem da matriz.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-153">Also, a three element array with two single-texel 64KB aligned textures and a single-texel 4MB aligned texture reports differing sizes based on the order of the array.</span></span> <span data-ttu-id="0d9ef-154">Se as texturas alinhadas de 4 MB estão no meio, o *Tamanho* resultante é de 12 MB.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-154">If the 4MB aligned textures is in the middle, then the resulting *Size* is 12MB.</span></span> <span data-ttu-id="0d9ef-155">Caso contrário, o Tamanho resultante será de 8 MB.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-155">Otherwise, the resulting Size is 8MB.</span></span> <span data-ttu-id="0d9ef-156">O Alinhamento retornado sempre seria de 4 MB, o superconjunto de todos os alinhamentos na matriz de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-156">The Alignment returned would always be 4MB, the superset of all alignments in the resource array.</span></span>

<span data-ttu-id="0d9ef-157">Consulte as APIs a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-157">Reference the following APIs.</span></span>

- [<span data-ttu-id="0d9ef-158">**D3D12 \_ INFORMAÇÕES DE \_ ALOCAÇÃO DE \_ RECURSOS**</span><span class="sxs-lookup"><span data-stu-id="0d9ef-158">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
- [<span data-ttu-id="0d9ef-159">**GetResourceAllocationInfo**</span><span class="sxs-lookup"><span data-stu-id="0d9ef-159">**GetResourceAllocationInfo**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="buffer-alignment"></a><span data-ttu-id="0d9ef-160">Alinhamento do buffer</span><span class="sxs-lookup"><span data-stu-id="0d9ef-160">Buffer alignment</span></span>

<span data-ttu-id="0d9ef-161">As restrições de alinhamento do buffer não foram alteradas do Direct3D 11, principalmente:</span><span class="sxs-lookup"><span data-stu-id="0d9ef-161">Buffer alignment restrictions have not changed from Direct3D 11, notably:</span></span>

- <span data-ttu-id="0d9ef-162">4 MB para texturas de várias amostras.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-162">4 MB for multi-sample textures.</span></span>
- <span data-ttu-id="0d9ef-163">64 KB para texturas e buffers de amostra única.</span><span class="sxs-lookup"><span data-stu-id="0d9ef-163">64 KB for single-sample textures and buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d9ef-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d9ef-164">Related topics</span></span>

* [<span data-ttu-id="0d9ef-165">Sublocação em buffers</span><span class="sxs-lookup"><span data-stu-id="0d9ef-165">Suballocation within buffers</span></span>](large-buffers.md)
