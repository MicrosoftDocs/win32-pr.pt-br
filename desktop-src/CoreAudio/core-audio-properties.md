---
description: Essa referência de programação para o SDK de áudio principal inclui as propriedades a seguir.
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: Propriedades de áudio de núcleo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41528e66977f1f3b9282cf78ba76e4bae32c5bd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500760"
---
# <a name="core-audio-properties"></a>Propriedades de áudio de núcleo

Essa referência de programação para o SDK de áudio principal inclui as propriedades a seguir.

## <a name="audio-endpoint-properties"></a>Propriedades do ponto de extremidade de áudio

O SDK de áudio principal inclui várias propriedades de [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md). Para obter mais informações, consulte [Propriedades de ponto de extremidade de áudio](audio-endpoint-properties.md).

As propriedades a seguir são definidas em Mmdeviceapi. h no Windows Vista e versões posteriores.



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
| [**PKEY \_ AudioEndpoint \_ JackSubType**](pkey-audioendpoint-jacksubtype.md)<br/>                               | Contém um GUID de categoria de saída para um dispositivo de ponto de extremidade de áudio. <br/>                                                                                    |



 

## <a name="device-properties"></a>Propriedades do Dispositivo

O SDK de áudio principal inclui várias propriedades de dispositivo de [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md). Para obter mais informações, consulte [Propriedades do dispositivo](device-properties.md).

As propriedades a seguir são definidas em Functiondiscoverykeys \_ devpkey. h no Windows Vista e posterior.



| Propriedade                                                                         | Descrição                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | O nome amigável do adaptador de áudio ao qual o dispositivo de ponto de extremidade está anexado (por exemplo, "adaptador de áudio XYZ").                                                                               |
| [**PKEY \_ dispositivo \_ DeviceDesc**](pkey-device-devicedesc.md)                       | A descrição do dispositivo do ponto de extremidade do dispositivo (por exemplo, "alto-falantes").                                                                                                                          |
| [**PKEY do \_ dispositivo \_ amigável**](pkey-device-friendlyname.md)                   | O nome amigável do dispositivo de ponto de extremidade (por exemplo, "alto-falantes (adaptador de áudio XYZ)").                                                                                                           |
| **\_Contêinerid do dispositivo PKEY \_**                                                    | Armazena o identificador do contêiner do dispositivo PnP que implementa o ponto de extremidade de áudio. Para obter mais informações sobre essa propriedade, consulte "referência de propriedade de dispositivo" na documentação do Windows WDK. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação](programming-reference.md)
</dt> </dl>

 

 




