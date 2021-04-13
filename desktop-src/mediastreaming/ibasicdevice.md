---
title: Interface IBasicDevice
description: Encapsula os métodos e eventos necessários para modelar um dispositivo DLNA.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- API de streaming de mídia da interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, descrita
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104366904"
---
# <a name="ibasicdevice-interface"></a>Interface IBasicDevice

Encapsula os métodos e eventos necessários para modelar um dispositivo DLNA.

## <a name="members"></a>Membros

A interface **IBasicDevice** herda de [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable). **IBasicDevice** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IBasicDevice** tem esses métodos.



| Método                                                                                 | Descrição                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Adicionar \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md)       | Registra um manipulador de eventos para o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .<br/>                |
| [**CanWakeDevices**](ibasicdevice-canwakedevices.md)                                  | Recupera um valor que indica se o dispositivo pode ser ativado.<br/>                                                            |
| [**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))                              | Retorna um valor de enumeração que indica se o dispositivo está atualmente online, off-line ou em suspensão, mas Despertável.<br/> |
| [**Descrição**](ibasicdevice-description.md)                                        | Recupera uma descrição do dispositivo.<br/>                                                                              |
| [**DiscoveredOnCurrentNetwork**](ibasicdevice-discoveredoncurrentnetwork.md)          | Recupera um valor que indica se o dispositivo está na rede atual.<br/>                                           |
| [**FriendlyName**](ibasicdevice-friendlyname.md)                                      | Recupera o nome amigável do dispositivo.<br/>                                                                               |
| [**Ícones**](ibasicdevice-icons.md)                                                    | Retorna um vetor de interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .<br/>                                                  |
| [**IpAddresses**](ibasicdevice-ipaddresses.md)                                        | Retorna um vetor de endereços IP.<br/>                                                                                   |
| [**ManufacturerName**](ibasicdevice-manufacturername.md)                              | Recupera o nome do fabricante do dispositivo.<br/>                                                                           |
| [**ManufacturerUrl**](ibasicdevice-manufacturerurl.md)                                | Recupera a URL do fabricante do dispositivo.<br/>                                                                            |
| [**ModelName**](ibasicdevice-modelname.md)                                            | Recupera o nome do modelo do dispositivo.<br/>                                                                                  |
| [**ModelNumber**](ibasicdevice-modelnumber.md)                                        | Recupera o número do modelo do dispositivo.<br/>                                                                                |
| [**ModelUrl**](ibasicdevice-modelurl.md)                                              | Recupera a URL do modelo do dispositivo.<br/>                                                                                   |
| [**PhysicalAddresses**](ibasicdevice-physicaladdresses.md)                            | Retorna um vetor de endereços físicos.<br/>                                                                             |
| [**PresentationUrl**](ibasicdevice-presentationurl.md)                                | Recupera a URL de apresentação do dispositivo.<br/>                                                                            |
| [**RemoteStreamingUrls**](ibasicdevice-remotestreamingurls.md)                        | Retorna um vetor de URLs de streaming remota.<br/>                                                                          |
| [**Remover \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) | Cancela o registro de um manipulador de eventos para o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .<br/>              |
| [**SerialNumber**](ibasicdevice-serialnumber.md)                                      | Recupera o número de série do dispositivo.<br/>                                                                               |
| [**Escreva**](ibasicdevice-type.md)                                                      | Recupera um valor de enumeração que indica o tipo de dispositivo do dispositivo DLNA.<br/>                                       |
| [**UniqueDeviceName**](ibasicdevice-uniquedevicename.md)                              | Recupera o nome do dispositivo exclusivo do dispositivo (UDN).<br/>                                                                    |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

