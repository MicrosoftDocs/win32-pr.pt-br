---
description: Os dispositivos portáteis do Windows definem os seguintes valores de evento.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Constantes de evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EVENT_DEVICE_CAPABILITIES_UPDATED
- WPD_EVENT_DEVICE_REMOVED
- WPD_EVENT_DEVICE_RESET
- WPD_EVENT_OBJECT_ADDED
- WPD_EVENT_OBJECT_REMOVED
- WPD_EVENT_OBJECT_TRANSFER_REQUESTED
- WPD_EVENT_OBJECT_UPDATED
- WPD_EVENT_SERVICE_METHOD_COMPLETE
- WPD_EVENT_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e60c44cda2585655a86ca1cdb4653ad002a0225d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781409"
---
# <a name="event-constants-portabledeviceh"></a>Constantes de evento (PortableDevice. h)

Os dispositivos portáteis do Windows definem os seguintes valores de evento.



| Constante                                                                                                                                                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <dt>**\_recursos do dispositivo de eventos WPD \_ \_ \_ atualizados**</dt> </dl> | Esse evento indica que os recursos do dispositivo foram alterados. Os clientes devem repetir o dispositivo se tiverem tomada alguma decisão com base nos recursos do dispositivo.<br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <dt>**\_dispositivo de eventos WPD \_ \_ removido**</dt> </dl>                                         | Esse evento é enviado quando um driver de um dispositivo está sendo descarregado. Normalmente, isso é resultado do dispositivo que está sendo desconectado.<br/> Os clientes devem liberar a interface **IPortableDevice** e todas as interfaces [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) especificadas na **\_ \_ \_ \_ \_ ID do dispositivo PnP do parâmetro de evento WPD**.<br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <dt>**redefinição de \_ dispositivo de evento WPD \_ \_**</dt> </dl>                                               | Esse evento indica que o dispositivo está prestes a ser redefinido e que todos os clientes conectados devem fechar suas conexões com o dispositivo.<br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <dt>**\_objeto de evento WPD \_ \_ adicionado**</dt> </dl>                                               | Esse evento indica que um novo objeto está disponível no dispositivo.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <dt>**\_objeto de evento WPD \_ \_ removido**</dt> </dl>                                         | Esse evento é enviado depois que um objeto existente anteriormente é removido do dispositivo.<br/> O objeto pode ser um objeto de conteúdo, por exemplo, um arquivo de imagem foi excluído; ou pode ser um objeto funcional, por exemplo, um novo dispositivo de armazenamento foi desconectado do dispositivo.<br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <dt>**\_transferência de objeto de evento WPD \_ \_ \_ solicitada**</dt> </dl>       | Esse evento é enviado para solicitar que um aplicativo Transfira um objeto específico do dispositivo.<br/> O objeto é geralmente um objeto de conteúdo, por exemplo, um arquivo de imagem.<br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <dt>**\_objeto de evento WPD \_ \_ atualizado**</dt> </dl>                                         | Esse evento é enviado após a atualização de um objeto e qualquer cliente conectado deve atualizar sua exibição desse objeto.<br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <dt>**\_método de serviço de evento WPD \_ \_ \_ concluído**</dt> </dl>             | Esse evento é enviado quando um driver conclui a invocação de um método de serviço. Esse evento deve ser enviado mesmo quando o método falhar. Esse é um evento de DDI de WPD interno e não estará disponível para nenhum aplicativo por meio de [**IPortableDevice:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) ou [**IPortableDeviceService:: Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).<br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <dt>**\_formato de \_ armazenamento de eventos WPD \_**</dt> </dl>                                         | Esse evento indica o progresso de uma operação de formatação em um objeto de armazenamento.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes](constants.md)
</dt> </dl>

 

 




