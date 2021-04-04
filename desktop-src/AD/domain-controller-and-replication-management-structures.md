---
title: Estruturas de gerenciamento de replicação e controlador de domínio
description: O controlador de domínio e as funções de gerenciamento de replicação usam as seguintes estruturas.
ms.assetid: 42b20d3b-1799-4f5f-b74e-fe9284dd8ac3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4afe084e4285f4851457f9a519e747952e3bbd67
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823662"
---
# <a name="domain-controller-and-replication-management-structures"></a>Estruturas de gerenciamento de replicação e controlador de domínio

O controlador de domínio e as funções de gerenciamento de replicação usam as seguintes estruturas:

-   [**\_Informações do controlador de domínio DS \_ \_ \_ 1**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a)
-   [**\_Informações do controlador de domínio DS \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a)
-   [**\_Informações do controlador de domínio DS \_ \_ \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a)
-   [**\_resultado do nome DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_resulta)
-   [**\_item de \_ resultado do nome DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_result_itema)
-   [**\_metadados de \_ attr de repl \_ DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data)
-   [**\_Metadados de attr de repl DS \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2)
-   [**\_blob de \_ metadados de attr DS repl \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_blob)
-   [**\_metadados de \_ \_ valor de \_ attr \_ do DS repl**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data)
-   [**Metadados do valor de attr do DS \_ repl \_ \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2)
-   [**EXT. de metadados do valor de attr do DS \_ repl \_ \_ \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext)
-   [**\_cursor repl \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
-   [**\_Cursor de repl DS \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_2)
-   [**\_Cursor de repl DS \_ \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_3w)
-   [**\_blob de \_ cursor \_ repl DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_blob)
-   [**\_cursores de repl DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)
-   [**\_Cursores de repl do DS \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_2)
-   [**\_Cursores de repl do DS \_ \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_3w)
-   [**\_falha de \_ DSA do KCC \_ \_ do DS repl**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew)
-   [**\_falhas do \_ DSA do KCC \_ \_ do DS repl**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw)
-   [**\_ \_ \_ blob FAILUREW do DSA \_ de repl do DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew_blob)
-   [**\_vizinho de repl DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw)
-   [**\_vizinhos de repl DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborsw)
-   [**\_blob de \_ NEIGHBORW \_ repl DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw_blob)
-   [**\_metadados de \_ obj \_ repl \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data)
-   [**\_Metadados obj do DS repl \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2)
-   [**\_op de repl DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw)
-   [**\_blob de \_ OPW \_ repl DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw_blob)
-   [**\_ \_ operações pendentes de repl DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_pending_opsw)
-   [**\_STATISTICSW de \_ fila de repl DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_queue_statisticsw)
-   [**\_ \_ blob STATISTICSW da fila de repl DS \_ \_**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))
-   [**\_metadados de \_ valor de repl \_ DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data)
-   [**\_Metadados do valor de repl DS \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_2)
-   [**EXT. de metadados de valor de \_ repl DS \_ \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext)
-   [**\_blob de \_ metadados de valor de repl DS \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob)
-   [**EXT. de blob de \_ metadados de valor de repl DS \_ \_ \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob_ext)
-   [**\_ERRINFO REPSYNCALL \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa)
-   [**\_sincronização de REPSYNCALL DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_synca)
-   [**\_atualização de REPSYNCALL DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_updatea)
-   [**\_mapa de \_ GUID de esquema DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_schema_guid_mapa)
-   [**\_informações de \_ custo do site do DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_site_cost_info)
-   [**AGENDAMENTO**](/windows/desktop/api/Schedule/ns-schedule-schedule)
-   [**cabeçalho da agenda \_**](/windows/desktop/api/Schedule/ns-schedule-schedule_header)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estruturas no Active Directory Domain Services](structures-in-active-directory-domain-services.md)
</dt> </dl>

 

 