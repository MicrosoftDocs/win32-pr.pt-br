---
description: Estruturas de áudio de núcleo
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Estruturas de áudio de núcleo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078f49ac7abce8fc2773549df26431b780550c1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753560"
---
# <a name="core-audio-structures"></a>Estruturas de áudio de núcleo

Esta seção descreve as estruturas usadas pelas principais APIs de áudio no Windows Vista e versões posteriores.



| Estrutura                                                                     | Descrição                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_dados de \_ notificação por volume de áudio \_**](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | Descreve uma alteração no nível do volume ou estado de mudo de um dispositivo de ponto de extremidade de áudio.                                                                                 |
| [**\_ \_ params de ativação de áudio DirectX \_**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | Especifica os parâmetros de inicialização para um fluxo do DirectSound.                                                                                                   |
| [**Descrição de KSJACK \_**](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | Recuperado por meio de [**IKsJackDescription:: GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); descreve uma tomada de áudio.                                 |
| [**KSJACK \_ DESCRIPTION2**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | Recuperado por meio de [**IKsJackDescription2:: GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); descreve uma tomada de áudio. <br/>                 |
| [**\_informações do coletor KSJACK \_**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | Recuperado por meio de [**IKsJackSinkInformation:: GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); Descreve um coletor de tomada de áudio.<br/> |
| [**LUID**](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | Armazena o identificador da porta de vídeo.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação](programming-reference.md)
</dt> </dl>

 

 




