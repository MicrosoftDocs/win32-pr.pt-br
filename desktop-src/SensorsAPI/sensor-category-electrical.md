---
description: A \_ categoria elétrica categoria de sensor \_ contém sensores que fornecem informações sobre sistemas elétricos.
ms.assetid: c4efa821-fb9f-4606-898a-5be103581f39
title: SENSOR_CATEGORY_ELECTRICAL (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3487b779cfefc78a541fcc72d1f2c5c5e7c0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751072"
---
# <a name="sensor_category_electrical"></a>Categoria do SENSOR \_ \_ elétrica

A \_ categoria elétrica categoria de sensor \_ contém sensores que fornecem informações sobre sistemas elétricos.

**Tipos de sensor definidos pela plataforma**

Essa categoria inclui os seguintes tipos de sensor definidos pela plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                              | Descrição                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| <span id="SENSOR_TYPE_CAPACITANCE"></span><span id="sensor_type_capacitance"></span><dl> <dt>**Sensor \_ \_Capacite de tipo**</dt> <dt>{CA2FFB1C-2317-49C0-A0B4-B63CE63461A0}</dt> </dl>                 | Sensores de capacitância.<br/>         |
| <span id="SENSOR_TYPE_CURRENT"></span><span id="sensor_type_current"></span><dl> <dt>**Sensor \_ Digite \_**</dt> o <dt>{5ADC9FCE-15A0-4bbe-A1AD-2D38A9AE831C}</dt> atual </dl>                             | Sensores de corrente elétrica.<br/>  |
| <span id="SENSOR_TYPE_ELECTRICAL_POWER"></span><span id="sensor_type_electrical_power"></span><dl> <dt>**Sensor \_ Digite \_ a \_ energia elétrica**</dt> <dt>{212F10F5-14AB-4376-9A43-A7794098C2FE}</dt> </dl> | Sensores de energia elétrica.<br/>    |
| <span id="SENSOR_TYPE_FREQUENCY"></span><span id="sensor_type_frequency"></span><dl> <dt>**Sensor \_ \_Frequência de tipo**</dt> <dt>{8CD2CBB6-73E6-4640-A709-72AE8FB60D7F}</dt> </dl>                       | Sensor de frequência elétrica.<br/> |
| <span id="SENSOR_TYPE_INDUCTANCE"></span><span id="sensor_type_inductance"></span><dl> <dt>**Sensor \_ Digite \_ INDUCTANCE**</dt> <dt>{DC1D933F-C435-4C7D-A2FE-607192A524D3}</dt> </dl>                    | Sensores de Inductance.<br/>          |
| <span id="SENSOR_TYPE_POTENTIOMETER"></span><span id="sensor_type_potentiometer"></span><dl> <dt>**Sensor \_ Digite \_ POTENTIOMETER**</dt> <dt>{2B3681A9-CADC-45AA-A6FF-54957C8BB440}</dt> </dl>           | Potentiometers.<br/>              |
| <span id="SENSOR_TYPE_RESISTANCE"></span><span id="sensor_type_resistance"></span><dl> <dt>**Sensor \_ \_Resistência de tipo**</dt> <dt>{9993D2C8-C157-4A52-A7B5-195C76037231}</dt> </dl>                    | Sensores de resistência.<br/>          |
| <span id="SENSOR_TYPE_VOLTAGE"></span><span id="sensor_type_voltage"></span><dl> <dt>**Sensor \_ \_Tensão de tipo**</dt> <dt>{C5484637-4FB7-4953-98B8-A56D8AA1FB1E}</dt> </dl>                             | Sensores de tensão.<br/>             |



**Campos de dados definidos pela plataforma**

As chaves de propriedade definidas pela plataforma para esta categoria são baseadas no tipo de dados do SENSOR \_ \_ \_ \_ GUID elétrico:

{BBB246D1-E242-4780-A2D3-CDED84F35842}

Essa categoria inclui os seguintes campos de dados definidos pela plataforma.



| Nome do campo de dados e PID                                                                                                                                                                                                                                                                                                         | Descrição                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CAPACITANCE_FARAD"></span><span id="sensor_data_type_capacitance_farad"></span><dl> <dt>**Sensor \_ \_ \_ \_ Farad de capacitância de tipo de dados**</dt> <dt> (PID = 4)</dt> </dl>                                | **R8 de VT \_**<br/> Capacitância em farads.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_CURRENT_AMPS"></span><span id="sensor_data_type_current_amps"></span><dl> <dt>**Sensor \_ Tipos de dados \_ \_ atuais \_ amps**</dt> <dt>(PID = 3)</dt> </dl>                                                | **R8 de VT \_**<br/> Atual em amperes.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_FREQUENCY_HERTZ"></span><span id="sensor_data_type_electrical_frequency_hertz"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ \_ frequência elétrica \_ Hertz**</dt> <dt>(PID = 9)</dt> </dl>     | **R8 de VT \_**<br/> Frequência elétrica em Hertz.<br/>                               |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_PERCENT_OF_RANGE"></span><span id="sensor_data_type_electrical_percent_of_range"></span><dl> <dt>**Sensor \_ \_ \_ \_ Percentual elétrico do tipo \_ de dados do \_ intervalo**</dt> <dt>(PID = 8)</dt> </dl> | **R8 de VT \_**<br/> Potentiometer lendo como uma porcentagem de seu intervalo possível.<br/> |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_POWER_WATTS"></span><span id="sensor_data_type_electrical_power_watts"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ energia elétrica- \_ \_ watts**</dt> <dt> (PID = 7)</dt> </dl>                | **R8 de VT \_**<br/> Potência elétrica em watts.<br/>                                   |
| <span id="SENSOR_DATA_TYPE_INDUCTANCE_HENRY"></span><span id="sensor_data_type_inductance_henry"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ INDUCTANCE \_ Henry**</dt> <dt>(PID = 6)</dt> </dl>                                    | **R8 de VT \_**<br/> Inductance em Henries.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_RESISTANCE_OHMS"></span><span id="sensor_data_type_resistance_ohms"></span><dl> <dt>**Sensor \_ Resistência de tipo de dados \_ \_ \_ ohms**</dt> <dt>(PID = 5)</dt> </dl>                                       | **R8 de VT \_**<br/> Resistência em ohms.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_VOLTAGE_VOLTS"></span><span id="sensor_data_type_voltage_volts"></span><dl> <dt>**Sensor \_ \_ \_ \_ Volts de tensão de tipo de dados**</dt> <dt>(PID = 2)</dt> </dl>                                             | **R8 de VT \_**<br/> Potencial elétrico em volts.<br/>                               |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Sensores. h</dt> </dl> |



 

 




