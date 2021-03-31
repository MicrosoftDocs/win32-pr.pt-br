---
title: Constantes de WINBIO_SENSOR_MODE (WinBio \_ Types. h)
description: Defina o modo do adaptador do sensor.
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
ms.openlocfilehash: 2fedf419a64b3629d0cccbcb3d56de31a4adf383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645192"
---
# <a name="winbio_sensor_mode-constants"></a>Constantes do modo de \_ sensor WINBIO \_

Os valores a seguir são usados na função [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) para definir o modo do adaptador do sensor.



| Constante                                                                                                                                                                                                        | Descrição                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_SENSOR_UNKNOWN_MODE"></span><span id="winbio_sensor_unknown_mode"></span><dl> <dt>**\_ \_ modo desconhecido do sensor de WINBIO \_**</dt> </dl>          | O modo de operação não é conhecido.<br/>                                                                                                                    |
| <span id="WINBIO_SENSOR_BASIC_MODE"></span><span id="winbio_sensor_basic_mode"></span><dl> <dt>**\_ \_ modo básico do sensor WINBIO \_**</dt> </dl>                | Opere o sensor no modo básico. O sensor atua apenas como um dispositivo de captura. Qualquer recurso integrado de processamento ou armazenamento que não exista não será usado.<br/> |
| <span id="WINBIO_SENSOR_ADVANCED_MODE"></span><span id="winbio_sensor_advanced_mode"></span><dl> <dt>**\_ \_ modo avançado do sensor WINBIO \_**</dt> </dl>       | Opere o sensor no modo avançado. O sensor pode capturar amostras e executar funções de correspondência e armazenamento.<br/>                                     |
| <span id="WINBIO_SENSOR_NAVIGATION_MODE"></span><span id="winbio_sensor_navigation_mode"></span><dl> <dt>**\_modo de \_ navegação do sensor WINBIO \_**</dt> </dl> | Operar o sensor como um mouse pad. Atualmente, não há suporte para esse recurso.<br/>                                                                                 |
| <span id="WINBIO_SENSOR_SLEEP_MODE"></span><span id="winbio_sensor_sleep_mode"></span><dl> <dt>**\_modo de \_ suspensão do sensor WINBIO \_**</dt> </dl>                | Opere o sensor no modo de suspensão.<br/>                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





