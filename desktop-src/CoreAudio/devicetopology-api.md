---
description: API DeviceTopology
ms.assetid: 051311ef-dd29-4014-bb9c-4cdccf7ce7de
title: API DeviceTopology
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 472c02cd59ca0cadd922cbe398a768c97cfab73a
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105749299"
---
# <a name="devicetopology-api"></a>API DeviceTopology

Consulte o [exemplo de Microsoft de alta qualidade Voice Capture DMO](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/audio/aecmicarray).

A API do DeviceTopology fornece aos aplicativos cliente a capacidade de atravessar as topologias de hardware funcionais dos dispositivos de renderização e captura de áudio. Por meio das interfaces e métodos na API DeviceTopology, os clientes podem descobrir as subunidades funcionais (por exemplo, controle de volume) que se encontram nos caminhos de dados que levam e para [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md). Os clientes podem atravessar as topologias internas de dispositivos de adaptador de áudio e dispositivos de ponto de extremidade de áudio e passar pelas conexões que vinculam um dispositivo a outro. Para obter mais informações, consulte [topologias de dispositivo](device-topologies.md).

O arquivo de cabeçalho Devicetopology. h define as interfaces na API DeviceTopology.

Para acessar as interfaces de API do DeviceTopology, um cliente primeiro obtém uma referência à interface [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) para um dispositivo de ponto de extremidade de áudio seguindo estas etapas:

1.  Usando uma das técnicas descritas na [**interface IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice), obtenha uma referência à interface **IMMDevice** para um dispositivo de ponto de extremidade de áudio.
2.  Chame o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) com o parâmetro *IID* definido como **REFIID** IID \_ IDeviceTopology.

O cliente pode obter referências às outras interfaces na API DeviceTopology chamando os métodos na interface [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) .

A API DeviceTopology implementa as interfaces a seguir.



| Interface                                                  | Descrição                                                                                                                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | Fornece acesso a um AGC (controle de acesso automático de hardware).                                                                                                                                                               |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | Fornece acesso a um controle de nível baixo de hardware.                                                                                                                                                                         |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | Fornece acesso a um controle de configuração de canal de hardware.                                                                                                                                                              |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | Fornece acesso a um controle de Multiplexador de hardware (seletor de entrada).                                                                                                                                                       |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | Fornece acesso a um controle de compensação de "intensidade".                                                                                                                                                                     |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | Fornece acesso a um controle de nível de midrange de hardware.                                                                                                                                                                     |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | Fornece acesso a um controle de mudo de hardware.                                                                                                                                                                               |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | Fornece acesso a um controle de demultiplexador de hardware (seletor de saída).                                                                                                                                                    |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | Fornece acesso a um controle de medidor de pico de hardware.                                                                                                                                                                         |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | Fornece acesso a um controle de nível de agudo de hardware.                                                                                                                                                                       |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | Fornece acesso a um controle de volume de hardware.                                                                                                                                                                             |
| [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector)                           | Representa um ponto de conexão entre componentes.                                                                                                                                                                      |
| [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)             | Representa uma interface de controle em uma parte (subunidade ou conector).                                                                                                                                                          |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | Representa uma propriedade específica do dispositivo de um conector ou subunidade.                                                                                                                                                          |
| [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology)                 | Fornece acesso à topologia de um dispositivo de áudio.                                                                                                                                                                       |
| [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)               | Fornece informações sobre os formatos de dados de áudio com suporte de uma conexão de e/s configurada por software (normalmente um canal DMA) entre o dispositivo de áudio e a memória do sistema.                                        |
| [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)           | Fornece informações sobre as tomadas ou conectores internos que fornecem uma conexão física entre um dispositivo em um adaptador de áudio e um dispositivo de ponto de extremidade interno ou externo (por exemplo, um microfone ou CD player). |
| [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart)                                     | Representa uma parte (conector ou subunidade) de uma topologia de dispositivo.                                                                                                                                                            |
| [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist)                           | Representa uma lista de partes (conectores e subunidades).                                                                                                                                                                     |
| [**IPerChannelDbLevel**](/windows/desktop/api/Devicetopology/nn-devicetopology-iperchanneldblevel)           | Representa uma interface de controle de subunidade genérica que fornece controle por canal sobre o nível de volume, em decibéis, de um fluxo de áudio ou de uma banda de frequência em um fluxo de áudio.                                        |
| [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit)                               | Representa uma subunidade de hardware (por exemplo, um controle de nível de volume) que está no caminho de dados entre um cliente e um dispositivo de ponto de extremidade de áudio.                                                                             |



 

Os clientes da API DeviceTopology que exigem a notificação de eventos de alteração de controle em conectores e subunidades devem implementar a interface a seguir.



| Interface                                            | Descrição                                                                      |
|------------------------------------------------------|----------------------------------------------------------------------------------|
| [**IControlChangeNotify**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolchangenotify) | Fornece notificações quando o status de uma parte (conector ou subunidade) é alterado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Topologias de dispositivo](device-topologies.md)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 
