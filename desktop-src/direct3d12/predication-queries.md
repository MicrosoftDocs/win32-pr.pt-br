---
title: Consultas de predicação
description: O exemplo D3D12PredicationQueries demonstra a eliminação de oclusão usando heaps de consulta e predicação do DirectX 12. O passo a passo descreve o código adicional necessário para estender o exemplo HelloConstBuffer para lidar com consultas de pré-sindicalidade.
ms.assetid: F61817BB-45BC-4977-BE4A-EE0FDAFBCB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d37bd4653ec7610e36214cce31955f1742e5b27a42a381cc2aa7d758daaf5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733380"
---
# <a name="predication-queries"></a>Consultas de predicação

O **exemplo D3D12PredicationQueries** demonstra a eliminação de oclusão usando heaps de consulta e predicação do DirectX 12. O passo a passo descreve o código adicional necessário para estender o **exemplo HelloConstBuffer** para lidar com consultas de pré-sindicalidade.

-   [Criar um heap de descritor de estêncil de profundidade e um heap de consulta de oclusão](#create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap)
-   [Habilitar a combinação alfa](#enable-alpha-blending)
-   [Desabilitar gravações de cores e profundidade](#disable-color-and-depth-writes)
-   [Criar um buffer para armazenar os resultados da consulta](#create-a-buffer-to-store-the-results-of-the-query)
-   [Desenhar os quads e executar e resolver a consulta de oclusão](#draw-the-quads-and-perform-and-resolve-the-occlusion-query)
-   [Executar o exemplo](#run-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="create-a-depth-stencil-descriptor-heap-and-an-occlusion-query-heap"></a>Criar um heap de descritor de estêncil de profundidade e um heap de consulta de oclusão

No método **LoadPipeline,** crie um heap de descritor de estêncil de profundidade.

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
<th>Fluxo de chamada</th>
<th>Parâmetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc"><strong>D3D12_DESCRIPTOR_HEAP_DESC</strong></a></td>
<td><dl><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type"><strong>D3D12_DESCRIPTOR_HEAP_TYPE</strong></a><br />
[<strong>D3D12_DESCRIPTOR_HEAP_FLAG</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap"><strong>CreateDescriptorHeap</strong></a></td>

</tr>
</tbody>
</table>



 

No método **LoadAssets,** crie um heap para consultas de oclusão.

``` syntax
     // Describe and create a heap for occlusion queries.
              D3D12_QUERY_HEAP_DESC queryHeapDesc = {};
              queryHeapDesc.Count = 1;
              queryHeapDesc.Type = D3D12_QUERY_HEAP_TYPE_OCCLUSION;
              ThrowIfFailed(m_device->CreateQueryHeap(&queryHeapDesc, IID_PPV_ARGS(&m_queryHeap)));
```



| Fluxo de chamada                                                 | Parâmetros                                                |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**DESC DE HEAP DE CONSULTA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc) | [**TIPO DE HEAP DE CONSULTA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type) |
| [**CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap)   |                                                           |



 

## <a name="enable-alpha-blending"></a>Habilitar a combinação alfa

Este exemplo desenha dois quads e ilustra uma consulta de oclusão binária. O quad na frente é animado pela tela e o que está atrás ocasionalmente será ocluído. No método **LoadAssets,** a combinação alfa é habilitada para este exemplo para que possamos ver em que ponto d3D considera o quad in back occluded.

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
<th>Fluxo de chamada</th>
<th>Parâmetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="cd3dx12-blend-desc.md"><strong>CD3DX12_BLEND_DESC</strong></a></td>
<td><dl><a href="cd3dx12-default.md"><strong>CD3DX12_DEFAULT</strong></a><br />
[<strong>D3D12_BLEND</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend)<br />
[<strong>D3D12_BLEND_OP</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_blend_op)<br />
[<strong>D3D12_LOGIC_OP</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_logic_op)<br />
[<strong>D3D12_COLOR_WRITE_ENABLE</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_color_write_enable)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="disable-color-and-depth-writes"></a>Desabilitar gravações de cores e profundidade

A consulta de oclusão é executada renderizar um quad que abrange a mesma área que o quad cuja visibilidade desejamos testar. Em cenas mais complexas, a consulta provavelmente seria um volume delimitante, em vez de um quad simples. Em ambos os casos, é criado um novo estado de pipeline que desabilita a escrita no destino de renderização e no buffer z para que a consulta de oclusão em si não afete a saída visível da passagem de renderização.

No método **LoadAssets,** desabilite gravações de cores e gravações de profundidade para o estado da consulta de oclusão.

``` syntax
 // Disable color writes and depth writes for the occlusion query's state.
              psoDesc.BlendState.RenderTarget[0].RenderTargetWriteMask = 0;
              psoDesc.DepthStencilState.DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ZERO;

              ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_queryState)));
```



| Fluxo de chamada                                                                            | Parâmetros                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) | [**MÁSCARA DE GRAVAÇÃO DE PROFUNDIDADE D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) |
| [**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)      |                                                             |



 

## <a name="create-a-buffer-to-store-the-results-of-the-query"></a>Criar um buffer para armazenar os resultados da consulta

No método **LoadAssets,** um buffer precisa ser criado para armazenar os resultados da consulta. Cada consulta requer 8 bytes de espaço na memória da GPU. Este exemplo executa apenas uma consulta e, para simplificar e ler, cria um buffer exatamente desse tamanho (embora essa chamada de função aloque uma página de 64K de memória de GPU– a maioria dos aplicativos reais provavelmente criaria um buffer maior).

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
<th>Fluxo de chamada</th>
<th>Parâmetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></td>
<td><dl><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a><br />
[<strong>D3D12_HEAP_TYPE</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)<br />
[<strong>D3D12_HEAP_FLAG</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags)<br />
[<strong>CD3DX12_RESOURCE_DESC</strong>] (cd3dx12-resource-desc.md)<br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="draw-the-quads-and-perform-and-resolve-the-occlusion-query"></a>Desenhar os quads e executar e resolver a consulta de oclusão

Depois de fazer a instalação, o loop principal é atualizado no **método PopulateCommandLists.**

<dl> 1. Desenhe os quads de trás para a frente para fazer com que o efeito de transparência funcione corretamente. Desenhar o quad de volta para frente é predicado no resultado da consulta do quadro anterior e é uma técnica bastante comum para isso.  
2. Altere o PSO para desabilitar as gravações de estêncil de destino e profundidade de renderização.  
3. Execute a consulta de oclusão.  
4. Resolva a consulta de oclusão.  
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
<th>Fluxo de chamada</th>
<th>Parâmetros</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></td>
<td><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication"><strong>SetPredication</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op"><strong>D3D12_PREDICATION_OP</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable"><strong>SetGraphicsRootDescriptorTable</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate"><strong>SetPipelineState</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery"><strong>BeginQuery</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced"><strong>DrawInstanced</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery"><strong>EndQuery</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata"><strong>ResolveQueryData</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type"><strong>D3D12_QUERY_TYPE</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></td>
<td><dl><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a><br />
[<strong>D3D12_RESOURCE_STATES</strong>] (/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="run-the-sample"></a>Execute o exemplo

Não ocluído:

![duas caixas não obstruído](images/not-occluded.png)

Obstruído

![uma caixa totalmente obstruído](images/occluded.png)

Obstruído parcialmente:

![obstruído uma caixa parcialmente](images/partially-occluded.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia detalhado do código D3D12](d3d12-code-walk-throughs.md)
</dt> <dt>

[Predicação](predication.md)
</dt> <dt>

[Consultas](queries.md)
</dt> </dl>

 

 
