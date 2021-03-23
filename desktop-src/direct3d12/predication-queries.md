---
title: Consultas do predicação
description: O exemplo D3D12PredicationQueries demonstra a remoção de oclusão usando heaps de consulta do DirectX 12 e predicação. O passo a passos descreve o código adicional necessário para estender o exemplo de HelloConstBuffer para manipular consultas predicação.
ms.assetid: F61817BB-45BC-4977-BE4A-EE0FDAFBCB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad14e55864ee8d568acc0c9eb46134834d27ff54
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548199"
---
# <a name="predication-queries"></a><span data-ttu-id="0ff95-104">Consultas do predicação</span><span class="sxs-lookup"><span data-stu-id="0ff95-104">Predication queries</span></span>

<span data-ttu-id="0ff95-105">O exemplo **D3D12PredicationQueries** demonstra a remoção de oclusão usando heaps de consulta do DirectX 12 e predicação.</span><span class="sxs-lookup"><span data-stu-id="0ff95-105">The **D3D12PredicationQueries** sample demonstrates occlusion culling using DirectX 12 query heaps and predication.</span></span> <span data-ttu-id="0ff95-106">O passo a passos descreve o código adicional necessário para estender o exemplo de **HelloConstBuffer** para manipular consultas predicação.</span><span class="sxs-lookup"><span data-stu-id="0ff95-106">The walkthrough describes the additional code needed to extend the **HelloConstBuffer** sample to handle predication queries.</span></span>

