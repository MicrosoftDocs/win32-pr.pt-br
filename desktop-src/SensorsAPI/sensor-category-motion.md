---
description: A categoria de movimento de categoria de SENSOR \_ \_ contém sensores que fornecem informações relacionadas ao movimento físico.
ms.assetid: be025c86-46b5-4f50-a3af-0408bb3c9b5b
title: SENSOR_CATEGORY_MOTION (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1edcb1b5f0a6d02c481774d18ee111ad4ca5e5cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756372"
---
# <a name="sensor_category_motion"></a>\_movimento de categoria do sensor \_

A categoria de movimento de categoria de SENSOR \_ \_ contém sensores que fornecem informações relacionadas ao movimento físico. Os acelerômetros medem a aceleração do sensor, incluindo a aceleração de Gravitational. Detectores de movimento, como a detecção de movimento humano em um sistema de segurança, faz sentido mover objetos. Alterações de sensor de Gyrometers na velocidade angular. Velocidade de medida do velocímetros.

**Tipos de sensor definidos pela plataforma**

Essa categoria inclui os seguintes tipos de sensor definidos pela plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                              | Description                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="SENSOR_TYPE_ACCELEROMETER_1D"></span><span id="sensor_type_accelerometer_1d"></span><dl> <dt>**Sensor \_ Digite \_ acelerômetro \_ 1D**</dt> <dt>{C04D2387-7340-4CC2-991E-3B18CB8EF2F4}</dt> </dl> | Acelerômetros de um eixo.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_2D"></span><span id="sensor_type_accelerometer_2d"></span><dl> <dt>**Sensor \_ Digite o \_ acelerômetro \_ 2D**</dt> <dt>{B2C517A8-F6B5-4BA6-A423-5DF560B4CC07}</dt> </dl> | Acelerômetros de dois eixos.<br/>                                  |
| <span id="SENSOR_TYPE_ACCELEROMETER_3D"></span><span id="sensor_type_accelerometer_3d"></span><dl> <dt>**Sensor \_ TIPO \_ acelerômetro \_ 3D**</dt> <dt>{C2FB0F5F-E2D2-4C78-BCD0-352A9582819D}</dt> </dl> | Acelerômetros de três eixos.<br/>                                |
| <span id="SENSOR_TYPE_GYROMETER_1D"></span><span id="sensor_type_gyrometer_1d"></span><dl> <dt>**Sensor \_ Digite \_ girômetro \_ 1D**</dt> <dt>{FA088734-F552-4584-8324-EDFAF649652C}</dt> </dl>             | Gyrometers de um eixo.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_2D"></span><span id="sensor_type_gyrometer_2d"></span><dl> <dt>**Sensor \_ Digite \_ girômetro \_ 2D**</dt> <dt>{31EF4F83-919B-48BF-8DE0-5D7A9D240556}</dt> </dl>             | Gyrometers de dois eixos.<br/>                                      |
| <span id="SENSOR_TYPE_GYROMETER_3D"></span><span id="sensor_type_gyrometer_3d"></span><dl> <dt>**Sensor \_ Digite \_ girômetro \_ 3D**</dt> <dt>{09485F5A-759E-42C2-BD4B-A349B75C8643}</dt> </dl>             | Gyrometers de três eixos.<br/>                                    |
| <span id="SENSOR_TYPE_MOTION_DETECTOR"></span><span id="sensor_type_motion_detector"></span><dl> <dt>**Sensor \_ \_ \_ Detector de movimento de tipo**</dt> <dt>{5C7C1A12-30A5-43B9-A4B2-CF09EC5B7BE8}</dt> </dl>    | Detectores de movimento, como os usados em sistemas de segurança.<br/> |
| <span id="SENSOR_TYPE_SPEEDOMETER"></span><span id="sensor_type_speedometer"></span><dl> <dt>**Sensor \_ Digite \_ velocímetro**</dt> <dt>{6BD73C1F-0BB4-4310-81B2-DFC18A52BF94}</dt> </dl>                 | Sensores de taxa de movimento.<br/>                                   |



**Campos de dados definidos pela plataforma**

As chaves de propriedade definidas pela plataforma para essa categoria baseiam-se no GUID de movimento do tipo de dados do SENSOR \_ \_ \_ \_ :

{3F8A69A2-07C5-4E48-A965-CD797AAB56D5}

Essa categoria inclui os seguintes campos de dados definidos pela plataforma.



| Nome do campo de dados e PID                                                                                                                                                                                                                                                                                                                                                                               | Description                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ACCELERATION_X_G"></span><span id="sensor_data_type_acceleration_x_g"></span><dl> <dt>**Sensor \_ \_Aceleração de tipo de dados \_ \_ X \_ G**</dt> <dt>(PID = 2)</dt> </dl>                                                                                                         | **R8 de VT \_**<br/> Aceleração do eixo X, em *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Y_G"></span><span id="sensor_data_type_acceleration_y_g"></span><dl> <dt>**Sensor \_ \_ \_ Aceleração de \_ \_ tipo de dados Y**</dt> <dt>(PID = 3)</dt> </dl>                                                                                                         | **R8 de VT \_**<br/> Aceleração do eixo Y, em *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ACCELERATION_Z_G"></span><span id="sensor_data_type_acceleration_z_g"></span><dl> <dt>**Sensor \_ \_Aceleração de tipo de dados \_ \_ Z \_ G**</dt> <dt>(PID = 4)</dt> </dl>                                                                                                         | **R8 de VT \_**<br/> Aceleração do eixo Z, em *g*.<br/>                                 |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_X_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_x_degrees_per_second_squared"></span><dl> <dt>**Sensor \_ \_Aceleração angular de tipo de dados \_ \_ \_ X \_ graus \_ por \_ segundo ao \_ quadrado**</dt> <dt>(PID = 5)</dt> </dl>  | **R8 de VT \_**<br/> Aceleração do eixo x do Gyrometric, em graus por segundo ao quadrado.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Y_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_y_degrees_per_second_squared"></span><dl> <dt>**Sensor \_ \_Tipo de \_ dados \_ aceleração angular \_ Y \_ graus \_ por \_ segundo ao \_ quadrado**</dt> <dt> (PID = 6)</dt> </dl> | **R8 de VT \_**<br/> Aceleração do eixo y Gyrometric, em graus por segundo ao quadrado.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_ACCELERATION_Z_DEGREES_PER_SECOND_SQUARED"></span><span id="sensor_data_type_angular_acceleration_z_degrees_per_second_squared"></span><dl> <dt>**Sensor \_ \_Aceleração angular de tipo de dados \_ \_ \_ Z \_ graus \_ por \_ segundo ao \_ quadrado**</dt> <dt> (PID = 7)</dt> </dl> | **R8 de VT \_**<br/> Aceleração do eixo z do Gyrometric, em graus por segundo ao quadrado.<br/> |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_X_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_x_degrees_per_second"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ \_ velocidade angular \_ X \_ graus \_ por \_ segundo**</dt> <dt> (PID = 10)</dt> </dl>                                      | **R8 de VT \_**<br/> Velocidade do eixo x do Gyrometric, em graus por segundo.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Y_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_y_degrees_per_second"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ \_ velocidade angular \_ Y \_ graus \_ por \_ segundo**</dt> <dt> (PID = 11)</dt> </dl>                                      | **R8 de VT \_**<br/> Velocidade do eixo y do Gyrometric, em graus por segundo.<br/>             |
| <span id="SENSOR_DATA_TYPE_ANGULAR_VELOCITY_Z_DEGREES_PER_SECOND"></span><span id="sensor_data_type_angular_velocity_z_degrees_per_second"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ \_ velocidade angular \_ Z \_ graus \_ por \_ segundo**</dt> <dt> (PID = 12)</dt> </dl>                                      | **R8 de VT \_**<br/> Velocidade do eixo z do Gyrometric, em graus por segundo.<br/>             |
| <span id="SENSOR_DATA_TYPE_MOTION_STATE"></span><span id="sensor_data_type_motion_state"></span><dl> <dt>**Sensor \_ \_Estado do \_ movimento \_ do tipo de dados**</dt> <dt>(PID = 9)</dt> </dl>                                                                                                                      | **BOOL do VT \_**<br/> **True** se o movimento for detectado; caso contrário, **false**.<br/>        |
| <span id="SENSOR_DATA_TYPE_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_speed_meters_per_second"></span><dl> <dt>**Sensor \_ \_Medidores de velocidade de tipo de dados \_ \_ \_ por \_ segundo**</dt> <dt> (PID = 8)</dt> </dl>                                                                                  | **R8 de VT \_**<br/> Velocidade em metros por segundo.<br/>                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Sensores. h</dt> </dl> |



 

 




