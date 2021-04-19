---
description: Esta seção contém informações de referência para as estruturas da API de vídeo do Microsoft Direct3D 12.
ms.assetid: ''
title: Estruturas de vídeo do Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 8914e8af9e21f3ee9a93e8bf9d122bec71483932
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314559"
---
# <a name="direct3d-12-video-structures"></a>Estruturas de vídeo do Direct3D 12

Esta seção contém informações de referência para as estruturas da API de vídeo do Microsoft Direct3D 12.

## <a name="in-this-section"></a>Nesta seção

| Tópico                                                                                | Descrição                                                                                              |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_conversion_support)  | Recupera a lista de perfis com suporte.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_formats)  | Recupera a lista de formatos com suporte.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_histogram)  | Fornece dados para chamadas para ID3D12VideoDevice:: CheckFeatureSupport quando o recurso especificado é D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_profiles)  | Recupera a lista de perfis com suporte.|
| [D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_decode_support)  | Recupera informações de suporte para decodificação de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_count)  | Recupera o número de comandos de extensão de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameter_count)  | Recupera o número de parâmetros com suporte para o estágio de parâmetro especificado.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_parameters)  | Recupera a lista de parâmetros de comando de extensão de vídeo para o estágio de parâmetro especificado.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_size)  | Verifica o tamanho de alocação de um comando de extensão de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_command_support)  | Recupera o suporte ao comando de extensão de vídeo usando estruturas de entrada e saída definidas pelo comando.|
| [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_extension_commands)  | Recupera a lista de comandos de extensão de vídeo do driver.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator)  | Fornece dados para chamadas para ID3D12VideoDevice:: CheckFeatureSupport quando o recurso especificado é D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR. Recupera os recursos de estimativa de movimento para um codificador de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_protected_resources)  | Fornece dados para chamadas para ID3D12VideoDevice:: CheckFeatureSupport quando o recurso especificado é D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR_PROTECTED_RESOURCES. Recupera o suporte a recursos protegidos para a estimativa de movimento de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR_SIZE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator_size)  | Descreve o tamanho de alocação de um heap de avaliador de movimento de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_max_input_streams)  | Recupera o número máximo de fluxos de entrada habilitados com suporte pelo processador de vídeo.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_reference_info)  | Recupera o número de quadros de referência anteriores e futuros necessários para o modo de desentrelaçamento especificado, filtro, conversão de taxa ou recursos de processamento automático.|
| [D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_process_support)  | Fornece dados para chamadas para ID3D12VideoDevice:: CheckFeatureSupport quando o recurso especificado é D3D12_FEATURE_VIDEO_PROCESS_SUPPORT.|
| [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics)  | Representa dados de uma consulta de estatísticas de decodificação de vídeo chamada chamando ID3D12VideoDecodeCommandList:: endquery.|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_input)  | Fornece dados de entrada para chamadas para ID3D12VideoEncodeCommandList:: ResolveMotionVectorHeap.|
| [D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resolve_video_motion_vector_heap_output)  | Recebe dados de saída de chamadas para ID3D12VideoEncodeCommandList:: ResolveMotionVectorHeap.|
| [D3D12_RESOURCE_COORDINATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_resource_coordinate)  | Descreve as coordenadas de um recurso.|
| [D3D12_VIDEO_DECODER_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_desc)  | Descreve um ID3D12VideoDecoder.|
| [D3D12_VIDEO_DECODER_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc)  | Descreve um ID3D12VideoDecoderHeap.|
| [D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_compressed_bitstream)  | Representa um fragmentado compactado do qual o vídeo é decodificado.|
| [D3D12_VIDEO_DECODE_CONFIGURATION](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_configuration)  | Descreve a configuração de um decodificador de vídeo.|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments)  | Especifica os parâmetros para decodificar a conversão de saída.|
| [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments1)  | Especifica os parâmetros para decodificar a conversão de saída.|
| [D3D12_VIDEO_DECODE_FRAME_ARGUMENT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_frame_argument)  | Representa os parâmetros de decodificação para um quadro.|
| [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)  | Especifica os parâmetros para o fluxo de entrada para uma operação de decodificação de vídeo.|
| [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram)  | Representa o buffer de saída de histograma para um único componente.|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments)  | Especifica os parâmetros para o fluxo de saída para uma operação de decodificação de vídeo.|
| [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1)  | Especifica os parâmetros para o fluxo de saída para uma operação de decodificação de vídeo.|
| [D3D12_VIDEO_DECODE_REFERENCE_FRAMES](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_reference_frames)  | Contém a lista de quadros de referência para a operação de decodificação atual.|
| [D3D12_VIDEO_DECODE_SUB_SAMPLE_MAPPING_BLOCK](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_sub_sample_mapping_block)  | Define o mapeamento de bytes de criptografia de subamostras para decodificação de vídeo.|
| [D3D12_VIDEO_EXTENSION_COMMAND_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_desc)  | Descreve um comando de extensão de vídeo.|
| [D3D12_VIDEO_EXTENSION_COMMAND_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_info)  | Descreve um comando de extensão de vídeo.|
| [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_extension_command_parameter_info)  | Descreve um parâmetro de comando de extensão de vídeo.|
| [D3D12_VIDEO_FORMAT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_format)  | Define a combinação de um formato de pixel e espaço de cores para uma descrição de conteúdo de recurso.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_desc)  | Descreve um ID3D12VideoMotionEstimator. Passe essa estrutura em ID3D12VideoDevice1:: CreateVideoMotionEstimator para criar uma instância de ID3D12VideoMotionEstimator.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input)  | Fornece dados de entrada para chamadas para ID3D12VideoEncodeCommandList:: EstimateMotion.|
| [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output)  | Recebe dados de saída de chamadas para ID3D12VideoEncodeCommandList:: EstimateMotion.|
| [D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_motion_vector_heap_desc)  | Descreve um ID3D12VideoMotionEstimatorHeap. Passe essa estrutura em ID3D12VideoDevice1:: CreateVideoMotionEstimatorHeap para criar uma instância de ID3D12VideoMotionEstimatorHeap.|
| [D3D12_VIDEO_PROCESS_ALPHA_BLENDING](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_alpha_blending)  | Especifica os parâmetros de mesclagem alfa para processamento de vídeo.|
| [D3D12_VIDEO_PROCESS_FILTER_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_filter_range)  | Define o intervalo de valores com suporte para um filtro de imagem.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream)  | Contém informações de entrada para a funcionalidade de Blend do processador de vídeo.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)  | Especifica argumentos de fluxo de entrada para um fluxo de entrada passado para ID3D12VideoCommandList::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_desc)  | Especifica os parâmetros para o fluxo de entrada para uma operação de processo de vídeo.|
| [D3D12_VIDEO_PROCESS_INPUT_STREAM_RATE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_rate)  | Fornece informações sobre a taxa de fluxo.|
| [D3D12_VIDEO_PROCESS_LUMA_KEY](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_luma_key)  | Especifica as configurações usadas para Luma de chaveamento.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream)  | Representa o fluxo de saída para comandos de processamento de vídeo.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments)  | Especifica argumentos de fluxo de saída para a saída passada para ID3D12VideoCommandList::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_DESC](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_desc)  | Especifica argumentos de fluxo de saída para a saída passada para ID3D12VideoProcessCommandList::P rocessFrames.|
| [D3D12_VIDEO_PROCESS_REFERENCE_SET](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_reference_set)  | Contém os quadros de referência necessários para executar o processamento de vídeo.|
| [D3D12_VIDEO_PROCESS_TRANSFORM](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_transform)  | Especifica parâmetros de transformação para processamento de vídeo.|
| [D3D12_VIDEO_SAMPLE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_sample)  | Descreve a largura, a altura, o formato e o espaço de cores de um buffer de imagem.|
| [D3D12_VIDEO_SCALE_SUPPORT](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_scale_support)  | Descreve o intervalo de dimensionamento com suporte de tamanhos de saída para um dimensionador de vídeo.|
| [D3D12_VIDEO_SIZE_RANGE](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_size_range)  | Descreve o intervalo de tamanhos com suporte para um dimensionador de vídeo.|



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs de vídeo do Direct3D 12](direct3d-12-video-apis.md)
</dt> </dl>

 

 



