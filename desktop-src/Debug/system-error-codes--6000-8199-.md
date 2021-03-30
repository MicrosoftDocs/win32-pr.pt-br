---
description: Descreve os códigos de erro 6000-8199 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Códigos de erro do sistema (6000-8199) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826518"
---
# <a name="system-error-codes-6000-8199"></a>Códigos de erro do sistema (6000-8199)

> [!NOTE]
> Essas informações destinam-se a desenvolvedores Depurando erros do sistema. Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .

A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) (erros 6000 a 8199). Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham. Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .

<dl> <dt>

<span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**\_falha na criptografia de erro \_**
</dt> <dd> <dl> <dt>

6000 (0x1770)
</dt> <dt>



O arquivo especificado não pôde ser criptografado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**\_falha na descriptografia de erro \_**
</dt> <dd> <dl> <dt>

6001 (0x1771)
</dt> <dt>



O arquivo especificado não pôde ser descriptografado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**arquivo de erro \_ \_ criptografado**
</dt> <dd> <dl> <dt>

6002 (0x1772)
</dt> <dt>



O arquivo especificado é criptografado e o usuário não tem a capacidade de descriptografá-lo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERRO \_ sem \_ política de recuperação \_**
</dt> <dd> <dl> <dt>

6003 (0x1773)
</dt> <dt>



Não há uma política de recuperação de criptografia válida configurada para este sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERRO \_ sem \_ EFS**
</dt> <dd> <dl> <dt>

6004 (0x1774)
</dt> <dt>



O driver de criptografia necessário não está carregado para este sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERRO \_ de \_ EFS incorreto**
</dt> <dd> <dl> <dt>

6005 (0x1775)
</dt> <dt>



O arquivo foi criptografado com um driver de criptografia diferente do que está carregado no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERRO \_ sem \_ chaves de usuário \_**
</dt> <dd> <dl> <dt>

6006 (0x1776)
</dt> <dt>



Não há chaves EFS definidas para o usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**arquivo de erro \_ \_ não \_ criptografado**
</dt> <dd> <dl> <dt>

6007 (0x1777)
</dt> <dt>



O arquivo especificado não está criptografado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERRO de \_ não \_ Exportar \_ formato**
</dt> <dd> <dl> <dt>

6008 (0x1778)
</dt> <dt>



O arquivo especificado não está no formato de exportação EFS definido.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**\_arquivo de \_ erro \_ somente leitura**
</dt> <dd> <dl> <dt>

6009 (0x1779)
</dt> <dt>



O arquivo especificado é somente leitura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERRO de \_ dir do \_ DFS não \_ permitido**
</dt> <dd> <dl> <dt>

6010 (0x177A)
</dt> <dt>



O diretório foi desabilitado para criptografia.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERRO \_ de \_ servidor EFS \_ não \_ confiável**
</dt> <dd> <dl> <dt>

6011 (0x177B)
</dt> <dt>



O servidor não é confiável para a operação de criptografia remota.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERRO \_ de \_ política de recuperação inadequada \_**
</dt> <dd> <dl> <dt>

6012 (0x177C)
</dt> <dt>



A política de recuperação configurada para este sistema contém um certificado de recuperação inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERRO \_ de \_ blob de alg EFS \_ \_ muito \_ grande**
</dt> <dd> <dl> <dt>

6013 (0x177D)
</dt> <dt>



O algoritmo de criptografia usado no arquivo de origem precisa de um buffer de chave maior do que aquele no arquivo de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**o \_ volume de erros \_ não \_ dá suporte ao \_ EFS**
</dt> <dd> <dl> <dt>

6014 (0x177E)
</dt> <dt>



A partição de disco não dá suporte à criptografia de arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERRO \_ EFS \_ desabilitado**
</dt> <dd> <dl> <dt>

6015 (0x177F)
</dt> <dt>



Este computador está desabilitado para criptografia de arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERRO \_ de \_ versão do EFS \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

6016 (0x1780)
</dt> <dt>



Um sistema mais recente é necessário para descriptografar esse arquivo criptografado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERRO \_ cs \_ Encryption \_ inválida \_ do servidor de \_ resposta**
</dt> <dd> <dl> <dt>

6017 (0x1781)
</dt> <dt>



O servidor remoto enviou uma resposta inválida para um arquivo que está sendo aberto com criptografia do lado do cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERRO \_ cs \_ criptografia \_ \_ do servidor sem suporte**
</dt> <dd> <dl> <dt>

6018 (0x1782)
</dt> <dt>



A criptografia do lado do cliente não é compatível com o servidor remoto, mesmo que ele alega oferecer suporte a ele.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERRO \_ cs \_ criptografia \_ \_ arquivo criptografado existente \_**
</dt> <dd> <dl> <dt>

6019 (0x1783)
</dt> <dt>



O arquivo é criptografado e deve ser aberto no modo de criptografia do lado do cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERRO \_ cs \_ criptografia \_ novo \_ arquivo criptografado \_**
</dt> <dd> <dl> <dt>

6020 (0x1784)
</dt> <dt>



Um novo arquivo criptografado está sendo criado e um $EFS precisa ser fornecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERRO \_ cs \_ criptografia \_ arquivo \_ não \_ CSE**
</dt> <dd> <dl> <dt>

6021 (0x1785)
</dt> <dt>



O cliente SMB solicitou um CSE FSCTL em um arquivo que não é CSE.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**\_operação de \_ negação de política de criptografia de erro \_ \_**
</dt> <dd> <dl> <dt>

6022 (0x1786)
</dt> <dt>



A operação solicitada foi bloqueada pela política. Para obter mais informações, contate o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERRO \_ nenhum \_ servidor de navegador \_ \_ encontrado**
</dt> <dd> <dl> <dt>

6118 (0x17E6)
</dt> <dt>



A lista de servidores para este grupo de trabalho não está disponível no momento.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED \_ E \_ serviço \_ não \_ LOCALSYSTEM**
</dt> <dd> <dl> <dt>

6200 (0x1838)
</dt> <dt>



O serviço de Agendador de Tarefas deve ser configurado para ser executado na conta do sistema para funcionar corretamente. Tarefas individuais podem ser configuradas para serem executadas em outras contas.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**setor de log de erros \_ \_ \_ inválido**
</dt> <dd> <dl> <dt>

6600 (0x19C8)
</dt> <dt>



O serviço de log encontrou um setor de log inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**paridade de setor de log de erros \_ \_ \_ \_ inválida**
</dt> <dd> <dl> <dt>

6601 (0x19C9)
</dt> <dt>



O serviço de log encontrou um setor de log com paridade de bloco inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**setor de log de erros \_ \_ \_ remapeado**
</dt> <dd> <dl> <dt>

6602 (0x19CA)
</dt> <dt>



O serviço de log encontrou um setor de log remapeado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**bloco de log de erros \_ \_ \_ incompleto**
</dt> <dd> <dl> <dt>

6603 (0x19CB)
</dt> <dt>



