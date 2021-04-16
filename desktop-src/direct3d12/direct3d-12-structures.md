---
title: Estruturas principais (gráficos do Direct3D 12)
description: As seguintes estruturas são declaradas em d3d12. h.
ms.assetid: 7FE8796A-98D1-4333-8755-2A47567460B3
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 456ca501426142182d9823427c7d13599e4a92db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105752552"
---
# <a name="core-structures"></a>Estruturas do núcleo

As seguintes estruturas são declaradas em d3d12. h.

## <a name="in-this-section"></a>Nesta seção

| Tópico e descrição |
|-|
| [**D3D12_AUTO_BREADCRUMB_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node). Representa dados de navegação automática de DRED com (dados estendidos) removidos do dispositivo como um nó em uma lista vinculada. |
| [**D3D12_BLEND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc). Descreve o estado de mesclagem. |
| [**D3D12_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box). Descreve uma caixa 3D. |
| [**D3D12_BUFFER_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_rtv). Descreve os elementos em um recurso de buffer para usar em uma exibição de destino de renderização. |
| [**D3D12_BUFFER_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_srv). Descreve os elementos em um recurso de buffer para usar em uma exibição de recurso de sombreador. |
| [**D3D12_BUFFER_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav). Descreve os elementos em um buffer para usar em uma exibição de acesso não ordenado. |
| [**D3D12_CACHED_PIPELINE_STATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state). Armazena um estado de pipeline. |
| [**D3D12_CLEAR_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value). Descreve um valor usado para otimizar as operações claras de um recurso específico. |
| [**D3D12_COMMAND_QUEUE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_queue_desc). Descreve uma fila de comandos. |
| [**D3D12_COMMAND_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Descreve os argumentos (parâmetros) de uma assinatura de comando. |
| [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc). Descreve um objeto de estado de pipeline de computação. |
| [**D3D12_CONSTANT_BUFFER_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc). Descreve um buffer de constantes para exibir. |
| [**D3D12_CPU_DESCRIPTOR_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle). Descreve um identificador de descritor de CPU. |
| [**D3D12_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc). Descreve o estado de estêncil de profundidade. |
| [**D3D12_DEPTH_STENCIL_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1). Descreve o estado de estêncil de profundidade. |
| [**D3D12_DEPTH_STENCIL_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_value). Especifica um valor de profundidade e de estêncil. |
| [**D3D12_DEPTH_STENCIL_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc). Descreve os subrecursos de uma textura que são acessíveis a partir de uma exibição de estêncil de profundidade. |
| [**D3D12_DEPTH_STENCILOP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencilop_desc). Descreve as operações de estêncil que podem ser executadas com base nos resultados do teste de estêncil. |
| [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc). Descreve o heap do descritor. |
| [**D3D12_DESCRIPTOR_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range). Descreve um intervalo de descritores. |
| [**D3D12_DESCRIPTOR_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1). Descreve um intervalo de descritor, com sinalizadores para determinar seus volatilidade. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data). Representa dados de dados estendidos removidos do dispositivo (DRED com) versão 1,0. |
| [**D3D12_DEVICE_REMOVED_EXTENDED_DATA1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data1). Representa os dados de remoção de dispositivo do DRED com (dados estendidos removidos do dispositivo) versão 1,1, para que os depuradores e extensões do depurador possam acessar os dados do DRED com. |
| [**D3D12_DISCARD_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region). Descreve detalhes para a operação descartar-recurso. |
| [**D3D12_DISPATCH_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments). Descreve os parâmetros de expedição para uso pelo sombreador de computação. |
| [**D3D12_DRAW_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments). Descreve parâmetros para instâncias de desenho. |
| [**D3D12_DRAW_INDEXED_ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments). Descreve os parâmetros para o desenho de instâncias indexadas. |
| [**D3D12_DRED_ALLOCATION_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_allocation_node). Descreve, como um nó em uma lista vinculada, dados sobre uma alocação rastreada pelo dispositivo dados estendidos removidos (DRED com). |
| [**D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_auto_breadcrumbs_output). Contém um ponteiro para o cabeçalho de uma lista vinculada de objetos [D3D12_AUTO_BREADCRUMB_NODE](/windows/desktop/api/d3d12/ns-d3d12-d3d12_auto_breadcrumb_node) . A lista representa o estado de navegação automática antes da remoção do dispositivo. |
| [**D3D12_DRED_PAGE_FAULT_OUTPUT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dred_page_fault_output). Descreve os dados de alocação relacionados a uma falha de página de GPU em um determinado endereço virtual (VA). |
| [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture). Forneça detalhes sobre a arquitetura do adaptador, ajudando os aplicativos a otimizar melhor para determinadas propriedades de adaptador. |
| [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1). Forneça detalhes sobre a arquitetura do adaptador, ajudando os aplicativos a otimizar melhor para determinadas propriedades de adaptador. |
| [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority). Detalha o suporte do adaptador para priorização de diferentes tipos de fila de comandos. |
| [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node). Indica o nível de suporte para o compartilhamento de recursos entre adaptadores diferentes. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options). Descreve as opções de recurso do Direct3D 12 no driver de gráficos atual. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1). Descreve o nível de suporte para operações de onda do HLSL 6,0. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2). Detalha o suporte do adaptador para determinados recursos opcionais do Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3). Usado para indicar o nível de suporte que o adaptador fornece para recursos opcionais do Direct3D 12. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4). Indica o nível de suporte para texturas de MSAA alinhadas a 64 KB, compartilhamento de API cruzada e operações de sombreador de 16 bits nativo. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5). Indica o nível de suporte que o adaptador fornece para os recursos de processamento de passagem de renderização, Ray tracing e Shader-Resource View Tier 3. |
| [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6). Indica o nível de suporte que o adaptador fornece para o sombreamento de taxa variável (VRS) e indica se há suporte para o processamento em segundo plano ou não. |
| [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps). Usado para determinine se o adaptador dá suporte à criação de heaps a partir da memória do sistema existente. Esses heaps não são destinados ao uso geral, mas são excepcionalmente úteis para fins de diagnóstico, pois eles têm a garantia de persistir mesmo após as falhas do adaptador ou apresentarem um evento de remoção de dispositivo. |
| [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels). Descreve informações sobre os [níveis de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) com suporte no driver gráfico atual. |
| [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info). Descreve o formato de dados DXGI. |
| [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support). Descreve quais recursos têm suporte pelo driver de gráficos atual para um determinado formato. |
| [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support). Detalha as limitações de espaço de endereço virtual da GPU do adaptador, incluindo bits de endereço máximo por recurso e por processo. |
| [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels). Descreve os níveis de qualidade da imagem para um determinado formato e contagem de amostra. |
| [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support). Indica o nível de suporte para sessões de recursos protegidos. |
| [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command). Indica o nível de suporte que o adaptador fornece para metacomandos. |
| [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature). Passe essa estrutura para [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) para verificar o suporte à versão da assinatura de raiz. |
| [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization). Indica o nível de suporte para serialização de heap. |
| [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache). Descreve o nível de cache de sombreador com suporte no driver gráfico atual. |
| [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model). Contém o modelo de sombreador com suporte. |
| [**D3D12_GPU_DESCRIPTOR_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle). Descreve um identificador de descritor de GPU. |
| [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc). Descreve um objeto de estado de pipeline de gráficos. |
| [**D3D12_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc). Descreve um heap. |
| [**D3D12_HEAP_PROPERTIES**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties). Descreve as propriedades de heap. |
| [**D3D12_INDEX_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view). Descreve o buffer de índice a ser exibido. |
| [**D3D12_INDIRECT_ARGUMENT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc). Descreve um argumento indireto (um parâmetro indireto) para uso com uma assinatura de comando. |
| [**D3D12_INPUT_ELEMENT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_element_desc). Descreve um único elemento para o estágio de Assembler de entrada do pipeline de gráficos. |
| [**D3D12_INPUT_LAYOUT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc). Descreve os dados de buffer de entrada para o estágio de Assembler de entrada. |
| [**D3D12_MEMCPY_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest). Descreve o destino de uma operação de cópia de memória. |
| [**D3D12_META_COMMAND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_meta_command_desc). Descreve um comando meta. |
| [**D3D12_META_COMMAND_PARAMETER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_meta_command_parameter_desc). Descreve um parâmetro para um meta comando. |
| [**D3D12_PACKED_MIP_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info). Descreve a estrutura lado a lado de um recurso de mosaico com mipmaps. |
| [**D3D12_PIPELINE_STATE_STREAM_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc). Descreve um fluxo de estado de pipeline. |
| [**D3D12_PLACED_SUBRESOURCE_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint). Descreve a superfície de um subrecurso inserido, incluindo o deslocamento e o D3D12_SUBRESOURCE_FOOTPRINT. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_protected_resource_session_desc). Descreve os sinalizadores para uma sessão de recurso protegido, por adaptador. |
| [**D3D12_QUERY_DATA_PIPELINE_STATISTICS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_data_pipeline_statistics). Consultar informações sobre a atividade de pipeline de gráficos entre chamadas para [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery). |
| [**D3D12_QUERY_DATA_SO_STATISTICS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_data_so_statistics). Descreve dados de consulta para saída de fluxo. |
| [**D3D12_QUERY_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc). Descreve a finalidade de um heap de consulta. Um heap de consulta contém uma matriz de consultas individuais. |
| [**D3D12_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range). Descreve um intervalo de memória. |
| [**D3D12_RANGE_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64). Descreve um intervalo de memória em um espaço de endereço de 64 bits. |
| [**D3D12_RASTERIZER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc). Descreve o estado do rasterizador. |
| [**D3D12_RAYTRACING_AABB**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_aabb). Representa uma AABB (caixa delimitadora alinhada em eixo) usada como geometria raytracing. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc). Descreve o requisito de espaço para a estrutura de aceleração após a compactação. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc). Descreve o espaço usado atualmente por uma estrutura de aceleração. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc). Descrição das informações de pós-compilação a serem geradas de uma estrutura de aceleração. Use essa estrutura em chamadas para [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) e [**BuildRaytracingAccelerationStructure**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc). Descreve o tamanho e o layout da estrutura e do cabeçalho de aceleração serializada |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc). Descreve o requisito de espaço para decodificar uma estrutura de aceleração em um formulário que pode ser visualizado por ferramentas. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info). Representa informações de compilação sobre uma estrutura de aceleração de raytracing. Obtenha uma instância desse Stucture chamando [**GetRaytracingAccelerationStructurePrebuildInfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv). Uma estrutura de exibição de recurso de sombreador (SRV) para armazenar uma estrutura de aceleração raytracing. |
| [**D3D12_RAYTRACING_GEOMETRY_AABBS_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc). Descreve um conjunto de caixas delimitadoras alinhadas ao eixo que são usadas na estrutura de [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) para fornecer dados de entrada para uma operação de compilação da estrutura de aceleração RAYTRACING. |
| [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). Descreve um conjunto de geometria que é usado na estrutura de [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) para fornecer dados de entrada para uma operação de compilação da estrutura de aceleração RAYTRACING. |
| [**D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc). Descreve um conjunto de triângulos usado como geometria de raytracing. A geometria apontada por esta struct sempre está no formato de lista de triângulo, indexada ou não indexada. Não há suporte para as faixas de triângulo. |
| [**D3D12_RAYTRACING_INSTANCE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc). Descreve uma instância de uma estrutura de aceleração raytracing usada na memória da GPU durante o processo de compilação da estrutura de aceleração. |
| [**D3D12_RAYTRACING_PIPELINE_CONFIG**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config). Um subobjeto de estado que representa uma configuração de pipeline raytracing. |
| [**D3D12_RAYTRACING_SHADER_CONFIG**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config). Um subobjeto de estado que representa uma configuração de sombreador. |
| [**D3D12_RECT**](d3d12-rect.md). D3D12_RECT é declarado como um RECT. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access). Descreve o acesso a recursos que são solicitados por um aplicativo na transição para uma passagem de renderização. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access_clear_parameters). Descreve o valor claro para o qual os recursos devem ser limpos no início de uma passagem de renderização. |
| [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc). Descreve uma associação (fixada pela duração da passagem de renderização) a uma DSV (exibição de estêncil de profundidade), bem como suas características de acesso inicial e final. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access). Descreve o acesso a recursos que são solicitados por um aplicativo na transição para fora de uma passagem de renderização. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_parameters). Descreve um recurso para resolver na conclusão de uma passagem de renderização. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_subresource_parameters). Descreve os subrecursos envolvidos na resolução na conclusão de uma passagem de renderização. |
| [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc). Descreve as associações (fixas para a duração da passagem de renderização) em uma ou mais exibições de destino de renderização (RTVs), bem como suas características de acesso inicial e final. |
| [**D3D12_RENDER_TARGET_BLEND_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_blend_desc). Descreve o estado de mesclagem para um destino de renderização. |
| [**D3D12_RENDER_TARGET_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc). Descreve os subrecursos de um recurso que são acessíveis usando uma exibição de destino de renderização. |
| [**D3D12_RESOURCE_ALIASING_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier). Descreve a transição entre os usos de dois recursos diferentes que têm mapeamentos para o mesmo heap. |
| [**D3D12_RESOURCE_ALLOCATION_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info). Descreve os parâmetros necessários para alocar recursos. |
| [**D3D12_RESOURCE_ALLOCATION_INFO1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info1). Descreve os parâmetros necessários para alocar recursos, incluindo o deslocamento. |
| [**D3D12_RESOURCE_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier). Descreve uma barreira de recurso (transição no uso de recursos). |
| [**D3D12_RESOURCE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc). Descreve um recurso, como uma textura. Essa estrutura é usada extensivamente. |
| [**D3D12_RESOURCE_TRANSITION_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier). Descreve a transição de subrecursos entre diferentes usos. |
| [**D3D12_RESOURCE_UAV_BARRIER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier). Representa um recurso no qual todos os acessos do UAV devem ser concluídos antes que qualquer acesso de UAV futuro possa começar. |
| [**D3D12_ROOT_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants). Descreve as constantes embutidas na assinatura raiz que aparecem em sombreadores como um buffer constante. |
| [**D3D12_ROOT_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor). Descreve os descritores embutidos na versão de assinatura raiz 1,0 que aparecem em sombreadores. |
| [**D3D12_ROOT_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1). Descreve os descritores embutidos na versão de assinatura raiz 1,1 que aparecem em sombreadores. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table). Descreve o layout da assinatura raiz 1,0 de uma tabela de descritores como uma coleção de intervalos de descritores que aparecem um após o outro em um heap de descritor. |
| [**D3D12_ROOT_DESCRIPTOR_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1). Descreve o layout da assinatura raiz 1,1 de uma tabela de descritores como uma coleção de intervalos de descritores que aparecem um após o outro em um heap de descritor. |
| [**D3D12_ROOT_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter). Descreve o slot de uma assinatura de raiz versão 1,0. |
| [**D3D12_ROOT_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1). Descreve o slot de uma assinatura de raiz versão 1,1. |
| [**D3D12_ROOT_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc). Descreve o layout de uma assinatura de raiz versão 1,0. |
| [**D3D12_ROOT_SIGNATURE_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1). Descreve o layout de uma assinatura de raiz versão 1,1. |
| [**D3D12_RT_FORMAT_ARRAY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array). Encapsula uma matriz de formatos de destino de renderização. |
| [**D3D12_SAMPLE_POSITION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sample_position). Descreve uma posição de exemplo de subpixel para uso com posições de exemplo programáveis. |
| [**D3D12_SAMPLER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc). Descreve um estado de amostra. |
| [**D3D12_SHADER_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode). Descreve os dados do sombreador. |
| [**D3D12_SHADER_RESOURCE_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc). Descreve uma exibição de recurso de sombreador. |
| [**D3D12_SO_DECLARATION_ENTRY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_so_declaration_entry). Descreve um elemento Vertex em um buffer de vértice em um slot de saída. |
| [**D3D12_STATIC_SAMPLER_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc). Descreve uma amostra estática. |
| [**D3D12_STREAM_OUTPUT_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_buffer_view). Descreve um buffer de saída de fluxo. |
| [**D3D12_STREAM_OUTPUT_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc). Descreve um buffer de saída de streaming. |
| [**D3D12_SUBRESOURCE_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data). Descreve dados de subrecurso. |
| [**D3D12_SUBRESOURCE_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint). Descreve o formato, a largura, a altura, a profundidade e a densidade de linha do subrecurso no recurso pai. |
| [**D3D12_SUBRESOURCE_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_info). Descreve dados de subrecurso. |
| [**D3D12_SUBRESOURCE_RANGE_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64). Descreve um intervalo de memória de subrecurso. |
| [**D3D12_SUBRESOURCE_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling). Descreve um volume de subrecurso em ladrilho. |
| [**D3D12_TEX1D_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_dsv). Descreve os subrecursos de uma matriz de texturas 1D para usar em uma exibição de estêncil de profundidade. |
| [**D3D12_TEX1D_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_rtv). Descreve os subrecursos de uma matriz de texturas 1D para usar em uma exibição de destino de renderização. |
| [**D3D12_TEX1D_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_srv). Descreve os subrecursos de uma matriz de texturas 1D para usar em uma exibição de recurso de sombreador. |
| [**D3D12_TEX1D_ARRAY_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_array_uav). Descreve uma matriz de recursos de textura de 1D de acesso não ordenado. |
| [**D3D12_TEX1D_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_dsv). Descreve o subrecurso de uma textura 1D que é acessível para uma exibição de estêncil de profundidade. |
| [**D3D12_TEX1D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_rtv). Descreve o subrecurso de uma textura 1D para usar em uma exibição de destino de renderização. |
| [**D3D12_TEX1D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_srv). Especifica o subrecurso de uma textura 1D para usar em um modo de exibição de recurso de sombreador. |
| [**D3D12_TEX1D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex1d_uav). Descreve um recurso de textura de 1D de acesso não ordenado. |
| [**D3D12_TEX2D_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_dsv). Descreve os subrecursos de uma matriz de texturas 2D que são acessíveis a uma exibição de estêncil de profundidade. |
| [**D3D12_TEX2D_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_rtv). Descreve os subrecursos de uma matriz de texturas 2D para usar em uma exibição de destino de renderização. |
| [**D3D12_TEX2D_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_srv). Descreve os subrecursos de uma matriz de texturas 2D para usar em uma exibição de recurso de sombreador. |
| [**D3D12_TEX2D_ARRAY_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_array_uav). Descreve uma matriz de recursos de textura 2D de acesso não ordenado. |
| [**D3D12_TEX2D_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_dsv). Descreve o subrecurso de uma textura 2D que é acessível para uma exibição de estêncil de profundidade. |
| [**D3D12_TEX2D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_rtv). Descreve o subrecurso de uma textura 2D para usar em uma exibição de destino de renderização. |
| [**D3D12_TEX2D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_srv). Descreve o subrecurso de uma textura 2D para usar em uma exibição de recurso de sombreador. |
| [**D3D12_TEX2D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2d_uav). Descreve um recurso de textura 2D de acesso não ordenado. |
| [**D3D12_TEX2DMS_ARRAY_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_dsv). Descreve os subrecursos de uma matriz de texturas 2D de várias amostras para uma exibição de estêncil de profundidade. |
| [**D3D12_TEX2DMS_ARRAY_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_rtv). Descreve os subrecursos de uma matriz de texturas 2D de várias amostras para usar em uma exibição de destino de renderização. |
| [**D3D12_TEX2DMS_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_array_srv). Descreve os subrecursos de uma matriz de texturas 2D de várias amostras para usar em uma exibição de recurso de sombreador. |
| [**D3D12_TEX2DMS_DSV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_dsv). Descreve o subrecurso de uma textura 2D de várias amostras que é acessível para uma exibição de estêncil de profundidade. |
| [**D3D12_TEX2DMS_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_rtv). Descreve o subrecurso de uma textura 2D de várias amostras para usar em uma exibição de destino de renderização. |
| [**D3D12_TEX2DMS_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex2dms_srv). Descreve os subrecursos de uma textura 2D de várias amostras para usar em uma exibição de recurso de sombreador. |
| [**D3D12_TEX3D_RTV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_rtv). Descreve os subrecursos de uma textura 3D para usar em uma exibição de destino de renderização. |
| [**D3D12_TEX3D_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_srv). Descreve os subrecursos de uma textura 3D para usar em uma exibição de recurso de sombreador. |
| [**D3D12_TEX3D_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tex3d_uav). Descreve um recurso de textura 3D de acesso não ordenado. |
| [**D3D12_TEXCUBE_ARRAY_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_array_srv). Descreve os subrecursos de uma matriz de texturas de cubo a serem usadas em uma exibição de recurso de sombreador. |
| [**D3D12_TEXCUBE_SRV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texcube_srv). Descreve o subrecurso de uma textura de cubo a ser usada em uma exibição de recurso de sombreador. |
| [**D3D12_TEXTURE_COPY_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location). Descreve uma parte de uma textura para fins de cópias de textura. |
| [**D3D12_TILE_REGION_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size). Descreve o tamanho de uma região em ladrilho. |
| [**D3D12_TILE_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape). Descreve a forma de um bloco especificando suas dimensões. |
| [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate). Descreve as coordenadas de um recurso em ladrilho. |
| [**D3D12_UNORDERED_ACCESS_VIEW_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc). Descreve os subrecursos de um recurso que são acessíveis usando uma exibição de acesso não ordenado. |
| [**D3D12_VERTEX_BUFFER_VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view). Descreve uma exibição de buffer de vértice. |
| [**D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). Representa dados de DRED com (dados estendidos removidos de dispositivo com versão), para que os depuradores e extensões do depurador possam acessar dados do DRED com. |
| [**D3D12_VERSIONED_ROOT_SIGNATURE_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc). Mantém qualquer versão de uma descrição de assinatura raiz e é projetada para ser usada com as funções de serialização/desserialização. |
| [**D3D12_VIEW_INSTANCE_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_view_instance_location). Especifica o visor/estêncil e o destino de renderização associados a uma instância de exibição. |
| [**D3D12_VIEW_INSTANCING_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_view_instancing_desc). Especifica os parâmetros usados durante a exibição da configuração de instanciação. |
| [**D3D12_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport). Descreve as dimensões de um visor. |
| [**D3D12_WRITEBUFFERIMMEDIATE_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_writebufferimmediate_parameter). Especifica o valor imediato e o endereço de destino gravados usando [**ID3D12CommandList2:: WriteBufferImmediate**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2). |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência principal](direct3d-12-core-reference.md)
* [Referência do Direct3D 12](direct3d-12-reference.md)