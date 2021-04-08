---
description: A \_ categoria ambiente de categoria do sensor \_ contém sensores que fornecem informações sobre o ambiente ou clima ao redor.
ms.assetid: 4a29d44b-8949-474d-a2bf-0c6e1d30b198
title: SENSOR_CATEGORY_ENVIRONMENTAL (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5c41d4c117dc27a3303210a485b2233cf24cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826962"
---
# <a name="sensor_category_environmental"></a>\_ambiente da categoria do sensor \_

A \_ categoria ambiente de categoria do sensor \_ contém sensores que fornecem informações sobre o ambiente ou clima ao redor.

**Tipos de sensor definidos pela plataforma**

Essa categoria inclui os seguintes tipos de sensor definidos pela plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                                                                                     | Descrição               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------|
| <span id="SENSOR_TYPE_ENVIRONMENTAL_ATMOSPHERIC_PRESSURE"></span><span id="sensor_type_environmental_atmospheric_pressure"></span><dl> <dt>**Sensor \_ DIGITAR \_ \_ \_ pressão de atmosférica ambiental**</dt> <dt>{0E903829-FF8A-4A93-97DF-3DCBDE402288}</dt> </dl> | Barometers.<br/>    |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_HUMIDITY"></span><span id="sensor_type_environmental_humidity"></span><dl> <dt>**Sensor \_ TIPO \_ de \_ umidade ambiental**</dt> <dt>{5C72BF67-BD7E-4257-990B-98A3BA3B400A}</dt> </dl>                                      | Hygrometers.<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_TEMPERATURE"></span><span id="sensor_type_environmental_temperature"></span><dl> <dt>**Sensor \_ DIGITAR \_ \_ temperatura ambiental**</dt> <dt>{04FD0EC4-D5DA-45FA-95A9-5DB38EE19306}</dt> </dl>                             | Termômetros<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_DIRECTION"></span><span id="sensor_type_environmental_wind_direction"></span><dl> <dt>**Sensor \_ Digite \_ a \_ \_ direção do vento ambiental**</dt> <dt>{9EF57A35-9306-434D-AF09-37FA5A9C00BD}</dt> </dl>                   | Clima Vanes.<br/> |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_SPEED"></span><span id="sensor_type_environmental_wind_speed"></span><dl> <dt>**Sensor \_ Digite \_ a \_ \_ velocidade do vento ambiental**</dt> <dt>{DD50607B-A45F-42CD-8EFD-EC61761C4226}</dt> </dl>                               | Anemometers.<br/>   |



**Campos de dados definidos pela plataforma**

As chaves de propriedade definidas pela plataforma para esta categoria são baseadas no tipo de dados do SENSOR \_ \_ \_ \_ GUID ambiental:

{8B0AA2F1-2D57-42EE-8CC0-4D27622B46C4}

Essa categoria inclui os seguintes campos de dados definidos pela plataforma.



| Nome do campo de dados e PID                                                                                                                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ATMOSPHERIC_PRESSURE_BAR"></span><span id="sensor_data_type_atmospheric_pressure_bar"></span><dl> <dt>**Sensor \_ \_Barra de \_ \_ pressão \_ do atmosférica de tipo de dados**</dt> <dt>(PID = 4)</dt> </dl>                                      | **VT \_ R4**<br/> Pressão atmosférica em atmosferas (barras).<br/>                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_TEMPERATURE_CELSIUS"></span><span id="sensor_data_type_temperature_celsius"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ temperatura \_ Celsius**</dt> <dt>(PID = 2)</dt> </dl>                                                      | **VT \_ R4**<br/> Temperatura em graus Celsius.<br/>                                                                                                                                                          |
| <span id="SENSOR_DATA_TYPE_RELATIVE_HUMIDITY_PERCENT"></span><span id="sensor_data_type_relative_humidity_percent"></span><dl> <dt>**Sensor \_ \_Porcentagem de \_ \_ umidade relativa \_ de tipo de dados**</dt> <dt> (PID = 3)</dt> </dl>                                  | **VT \_ R4**<br/> Umidade relativa como uma porcentagem.<br/>                                                                                                                                                       |
| <span id="SENSOR_DATA_TYPE_WIND_DIRECTION_DEGREES_ANTICLOCKWISE"></span><span id="sensor_data_type_wind_direction_degrees_anticlockwise"></span><dl> <dt>**Sensor \_ Direção do vento do tipo de dados \_ \_ \_ \_ graus \_ no sentido horário**</dt> <dt>(PID = 5)</dt> </dl> | **VT \_ R4**<br/> Direção do vento em relação ao norte magnético, em graus. O norte é representado como 0,0 (topo do eixo X), com valores aumentando em uma rotação no sentido anti-horário. O eixo Z aponta para cima. <br/> |
| <span id="SENSOR_DATA_TYPE_WIND_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_wind_speed_meters_per_second"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ \_ medidores de velocidade de vento \_ \_ por \_ segundo**</dt> <dt>(PID = 6)</dt> </dl>                        | **VT \_ R4**<br/> Velocidade do vento em metros por segundo.<br/>                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Sensores. h</dt> </dl> |



 

 




