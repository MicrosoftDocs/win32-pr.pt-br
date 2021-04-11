---
description: Propriedades do ponto de extremidade de áudio
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: Propriedades do ponto de extremidade de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ce4ed9b853c2b73b73de014f3a4c8a90072a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164051"
---
# <a name="audio-endpoint-properties"></a>Propriedades do ponto de extremidade de áudio

O arquivo de cabeçalho Mmdeviceapi. h define várias propriedades de [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md) no Windows Vista e posterior. O serviço de áudio do Windows define os valores dessas propriedades. Os clientes podem ler essas propriedades, mas não devem defini-las. Os valores de propriedade são armazenados como estruturas **PROPVARIANT** .

A maneira recomendada de ler as propriedades de um dispositivo de entrada de áudio é usar as APIs no namespace [**Windows. Devices. Enumeration**](/uwp/api/Windows.Devices.Enumeration) . Essas APIs têm suporte para aplicativos da Windows Store e aplicativos da área de trabalho. Para aplicativos de área de trabalho existentes que lêem Propriedades de dispositivo usando a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , consulte [Propriedades do dispositivo](device-properties.md). **IMMDevice** não tem suporte para aplicativos da Windows Store.

Para obter exemplos de código que mostram como acessar as propriedades de um dispositivo de ponto de extremidade de áudio, consulte os seguintes tópicos:

-   [Eventos de dispositivo](device-events.md)
-   [Funções de dispositivo para aplicativos DirectSound](device-roles-for-directsound-applications.md)

Para obter informações sobre o **PROPVARIANT**, consulte a documentação do SDK do Windows.

As propriedades a seguir são específicas para dispositivos de ponto de extremidade de áudio.



| Propriedade                                                                                                            | Descrição                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ AudioEndpoint \_ Association**](pkey-audioendpoint-association.md)                                          | Associa uma categoria de PIN de streaming de kernel (KS) a um dispositivo de ponto de extremidade de áudio.                                                                                |
| [**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Especifica o CLSID do provedor registrado da extensão de propriedades de dispositivo para o dispositivo de ponto de extremidade de áudio.                                              |
| [**PKEY \_ AudioEndpoint \_ Disable \_ SysFx**](pkey-audioendpoint-disable-sysfx.md)                                     | Indica se os efeitos do sistema estão habilitados no fluxo de modo compartilhado que flui para ou do dispositivo de ponto de extremidade de áudio.                                       |
| [**PKEY \_ AudioEndpoint \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Indica os atributos físicos do dispositivo de ponto de extremidade de áudio.                                                                                               |
| [**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Especifica a máscara de configuração de canal para os alto-falantes de intervalo completo que estão conectados ao dispositivo de ponto de extremidade de áudio.                                         |
| [**PKEY \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md)                                                        | Fornece o identificador de dispositivo DirectSound que corresponde ao dispositivo de ponto de extremidade de áudio.                                                                     |
| [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Define a configuração de alto-falante físico para o dispositivo de ponto de extremidade de áudio.                                                                                     |
| [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md)                                            | Especifica o formato do dispositivo, que é o formato que o mecanismo de áudio usa para o fluxo de modo compartilhado que flui para ou do dispositivo de ponto de extremidade de áudio.       |
| [**PKEY \_ AudioEngine \_ OEMFormat**](pkey-audioengine-oemformat.md)<br/>                                       | Especifica o formato padrão do dispositivo que é usado para processar ou capturar um fluxo. Os valores são preenchidos pelo OEM em um arquivo. inf. <br/> |
| [**PKEY \_ AudioEndpoint \_ dá suporte ao \_ \_ modo EventDriven**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Indica se o ponto de extremidade dá suporte ao modo controlado por evento. Os valores são preenchidos pelo OEM em um arquivo. inf.<br/>                                |



 

As APIs de áudio principais dão suporte a propriedades adicionais que não se aplicam exclusivamente a dispositivos de ponto de extremidade de áudio. Para obter mais informações sobre essas propriedades adicionais, consulte [Propriedades do dispositivo](device-properties.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

