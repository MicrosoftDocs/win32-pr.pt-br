---
title: Erros de registro em log e recuperação em funções Active Directory Domain Services
description: Este tópico lista os valores de retorno de erro de log e recuperação para funções Active Directory Domain Services.
ms.assetid: b927073a-8bbc-45d4-b9d3-25f3aa6c6f53
ms.tgt_platform: multiple
keywords:
- AD de erros de registro em log e recuperação do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b267b359b5244fddc0e8a9b2ddfbfb5d6e5f9ab0a7e647683d44759f8a7261b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186583"
---
# <a name="logging-and-recovery-errors-in-functions-in-active-directory-domain-services"></a>Erros de registro em log e recuperação em funções Active Directory Domain Services

Este tópico lista os valores de retorno de erro de log e recuperação para funções Active Directory Domain Services.



| Valor                                | Descrição                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **hrLogFileCorrupt**                 | O arquivo de log está danificado.                                                                                                         |
| **hrNoBackupDirectory**              | Nenhum diretório de backup foi dado.                                                                                                   |
| **hrBackupDirectoryNotEmpty**        | O diretório de backup não está vazio.                                                                                               |
| **hrBackupInProgress**               | O backup está ativo.                                                                                                                |
| **hrMissingPreviousLogFile**         | Um arquivo de log para o ponto de verificação está ausente.                                                                                        |
| **hrLogWriteFail**                   | Não é possível gravar no arquivo de log.                                                                                                 |
| **hrBadLogVersion**                  | A versão do arquivo de log não é compatível com a versão do banco de dados Windows NT/Windows 2000 Directory Service (NTDS). |
| **hrInvalidLogSequence**             | O carimbo de data/hora no próximo log não é igual ao esperado.                                                                 |
| **hrLoggingDisabled**                | O log não está ativo.                                                                                                           |
| **hrLogBufferTooSmall**              | O buffer de log é muito pequeno para ser recuperado.                                                                                     |
| **hrLogSequenceEnd**                 | O número máximo de arquivos de log foi excedido.                                                                               |
| **hrNoBackup**                       | Não há nenhum backup em andamento.                                                                                                  |
| **hrInvalidBackupSequence**          | A chamada de backup está fora de sequência.                                                                                              |
| **hrBackupNotAllowedYet**            | Não é possível executar um backup agora.                                                                                                  |
| **hrDeleteBackupFileFail**           | Não é possível excluir o arquivo de backup.                                                                                                |
| **hrMakeBackupDirectoryFail**        | Não é possível fazer um diretório temporário de backup.                                                                                     |
| **hrInvalidBackup**                  | Um backup incremental não pode ser executado quando o log circular está habilitado.                                                      |
| **hrRecoveredWithErrors**            | Erros foram encontrados durante o processo de reparo.                                                                               |
| **hrMissingLogFile**                 | O arquivo de log atual está faltando.                                                                                                 |
| **hrLogDiskFull**                    | O disco de log está cheio.                                                                                                            |
| **hrBadLogSignature**                | Um arquivo de log está danificado.                                                                                                           |
| **hrBadDbSignature**                 | Um arquivo de banco de dados está danificado.                                                                                                      |
| **hrBadCheckpointSignature**         | Um arquivo de ponto de verificação está danificado.                                                                                                    |
| **hrCheckpointCorrupt**              | Um arquivo de ponto de verificação não pôde ser encontrado ou está danificado.                                                                       |
| **hrDatabaseInconsistent**           | O banco de dados está danificado.                                                                                                         |
| **hrConsistentTimeMismatch**         | Há uma incompatibilidade na última hora consistente do banco de dados.                                                                      |
| **hrPatchFileMismatch**              | O arquivo de patch não é gerado com esse backup.                                                                                |
| **hrRestoreLogTooLow**               | O número de log inicial é muito baixo para a restauração.                                                                              |
| **hrRestoreLogTooHigh**              | O número de log inicial é muito alto para a restauração.                                                                             |
| **hrGivenLogFileHasBadSignature**    | O arquivo de log baixado da fita está danificado.                                                                                |
| **hrGivenLogFileIsNotContiguous**    | Não é possível encontrar um arquivo de log obrigatório depois que a fita foi baixada.                                                               |
| **hrMissingRestoreLogFiles**         | Os dados não são totalmente restaurados porque alguns arquivos de log estão ausentes.                                                               |
| **hrExistingLogFileHasBadSignature** | O arquivo de log no caminho do arquivo de log está danificado.                                                                                    |
| **hrExistingLogFileIsNotContiguous** | Não é possível encontrar um arquivo de log obrigatório no caminho do arquivo de log.                                                                        |
| **hrMissingFullBackup**              | O banco de dados perdeu um backup completo anterior antes do backup incremental.                                                        |
| **hrBadBackupDatabaseSize**          | O tamanho do banco de dados de backup deve ser um múltiplo de 4000 (4096 bytes).                                                                |
| **hrTermInProgress**                 | O banco de dados está sendo desligado.                                                                                                 |
| **hrFeatureNotAvailable**            | O recurso não está disponível.                                                                                                    |
| **hrInvalidName**                    | O nome é inválido.                                                                                                             |
| **hrInvalidParameter**               | O parâmetro é inválido.                                                                                                        |
| **hrColumnNull**                     | O valor da coluna é nulo.                                                                                                 |
| **hrBufferTruncated**                | O buffer é muito pequeno para dados.                                                                                                |
| **hrDatabaseAttached**               | O banco de dados já está anexado.                                                                                                |
| **hrInvalidDatabaseId**              | A ID do banco de dados é inválida.                                                                                                      |
| **hrOutOfMemory**                    | O computador está sem memória.                                                                                                   |
| **hrOutOfDatabaseSpace**             | O banco de dados atingiu o tamanho máximo de 16 GB.                                                                              |
| **hrOutOfCursors**                   | Cursores fora da tabela.                                                                                                            |
| **hrOutOfBuffers**                   | Buffers de página fora do banco de dados.                                                                                                    |
| **hrTooManyIndexes**                 | Há muitos índices.                                                                                                      |
| **hrTooManyKeys**                    | Há muitas colunas em um índice.                                                                                          |
| **hrRecordDeleted**                  | O registro foi excluído.                                                                                                     |
| **hrReadVerifyFailure**              | Ocorreu um erro de verificação de leitura.                                                                                              |
| **hrOutOfFileHandles**               | Falta de identificadores de arquivos.                                                                                                             |
| **hrDiskIO**                         | Ocorreu um erro de E/S de disco.                                                                                                       |
| **hrInvalidPath**                    | O caminho para o arquivo é inválido.                                                                                                 |
| **hrRecordTooBig**                   | O registro excedeu o tamanho máximo.                                                                                        |
| **hrTooManyOpenDatabases**           | Há muitos bancos de dados abertos.                                                                                               |
| **hrInvalidDatabase**                | O arquivo não é um arquivo de banco de dados.                                                                                                 |
| **hrNotInitialized**                 | O banco de dados ainda não foi chamado.                                                                                                 |
| **hrAlreadyInitialized**             | O banco de dados já foi chamado.                                                                                                 |
| **hrFileAccessDenied**               | Não é possível acessar o arquivo.                                                                                                       |
| **hrBufferTooSmall**                 | O buffer é muito pequeno.                                                                                                         |
| **hrSeekNotEqual**                   | SeekLE ou SeekGE não podem encontrar uma combinação exata.                                                                              |
| **hrTooManyColumns**                 | Há muitas colunas definidas.                                                                                              |
| **hrContainerNotEmpty**              | O contêiner não está vazio.                                                                                                      |
| **hrInvalidFilename**                | O nome do arquivo é inválido.                                                                                                         |
| **hrInvalidBookmark**                | O indicador é inválido.                                                                                                         |
| **hrColumnInUse**                    | A coluna é usada em um índice.                                                                                                  |
| **hrInvalidBufferSize**              | O buffer de dados não é igual ao tamanho da coluna.                                                                                  |
| **hrColumnNotUpdatable**             | Não é possível definir o valor da coluna.                                                                                                  |
| **hrIndexInUse**                     | O índice está em uso.                                                                                                             |
| **hrNullKeyDisallowed**              | Chaves nulas não são permitidas em um índice.                                                                                           |
| **hrNotInTransaction**               | A operação deve ser executada dentro de uma transação.                                                                                      |
| **hrNoIdleActivity**                 | Nenhuma atividade ociosa ocorreu.                                                                                                       |
| **hrTooManyActiveUsers**             | Há muitos usuários de banco de dados ativos.                                                                                        |
| **hrInvalidCountry**                 | O código de país ou região não é conhecido ou é inválido.                                                                    |
| **hrInvalidLanguageId**              | A ID do idioma não é conhecida ou é inválida.                                                                               |
| **hrInvalidCodePage**                | A página de código não é conhecida ou é inválida.                                                                                 |
| **hrNoWriteLock**                    | Não há nenhum bloqueio de gravação no nível de transação 0.                                                                                   |
| **hrColumnSetNull**                  | O valor da coluna é definido como nulo.                                                                                                 |
| **hrVersionStoreOutOfMemory**        | O lMaxVerPages excedeu (somente XJET).                                                                                           |
| **hrCurrencyStackOutOfMemory**       | Fora dos cursores.                                                                                                                  |
| **hrOutOfSessions**                  | Fora das sessões.                                                                                                                 |
| **hrWriteConflict**                  | Falha no bloqueio de gravação devido a um bloqueio de gravação pendente.                                                                          |
| **hrTransTooDeep**                   | As transações são aninhadas muito profundamente.                                                                                          |
| **hrInvalidSesid**                   | O alça de sessão é inválido.                                                                                                   |
| **hrSessionWriteConflict**           | Outra sessão tem uma versão privada da página.                                                                               |
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
| **hrDensityInvalid**                 | A densidade de arquivo/índice é inválida.                                                                                               |
| **hrTableNotEmpty**                  | Não é possível definir o índice cluster.                                                                                            |
| **hrInvalidTableId**                 | A ID da tabela é inválida.                                                                                                         |
| **hrTooManyOpenTables**              | Não é possível abrir mais tabelas.                                                                                                  |
| **hrIagalOperation**               | Não há suporte para a operação em tabelas.                                                                                        |
| **hrObjectDuplicate**                | O nome da tabela ou objeto já está sendo usado.                                                                                  |
| **hrInvalidObject**                  | O objeto é inválido para a operação.                                                                                             |
| **hrIndexInaBuild**                 | Não é possível criar um índice cluster.                                                                                               |
| **hrIndexHasPrimary**                | O índice primário já está definido.                                                                                            |
| **hrIndexDuplicate**                 | O índice já está definido.                                                                                                    |
| **hrIndexNotFound**                  | O índice não existe.                                                                                                        |
| **hrIndexMustStay**                  | Não é possível excluir um índice clusterado.                                                                                              |
| **hrIndexInvalidDef**                | A definição de índice é ilegal.                                                                                                 |
| **hrIndexHasClustered**              | O índice cluster já está definido.                                                                                          |
| **hrCreateIndexFailed**              | Não é possível criar o índice porque ocorreu um erro ao criar uma tabela.                                                     |
| **hrTooManyOpenIndexes**             | Blocos de descrição fora do índice.                                                                                                 |
| **hrColumnLong**                     | O valor da coluna é muito longo.                                                                                                    |
| **hrColumnDoesNotFit**               | O campo não se ajustará ao registro.                                                                                            |
| **hrNullInvalid**                    | O valor não pode ser nulo.                                                                                                        |
| **hrColumnIndexed**                  | Não é possível excluir porque a coluna está indexada.                                                                                  |
| **hrColumnTooBig**                   | O comprimento do campo excede o comprimento máximo de 255 bytes.                                                                 |
| **hrColumnNotFound**                 | Não é possível encontrar a coluna.                                                                                                       |
| **hrColumnDuplicate**                | O campo já está definido.                                                                                                    |
| **hrColumn2ndSysMaint**              | Apenas uma coluna de incremento automático ou versão é permitida por tabela.                                                                  |
| **hrInvalidColumnType**              | O tipo de dados de coluna é inválido.                                                                                                 |
| **hrColumnMaxTruncated**             | A coluna foi truncada porque excedeu o comprimento máximo de 255 bytes.                                                    |
| **hrColumnCannotIndex**              | Não é possível indexar uma coluna de valor longo.                                                                                             |
| **hrTaggedNotNULL**                  | Colunas marcadas não podem ser nulas.                                                                                                   |
| **hrNoCurrentIndex**                 | A entrada é inválida sem um índice atual.                                                                                    |
| **hrKeyIsKeyIsKey**                      | A chave está concluída.                                                                                                             |
| **hrBadColumnId**                    | A ID da coluna está incorreta.                                                                                                      |
| **hrBadItagSequence**                | Há um identificador de instância ruim para uma coluna com vários valores.                                                                     |
| **hrCannotBeTagged**                 | AutoIncrement e Version não podem ter vários valores.                                                                                 |
| **hrRecordNotFound**                 | Não é possível encontrar a chave.                                                                                                          |
| **hrNoCurrentRecord**                | A moeda não está em um registro.                                                                                                 |
| **hrRecordClusteredChanged**         | Uma chave clusterada não pode ser alterada.                                                                                               |
| **hrKeyDuplicate**                   | A chave já existe.                                                                                                          |
| **hrAlreadyPrepared**                | A entrada atual já foi copiada ou limpa.                                                                            |
| **hrKeyNotNot**                     | Nenhuma chave foi feita.                                                                                                                 |
| **hrUpdateNotPrepared**              | A atualização não foi preparada.                                                                                                         |
| **hrwrnDataHasChanged**              | Os dados foram alterados.                                                                                                                |
| **mutrDataHasChanged**              | A operação foi abandonada porque os dados foram alterados.                                                                            |
| **hrKeyChanged**                     | Movido para uma nova chave.                                                                                                              |
| **hrTooManySorts**                   | Há muitos processos de classificação.                                                                                               |
| **hrInvalidOnSort**                  | Uma operação inválida ocorreu na classificação.                                                                               |
| **hrTempFileOpenError**              | Não é possível abrir o arquivo temporário.                                                                                               |
| **hrTooManyAttachedDatabases**       | Há muitos bancos de dados abertos.                                                                                               |
| **hrDiskFull**                       | O disco está cheio.                                                                                                                |
| **hrPermissionDenied**               | Permissão negada.                                                                                                            |
| **hrFileNotFound**                   | Não é possível localizar o arquivo.                                                                                                         |
| **hrFileOpenReadOnly**               | O arquivo de banco de dados é somente leitura.                                                                                                  |
| **hrAfterInitialization**            | Não é possível restaurar após a inicialização.                                                                                          |
| **hrLogCorrupted**                   | Os arquivos de log do banco de dados estão danificados.                                                                                              |
| **hrInvalidOperation**               | A operação é inválida.                                                                                                        |
| **hrAccessDenied**                   | Acesso negado.                                                                                                                |



 

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

 

 




