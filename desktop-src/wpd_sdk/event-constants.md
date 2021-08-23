---
description: Windows Dispositivos Portáteis define os seguintes valores de evento.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Constantes de evento (PortableDevice.h)
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
ms.openlocfilehash: 5ae8a0a519af32a68bd65241f847cadcaa3d623be932a747e21a3b86338d680d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704786"
---
# <a name="event-constants-portabledeviceh"></a>Constantes de evento (PortableDevice.h)

Windows Dispositivos Portáteis define os seguintes valores de evento.



| Constante                                                                                                                                                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <dt>**FUNCIONALIDADES DO DISPOSITIVO DE EVENTO WPD \_ \_ \_ \_ ATUALIZADAS**</dt> </dl> | Esse evento indica que os recursos do dispositivo foram alterados. Os clientes deverão requery o dispositivo se eles tomarem decisões com base nas funcionalidades do dispositivo.<br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <dt>**DISPOSITIVO DE EVENTO WPD \_ \_ \_ REMOVIDO**</dt> </dl>                                         | Esse evento é enviado quando um driver para um dispositivo está sendo descarregado. Normalmente, isso é resultado da desconectação do dispositivo.<br/> Os clientes devem liberar a interface **IPortableDevice** e as interfaces [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) especificadas em **WPD \_ EVENT PARAMETER \_ \_ PNP DEVICE \_ \_ ID**.<br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <dt>**WPD \_ EVENT \_ DEVICE \_ RESET**</dt> </dl>                                               | Esse evento indica que o dispositivo está prestes a ser redefinido e todos os clientes conectados devem fechar suas conexões com o dispositivo.<br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <dt>**OBJETO DE EVENTO WPD \_ \_ \_ ADICIONADO**</dt> </dl>                                               | Esse evento indica que um novo objeto está disponível no dispositivo.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <dt>**OBJETO DE EVENTO WPD \_ \_ \_ REMOVIDO**</dt> </dl>                                         | Esse evento é enviado depois que um objeto existente anteriormente foi removido do dispositivo.<br/> O objeto pode ser um objeto de conteúdo, por exemplo, um arquivo de imagem foi excluído; ou pode ser um objeto funcional, por exemplo, um novo dispositivo de armazenamento foi desconectado do dispositivo.<br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <dt>**TRANSFERÊNCIA DE OBJETO DE EVENTO WPD \_ \_ \_ \_ SOLICITADA**</dt> </dl>       | Esse evento é enviado para solicitar que um aplicativo transfira um objeto específico do dispositivo.<br/> O objeto geralmente é um objeto de conteúdo, por exemplo, um arquivo de imagem.<br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <dt>**OBJETO DE EVENTO WPD \_ \_ \_ ATUALIZADO**</dt> </dl>                                         | Esse evento é enviado depois que um objeto é atualizado e qualquer cliente conectado deve atualizar sua exibição desse objeto.<br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <dt>**MÉTODO DE SERVIÇO DE EVENTO WPD \_ \_ \_ \_ CONCLUÍDO**</dt> </dl>             | Esse evento é enviado quando um driver conclui a invocação de um método de serviço. Esse evento deve ser enviado mesmo quando o método falhar. Esse é um evento DDI WPD interno e não estará disponível para nenhum aplicativo por meio de [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) ou [**IPortableDeviceService::Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).<br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <dt>**FORMATO DE ARMAZENAMENTO DE EVENTOS WPD \_ \_ \_**</dt> </dl>                                         | Esse evento indica o progresso de uma operação de formato em um objeto de armazenamento.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes](constants.md)
</dt> </dl>

 

 




