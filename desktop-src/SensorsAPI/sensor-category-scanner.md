---
description: A categoria SENSOR \_ CATEGORY SCANNER contém sensores que fornecem informações \_ obtidas pela verificação.
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59af4dbcd4ce4687a7fe2853384b4b19287cd95a0dd2033e7af031d2289f3d87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126586"
---
# <a name="sensor_category_scanner"></a>SCANNER \_ DE CATEGORIA DO \_ SENSOR

A categoria SENSOR \_ CATEGORY SCANNER contém sensores que fornecem informações \_ obtidas pela verificação.

**Tipos de sensor definidos pela plataforma**

Essa categoria inclui os seguintes tipos de sensor definidos pela plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                           | Descrição                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <dt>**SENSOR \_ SCANNER \_ DE CÓDIGO DE \_ BARRAS**</dt> <dt>DE TIPO {990B3D8F-85BB-45FF-914D-998C04F372DF}</dt> </dl> | Sensores que usam a verificação óptica para ler códigos de barras.<br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <dt>**SENSOR \_ SCANNER \_ DE \_ TIPO RFID**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt> </dl>          | Sensores de verificação de ID de frequência de rádio.<br/>                 |



**Campos de dados definidos pela plataforma**

As chaves de propriedade definidas pela plataforma para essa categoria são baseadas no GUID DO \_ SCANNER DO TIPO DE DADOS DO \_ \_ \_ SENSOR:

{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}

Essa categoria inclui os campos de dados definidos pela plataforma a seguir.



| Nome do campo de dados e PID                                                                                                                                                                                                                                                                     | Descrição                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <dt>**SENSOR \_ DATA \_ TYPE \_ RFID TAG \_ \_ 40 \_ BIT**</dt> <dt>(PID = 2)</dt> </dl> | **VT \_ UI8**<br/> Valor da marca de ID de frequência de rádio de 40 bits.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Cabeçalho<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




