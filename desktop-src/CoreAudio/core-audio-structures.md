---
description: Estruturas de áudio principais
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Estruturas de áudio principais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8ea83d0de4c07c1a3d36bab169d5cb581e82cf60e84e308d04dff49af0dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407210"
---
# <a name="core-audio-structures"></a>Estruturas de áudio principais

Esta seção descreve as estruturas usadas pelas APIs de Áudio Principal no Windows Vista e posterior.



| Estrutura                                                                     | Descrição                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DADOS DE \_ NOTIFICAÇÃO DE VOLUME \_ DE \_ ÁUDIO**](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | Descreve uma alteração no nível do volume ou estado de mutação de um dispositivo de ponto de extremidade de áudio.                                                                                 |
| [**\_PARAMS DE \_ ATIVAÇÃO DE \_ ÁUDIO DIRECTX**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | Especifica os parâmetros de inicialização para um fluxo DirectSound.                                                                                                   |
| [**DESCRIÇÃO DO \_ KSJACK**](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | Recuperado por [**meio de IKsJackDescription::GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); descreve uma tomada de áudio.                                 |
| [**KSJACK \_ DESCRIPTION2**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | Recuperado por [**meio de IKsJackDescription2::GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); descreve uma tomada de áudio. <br/>                 |
| [**INFORMAÇÕES DO KSJACK \_ SINK \_**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | Recuperado por [**meio de IKsJackSinkInformation::GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); descreve um sink de tomada de áudio.<br/> |
| [**Luid**](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | Armazena o identificador de porta de vídeo.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação](programming-reference.md)
</dt> </dl>

 

 