O serviço de log encontrou um bloco de log parcial ou incompleto.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ intervalo inválido do log de erros \_**
</dt> <dd> <dl> <dt>

6604 (0x19CC)
</dt> <dt>



O serviço de log encontrou uma tentativa de acessar dados fora do intervalo de log ativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**blocos de log de erros \_ \_ \_ esgotados**
</dt> <dd> <dl> <dt>

6605 (0x19CD)
</dt> <dt>



Os buffers de Marshalling de usuário do serviço de log estão esgotados.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**contexto de leitura do log de erros \_ \_ \_ \_ inválido**
</dt> <dd> <dl> <dt>

6606 (0x19CE)
</dt> <dt>



O serviço de log encontrou uma tentativa de leitura de uma área de Marshalling com um contexto de leitura inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**reinicialização do log de erros \_ \_ \_ inválida**
</dt> <dd> <dl> <dt>

6607 (0x19CF)
</dt> <dt>



O serviço de log encontrou uma área de reinício de log inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**\_versão do \_ bloco de log de erros \_**
</dt> <dd> <dl> <dt>

6608 (0x19D0)
</dt> <dt>



O serviço de log encontrou uma versão de bloco de log inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**bloco de log de erros \_ \_ \_ inválido**
</dt> <dd> <dl> <dt>

6609 (0x19D1)
</dt> <dt>



O serviço de log encontrou um bloco de log inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**modo de leitura de log de erros \_ \_ \_ \_ inválido**
</dt> <dd> <dl> <dt>

6610 (0x19D2)
</dt> <dt>



O serviço de log encontrou uma tentativa de ler o log com um modo de leitura inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**LOG de erros \_ \_ sem \_ reinicialização**
</dt> <dd> <dl> <dt>

6611 (0x19D3)
</dt> <dt>



O serviço de log encontrou um fluxo de log sem área de reinicialização.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**metadados do log de erros \_ \_ \_ corrompidos**
</dt> <dd> <dl> <dt>

6612 (0x19D4)
</dt> <dt>



O serviço de log encontrou um arquivo de metadados corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**metadados de log de erros \_ \_ \_ inválidos**
</dt> <dd> <dl> <dt>

6613 (0x19D5)
</dt> <dt>



O serviço de log encontrou um arquivo de metadados que não pôde ser criado pelo sistema de arquivos de log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**metadados do log de erros \_ \_ \_ inconsistentes**
</dt> <dd> <dl> <dt>

6614 (0x19D6)
</dt> <dt>



O serviço de log encontrou um arquivo de metadados com dados inconsistentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**Reserva de log de erros \_ \_ \_ inválida**
</dt> <dd> <dl> <dt>

6615 (0x19D7)
</dt> <dt>



O serviço de log encontrou uma tentativa de alocar ou descartar o espaço de reserva.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**o log de erros não \_ \_ consegue \_ excluir**
</dt> <dd> <dl> <dt>

6616 (0x19D8)
</dt> <dt>



O serviço de log não pode excluir o arquivo de log ou o contêiner do sistema de arquivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**limite de contêiner de log de erros \_ \_ \_ \_ excedido**
</dt> <dd> <dl> <dt>

6617 (0x19D9)
</dt> <dt>



O serviço de log atingiu o máximo de contêineres permitidos alocados para um arquivo de log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**\_ \_ início do log \_ de erros do \_ log**
</dt> <dd> <dl> <dt>

6618 (0x19DA)
</dt> <dt>



O serviço de log tentou ler ou gravar para trás após o início do log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**política de log de erros \_ \_ \_ já \_ instalada**
</dt> <dd> <dl> <dt>

6619 (0x19DB)
</dt> <dt>



Não foi possível instalar a política de log porque já existe uma política do mesmo tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**política de log de erros \_ \_ \_ não \_ instalada**
</dt> <dd> <dl> <dt>

6620 (0x19DC)
</dt> <dt>



A política de log em questão não foi instalada no momento da solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**política de log de erros \_ \_ \_ inválida**
</dt> <dd> <dl> <dt>

6621 (0x19DD)
</dt> <dt>



O conjunto de políticas instalado no log é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**\_conflito de \_ política de log de erros \_**
</dt> <dd> <dl> <dt>

6622 (0x19DE)
</dt> <dt>



Uma política no log em questão impediu a conclusão da operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**\_final do \_ \_ arquivo fixado do log \_ de erros**
</dt> <dd> <dl> <dt>

6623 (0x19DF)
</dt> <dt>



O espaço de log não pode ser recuperado porque o log está fixado pela parte final do arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**registro de log de erros não \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

6624 (0x19E0)
</dt> <dt>



O registro de log não é um registro no arquivo de log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**registros de log de erros \_ \_ \_ reservados \_ inválidos**
</dt> <dd> <dl> <dt>

6625 (0x19E1)
</dt> <dt>



O número de registros de log reservados ou o ajuste do número de registros de log reservados é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**\_espaço reservado para log de erros \_ \_ \_ inválido**
</dt> <dd> <dl> <dt>

6626 (0x19E2)
</dt> <dt>



O espaço de log reservado ou o ajuste do espaço de log é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**cauda do log de erros \_ \_ \_ inválida**
</dt> <dd> <dl> <dt>

6627 (0x19E3)
</dt> <dt>



Uma parte final ou uma base de arquivo novo ou existente do log ativo é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**LOG de erros \_ \_ completo**
</dt> <dd> <dl> <dt>

6628 (0x19E4)
</dt> <dt>



Espaço de log esgotado.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERRO \_ não foi possível \_ \_ redimensionar o \_ log**
</dt> <dd> <dl> <dt>

6629 (0x19E5)
</dt> <dt>



Não foi possível definir o log para o tamanho solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**LOG de erros \_ \_ multiplexado**
</dt> <dd> <dl> <dt>

6630 (0x19E6)
</dt> <dt>



O log é multiplexado, não é permitida nenhuma gravação direta no log físico.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**LOG de erros \_ \_ dedicado**
</dt> <dd> <dl> <dt>

6631 (0x19E7)
</dt> <dt>



A operação falhou porque o log é um log dedicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**\_ \_ arquivo morto \_ de log de erros não está \_ em \_ andamento**
</dt> <dd> <dl> <dt>

6632 (0x19E8)
</dt> <dt>



A operação requer um contexto de arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**\_ \_ arquivo de log \_ de erros em \_ andamento**
</dt> <dd> <dl> <dt>

6633 (0x19E9)
</dt> <dt>



O arquivamento de log está em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**LOG de erros \_ \_ efêmero**
</dt> <dd> <dl> <dt>

6634 (0x19EA)
</dt> <dt>



A operação requer um log não efêmero, mas o log é efêmero.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**LOG de erros \_ \_ sem \_ \_ contêineres suficientes**
</dt> <dd> <dl> <dt>

6635 (0x19EB)
</dt> <dt>



