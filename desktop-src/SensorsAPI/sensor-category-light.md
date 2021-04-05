---
description: A \_ categoria leve categoria de sensor \_ contém sensores que fornecem informações sobre características de luz.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826961"
---
# <a name="sensor_category_light"></a>\_luz da categoria do sensor \_

A \_ categoria leve categoria de sensor \_ contém sensores que fornecem informações sobre características de luz.

**Tipos de sensor definidos pela plataforma**

Essa categoria inclui os seguintes tipos de sensor definidos pela plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                     | Descrição                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <dt>**Sensor \_ TIPO \_ de \_ luz ambiente**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt> </dl> | Sensores de luz ambiente.<br/> |



**Campos de dados definidos pela plataforma**

As chaves de propriedade definidas pela plataforma para esta categoria são baseadas no tipo de dados do SENSOR \_ \_ GUID de \_ luz \_ :

{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}

Essa categoria inclui os seguintes campos de dados definidos pela plataforma.



| Nome do campo de dados e PID                                                                                                                                                                                                                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <dt> **Tipo de dados do sensor \_ \_ \_ \_ CHROMACITY claro**</dt> <dt>(PID = 4)</dt> </dl>                     | **\_UI1 de vetor \| VT \_ VT**<br/> A desvio como uma matriz contada de valores float.<br/> Os dados para tipos de vetor são sempre serializados como **VT \_ UI1** (uma matriz de caracteres não assinados de 1 byte). Esse campo de dados realmente contém cada valor como um valor real de 4 bytes do IEEE (**VT \_ R4**).<br/> Para obter informações sobre como trabalhar com matrizes, consulte [Recuperando tipos de vetor](retrieving-vector-types.md).<br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ \_ \_ Lux de nível claro**</dt> <dt> (PID = 2)</dt> </dl>                            | **VT \_ R4**<br/> Nível de Illuminance, em Lux.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <dt>**Sensor \_ Tipo de dados \_ \_ \_ temperatura clara \_ Kelvin**</dt> <dt> (PID = 3)</dt> </dl> | **VT \_ R4**<br/> Temperatura de cor, em graus Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>Sensores. h</dt> </dl> |



 

 




