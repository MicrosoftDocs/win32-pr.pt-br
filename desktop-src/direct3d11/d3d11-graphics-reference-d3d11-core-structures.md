---
title: Estruturas principais do Direct3D 11
description: Esta seção contém informações sobre as estruturas principais.
ms.assetid: 2a45182a-7114-4075-b8b8-147f52fe7aa9
keywords:
- estruturas, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf2daccc08066d37c00ed2a4b15a19da35afb8e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473102"
---
# <a name="direct3d-11-core-structures"></a>Estruturas principais do Direct3D 11

Esta seção contém informações sobre as estruturas principais.

## <a name="in-this-section"></a>Nesta seção


| Tópico | Descrição | 
|-------|-------------|
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a><br /> | Descreve o estado de mistura que você usa em uma chamada para <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device:: Createblendstate</strong></a> para criar um objeto de estado de mesclagem. <br /> | 
| <a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a><br /> | <blockquote>[!Note]<br />essa estrutura é suportada pelo tempo de execução do Direct3D 11,1, que está disponível em Windows 8 e em sistemas operacionais posteriores.</blockquote><br /> Descreve o estado de mistura que você usa em uma chamada para <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1:: CreateBlendState1</strong></a> para criar um objeto de estado de mesclagem. <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a><br /> | Define uma caixa 3D.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a><br /> | Descreve um contador.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a><br /> | Informações sobre os recursos do contador de desempenho da placa de vídeo.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a><br /> | Descreve o estado de estêncil de profundidade.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a><br /> | Operações de estêncil que podem ser executadas com base nos resultados do teste de estêncil.<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a><br /> | Argumentos para desenhar instância indexada indireta. <br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a><br /> | Argumentos para desenho de instância indireta. <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a><br /> | <blockquote>[!Note]<br />essa estrutura é suportada pelo tempo de execução do Direct3D 11,1, que está disponível em Windows 8 e em sistemas operacionais posteriores.</blockquote><br /> Descreve informações sobre a arquitetura do adaptador do Direct3D 11,1.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a><br /> | <blockquote>[!Note]<br />essa estrutura é suportada pelo tempo de execução do Direct3D 11,1, que está disponível em Windows 8 e em sistemas operacionais posteriores.</blockquote><br /> Descreve as opções de recurso do Direct3D 9 no driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a><br /> | Descreve as opções de recurso do Direct3D 9 no driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a><br /> | <blockquote>[!Note]<br />essa estrutura é suportada pelo tempo de execução do Direct3D 11,1, que está disponível em Windows 8 e em sistemas operacionais posteriores.</blockquote><br /> Descreve o suporte de sombra do Direct3D 9 no driver de gráficos atual. <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a><br /> | Descreve se há suporte para instanciação simples.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a><br /> | Descreve o sombreador de computação e o suporte a buffer estruturado e bruto no driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a><br /> | <blockquote>[!Note]<br />essa estrutura é suportada pelo tempo de execução do Direct3D 11,1, que está disponível em Windows 8 e em sistemas operacionais posteriores.</blockquote><br /> Descreve as opções de recurso do Direct3D 11,1 no driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a><br /> | Descreve as opções de recurso do Direct3D 11,2 no driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a><br /> | Descreve as opções de recurso do Direct3D 11,3 no driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a><br /> | Descreve as opções de recurso do Direct3D 11,3 no driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a><br /> | Descreve as opções de recurso do Direct3D 11,4 no driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a><br /> | Descreve o nível de suporte para recursos compartilhados no driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a><br /> | Descreve o suporte de tipo de dados duplo no driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a><br /> | Descreve quais recursos têm suporte pelo driver de gráficos atual para um determinado formato.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a><br /> | Descreve quais opções de recursos não ordenados são suportadas pelo driver de gráficos atual para um determinado formato.<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a><br /> | Descreve o suporte a endereço virtual de GPU de dados de recurso, incluindo bits de endereço máximo por recurso e por processo. <br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a><br /> | Descreve se há suporte para uma técnica de criação de perfil de GPU.<br /> | 
| <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a><br /> | Descreve o nível de cache de sombreador com suporte no driver gráfico atual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a><br /> | <blockquote>[!Note]<br />essa estrutura é suportada pelo tempo de execução do Direct3D 11,1, que está disponível em Windows 8 e em sistemas operacionais posteriores.</blockquote><br /> Descreve as opções de suporte de precisão para sombreadores no driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a><br /> | Descreve os recursos de multithreading que são suportados pelo driver de gráficos atual.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a><br /> | Uma descrição de um único elemento para o estágio de Assembler de entrada.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a><br /> | Consultar informações sobre a atividade de pipeline de gráficos entre chamadas para <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext:: Begin</strong></a> e <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext:: End</strong></a>.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a><br /> | Informações de consulta sobre a quantidade de dados transmitidos para os buffers de saída de fluxo entre <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext:: Begin</strong></a> e <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext:: End</strong></a>.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a><br /> | Consultar informações sobre a confiabilidade de uma consulta de carimbo de data/hora.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a><br /> | Descreve uma consulta.<br /> | 
| <a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a><br /> | Descreve uma consulta.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a><br /> | Descreve o estado do rasterizador.<br /> | 
| <a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a><br /> | <blockquote>[!Note]<br />essa estrutura é suportada pelo tempo de execução do Direct3D 11,1, que está disponível em Windows 8 e em sistemas operacionais posteriores.</blockquote><br /> Descreve o estado do rasterizador.<br /> | 
| <a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a><br /> | Descreve o estado do rasterizador.<br /> | 
| <a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a><br /> | D3D11_RECT é declarado da seguinte maneira:<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a><br /> | Descreve o estado de mesclagem para um destino de renderização.<br /> | 
| <a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a><br /> | <blockquote>[!Note]<br />essa estrutura é suportada pelo tempo de execução do Direct3D 11,1, que está disponível em Windows 8 e em sistemas operacionais posteriores.</blockquote><br /> Descreve o estado de mesclagem para um destino de renderização.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a><br /> | Descreve um estado de amostra.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a><br /> | Descrição de um elemento de vértice em um buffer de vértice em um slot de saída.<br /> | 
| <a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a><br /> | Define as dimensões de um viewport.<br /> | 


Além disso, há uma estrutura de retângulo 2D definida em D3D11.h.

```cpp
typedef RECT D3D11_RECT;
```

Para documentação, [consulte RECT](/previous-versions/dd162897%28v%3dvs.85%29) [no Windows GDI](../gdi/windows-gdi.md).

## <a name="related-topics"></a>Tópicos relacionados

[Referência principal](d3d11-graphics-reference-d3d11-core.md)
