---
title: Erros de log e recuperação em funções no Active Directory Domain Services
description: Este tópico lista os valores de retorno de erro de log e recuperação para funções no Active Directory Domain Services.
ms.assetid: b927073a-8bbc-45d4-b9d3-25f3aa6c6f53
ms.tgt_platform: multiple
keywords:
- Active Directory o registro em log e erros de recuperação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6fba921a63eb399d6ed4f44ef8569ed05370403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105751015"
---
# <a name="logging-and-recovery-errors-in-functions-in-active-directory-domain-services"></a>Erros de log e recuperação em funções no Active Directory Domain Services

Este tópico lista os valores de retorno de erro de log e recuperação para funções no Active Directory Domain Services.



| Valor                                | Descrição                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **hrLogFileCorrupt**                 | O arquivo de log está danificado.                                                                                                         |
| **hrNoBackupDirectory**              | Nenhum diretório de backup foi fornecido.                                                                                                   |
| **hrBackupDirectoryNotEmpty**        | O diretório de backup não está vazio.                                                                                               |
| **hrBackupInProgress**               | O backup está ativo.                                                                                                                |
| **hrMissingPreviousLogFile**         | Um arquivo de log para o ponto de verificação está ausente.                                                                                        |
| **hrLogWriteFail**                   | Não é possível gravar no arquivo de log.                                                                                                 |
| **hrBadLogVersion**                  | A versão do arquivo de log não é compatível com a versão do banco de dados do serviço de diretório do Windows NT/Windows 2000 (NTDS). |
| **hrInvalidLogSequence**             | O carimbo de data/hora no próximo log não corresponde ao esperado.                                                                 |
| **hrLoggingDisabled**                | O log não está ativo.                                                                                                           |
| **hrLogBufferTooSmall**              | O buffer de log é muito pequeno para ser recuperado.                                                                                     |
| **hrLogSequenceEnd**                 | O número máximo de arquivos de log foi excedido.                                                                               |
| **hrNoBackup**                       | Não há backup em andamento.                                                                                                  |
| **hrInvalidBackupSequence**          | A chamada de backup está fora de sequência.                                                                                              |
| **hrBackupNotAllowedYet**            | Não é possível executar um backup agora.                                                                                                  |
| **hrDeleteBackupFileFail**           | Não é possível excluir o arquivo de backup.                                                                                                |
| **hrMakeBackupDirectoryFail**        | Não é possível criar um diretório temporário de backup.                                                                                     |
| **hrInvalidBackup**                  | Um backup incremental não pode ser executado quando o log circular está habilitado.                                                      |
| **hrRecoveredWithErrors**            | Foram encontrados erros durante o processo de reparo.                                                                               |
| **hrMissingLogFile**                 | O arquivo de log atual está faltando.                                                                                                 |
| **hrLogDiskFull**                    | O disco de log está cheio.                                                                                                            |
| **hrBadLogSignature**                | Um arquivo de log está danificado.                                                                                                           |
| **hrBadDbSignature**                 | Um arquivo de banco de dados está danificado.                                                                                                      |
| **hrBadCheckpointSignature**         | Um arquivo de ponto de verificação está danificado.                                                                                                    |
| **hrCheckpointCorrupt**              | Não foi possível encontrar um arquivo de ponto de verificação ou ele está danificado.                                                                       |
| **hrDatabaseInconsistent**           | O banco de dados está danificado.                                                                                                         |
| **hrConsistentTimeMismatch**         | Há uma incompatibilidade na última hora consistente do banco de dados.                                                                      |
| **hrPatchFileMismatch**              | O arquivo de patch não é gerado a partir deste backup.                                                                                |
| **hrRestoreLogTooLow**               | O número de log inicial é muito baixo para a restauração.                                                                              |
| **hrRestoreLogTooHigh**              | O número de log inicial é muito alto para a restauração.                                                                             |
| **hrGivenLogFileHasBadSignature**    | O arquivo de log baixado da fita está danificado.                                                                                |
| **hrGivenLogFileIsNotContiguous**    | Não é possível localizar um arquivo de log obrigatório depois que a fita foi baixada.                                                               |
| **hrMissingRestoreLogFiles**         | Os dados não são totalmente restaurados porque alguns arquivos de log estão ausentes.                                                               |
| **hrExistingLogFileHasBadSignature** | O arquivo de log no caminho do arquivo de log está danificado.                                                                                    |
| **hrExistingLogFileIsNotContiguous** | Não é possível localizar um arquivo de log obrigatório no caminho do arquivo de log.                                                                        |
| **hrMissingFullBackup**              | O banco de dados perdeu um backup completo anterior antes do backup incremental.                                                        |
| **hrBadBackupDatabaseSize**          | O tamanho do banco de dados de backup deve ser um múltiplo de 4000 (4096 bytes).                                                                |
| **hrTermInProgress**                 | O banco de dados está sendo desligado.                                                                                                 |
| **hrFeatureNotAvailable**            | O recurso não está disponível.                                                                                                    |
| **hrInvalidName**                    | O nome é inválido.                                                                                                             |
| **hrInvalidParameter**               | O parâmetro é inválido.                                                                                                        |
| **hrColumnNull**                     | O valor da coluna é nulo.                                                                                                 |
| **hrBufferTruncated**                | O buffer é muito pequeno para os dados.                                                                                                |
| **hrDatabaseAttached**               | O banco de dados já está anexado.                                                                                                |
| **hrInvalidDatabaseId**              | A ID do banco de dados é inválida.                                                                                                      |
| **hrOutOfMemory**                    | O computador está sem memória.                                                                                                   |
| **hrOutOfDatabaseSpace**             | O banco de dados atingiu o tamanho máximo de 16 GB.                                                                              |
| **hrOutOfCursors**                   | Sem cursores de tabela.                                                                                                            |
| **hrOutOfBuffers**                   | Sem buffers de página de banco de dados.                                                                                                    |
| **hrTooManyIndexes**                 | Há muitos índices.                                                                                                      |
| **hrTooManyKeys**                    | Há muitas colunas em um índice.                                                                                          |
| **hrRecordDeleted**                  | O registro foi excluído.                                                                                                     |
| **hrReadVerifyFailure**              | Ocorreu um erro de verificação de leitura.                                                                                              |
| **hrOutOfFileHandles**               | Falta de identificadores de arquivos.                                                                                                             |
| **hrDiskIO**                         | Ocorreu um erro de e/s de disco.                                                                                                       |
| **hrInvalidPath**                    | O caminho para o arquivo é inválido.                                                                                                 |
| **hrRecordTooBig**                   | O registro excedeu o tamanho máximo.                                                                                        |
| **hrTooManyOpenDatabases**           | Há muitos bancos de dados abertos.                                                                                               |
| **hrInvalidDatabase**                | O arquivo não é um arquivo de banco de dados.                                                                                                 |
| **hrNotInitialized**                 | O banco de dados ainda não foi chamado.                                                                                                 |
| **hrAlreadyInitialized**             | O banco de dados já foi chamado.                                                                                                 |
| **hrFileAccessDenied**               | Não é possível acessar o arquivo.                                                                                                       |
| **hrBufferTooSmall**                 | O buffer é muito pequeno.                                                                                                         |
| **hrSeekNotEqual**                   | O SeekLE ou o SeekGE não pode encontrar uma correspondência exata.                                                                              |
| **hrTooManyColumns**                 | Há muitas colunas definidas.                                                                                              |
| **hrContainerNotEmpty**              | O contêiner não está vazio.                                                                                                      |
| **hrInvalidFilename**                | O nome do arquivo é inválido.                                                                                                         |
| **hrInvalidBookmark**                | O indicador é inválido.                                                                                                         |
| **hrColumnInUse**                    | A coluna é usada em um índice.                                                                                                  |
| **hrInvalidBufferSize**              | O buffer de dados não corresponde ao tamanho da coluna.                                                                                  |
| **hrColumnNotUpdatable**             | Não é possível definir o valor da coluna.                                                                                                  |
| **hrIndexInUse**                     | O índice está em uso.                                                                                                             |
| **hrNullKeyDisallowed**              | Chaves nulas não são permitidas em um índice.                                                                                           |
| **hrNotInTransaction**               | A operação deve ser executada dentro de uma transação.                                                                                      |
| **hrNoIdleActivity**                 | Não ocorreu nenhuma atividade ociosa.                                                                                                       |
| **hrTooManyActiveUsers**             | Há muitos usuários de banco de dados ativos.                                                                                        |
| **hrInvalidCountry**                 | O código de país ou região não é conhecido ou é inválido.                                                                    |
| **hrInvalidLanguageId**              | A ID do idioma não é conhecida ou é inválida.                                                                               |
| **hrInvalidCodePage**                | A página de código não é conhecida ou é inválida.                                                                                 |
| **hrNoWriteLock**                    | Não há nenhum bloqueio de gravação no nível de transação 0.                                                                                   |
| **hrColumnSetNull**                  | O valor da coluna é definido como nulo.                                                                                                 |
| **hrVersionStoreOutOfMemory**        | O lMaxVerPages foi excedido (somente XJET).                                                                                           |
| **hrCurrencyStackOutOfMemory**       | Sem cursores.                                                                                                                  |
| **hrOutOfSessions**                  | Fora de sessões.                                                                                                                 |
| **hrWriteConflict**                  | Falha no bloqueio de gravação devido a um bloqueio de gravação pendente.                                                                          |
| **hrTransTooDeep**                   | As transações estão aninhadas muito profundamente.                                                                                          |
| **hrInvalidSesid**                   | O identificador de sessão é inválido.                                                                                                   |
| **hrSessionWriteConflict**           | Outra sessão tem uma versão particular da página.                                                                               |
| **hrInTransaction**                  | A operação não é permitida em uma transação.                                                                               |
| **hrDatabaseDuplicate**              | O banco de dados já existe.                                                                                                     |
| **hrDatabaseInUse**                  | O banco de dados está em uso.                                                                                                          |
| **hrDatabaseNotFound**               | O banco de dados não existe.                                                                                                     |
| **hrDatabaseInvalidName**            | O nome do banco de dados é inválido.                                                                                                    |
| **hrDatabaseInvalidPages**           | O número de páginas é inválido.                                                                                                  |
| **hrDatabaseCorrupted**              | O arquivo de banco de dados está danificado ou não pode ser encontrado.                                                                          |
| **hrDatabaseLocked**                 | O banco de dados está bloqueado.                                                                                                          |
| **hrTableEmpty**                     | Uma tabela vazia foi aberta.                                                                                                       |
| **hrTableLocked**                    | A tabela está bloqueada.                                                                                                             |
| **hrTableDuplicate**                 | A tabela já existe.                                                                                                        |
| **hrTableInUse**                     | Não é possível bloquear a tabela porque ela já está em uso.                                                                           |
| **hrObjectNotFound**                 | A tabela ou o objeto não existe.                                                                                              |
| **hrCannotRename**                   | Não é possível renomear o arquivo temporário.                                                                                             |
| **hrDensityInvalid**                 | A densidade do arquivo/índice é inválida.                                                                                               |
| **hrTableNotEmpty**                  | Não é possível definir o índice clusterizado.                                                                                            |
| **hrInvalidTableId**                 | A ID da tabela é inválida.                                                                                                         |
| **hrTooManyOpenTables**              | Não é possível abrir mais tabelas.                                                                                                  |
| **hrIllegalOperation**               | Não há suporte para a operação em tabelas.                                                                                        |
| **hrObjectDuplicate**                | O nome da tabela ou do objeto já está sendo usado.                                                                                  |
| **hrInvalidObject**                  | O objeto é inválido para a operação.                                                                                             |
| **hrIndexCantBuild**                 | Não é possível criar um índice clusterizado.                                                                                               |
| **hrIndexHasPrimary**                | O índice primário já está definido.                                                                                            |
| **hrIndexDuplicate**                 | O índice já está definido.                                                                                                    |
| **hrIndexNotFound**                  | O índice não existe.                                                                                                        |
| **hrIndexMustStay**                  | Não é possível excluir um índice clusterizado.                                                                                              |
| **hrIndexInvalidDef**                | A definição do índice é inválida.                                                                                                 |
| **hrIndexHasClustered**              | O índice clusterizado já está definido.                                                                                          |
| **hrCreateIndexFailed**              | Não é possível criar o índice porque ocorreu um erro ao criar uma tabela.                                                     |
| **hrTooManyOpenIndexes**             | Fora dos blocos de descrição de índice.                                                                                                 |
| **hrColumnLong**                     | O valor da coluna é muito longo.                                                                                                    |
| **hrColumnDoesNotFit**               | O campo não será ajustado no registro.                                                                                            |
| **hrNullInvalid**                    | O valor não pode ser nulo.                                                                                                        |
| **hrColumnIndexed**                  | Não é possível excluir porque a coluna está indexada.                                                                                  |
| **hrColumnTooBig**                   | O comprimento do campo excede o comprimento máximo de 255 bytes.                                                                 |
| **hrColumnNotFound**                 | Não é possível localizar a coluna.                                                                                                       |
| **hrColumnDuplicate**                | O campo já está definido.                                                                                                    |
| **hrColumn2ndSysMaint**              | Apenas uma coluna de incremento automático ou de versão é permitida por tabela.                                                                  |
| **hrInvalidColumnType**              | O tipo de dados da coluna é inválido.                                                                                                 |
| **hrColumnMaxTruncated**             | A coluna foi truncada porque excedeu o comprimento máximo de 255 bytes.                                                    |
| **hrColumnCannotIndex**              | Não é possível indexar uma coluna de valor longo.                                                                                             |
| **hrTaggedNotNULL**                  | As colunas marcadas não podem ser nulas.                                                                                                   |
| **hrNoCurrentIndex**                 | A entrada é inválida sem um índice atual.                                                                                    |
| **hrKeyIsMade**                      | A chave foi concluída.                                                                                                             |
| **hrBadColumnId**                    | A ID da coluna está incorreta.                                                                                                      |
| **hrBadItagSequence**                | Há um identificador de instância inadequado para uma coluna com valores.                                                                     |
| **hrCannotBeTagged**                 | O incremento automático e a versão não podem ter valores de multivalor.                                                                                 |
| **hrRecordNotFound**                 | Não é possível localizar a chave.                                                                                                          |
| **hrNoCurrentRecord**                | A moeda não está em um registro.                                                                                                 |
| **hrRecordClusteredChanged**         | Uma chave clusterizada não pode ser alterada.                                                                                               |
| **hrKeyDuplicate**                   | A chave já existe.                                                                                                          |
| **hrAlreadyPrepared**                | A entrada atual já foi copiada ou desmarcada.                                                                            |
| **hrKeyNotMade**                     | Nenhuma chave foi feita.                                                                                                                 |
| **hrUpdateNotPrepared**              | A atualização não foi preparada.                                                                                                         |
| **hrwrnDataHasChanged**              | Os dados foram alterados.                                                                                                                |
| **hrerrDataHasChanged**              | A operação foi abandonada porque os dados foram alterados.                                                                            |
| **hrKeyChanged**                     | Movido para uma nova chave.                                                                                                              |
| **hrTooManySorts**                   | Há muitos processos de classificação.                                                                                               |
| **hrInvalidOnSort**                  | Uma operação que é inválida ocorreu na classificação.                                                                               |
| **hrTempFileOpenError**              | Não é possível abrir o arquivo temporário.                                                                                               |
| **hrTooManyAttachedDatabases**       | Há muitos bancos de dados abertos.                                                                                               |
| **hrDiskFull**                       | O disco está cheio.                                                                                                                |
| **hrPermissionDenied**               | Permissão negada.                                                                                                            |
| **hrFileNotFound**                   | Não é possível localizar o arquivo.                                                                                                         |
| **hrFileOpenReadOnly**               | O arquivo de banco de dados é somente leitura.                                                                                                  |
| **hrAfterInitialization**            | Não é possível restaurar após a inicialização.                                                                                          |
| **hrLogCorrupted**                   | Os arquivos de log do banco de dados estão danificados.                                                                                              |
| **hrInvalidOperation**               | A operação é inválida.                                                                                                        |
| **hrAccessDenied**                   | O acesso foi negado.                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Êxito](success.md)
</dt> <dt>

[Erros de backup no Active Directory Domain Services](backup-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Erros do sistema no Active Directory Domain Services](system-errors-in-active-directory-domain-services.md)
</dt> <dt>

[Erros do Gerenciador de diretórios](directory-manager-errors.md)
</dt> <dt>

[Valores de retorno para funções no Active Directory Domain Services](return-values-for-functions-in-active-directory-domain-services.md)
</dt> </dl>

 

 




