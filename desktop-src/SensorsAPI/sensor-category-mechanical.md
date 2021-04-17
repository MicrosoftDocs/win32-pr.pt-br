---
description: A \_ categoria mecânica da categoria de sensor \_ contém sensores que fornecem informações relacionadas a dispositivos e medições mecânicos.
ms.assetid: d1243303-d26c-45ce-b97b-d554daeeb462
title: SENSOR_CATEGORY_MECHANICAL (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2446559820141b65a70bc75d25680da79563388c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754496"
---
# <a name="sensor_category_mechanical"></a>\_mecânica da categoria de sensor \_

A \_ categoria mecânica da categoria de sensor \_ contém sensores que fornecem informações relacionadas a dispositivos e medições mecânicos.

**Tipos de sensor definidos pela plataforma**

Essa categoria inclui os seguintes tipos de sensor definidos pela plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                                           | Description                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------|
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH"></span><span id="sensor_type_boolean_switch"></span><dl> <dt>**Sensor \_ Digite \_ a \_ opção booliana**</dt> <dt>{9C7E371F-1041-460B-8D5C-71E4752E350C}</dt> </dl>                    | Opções de dois Estados (desativado ou ativado).<br/>          |
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH_ARRAY"></span><span id="sensor_type_boolean_switch_array"></span><dl> <dt>**Sensor \_ Digite \_ a \_ \_ matriz de opção booliana**</dt> <dt>{545C8BA5-B143-4545-868F-CA7FD986B4F6}</dt> </dl> | Matriz de opções de dois Estados (desativado ou ativado).<br/> |
| <span id="SENSOR_TYPE_FORCE"></span><span id="sensor_type_force"></span><dl> <dt>**Sensor \_ Digite \_ Force**</dt> <dt>{C2AB2B02-1A1C-4778-A81B-954A1788CC75}</dt> </dl>                                                | Forçar sensores.<br/>                           |
| <span id="SENSOR_TYPE_MULTIVALUE_SWITCH"></span><span id="sensor_type_multivalue_switch"></span><dl> <dt>**Sensor \_ \_ \_ Opção de tipo**</dt> de vários valores <dt>{B3EE4D76-37A4-4402-B25E-99C60A775FA1}</dt> </dl>           | Opções de várias posições.<br/>              |
| <span id="SENSOR_TYPE_PRESSURE"></span><span id="sensor_type_pressure"></span><dl> <dt>**Sensor \_ \_Pressão de tipo**</dt> <dt>{26D31F34-6352-41CF-B793-EA0713D53D77}</dt> </dl>                                       | Sensores de pressão.<br/>                        |
| <span id="SENSOR_TYPE_SCALE"></span><span id="sensor_type_scale"></span><dl> <dt>**Sensor \_ \_Escala de tipos**</dt> <dt>{C06DD92C-7FEB-438E-9BF6-82207FFF5BB8}</dt> </dl>                                                | Sensores de peso.<br/>                          |
| <span id="SENSOR_TYPE_STRAIN"></span><span id="sensor_type_strain"></span><dl> <dt>**Sensor \_ \_Carga de tipo**</dt> <dt>{C6D1EC0E-6803-4361-AD3D-85BCC58C6D29}</dt> </dl>                                             | Sensores de tensão.<br/>                          |



**Campos de dados definidos pela plataforma**

As chaves de propriedade definidas pela plataforma para essa categoria baseiam-se no \_ \_ GUID mecânico do GUID tipo de dados do sensor \_ \_ \_ :

{38564A7C-F2F2-49BB-9B2B-BA60F66A58DF}

Essa categoria inclui os seguintes campos de dados definidos pela plataforma.



| Nome do campo de dados e PID                                                                                                                                                                                                                                                                                                         | Description                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ABSOLUTE_PRESSURE_PASCAL"></span><span id="sensor_data_type_absolute_pressure_pascal"></span><dl> <dt>**Sensor \_ Tipo de dados de \_ \_ \_ pressão absoluta \_ Pascal**</dt> <dt> (PID = 5)</dt> </dl>          | **R8 de VT \_**<br/> Pressão absoluta, em pascals.<br/>                    |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_ARRAY_STATES"></span><span id="sensor_data_type_boolean_switch_array_states"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ switch booliano \_ \_ \_ Estados da matriz**</dt> <dt>(PID = 10)</dt> </dl> | **\_UI4 VT**<br/> Campos de estado para uma matriz de opções boolianas.<br/>   |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_STATE"></span><span id="sensor_data_type_boolean_switch_state"></span><dl> <dt>**Sensor \_ \_Estado da \_ \_ opção \_ booliana do tipo de dados**</dt> <dt>(PID = 2)</dt> </dl>                       | **BOOL do VT \_**<br/> Campo de estado para \_ a \_ opção booliana do tipo de sensor \_ .<br/>  |
| <span id="SENSOR_DATA_TYPE_FORCE_NEWTONS"></span><span id="sensor_data_type_force_newtons"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ Force \_ Newtons**</dt> <dt> (PID = 4)</dt> </dl>                                            | **R8 de VT \_**<br/> Force, em Newtons.<br/>                                |
| <span id="SENSOR_DATA_TYPE_GAUGE_PRESSURE_PASCAL"></span><span id="sensor_data_type_gauge_pressure_pascal"></span><dl> <dt>**Sensor \_ Pressão do medidor de tipo de dados \_ \_ \_ \_ Pascal**</dt> <dt> (PID = 6)</dt> </dl>                   | **R8 de VT \_**<br/> Pressão de medidor relativo, em pascals.<br/>              |
| <span id="SENSOR_DATA_TYPE_MULTIVALUE_SWITCH_STATE"></span><span id="sensor_data_type_multivalue_switch_state"></span><dl> <dt>**Sensor \_ \_Estado da \_ \_ opção de \_ múltiplos tipos de dados**</dt> <dt> (PID = 3)</dt> </dl>             | **R8 de VT \_**<br/> Campo de estado para o tipo de SENSOR chave de vários \_ \_ valores \_ .<br/> |
| <span id="SENSOR_DATA_TYPE_STRAIN"></span><span id="sensor_data_type_strain"></span><dl> <dt>**Sensor \_ \_ \_ Tensão de tipo de dados**</dt> <dt> (PID = 7)</dt> </dl>                                                                  | **R8 de VT \_**<br/> Limitada.<br/>                                           |
| <span id="SENSOR_DATA_TYPE_WEIGHT_KILOGRAMS"></span><span id="sensor_data_type_weight_kilograms"></span><dl> <dt>**Sensor \_ \_ \_ \_ Quilogramas de peso do tipo de dados**</dt> <dt> (PID = 8)</dt> </dl>                                   | **R8 de VT \_**<br/> Peso, em quilogramas.<br/>                             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Sensores. h</dt> </dl> |



 

 




