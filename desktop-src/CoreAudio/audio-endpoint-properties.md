---
description: Propriedades do ponto de extremidade de áudio
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: Propriedades do ponto de extremidade de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf76ef70afaed98ed04ad2ee56e83c38c14ffde1bb6e4d43b557d25769afb2f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828497"
---
# <a name="audio-endpoint-properties"></a>Propriedades do ponto de extremidade de áudio

O arquivo de header Mmdeviceapi.h define várias propriedades de dispositivos de ponto de extremidade de [áudio](audio-endpoint-devices.md) no Windows Vista e posterior. O Windows de áudio define os valores dessas propriedades. Os clientes podem ler essas propriedades, mas não devem defini-las. Os valores de propriedade são armazenados **como estruturas PROPVARIANT.**

A maneira recomendada de ler as propriedades de um dispositivo de entrada de áudio é usar as APIs no [**Windows. Namespace Devices.Enumeration.**](/uwp/api/Windows.Devices.Enumeration) Essas APIs têm suporte para aplicativos Windows Store e aplicativos da área de trabalho. Para aplicativos da área de trabalho existentes que leem as propriedades do dispositivo usando a interface [**IMMDevice,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) consulte [Propriedades do dispositivo](device-properties.md). **Não há suporte para IMMDevice** para aplicativos Windows Store.

Para exemplos de código que mostram como acessar as propriedades de um dispositivo de ponto de extremidade de áudio, consulte os seguintes tópicos:

-   [Eventos de dispositivo](device-events.md)
-   [Funções de dispositivo para aplicativos DirectSound](device-roles-for-directsound-applications.md)

Para obter informações sobre **PROPVARIANT,** consulte a documentação Windows do SDK.

As propriedades a seguir são específicas para dispositivos de ponto de extremidade de áudio.



| Propriedade                                                                                                            | Descrição                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Associação de \_ AudioEndpoint PKEY \_**](pkey-audioendpoint-association.md)                                          | Associa uma categoria de pino de streaming de kernel (KS) a um dispositivo de ponto de extremidade de áudio.                                                                                |
| [**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Especifica o CLSID do provedor registrado da extensão de propriedades do dispositivo para o dispositivo de ponto de extremidade de áudio.                                              |
| [**PKEY \_ AudioEndpoint \_ Disable \_ SysFx**](pkey-audioendpoint-disable-sysfx.md)                                     | Indica se os efeitos do sistema estão habilitados no fluxo de modo compartilhado que flui para ou do dispositivo de ponto de extremidade de áudio.                                       |
| [**PKEY \_ AudioEndpoint \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Indica os atributos físicos do dispositivo de ponto de extremidade de áudio.                                                                                               |
| [**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Especifica a máscara de configuração de canal para os alto-falantes de intervalo completo que estão conectados ao dispositivo de ponto de extremidade de áudio.                                         |
| [**GUID do \_ ponto de vista de áudio \_ PKEY**](pkey-audioendpoint-guid.md)                                                        | Fornece o identificador de dispositivo DirectSound que corresponde ao dispositivo de ponto de extremidade de áudio.                                                                     |
| [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Define a configuração do locutor físico para o dispositivo de ponto de extremidade de áudio.                                                                                     |
| [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md)                                            | Especifica o formato do dispositivo, que é o formato que o mecanismo de áudio usa para o fluxo de modo compartilhado que flui para ou do dispositivo de ponto de extremidade de áudio.       |
| [**PKEY \_ AudioEngine \_ OEMFormat**](pkey-audioengine-oemformat.md)<br/>                                       | Especifica o formato padrão do dispositivo usado para renderizar ou capturar um fluxo. Os valores são preenchidos pelo OEM em um arquivo .inf. <br/> |
| [**O PKEY \_ AudioEndpoint \_ dá suporte ao modo \_ EventDriven \_**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Indica se o ponto de extremidade dá suporte ao modo orientado a eventos. Os valores são preenchidos pelo OEM em um arquivo .inf.<br/>                                |



 

As APIs de áudio principais são compatíveis com propriedades adicionais que não se aplicam exclusivamente a dispositivos de ponto de extremidade de áudio. Para obter mais informações sobre essas propriedades adicionais, consulte [Propriedades do dispositivo](device-properties.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)
</dt> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

