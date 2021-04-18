---
description: O sensor do Windows e a plataforma de localização definem constantes para eventos de driver. O sensor manfuactureres também pode definir suas próprias constantes.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Constantes de evento (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753091"
---
# <a name="event-constants-sensorsh"></a>Constantes de evento (sensores. h)

O sensor do Windows e a plataforma de localização definem constantes para eventos de driver. O sensor manfuactureres também pode definir suas próprias constantes.

**Tipos de evento de sensor**

A plataforma define os seguintes identificadores de tipo de evento de sensor.



| Tipo de evento de sensor                                                                                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <dt>**Sensor \_ \_ \_ Agitar o ACELERÔMETRO de evento**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt> </dl> | Indica que o dispositivo foi Shaken.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <dt>**Sensor \_ Dados de evento \_ \_ atualizados**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt> </dl>                      | Indica que novos dados estão disponíveis.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <dt>**Sensor \_ Propriedade de evento \_ \_ alterada**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt> </dl>          | Indica que um valor de propriedade foi alterado. Verifique a interface [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) , passada pelo parâmetro *PEventData* para [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), para determinar qual propriedade foi alterada e seu novo valor.<br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <dt>**Sensor \_ Estado do evento \_ \_ alterado**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt> </dl>                   | Indica uma alteração do estado operacional, por exemplo, do estado do SENSOR \_ \_ inicializando para o estado do sensor \_ \_ pronto.<br/>                                                                                                                                                                                            |



**Evento de sensor PROPERTYKEYs**

As chaves de propriedade definidas pela plataforma para eventos são baseadas no seguinte GUID:

{64346E30-8728-4B34-BDF6-4F52442C5C28}

A plataforma de sensor define os seguintes **PROPERTYKEY** s que identificam os parâmetros de evento do sensor.



| O evento de sensor PROPERTYKEY e PID                                                                                                                                                                                                                                                      | Descrição                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <dt>**Sensor \_ \_ID do \_ evento \_ de parâmetro de evento**</dt> <dt>(PID = 2)</dt> </dl> | Indica que o valor de **GUID** em [IPORTABLEDEVICEVALUES](/previous-versions//ms740012(v=vs.85)) é uma ID de tipo de evento, como dados de evento de sensor \_ \_ \_ atualizados.<br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <dt>**Sensor \_ \_ \_ Estado do parâmetro de evento**</dt> <dt>(PID = 3)</dt> </dl>           | Indica que o valor inteiro sem sinal em **IPortableDeviceValues** é um estado de sensor, como \_ pronto para o estado do sensor \_ .<br/>                                                  |



**Erro de sensor PROPERTYKEYs**

As chaves de propriedade definidas pela plataforma para erros serão baseadas no seguinte GUID:

{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}

A plataforma do sensor reserva esse GUID para uso futuro.

<dl></dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Sensores. h</dt> </dl> |



 

