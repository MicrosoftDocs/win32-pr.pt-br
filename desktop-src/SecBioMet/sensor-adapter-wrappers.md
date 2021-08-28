---
title: Wrappers do adaptador do sensor
description: Funções que você pode usar para chamar funções no adaptador do sensor. Essas funções são definidas em WinBio \_ Adapter. h.
ms.assetid: 302a831c-38f7-4d32-8d9f-5ff58931224b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a9e4ade931e10a93320d132662bb7622e62028299816eb6ad0e41fd7bff527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683196"
---
# <a name="sensor-adapter-wrappers"></a>Wrappers do adaptador do sensor

As seguintes funções de wrapper são definidas em WinBio \_ Adapter. h. Você pode usá-los para chamar funções no adaptador do sensor.



| Função                                     | Descrição                                                                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioSensorAcceptCalibrationData<br/>   | Chama a função [**SensorAdapterAcceptCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>     |
| WbioSensorActivate<br/>                | Chama a função [**SensorAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                               |
| WbioSensorAttach<br/>                  | Chama a função [**SensorAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn) .<br/>                                                                                                         |
| WbioSensorCancel<br/>                  | Chama a função [**SensorAdapterCancel**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn) .<br/>                                                                                                         |
| WbioSensorClearContext<br/>            | Chama a função [**SensorAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn) .<br/>                                                                                             |
| WbioSensorControlUnit<br/>             | Chama a função [**SensorAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn) .<br/>                                                                                               |
| WbioSensorControlUnitPrivileged<br/>   | Chama a função [**SensorAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn) .<br/>                                                                           |
| WbioSensorDeactivate<br/>              | Chama a função [**SensorAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                           |
| WbioSensorDetach<br/>                  | Chama a função [**SensorAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn) .<br/>                                                                                                         |
| WbioSensorExportSensorData<br/>        | Chama a função [**SensorAdapterExportSensorData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn) .<br/>                                                                                     |
| WbioSensorFinishCapture<br/>           | Chama a função [**SensorAdapterFinishCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn) .<br/>                                                                                           |
| WbioSensorNotifyPowerChange<br/>       | Chama a função [**SensorAdapterNotifyPowerChange**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 8.<br/>              |
| WbioSensorPipelineCleanup<br/>         | Chama a função [**SensorAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                 |
| WbioSensorPipelineInit<br/>            | Chama a função [**SensorAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                       |
| WbioSensorPushDataToEngine<br/>        | Chama a função [**SensorAdapterPushDataToEngine**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn) .<br/>                                                                                     |
| WbioSensorQueryCalibrationFormats<br/> | Chama a função [**SensorAdapterQueryCalibrationFormats**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/> |
| WbioSensorQueryExtendedInfo<br/>       | Chama a função [**SensorAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>             |
| WbioSensorQueryStatus<br/>             | Chama a função [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn) .<br/>                                                                                               |
| WbioSensorReset<br/>                   | Chama a função [**SensorAdapterReset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn) .<br/>                                                                                                           |
| WbioSensorSetCalibrationFormat<br/>    | Chama a função [**SensorAdapterSetCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>       |
| WbioSensorSetMode<br/>                 | Chama a função [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) .<br/>                                                                                                       |
| WbioSensorStartCapture<br/>            | Chama a função [**SensorAdapterStartCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn) .<br/>                                                                                             |



 

Não há nenhuma função de wrapper para as funções [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn) e [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções do adaptador do sensor](sensor-adapter-functions.md)
</dt> <dt>

[Funções de plug-in](plug-in-functions.md)
</dt> </dl>

 

 





