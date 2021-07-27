---
title: Enumerações de núcleo
description: As enumerações a seguir são declaradas em d3d12. h.
ms.assetid: 76E76C85-128E-4F0E-9711-C72C4CF6C835
ms.localizationpriority: low
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 31cac62c8dfa6b1126d8ff2a7c134490c0c58038
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436221"
---
# <a name="core-enumerations"></a>Enumerações de núcleo

As enumerações a seguir são declaradas em d3d12. h.

## <a name="in-this-section"></a>Nesta seção

| Tópico e descrição |
|-|
| [**D3D_ROOT_SIGNATURE_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version). Especifica a versão do layout de assinatura raiz. |
| [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model). Especifica um modelo de sombreador. |
| [**D3D12_AUTO_BREADCRUMB_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_auto_breadcrumb_op). Define constantes que especificam operações de GPU de processamento/computação. |
| [**D3D12_BACKGROUND_PROCESSING_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_background_processing_mode). Define constantes que especificam um nível de otimização dinâmica a ser aplicado ao trabalho de GPU que é enviado posteriormente. |
| [**D3D12_BLEND**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend). Especifica fatores de mistura, que modulam valores para o sombreador de pixel e destino de renderização. |
| [**D3D12_BLEND_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_blend_op). Especifica operações de mesclagem RGB ou alfa. |
| [**D3D12_BUFFER_SRV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags). Identifica como exibir um recurso de buffer. |
| [**D3D12_BUFFER_UAV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags). Identifica as opções de exibição de acesso não ordenado para um recurso de buffer. |
| [**D3D12_CLEAR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_clear_flags). Especifica o que limpar da exibição de estêncil de profundidade. |
| [**D3D12_COLOR_WRITE_ENABLE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_color_write_enable). Identifica quais componentes de cada pixel de um destino de renderização são graváveis durante a mesclagem. |
| [**D3D12_COMMAND_LIST_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_support_flags). Usado para determinar quais tipos de listas de comandos são capazes de dar suporte a várias operações. |
| [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type). Especifica o tipo de uma lista de comandos. |
| [**D3D12_COMMAND_QUEUE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_flags). Especifica os sinalizadores a serem usados ao criar uma fila de comandos. |
| [**D3D12_COMMAND_QUEUE_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_priority). Define os níveis de prioridade para uma fila de comando. |
| [**D3D12_COMPARISON_FUNC**](/windows/win32/api/d3d12/ne-d3d12-d3d12_comparison_func). Especifica as opções de comparação. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode). Identifica se a rasterização conservadora está ativada ou desativada. |
| [**D3D12_CONSERVATIVE_RASTERIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier). Identifica o nível de camada de rasterização conservadora. |
| [**D3D12_CPU_PAGE_PROPERTY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cpu_page_property). Especifica as propriedades da página de CPU para o heap. |
| [**D3D12_CROSS_NODE_SHARING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier). Especifica o nível de compartilhamento entre os nós de um adaptador, como a camada 1 emulada, a camada 1 ou a camada 2.  |
| [**D3D12_CULL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cull_mode). Especifica triângulos voltados para uma direção específica não são desenhados. |
| [**D3D12_DEBUG_DEVICE_PARAMETER_TYPE**](/windows/win32/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type). Especifica o tipo de dados da memória apontada pelo parâmetro *pData* de [**ID3D12DebugDevice1:: SetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) e [**ID3D12DebugDevice1:: GetDebugParameter**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter). |
| [**D3D12_DEPTH_WRITE_MASK**](/windows/win32/api/d3d12/ne-d3d12-d3d12_depth_write_mask). Identifica a parte de um buffer de estêncil de profundidade para gravar dados de profundidade. |
| [**D3D12_DESCRIPTOR_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_flags). Especifica as opções para um heap. |
| [**D3D12_DESCRIPTOR_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_heap_type). Especifica um tipo de heap de descritor.  |
| [**D3D12_DESCRIPTOR_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags). Especifica o volatilidade de ambos os descritores e os dados que eles referenciam em uma descrição de assinatura raiz 1,1, que pode habilitar algumas otimizações de driver. |
| [**D3D12_DESCRIPTOR_RANGE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type). Especifica um intervalo para que, por exemplo, se parte de uma tabela de descritor tenha 100 SRVs (exibições de recursos de sombreador) que o intervalo possa ser declarado em uma entrada em vez de 100.  |
| [**D3D12_DRED_ALLOCATION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_allocation_type). Define constantes que especificam operações de GPU de processamento/computação. |
| [**D3D12_DRED_ENABLEMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_enablement). Define constantes (usadas pela [interface ID3D12DeviceRemovedExtendedDataSettings](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings)) que especificam como os recursos de Dred com (dados estendidos removidos do dispositivo) individuais são habilitados. |
| [**D3D12_DRED_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_flags). Define constantes usadas na [estrutura de D3D12_DEVICE_REMOVED_EXTENDED_DATA](/windows/win32/api/d3d12/ns-d3d12-d3d12_device_removed_extended_data) para especificar sinalizadores de controle para o tempo de execução do Direct3D. |
| [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version). Define constantes que especificam uma versão do dispositivo removeu dados estendidos (DRED com), conforme usado pela [estrutura de D3D12_VERSIONED_DEVICE_REMOVED_EXTENDED_DATA](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_device_removed_extended_data). |
| [**D3D12_DSV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_dimension). Especifica como acessar um recurso usado em uma exibição de estêncil de profundidade. |
| [**D3D12_DSV_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dsv_flags). Especifica opções de exibição de estêncil de profundidade. |
| [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature). Opções de recurso do Direct3D 12 com suporte do driver de gráficos atual.  |
| [**D3D12_FENCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). Especifica as opções de isolamento.  |
| [**D3D12_FILL_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fill_mode). Especifica o modo de preenchimento a ser usado ao renderizar triângulos. |
| [**D3D12_FILTER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter). Especifica as opções de filtragem durante a amostragem de textura. |
| [**D3D12_FILTER_REDUCTION_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_reduction_type). Especifica o tipo de redução de filtro.  |
| [**D3D12_FILTER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_filter_type). Especifica o tipo de filtros de amostra de ampliação ou minificação.  |
| [**D3D12_FORMAT_SUPPORT1**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support1). Especifica os recursos que têm suporte para um formato fornecido. |
| [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2). Especifica quais opções de recursos não ordenados têm suporte para um formato fornecido. |
| [**D3D12_GRAPHICS_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_graphics_states). Define sinalizadores que especificam Estados relacionados a uma lista de comandos gráficos. Os valores podem ser unificados ou juntos. |
| [**D3D12_HEAP_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags). Especifica opções de heap, como se o heap pode conter texturas e se os recursos são compartilhados entre os adaptadores.  |
| [**D3D12_HEAP_SERIALIZATION_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_serialization_tier). Define constantes que especificam o suporte à serialização de heap. |
| [**D3D12_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type). Especifica o tipo de heap. Quando residentes, os heaps residem em um pool de memória física específico com determinadas propriedades de cache de CPU.  |
| [**D3D12_INDEX_BUFFER_STRIP_CUT_VALUE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value). Ao usar a topologia primitiva da faixa de triângulo, as posições de vértice são interpretadas como vértices de uma faixa de triângulo contínua. Há um valor de índice especial que representa o desejo de ter uma descontinuidade na faixa, o valor de índice de recorte. Essa enumeração lista os valores de recorte com suporte.  |
| [**D3D12_INDIRECT_ARGUMENT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_indirect_argument_type). Especifica o tipo do parâmetro indireto.  |
| [**D3D12_INPUT_CLASSIFICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_input_classification). Identifica o tipo de dados contidos em um slot de entrada. |
| [**D3D12_LIFETIME_STATE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_lifetime_state). Define constantes que especificam o estado de tempo de vida de um objeto rastreado por tempo de vida. |
| [**D3D12_LOGIC_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_logic_op). Especifica operações lógicas a serem configuradas para um destino de renderização. |
| [**D3D12_MEASUREMENTS_ACTION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_measurements_action). Define constantes que especificam o que deve ser feito com os resultados da instrumentação de carga de trabalho anterior. |
| [**D3D12_MEMORY_POOL**](/windows/win32/api/d3d12/ne-d3d12-d3d12_memory_pool). Especifica o pool de memória para o heap. |
| [**D3D12_MESH_SHADER_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_mesh_shader_tier). Define constantes que especificam o suporte ao sombreador de malha e amplificação. |
| [**D3D12_META_COMMAND_PARAMETER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_flags). Define constantes que especificam os sinalizadores para um parâmetro para um meta comando. Os valores podem ser unificados ou juntos. |
| [**D3D12_META_COMMAND_PARAMETER_STAGE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_stage). Define constantes que especificam o estágio de um parâmetro para um comando meta. |
| [**D3D12_META_COMMAND_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_meta_command_parameter_type). Define constantes que especificam o tipo de dados de um parâmetro para um meta comando. |
| [**D3D12_MULTIPLE_FENCE_WAIT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multiple_fence_wait_flags). Especifica vários sinalizadores de espera para vários limites. |
| [**D3D12_MULTISAMPLE_QUALITY_LEVELS_FLAG**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags). Especifica opções para determinar os níveis de qualidade.  |
| [**D3D12_PIPELINE_STATE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags). Sinalizadores para controlar o estado do pipeline.  |
| [**D3D12_PIPELINE_STATE_SUBOBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type). Especifica o tipo de um subobjeto em uma descrição de fluxo de estado de pipeline. |
| [**D3D12_PREDICATION_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_predication_op). Especifica a operação predicação a ser aplicada.  |
| [**D3D12_PRIMITIVE_TOPOLOGY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type). Especifica como o pipeline interpreta primitivas de entrada do sombreador envoltória ou Geometry. |
| [**D3D12_PROGRAMMABLE_SAMPLE_POSITIONS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_programmable_sample_positions_tier). Especifica o nível de suporte para as posições de exemplo programáveis que são oferecidas pelo adaptador. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_flags). Define constantes que especificam sinalizadores de sessão de recurso protegido. |
| [**D3D12_PROTECTED_RESOURCE_SESSION_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_resource_session_support_flags). Define constantes que especificam o suporte à sessão de recurso protegido. |
| [**D3D12_PROTECTED_SESSION_STATUS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_protected_session_status). Define constantes que especificam o status da sessão protegida. |
| [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type). Especifica o tipo de heap de consulta a ser criado. |
| [**D3D12_QUERY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Especifica o tipo de consulta. |
| [**D3D12_RAY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_ray_flags). Sinalizadores passados para a função [**TraceRay**](./traceray-function.md) para substituir transparência, remoção e comportamento de início. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags). Especifica os sinalizadores para a compilação de uma estrutura de aceleração raytracing. Use um valor dessa enumeração com a estrutura [**D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs) que fornece entrada para a operação de criação da estrutura de aceleração. |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode). Especifica o tipo de operação de cópia executada ao chamar [**CopyRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type). Especifica o tipo de informações de pós-compilação da estrutura de aceleração que podem ser recuperadas com chamadas para [**EmitRaytracingAccelerationStructurePostbuildInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo) e [**BuildRaytracingAccelerationStructure**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure). |
| [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_type). Especifica o tipo de uma estrutura de aceleração raytracing. |
| [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags). Especifica sinalizadores para geometria de raytracing em uma estrutura de [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc) . |
| [**D3D12_RAYTRACING_GEOMETRY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_type). Especifica o tipo de geometria usado para raytracing. Use um valor dessa enumeração para especificar o tipo de geometria em um [**D3D12_RAYTRACING_GEOMETRY_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc). |
| [**D3D12_RAYTRACING_INSTANCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags). Sinalizadores para uma instância de estrutura de aceleração raytracing. Esses sinalizadores podem ser usados para substituir [**D3D12_RAYTRACING_GEOMETRY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags) para instâncias individuais. |
| [**D3D12_RAYTRACING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_tier). Especifica o nível de suporte ao rastreamento de Ray no dispositivo de gráficos. |
| [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type). Especifica o tipo de acesso que um aplicativo recebe para os recursos especificados na transição para uma passagem de renderização. |
| [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type). Especifica o tipo de acesso que um aplicativo recebe para os recursos especificados na transição de uma passagem de renderização. |
| [**D3D12_RENDER_PASS_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_flags). Especifica a natureza da passagem de renderização; por exemplo, se é uma passagem de renderização de suspensão ou de retomada. |
| [**D3D12_RESIDENCY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_flags). Usado com a função EnqueueMakeResident para escolher como as operações de residência continuarão quando o orçamento de memória for excedido. |
| [**D3D12_RESIDENCY_PRIORITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_residency_priority). Especifica amplo buckets de prioridade de residência úteis para estabelecer rapidamente um esquema de prioridade de aplicativo. |
| [**D3D12_RESOLVE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resolve_mode). Especifica uma operação de resolução. |
| [**D3D12_RESOURCE_BARRIER_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags). Sinalizadores para definir barreiras de recurso de divisão.  |
| [**D3D12_RESOURCE_BARRIER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_type). Especifica um tipo de barreira de recurso (transição em uso de recursos) descrição. |
| [**D3D12_RESOURCE_BINDING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_binding_tier). Identifica a camada de associação de recursos que está sendo usada.  |
| [**D3D12_RESOURCE_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension). Identifica o tipo de recurso que está sendo usado. |
| [**D3D12_RESOURCE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags). Especifica opções para trabalhar com recursos.  |
| [**D3D12_RESOURCE_HEAP_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_heap_tier). Especifica a qual camada de heap de recursos o hardware e o driver dão suporte.  |
| [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). Especifica o estado de um recurso em relação a como o recurso está sendo usado.  |
| [**D3D12_ROOT_DESCRIPTOR_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags). Especifica o volatilidade dos dados referenciados por descritores em uma assinatura de raiz 1,1 Descrição, que pode habilitar algumas otimizações de driver. |
| [**D3D12_ROOT_PARAMETER_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_parameter_type). Especifica o tipo de slot de assinatura raiz.  |
| [**D3D12_ROOT_SIGNATURE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags). Especifica as opções para o layout de assinatura raiz.  |
| [**D3D12_RTV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_rtv_dimension). Identifica o tipo de recurso a ser exibido como um destino de renderização. |
| [**D3D12_SAMPLER_FEEDBACK_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_sampler_feedback_tier). Define constantes que especificam o suporte aos comentários do sampler. |
| [**D3D12_SHADER_CACHE_SUPPORT_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_cache_support_flags). Descreve o nível de suporte para cache de sombreador no driver gráfico atual. |
| [**D3D12_SHADER_COMPONENT_MAPPING**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_component_mapping). Especifica como a memória é roteada por uma SRV (exibição de recurso de sombreador).  |
| [**D3D12_SHADER_MIN_PRECISION_SUPPORT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_min_precision_support). Descreve as opções de suporte de precisão mínima para sombreadores no driver gráfico atual.  |
| [**D3D12_SHADER_VISIBILITY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility). Especifica os sombreadores que podem acessar o conteúdo de um determinado slot de assinatura raiz. |
| [**D3D12_SHARED_RESOURCE_COMPATIBILITY_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_shared_resource_compatibility_tier). Define constantes que especificam uma camada de suporte de compartilhamento entre APIs. |
| [**D3D12_SRV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_srv_dimension). Identifica o tipo de recurso que será exibido como um recurso de sombreador. |
| [**D3D12_STATIC_BORDER_COLOR**](/windows/win32/api/d3d12/ne-d3d12-d3d12_static_border_color). Especifica a cor da borda de um exemplo estático.  |
| [**D3D12_STENCIL_OP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_stencil_op). Identifica as operações de estêncil que podem ser executadas durante o teste de estêncil de profundidade. |
| [**D3D12_TEXTURE_ADDRESS_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_address_mode). Identifica uma técnica para resolver coordenadas de textura que estão fora dos limites de uma textura.  |
| [**D3D12_TEXTURE_COPY_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_copy_type). Especifica que tipo de cópia de textura deve ocorrer. |
| [**D3D12_TEXTURE_LAYOUT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout). Especifica opções de layout de textura.  |
| [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags). Especifica como copiar umile.  |
| [**D3D12_TILE_MAPPING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_mapping_flags). Especifica como executar uma operação de mapeamento deile.  |
| [**D3D12_TILE_RANGE_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_range_flags). Especifica um intervalo de mapeamentos deile.  |
| [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier). Identifica o nível de camada no qual há suporte para recursos lado a lado.  |
| [**D3D12_UAV_DIMENSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_uav_dimension). Identifica opções de exibição de acesso não organizado. |
| [**D3D12_VIEW_INSTANCING_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_flags). Especifica opções para a instanciamento de exibição. |
| [**D3D12_VIEW_INSTANCING_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_view_instancing_tier). Indica o nível de camada no qual há suporte para a instanciamento de exibição. |
| [**D3D12_WAVE_MMA_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_wave_mma_tier). Define constantes que especificam um nível de suporte para operações waveMMA (wave_matrix). |
| [**D3D12_WRITEBUFFERIMMEDIATE_MODE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_writebufferimmediate_mode). Especifica o modo usado por uma **operação WriteBufferImmediate.** |

## <a name="related-topics"></a>Tópicos relacionados

* [Referência de núcleo](direct3d-12-core-reference.md)
* [Referência do Direct3D 12](direct3d-12-reference.md)
