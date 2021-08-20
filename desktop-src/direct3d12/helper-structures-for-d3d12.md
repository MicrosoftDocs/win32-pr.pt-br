---
title: Estruturas auxiliares para Direct3D 12
description: Essas estruturas auxiliares ajudam a inicializar muitas das estruturas do Direct3D 12. Eles são declarados em `d3dx12.h` .
ms.assetid: 822CACCE-4A45-4104-91BD-4968A657662E
keywords:
- Estruturas auxiliares
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 07/28/2021
ms.openlocfilehash: 16dfa0349a815a07db810d67c21747cb767f7c39
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812363"
---
# <a name="helper-structures-for-direct3d-12"></a>Estruturas auxiliares para Direct3D 12

Essas estruturas auxiliares ajudam a inicializar muitas das estruturas do Direct3D 12. Eles são declarados em `d3dx12.h` .

`d3dx12.h` está disponível separadamente dos cabeçalhos do Direct3D 12. Você pode baixar `d3dx12.h` da [biblioteca auxiliar do D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**CD3DX12_BLEND_DESC**](cd3dx12-blend-desc.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_BLEND_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_blend_desc) . |
| [**CD3DX12_BOX**](cd3dx12-box.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_BOX**](/windows/win32/api/d3d12/ns-d3d12-d3d12_box) . |
| [**CD3DX12_CLEAR_VALUE**](cd3dx12-clear-value.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_CLEAR_VALUE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value) . |
| [**CD3DX12_CPU_DESCRIPTOR_HANDLE**](cd3dx12-cpu-descriptor-handle.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) . |
| [**CD3DX12_DEFAULT**](cd3dx12-default.md) | Passa **D3D12_DEFAULT** para um construtor para cada estrutura auxiliar. Essa estrutura é simplesmente usada como um mecanismo para definir parâmetros padrão em outras estruturas auxiliares. |
| [**CD3DX12_DEPTH_STENCIL_DESC**](cd3dx12-depth-stencil-desc.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_DEPTH_STENCIL_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) . |
| [**CD3DX12_DEPTH_STENCIL_DESC1**](cd3dx12-depth-stencil-desc1.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_DEPTH_STENCIL_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) . |
| [**CD3DX12_DESCRIPTOR_RANGE**](cd3dx12-descriptor-range.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_DESCRIPTOR_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range) . |
| [**CD3DX12_DESCRIPTOR_RANGE1**](cd3dx12-descriptor-range1.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_DESCRIPTOR_RANGE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_range1) . |
| [**CD3DX12_DXIL_LIBRARY_SUBOBJECT**](cd3dx12-dxil-library-subobject.md) | Uma classe auxiliar para criar um subobjeto de estado de biblioteca DXIL. |
| [**CD3DX12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION**](cd3dx12-dxil-subobject-to-exports-association.md) | Uma classe auxiliar para criar um subobjeto de estado de associação DXIL-SubObject-to-Exports. |
| [**CD3DX12_EXISTING_COLLECTION_SUBOBJECT**](cd3dx12-existing-collection-subobject.md) | Uma classe auxiliar para criar um subobjeto de estado de coleção existente. |
| [**CD3DX12_GLOBAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-global-root-signature-subobject.md) | Uma classe auxiliar para criar um estado de assinatura de raiz global suboject. |
| [**CD3DX12_GPU_DESCRIPTOR_HANDLE**](cd3dx12-gpu-descriptor-handle.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) . |
| [**CD3DX12_HEAP_DESC**](cd3dx12-heap-desc.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_HEAP_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_desc) . |
| [**CD3DX12_HEAP_PROPERTIES**](cd3dx12-heap-properties.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_HEAP_PROPERTIES**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) . |
| [**CD3DX12_HIT_GROUP_SUBOBJECT**](cd3dx12-hit-group-subobject.md) | Uma classe auxiliar para criar um subobjeto de estado de grupo de acesso. |
| [**CD3DX12_NODE_MASK_SUBOBJECT**](cd3dx12-node-mask-subobject.md) | Uma classe auxiliar para criar um subobjeto de estado que identifica os nós de GPU aos quais o objeto de estado se aplica. |
| [**CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT**](cd3dx12-local-root-signature-subobject.md) | Uma classe auxiliar para criar um estado de assinatura de raiz local suboject. |
| [**CD3DX12_PACKED_MIP_INFO**](cd3dx12-packed-mip-info.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3D12_PACKED_MIP_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_packed_mip_info) . |
| [**CD3DX12_PIPELINE_STATE_STREAM**](cd3dx12-pipeline-state-stream.md) | Uma estrutura auxiliar para criar e trabalhar com os Estados de pipeline de computação e elementos gráficos por meio de uma interface combinada. Consulte [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM1**](cd3dx12-pipeline-state-stream1.md) | Uma estrutura auxiliar para criar e trabalhar com os Estados de pipeline de computação e elementos gráficos por meio de uma interface combinada. Consulte [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). |
| [**CD3DX12_PIPELINE_STATE_STREAM2**](cd3dx12-pipeline-state-stream2.md) | Uma estrutura auxiliar para criar e trabalhar com os Estados de pipeline de computação e elementos gráficos por meio de uma interface combinada. |
| [**CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) | Uma estrutura auxiliar usada para descrever uma descrição de Blend como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO**](cd3dx12-pipeline-state-stream-cached-pso.md) | Uma estrutura auxiliar usada para descrever um PSO armazenado em cache como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_CS**](cd3dx12-pipeline-state-stream-cs.md) | Uma estrutura auxiliar usada para descrever um sombreador de computação como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md) | Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md) | Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT**](cd3dx12-pipeline-state-stream-depth-stencil-format.md) | Uma estrutura auxiliar usada para descrever o formato de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_DS**](cd3dx12-pipeline-state-stream-ds.md) | Uma estrutura auxiliar usada para descrever um sombreador de domínio como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_FLAGS**](cd3dx12-pipeline-state-stream-flags.md) | Uma estrutura auxiliar usada para descrever os sinalizadores de estado do pipeline como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_GS**](cd3dx12-pipeline-state-stream-gs.md) | Uma estrutura auxiliar usada para descrever um sombreador de geometria como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_HS**](cd3dx12-pipeline-state-stream-hs.md) | Uma estrutura auxiliar usada para descrever um sombreador envoltória como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md) | Uma estrutura auxiliar usada para descrever o valor de recorte da faixa de buffer de índice como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT**](cd3dx12-pipeline-state-stream-input-layout.md) | Uma estrutura auxiliar usada para descrever um layout de entrada como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK**](cd3dx12-pipeline-state-stream-node-mask.md) | Uma estrutura auxiliar usada para descrever uma máscara de nó como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER**](cd3dx12-pipeline-state-stream-parse-helper.md) | Cria um objeto CD3DX12_PIPELINE_STATE_STREAM interno a partir dos detalhes do subobjeto passados para as funções de membro correspondentes. Essa estrutura implementa a interface [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) . |
| [**CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY**](cd3dx12-pipeline-state-stream-primitive-topology.md) | Uma estrutura auxiliar usada para descrever a topologia primitiva como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_PS**](cd3dx12-pipeline-state-stream-ps.md) | Uma estrutura auxiliar usada para descrever um sombreador de pixel como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) | Uma estrutura auxiliar usada para descrever uma descrição do rasterizador como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS**](cd3dx12-pipeline-state-stream-render-target-formats.md) | Uma estrutura auxiliar usada para descrever os formatos de destino de renderização como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE**](cd3dx12-pipeline-state-stream-root-signature.md) | Uma estrutura auxiliar usada para descrever a assinatura raiz como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC**](cd3dx12-pipeline-state-stream-sample-desc.md) | Uma estrutura auxiliar usada para descrever uma descrição de exemplo como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK**](cd3dx12-pipeline-state-stream-sample-mask.md) | Uma estrutura auxiliar usada para descrever uma máscara de exemplo como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT**](cd3dx12-pipeline-state-stream-stream-output.md) | Uma estrutura auxiliar usada para descrever a descrição da saída do fluxo como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md) | Uma estrutura auxiliar modelo usada para encapsular pares de dados de subobjeto e tipo de subobjeto como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING**](cd3dx12-pipeline-state-stream-view-instancing.md) | Uma estrutura auxiliar usada para envolver uma [estrutura CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) dados. Permite que sombreadores renderizem para várias exibições com uma única chamada de desenho; útil para a visão estéreo ou geração de cubemap. |
| [**CD3DX12_PIPELINE_STATE_STREAM_VS**](cd3dx12-pipeline-state-stream-vs.md) | Uma estrutura auxiliar usada para descrever um sombreador de vértice como um único objeto adequado para uma descrição de fluxo. |
| [**CD3DX12_RANGE**](cd3dx12-range.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_RANGE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range) estrutura. |
| [**CD3DX12_RANGE_UINT64**](cd3dx12-range-uint64.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_range_uint64) estrutura. |
| [**CD3DX12_RASTERIZER_DESC**](cd3dx12-rasterizer-desc.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_RASTERIZER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) estrutura. |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT**](cd3dx12-raytracing-pipeline-config-subobject.md) | Uma classe auxiliar para criar um subobjeto de estado de configuração de pipeline de raytracing. |
| [**CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT**](cd3dx12-raytracing-pipeline-config1-subobject.md) | Uma classe auxiliar para criar um subobjeto de estado de configuração de pipeline de raytracing, com sinalizadores. |
| [**CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT**](cd3dx12-raytracing-shader-config-subobject.md) | Uma classe auxiliar para criar um subobjeto de estado de configuração do sombreador de raio. |
| [**CD3DX12_RECT**](cd3dx12-rect.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_RECT**](d3d12-rect.md) estrutura. |
| [**CD3DX12_RESOURCE_ALLOCATION_INFO**](cd3dx12-resource-allocation-info.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_RESOURCE_ALLOCATION_INFO**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) estrutura. |
| [**CD3DX12_RESOURCE_BARRIER**](cd3dx12-resource-barrier.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_RESOURCE_BARRIER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_barrier) estrutura. |
| [**CD3DX12_RESOURCE_DESC**](cd3dx12-resource-desc.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_RESOURCE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc) estrutura. |
| [**CD3DX12_RESOURCE_DESC1**](cd3dx12-resource-desc1.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) estrutura. |
| [**CD3DX12_ROOT_CONSTANTS**](cd3dx12-root-constants.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_ROOT_CONSTANTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_constants) estrutura. |
| [**CD3DX12_ROOT_DESCRIPTOR**](cd3dx12-root-descriptor.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_ROOT_DESCRIPTOR**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor) estrutura. |
| [**CD3DX12_ROOT_DESCRIPTOR1**](cd3dx12-root-descriptor1.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_ROOT_DESCRIPTOR1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor1) estrutura. |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE**](cd3dx12-root-descriptor-table.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) estrutura. |
| [**CD3DX12_ROOT_DESCRIPTOR_TABLE1**](cd3dx12-root-descriptor-table1.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) estrutura. |
| [**CD3DX12_ROOT_PARAMETER**](cd3dx12-root-parameter.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_ROOT_PARAMETER**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter) estrutura. |
| [**CD3DX12_ROOT_PARAMETER1**](cd3dx12-root-parameter1.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**D3D12_ROOT_PARAMETER1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_parameter1) estrutura. |
| [**CD3DX12_ROOT_SIGNATURE_DESC**](cd3dx12-root-signature-desc.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) estrutura. |
| [**CD3DX12_RT_FORMAT_ARRAY**](cd3dx12-rt-format-array.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de uma [**D3D12_RT_FORMAT_ARRAY**](/windows/win32/api/d3d12/ns-d3d12-d3d12_rt_format_array) estrutura. |
| [**CD3DX12_SHADER_BYTECODE**](cd3dx12-shader-bytecode.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_SHADER_BYTECODE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_shader_bytecode) estrutura. |
| [**CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**](cd3dx12-state-object-config-subobject.md) | Uma classe auxiliar para criar um subobjeto que define as propriedades gerais de um objeto de estado. |
| [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) | A classe central dos Auxiliares de Criação de Objeto de Estado D3DX12, que são classes auxiliares para criar objetos de estado de um conjunto arbitrário de subobjetos. |
| [**CD3DX12_STATIC_SAMPLER_DESC**](cd3dx12-static-sampler-desc.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_STATIC_SAMPLER_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) estrutura. |
| [**CD3DX12_SUBOBJECT_TO_EXPORTS_ASSOCIATION_SUBOBJECT**](cd3dx12-subobject-to-exports-association-subobject.md) | Uma classe auxiliar para criar um subobjeto de estado de associação subobject-to-exports. |
| [**CD3DX12_SUBRESOURCE_FOOTPRINT**](cd3dx12-subresource-footprint.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_SUBRESOURCE_FOOTPRINT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint) estrutura. |
| [**CD3DX12_SUBRESOURCE_RANGE_UINT64**](cd3dx12-subresource-range-uint64.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) estrutura. |
| [**CD3DX12_SUBRESOURCE_TILING**](cd3dx12-subresource-tiling.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_SUBRESOURCE_TILING**](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_tiling) estrutura. |
| [**CD3DX12_TEXTURE_COPY_LOCATION**](cd3dx12-texture-copy-location.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_TEXTURE_COPY_LOCATION**](/windows/win32/api/d3d12/ns-d3d12-d3d12_texture_copy_location) estrutura. |
| [**CD3DX12_TILE_REGION_SIZE**](cd3dx12-tile-region-size.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) estrutura. |
| [**CD3DX12_TILE_SHAPE**](cd3dx12-tile-shape.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) estrutura. |
| [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) estrutura. |
| [**CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC**](cd3dx12-versioned-root-signature-desc.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) estrutura. |
| [**CD3DX12_VIEW_INSTANCING_DESC**](cd3dx12-view-instancing-desc.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) estrutura. |
| [**CD3DX12_VIEWPORT**](cd3dx12-viewport.md) | Uma estrutura auxiliar para habilitar a inicialização fácil de [**uma D3D12_VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport) estrutura. |
| [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) | Para [sombreadores de malha/amplificações](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html), você pode usar os dados de [um EffectPipelineStateDescription](https://github.com/Microsoft/DirectXTK12/wiki/EffectPipelineStateDescription), com **D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**, para fornecer todo o estado. |

## <a name="related-topics"></a>Tópicos relacionados

* [Estruturas auxiliares e funções para D3D12](helper-structures-and-functions-for-d3d12.md)
* [Referência do Direct3D 12](direct3d-12-reference.md)
