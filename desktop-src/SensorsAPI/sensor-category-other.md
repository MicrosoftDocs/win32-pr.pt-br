---
description: A categoria de SENSOR de \_ \_ outra categoria contém sensores que dão suporte à classe personalizada no driver de classe HID.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010426"
---
# <a name="sensor_category_other"></a>Categoria de SENSOR \_ \_ outra

A categoria de SENSOR de \_ \_ outra categoria contém sensores que dão suporte à classe personalizada no driver de classe HID.

<dl> <dt>

<span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**tipo de SENSOR \_ \_ personalizado**
</dt> <dd> <dl> <dt>

{E83AF229-8640-4D18-A213-E22675EBB2C3}
</dt> <dt>



Sensor personalizado que dá suporte à classe personalizada no driver de classe HID.


</dt> </dl> </dd> </dl>

**Campos de dados definidos pela plataforma**

As chaves de propriedade definidas pela plataforma para essa categoria se baseiam no \_ GUID personalizado de tipo de dados do sensor \_ \_ \_ :

{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}

Essa categoria inclui os seguintes campos de dados definidos pela plataforma.



| Nome do campo de dados e PID                                                                                                                                                                                                                                                                                    | Descrição                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <dt>**Sensor \_ \_ \_ \_ Uso personalizado de tipo de dados**</dt> <dt> (PID = 5)</dt> </dl>                          | **\_UI4 VT**<br/> Um uso de HID que pode ser usado para distinguir vários sensores personalizados.<br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <dt>**Sensor \_ \_ \_ \_ \_ Matriz booleana personalizada de tipo de dados**</dt> <dt> (PID = 6)</dt> </dl> | **\_UI4 VT**<br/> Uma matriz de valores Boolianos para um determinado sensor personalizado.<br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <dt>**Sensor \_ \_ \_ \_ Value1 personalizado de tipo de dados**</dt> <dt> (PID = 7)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Um dos seis valores disponíveis para um determinado sensor personalizado.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <dt>**Sensor \_ \_ \_ \_ VALUE2 personalizado de tipo de dados**</dt> <dt> (PID = 8)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Um dos seis valores disponíveis para um determinado sensor personalizado.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ Custom \_ VALUE3**</dt> <dt> (PID = 9)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Um dos seis valores disponíveis para um determinado sensor personalizado.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ Custom \_ VALUE4**</dt> <dt> (PID = 10)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Um dos seis valores disponíveis para um determinado sensor personalizado.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ Custom \_ VALUE5**</dt> <dt> (PID = 11)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Um dos seis valores disponíveis para um determinado sensor personalizado.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ Custom \_ VALUE6**</dt> <dt> (PID = 12)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Um dos seis valores disponíveis para um determinado sensor personalizado.<br/>       |



## <a name="remarks"></a>Comentários

Um sensor que dá suporte à classe genérica no driver de classe HID será mapeado para uma das outras categorias definidas (biométrica, elétrica, ambiental e assim por diante).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Sensores. h</dt> </dl> |



 

 




