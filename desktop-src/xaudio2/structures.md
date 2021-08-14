---
title: Estruturas XAudio2
description: Esta seção contém informações sobre estruturas fornecidas pela API do Microsoft XAudio2.
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59dcbdf454f282ca696a040aa7c1a3fe84c372ca4e0607c0a60f18b59d5f5e42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962585"
---
# <a name="xaudio2-structures"></a>Estruturas XAudio2

Esta seção contém informações sobre estruturas fornecidas pela API do Microsoft XAudio2.



| Estrutura                                                                                 | Descrição                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XAUDIO2 \_ BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | Representa um buffer de dados de áudio.<br/>                                                                                                    |
| [**\_WMA DE BUFFER XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | Representa um buffer de dados de áudio WMA.<br/>                                                                                                 |
| [**CONFIGURAÇÃO DE \_ DEPURAÇÃO XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | Define uma nova configuração de depuração global para XAudio2 quando usada pela função SetDebugConfiguration.                                             |
| [**CADEIA DE EFEITO XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | Define uma cadeia de efeitos.<br/>                                                                                                            |
| [**\_DESCRITOR DE EFEITO XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | Define um efeito.<br/>                                                                                                                  |
| [**PARÂMETROS DE FILTRO XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | Define parâmetros de filtro para uma voz de origem.<br/>                                                                                       |
| [**DADOS DE DESEMPENHO XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | Recupera informações de desempenho.<br/>                                                                                                  |
| [**DESCRITOR \_ DE ENVIO \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | Descreve um destino de envio de voz.<br/>                                                                                                 |
| [**DETALHES DA VOZ XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | Contém informações sobre os sinalizadores de criação, os canais de entrada e a taxa de amostra de uma voz.<br/>                                          |
| [**XAUDIO2 \_ VOICE \_ SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | Define um conjunto de vozes para receber dados de uma única voz de saída.<br/>                                                                 |
| [**ESTADO DE VOZ XAUDIO2 \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | Retorna o estado atual da voz e os dados de posição do cursor.<br/>                                                                         |
| [**PARÂMETROS XAUDIO2FX \_ REVERB \_ I3DL2 \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | Descreve parâmetros I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) para uso na função ReverbConvertI3DL2ToNative.           |
| [**PARÂMETROS REVERB XAUDIO2FX \_ \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | Descreve parâmetros para uso no APO reverb.                                                                                                |
| [**NÍVEIS DE VOLUMEMETER XAUDIO2FX \_ \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | Descreve parâmetros para uso com o APO do medidor de volume.                                                                                        |
| [**PARÂMETROS DE \_ BUFFER XAPO LOCKFORPROCESS \_ \_**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | Define parâmetros de buffer que permanecem constantes enquanto um XAPO é bloqueado.<br/>                                                             |
| [**PARÂMETROS DE BUFFER DO PROCESSO XAPO \_ \_ \_**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | Define parâmetros de buffer que podem mudar de uma chamada para a próxima.<br/>                                                                |
| [**PROPRIEDADES DE REGISTRO \_ \_ XAPO**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | Descreve as características gerais de um XAPO.<br/>                                                                                       |
| [**FXECHO \_ INITDATA**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | Parâmetros de inicialização para uso com o XAPO FXECHO.<br/>                                                                             |
| [**PARÂMETROS FXECHO \_**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | Parâmetros para uso com o XAPO FXECHO.<br/>                                                                                            |
| [**PARÂMETROS FXEQ \_**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | Parâmetros para uso com o XAPO FXEQ.<br/>                                                                                              |
| [**PARÂMETROS FXMASTERINGLIMITER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | Parâmetros para uso com o XAPO FXMasteringLimiter.<br/>                                                                                |
| [**PARÂMETROS FXREVERB \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | Parâmetros para uso com o XAPO FXReverb.<br/>                                                                                          |
| [**X3DAUDIO \_ CONE**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | Especifica a direcionalidade para um emissor não LFE de canal único dimensionando o comportamento do DSP em relação à orientação do emissor.<br/>    |
| [**CURVA DE DISTÂNCIA DE X3DAUDIO \_ \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | Define uma curva por parte explícita feita de segmentos lineares, definindo diretamente o comportamento do DSP em relação à distância normalizada.<br/> |
| [**PONTO DE CURVA DE DISTÂNCIA DE X3DAUDIO \_ \_ \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | Define uma configuração de DSP a uma determinada distância normalizada.<br/>                                                                               |
| [**CONFIGURAÇÕES DO DSP X3DAUDIO \_ \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | Recebe os resultados de uma chamada para X3DAudioCalculate.<br/>                                                                              |
| [**X3DAUDIO \_ EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | Define uma fonte de áudio 3D de ponto único ou multi point usada com um número arbitrário de canais de som.<br/>                                    |
| [**OUVINTE X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | Define um ponto de recepção de áudio 3D.<br/>                                                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação](programming-reference.md)
</dt> </dl>

 

 




