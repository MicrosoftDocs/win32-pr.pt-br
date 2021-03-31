---
title: Estruturas XAudio2
description: Esta seção contém informações sobre estruturas fornecidas pela API do Microsoft XAudio2.
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b67e0312c5ac6b753881d895dff3972564f2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663147"
---
# <a name="xaudio2-structures"></a>Estruturas XAudio2

Esta seção contém informações sobre estruturas fornecidas pela API do Microsoft XAudio2.



| Estrutura                                                                                 | Descrição                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | Representa um buffer de dados de áudio.<br/>                                                                                                    |
| [**XAUDIO2 \_ buffer \_ WMA**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | Representa um buffer de dados de áudio de WMA.<br/>                                                                                                 |
| [**\_Configuração de depuração XAudio2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | Define uma nova configuração de depuração global para XAudio2 quando usada pela função SetDebugConfiguration.                                             |
| [**\_Cadeia de efeito de XAudio2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | Define uma cadeia de efeitos.<br/>                                                                                                            |
| [**\_Descritor de efeito XAudio2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | Define um efeito.<br/>                                                                                                                  |
| [**\_Parâmetros de filtro XAudio2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | Define os parâmetros de filtro para uma voz de origem.<br/>                                                                                       |
| [**\_Dados de desempenho do XAudio2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | Recupera informações de desempenho.<br/>                                                                                                  |
| [**\_Descritor de envio XAudio2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | Descreve um destino de envio de voz.<br/>                                                                                                 |
| [**\_Detalhes de voz do XAudio2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | Contém informações sobre os sinalizadores de criação, os canais de entrada e a taxa de amostra de uma voz.<br/>                                          |
| [**\_Envios de voz XAudio2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | Define um conjunto de vozes para receber dados de uma única voz de saída.<br/>                                                                 |
| [**\_Estado de voz XAudio2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | Retorna o estado atual da voz e os dados da posição do cursor.<br/>                                                                         |
| [**\_Parâmetros de I3DL2 de reverberação de XAUDIO2FX \_ \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | Descreve os parâmetros de I3DL2 (diretrizes de renderização de áudio 3D interativo nível 2,0) para uso na função ReverbConvertI3DL2ToNative.           |
| [**\_Parâmetros de reverberação XAUDIO2FX \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | Descreve os parâmetros para uso no APO de reverberação.                                                                                                |
| [**XAUDIO2FX \_ VOLUMEMETER \_ níveis**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | Descreve os parâmetros para uso com o APO de medidor de volume.                                                                                        |
| [**\_parâmetros de \_ buffer XAPO LOCKFORPROCESS \_**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | Define os parâmetros de buffer que permanecem constantes enquanto um XAPO está bloqueado.<br/>                                                             |
| [**\_parâmetros de \_ buffer de processo XAPO \_**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | Define os parâmetros de buffer que podem mudar de uma chamada para a próxima.<br/>                                                                |
| [**\_Propriedades de registro do XAPO \_**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | Descreve as características gerais de um XAPO.<br/>                                                                                       |
| [**FXECHO \_ INITDATA**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | Parâmetros de inicialização para uso com FXECHO XAPO.<br/>                                                                             |
| [**parâmetros de FXECHO \_**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | Parâmetros para uso com FXECHO XAPO.<br/>                                                                                            |
| [**parâmetros de FXEQ \_**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | Parâmetros para uso com FXEQ XAPO.<br/>                                                                                              |
| [**parâmetros de FXMASTERINGLIMITER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | Parâmetros para uso com FXMasteringLimiter XAPO.<br/>                                                                                |
| [**parâmetros de FXREVERB \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | Parâmetros para uso com FXReverb XAPO.<br/>                                                                                          |
| [**\_Cone X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | Especifica a direcionalidade para um emissor não-LFE de canal único, dimensionando o comportamento do DSP em relação à orientação do emissor.<br/>    |
| [**\_Curva de distância X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | Define uma curva piecewise explícita composta por segmentos lineares, definindo diretamente o comportamento do DSP com relação à distância normalizada.<br/> |
| [**\_Ponto de \_ curva de distância X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | Define uma configuração de DSP em uma determinada distância normalizada.<br/>                                                                               |
| [**\_Configurações do DSP X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | Recebe os resultados de uma chamada para X3DAudioCalculate.<br/>                                                                              |
| [**Emissor de X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | Define uma fonte de áudio 3D única ou de vários pontos usada com um número arbitrário de canais de som.<br/>                                    |
| [**\_Ouvinte de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | Define um ponto de recebimento de áudio 3D.<br/>                                                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação](programming-reference.md)
</dt> </dl>

 

 




