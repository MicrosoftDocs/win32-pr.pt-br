---
description: 'Essa referência de programação para o SDK de áudio principal inclui as seguintes interfaces:'
ms.assetid: b18e2094-e974-4c23-b70b-ace5a168132d
title: Interfaces de áudio de núcleo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 330bb620b48b865db3db2ab5ea5625b7859588bd8e53e1addbcd8fd8ec9bda6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109466"
---
# <a name="core-audio-interfaces"></a>Interfaces de áudio de núcleo

Essa referência de programação para o SDK de áudio principal inclui as seguintes interfaces:

## <a name="mmdevice-api"></a>API MMDevice

a API do dispositivo de multimídia Windows (MMDevice) permite que os clientes de áudio descubram [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md), determinem seus recursos e criem instâncias de driver para esses dispositivos. O arquivo de cabeçalho Mmdeviceapi. h define as interfaces na API MMDevice. Para obter mais informações, consulte [about MMDEVICE API](mmdevice-api.md).

a tabela a seguir lista as interfaces MMDevice disponíveis com o SDK de áudio principal para Windows Vista.



| Interface                                              | Descrição                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                         | Representa um dispositivo de áudio.                                                                                                                                                                    |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)     | Representa uma coleção de dispositivos de áudio.                                                                                                                                                      |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)     | Fornece métodos para enumerar dispositivos de áudio.                                                                                                                                                |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                     | Representa um dispositivo de ponto de extremidade de áudio.                                                                                                                                                           |
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Fornece notificações quando um dispositivo de ponto de extremidade de áudio é adicionado ou removido, quando o estado ou as propriedades de um dispositivo são alterados ou quando há uma alteração na função padrão atribuída a um dispositivo. |



 

## <a name="wasapi"></a>WASAPI

o Windows API de sessão de áudio (WASAPI) permite que os aplicativos cliente gerenciem o fluxo de dados de áudio entre o aplicativo e um [dispositivo de ponto de extremidade de áudio](audio-endpoint-devices.md). Os arquivos de cabeçalho Audioclient. h e Audiopolicy. h definem as interfaces WASAPI. Para obter mais informações, consulte [about WASAPI](wasapi.md).

a tabela a seguir lista as interfaces WASAPI disponíveis com o SDK de áudio principal para Windows Vista e posterior.



| Interface                                                                                    | Descrição                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActivateAudioInterfaceAsyncOperation**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation)       | Representa uma operação assíncrona ativando uma interface [WASAPI](wasapi.md) e fornece um método para recuperar os resultados da ativação.<br/> Aplica-se começando com Windows 8.<br/> |
| [**IActivateAudioInterfaceCompletionHandler**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler) | Fornece um retorno de chamada para indicar que a ativação de uma interface [WASAPI](wasapi.md) foi concluída.<br/> Aplica-se começando com Windows 8.<br/>                                                  |
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)                                           | Permite que um cliente leia dados de entrada de um buffer de ponto de extremidade de captura.                                                                                                                                       |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                                                         | Permite que um cliente crie e inicialize um fluxo de áudio entre um aplicativo de áudio e o mecanismo de áudio ou o buffer de hardware de um dispositivo de ponto de extremidade de áudio.                                           |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                                                           | Permite que um cliente monitore a taxa de dados de um fluxo e a posição atual no fluxo.                                                                                                                  |
| [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)<br/>                                              | Permite que um cliente obtenha a posição atual do dispositivo.<br/>                                                                                                                                           |
| [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)<br/>                            | Permite que um cliente defina a taxa de amostragem de um fluxo.<br/>                                                                                                                                           |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)                                             | Permite que um cliente grave dados de saída em um buffer de ponto de extremidade de renderização.                                                                                                                                     |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)                                         | Permite que um cliente configure os parâmetros de controle para uma sessão de áudio e monitore eventos na sessão.                                                                                           |
| [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)<br/>                            | Permite que um cliente obtenha informações sobre a sessão de áudio.<br/>                                                                                                                                   |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)                                         | Permite que um cliente acesse os controles de sessão e os controles de volume para sessões de áudio de processo cruzado e específicas de processo.                                                                           |
| [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)<br/>                            | Gerencia todas as subestações, incluindo enumeração e notificação de subcombinações. Ele também fornece suporte para notificações de pato.<br/>                                                                   |
| [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)<br/>                        | Permite que um cliente enumere sessões de áudio.<br/>                                                                                                                                                  |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)                                             | Permite que um cliente controle e monitore os níveis de volume para todos os canais em um fluxo de áudio.                                                                                                     |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)                                           | Permite que um cliente controle os níveis de volume para todos os canais na sessão de áudio a que o fluxo pertence.                                                                                    |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)                                             | Permite que um cliente controle o nível de volume mestre de uma sessão de áudio.                                                                                                                                  |
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)                                           | Fornece notificações de eventos relacionados à sessão, como alterações no nível do volume, no nome de exibição e no estado da sessão.                                                                                    |
| [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)<br/>                    | Envia notificações quando ocorrem alterações na sessão. <br/>                                                                                                                                               |
| [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)<br/>              | Envia notificações sobre alterações de patos do sistema pendentes.<br/>                                                                                                                                      |



 

