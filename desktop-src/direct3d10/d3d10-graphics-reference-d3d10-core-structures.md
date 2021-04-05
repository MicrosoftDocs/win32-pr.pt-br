---
description: 'Esta seção contém informações sobre as seguintes estruturas principais:'
ms.assetid: 84769515-3f3b-4464-9620-7b806bf905b3
title: Estruturas principais do Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de2260b108ea340a97f24acf61f6ae686e00342
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646542"
---
# <a name="direct3d-10-core-structures"></a>Estruturas principais do Direct3D 10

Esta seção contém informações sobre as seguintes estruturas principais:



| Estruturas                                                                               | Descrição                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**D3D10 de \_ combinação \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)                                           | Opções de mesclagem para um dispositivo Direct3D 10,0.                         |
| [**D3D10 \_ Blend \_ DESC1**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)                                         | Opções de mesclagem para um dispositivo Direct3D 10,1.                         |
| [**Caixa de D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)                                                          | Uma região retangular, geralmente em uma textura.                            |
| [**\_Desc. contador de d3d10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_counter_desc)                                       | Uma descrição do contador de desempenho.                                   |
| [**\_Informações do contador de d3d10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_counter_info)                                       | Informações sobre os recursos do contador de desempenho da placa de vídeo. |
| [**Desc. de estêncil de profundidade de D3D10 \_ \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)                          | Uma descrição do estêncil de profundidade.                                         |
| [**D3D10 \_ profundidade \_ STENCILOP \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)                      | Uma operação de estêncil de profundidade.                                           |
| [**\_Filtro de \_ fila de informações de d3d10 \_**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter)                            | Um filtro de mensagens de depuração.                                              |
| [**D3D10 \_ de \_ filtro de fila de informações \_ \_ desc**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc)                 | Uma descrição do filtro de mensagem de depuração.                                  |
| [**\_Elemento de entrada d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                          | Uma descrição do elemento do buffer de vértice para um slot de entrada.               |
| [**\_Estatísticas de \_ pipeline de dados de consulta d3d10 \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_data_pipeline_statistics) | Estatísticas de consulta de pipeline.                                           |
| [**D3D10 \_ consultar \_ dados \_ para \_ estatísticas**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_data_so_statistics)             | Estatísticas de consulta do estágio Stream-output.                                |
| [**D3D10 de carimbo de data \_ \_ /hora de dados de consulta não \_ \_ contíguo**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_data_timestamp_disjoint)   | Estatísticas de consulta de carimbo de hora.                                          |
| [**D3D10 de \_ consulta \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_query_desc)                                           | Uma descrição de consulta.                                                 |
| [**\_Mensagem d3d10**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_message)                                                  | Uma mensagem de depuração para a fila de informações.                           |
| [**D3D10 do \_ rasterizador \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                 | Rasterizador-descrição do estágio.                                        |
| [**D3D10 \_ Rect**](d3d10-rect.md)                                                        | Um retângulo 2D.                                                      |
| [**D3D10 \_ render \_ \_ DESC1 Blend de destino \_**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)           | Opções de mesclagem para um destino de renderização do Direct3D 10,1.                  |
| [**D3D10 de \_ amostra \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)                                       | Uma descrição de amostra.                                               |
| [**\_Exibição de recursos do sombreador d3d10 \_ \_ \_ desc**](/windows/desktop/api/d3d10/ns-d3d10-d3d10_shader_resource_view_desc)           | Descreve uma exibição de recurso de sombreador para o Direct3D 10,0.                  |
| [**\_DESC1 da \_ exibição de recursos do SOMBREAdor d3d10 \_ \_**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)         | Descreve uma exibição de recurso de sombreador para o Direct3D 10,1.                  |
| [**D3D10 \_ de \_ parâmetro de assinatura \_ desc**](/windows/desktop/api/D3D10Shader/ns-d3d10shader-d3d10_signature_parameter_desc)              | Uma descrição do sombreador-parâmetro.                                      |
| [**\_Máscara de \_ bloco de estado d3d10 \_**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_state_block_mask)                              | Uma máscara de bloco de estado.                                                  |
| [**D3D10 \_ de \_ entrada de Declaração \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_so_declaration_entry)                      | Uma descrição do elemento do buffer de vértice para um slot de saída.              |
| [**\_Visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)                                                | Dimensões do visor.                                                 |



 

Além disso, há uma estrutura de retângulo 2D definida em d3d10. h.


```
typedef RECT D3D10_RECT;
```



Para obter a documentação, consulte [Rect](/previous-versions//ms536136(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência principal](d3d10-graphics-reference-d3d10-core.md)
</dt> </dl>

 

 
