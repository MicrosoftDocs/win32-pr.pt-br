---
title: Wrappers do adaptador de armazenamento
description: Funções que você pode usar para chamar funções em seu adaptador de armazenamento. Essas funções são definidas em WinBio \_ Adapter. h.
ms.assetid: 3e7ff098-b8f3-4745-aa75-712a392c6c78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5dfdf562546e1520ee85c5a9a0164acdff53904
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364058"
---
# <a name="storage-adapter-wrappers"></a>Wrappers do adaptador de armazenamento

As seguintes funções de wrapper são definidas em WinBio \_ Adapter. h. Você pode usá-los para chamar funções em seu adaptador de armazenamento.



| Função                                    | Descrição                                                                                                                                                                     |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioStorageActivate<br/>              | Chama a função [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>                   |
| WbioStorageAddRecord<br/>             | Chama a função [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn) .<br/>                                                                                       |
| WbioStorageAttach<br/>                | Chama a função [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn) .<br/>                                                                                             |
| WbioStorageClearContext<br/>          | Chama a função [**StorageAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn) .<br/>                                                                                 |
| WbioStorageCloseDatabase<br/>         | Chama a função [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn) .<br/>                                                                               |
| WbioStorageControlUnit<br/>           | Chama a função [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn) .<br/>                                                                                   |
| WbioStorageControlUnitPrivileged<br/> | Chama a função [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn) .<br/>                                                               |
| WbioStorageCreateDatabase<br/>        | Chama a função [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn) .<br/>                                                                             |
| WbioStorageDeactivate<br/>            | Chama a função [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>               |
| WbioStorageDeleteRecord<br/>          | Chama a função [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn) .<br/>                                                                                 |
| WbioStorageDetach<br/>                | Chama a função [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn) .<br/>                                                                                             |
| WbioStorageEraseDatabase<br/>         | Chama a função [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn) .<br/>                                                                               |
| WbioStorageFirstRecord<br/>           | Chama a função [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn) .<br/>                                                                                   |
| WbioStorageGetCurrentRecord<br/>      | Chama a função [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn) .<br/>                                                                         |
| WbioStorageGetDatabaseSize<br/>       | Chama a função [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn) .<br/>                                                                           |
| WbioStorageGetDataFormat<br/>         | Chama a função [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn) .<br/>                                                                               |
| WbioStorageGetRecordCount<br/>        | Chama a função [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn) .<br/>                                                                             |
| WbioStorageNextRecord<br/>            | Chama a função [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn) .<br/>                                                                                     |
| WbioStorageNotifyPowerChange<br/>     | Chama a função [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 8.<br/>    |
| WbioStorageOpenDatabase<br/>          | Chama a função [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn) .<br/>                                                                                 |
| WbioStoragePipelineCleanup<br/>       | Chama a função [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>     |
| WbioStoragePipelineInit<br/>          | Chama a função [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/>           |
| WbioStorageQueryByContent<br/>        | Chama a função [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn) .<br/>                                                                             |
| WbioStorageQueryBySubject<br/>        | Chama a função [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn) .<br/>                                                                             |
| WbioStorageQueryExtendedInfo<br/>     | Chama a função [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn) .<br/> Essa função de wrapper tem suporte a partir do Windows 10.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções do adaptador de armazenamento](storage-adapter-functions.md)
</dt> <dt>

[Funções de plug-in](plug-in-functions.md)
</dt> </dl>

 

 