O log deve ter pelo menos dois contêineres para que possa ser lido ou gravado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**cliente de log de erros \_ \_ \_ já \_ registrado**
</dt> <dd> <dl> <dt>

6636 (0x19EC)
</dt> <dt>



Um cliente de log já foi registrado no fluxo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**cliente de log de erros \_ \_ \_ não \_ registrado**
</dt> <dd> <dl> <dt>

6637 (0x19ED)
</dt> <dt>



Um cliente de log não foi registrado no fluxo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**\_ \_ \_ manipulador completo do log \_ de erros em \_ andamento**
</dt> <dd> <dl> <dt>

6638 (0x19EE)
</dt> <dt>



Uma solicitação já foi feita para lidar com a condição completa de log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**\_ \_ \_ falha ao ler contêiner de log de erros \_**
</dt> <dd> <dl> <dt>

6639 (0x19EF)
</dt> <dt>



O serviço de log encontrou um erro ao tentar ler um contêiner de log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**\_ \_ \_ falha na gravação do contêiner de log de erros \_**
</dt> <dd> <dl> <dt>

6640 (0x19F0)
</dt> <dt>



O serviço de log encontrou um erro ao tentar gravar em um contêiner de log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**\_ \_ \_ falha na abertura do contêiner de log de erros \_**
</dt> <dd> <dl> <dt>

6641 (0x19F1)
</dt> <dt>



O serviço de log encontrou um erro ao tentar abrir um contêiner de log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**Estado do contêiner do log de erros \_ \_ \_ \_ inválido**
</dt> <dd> <dl> <dt>

6642 (0x19F2)
</dt> <dt>



O serviço de log encontrou um estado de contêiner inválido ao tentar uma ação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**Estado do log de erros \_ \_ \_ inválido**
</dt> <dd> <dl> <dt>

6643 (0x19F3)
</dt> <dt>



O serviço de log não está no estado correto para executar uma ação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**LOG de erros \_ \_ fixado**
</dt> <dd> <dl> <dt>

6644 (0x19F4)
</dt> <dt>



O espaço de log não pode ser recuperado porque o log está fixado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**\_ \_ \_ falha na liberação de metadados do log de erros \_**
</dt> <dd> <dl> <dt>

6645 (0x19F5)
</dt> <dt>



Falha na liberação de metadados do log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**\_ \_ segurança inconsistente no log de erros \_**
</dt> <dd> <dl> <dt>

6646 (0x19F6)
</dt> <dt>



A segurança no log e seus contêineres são inconsistentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**\_ \_ \_ falha ao liberar o log \_ de erros**
</dt> <dd> <dl> <dt>

6647 (0x19F7)
</dt> <dt>



Os registros foram anexados ao log ou as alterações de reserva foram feitas, mas o log não pôde ser liberado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**Reserva de log de erros \_ \_ fixa \_**
</dt> <dd> <dl> <dt>

6648 (0x19F8)
</dt> <dt>



O log é fixado devido a uma reserva que consome a maior parte do espaço de log. Libere alguns registros reservados para disponibilizar espaço.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERRO \_ de \_ transação inválida**
</dt> <dd> <dl> <dt>

6700 (0x1A2C)
</dt> <dt>



O identificador de transação associado a esta operação não é válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**transação de erro \_ \_ não \_ ativa**
</dt> <dd> <dl> <dt>

6701 (0x1A2D)
</dt> <dt>



A operação solicitada foi feita no contexto de uma transação que não está mais ativa.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**solicitação de transação de erro \_ \_ \_ \_ inválida**
</dt> <dd> <dl> <dt>

6702 (0x1A2E)
</dt> <dt>



A operação solicitada não é válida no objeto de transação em seu estado atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**transação de erro \_ \_ não \_ solicitada**
</dt> <dd> <dl> <dt>

6703 (0x1A2F)
</dt> <dt>



O chamador chamou uma API de resposta, mas a resposta não é esperada porque a TM não emitiu a solicitação correspondente ao chamador.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**transação de erro \_ \_ já \_ anulada**
</dt> <dd> <dl> <dt>

6704 (0x1A30)
</dt> <dt>



É tarde demais para executar a operação solicitada, já que a transação já foi anulada.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**transação de erro \_ \_ já \_ confirmada**
</dt> <dd> <dl> <dt>

6705 (0x1A31)
</dt> <dt>



É tarde demais para executar a operação solicitada, já que a transação já foi confirmada.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERRO \_ de \_ inicialização de TM \_ falhou**
</dt> <dd> <dl> <dt>

6706 (0x1A32)
</dt> <dt>



O Gerenciador de transações não pôde ser inicializado com êxito. Não há suporte para operações transacionadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERRO \_ \_ somente leitura de RESOURCEMANAGER \_**
</dt> <dd> <dl> <dt>

6707 (0x1A33)
</dt> <dt>



O ResourceManager especificado não fez alterações ou atualizações no recurso sob esta transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**transação de erro \_ \_ não \_ unida**
</dt> <dd> <dl> <dt>

6708 (0x1A34)
</dt> <dt>



O Gerenciador de recursos tentou preparar uma transação que não ingressou com êxito.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**a \_ transação de erro \_ superior \_ existe**
</dt> <dd> <dl> <dt>

6709 (0x1A35)
</dt> <dt>



O objeto de transação já tem uma inscrição superior e o chamador tentou uma operação que teria criado um novo superior. Apenas uma única inscrição superior é permitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERRO \_ o \_ protocolo CRM \_ já \_ existe**
</dt> <dd> <dl> <dt>

6710 (0x1A36)
</dt> <dt>



O RM tentou registrar um protocolo que já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**\_ \_ falha na propagação da transação de erro \_**
</dt> <dd> <dl> <dt>

6711 (0x1A37)
</dt> <dt>



Falha na tentativa de propagar a transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERRO \_ do \_ protocolo CRM \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

6712 (0x1A38)
</dt> <dt>



O protocolo de propagação solicitado não foi registrado como um CRM.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**\_buffer de \_ \_ Marshall inválido de transação \_ de erro**
</dt> <dd> <dl> <dt>

6713 (0x1A39)
</dt> <dt>



O buffer passado para PushTransaction ou PullTransaction não está em um formato válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**a \_ transação atual do erro \_ \_ não é \_ válida**
</dt> <dd> <dl> <dt>

6714 (0x1A3A)
</dt> <dt>



O contexto de transação atual associado ao thread não é um identificador válido para um objeto de transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**transação de erro \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

6715 (0x1A3B)
</dt> <dt>



Não foi possível abrir o objeto de transação especificado porque ele não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERRO \_ RESOURCEMANAGER \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

6716 (0x1A3C)
</dt> <dt>



Não foi possível abrir o objeto ResourceManager especificado, pois ele não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**inscrição de erro \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

6717 (0x1A3D)
</dt> <dt>



Não foi possível abrir o objeto de inscrição especificado, pois ele não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERRO de \_ TRANSacçãomanager \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

6718 (0x1A3E)
</dt> <dt>