-   [<span data-ttu-id="0ff95-107">Criar um heap de descritor de estêncil de profundidade e um heap de consulta oclusão</span><span class="sxs-lookup"><span data-stu-id="0ff95-107">Create a depth stencil descriptor heap and an occlusion query heap</span></span>](#create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap)
-   [<span data-ttu-id="0ff95-108">Habilitar mesclagem alfa</span><span class="sxs-lookup"><span data-stu-id="0ff95-108">Enable alpha blending</span></span>](#enable-alpha-blending)
-   [<span data-ttu-id="0ff95-109">Desabilitar gravações de cores e de profundidade</span><span class="sxs-lookup"><span data-stu-id="0ff95-109">Disable color and depth writes</span></span>](#disable-color-and-depth-writes)
-   [<span data-ttu-id="0ff95-110">Criar um buffer para armazenar os resultados da consulta</span><span class="sxs-lookup"><span data-stu-id="0ff95-110">Create a buffer to store the results of the query</span></span>](#create-a-buffer-to-store-the-results-of-the-query)
-   [<span data-ttu-id="0ff95-111">Desenhar os quatro quádruplos e executar e resolver a consulta oclusão</span><span class="sxs-lookup"><span data-stu-id="0ff95-111">Draw the quads and perform and resolve the occlusion query</span></span>](#draw-the-quads-and-perform-and-resolve-the-occlusion-query)
-   [<span data-ttu-id="0ff95-112">Execute o exemplo</span><span class="sxs-lookup"><span data-stu-id="0ff95-112">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="0ff95-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ff95-113">Related topics</span></span>](#related-topics)

## <a name="create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap"></a><span data-ttu-id="0ff95-114">Criar um heap de descritor de estêncil de profundidade e um heap de consulta oclusão</span><span class="sxs-lookup"><span data-stu-id="0ff95-114">Create a depth stencil descriptor heap and an occlusion query heap</span></span>

<span data-ttu-id="0ff95-115">No método **LoadPipe** bidirecional, crie um heap de descritor de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="0ff95-115">In the **LoadPipeline** method create a depth stencil descriptor heap.</span></span>

``` syntax
              // Describe and create a depth stencil view (DSV) descriptor heap.
              D3D12_DESCRIPTOR_HEAP_DESC dsvHeapDesc = {};
              dsvHeapDesc.NumDescriptors = 1;
              dsvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_DSV;
              dsvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
              ThrowIfFailed(m_device->CreateDescriptorHeap(&dsvHeapDesc, IID_PPV_ARGS(&m_dsvHeap)));
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0ff95-116">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="0ff95-116">Call flow</span></span></th>
<th><span data-ttu-id="0ff95-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ff95-117">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0ff95-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-118"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="0ff95-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-119"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a></span></span><br />
<span data-ttu-id="0ff95-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="0ff95-120">[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ff95-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-121"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="0ff95-122">No método **Loadassets** , crie um heap para consultas oclusão.</span><span class="sxs-lookup"><span data-stu-id="0ff95-122">In the **LoadAssets** method create a heap for occlusion queries.</span></span>

``` syntax
     // Describe and create a heap for occlusion queries.
              D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
              queryHeapDesc.Count = 1;
              queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
              ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));
```



| <span data-ttu-id="0ff95-123">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="0ff95-123">Call flow</span></span>                                                 | <span data-ttu-id="0ff95-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ff95-124">Parameters</span></span>                                                |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="0ff95-125">**D3D12 \_ de \_ heap de consulta \_ desc**</span><span class="sxs-lookup"><span data-stu-id="0ff95-125">**D3D12\_QUERY\_HEAP\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc) | [<span data-ttu-id="0ff95-126">**\_Tipo de \_ heap de consulta D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="0ff95-126">**D3D12\_QUERY\_HEAP\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type) |
| [<span data-ttu-id="0ff95-127">**CreateQueryHeap**</span><span class="sxs-lookup"><span data-stu-id="0ff95-127">**CreateQueryHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)   |                                                           |



 

## <a name="enable-alpha-blending"></a><span data-ttu-id="0ff95-128">Habilitar mesclagem alfa</span><span class="sxs-lookup"><span data-stu-id="0ff95-128">Enable alpha blending</span></span>

<span data-ttu-id="0ff95-129">Este exemplo desenha dois quatro quádruplos e ilustra uma consulta oclusão binária.</span><span class="sxs-lookup"><span data-stu-id="0ff95-129">This sample draws two quads and illustrates a binary occlusion query.</span></span> <span data-ttu-id="0ff95-130">O quad na frente anima na tela e o que, em outras ocasiões, será obstruído.</span><span class="sxs-lookup"><span data-stu-id="0ff95-130">The quad in front animates across the screen, and the one in back will occasionally be occluded.</span></span> <span data-ttu-id="0ff95-131">No método **Loadassets** , a combinação alfa está habilitada para este exemplo, de modo que possamos ver em que ponto o D3D considera o quad in back obstruído.</span><span class="sxs-lookup"><span data-stu-id="0ff95-131">In the **LoadAssets** method, alpha blending is enabled for this sample so that we can see at what point D3D considers the quad in back occluded.</span></span>

``` syntax
     // Enable alpha blending so we can visualize the occlusion query results.
              CD3DX12_BLEND_DESC blendDesc(CD3DX12_DEFAULT);
              blendDesc.RenderTarget[0] =
              {
                     TRUE, FALSE,
                     D3D12_BLEND_SRC_ALPHA, D3D12_BLEND_INV_SRC_ALPHA, D3D12_BLEND_OP_ADD,
                     D3D12_BLEND_ONE, D3D12_BLEND_ZERO, D3D12_BLEND_OP_ADD,
                     D3D12_LOGIC_OP_NOOP,
                     D3D12_COLOR_WRITE_ENABLE_ALL,
              };
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0ff95-132">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="0ff95-132">Call flow</span></span></th>
<th><span data-ttu-id="0ff95-133">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ff95-133">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0ff95-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-134"><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="0ff95-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-135"><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a></span></span><br />
<span data-ttu-id="0ff95-136">[<strong>D3D12_BLEND</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend)</span><span class="sxs-lookup"><span data-stu-id="0ff95-136">[<strong>D3D12_BLEND</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend)</span></span><br />
<span data-ttu-id="0ff95-137">[<strong>D3D12_BLEND_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_blend_op)</span><span class="sxs-lookup"><span data-stu-id="0ff95-137">[<strong>D3D12_BLEND_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend_op)</span></span><br />
<span data-ttu-id="0ff95-138">[<strong>D3D12_LOGIC_OP</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_logic_op)</span><span class="sxs-lookup"><span data-stu-id="0ff95-138">[<strong>D3D12_LOGIC_OP</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_logic_op)</span></span><br />
<span data-ttu-id="0ff95-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_color_write_enable)</span><span class="sxs-lookup"><span data-stu-id="0ff95-139">[<strong>D3D12_COLOR_WRITE_ENABLE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_color_write_enable)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="disable-color-and-depth-writes"></a><span data-ttu-id="0ff95-140">Desabilitar gravações de cores e de profundidade</span><span class="sxs-lookup"><span data-stu-id="0ff95-140">Disable color and depth writes</span></span>

<span data-ttu-id="0ff95-141">A consulta oclusão é executada pela renderização de um quad que cobre a mesma área que o quad cuja visibilidade queremos testar.</span><span class="sxs-lookup"><span data-stu-id="0ff95-141">The occlusion query is performed by rendering a quad that covers the same area as the quad whose visibility we want to test.</span></span> <span data-ttu-id="0ff95-142">Em cenas mais complexas, a consulta provavelmente seria um volume delimitador, em vez de um quádruplo simples.</span><span class="sxs-lookup"><span data-stu-id="0ff95-142">In more complex scenes, the query would likely be a bounding volume, rather than a simple quad.</span></span> <span data-ttu-id="0ff95-143">Em ambos os casos, um novo estado de pipeline é criado para desabilitar a gravação no destino de renderização e no buffer z para que a consulta oclusão em si não afete a saída visível da passagem de renderização.</span><span class="sxs-lookup"><span data-stu-id="0ff95-143">In either case, a new pipeline state is created that disables writing to the render target and the z buffer so that the occlusion query itself does not affect the visible output of the rendering pass.</span></span>

<span data-ttu-id="0ff95-144">No método **Loadassets** , desabilite gravações de cores e gravações de profundidade para o estado da consulta oclusão.</span><span class="sxs-lookup"><span data-stu-id="0ff95-144">In the **LoadAssets** method, disable color writes and depth writes for the occlusion query's state.</span></span>

``` syntax
 // Disable color writes and depth writes for the occlusion query's state.
              psoDesc.BlendState.RenderTarget[0].RenderTargetWriteMask = 0;
              psoDesc.DepthStencilState.DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ZERO;

              ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_queryState)));
```



| <span data-ttu-id="0ff95-145">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="0ff95-145">Call flow</span></span>                                                                            | <span data-ttu-id="0ff95-146">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ff95-146">Parameters</span></span>                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="0ff95-147">**Desc. de estado do pipeline de \_ gráficos D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0ff95-147">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) | [<span data-ttu-id="0ff95-148">**\_Máscara de \_ gravação de profundidade de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="0ff95-148">**D3D12\_DEPTH\_WRITE\_MASK**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) |
| [<span data-ttu-id="0ff95-149">**CreateGraphicsPipelineState**</span><span class="sxs-lookup"><span data-stu-id="0ff95-149">**CreateGraphicsPipelineState**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)      |                                                             |



 

## <a name="create-a-buffer-to-store-the-results-of-the-query"></a><span data-ttu-id="0ff95-150">Criar um buffer para armazenar os resultados da consulta</span><span class="sxs-lookup"><span data-stu-id="0ff95-150">Create a buffer to store the results of the query</span></span>

<span data-ttu-id="0ff95-151">No método **Loadassets** , um buffer precisa ser criado para armazenar os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="0ff95-151">In the **LoadAssets** method a buffer needs to be created to store the results of the query.</span></span> <span data-ttu-id="0ff95-152">Cada consulta requer 8 bytes de espaço na memória da GPU.</span><span class="sxs-lookup"><span data-stu-id="0ff95-152">Each query requires 8 bytes of space in GPU memory.</span></span> <span data-ttu-id="0ff95-153">Este exemplo executa apenas uma consulta e, para simplificar e legibilidade, cria um buffer exatamente com esse tamanho (embora essa chamada de função aloque uma página de 64K de memória da GPU, a maioria dos aplicativos reais provavelmente criaria um buffer maior).</span><span class="sxs-lookup"><span data-stu-id="0ff95-153">This sample only performs one query and for simplicity and readability creates a buffer exactly that size (even though this function call will allocate a 64K page of GPU memory - most real apps would likely create a larger buffer).</span></span>

``` syntax
 // Create the query result buffer.
              CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
              auto queryBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(8);
              ThrowIfFailed(m_device->CreateCommittedResource(
                     &heapProps,
                     D3D12_HEAP_FLAG_NONE,
                     &queryBufferDesc,
                     D3D12_RESOURCE_STATE_GENERIC_READ,
                     nullptr,
                     IID_PPV_ARGS(&m_queryResult)
                     ));
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0ff95-154">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="0ff95-154">Call flow</span></span></th>
<th><span data-ttu-id="0ff95-155">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ff95-155">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0ff95-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-156"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="0ff95-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-157"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br />
<span data-ttu-id="0ff95-158">[<strong>D3D12_HEAP_TYPE</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_type)</span><span class="sxs-lookup"><span data-stu-id="0ff95-158">[<strong>D3D12_HEAP_TYPE</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)</span></span><br />
<span data-ttu-id="0ff95-159">[<strong>D3D12_HEAP_FLAG</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_heap_flags)</span><span class="sxs-lookup"><span data-stu-id="0ff95-159">[<strong>D3D12_HEAP_FLAG</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)</span></span><br />
<span data-ttu-id="0ff95-160">[<strong>CD3DX12_RESOURCE_DESC</strong>] (cd3dx12-resource-desc.md)</span><span class="sxs-lookup"><span data-stu-id="0ff95-160">[<strong>CD3DX12_RESOURCE_DESC</strong>](cd3dx12-resource-desc.md)</span></span><br />
<span data-ttu-id="0ff95-161">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="0ff95-161">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="draw-the-quads-and-perform-and-resolve-the-occlusion-query"></a><span data-ttu-id="0ff95-162">Desenhar os quatro quádruplos e executar e resolver a consulta oclusão</span><span class="sxs-lookup"><span data-stu-id="0ff95-162">Draw the quads and perform and resolve the occlusion query</span></span>

<span data-ttu-id="0ff95-163">Tendo feito a configuração, o loop principal é atualizado no método **PopulateCommandLists** .</span><span class="sxs-lookup"><span data-stu-id="0ff95-163">Having done the setup, the main loop is updated in the **PopulateCommandLists** method.</span></span>

<dl> 1. <span data-ttu-id="0ff95-164">Desenhe os quatro processadores de volta para frente para fazer com que o efeito de transparência funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="0ff95-164">Draw the quads from back to front to make the transparency effect work properly.</span></span> <span data-ttu-id="0ff95-165">Desenhar o quad de volta ao front é predicado sobre o resultado da consulta do quadro anterior e é uma técnica bastante comum para isso.</span><span class="sxs-lookup"><span data-stu-id="0ff95-165">Drawing the quad in back to front is predicated on the result of the previous frame’s query and is a fairly common technique for this.</span></span>  
2. <span data-ttu-id="0ff95-166">Altere o PSO para desabilitar o destino de renderização e as gravações de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="0ff95-166">Change the PSO to disable render target and depth stencil writes.</span></span>  
3. <span data-ttu-id="0ff95-167">Execute a consulta oclusão.</span><span class="sxs-lookup"><span data-stu-id="0ff95-167">Perform the occlusion query.</span></span>  
4. <span data-ttu-id="0ff95-168">Resolva a consulta oclusão.</span><span class="sxs-lookup"><span data-stu-id="0ff95-168">Resolve the occlusion query.</span></span>  
</dl>

``` syntax
       // Draw the quads and perform the occlusion query.
       {
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvFarQuad(m_cbvHeap->GetGPUDescriptorHandleForHeapStart(), m_frameIndex * CbvCountPerFrame, m_cbvSrvDescriptorSize);
              CD3DX12_GPU_DESCRIPTOR_HANDLE cbvNearQuad(cbvFarQuad, m_cbvSrvDescriptorSize);

              m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
              m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

              // Draw the far quad conditionally based on the result of the occlusion query
              // from the previous frame.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPredication(m_queryResult.Get(), 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->DrawInstanced(4, 1, 0, 0);

              // Disable predication and always draw the near quad.
              m_commandList->SetPredication(nullptr, 0, D3D12_PREDICATION_OP_EQUAL_ZERO);
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvNearQuad);
              m_commandList->DrawInstanced(4, 1, 4, 0);

              // Run the occlusion query with the bounding box quad.
              m_commandList->SetGraphicsRootDescriptorTable(0, cbvFarQuad);
              m_commandList->SetPipelineState(m_queryState.Get());
              m_commandList->BeginQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);
              m_commandList->DrawInstanced(4, 1, 8, 0);
              m_commandList->EndQuery(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0);

              // Resolve the occlusion query and store the results in the query result buffer
              // to be used on the subsequent frame.
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_GENERIC_READ, D3D12_RESOURCE_STATE_COPY_DEST));
              m_commandList->ResolveQueryData(m_queryHeap.Get(), D3D12_QUERY_TYPE_BINARY_OCCLUSION, 0, 1, m_queryResult.Get(), 0);
              m_commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_queryResult.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_GENERIC_READ));
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0ff95-169">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="0ff95-169">Call flow</span></span></th>
<th><span data-ttu-id="0ff95-170">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ff95-170">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0ff95-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-171"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="0ff95-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-172"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ff95-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-173"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span></span></td>
<td><span data-ttu-id="0ff95-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-174"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ff95-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-175"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="0ff95-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-176"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="0ff95-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-177"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="0ff95-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-178"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ff95-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-179"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="0ff95-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-180"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></span></span></td>
<td><span data-ttu-id="0ff95-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-181"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ff95-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-182"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="0ff95-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-183"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="0ff95-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="0ff95-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>Setpipelinestate</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="0ff95-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-186"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></span></span></td>
<td><span data-ttu-id="0ff95-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-187"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ff95-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-188"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="0ff95-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>Endquery</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-189"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></span></span></td>
<td><span data-ttu-id="0ff95-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-190"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ff95-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-191"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="0ff95-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-192"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="0ff95-193">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="0ff95-193">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ff95-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-194"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></span></span></td>
<td><span data-ttu-id="0ff95-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-195"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ff95-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-196"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><dl><span data-ttu-id="0ff95-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="0ff95-197"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br />
<span data-ttu-id="0ff95-198">[<strong>D3D12_RESOURCE_STATES</strong>] (/Windows/Desktop/API/d3d12/ne-d3d12-d3d12_resource_states)</span><span class="sxs-lookup"><span data-stu-id="0ff95-198">[<strong>D3D12_RESOURCE_STATES</strong>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="run-the-sample"></a><span data-ttu-id="0ff95-199">Execute o exemplo</span><span class="sxs-lookup"><span data-stu-id="0ff95-199">Run the sample</span></span>

<span data-ttu-id="0ff95-200">Não obstruído:</span><span class="sxs-lookup"><span data-stu-id="0ff95-200">Not occluded:</span></span>

![duas caixas não obstruído](images/not-occluded.png)

<span data-ttu-id="0ff95-202">Obstruído</span><span class="sxs-lookup"><span data-stu-id="0ff95-202">Occluded:</span></span>

![uma caixa totalmente obstruído](images/occluded.png)

<span data-ttu-id="0ff95-204">Obstruído parcialmente:</span><span class="sxs-lookup"><span data-stu-id="0ff95-204">Partially occluded:</span></span>

![obstruído uma caixa parcialmente](images/partially-occluded.png)

## <a name="related-topics"></a><span data-ttu-id="0ff95-206">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ff95-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ff95-207">Instruções passo a passo de código do D3D12</span><span class="sxs-lookup"><span data-stu-id="0ff95-207">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="0ff95-208">Predicação</span><span class="sxs-lookup"><span data-stu-id="0ff95-208">Predication</span></span>](predication.md)
</dt> <dt>

[<span data-ttu-id="0ff95-209">Consultas</span><span class="sxs-lookup"><span data-stu-id="0ff95-209">Queries</span></span>](queries.md)
</dt> </dl>

 

 