## <a name="devicetopology-api"></a>API DeviceTopology

A API do DeviceTopology fornece aos aplicativos cliente a capacidade de atravessar as topologias de hardware funcionais dos dispositivos de renderização e captura de áudio. O arquivo de cabeçalho Devicetopology. h define as interfaces na API DeviceTopology. Para obter mais informações, consulte [topologias de dispositivo](device-topologies.md) e [**API DeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology).

a tabela a seguir lista as interfaces DeviceTopology disponíveis com o SDK de áudio principal para Windows Vista e posterior.



| Interface                                                           | Descrição                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)              | Fornece acesso a um AGC (controle de acesso automático de hardware).                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                                    | Fornece acesso a um controle de nível baixo de hardware.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)                  | Fornece acesso a um controle de configuração de canal de hardware.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)                  | Fornece acesso a um controle de Multiplexador de hardware (seletor de entrada).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                            | Fornece acesso a um controle de compensação de "intensidade".                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                            | Fornece acesso a um controle de nível de midrange de hardware.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                                    | Fornece acesso a um controle de mudo de hardware.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)                | Fornece acesso a um controle de demultiplexador de hardware (seletor de saída).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                          | Fornece acesso a um controle de medidor de pico de hardware.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                                | Fornece acesso a um controle de nível de agudo de hardware.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)                      | Fornece acesso a um controle de volume de hardware.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                                    | Representa um ponto de conexão entre componentes.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)                      | Representa uma interface de controle em uma parte (subunidade ou conector).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)          | Representa uma propriedade específica do dispositivo de um conector ou subunidade.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                          | Fornece acesso à topologia de um dispositivo de áudio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)                        | Fornece informações sobre os formatos de dados de áudio com suporte por uma conexão de E/S configurada por software (normalmente um canal DMA) entre o dispositivo de áudio e a memória do sistema.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)                    | Fornece informações sobre os conectores internos ou conectores internos que fornecem uma conexão física entre um dispositivo em um adaptador de áudio e um dispositivo de ponto de extremidade externo ou interno (por exemplo, um microfone ou player de CD). |
| [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)<br/>       | Fornece acesso conveniente à **propriedade KSPROPERTY \_ JACK \_ DESCRIPTION2** de um conector para um dispositivo de ponto de extremidade.<br/>                                                                                            |
| [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)<br/> | Fornece informações sobre o valete se o jack for suportado pelo hardware.<br/>                                                                                                                             |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                              | Representa uma parte (conector ou subunidade) de uma topologia de dispositivo.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                                    | Representa uma lista de partes (conectores e subunidades).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)                    | Representa uma interface de controle de subunidade genérica que fornece controle por canal sobre o nível de volume, em decibéis, de um fluxo de áudio ou de uma faixa de frequência em um fluxo de áudio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                                        | Representa uma subunidade de hardware (por exemplo, um controle de nível de volume) que está no caminho de dados entre um cliente e um dispositivo de ponto de extremidade de áudio.                                                                             |
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify)                | Fornece notificações quando o status de uma parte (conector ou subunidade) muda.                                                                                                                                          |



 

## <a name="endpointvolume-api"></a>EndpointVolume API

A API EndpointVolume permite que clientes especializados controlem e monitorem os níveis de volume de dispositivos [de ponto de extremidade de áudio](audio-endpoint-devices.md). O arquivo de header Endpointvolume.h define as interfaces na API EndpointVolume. Para obter mais informações, consulte [**EndpointVolume API**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) .

A tabela a seguir lista as interfaces EndpointVolume disponíveis com o SDK de Áudio Principal para Windows Vista.



| **Interface**                                                        | **Descrição**                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)                 | Representa os controles de volume no fluxo de áudio de ou para um dispositivo de ponto de extremidade de áudio.           |
| [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)<br/>  | Fornece controles de volume no fluxo de áudio de ou para um ponto de extremidade do dispositivo.<br/>             |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation)             | Representa um medidor de pico no fluxo de áudio de ou para um dispositivo de ponto de extremidade de áudio.                  |
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Fornece notificações quando o nível de volume ou o estado de muting de um dispositivo de ponto de extremidade de áudio muda. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação](programming-reference.md)
</dt> </dl>

 