Não foi possível abrir o objeto TransactionManager especificado porque ele não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERRO de \_ TRANSacçãomanager \_ não \_ online**
</dt> <dd> <dl> <dt>

6719 (0x1A3F)
</dt> <dt>



O objeto especificado não pôde ser criado ou aberto, pois seu TransactionManager associado não está online. O TransactionManager deve ser colocado totalmente online chamando RecoverTransactionManager para recuperar no final de seu arquivo de log antes que os objetos em seus namespaces de transação ou ResourceManager possam ser abertos. Além disso, os erros de gravação de registros em seu arquivo de log podem fazer com que um TransactionManager fique offline.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERRO de \_ colisão de \_ nome de recuperação de transacionador \_ \_**
</dt> <dd> <dl> <dt>

6720 (0x1A40)
</dt> <dt>



O TransactionManager especificado não pôde criar os objetos contidos em seu arquivo de log no namespace OB. Portanto, o TransactionManager não pôde ser recuperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**transação de erro \_ \_ não \_ raiz**
</dt> <dd> <dl> <dt>

6721 (0x1A41)
</dt> <dt>



Não foi possível concluir a chamada para criar uma inscrição superior neste objeto de transação, pois o objeto de transação especificado para a inscrição é uma ramificação subordinada da transação. Somente a raiz da transação pode ser inscrito em como uma superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**objeto de transação de erro \_ \_ \_ expirado**
</dt> <dd> <dl> <dt>

6722 (0x1A42)
</dt> <dt>



Como o Gerenciador de transações associado ou o Gerenciador de recursos foi fechado, o identificador não é mais válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**resposta de transação de erro \_ \_ \_ não \_ listada**
</dt> <dd> <dl> <dt>

6723 (0x1A43)
</dt> <dt>



A operação especificada não pôde ser executada nesta inscrição superior, pois a inscrição não foi criada com a resposta de conclusão correspondente no NotificationMask.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**registro de transação de erro \_ \_ \_ muito \_ longo**
</dt> <dd> <dl> <dt>

6724 (0x1A44)
</dt> <dt>



A operação especificada não pôde ser executada, pois o registro que seria registrado era muito longo. Isso pode ocorrer devido a duas condições: há muitas inlistagens nessa transação ou a RecoveryInformation combinada que está sendo registrada em nome dessas inlistagens é muito longa.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERRO \_ de \_ transação implícita \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

6725 (0x1A45)
</dt> <dt>



Não há suporte para a transação implícita.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**integridade da transação de erro \_ \_ \_ violada**
</dt> <dd> <dl> <dt>

6726 (0x1A46)
</dt> <dt>



O Gerenciador de transações do kernel teve que anular ou esquecer a transação porque ela bloqueou o progresso.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERRO de \_ \_ incompatibilidade de identidade do TransactionManager \_**
</dt> <dd> <dl> <dt>

6727 (0x1A47)
</dt> <dt>



A identidade do transacionator fornecida não corresponde à que foi registrada no arquivo de log do TransactionManager.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERRO \_ RM \_ não pode \_ ser \_ congelado \_ para \_ instantâneo**
</dt> <dd> <dl> <dt>

6728 (0x1A48)
</dt> <dt>



Esta operação de instantâneo não pode continuar porque um Gerenciador de recursos transacionais não pode ser congelado em seu estado atual. Tente novamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**a \_ transação de erro \_ deve \_ WRITETHROUGH**
</dt> <dd> <dl> <dt>

6729 (0x1A49)
</dt> <dt>



A transação não pode ser enlistada com o EnlistmentMask especificado, pois a transação já concluiu a fase de preprepare. Para garantir a exatidão, o ResourceManager deve alternar para um modo de write-through e deixar de armazenar em cache os dados nessa transação. A inscreveção para apenas fases de transação subsequentes ainda pode ter sucesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**transação de erro \_ \_ não \_ superior**
</dt> <dd> <dl> <dt>

6730 (0x1A4A)
</dt> <dt>



A transação não tem uma inscrição superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**ERRO \_ de \_ dano heurístico \_ possível**
</dt> <dd> <dl> <dt>

6731 (0x1A4B)
</dt> <dt>



A tentativa de confirmar a transação foi concluída, mas é possível que alguma parte da árvore de transação não tenha sido confirmada com êxito devido à heurística. Portanto, é possível que alguns dados modificados na transação possam não ter sido confirmados, resultando em inconsistência transacional. Se possível, verifique a consistência dos dados associados.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERRO de \_ conflito TRANSacional \_**
</dt> <dd> <dl> <dt>

6800 (0x1A90)
</dt> <dt>



A função tentou usar um nome que está reservado para uso por outra transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERRO \_ RM \_ não \_ ativo**
</dt> <dd> <dl> <dt>

6801 (0x1A91)
</dt> <dt>



O suporte de transação no Gerenciador de recursos especificado não foi iniciado ou foi desligado devido a um erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERRO \_ de \_ metadados do RM \_ corrompidos**
</dt> <dd> <dl> <dt>

6802 (0x1A92)
</dt> <dt>



Os metadados do RM foram corrompidos. O RM não funcionará.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**diretório de erros \_ \_ não \_ RM**
</dt> <dd> <dl> <dt>

6803 (0x1A93)
</dt> <dt>



O diretório especificado não contém um Gerenciador de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**transações de erro \_ \_ sem suporte \_ remoto**
</dt> <dd> <dl> <dt>

6805 (0x1A95)
</dt> <dt>



O servidor ou compartilhamento remoto não oferece suporte a operações de arquivo transacionadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**\_ \_ tamanho inválido de redimensionamento do log de \_ erros \_**
</dt> <dd> <dl> <dt>

6806 (0x1A96)
</dt> <dt>



O tamanho de log solicitado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**o \_ objeto de erro \_ não \_ \_ existe mais**
</dt> <dd> <dl> <dt>

6807 (0x1A97)
</dt> <dt>



O objeto (arquivo, fluxo, link) correspondente ao identificador foi excluído por uma reversão de salvamento de transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**fluxo de erro \_ \_ miniversão \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

6808 (0x1A98)
</dt> <dt>



O arquivo especificado miniversão não foi encontrado para este arquivo transacionado aberto.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**o \_ fluxo de erro \_ miniversão \_ não é \_ válido**
</dt> <dd> <dl> <dt>

6809 (0x1A99)
</dt> <dt>



O arquivo especificado miniversão foi encontrado, mas foi invalidado. A causa mais provável é a reversão do salvamento de uma transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERRO \_ miniversão \_ inacessível \_ da \_ \_ transação especificada**
</dt> <dd> <dl> <dt>

6810 (0x1A9A)
</dt> <dt>



Um miniversão só pode ser aberto no contexto da transação que o criou.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERRO não é possível \_ \_ abrir \_ miniversão \_ com a \_ intenção de modificação \_**
</dt> <dd> <dl> <dt>

6811 (0x1A9B)
</dt> <dt>



