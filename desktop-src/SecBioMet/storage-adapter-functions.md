---
title: Armazenamento Funções de adaptador
description: Um adaptador de armazenamento gerencia bancos de dados de modelo.
ms.assetid: bfb0c9e5-a95e-4054-bc83-98ff682994a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7072847c6d1ca653bd9e8edad9c51b7736354b447feeafda7c465973d4c25aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911798"
---
# <a name="storage-adapter-functions"></a>Armazenamento Funções de adaptador

Um adaptador de armazenamento gerencia bancos de dados de modelo. As funções a seguir devem ser implementadas pelo desenvolvedor do adaptador. eles são chamados pelo serviço biométrico Windows.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                         | Descrição                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn)<br/>                           | dá ao adaptador de Armazenamento a chance de executar qualquer trabalho necessário para colocar o componente de armazenamento fora do estado ocioso.<br/>         |
| [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn)<br/>                         | Adiciona um modelo ao banco de dados.<br/>                                                                                             |
| [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn)<br/>                               | Adiciona um adaptador de armazenamento ao pipeline de processamento da unidade biométrica.<br/>                                                     |
| [**StorageAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn)<br/>                   | Prepara o pipeline de processamento da unidade biométrica para uma nova operação.<br/>                                                  |
| [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn)<br/>                 | Fecha o banco de dados associado ao pipeline e libera todos os recursos relacionados.<br/>                                            |
| [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn)<br/>                     | Executa uma operação de controle definida pelo fornecedor que não requer privilégios elevados.<br/>                                        |
| [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn)<br/> | Executa uma operação de controle definida pelo fornecedor que requer privilégio elevado.<br/>                                                |
| [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn)<br/>               | Cria e configura um novo banco de dados.<br/>                                                                                       |
| [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn)<br/>                       | dá ao adaptador de Armazenamento a chance de executar qualquer trabalho necessário para colocar o componente de armazenamento em um estado ocioso.<br/>             |
| [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn)<br/>                   | Exclui um ou mais modelos do banco de dados.<br/>                                                                             |
| [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn)<br/>                               | Libera recursos específicos do adaptador anexados ao pipeline.<br/>                                                                |
| [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn)<br/>                 | Apaga o banco de dados e o marca para exclusão.<br/>                                                                               |
| [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn)<br/>                     | Posiciona o cursor do conjunto de resultados no primeiro registro do conjunto.<br/>                                                              |
| [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn)<br/>           | Recupera o conteúdo do registro atual no conjunto de resultados do pipeline.<br/>                                                     |
| [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn)<br/>             | Recupera o tamanho do banco de dados e o espaço disponível.<br/>                                                                             |
| [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn)<br/>                 | Recupera as informações de formato e versão usadas pelo banco de dados atual associado ao pipeline.<br/>                          |
| [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn)<br/>               | Recupera o número de registros de modelo no conjunto de resultados do pipeline.<br/>                                                         |
| [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn)<br/>                       | Avança o cursor do conjunto de resultados por um registro.<br/>                                                                                |
| [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn)<br/>           | Recebe uma notificação sobre uma alteração no estado de energia do computador e prepara o adaptador de armazenamento de acordo.<br/>               |
| [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn)<br/>                   | Abre um banco de dados para uso pelo adaptador de armazenamento.<br/>                                                                             |
| [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn)<br/>             | dá ao adaptador de Armazenamento a chance de executar qualquer limpeza na preparação para fechar o banco de dados de modelo.<br/>                |
| [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn)<br/>                   | dá ao adaptador de Armazenamento a chance de executar qualquer inicialização que permaneça incompleta.<br/>                                  |
| [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn)<br/>               | Consulta o banco de dados que está aberto atualmente para modelos associados a um vetor de índice especificado.<br/>                          |
| [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn)<br/>               | Consulta o banco de dados que está aberto atualmente para modelos associados a uma identidade e um subfatores especificados.<br/>               |
| [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn)<br/>         | Determina os recursos e as limitações do componente de armazenamento biométrico.<br/>                                              |
| [**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)<br/>                     | Recupera um ponteiro para a estrutura de [**\_ \_ interface de armazenamento WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface) para o adaptador de armazenamento.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de plug-in](plug-in-functions.md)
</dt> </dl>

 

 





