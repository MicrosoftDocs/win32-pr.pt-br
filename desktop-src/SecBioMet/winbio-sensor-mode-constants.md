---
title: WINBIO_SENSOR_MODE constantes (tipos \_ Winbio.h)
description: Definir o modo do adaptador de sensor.
ms.assetid: fceaed5c-de59-4da7-9d7a-adeef353292f
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_UNKNOWN_MODE
- WINBIO_SENSOR_BASIC_MODE
- WINBIO_SENSOR_ADVANCED_MODE
- WINBIO_SENSOR_NAVIGATION_MODE
- WINBIO_SENSOR_SLEEP_MODE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e8f0cb4592931629e6feec4fff4a6ac3e5986d3b199afee719dd8dae67a9580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909324"
---
# <a name="winbio_sensor_mode-constants"></a>Constantes DO \_ \_ MODO SENSOR WINBIO

Os valores a seguir são usados na [**função SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) para definir o modo de adaptador do sensor.



| Constante                                                                                                                                                                                                        | Descrição                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <dt>**MODO DESCONHECIDO DO SENSOR WINBIO \_ \_ \_**</dt> </dl>          | O modo de operação não é conhecido.<br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <dt>**MODO BÁSICO \_ DO SENSOR \_ WINBIO \_**</dt> </dl>                | Opere o sensor no modo básico. O sensor atua apenas como um dispositivo de captura. Todos os recursos de processamento ou armazenamento de integração existentes não são usados.<br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <dt>**MODO AVANÇADO \_ DO SENSOR \_ WINBIO \_**</dt> </dl>       | Opere o sensor no modo avançado. O sensor pode capturar exemplos e executar funções de correspondência e armazenamento.<br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <dt>**MODO DE NAVEGAÇÃO DO SENSOR WINBIO \_ \_ \_**</dt> </dl> | Opere o sensor como um painel do mouse. Atualmente, não há suporte para esse recurso.<br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <dt>**MODO DE \_ SLEEP DO SENSOR \_ WINBIO \_**</dt> </dl>                | Opere o sensor no modo de espera.<br/>                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





