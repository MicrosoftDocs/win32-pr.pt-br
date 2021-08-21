---
description: Esta seção contém informações sobre as enumerações fornecidas pelo DXGI.
ms.assetid: c4574c89-dee2-4841-9318-5383cf417111
title: Enumerações DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9347fdf39f2cde6bb50e3ae4c65f2601c570e084516bf817c4dc66169a83925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987136"
---
# <a name="dxgi-enumerations"></a>Enumerações DXGI

Esta seção contém informações sobre as enumerações fornecidas pelo DXGI.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                         | Descrição                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SINALIZADOR DO \_ ADAPTADOR DXGI \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag)<br/>                                          | Identifica o tipo de adaptador DXGI.<br/>                                                                                                                                   |
| [**SINALIZADOR DO \_ ADAPTADOR DXGI3 \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)<br/>                                        | Identifica o tipo de adaptador DXGI.<br/>                                                                                                                                   |
| [**MODO ALFA \_ \_ DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)<br/>                                                       | Identifica o valor alfa, o comportamento de transparência, de uma superfície.<br/>                                                                                                       |
| [**TIPO DE ESPAÇO DE COR DXGI \_ \_ \_**](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)<br/>                                          | Especifica tipos de espaço de cores.<br/>                                                                                                                                           |
| [**\_GRANULARIDADE DE \_ PREEMPÇÃO \_ DE COMPUTAÇÃO DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_compute_preemption_granularity)<br/>              | Identifica a granularidade na qual a GPU (unidade de processamento gráfico) pode ser preempção de executar sua tarefa de computação atual.<br/>                                      |
| [**SINALIZADORES \_ RLO DE DEPURAÇÃO DO DXGI \_ \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_debug_rlo_flags)<br/>                                            | Sinalizadores usados com [**ReportLiveObjects**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgidebug-reportliveobjects) para especificar a quantidade de informações a relatar sobre o tempo de vida de um objeto. <br/>                         |
| [**RECURSO \_ DXGI**](/windows/desktop/api/DXGI1_5/ne-dxgi1_5-dxgi_feature)<br/>                                                              | Especifica uma variedade de recursos de hardware a serem usados ao verificar o suporte a recursos.<br/>                                                                                  |
| [**FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br/>                                                       | Formatos de dados de recurso, incluindo formatos totalmente digitados e sem tipo. Uma lista de modificadores na parte inferior da página descreve mais completamente cada tipo de formato. <br/>               |
| [**MODO DE APRESENTAÇÃO DE QUADRO DXGI \_ \_ \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode)<br/>                            | Indica opções para apresentar quadros para a cadeia de permuta. <br/>                                                                                                            |
| [**PREFERÊNCIA DE \_ GPU DO DXGI \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference)<br/>                                               | A preferência de GPU para o aplicativo ser executado.<br/>                                                                                                                           |
| [**\_GRANULARIDADE DE \_ PREEMPÇÃO DE ELEMENTOS GRÁFICOS DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_graphics_preemption_granularity)<br/>            | Identifica a granularidade na qual a GPU pode ser preempção de executar sua tarefa de renderização de gráficos atual.<br/>                                                      |
| [**SINALIZADORES DE SUPORTE À \_ \_ COMPOSIÇÃO \_ DE HARDWARE DXGI \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)<br/>     | Descreve quais níveis de composição de hardware são compatíveis.<br/>                                                                                                          |
| [**TIPO DE \_ METADADOS DXGI HDR \_ \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type)<br/>                                        | Especifica o tipo de metadados do header.<br/>                                                                                                                                    |
| [**CATEGORIA DE MENSAGEM DA FILA \_ DE INFORMAÇÕES \_ \_ DO \_ DXGI**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_category)<br/>                   | Valores que especificam categorias de mensagens de depuração.<br/>                                                                                                                      |
| [**SEVERIDADE DA MENSAGEM \_ DA FILA DE INFORMAÇÕES \_ \_ DO \_ DXGI**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_severity)<br/>                   | Valores que especificam níveis de severidade da mensagem de depuração para uma fila de informações.<br/>                                                                                            |
| [**GRUPO DE \_ SEGMENTOS DE MEMÓRIA DXGI \_ \_**](/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)<br/>                                  | Especifica o grupo de segmentos de memória a ser usado.<br/>                                                                                                                             |
| [**ROTAÇÃO DO MODO \_ \_ DXGI**](/previous-versions/windows/desktop/legacy/bb173065(v=vs.85))<br/>                                        | Sinalizadores que indicam como os buffers de fundo devem ser girados para se ajustar à rotação física de um monitor.<br/>                                                                  |
| [**DIMENSIONAMENTO DO MODO DXGI \_ \_**](/previous-versions/windows/desktop/legacy/bb173066(v=vs.85))<br/>                                          | Sinalizadores que indicam como uma imagem é alongada para se ajustar à resolução de um determinado monitor.<br/>                                                                                        |
| [**ORDEM \_ SCANLINE DO \_ MODO DXGI \_**](/previous-versions/windows/desktop/legacy/bb173067(v=vs.85))<br/>                           | Sinalizadores que indicam o método usado pelo raster para criar uma imagem em uma superfície.<br/>                                                                                           |
| [**SINALIZADORES \_ \_ YCbCr DE SOBREPOSIÇÃO \_ DE MULTIPLANO DXGI \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags)<br/>             | Opções para o espaço de cores da cadeia de permuta.<br/>                                                                                                                                    |
| [**SINALIZADORES DE RECURSOS \_ \_ DA OFERTA DXGI \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags)<br/>                                  | Especifica sinalizadores para o [**método OfferResources1.**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1)<br/>                                                                                |
| [**PRIORIDADE DE RECURSO DA OFERTA DXGI \_ \_ \_**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority)<br/>                           | Identifica a importância do conteúdo de um recurso quando você chama o [**método IDXGIDevice2::OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) para oferecer o recurso. <br/> |
| [**TIPO DE FORMA DE PONTEIRO DXGI \_ OUTDUPL \_ \_ \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_outdupl_pointer_shape_type)<br/>                     | Identifica o tipo de forma do ponteiro.<br/>                                                                                                                                  |
| [**SINALIZADOR DE SUPORTE DE ESPAÇO \_ \_ DE COR DE \_ SOBREPOSIÇÃO \_ DO DXGI \_**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_overlay_color_space_support_flag)<br/>        | Especifica o suporte para espaço de cor de sobreposição.<br/>                                                                                                                             |
| [**SINALIZADOR DE SUPORTE \_ DE SOBREPOSIÇÃO DO DXGI \_ \_**](/windows/desktop/api/DXGI1_3/ne-dxgi1_3-dxgi_overlay_support_flag)<br/>                                  | Especifica o suporte de sobreposição para verificar em uma chamada para [**IDXGIOutput3::CheckOverlaySupport**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgioutput3-checkoverlaysupport).<br/>                                     |
| [**RESULTADOS DO RECURSO \_ DE \_ RECUPERAÇÃO DO DXGI \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results)<br/>                          | Especifica sinalizadores de resultado para o [**método ReclaimResources1.**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1)<br/>                                                                     |
| [**RESIDÊNCIA DO \_ DXGI**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency)<br/>                                                 | Sinalizadores que indicam o local de memória de um recurso.<br/>                                                                                                                    |
| [**DIMENSIONAMENTO \_ DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling)<br/>                                                              | Identifica o comportamento de resize quando o tamanho do buffer de fundo não corresponder ao tamanho da saída de destino.<br/>                                                                     |
| [**SINALIZADOR DE SUPORTE DE ESPAÇO DE COR DA \_ \_ CADEIA DE \_ \_ PERMUTA \_ DO \_ DXGI**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag)<br/> | Especifica o suporte ao espaço de cores para a cadeia de permuta.<br/>                                                                                                                      |
| [**SINALIZADOR DE CADEIA \_ DE \_ PERMUTA DXGI \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag)<br/>                                   | Opções para o comportamento da cadeia de permuta.<br/>                                                                                                                                       |
| [**EFEITO SWAP \_ DXGI \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)<br/>                                                     | Opções para lidar com pixels em uma superfície de exibição depois de chamar [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). <br/>                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