Não é possível abrir um miniversão com o acesso de modificação.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERRO não é possível \_ \_ criar \_ mais \_ fluxo \_ MINIVERSIONS**
</dt> <dd> <dl> <dt>

6812 (0x1A9C)
</dt> <dt>



Não é possível criar mais miniversions para esse fluxo.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de versão de arquivo remoto \_**
</dt> <dd> <dl> <dt>

6814 (0x1A9E)
</dt> <dt>



O servidor remoto enviou uma incompatibilidade de número de versão ou FID para um arquivo aberto com transações.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**o \_ identificador de erro \_ não é \_ mais \_ válido**
</dt> <dd> <dl> <dt>

6815 (0x1A9F)
</dt> <dt>



O identificador foi invalidado por uma transação. A causa mais provável é a presença de mapeamento de memória em um arquivo ou um identificador aberto quando a transação foi encerrada ou revertida para o salvamento de pontos.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERRO \_ nenhum \_ \_ metadado TxF**
</dt> <dd> <dl> <dt>

6816 (0x1AA0)
</dt> <dt>



Não há nenhum metadado de transação no arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**corrupção do log de erros \_ \_ \_ detectada**
</dt> <dd> <dl> <dt>

6817 (0x1AA1)
</dt> <dt>



Os dados de log estão corrompidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERRO não é possível \_ \_ recuperar \_ com o \_ identificador \_ aberto**
</dt> <dd> <dl> <dt>

6818 (0x1AA2)
</dt> <dt>



O arquivo não pode ser recuperado porque ainda há um identificador aberto nele.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERRO \_ RM \_ desconectado**
</dt> <dd> <dl> <dt>

6819 (0x1AA3)
</dt> <dt>



O resultado da transação não está disponível porque o Gerenciador de recursos responsável por ele foi desconectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**inscrição de erro \_ \_ não \_ superior**
</dt> <dd> <dl> <dt>

6820 (0x1AA4)
</dt> <dt>



A solicitação foi rejeitada porque a inscrição em questão não é uma inscrição superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**recuperação de erro \_ \_ não \_ necessária**
</dt> <dd> <dl> <dt>

6821 (0x1AA5)
</dt> <dt>



O Gerenciador de recursos transacionais já está consistente. A recuperação não é necessária.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**o \_ RM de erro \_ já \_ foi iniciado**
</dt> <dd> <dl> <dt>

6822 (0x1AA6)
</dt> <dt>



O Gerenciador de recursos transacionais já foi iniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**identidade do arquivo de erro \_ \_ \_ não \_ persistente**
</dt> <dd> <dl> <dt>

6823 (0x1AA7)
</dt> <dt>



O arquivo não pode ser aberto transacionalmente, porque sua identidade depende do resultado de uma transação não resolvida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERRO não é possível \_ \_ interromper a \_ dependência transacional \_**
</dt> <dd> <dl> <dt>

6824 (0x1AA8)
</dt> <dt>



A operação não pode ser executada porque outra transação está dependendo do fato de que essa propriedade não será alterada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERRO não é possível \_ \_ cruzar o \_ limite do RM \_**
</dt> <dd> <dl> <dt>

6825 (0x1AA9)
</dt> <dt>



A operação envolveria um único arquivo com dois gerenciadores de recursos transacionais e, portanto, não é permitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERRO \_ de \_ dir do TxF \_ não \_ vazio**
</dt> <dd> <dl> <dt>

6826 (0x1AAA)
</dt> <dt>



O diretório $Txf deve estar vazio para que essa operação tenha sucesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**\_existem transações INcertas de erro \_ \_**
</dt> <dd> <dl> <dt>

6827 (0x1AAB)
</dt> <dt>



A operação deixaria um Gerenciador de recursos transacionais em um estado inconsistente e, portanto, não é permitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERRO \_ TM \_ volátil**
</dt> <dd> <dl> <dt>

6828 (0x1AAC)
</dt> <dt>



A operação não pôde ser concluída porque o Gerenciador de transações não tem um log.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERRO de \_ reversão do \_ temporizador \_ expirado**
</dt> <dd> <dl> <dt>

6829 (0x1AAD)
</dt> <dt>



Não foi possível agendar uma reversão porque uma reversão agendada anteriormente já foi executada ou foi enfileirada para execução.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERRO \_ de \_ atributo TxF \_ corrompido**
</dt> <dd> <dl> <dt>

6830 (0x1AAE)
</dt> <dt>



O atributo de metadados transacionais no arquivo ou diretório está corrompido e ilegível.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERRO \_ EFS \_ não \_ permitido \_ na \_ transação**
</dt> <dd> <dl> <dt>

6831 (0x1AAF)
</dt> <dt>



A operação de criptografia não pôde ser concluída porque uma transação está ativa.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERRO de \_ abertura TRANSacional \_ \_ não \_ permitido**
</dt> <dd> <dl> <dt>

6832 (0x1AB0)
</dt> <dt>



Este objeto não pode ser aberto em uma transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**\_ \_ falha no crescimento do log de erros \_**
</dt> <dd> <dl> <dt>

6833 (0x1AB1)
</dt> <dt>



Falha ao tentar criar espaço no log do Gerenciador de recursos transacionais. O status de falha foi registrado no log de eventos.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERRO de \_ mapeamento transacionado \_ \_ sem suporte \_ remoto**
</dt> <dd> <dl> <dt>

6834 (0x1AB2)
</dt> <dt>



Não há suporte para o mapeamento de memória (criando uma seção mapeada) de um arquivo remoto em uma transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**os \_ metadados TxF de erro \_ \_ já estão \_ presentes**
</dt> <dd> <dl> <dt>

6835 (0x1AB3)
</dt> <dt>



Os metadados da transação já estão presentes neste arquivo e não podem ser substituídos.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**ERRO \_ de \_ retornos de chamada de escopo de transação \_ \_ não \_ definido**
</dt> <dd> <dl> <dt>

6836 (0x1AB4)
</dt> <dt>



Não foi possível inserir um escopo de transação porque o manipulador de escopo não foi inicializado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**\_ \_ promoção necessária da transação de erro \_**
</dt> <dd> <dl> <dt>

6837 (0x1AB5)
</dt> <dt>



A promoção era necessária para permitir que o Gerenciador de recursos se inscreva, mas a transação foi definida para não permitir.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERRO \_ não é possível \_ executar o \_ arquivo \_ na \_ transação**
</dt> <dd> <dl> <dt>

6838 (0x1AB6)
</dt> <dt>



Este arquivo está aberto para modificação em uma transação não resolvida e pode ser aberto para execução somente por um leitor transacionado.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**transações de erro \_ \_ não \_ congeladas**
</dt> <dd> <dl> <dt>

6839 (0x1AB7)
</dt> <dt>



A solicitação para descongelar transações congeladas foi ignorada porque as transações não tinham sido congeladas anteriormente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERRO \_ ao \_ congelar transação \_ em \_ andamento**
</dt> <dd> <dl> <dt>

6840 (0x1AB8)
</dt> <dt>



