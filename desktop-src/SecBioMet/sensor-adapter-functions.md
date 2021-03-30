---
title: Funções do adaptador do sensor
description: Um adaptador de sensor encapsula um dispositivo biométrico e fornece uma interface padrão que permite que o serviço de biometria do Windows configure o sensor, Capture amostras e controle o fluxo de dados biométricos para o mecanismo de processamento.
ms.assetid: 32cf28d3-cb78-442d-81db-7827f55b0ba8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cefc5e9221a56a7766e6af6a47449db4405b369
ms.sourcegitcommit: 8a30948ba97ab969fcaa7f7ff05b853f59d8bd5c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/14/2020
ms.locfileid: "103640355"
---
# <a name="sensor-adapter-functions"></a>Funções do adaptador do sensor

Um adaptador de sensor encapsula um dispositivo biométrico e fornece uma interface padrão que permite que o serviço de biometria do Windows configure o sensor, Capture amostras e controle o fluxo de dados biométricos para o mecanismo de processamento. As funções a seguir devem ser implementadas pelo desenvolvedor do adaptador. Eles são chamados pelo serviço de biometria do Windows.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                           | Descrição                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SensorAdapterAcceptCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn)<br/>     | Passa dados de calibragem do adaptador do mecanismo para o adaptador do sensor.<br/>                                                                                            |
| [**SensorAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn)<br/>                               | Dá ao adaptador do sensor a chance de executar qualquer trabalho necessário para colocar o componente do sensor fora de um estado ocioso.<br/>                                                |
| [**SensorAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn)<br/>                                   | Adiciona um adaptador de sensor ao pipeline de processamento da unidade biométrica.<br/>                                                                                           |
| [**SensorAdapterCancel**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn)<br/>                                   | Cancela todas as operações de sensor pendentes.<br/>                                                                                                                            |
| [**SensorAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn)<br/>                       | Prepara o pipeline de processamento da unidade biométrica para uma nova operação.<br/>                                                                                       |
| [**SensorAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn)<br/>                         | Executa uma operação de controle definida pelo fornecedor que não requer privilégios elevados.<br/>                                                                             |
| [**SensorAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn)<br/>     | Executa uma operação de controle definida pelo fornecedor que requer privilégio elevado.<br/>                                                                                     |
| [**SensorAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn)<br/>                           | Dá ao adaptador do sensor a chance de executar qualquer trabalho necessário para colocar o componente do sensor em um estado ocioso.<br/>                                                    |
| [**SensorAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn)<br/>                                   | Libera recursos específicos do adaptador anexados ao pipeline.<br/>                                                                                                     |
| [**SensorAdapterExportSensorData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn)<br/>               | Recupera a amostra biométrica capturada mais recentemente, formatada como uma estrutura [**WINBIO \_ Bir**](winbio-bir.md) padrão.<br/>                                        |
| [**SensorAdapterFinishCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn)<br/>                     | Chamado pelo Windows Biometric Framework para aguardar a conclusão de uma operação de captura iniciada pela função SensorAdapterStartCapture.<br/>                                                                                       |
| [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)<br/>           | Recupera um valor que indica se o indicador do sensor está ativado ou desativado.<br/>                                                                                       |
| [*SensorAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn)<br/>               | Recebe uma notificação sobre uma alteração no estado de energia do computador e prepara o adaptador do sensor de acordo.<br/>                                                     |
| [**SensorAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn)<br/>                 | Dá ao adaptador do sensor a chance de executar qualquer limpeza no que exija ajuda do mecanismo ou dos componentes do adaptador de armazenamento.<br/>                                   |
| [**SensorAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn)<br/>                       | Dá ao adaptador do sensor a chance de executar qualquer inicialização que permaneça incompleta e que requer ajuda do mecanismo ou dos componentes do adaptador de armazenamento.<br/> |
| [**SensorAdapterPushDataToEngine**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn)<br/>               | Torna o conteúdo atual do buffer de exemplo disponível para o adaptador do mecanismo.<br/>                                                                                  |
| [**SensorAdapterQueryCalibrationFormats**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn)<br/> | Determina o conjunto de formatos de calibragem com suporte pelo adaptador do sensor.<br/>                                                                                        |
| [**SensorAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn)<br/>             | Determina os recursos e as limitações do componente sensor biométrico.<br/>                                                                                    |
| [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)<br/>                         | Recupera informações sobre o status atual do dispositivo de sensor.<br/>                                                                                              |
| [**SensorAdapterReset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn)<br/>                                     | Reinicializa o sensor.<br/>                                                                                                                                         |
| [**SensorAdapterSetCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn)<br/>       | Notifica o adaptador do sensor de que um formato de dados de calibragem específico foi selecionado pelo adaptador do mecanismo.<br/>                                                    |
| [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)<br/>           | Ativa ou desativa o indicador do sensor.<br/>                                                                                                                           |
| [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn)<br/>                                 | Define o modo do adaptador do sensor.<br/>                                                                                                                                     |
| [**SensorAdapterStartCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn)<br/>                       | Inicia uma captura biométrica assíncrona.<br/>                                                                                                                         |
| [**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)<br/>                         | Recupera um ponteiro para a estrutura da [**\_ \_ interface do sensor WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface) para o adaptador do sensor.<br/>                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de plug-in](plug-in-functions.md)
</dt> </dl>

 

 





