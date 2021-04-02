---
description: Enumerações usadas no gerenciamento de arquivos.
ms.assetid: 14b1cfff-5e47-4309-8e62-fb5c8da9ce97
title: Enumerações de gerenciamento de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b53d8f53bf9dbe16c15d21171e52ea3dd0015d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922630"
---
# <a name="file-management-enumerations"></a>Enumerações de gerenciamento de arquivos

As enumerações a seguir são usadas no gerenciamento de arquivos.

## <a name="in-this-section"></a>Nesta seção



| Enumeração                                                                   | Descrição                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Fase de cópia do COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_copy_phase)<br/>             | Indica a fase de uma cópia no momento de um erro.<br/>                                                                                                                                                                           |
| [**\_Ação de mensagem COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_action)<br/>     | Retornado pela função de retorno de chamada [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) para indicar qual ação deve ser executada para a operação de cópia pendente.<br/>                                                             |
| [**\_Tipo de mensagem COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_type)<br/>         | Indica o tipo de mensagem passada na estrutura [**de \_ mensagens COPYFILE2**](/windows/desktop/api/WinBase/ns-winbase-copyfile2_message) para a função de retorno de chamada [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) .<br/>                                       |
| [**\_operação do controle CSV \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-csv_control_op)<br/>                         | Especifica o tipo de operação de controle CSV a ser usado com o código de controle de [**\_ \_ controle CSV fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control) .<br/>                                                                                                       |
| [**\_tipo de ID de arquivo \_**](/windows/desktop/api/WinBase/ne-winbase-file_id_type)<br/>                             | Discriminador para a União na estrutura do [**\_ \_ descritor de ID de arquivo**](/windows/desktop/api/WinBase/ns-winbase-file_id_descriptor) .<br/>                                                                                                                                 |
| [**\_informações \_ de arquivo \_ por \_ classe de identificador**](/windows/win32/api/minwinbase/ne-minwinbase-file_info_by_handle_class)<br/> | Identifica o tipo de informações de arquivo que [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) deve recuperar ou [**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle) deve definir.<br/>                |
| [**\_níveis de informações do FINDEX \_**](/windows/win32/api/minwinbase/ne-minwinbase-findex_info_levels)<br/>             | Define os valores que são usados com a função [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) para especificar o nível de informações dos dados retornados.<br/>                                                                                 |
| [**\_operações de pesquisa do FINDEX \_**](/windows/win32/api/minwinbase/ne-minwinbase-findex_search_ops)<br/>               | Define os valores que são usados com a função [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) para especificar o tipo de filtragem a ser executado.<br/>                                                                                           |
| [**OBTER \_ \_ níveis de informações do FILEEX \_**](/windows/win32/api/minwinbase/ne-minwinbase-get_fileex_info_levels)<br/>        | Define os valores que são usados com as funções [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) e [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda) para especificar o nível de informações dos dados retornados.<br/> |
| [**Dica de prioridade \_**](/windows/desktop/api/WinBase/ne-winbase-priority_hint)<br/>                            | Define os valores que são usados com a estrutura de [**informações de dica de prioridade de e/s de arquivo \_ \_ \_ \_**](/windows/desktop/api/WinBase/ns-winbase-file_io_priority_hint_info) para especificar a dica de prioridade para uma operação de e/s de arquivo.<br/>                                                      |
| [**\_níveis de informações de fluxo \_**](/windows/desktop/api/fileapi/ne-fileapi-stream_info_levels)<br/>                 | Define os valores que são usados com a função [**FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) para especificar o nível de informações dos dados retornados.<br/>                                                                               |



 

 