As transações não podem ser congeladas porque um congelamento já está em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERRO \_ não \_ volume de instantâneo \_**
</dt> <dd> <dl> <dt>

6841 (0x1AB9)
</dt> <dt>



O volume de destino não é um volume de instantâneo. Esta operação só é válida em um volume montado como um instantâneo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERRO \_ sem \_ pontos \_ de salvamento com \_ \_ arquivos abertos**
</dt> <dd> <dl> <dt>

6842 (0x1ABA)
</dt> <dt>



A operação de salvamento falhou porque os arquivos estão abertos na transação. Isso não é permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**reparo de dados de erro \_ \_ perdido \_**
</dt> <dd> <dl> <dt>

6843 (0x1ABB)
</dt> <dt>



O Windows descobriu corrupção em um arquivo e esse arquivo foi reparado desde então. Pode ter ocorrido perda de dados.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERRO \_ esparso \_ não \_ permitido \_ na \_ transação**
</dt> <dd> <dl> <dt>

6844 (0x1ABC)
</dt> <dt>



A operação esparsa não pôde ser concluída porque uma transação está ativa no arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**incompatibilidade de \_ identidade TM de erro \_ \_**
</dt> <dd> <dl> <dt>

6845 (0x1ABD)
</dt> <dt>



Falha na chamada para criar um objeto TransactionManager porque a identidade TM armazenada no arquivo de log não corresponde à identidade de TM que foi passada como um argumento.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERRO na \_ \_ seção flutuante**
</dt> <dd> <dl> <dt>

6846 (0x1ABE)
</dt> <dt>



Houve uma tentativa de e/s em um objeto de seção que foi flutuado como resultado de uma transação terminando. Não há dados válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERRO \_ não é possível \_ aceitar \_ trabalho transacionado \_**
</dt> <dd> <dl> <dt>

6847 (0x1ABF)
</dt> <dt>



Atualmente, o Gerenciador de recursos transacionais não pode aceitar o trabalho de transação devido a uma condição transitória, como baixa de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERRO \_ não é possível \_ anular \_ Transações**
</dt> <dd> <dl> <dt>

6848 (0x1AC0)
</dt> <dt>



O Gerenciador de recursos transacionais tinha muitos transações pendentes que não puderam ser anulados. O Gerenciador de recursos transacionais foi desligado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERROS \_ de \_ clusters inválidos**
</dt> <dd> <dl> <dt>

6849 (0x1AC1)
</dt> <dt>



A operação não pôde ser concluída devido a clusters inválidos no disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**\_compactação \_ de erro não \_ permitida \_ na \_ transação**
</dt> <dd> <dl> <dt>

6850 (0x1AC2)
</dt> <dt>



Não foi possível concluir a operação de compactação porque uma transação está ativa no arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERRO de \_ volume \_ sujo**
</dt> <dd> <dl> <dt>

6851 (0x1AC3)
</dt> <dt>



A operação não pôde ser concluída porque o volume está sujo. Execute Chkdsk e tente novamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERRO \_ sem \_ \_ rastreamento \_ de link na \_ transação**
</dt> <dd> <dl> <dt>

6852 (0x1AC4)
</dt> <dt>



A operação de rastreamento de link não pôde ser concluída porque uma transação está ativa.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_operação \_ de erro sem \_ suporte \_ na \_ transação**
</dt> <dd> <dl> <dt>

6853 (0x1AC5)
</dt> <dt>



Esta operação não pode ser executada em uma transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**identificador de erro \_ expirado \_**
</dt> <dd> <dl> <dt>

6854 (0x1AC6)
</dt> <dt>



O identificador não está mais corretamente associado à sua transação. Ele pode ter sido aberto em um Gerenciador de recursos transacionais que foi subsequentemente forçado a reiniciar. Feche a alça e abra uma nova.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**transação de erro \_ \_ não \_ listada**
</dt> <dd> <dl> <dt>

6855 (0x1AC7)
</dt> <dt>



A operação especificada não pôde ser executada porque o Gerenciador de recursos não está inscrito na transação.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERRO \_ CTX \_ WINSTATION \_ nome \_ inválido**
</dt> <dd> <dl> <dt>

7001 (0x1B59)
</dt> <dt>



O nome de sessão especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERRO \_ CTX \_ \_ PD inválido**
</dt> <dd> <dl> <dt>

7002 (0x1B5A)
</dt> <dt>



O driver de protocolo especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERRO \_ CTX \_ PD \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

7003 (0x1B5B)
</dt> <dt>



O driver de protocolo especificado não foi encontrado no caminho do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERRO \_ CTX \_ WD \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

7004 (0x1B5C)
</dt> <dt>



O driver de conexão de terminal especificado não foi encontrado no caminho do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERRO \_ CTX \_ não é possível \_ criar a \_ entrada de EventLog \_**
</dt> <dd> <dl> <dt>

7005 (0x1B5D)
</dt> <dt>



Não foi possível criar uma chave do registro para o log de eventos para esta sessão.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERRO \_ de \_ \_ colisão de nome de serviço CTX \_**
</dt> <dd> <dl> <dt>

7006 (0x1B5E)
</dt> <dt>



Já existe um serviço com o mesmo nome no sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERRO \_ CTX \_ fechar \_ pendente**
</dt> <dd> <dl> <dt>

7007 (0x1B5F)
</dt> <dt>



Uma operação de fechamento está pendente na sessão.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERRO \_ CTX \_ \_ OUTBUF**
</dt> <dd> <dl> <dt>

7008 (0x1B60)
</dt> <dt>



Não há buffers de saída livres disponíveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERRO \_ CTX de \_ modem \_ inf \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

7009 (0x1B61)
</dt> <dt>



O MODEM. O arquivo INF não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERRO de \_ CTX de \_ \_ modem inválido**
</dt> <dd> <dl> <dt>

7010 (0x1B62)
</dt> <dt>



O nome do modem não foi encontrado em MODEM. INF.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**erro \_ CTX \_ \_ erro de resposta do modem \_**
</dt> <dd> <dl> <dt>

7011 (0x1B63)
</dt> <dt>



O modem não aceitou o comando enviado a ele. Verifique se o nome do modem configurado corresponde ao modem conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERRO \_ CTX \_ \_ tempo limite de resposta de modem \_**
</dt> <dd> <dl> <dt>

7012 (0x1B64)
</dt> <dt>



O modem não respondeu ao comando enviado a ele. Verifique se o modem está corretamente conectado e ligado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERRO \_ CTX \_ resposta de modem \_ \_ sem \_ portadora**
</dt> <dd> <dl> <dt>

7013 (0x1B65)
</dt> <dt>



A detecção da operadora falhou ou a portadora foi descartada devido à desconexão.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERRO \_ CTX \_ resposta do modem \_ \_ sem \_ Tom de sinal de**
</dt> <dd> <dl> <dt>

7014 (0x1B66)
</dt> <dt>



