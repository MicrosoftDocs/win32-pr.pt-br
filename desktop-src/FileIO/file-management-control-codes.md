---
description: Códigos de controle usados no gerenciamento de arquivos.
ms.assetid: e27ded4b-d104-4244-b38e-5fed10d32e1e
title: Códigos de controle de gerenciamento de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cb3baf78c4066a640242afe8465592bc9a6f8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837001"
---
# <a name="file-management-control-codes"></a>Códigos de controle de gerenciamento de arquivos

Os códigos de controle a seguir são usados no gerenciamento de arquivos.

## <a name="in-this-section"></a>Nesta seção



| Código de controle                                                                                    | Descrição                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ permitir \_ \_ \_ e/s de DASD estendidas**](/windows/win32/api/winioctl/ni-winioctl-fsctl_allow_extended_dasd_io)<br/>             | Sinaliza ao driver do sistema de arquivos para não executar verificações de limite de e/s em chamadas de leitura ou gravação de partição.<br/>                                                                                  |
| [**FSCTL \_ criar \_ ou \_ obter \_ ID de objeto \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)<br/>          | Recupera o identificador de objeto para o arquivo ou diretório especificado. Se não existir nenhum identificador de objeto, o uso **\_ de fsctl Create \_ ou \_ Get \_ Object \_ ID** criará um.<br/>                           |
| [**\_controle CSV \_ fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control)<br/>                                     | Recupera os resultados de uma operação de controle CSV.<br/>                                                                                                                                        |
| [**FSCTL \_ excluir \_ ID de objeto \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)<br/>                          | Remove o identificador de objeto de um arquivo ou diretório especificado.<br/>                                                                                                                        |
| [**FSCTL \_ \_ extensões duplicadas \_ para o \_ arquivo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)<br/>       | Instrui o sistema de arquivos a copiar um intervalo de bytes de arquivo em nome de um aplicativo.<br/>                                                                                                     |
| [**\_corte de \_ nível de arquivo fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_file_level_trim)<br/>                            | Indica ao sistema de armazenamento quais intervalos no arquivo não são necessários para serem armazenados.<br/>                                                                                                    |
| [**Estatísticas de obtenção do sistema de \_ arquivos fsctl \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics)<br/>        | Recupera as informações de vários contadores de desempenho do sistema de arquivos.<br/>                                                                                                                 |
| [**FSCTL do \_ sistema de arquivos \_ Get \_ Statistics \_ ex**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics_ex)<br/> | Recupera as informações de vários contadores de desempenho do sistema de arquivos.<br/> O suporte para esse código de controle foi iniciado com o Windows 10.<br/>                                               |
| [**FSCTL \_ localizar \_ arquivos \_ por \_ Sid**](/windows/win32/api/winioctl/ni-winioctl-fsctl_find_files_by_sid)<br/>                       | Pesquisa um diretório em busca de um arquivo cujo proprietário do criador corresponda ao SID especificado.<br/>                                                                                                           |
| [**FSCTL \_ obter \_ compactação**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)<br/>                             | Recupera o estado de compactação atual de um arquivo ou diretório em um volume cujo sistema de arquivos dá suporte à compactação por fluxo.<br/>                                                            |
| [**FSCTL \_ obter \_ \_ registro de arquivo NTFS \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record)<br/>                 | Recupera o primeiro registro de arquivo que está em uso e que é de um valor ordinal menor ou igual ao número de referência do arquivo solicitado.<br/>                                                    |
| [**FSCTL \_ obter \_ ID de objeto \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)<br/>                                | Recupera o identificador de objeto para o arquivo ou diretório especificado.<br/>                                                                                                                     |
| [**FSCTL \_ obter \_ reparo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)<br/>                                       | Recupera informações sobre o mecanismo de auto-recuperação do sistema de arquivos NTFS.<br/>                                                                                                               |
| [**FSCTL \_ Iniciar \_ reparo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)<br/>                             | Dispara o sistema de arquivos NTFS para iniciar um ciclo de auto-recuperação em um único arquivo.<br/>                                                                                                            |
| [**FSCTL \_ tornar \_ mídia \_ compatível**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)<br/>                | Fecha uma sessão UDF aberta em uma mídia de gravação única para tornar a ROM de mídia compatível.<br/>                                                                                                         |
| [**FSCTL \_ OPBATCH \_ ACK \_ fechamento \_ pendente**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)<br/>       | Notifica um servidor de que um aplicativo cliente está pronto para fechar um arquivo.<br/>                                                                                                                    |
| [**\_ACK de quebra de oplock fsctl \_ \_ \_ não \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)<br/>              | Responde à notificação de que um bloqueio oportunista em um arquivo está prestes a ser interrompido. Use esta operação para desbloquear todos os bloqueios oportunistas no arquivo, mas mantenha o arquivo aberto.<br/>            |
| [**\_confirmação de \_ quebra de oplock fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)<br/>          | Responde à notificação de que um bloqueio oportunista exclusivo em um arquivo está prestes a ser interrompido. Use essa operação para indicar que o arquivo deve receber um bloqueio oportunista de nível 2.<br/> |
| [**\_notificação de \_ quebra de oplock fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)<br/>                    | Permite que o aplicativo de chamada aguarde a conclusão de uma interrupção de bloqueio oportunista.<br/>                                                                                                   |
| [**\_ \_ intervalos alocados da consulta fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)<br/>              | Examina um arquivo ou um fluxo alternativo procurando intervalos que possam conter dados diferentes de zero.<br/>                                                                                                       |
| [**\_consulta \_ do fsctl \_ em \_ informações de volume do disco \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)<br/>      | Solicita informações de volume específicas de UDF.<br/>                                                                                                                                                |
| [**\_informações de \_ Sparing de consulta do fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)<br/>                      | Recupera as propriedades de gerenciamento de defeito do volume. Usado para sistemas de arquivos UDF.<br/>                                                                                                     |
| [**FSCTL \_ recuperar \_ arquivo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_recall_file)<br/>                                     | O recupera um arquivo da mídia de armazenamento que o armazenamento remoto gerencia, que é o software de gerenciamento de armazenamento hierárquico.<br/>                                                                    |
| [**OPLOCK FSCTL de \_ solicitação de \_ lote \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)<br/>                  | Solicita um bloqueio oportunista em lote em um arquivo.<br/>                                                                                                                                           |
| [**\_oplock de \_ filtro de solicitação fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)<br/>                | Solicita um bloqueio oportunista de filtro em um arquivo.<br/>                                                                                                                                          |
| [**\_oplock de solicitação de fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)<br/>                               | Solicita um bloqueio oportunista (oplock) em um arquivo e confirma que ocorreu uma interrupção de oplock.<br/>                                                                                    |
| [**\_Nível de bloqueio de solicitação fsctl \_ \_ \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)<br/>             | Solicita um bloqueio oportunista de nível 1 em um arquivo.<br/>                                                                                                                                         |
| [**\_Nível de bloqueio de solicitação fsctl \_ \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)<br/>             | Solicita um bloqueio oportunista de nível 2 em um arquivo.<br/>                                                                                                                                         |
| [**\_compactação do conjunto de fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                             | Define o estado de compactação de um arquivo ou diretório em um volume cujo sistema de arquivos dá suporte à compactação por arquivo e por diretório.<br/>                                                         |
| [**FSCTL \_ definir \_ Gerenciamento de defeitos \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)<br/>                | Define o estado de gerenciamento de defeitos de software para o arquivo especificado. Usado para sistemas de arquivos UDF.<br/>                                                                                             |
| [**FSCTL \_ definir \_ ID de objeto \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)<br/>                                | Define o identificador de objeto para o arquivo ou diretório especificado.<br/>                                                                                                                          |
| [**FSCTL \_ definir \_ ID de objeto \_ \_ estendido**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)<br/>             | Modifica os dados do usuário associados ao identificador de objeto para o arquivo ou diretório especificado.<br/>                                                                                            |
| [**FSCTL \_ definir \_ reparo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)<br/>                                       | Define o modo de um recurso de auto-recuperação do sistema de arquivos NTFS.<br/>                                                                                                                          |
| [**FSCTL \_ definir \_ esparso**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)<br/>                                       | Marca o arquivo indicado como esparso ou não esparso. Em um arquivo esparso, grandes intervalos de zeros podem não exigir alocação de disco.<br/>                                                               |
| [**FSCTL \_ definir \_ zero \_ dados**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)<br/>                                | Preenche um intervalo especificado de um arquivo com zeros (0).<br/>                                                                                                                                        |
| [**FSCTL \_ definir \_ zero \_ na \_ desalocação**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_on_deallocation)<br/>         | Indica que um identificador de arquivo do sistema de arquivos NTFS deve ter seus clusters preenchidos com zeros quando ele é desalocado.<br/>                                                                             |
| [**FSCTL \_ aguardar \_ \_ reparo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)<br/>                            | Retorna quando os reparos especificados são concluídos.<br/>                                                                                                                                        |



 

Os códigos de controle a seguir são usados com [compactação e descompactação de arquivo](file-compression-and-decompression.md).

<dl>

[**FSCTL \_ obter \_ compactação**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)  
[**\_compactação do conjunto de fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)  
</dl>

Os códigos de controle a seguir são usados com [identificadores de objeto](distributed-link-tracking-and-object-identifiers.md).

<dl>

[**FSCTL \_ criar \_ ou \_ obter \_ ID de objeto \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)  
[**FSCTL \_ excluir \_ ID de objeto \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)  
[**FSCTL \_ obter \_ ID de objeto \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)  
[**FSCTL \_ definir \_ ID de objeto \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)  
[**FSCTL \_ definir \_ ID de objeto \_ \_ estendido**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)  
</dl>

Os códigos de controle a seguir são usados com [bloqueios oportunistas](opportunistic-locks.md).

<dl>

[**FSCTL \_ OPBATCH \_ ACK \_ fechamento \_ pendente**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**\_ACK de quebra de oplock fsctl \_ \_ \_ não \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**\_confirmação de \_ quebra de oplock fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**\_notificação de \_ quebra de oplock fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**OPLOCK FSCTL de \_ solicitação de \_ lote \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**\_oplock de \_ filtro de solicitação fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**\_oplock de solicitação de fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**\_Nível de bloqueio de solicitação fsctl \_ \_ \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**\_Nível de bloqueio de solicitação fsctl \_ \_ \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

Os códigos de controle a seguir são usados com [arquivos esparsos](sparse-files.md).

<dl>

[**\_ \_ intervalos alocados da consulta fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)  
[**FSCTL \_ definir \_ esparso**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)  
[**FSCTL \_ definir \_ zero \_ dados**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)  
</dl>

Os códigos de controle a seguir são usados com o mecanismo de auto-recuperação do NTFS.

<dl>

[**FSCTL \_ obter \_ reparo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)  
[**FSCTL \_ Iniciar \_ reparo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)  
[**FSCTL \_ definir \_ reparo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)  
[**FSCTL \_ aguardar \_ \_ reparo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)  
</dl>

Os códigos de controle a seguir são usados com UDF.

<dl>

[**FSCTL \_ tornar \_ mídia \_ compatível**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)  
[**\_consulta \_ do fsctl \_ em \_ informações de volume do disco \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)  
[**\_informações de \_ Sparing de consulta do fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)  
[**FSCTL \_ definir \_ Gerenciamento de defeitos \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Códigos de controle de gerenciamento de diretório](directory-management-control-codes.md)
</dt> <dt>

[Códigos de controle de gerenciamento de volume](volume-management-control-codes.md)
</dt> </dl>

 

