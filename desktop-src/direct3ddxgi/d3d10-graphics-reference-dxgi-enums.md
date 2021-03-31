---
description: Esta seção contém informações sobre as enumerações fornecidas pelo DXGI.
ms.assetid: c4574c89-dee2-4841-9318-5383cf417111
title: Enumerações de DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49f8309552662d0edd9833ce037a256c3c09c48
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645756"
---
# <a name="dxgi-enumerations"></a>Enumerações de DXGI

Esta seção contém informações sobre as enumerações fornecidas pelo DXGI.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                         | Descrição                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_sinalizador do adaptador dxgi \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag)<br/>                                          | Identifica o tipo de adaptador DXGI.<br/>                                                                                                                                   |
| [**\_Adaptador dxgi \_ FLAG3**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)<br/>                                        | Identifica o tipo de adaptador DXGI.<br/>                                                                                                                                   |
| [**\_modo alfa \_ dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)<br/>                                                       | Identifica o valor alfa, o comportamento de transparência de uma superfície.<br/>                                                                                                       |
| [**\_tipo de \_ espaço de cores dxgi \_**](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)<br/>                                          | Especifica os tipos de espaço de cor.<br/>                                                                                                                                           |
| [**\_granularidade de \_ preempção de computação \_ dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_compute_preemption_granularity)<br/>              | Identifica a granularidade na qual a GPU (unidade de processamento gráfico) pode ser admitida de executar sua tarefa de computação atual.<br/>                                      |
| [**\_sinalizadores de \_ RLO de depuração dxgi \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_debug_rlo_flags)<br/>                                            | Sinalizadores usados com [**ReportLiveObjects**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgidebug-reportliveobjects) para especificar a quantidade de informações a serem relatadas sobre o tempo de vida de um objeto. <br/>                         |
| [**\_recurso dxgi**](/windows/desktop/api/DXGI1_5/ne-dxgi1_5-dxgi_feature)<br/>                                                              | Especifica um intervalo de recursos de hardware a ser usado ao verificar o suporte a recursos.<br/>                                                                                  |
| [**\_formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br/>                                                       | Formatos de dados de recurso, incluindo formatos totalmente tipados e de tipo incompleto. Uma lista de modificadores na parte inferior da página descreve mais totalmente cada tipo de formato. <br/>               |
| [**\_modo de \_ apresentação de quadro dxgi \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode)<br/>                            | Indica opções para apresentar quadros à cadeia de permuta. <br/>                                                                                                            |
| [**\_preferência de GPU dxgi \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference)<br/>                                               | A preferência de GPU na qual o aplicativo será executado.<br/>                                                                                                                           |
| [**\_granularidade de \_ preempção de gráficos \_ dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_graphics_preemption_granularity)<br/>            | Identifica a granularidade na qual a GPU pode ser admitida de executar sua tarefa atual de renderização de gráficos.<br/>                                                      |
| [**\_sinalizadores de \_ suporte de composição de hardware dxgi \_ \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)<br/>     | Descreve quais níveis de composição de hardware são compatíveis.<br/>                                                                                                          |
| [**\_tipo de \_ metadados \_ HDR dxgi**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type)<br/>                                        | Especifica o tipo de metadados do cabeçalho.<br/>                                                                                                                                    |
| [**\_categoria de \_ mensagem da fila de informações dxgi \_ \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_category)<br/>                   | Valores que especificam categorias de mensagens de depuração.<br/>                                                                                                                      |
| [**\_severidade de \_ mensagem da fila de informações dxgi \_ \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_severity)<br/>                   | Valores que especificam os níveis de severidade da mensagem de depuração para uma fila de informações.<br/>                                                                                            |
| [**\_grupo de \_ segmentos de memória dxgi \_**](/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)<br/>                                  | Especifica o grupo de segmentos de memória a ser usado.<br/>                                                                                                                             |
| [**\_rotação do modo dxgi \_**](/previous-versions/windows/desktop/legacy/bb173065(v=vs.85))<br/>                                        | Sinalizadores que indicam como os buffers posteriores devem ser girados para se ajustarem à rotação física de um monitor.<br/>                                                                  |
| [**\_dimensionamento do modo dxgi \_**](/previous-versions/windows/desktop/legacy/bb173066(v=vs.85))<br/>                                          | Sinalizadores que indicam como uma imagem é ampliada para se ajustar a uma determinada resolução do monitor.<br/>                                                                                        |
| [**\_ordem de \_ varredura do modo dxgi \_**](/previous-versions/windows/desktop/legacy/bb173067(v=vs.85))<br/>                           | Sinalizadores que indicam o método que a varredura usa para criar uma imagem em uma superfície.<br/>                                                                                           |
| [**\_ \_ Sinalizadores YCbCr de sobreposição MULTIplan dxgi \_ \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags)<br/>             | Opções para o espaço de cores da cadeia de permuta.<br/>                                                                                                                                    |
| [**\_sinalizadores de \_ recursos da oferta dxgi \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags)<br/>                                  | Especifica os sinalizadores para o método [**OfferResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) .<br/>                                                                                |
| [**\_prioridade de \_ recursos da oferta dxgi \_**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority)<br/>                           | Identifica a importância de um conteúdo de recurso s quando você chama o método [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) para oferecer o recurso. <br/> |
| [**\_tipo de \_ forma de ponteiro OUTDUPL \_ dxgi \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_outdupl_pointer_shape_type)<br/>                     | Identifica o tipo de forma de ponteiro.<br/>                                                                                                                                  |
| [**\_sinalizador de \_ \_ \_ suporte ao espaço de cores \_ de sobreposição de dxgi**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_overlay_color_space_support_flag)<br/>        | Especifica o suporte para o espaço de cores de sobreposição.<br/>                                                                                                                             |
| [**\_sinalizador de \_ suporte à sobreposição de dxgi \_**](/windows/desktop/api/DXGI1_3/ne-dxgi1_3-dxgi_overlay_support_flag)<br/>                                  | Especifica o suporte à sobreposição para verificar em uma chamada para [**IDXGIOutput3:: CheckOverlaySupport**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgioutput3-checkoverlaysupport).<br/>                                     |
| [**resultados de recursos de recuperação de DXGI \_ \_ \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results)<br/>                          | Especifica os sinalizadores de resultado para o método [**ReclaimResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) .<br/>                                                                     |
| [**residência de DXGI \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency)<br/>                                                 | Sinalizadores que indicam o local da memória de um recurso.<br/>                                                                                                                    |
| [**\_dimensionamento de dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling)<br/>                                                              | Identifica o comportamento de redimensionamento quando o tamanho do buffer de fundo não corresponde ao tamanho da saída de destino.<br/>                                                                     |
| [**\_sinalizador de \_ \_ \_ \_ suporte ao espaço de cores da cadeia de permuta dxgi \_**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag)<br/> | Especifica o suporte ao espaço de cores para a cadeia de permuta.<br/>                                                                                                                      |
| [**\_sinalizador de \_ cadeia de permuta dxgi \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag)<br/>                                   | Opções de comportamento de cadeia de permuta.<br/>                                                                                                                                       |
| [**\_efeito de permuta de dxgi \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)<br/>                                                     | Opções para tratamento de pixels em uma superfície de exibição depois de chamar [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). <br/>                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