Tom de discagem não detectado dentro do tempo necessário. Verifique se o cabo do telefone está corretamente conectado e funcional.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERRO \_ CTX \_ resposta de modem \_ \_ ocupada**
</dt> <dd> <dl> <dt>

7015 (0x1B67)
</dt> <dt>



Sinal de ocupado detectado no site remoto no retorno de chamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERRO \_ CTX \_ de \_ resposta de modem \_**
</dt> <dd> <dl> <dt>

7016 (0x1B68)
</dt> <dt>



Voz detectada no site remoto no retorno de chamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**erro \_ CTX erro \_ td \_**
</dt> <dd> <dl> <dt>

7017 (0x1B69)
</dt> <dt>



Erro do driver de transporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERRO \_ CTX \_ WINSTATION \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

7022 (0x1B6E)
</dt> <dt>



Não é possível encontrar a sessão especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERRO \_ CTX \_ WINSTATION \_ já \_ existe**
</dt> <dd> <dl> <dt>

7023 (0x1B6F)
</dt> <dt>



O nome de sessão especificado já está em uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERRO \_ CTX \_ WINSTATION \_ Busy**
</dt> <dd> <dl> <dt>

7024 (0x1B70)
</dt> <dt>



A tarefa que você está tentando fazer não pode ser concluída porque Serviços de Área de Trabalho Remota está ocupada no momento. Tente novamente em alguns minutos. Outros usuários ainda devem ser capazes de fazer logon.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERRO \_ CTX \_ \_ modo de vídeo defeituoso \_**
</dt> <dd> <dl> <dt>

7025 (0x1B71)
</dt> <dt>



Foi feita uma tentativa de conexão a uma sessão cujo modo de vídeo não é suportado pelo cliente atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERRO \_ CTX \_ gráficos \_ inválido**
</dt> <dd> <dl> <dt>

7035 (0x1B7B)
</dt> <dt>



O aplicativo tentou habilitar o modo gráfico do DOS. Não há suporte para o modo gráfico do DOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERRO \_ CTX \_ logon \_ desabilitado**
</dt> <dd> <dl> <dt>

7037 (0x1B7D)
</dt> <dt>



O privilégio de logon interativo foi desabilitado. Contate o administrador.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERRO \_ CTX \_ não \_ console**
</dt> <dd> <dl> <dt>

7038 (0x1B7E)
</dt> <dt>



A operação solicitada pode ser executada somente no console do sistema. Isso é geralmente o resultado de um driver ou DLL do sistema que requer acesso direto ao console.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERRO \_ CTX \_ \_ tempo limite de consulta do cliente \_**
</dt> <dd> <dl> <dt>

7040 (0x1B80)
</dt> <dt>



Falha do cliente ao responder à mensagem de conexão do servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERRO \_ CTX \_ \_ desconexão do console**
</dt> <dd> <dl> <dt>

7041 (0x1B81)
</dt> <dt>



Não há suporte para a desconexão da sessão de console.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERRO \_ CTX \_ console \_ Connect**
</dt> <dd> <dl> <dt>

7042 (0x1B82)
</dt> <dt>



Não há suporte para a reconexão de uma sessão desconectada ao console.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERRO de \_ CTX de \_ sombra \_ negado**
</dt> <dd> <dl> <dt>

7044 (0x1B84)
</dt> <dt>



A solicitação para controlar outra sessão remotamente foi negada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERRO \_ CTX \_ WINSTATION \_ acesso \_ negado**
</dt> <dd> <dl> <dt>

7045 (0x1B85)
</dt> <dt>



O acesso à sessão solicitado foi negado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERRO \_ CTX \_ com \_ WD inválido**
</dt> <dd> <dl> <dt>

7049 (0x1B89)
</dt> <dt>



O driver de conexão de terminal especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERRO \_ de \_ sombra de CTX \_ inválido**
</dt> <dd> <dl> <dt>

7050 (0x1B8A)
</dt> <dt>



A sessão solicitada não pode ser controlada remotamente. Isso pode ocorrer porque a sessão está desconectada ou não tem um usuário conectado no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERRO \_ de \_ sombra de CTX \_ desabilitado**
</dt> <dd> <dl> <dt>

7051 (0x1B8B)
</dt> <dt>



A sessão solicitada não está configurada para permitir o controle remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERRO \_ CTX \_ \_ licença \_ de cliente em \_ uso**
</dt> <dd> <dl> <dt>

7052 (0x1B8C)
</dt> <dt>



Sua solicitação para se conectar a este Terminal Server foi rejeitada. Seu número de licença de cliente do Terminal Server está sendo usado por outro usuário no momento. Entre em contato com o administrador do sistema para obter um número de licença exclusivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERRO \_ CTX \_ licença de cliente \_ \_ não \_ definida**
</dt> <dd> <dl> <dt>

7053 (0x1B8D)
</dt> <dt>



Sua solicitação para se conectar a este Terminal Server foi rejeitada. Seu número de licença de cliente Terminal Server não foi inserido para esta cópia do cliente de Terminal Server. Entre em contato com o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**a \_ licença CTX de erro \_ \_ não \_ está disponível**
</dt> <dd> <dl> <dt>

7054 (0x1B8E)
</dt> <dt>



O número de conexões a este computador é limitado e todas as conexões estão em uso no momento. Tente se conectar mais tarde ou contate o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERRO \_ de \_ cliente de licença CTX \_ \_ inválido**
</dt> <dd> <dl> <dt>

7055 (0x1B8F)
</dt> <dt>



O cliente que você está usando não está licenciado para usar este sistema. Sua solicitação de logon foi negada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERRO \_ CTX \_ licença \_ expirada**
</dt> <dd> <dl> <dt>

7056 (0x1B90)
</dt> <dt>



A licença do sistema expirou. Sua solicitação de logon foi negada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERRO \_ CTX \_ sombra \_ não \_ está em execução**
</dt> <dd> <dl> <dt>

7057 (0x1B91)
</dt> <dt>



O controle remoto não pôde ser encerrado porque a sessão especificada não está sendo controlada remotamente no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERRO \_ CTX \_ sombra \_ encerrada \_ por \_ alteração de modo \_**
</dt> <dd> <dl> <dt>

7058 (0x1B92)
</dt> <dt>



O controle remoto do console foi encerrado porque o modo de exibição foi alterado. Não há suporte para a alteração do modo de exibição em uma sessão de controle remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**contagem de ativação de erro \_ \_ \_ excedida**
</dt> <dd> <dl> <dt>

7059 (0x1B93)
</dt> <dt>



A ativação já foi redefinida para o número máximo de vezes para essa instalação. Seu temporizador de ativação não será limpo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERRO \_ CTX \_ WINSTATIONS \_ desabilitado**
</dt> <dd> <dl> <dt>

7060 (0x1B94)
</dt> <dt>



Os logons remotos estão desabilitados no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERRO \_ CTX \_ nível de criptografia \_ \_ necessário**
</dt> <dd> <dl> <dt>

