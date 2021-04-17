---
description: Estruturas de NTFS Transacional (TxF).
ms.assetid: 85b3cf8e-bff3-4693-b00e-64bf5d1f5065
title: Estruturas TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d490f608ef9ebfa6906d1acffa374a0c9327489b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783310"
---
# <a name="txf-structures"></a>Estruturas TxF

O NTFS Transacional (TxF) fornece as seguintes estruturas.

## <a name="in-this-section"></a>Nesta seção



| Estrutura                                                                                                    | Descrição                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TXFS \_ criar \_ informações de miniversão \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_create_miniversion_info)<br/>                           | Contém as informações de versão sobre o miniversão criado por [**fsctl \_ TXFS \_ Create \_ miniversão**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion).<br/>                                            |
| [**TXFS \_ obter \_ informações de metadados \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_metadata_info_out)<br/>                              | Contém as informações de versão sobre o miniversão que é criado.<br/>                                                                                                                 |
| [**ID do TXF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_id)<br/>                                                                         | Representa um identificador exclusivo dentro do contexto do Gerenciador de recursos.<br/>                                                                                                              |
| [**TXFS \_ obter \_ versão transacionada \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version)<br/>                             | Contém as informações sobre a base e as versões mais recentes do arquivo especificado.<br/>                                                                                                      |
| [**TXFS \_ listar \_ \_ arquivos bloqueados de transação \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files)<br/>              | Contém uma lista de arquivos bloqueados por um gravador transacionado.<br/>                                                                                                                                 |
| [**\_entrada de \_ \_ arquivos bloqueados de transação da \_ lista de TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files_entry)<br/> | Contém informações sobre uma transação bloqueada.<br/>                                                                                                                                        |
| [**TXFS \_ listar \_ Transações**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions)<br/>                                        | Contém uma lista de transações.<br/>                                                                                                                                                        |
| [**\_entrada de \_ Transações da lista de TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions_entry)<br/>                           | Contém informações sobre uma transação.<br/>                                                                                                                                               |
| [**\_ \_ arquivo afetado do registro de log TxF \_ \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_affected_file)<br/>                          | Contém informações para um arquivo que foi afetado por uma transação.<br/>                                                                                                                     |
| [**\_base de \_ registro de log TxF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_base)<br/>                                             | Contém as informações básicas de registro.<br/>                                                                                                                                                  |
| [**\_ \_ truncamento do registro de log TxF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_truncate)<br/>                                     | Contém o registro para uma operação de truncamento.<br/>                                                                                                                                           |
| [**\_gravação do \_ registro de log TxF \_**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_write)<br/>                                           | Contém o registro de uma operação de gravação.<br/>                                                                                                                                              |
| [**TXFS \_ Modificar \_ RM**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_modify_rm)<br/>                                                        | Contém as informações necessárias ao modificar os parâmetros de log e o modo de log para um Gerenciador de recursos secundário.<br/>                                                                      |
| [**\_informações do \_ RM de consulta TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_query_rm_information)<br/>                                 | Contém informações sobre o Gerenciador de recursos (RM).<br/>                                                                                                                                   |
| [**TXFS \_ ler \_ informações de backup \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/>                  | Contém uma estrutura específica de NTFS Transacional (TxF). Essas informações só devem ser usadas ao chamar [**TXFS \_ gravar \_ \_ informações de backup**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information).<br/>    |
| [**informações de pontos de \_ salvamento TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)<br/>                                | A estrutura de [**\_ informações do \_ salvamento \_ de fsctl TXFS**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information) especifica a ação a ser executada e em qual transação.<br/>                                      |
| [**\_ \_ informações ativas da transação do TXFS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_transaction_active_info)<br/>                           | Contém o sinalizador que indica se as transações estavam ativas ou não quando um instantâneo foi tirado.<br/>                                                                                     |
| [**TXFS \_ gravar \_ informações de backup \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>                         | Contém uma estrutura específica de NTFS Transacional (TxF). Essas informações só devem ser usadas ao chamar [**TXFS \_ gravar \_ \_ informações de backup**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out).<br/> |



 

 

