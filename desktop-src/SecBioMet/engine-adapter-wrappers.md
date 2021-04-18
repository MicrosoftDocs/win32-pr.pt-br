---
title: Wrappers do adaptador do mecanismo
description: Funções que você pode usar para chamar funções em seu adaptador de mecanismo. Essas funções são definidas em WinBio \_ Adapter. h.
ms.assetid: b3d6d617-e423-4ed5-9d29-be72c5dd8b49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5ec0fcc3b6ea358e8238061bc74e2933d8bf87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105760400"
---
# <a name="engine-adapter-wrappers"></a>Wrappers do adaptador do mecanismo

As seguintes funções de wrapper são definidas em WinBio \_ Adapter. h. Você pode usá-los para chamar funções em seu adaptador de mecanismo.



| Função                                           | Descrição                                                                                                                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioEngineAcceptSampleData<br/>              | Chama a função [**EngineAdapterAcceptSampleData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn) .<br/>                                                                                                 |
| WbioEngineActivate<br/>                      | Chama a função [**EngineAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_activate_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                                           |
| WbioEngineAttach<br/>                        | Chama a função [**EngineAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn) .<br/>                                                                                                                     |
| WbioEngineCheckForDuplicate<br/>             | Chama a função [**EngineAdapterCheckForDuplicate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn) .<br/>                                                                                               |
| WbioEngineClearContext<br/>                  | Chama a função [**EngineAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn) .<br/>                                                                                                         |
| WbioEngineCommitEnrollment<br/>              | Chama a função [**EngineAdapterCommitEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn) .<br/>                                                                                                 |
| WbioEngineControlUnit<br/>                   | Chama a função [**EngineAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn) .<br/>                                                                                                           |
| WbioEngineControlUnitPrivileged<br/>         | Chama a função [**EngineAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_privileged_fn) .<br/>                                                                                       |
| WbioEngineCreateEnrollment<br/>              | Chama a função [**EngineAdapterCreateEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn) .<br/>                                                                                                 |
| WbioEngineDeactivate<br/>                    | Chama a função [**EngineAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_deactivate_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                                       |
| WbioEngineDetach<br/>                        | Chama a função [**EngineAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_detach_fn) .<br/>                                                                                                                     |
| WbioEngineDiscardEnrollment<br/>             | Chama a função [**EngineAdapterDiscardEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn) .<br/>                                                                                               |
| WbioEngineExportEngineData<br/>              | Chama a função [**EngineAdapterExportEngineData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_export_engine_data_fn) .<br/>                                                                                                 |
| WbioEngineGetEnrollmentHash<br/>             | Chama a função [**EngineAdapterGetEnrollmentHash**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn) .<br/>                                                                                               |
| WbioEngineGetEnrollmentStatus<br/>           | Chama a função [**EngineAdapterGetEnrollmentStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_status_fn) .<br/>                                                                                           |
| WbioEngineIdentifyAll<br/>                   | Chama a função [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                                     |
| WbioEngineIdentifyFeatureSet<br/>            | Chama a função [**EngineAdapterIdentifyFeatureSet**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn) .<br/>                                                                                             |
| WbioEngineNotifyPowerChange<br/>             | Chama a função [*EngineAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_notify_power_change_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 8.<br/>                            |
| WbioEnginePipelineCleanup<br/>               | Chama a função [**EngineAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_cleanup_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                             |
| WbioEnginePipelineInit<br/>                  | Chama a função [**EngineAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_init_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                                   |
| WbioEngineQueryCalibrationData<br/>          | Chama a função [**EngineAdapterQueryCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_calibration_data_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                   |
| WbioEngineQueryExtendedEnrollmentStatus<br/> | Chama a função [**EngineAdapterQueryExtendedEnrollmentStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/> |
| WbioEngineQueryExtendedInfo<br/>             | Chama a função [**EngineAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                         |
| WbioEngineQueryHashAlgorithms<br/>           | Chama a função [**EngineAdapterQueryHashAlgorithms**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn) .<br/>                                                                                           |
| WbioEngineQueryIndexVectorSize<br/>          | Chama a função [**EngineAdapterQueryIndexVectorSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_index_vector_size_fn) .<br/>                                                                                         |
| WbioEngineQueryPreferredFormat<br/>          | Chama a função [**EngineAdapterQueryPreferredFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_preferred_format_fn) .<br/>                                                                                         |
| WbioEngineQuerySampleHint<br/>               | Chama a função [**EngineAdapterQuerySampleHint**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_sample_hint_fn) .<br/>                                                                                                   |
| WbioEngineRefreshCache<br/>                  | Chama a função [**EngineAdapterRefreshCache**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_refresh_cache_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                                   |
| WbioEngineSelectCalibrationFormat<br/>       | Chama a função [**EngineAdapterSelectCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_select_calibration_format_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>             |
| WbioEngineSetAccountPolicy<br/>              | Chama a função [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                           |
| WbioEngineSetEnrollmentParameters<br/>       | Chama a função [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>             |
| WbioEngineSetEnrollmentSelector<br/>         | Chama a função [**EngineAdapterSetEnrollmentSelector**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_selector_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                 |
| WbioEngineSetHashAlgorithm<br/>              | Chama a função [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) .<br/>                                                                                                 |
| WbioEngineUpdateEnrollment<br/>              | Chama a função [**EngineAdapterUpdateEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn) .<br/>                                                                                                 |
| WbioEngineVerifyFeatureSet<br/>              | Chama a função [**EngineAdapterVerifyFeatureSet**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_verify_feature_set_fn) .<br/>                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções do adaptador do mecanismo](engine-adapter-functions.md)
</dt> <dt>

[Funções de plug-in](plug-in-functions.md)
</dt> </dl>

 

 