7061 (0x1B95)
</dt> <dt>



Você não tem o nível de criptografia adequado para acessar esta sessão.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERRO \_ \_ de sessão CTX \_ em \_ uso**
</dt> <dd> <dl> <dt>

7062 (0x1B96)
</dt> <dt>



O usuário% s \\ \\ % s está conectado atualmente a este computador. Somente o usuário atual ou um administrador pode fazer logon neste computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERRO \_ CTX \_ não \_ forçar \_ logoff**
</dt> <dd> <dl> <dt>

7063 (0x1B97)
</dt> <dt>



O usuário% s \\ \\ % s já está conectado ao console deste computador. Você não tem permissão para fazer logon neste momento. Para resolver esse problema, entre em contato com% s \\ \\ % s e faça logoff.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERRO \_ de \_ restrição de conta do CTX \_**
</dt> <dd> <dl> <dt>

7064 (0x1B98)
</dt> <dt>



Não é possível fazer logon devido a uma restrição de conta.


</dt> </dl> </dd> <dt>

<span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**erro \_ de \_ erro de protocolo RDP \_**
</dt> <dd> <dl> <dt>

7065 (0x1B99)
</dt> <dt>



O componente de protocolo RDP %2 detectou um erro no fluxo de protocolo e desconectou o cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERRO \_ CTX \_ CDM \_ Connect**
</dt> <dd> <dl> <dt>

7066 (0x1B9A)
</dt> <dt>



O serviço de mapeamento de unidade de cliente conectou-se à conexão de terminal.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERRO \_ CTX \_ CDM \_ Disconnect**
</dt> <dd> <dl> <dt>

7067 (0x1B9B)
</dt> <dt>



O serviço de mapeamento de unidade do cliente foi desconectado da conexão de terminal.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**erro de erro de \_ \_ camada de segurança CTX \_ \_**
</dt> <dd> <dl> <dt>

7068 (0x1B9C)
</dt> <dt>



A camada de segurança Terminal Server detectou um erro no fluxo de protocolo e desconectou o cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERRO \_ de \_ sessões TS incompatíveis \_**
</dt> <dd> <dl> <dt>

7069 (0x1B9D)
</dt> <dt>



A sessão de destino é incompatível com a sessão atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**erro erro de \_ \_ \_ subsistema de vídeo TS \_**
</dt> <dd> <dl> <dt>

7070 (0x1B9E)
</dt> <dt>



O Windows não pode se conectar à sua sessão porque ocorreu um problema no subsistema de vídeo do Windows. Tente se conectar novamente mais tarde ou contate o administrador do servidor para obter assistência.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**sequência de API de erro do FRS \_ \_ inválida \_ \_**
</dt> <dd> <dl> <dt>

8001 (0x1F41)
</dt> <dt>



A API do serviço de replicação de arquivo foi chamada incorretamente.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**\_serviço de \_ inicialização de erro do FRS \_**
</dt> <dd> <dl> <dt>

8002 (0x1F42)
</dt> <dt>



Não é possível iniciar o serviço de replicação de arquivo.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**erro do FRS ao \_ \_ parar o \_ serviço**
</dt> <dd> <dl> <dt>

8003 (0x1F43)
</dt> <dt>



O serviço de replicação de arquivo não pode ser interrompido.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_ \_ API interna de erro do FRS \_**
</dt> <dd> <dl> <dt>

8004 (0x1F44)
</dt> <dt>



A API do serviço de replicação de arquivo encerrou a solicitação. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**\_erro \_ interno do FRS**
</dt> <dd> <dl> <dt>

8005 (0x1F45)
</dt> <dt>



O serviço de replicação de arquivo encerrou a solicitação. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**\_comunicação do \_ serviço de erro do FRS \_**
</dt> <dd> <dl> <dt>

8006 (0x1F46)
</dt> <dt>



O serviço de replicação de arquivo não pode ser contatado. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**erro de FRS \_ \_ insuficiente \_ priv**
</dt> <dd> <dl> <dt>

8007 (0x1F47)
</dt> <dt>



O serviço de replicação de arquivo não pode atender à solicitação porque o usuário tem privilégios insuficientes. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**\_autenticação de erro do FRS \_**
</dt> <dd> <dl> <dt>

8008 (0x1F48)
</dt> <dt>



O serviço de replicação de arquivo não pode atender à solicitação porque o RPC autenticado não está disponível. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**o FRS \_ Err \_ pai é \_ insuficiente \_ priv**
</dt> <dd> <dl> <dt>

8009 (0x1F49)
</dt> <dt>



O serviço de replicação de arquivo não pode atender à solicitação porque o usuário tem privilégios insuficientes no controlador de domínio. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**\_autenticação do \_ pai de erro do FRS \_**
</dt> <dd> <dl> <dt>

8010 (0x1F4A)
</dt> <dt>



O serviço de replicação de arquivo não pode atender à solicitação porque o RPC autenticado não está disponível no controlador de domínio. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**\_erro \_ de FRS filho \_ para \_ pai \_**
</dt> <dd> <dl> <dt>

8011 (0x1F4B)
</dt> <dt>



O serviço de replicação de arquivo não pode se comunicar com o serviço de replicação de arquivo no controlador de domínio. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS \_ \_ de Err pai \_ para \_ filho \_**
</dt> <dd> <dl> <dt>

8012 (0x1F4C)
</dt> <dt>



O serviço de replicação de arquivo no controlador de domínio não pode se comunicar com o serviço de replicação de arquivo neste computador. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**\_preenchimento do \_ SYSVOL de erro do FRS \_**
</dt> <dd> <dl> <dt>

8013 (0x1F4D)
</dt> <dt>



O serviço de replicação de arquivo não pode popular o volume do sistema devido a um erro interno. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**\_ \_ \_ tempo limite de preenchimento de SYSVOL de erro do FRS \_**
</dt> <dd> <dl> <dt>

8014 (0x1F4E)
</dt> <dt>



O serviço de replicação de arquivo não pode popular o volume do sistema devido a um tempo limite interno. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**o \_ SYSVOL de erro do FRS \_ \_ está \_ ocupado**
</dt> <dd> <dl> <dt>

8015 (0x1F4F)
</dt> <dt>



O serviço de replicação de arquivo não pode processar a solicitação. O volume do sistema está ocupado com uma solicitação anterior.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**\_rebaixar SYSVOL de erro do FRS \_ \_**
</dt> <dd> <dl> <dt>

8016 (0x1F50)
</dt> <dt>



O serviço de replicação de arquivo não pode parar de replicar o volume do sistema devido a um erro interno. O log de eventos pode ter mais informações.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**\_parâmetro de \_ \_ serviço inválido \_ do FRS Err**
</dt> <dd> <dl> <dt>

8017 (0x1F51)
</dt> <dt>



O serviço de replicação de arquivo detectou um parâmetro inválido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro do sistema](system-error-codes.md)
</dt> </dl>

 

 




