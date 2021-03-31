---
description: A \_ categoria biométrica da categoria do sensor \_ contém sensores que fornecem informações sobre seres de vida.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71660c7bc94037c21502c91e017a8eba369766a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090169"
---
# <a name="sensor_category_biometric"></a>\_biometria da categoria de sensor \_

A \_ categoria biométrica da categoria do sensor \_ contém sensores que fornecem informações sobre seres de vida.

**Tipos de sensor definidos pela plataforma**

Essa categoria inclui os seguintes tipos de sensor definidos pela plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                           | Descrição                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <dt>**Sensor \_ TIPO \_ de \_ presença humana**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt> </dl>    | Sensores que detectam a presença humana.<br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <dt>**Sensor \_ Digite \_ a \_ proximidade humana**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt> </dl> | Sensores que detectam proximidade humana.<br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <dt>**Sensor \_ Digite \_ Touch**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt> </dl>                                | Sensores de toque.<br/>                       |



**Campos de dados definidos pela plataforma**

As chaves de propriedade definidas pela plataforma para esta categoria são baseadas no tipo de dados do SENSOR \_ \_ \_ GUID biométrico \_ :

{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}

Essa categoria inclui os seguintes campos de dados definidos pela plataforma.



| Nome do campo de dados e PID                                                                                                                                                                                                                                                                                         | Descrição                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <dt>**Sensor \_ \_ \_ \_ Presença humana de tipo de dados**</dt> <dt>(PID = 2)</dt> </dl>                          | **BOOL do VT \_**<br/> **Verdadeiro** quando um humano estiver usando o computador.<br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <dt>**Sensor \_ \_ \_ \_ \_ Medidores de proximidade humana do tipo de dados**</dt> <dt>(PID = 3)</dt> </dl> | **VT \_ R4**<br/> Distância entre um humano e o computador, em metros.<br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <dt>**Sensor \_ \_Estado de \_ toque \_ do tipo de dados**</dt> <dt>(PID = 4)</dt> </dl>                                   | **BOOL do VT \_**<br/> **Verdadeiro** quando o sensor de toque está sendo tocado; caso contrário, **false**.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Sensores. h</dt> </dl> |



 

 




