---
description: A categoria SENSOR \_ CATEGORY BIOMETRIC contém sensores que fornecem informações sobre seres \_ vivos.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1551a82e359d2277c8b46f227d7a72660b1419b3ba3ddfcf58bdd4ac1de5425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889572"
---
# <a name="sensor_category_biometric"></a>BIOMETRIA \_ DA CATEGORIA \_ DO SENSOR

A categoria SENSOR \_ CATEGORY BIOMETRIC contém sensores que fornecem informações sobre seres \_ vivos.

**Tipos de sensor definidos pela plataforma**

Essa categoria inclui os seguintes tipos de sensor definidos pela plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                           | Descrição                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <dt>**SENSOR \_ DIGITE \_ PRESENÇA \_ HUMANA**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt> </dl>    | Sensores que detectam a presença humana.<br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <dt>**SENSOR \_ TIPO \_ \_ PROXIMIDADE HUMANA**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt> </dl> | Sensores que detectam proximidade humana.<br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <dt>**SENSOR \_ TYPE \_ TOUCH**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt> </dl>                                | Sensores de toque.<br/>                       |



**Campos de dados definidos pela plataforma**

As chaves de propriedade definidas pela plataforma para essa categoria são baseadas no \_ \_ GUID BIOMÉTRICO DO TIPO DE DADOS DO \_ \_ SENSOR:

{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}

Essa categoria inclui os campos de dados definidos pela plataforma a seguir.



| Nome do campo de dados e PID                                                                                                                                                                                                                                                                                         | Descrição                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <dt>**SENSOR \_ PRESENÇA \_ HUMANA DO TIPO DE \_ \_ DADOS**</dt> <dt>(PID = 2)</dt> </dl>                          | **BOOL da VT \_**<br/> **TRUE** quando um humano está usando o computador.<br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <dt>**SENSOR \_ MEDIDORES \_ DE PROXIMIDADE HUMANA DO TIPO DE \_ \_ \_ DADOS**</dt> <dt>(PID = 3)</dt> </dl> | **VT \_ R4**<br/> Distância entre um humano e o computador, em metros.<br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <dt>**SENSOR \_ ESTADO \_ DE TOQUE DO TIPO \_ \_ DE**</dt> <dt>DADOS (PID = 4)</dt> </dl>                                   | **BOOL da VT \_**<br/> **TRUE** quando o sensor de toque está sendo tocado; caso contrário, **FALSE.**<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Cabeçalho<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




