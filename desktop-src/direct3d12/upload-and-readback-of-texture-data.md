---
title: Carregando dados de textura por meio de buffers
description: Carregar dados de textura 2D ou 3D é semelhante a carregar dados 1D, exceto que os aplicativos precisam prestar mais atenção ao alinhamento de dados relacionado à densidade da linha.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadbd1e71b3c9895b75c973397488472b57f8eb1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548312"
---
# <a name="uploading-texture-data-through-buffers"></a><span data-ttu-id="58b18-103">Carregando dados de textura por meio de buffers</span><span class="sxs-lookup"><span data-stu-id="58b18-103">Uploading Texture Data Through Buffers</span></span>

<span data-ttu-id="58b18-104">Carregar dados de textura 2D ou 3D é semelhante a carregar dados 1D, exceto que os aplicativos precisam prestar mais atenção ao alinhamento de dados relacionado à densidade da linha.</span><span class="sxs-lookup"><span data-stu-id="58b18-104">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="58b18-105">Os buffers podem ser usados de forma ortogonal e simultânea de várias partes do pipeline de gráficos e são muito flexíveis.</span><span class="sxs-lookup"><span data-stu-id="58b18-105">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span>

-   [<span data-ttu-id="58b18-106">Carregar dados de textura por meio de buffers</span><span class="sxs-lookup"><span data-stu-id="58b18-106">Upload Texture Data via Buffers</span></span>](#upload-texture-data-via-buffers)
-   [<span data-ttu-id="58b18-107">Copia</span><span class="sxs-lookup"><span data-stu-id="58b18-107">Copying</span></span>](#copying)
-   [<span data-ttu-id="58b18-108">Mapeamento e desmapeamento</span><span class="sxs-lookup"><span data-stu-id="58b18-108">Mapping and unmapping</span></span>](#mapping-and-unmapping)
-   [<span data-ttu-id="58b18-109">Alinhamento do buffer</span><span class="sxs-lookup"><span data-stu-id="58b18-109">Buffer alignment</span></span>](#buffer-alignment)
-   [<span data-ttu-id="58b18-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58b18-110">Related topics</span></span>](#related-topics)

## <a name="upload-texture-data-via-buffers"></a><span data-ttu-id="58b18-111">Carregar dados de textura por meio de buffers</span><span class="sxs-lookup"><span data-stu-id="58b18-111">Upload Texture Data via Buffers</span></span>

<span data-ttu-id="58b18-112">Os aplicativos devem carregar dados por meio de [**ID3D12GraphicsCommandList:: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList:: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span><span class="sxs-lookup"><span data-stu-id="58b18-112">Applications must upload data via [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) or [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion).</span></span> <span data-ttu-id="58b18-113">É muito mais provável que os dados de textura sejam maiores, acessados repetidamente e se beneficiem da coerência de cache aprimorada de layouts de memória não linear do que outros dados de recurso.</span><span class="sxs-lookup"><span data-stu-id="58b18-113">Texture data is much more likely to be larger, accessed repeatedly, and benefit from the improved cache-coherency of non-linear memory layouts than other resource data.</span></span> <span data-ttu-id="58b18-114">Quando os buffers são usados no D3D12, os aplicativos têm controle total sobre o posicionamento de dados e a organização associada à cópia de dados de recurso, desde que os requisitos de alinhamento de memória sejam atendidos.</span><span class="sxs-lookup"><span data-stu-id="58b18-114">When buffers are used in D3D12, applications have full control on data placement and arrangement associated with copying resource data around, as long as the memory alignment requirements are satisfied.</span></span>

<span data-ttu-id="58b18-115">O exemplo destaca onde o aplicativo simplesmente achata os dados 2D em 1D antes de colocá-los no buffer.</span><span class="sxs-lookup"><span data-stu-id="58b18-115">The sample highlights where the application simply flattens 2D data into 1D before placing it in the buffer.</span></span> <span data-ttu-id="58b18-116">Para o cenário mipmap 2D, o aplicativo pode mesclar cada subrecurso discretamente e usar rapidamente um algoritmo de subalocação 1D ou usar uma técnica de subalocação 2D mais complicada para minimizar a utilização da memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="58b18-116">For the mipmap 2D scenario, the application can either flatten each sub-resource discretely and quickly use a 1D sub-allocation algorithm, or, use a more complicated 2D sub-allocation technique to minimize video memory utilization.</span></span> <span data-ttu-id="58b18-117">Espera-se que a primeira técnica seja usada com mais frequência, pois é mais simples.</span><span class="sxs-lookup"><span data-stu-id="58b18-117">The first technique is expected to be used more often as it is simpler.</span></span> <span data-ttu-id="58b18-118">A segunda técnica pode ser útil ao empacotar dados em um disco ou em uma rede.</span><span class="sxs-lookup"><span data-stu-id="58b18-118">The second technique may be useful when packing data onto a disk or across a network.</span></span> <span data-ttu-id="58b18-119">Em ambos os casos, o aplicativo ainda deve chamar as APIs de cópia para cada subrecurso.</span><span class="sxs-lookup"><span data-stu-id="58b18-119">In either case, the application must still call the copy APIs for each sub-resource.</span></span>

``` syntax
// Prepare a pBitmap in memory, with bitmapWidth, bitmapHeight, and pixel format of DXGI_FORMAT_B8G8R8A8_UNORM. 
//
// Sub-allocate from the buffer for texture data.
//

D3D12_SUBRESOURCE_FOOTPRINT pitchedDesc = { 0 };
pitchedDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
pitchedDesc.Width = bitmapWidth;
pitchedDesc.Height = bitmapHeight;
pitchedDesc.Depth = 1;
pitchedDesc.RowPitch = Align(bitmapWidth * sizeof(DWORD), D3D12_TEXTURE_DATA_PITCH_ALIGNMENT);

//
// Note that the helper function UpdateSubresource in D3DX12.h, and ID3D12Device::GetCopyableFootprints 
// can help applications fill out D3D12_SUBRESOURCE_FOOTPRINT and D3D12_PLACED_SUBRESOURCE_FOOTPRINT structures.
//
// Refer to the D3D12 Code example for the previous section "Uploading Different Types of Resources"
// for the code for SuballocateFromBuffer.
//

SuballocateFromBuffer(
    pitchedDesc.Height * pitchedDesc.RowPitch,
    D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT
    );

D3D12_PLACED_SUBRESOURCE_FOOTPRINT placedTexture2D = { 0 };
placedTexture2D.Offset = m_pDataCur – m_pDataBegin;
placedTexture2D.Footprint = pitchedDesc;

//
// Copy texture data from DWORD* pBitmap->pixels to the buffer
//

for (UINT y = 0; y < bitmapHeight; y++)
{
  UINT8 *pScan = m_pDataBegin + placedTexture2D.Offset + y * pitchedDesc.RowPitch;
  memcpy( pScan, &(pBitmap->pixels[y * bitmapWidth]), sizeof(DWORD) * bitmapWidth );
}

//
// Create default texture2D resource.
//

D3D12_RESOURCE_DESC  textureDesc { ... };

CComPtr<ID3D12Resource> texture2D;
d3dDevice->CreateCommittedResource( 
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT), 
        D3D12_HEAP_FLAG_NONE, &textureDesc, 
        D3D12_RESOURCE_STATE_COPY_DEST, 
        nullptr, 
        IID_PPV_ARGS(&texture2D) );

//
// Copy heap data to texture2D.
//

commandList->CopyTextureRegion( 
        &CD3DX12_TEXTURE_COPY_LOCATION( texture2D, 0 ), 
        0, 0, 0, 
        &CD3DX12_TEXTURE_COPY_LOCATION( m_spUploadHeap, placedTexture2D ), 
        nullptr );
```

<span data-ttu-id="58b18-120">Observe o uso das estruturas auxiliares [**CD3DX12 \_ heap de \_ Propriedades**](cd3dx12-heap-properties.md) e [**\_ \_ \_ local de cópia de textura CD3DX12**](cd3dx12-texture-copy-location.md)e os métodos [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) e [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span><span class="sxs-lookup"><span data-stu-id="58b18-120">Note the use of the helper structures [**CD3DX12\_HEAP\_PROPERTIES**](cd3dx12-heap-properties.md) and [**CD3DX12\_TEXTURE\_COPY\_LOCATION**](cd3dx12-texture-copy-location.md), and the methods [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) and [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).</span></span>

## <a name="copying"></a><span data-ttu-id="58b18-121">Copiando</span><span class="sxs-lookup"><span data-stu-id="58b18-121">Copying</span></span>

<span data-ttu-id="58b18-122">Os métodos D3D12 permitem que os aplicativos substituam os dados de D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)e Resource inicial.</span><span class="sxs-lookup"><span data-stu-id="58b18-122">D3D12 methods enable applications to replace D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion), and resource initial data.</span></span> <span data-ttu-id="58b18-123">Um único subrecurso 3D digno de dados de textura de linha principal pode estar localizado em recursos de buffer.</span><span class="sxs-lookup"><span data-stu-id="58b18-123">A single 3D subresource worth of row-major texture data may be located in buffer resources.</span></span> <span data-ttu-id="58b18-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) pode copiar esses dados de textura do buffer para um recurso de textura com um layout de textura desconhecido e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="58b18-124">[**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) can copy that texture data from the buffer to a texture resource with an unknown texture layout, and vice versa.</span></span> <span data-ttu-id="58b18-125">Os aplicativos devem preferir esse tipo de técnica para popular os recursos de GPU acessados com frequência, criando buffers grandes em um heap de carregamento ao criar os recursos de GPU acessados com frequência em um heap padrão que não tem acesso à CPU.</span><span class="sxs-lookup"><span data-stu-id="58b18-125">Applications should prefer this type of technique to populate frequently accessed GPU resources, by creating large buffers in an UPLOAD heap while creating the frequently accessed GPU resources in a DEFAULT heap that has no CPU access.</span></span> <span data-ttu-id="58b18-126">Uma técnica tão eficientemente dá suporte a GPUs discretas e a suas grandes quantidades de memória inacessível por CPU, sem o uso comum de arquiteturas de uma.</span><span class="sxs-lookup"><span data-stu-id="58b18-126">Such a technique efficiently supports discrete GPUs and their large amounts of CPU-inaccessible memory, without commonly impairing UMA architectures.</span></span>

<span data-ttu-id="58b18-127">Observe as duas constantes a seguir:</span><span class="sxs-lookup"><span data-stu-id="58b18-127">Note the following two constants:</span></span>

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [<span data-ttu-id="58b18-128">**\_Superfície do SUBrecurso do D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="58b18-128">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [<span data-ttu-id="58b18-129">**D3D12 \_ colocou a \_ superfície do subrecurso \_**</span><span class="sxs-lookup"><span data-stu-id="58b18-129">**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [<span data-ttu-id="58b18-130">**\_Local de \_ cópia de textura D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="58b18-130">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [<span data-ttu-id="58b18-131">**\_Tipo de \_ cópia de textura D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="58b18-131">**D3D12\_TEXTURE\_COPY\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [<span data-ttu-id="58b18-132">**ID3D12Device:: GetCopyableFootprints**</span><span class="sxs-lookup"><span data-stu-id="58b18-132">**ID3D12Device::GetCopyableFootprints**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [<span data-ttu-id="58b18-133">**ID3D12GraphicsCommandList::CopyResource**</span><span class="sxs-lookup"><span data-stu-id="58b18-133">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="58b18-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="58b18-134">**ID3D12GraphicsCommandList::CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="58b18-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="58b18-135">**ID3D12GraphicsCommandList::CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="58b18-136">**ID3D12GraphicsCommandList::CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="58b18-136">**ID3D12GraphicsCommandList::CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="58b18-137">**ID3D12CommandQueue::UpdateTileMappings**</span><span class="sxs-lookup"><span data-stu-id="58b18-137">**ID3D12CommandQueue::UpdateTileMappings**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a><span data-ttu-id="58b18-138">Mapeamento e desmapeamento</span><span class="sxs-lookup"><span data-stu-id="58b18-138">Mapping and unmapping</span></span>

<span data-ttu-id="58b18-139">[**Mapear**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) e cancelar o [**mapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) podem ser chamados por vários threads com segurança.</span><span class="sxs-lookup"><span data-stu-id="58b18-139">[**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) can be called by multiple threads safely.</span></span> <span data-ttu-id="58b18-140">A primeira chamada para **MAP** aloca um intervalo de endereços virtuais de CPU para o recurso.</span><span class="sxs-lookup"><span data-stu-id="58b18-140">The first call to **Map** allocates a CPU virtual address range for the resource.</span></span> <span data-ttu-id="58b18-141">A última chamada para o **mapeamento** Desaloca o intervalo de endereços virtuais da CPU.</span><span class="sxs-lookup"><span data-stu-id="58b18-141">The last call to **Unmap** deallocates the CPU virtual address range.</span></span> <span data-ttu-id="58b18-142">O endereço virtual da CPU é normalmente retornado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="58b18-142">The CPU virtual address is commonly returned to the application.</span></span>

<span data-ttu-id="58b18-143">Sempre que os dados são passados entre a CPU e a GPU por meio de recursos em heaps readback, o [**MAP**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) e o [**mapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) devem ser usados para dar suporte a todos os sistemas D3D12 com suporte no.</span><span class="sxs-lookup"><span data-stu-id="58b18-143">Whenever data is passed between the CPU and GPU through resources in readback heaps, [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) must be used to support all systems D3D12 is supported on.</span></span> <span data-ttu-id="58b18-144">Manter os intervalos o mais rígido possível maximiza a eficiência nos sistemas que exigem intervalos (consulte o [**\_ intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span><span class="sxs-lookup"><span data-stu-id="58b18-144">Keeping the ranges as tight as possible maximizes efficiency on the systems that require ranges (refer to [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).</span></span>

<span data-ttu-id="58b18-145">O desempenho das ferramentas de depuração beneficia-se não apenas do uso preciso de intervalos em todas as chamadas de mapeamento de [**mapa**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) , mas também de aplicativos desmapeando recursos quando as modificações de CPU não forem mais feitas.</span><span class="sxs-lookup"><span data-stu-id="58b18-145">The performance of debugging tools benefit not only from the accurate usage of ranges on all [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) / [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) calls, but also from applications unmapping resources when CPU modifications will no longer be made.</span></span>

<span data-ttu-id="58b18-146">O método D3D11 do uso de [**MAP**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (com o conjunto de parâmetros de descarte) para renomear recursos não tem suporte em D3D12.</span><span class="sxs-lookup"><span data-stu-id="58b18-146">The D3D11 method of using [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (with the DISCARD parameter set) to rename resources is not supported in D3D12.</span></span> <span data-ttu-id="58b18-147">Os aplicativos devem implementar a renomeação de recursos em si.</span><span class="sxs-lookup"><span data-stu-id="58b18-147">Applications must implement resource renaming themselves.</span></span> <span data-ttu-id="58b18-148">Todas as chamadas de **mapa** são implicitamente sem \_ substituição e multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="58b18-148">All **Map** calls are implicitly NO\_OVERWRITE and multi-threaded.</span></span> <span data-ttu-id="58b18-149">É responsabilidade do aplicativo garantir que qualquer trabalho de GPU relevante contido nas listas de comandos seja concluído antes de acessar os dados com a CPU.</span><span class="sxs-lookup"><span data-stu-id="58b18-149">It is the application’s responsibility to ensure that any relevant GPU work contained in command lists is finished before the accessing data with the CPU.</span></span> <span data-ttu-id="58b18-150">As chamadas D3D12 para **MAP** não liberam implicitamente nenhum buffer de comando, nem bloqueiam a espera do trabalho de conclusão da GPU.</span><span class="sxs-lookup"><span data-stu-id="58b18-150">D3D12 calls to **Map** do not implicitly flush any command buffers, nor do they block waiting for the GPU to finish work.</span></span> <span data-ttu-id="58b18-151">Como resultado, o **mapeamento** e o [**desmapeamento**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) podem até mesmo ser otimizados em alguns cenários.</span><span class="sxs-lookup"><span data-stu-id="58b18-151">As a result, **Map** and [**Unmap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) may even be optimized out in some scenarios.</span></span>

## <a name="buffer-alignment"></a><span data-ttu-id="58b18-152">Alinhamento do buffer</span><span class="sxs-lookup"><span data-stu-id="58b18-152">Buffer alignment</span></span>

<span data-ttu-id="58b18-153">Restrições de alinhamento de buffer:</span><span class="sxs-lookup"><span data-stu-id="58b18-153">Buffer alignment restrictions:</span></span>

-   <span data-ttu-id="58b18-154">A cópia linear de subrecurso deve estar alinhada a 512 bytes (com a densidade de linha alinhada aos \_ bytes de alinhamento de densidade de dados de textura D3D12 \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="58b18-154">Linear subresource copying must be aligned to 512 bytes (with the row pitch aligned to D3D12\_TEXTURE\_DATA\_PITCH\_ALIGNMENT bytes).</span></span>
-   <span data-ttu-id="58b18-155">As leituras de dados constantes devem ser um múltiplo de 256 bytes do início do heap (ou seja, somente de endereços que são de 256 bytes alinhados).</span><span class="sxs-lookup"><span data-stu-id="58b18-155">Constant data reads must be a multiple of 256 bytes from the beginning of the heap (i.e. only from addresses that are 256-byte aligned).</span></span>
-   <span data-ttu-id="58b18-156">As leituras de dados de índice devem ser um múltiplo do tamanho do tipo de dados de índice (ou seja, somente de endereços que são naturalmente alinhados para os dados).</span><span class="sxs-lookup"><span data-stu-id="58b18-156">Index data reads must be a multiple of the index data type size (i.e. only from addresses that are naturally aligned for the data).</span></span>
-   <span data-ttu-id="58b18-157">[**ID3D12GraphicsCommandList::D rawinstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) e [**ID3D12GraphicsCommandList:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) os dados de rawindexedinstanced de:D devem ser de deslocamentos que são múltiplos de 4 (ou seja, somente de endereços que são alinhados em DWORD).</span><span class="sxs-lookup"><span data-stu-id="58b18-157">[**ID3D12GraphicsCommandList::DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) and [**ID3D12GraphicsCommandList::DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) data must be from offsets that are multiples of 4 (i.e. only from addresses that are DWORD aligned).</span></span>

## <a name="related-topics"></a><span data-ttu-id="58b18-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58b18-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58b18-159">Subalocação em buffers</span><span class="sxs-lookup"><span data-stu-id="58b18-159">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 