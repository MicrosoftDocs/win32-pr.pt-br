---
description: Estruturas transacionais NTFS (TxF).
ms.assetid: 85b3cf8e-bff3-4693-b00e-64bf5d1f5065
title: Estruturas TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6acdbaac0798ef2dac3b3fefad9a1f5de505eb9781316fca82d45cfad26af0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765836"
---
# <a name="txf-structures"></a>Estruturas TxF

O NTFS transacional (TxF) fornece as seguintes estruturas.

## <a name="in-this-section"></a>Nesta seção



| Estrutura                                                                                                    | Descrição                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TXFS \_ CREATE \_ MINIVERSION \_ INFO**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_create_miniversion_info)<br/>                           | Contém as informações de versão sobre a miniversão criada por [**FSCTL \_ TXFS \_ CREATE \_ MINIVERSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion).<br/>                                            |
| [**OBTER INFORMAÇÕES DE \_ \_ \_ METADADOS DO TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_metadata_info_out)<br/>                              | Contém as informações de versão sobre a miniversão criada.<br/>                                                                                                                 |
| [**ID do TXF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_id)<br/>                                                                         | Representa um identificador exclusivo dentro do contexto do Resource Manager.<br/>                                                                                                              |
| [**VERSÃO DO TXFS \_ \_ GET \_ TRANSACTED**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version)<br/>                             | Contém as informações sobre as versões base e mais recente do arquivo especificado.<br/>                                                                                                      |
| [**ARQUIVOS BLOQUEADOS DA \_ \_ TRANSAÇÃO DE LISTA DO \_ TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files)<br/>              | Contém uma lista de arquivos bloqueados por um autor transacionado.<br/>                                                                                                                                 |
| [**ENTRADA DE ARQUIVOS BLOQUEADOS DA \_ \_ TRANSAÇÃO \_ DE \_ \_ LISTA DO TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files_entry)<br/> | Contém informações sobre uma transação bloqueada.<br/>                                                                                                                                        |
| [**TRANSAÇÕES DE LISTA DO TXFS \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions)<br/>                                        | Contém uma lista de transações.<br/>                                                                                                                                                        |
| [**ENTRADA DE TRANSAÇÕES DE LISTA DO TXFS \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions_entry)<br/>                           | Contém informações sobre uma transação.<br/>                                                                                                                                               |
| [**ARQUIVO DE REGISTRO \_ DE LOG TXF \_ \_ \_ AFETADO**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_affected_file)<br/>                          | Contém informações para um arquivo que foi afetado por uma transação.<br/>                                                                                                                     |
| [**BASE DE REGISTRO DE LOG DO TXF \_ \_ \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_base)<br/>                                             | Contém as informações básicas do registro.<br/>                                                                                                                                                  |
| [**TRUNCATE DE REGISTRO \_ DE LOG \_ \_ TXF**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_truncate)<br/>                                     | Contém o registro de uma operação de truncar.<br/>                                                                                                                                           |
| [**GRAVAÇÃO DE REGISTRO DE LOG TXF \_ \_ \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_write)<br/>                                           | Contém o registro de uma operação de gravação.<br/>                                                                                                                                              |
| [**TXFS \_ MODIFY \_ RM**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_modify_rm)<br/>                                                        | Contém as informações necessárias ao modificar os parâmetros de log e o modo de registro em log para um gerenciador de recursos secundário.<br/>                                                                      |
| [**INFORMAÇÕES DO RM \_ DE \_ CONSULTA DO \_ TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_query_rm_information)<br/>                                 | Contém informações sobre o RM (gerenciador de recursos).<br/>                                                                                                                                   |
| [**LER INFORMAÇÕES DE \_ \_ BACKUP \_ DO \_ TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/>                  | Contém uma estrutura específica de NTFS transacional (TxF). Essas informações só devem ser usadas ao chamar INFORMAÇÕES DE BACKUP DE GRAVAÇÃO [**\_ \_ do \_ TXFS.**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>    |
| [**INFORMAÇÕES DO \_ SAVEPOINT DO TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)<br/>                                | A [**estrutura FSCTL \_ TXFS \_ SAVEPOINT \_ INFORMATION**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information) especifica a ação a ser realizada e em qual transação.<br/>                                      |
| [**INFORMAÇÕES ATIVAS DA TRANSAÇÃO DO TXFS \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_transaction_active_info)<br/>                           | Contém o sinalizador que indica se as transações estavam ativas ou não quando um instantâneo foi tirado.<br/>                                                                                     |
| [**INFORMAÇÕES DE BACKUP DE GRAVAÇÃO DO TXFS \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>                         | Contém uma estrutura específica de NTFS transacional (TxF). Essas informações só devem ser usadas ao chamar INFORMAÇÕES DE BACKUP DE GRAVAÇÃO [**\_ \_ do \_ TXFS.**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/> |



 

 

