---
description: 'Saiba mais sobre: códigos de erro do mecanismo de armazenamento extensível'
title: Códigos de erro do mecanismo de armazenamento extensível
TOCTitle: Extensible Storage Engine Error Codes
ms:assetid: 7534370d-aed6-4980-b1ca-c3d063507e31
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269297(v=EXCHG.10)
ms:contentKeyID: 32765589
ms.date: 09/22/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9de4bd8157e0b7210315352ba0760293a892f087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798522"
---
# <a name="extensible-storage-engine-error-codes"></a>Códigos de erro do mecanismo de armazenamento extensível


_**Aplica-se a:** Windows | Windows Server_

## <a name="extensible-storage-engine-error-codes"></a>Códigos de erro do mecanismo de armazenamento extensível

Os códigos de erro (sinalizadores) a seguir são usados por funções na API do mecanismo de armazenamento extensível.

Um valor de [JET_ERR](./jet-err.md) de zero deve ser interpretado como êxito.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Êxito</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess 0</p></td>
<td><p>A função foi bem-sucedida.</p></td>
</tr>
</tbody>
</table>


Um valor [JET_ERR](./jet-err.md) maior que zero deve ser interpretado como um aviso.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Warnings</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnRemainingVersions<br />
321</p></td>
<td><p>O repositório de versão ainda está ativo. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnUniqueKey<br />
345</p></td>
<td><p>Uma busca em um índice não exclusivo gerou uma chave exclusiva. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeparateLongValue<br />
406</p></td>
<td><p>Uma coluna de banco de dados é um valor longo separado. Esse erro é retornado pelo Gerenciador de registros.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnExistingLogFileHasBadSignature<br />
558</p></td>
<td><p>O arquivo de log existente tem uma assinatura inadequada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnExistingLogFileIsNotContiguous<br />
559</p></td>
<td><p>O arquivo de log existente não é contíguo.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSkipThisRecord<br />
564</p></td>
<td><p>Esse erro é somente para uso interno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTargetInstanceRunning<br />
578</p></td>
<td><p>O TargetInstance especificado para a restauração está em execução.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseRepaired<br />
595</p></td>
<td><p>A corrupção do banco de dados foi reparada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull<br />
1004</p></td>
<td><p>A coluna tem um valor <strong>nulo</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated<br />
1006</p></td>
<td><p>O buffer é muito pequeno para os dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDatabaseAttached<br />
1007</p></td>
<td><p>O banco de dados já está anexado.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSortOverflow<br />
1009</p></td>
<td><p>A classificação que está sendo tentada não tem memória suficiente para ser concluída.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnSeekNotEqual<br />
1039</p></td>
<td><p>Uma correspondência exata não foi encontrada durante uma busca.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnRecordFoundGreater<br />
JET_wrnSeekNotEqual</p></td>
<td><p>Uma correspondência exata não foi encontrada durante uma busca. Esse erro é retornado pelo Gerenciador de registros.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnRecordFoundLess<br />
JET_wrnSeekNotEqual</p></td>
<td><p>Uma correspondência exata não foi encontrada durante uma busca. Esse erro é retornado pelo Gerenciador de registros.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoErrorInfo<br />
1055</p></td>
<td><p>Não há informações de erro estendidas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnNoIdleActivity<br />
1058</p></td>
<td><p>Não ocorreu nenhuma atividade ociosa.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnNoWriteLock<br />
1067</p></td>
<td><p>Não há um bloqueio de gravação no nível de transação 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSetNull<br />
1068</p></td>
<td><p>A coluna está definida como um valor <strong>nulo</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableEmpty<br />
1301</p></td>
<td><p>Uma tabela vazia foi aberta.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnTableInUseBySystem<br />
1327</p></td>
<td><p>A limpeza do sistema tem um cursor aberto na tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCorruptIndexDeleted<br />
1415</p></td>
<td><p>O índice desatualizado deve ser removido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated<br />
1512</p></td>
<td><p>O comprimento máximo é muito grande e foi truncado.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCopyLongValue<br />
1520</p></td>
<td><p>Um valor de BLOB foi movido do registro para um armazenamento separado de BLOBs grandes.</p>
<p><strong>Observação</strong> Esse erro é somente para uso interno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSkipped<br />
1531</p></td>
<td><p>Os valores da coluna não foram retornados porque a ID da coluna correspondente ou o membro <em>itagSequence</em> da estrutura de <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a> solicitada para enumeração era nulo.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnNotLocal<br />
1532</p></td>
<td><p>Os valores de coluna não foram retornados porque não puderam ser reconstruídos a partir dos dados existentes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMoreTags<br />
1533</p></td>
<td><p>Os valores de coluna existentes não foram solicitados para enumeração.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnTruncated<br />
1534</p></td>
<td><p>O valor da coluna foi truncado no limite de tamanho solicitado durante a enumeração.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnPresent<br />
1535</p></td>
<td><p>Os valores de coluna existem, mas não foram retornados pela solicitação.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSingleValue<br />
1536</p></td>
<td><p>O valor da coluna foi retornado em JET_COLUMNENUM como resultado da JET_bitEnumerateCompressOutput que está sendo definida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnDefault<br />
1537</p></td>
<td><p>O valor da coluna é definido como o valor padrão da coluna.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDataHasChanged<br />
1610</p></td>
<td><p>Os dados foram alterados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnKeyChanged<br />
1618</p></td>
<td><p>Uma nova chave está sendo usada.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly<br />
1813</p></td>
<td><p>O arquivo de banco de dados é somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnIdleFull<br />
1908</p></td>
<td><p>O registro ocioso está cheio.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragAlreadyRunning<br />
2000</p></td>
<td><p>Já havia uma desfragmentação online em execução no banco de dados especificado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragNotRunning<br />
2001</p></td>
<td><p>Uma desfragmentação online não está em execução no banco de dados especificado.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnCallbackNotRegistered<br />
2.100</p></td>
<td><p>Uma função de retorno de chamada não existente teve o registro cancelado.</p></td>
</tr>
</tbody>
</table>


Um valor [JET_ERR](./jet-err.md) menor que zero deve ser interpretado como um erro.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Errors</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_wrnNyi<br />
-1</p></td>
<td><p>A função ainda não foi implementada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRfsFailure<br />
-100</p></td>
<td><p>Falha no simulador de falha de recurso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRfsNotArmed<br />
-101</p></td>
<td><p>O simulador de falha de recurso não foi inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileClose<br />
-102</p></td>
<td><p>Não foi possível fechar o arquivo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfThreads<br />
-103</p></td>
<td><p>Não foi possível iniciar o thread.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyIO<br />
-105</p></td>
<td><p>O sistema está ocupado devido a muitos IOs.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaskDropped<br />
-106</p></td>
<td><p>Não foi possível executar a tarefa assíncrona solicitada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInternalError<br />
-107</p></td>
<td><p>Ocorreu um erro interno fatal.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseBufferDependenciesCorrupted<br />
-255</p></td>
<td><p>As dependências de buffer foram definidas incorretamente e houve uma falha na recuperação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPreviousVersion<br />
-322</p></td>
<td><p>A versão já existia e houve uma falha na recuperação. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageBoundary<br />
-323</p></td>
<td><p>O limite da página foi atingido. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyBoundary<br />
-324</p></td>
<td><p>O limite de chave foi atingido. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadPageLink<br />
-327</p></td>
<td><p>O banco de dados está corrompido. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadBookmark<br />
-328</p></td>
<td><p>O indicador não tem nenhum endereço correspondente no banco de dados. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNTSystemCallFailed<br />
-334</p></td>
<td><p>Falha na chamada para o sistema operacional. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadParentPageLink<br />
-338</p></td>
<td><p>Um banco de dados pai está corrompido. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfSync<br />
-340</p></td>
<td><p>O cache AvailExt não corresponde à árvore B +. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPAvailExtCorrupted<br />
-341</p></td>
<td><p>A árvore de espaço AllAvailExt está corrompida. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSPAvailExtCacheOutOfMemory<br />
-342</p></td>
<td><p>Ocorreu um erro de memória insuficiente ao alocar um nó de cache AvailExt. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSPOwnExtCorrupted<br />
-343</p></td>
<td><p>A árvore de espaço OwnExt está corrompida. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeCorrupted<br />
-344</p></td>
<td><p>O dbtime na página atual é maior que o banco de dados global dbtime. Esse erro é retornado pelo Gerenciador de diretórios.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyTruncated<br />
-346</p></td>
<td><p>Falha ao tentar criar uma chave para uma entrada de índice porque a chave teria sido truncada e a definição de índice não permite truncamento de chave.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyTooBig<br />
-408</p></td>
<td><p>A chave é muito grande. Esse erro é retornado pelo Gerenciador de registros.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLoggedOperation<br />
-500</p></td>
<td><p>A operação registrada em log não pode ser refeita.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogFileCorrupt<br />
-501</p></td>
<td><p>O arquivo de log está corrompido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackupDirectory<br />
-503</p></td>
<td><p>Um diretório de backup não foi fornecido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupDirectoryNotEmpty<br />
-504</p></td>
<td><p>O diretório de backup não está vazio.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress<br />
-505</p></td>
<td><p>O backup já está ativo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress<br />
-506</p></td>
<td><p>Uma restauração está em andamento.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingPreviousLogFile<br />
-509</p></td>
<td><p>O arquivo de log está ausente para o ponto de verificação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogWriteFail<br />
-510</p></td>
<td><p>Houve uma falha ao gravar no arquivo de log.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDisabledDueToRecoveryFailure<br />
-511</p></td>
<td><p>Falha na tentativa de gravar no log após a recuperação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotLogDuringRecoveryRedo<br />
-512</p></td>
<td><p>Falha na tentativa de gravar no log durante a refazer recuperação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogGenerationMismatch<br />
-513</p></td>
<td><p>O nome do arquivo de log não corresponde ao número de geração interno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogVersion<br />
-514</p></td>
<td><p>A versão do arquivo de log não é compatível com a versão do ESE.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogSequence<br />
-515</p></td>
<td><p>O carimbo de data/hora no próximo log não corresponde ao carimbo de data/hora esperado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLoggingDisabled<br />
-516</p></td>
<td><p>O log não está ativo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogBufferTooSmall<br />
-517</p></td>
<td><p>O buffer de log é muito pequeno para recuperação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEnd<br />
-519</p></td>
<td><p>O número máximo do arquivo de log foi excedido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup<br />
-520</p></td>
<td><p>Não há backup em andamento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackupSequence<br />
-521</p></td>
<td><p>A chamada de backup está fora de sequência.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupNotAllowedYet<br />
-523</p></td>
<td><p>Não é possível fazer um backup no momento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDeleteBackupFileFail<br />
-524</p></td>
<td><p>Não foi possível excluir um arquivo de backup.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMakeBackupDirectoryFail<br />
-525</p></td>
<td><p>Não foi possível criar o diretório temporário de backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBackup<br />
-526</p></td>
<td><p>O log circular está habilitado; Não é possível executar um backup incremental.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithErrors<br />
-527</p></td>
<td><p>Os dados foram restaurados com erros.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingLogFile<br />
-528</p></td>
<td><p>O arquivo de log atual está faltando.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogDiskFull<br />
-529</p></td>
<td><p>O disco de log está cheio.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadLogSignature<br />
-530</p></td>
<td><p>Há uma assinatura inadequada para um arquivo de log.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadDbSignature<br />
-531</p></td>
<td><p>Há uma assinatura inadequada para um arquivo de banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadCheckpointSignature<br />
-532</p></td>
<td><p>Há uma assinatura inadequada para um arquivo de ponto de verificação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointCorrupt<br />
-533</p></td>
<td><p>O arquivo de ponto de verificação não foi encontrado ou estava corrompido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingPatchPage<br />
-534</p></td>
<td><p>A página do arquivo de patch do banco de dados não foi encontrada durante a recuperação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadPatchPage<br />
-535</p></td>
<td><p>A página do arquivo de patch do banco de dados não é válida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRedoAbruptEnded<br />
-536</p></td>
<td><p>A refazer abruptamente terminou devido a uma falha repentina durante a leitura de logs do arquivo de log.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadSLVSignature<br />
-537</p></td>
<td><p>Esse sinalizador é reservado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPatchFileMissing<br />
-538</p></td>
<td><p>A restauração complexa detectou que um arquivo de patch de banco de dados está ausente do conjunto de backup.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLogSetMismatch<br />
-539</p></td>
<td><p>O banco de dados não pertence ao conjunto atual de arquivos de log.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseStreamingFileMismatch<br />
-540</p></td>
<td><p>Esse sinalizador é reservado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatch<br />
-541</p></td>
<td><p>O tamanho real do arquivo de log não corresponde ao <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCheckpointFileNotFound<br />
-542</p></td>
<td><p>Não foi possível localizar o arquivo de ponto de verificação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRequiredLogFilesMissing<br />
-543</p></td>
<td><p>Os arquivos de log necessários para recuperação estão ausentes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSoftRecoveryOnBackupDatabase<br />
-544</p></td>
<td><p>Uma recuperação simples está prestes a ser usada em um banco de dados de backup quando uma restauração deve ser usada em vez disso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFileSizeMismatchDatabasesConsistent<br />
-545</p></td>
<td><p>Os bancos de dados foram recuperados, mas o tamanho do arquivo de log usado durante a recuperação não corresponde ao <a href="gg269235(v=exchg.10).md">JET_paramLogFileSize</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSectorSizeMismatch<br />
-546</p></td>
<td><p>O tamanho do setor do arquivo de log não corresponde ao tamanho do setor do volume atual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogSectorSizeMismatchDatabasesConsistent<br />
-547</p></td>
<td><p>Os bancos de dados foram recuperados, mas o tamanho do setor do arquivo de log (usado durante a recuperação) não corresponde ao tamanho do setor do volume atual.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogSequenceEndDatabasesConsistent<br />
-548</p></td>
<td><p>Os bancos de dados foram recuperados, mas todas as gerações de log possíveis na sequência atual foram usadas. Todos os arquivos de log e o arquivo de ponto de verificação devem ser excluídos e o backup dos bancos de dados deve ser feito antes de continuar.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStreamingDataNotLogged<br />
-549</p></td>
<td><p>Houve uma tentativa ilegal de reproduzir uma operação de arquivo de streaming em que os dados não foram registrados. Isso provavelmente é causado por uma tentativa de avanço com o log circular habilitado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseDirtyShutdown<br />
-550</p></td>
<td><p>O banco de dados não foi desligado corretamente. Uma recuperação deve primeiro ser executada para concluir corretamente as operações de banco de dados para o desligamento anterior.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>Este erro está obsoleto e foi substituído por JET_errDatabaseDirtyShutdown.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errConsistentTimeMismatch<br />
-551</p></td>
<td><p>A hora da última consistência do banco de dados não foi correspondida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabasePatchFileMismatch<br />
-552</p></td>
<td><p>O arquivo de patch do banco de dados não é gerado deste backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEndingRestoreLogTooLow<br />
-553</p></td>
<td><p>O número de log inicial é muito baixo para a restauração.</p></td>
</tr>
<tr class="even">
<td><p>JET_errStartingRestoreLogTooHigh<br />
-554</p></td>
<td><p>O número de log inicial é muito alto para a restauração.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errGivenLogFileHasBadSignature<br />
-555</p></td>
<td><p>O arquivo de log de restauração tem uma assinatura inadequada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errGivenLogFileIsNotContiguous<br />
-556</p></td>
<td><p>O arquivo de log de restauração não é contíguo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingRestoreLogFiles<br />
-557</p></td>
<td><p>Alguns arquivos de log de restauração estão ausentes.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFullBackup<br />
-560</p></td>
<td><p>O banco de dados perdeu um backup completo anterior antes de tentar executar um backup incremental.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadBackupDatabaseSize<br />
-561</p></td>
<td><p>O tamanho do banco de dados de backup não é um múltiplo do tamanho da página do banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseAlreadyUpgraded<br />
-562</p></td>
<td><p>A tentativa atual de atualizar um banco de dados foi interrompida porque o banco de dados já está atualizado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIncompleteUpgrade<br />
-563</p></td>
<td><p>O banco de dados foi parcialmente convertido no formato atual. O banco de dados deve ser restaurado do backup.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingCurrentLogFiles<br />
-565</p></td>
<td><p>Alguns arquivos de log atuais estão ausentes para restauração contínua.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDbTimeTooOld<br />
-566</p></td>
<td><p>O dbtime em uma página é menor do que o dbtimeBefore que está no registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDbTimeTooNew<br />
-567</p></td>
<td><p>O dbtime em uma página está antes do dbtimeBefore que está no registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMissingFileToBackup<br />
-569</p></td>
<td><p>Alguns arquivos de patch de log ou banco de dados estavam ausentes durante o backup.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogTornWriteDuringHardRestore<br />
-570</p></td>
<td><p>Foi detectada uma gravação interrompida em um backup definido durante uma restauração complexa.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogTornWriteDuringHardRecovery<br />
-571</p></td>
<td><p>Foi detectada uma gravação interrompida durante uma recuperação complexa (o log não era parte de um conjunto de backup).</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorruptDuringHardRestore<br />
-573</p></td>
<td><p>Corrupção detectada em um conjunto de backup durante uma restauração complexa.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogCorruptDuringHardRecovery<br />
-574</p></td>
<td><p>Foi detectada corrupção durante a recuperação complexa (o log não era parte de um conjunto de backup).</p></td>
</tr>
<tr class="even">
<td><p>JET_errMustDisableLoggingForDbUpgrade<br />
-575</p></td>
<td><p>O registro em log não pode ser habilitado durante a tentativa de atualizar um banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadRestoreTargetInstance<br />
-577</p></td>
<td><p>O TargetInstance que foi especificado para restauração não foi encontrado ou os arquivos de log não coincidem.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecoveredWithoutUndo<br />
-579</p></td>
<td><p>O mecanismo de banco de dados reproduziu com êxito todas as operações no log de transações para executar uma recuperação de falha, mas o chamador optou por interromper a recuperação sem reverter atualizações não confirmadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabasesNotFromSameSnapshot<br />
-580</p></td>
<td><p>Os bancos de dados a serem restaurados não são do mesmo backup de cópia de sombra.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSoftRecoveryOnSnapshot<br />
-581</p></td>
<td><p>Há uma recuperação suave em um banco de dados de um conjunto de backup de cópia de sombra.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationBufferTooSmall<br />
-601</p></td>
<td><p>O buffer de conversão Unicode é muito pequeno.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUnicodeTranslationFail<br />
-602</p></td>
<td><p>Falha na normalização Unicode.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeNormalizationNotSupported<br />
-603</p></td>
<td><p>O sistema operacional não fornece suporte para normalização Unicode e um retorno de chamada de normalização não foi especificado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errExistingLogFileHasBadSignature<br />
-610</p></td>
<td><p>O arquivo de log existente tem uma assinatura inadequada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExistingLogFileIsNotContiguous<br />
-611</p></td>
<td><p>Um arquivo de log existente não é contíguo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure<br />
-612</p></td>
<td><p>Um erro de soma de verificação foi encontrado no arquivo de log durante o backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSLVReadVerifyFailure<br />
-613</p></td>
<td><p>Esse sinalizador é reservado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointDepthTooDeep<br />
-614</p></td>
<td><p>Há muitas gerações pendentes entre o ponto de verificação e a geração atual.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreOfNonBackupDatabase<br />
-615</p></td>
<td><p>Uma recuperação complexa foi tentada em um banco de dados que não era um banco de dados de backup.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidGrbit<br />
-900</p></td>
<td><p>Há um parâmetro grbit inválido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress<br />
-1000</p></td>
<td><p>O encerramento está em andamento.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFeatureNotAvailable<br />
-1001</p></td>
<td><p>Não há suporte para este elemento de API.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName<br />
-1002</p></td>
<td><p>Um nome inválido está sendo usado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter<br />
-1003</p></td>
<td><p>Um parâmetro de API inválido está sendo usado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly<br />
-1008</p></td>
<td><p>Houve uma tentativa de anexar a um arquivo de banco de dados somente leitura para operações de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId<br />
-1010</p></td>
<td><p>Há uma ID de banco de dados inválida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory<br />
-1011</p></td>
<td><p>O sistema está sem memória.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDatabaseSpace<br />
-1012</p></td>
<td><p>O tamanho máximo do banco de dados foi atingido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors<br />
-1013</p></td>
<td><p>A tabela está sem cursores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfBuffers<br />
-1014</p></td>
<td><p>O banco de dados está sem buffers de página.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyIndexes<br />
-1015</p></td>
<td><p>Há muitos índices.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyKeys<br />
-1016</p></td>
<td><p>Há muitas colunas em um índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted<br />
-1017</p></td>
<td><p>O registro foi excluído.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure<br />
-1018</p></td>
<td><p>Há um erro de soma de verificação em uma página de banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPageNotInitialized<br />
-1019</p></td>
<td><p>Há uma página de banco de dados em branco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfFileHandles<br />
-1020</p></td>
<td><p>Não há identificadores de arquivo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO<br />
-1022</p></td>
<td><p>Há um erro de e/s de disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath<br />
-1023</p></td>
<td><p>Há um caminho de arquivo inválido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSystemPath<br />
-1024</p></td>
<td><p>Há um caminho de sistema inválido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLogDirectory<br />
-1025</p></td>
<td><p>Há um diretório de log inválido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig<br />
-1026</p></td>
<td><p>O registro é maior que o tamanho máximo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenDatabases<br />
-1027</p></td>
<td><p>Há muitos bancos de dados abertos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabase<br />
-1028</p></td>
<td><p>Este não é um arquivo de banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized<br />
-1029</p></td>
<td><p>O mecanismo de banco de dados não foi inicializado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAlreadyInitialized<br />
-1030</p></td>
<td><p>O mecanismo de banco de dados já foi inicializado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInitInProgress<br />
-1031</p></td>
<td><p>O mecanismo de banco de dados está sendo inicializado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileAccessDenied<br />
-1032</p></td>
<td><p>O arquivo não pode ser acessado porque o arquivo está bloqueado ou em uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall<br />
-1038</p></td>
<td><p>O buffer é muito pequeno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyColumns<br />
-1040</p></td>
<td><p>Há muitas colunas definidas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errContainerNotEmpty<br />
-1043</p></td>
<td><p>O contêiner não está vazio.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidFilename<br />
-1044</p></td>
<td><p>O nome do arquivo é inválido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark<br />
-1045</p></td>
<td><p>Há um indicador inválido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInUse<br />
-1046</p></td>
<td><p>A coluna usada está em um índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize<br />
-1047</p></td>
<td><p>O buffer de dados não corresponde ao tamanho da coluna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable<br />
-1048</p></td>
<td><p>O valor da coluna não pode ser definido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInUse<br />
-1051</p></td>
<td><p>O índice está em uso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLinkNotSupported<br />
-1052</p></td>
<td><p>O suporte ao link não está disponível.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullKeyDisallowed<br />
-1053</p></td>
<td><p>Chaves nulas não são permitidas em um índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction<br />
-1054</p></td>
<td><p>A operação deve ocorrer em uma transação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyActiveUsers<br />
-1059</p></td>
<td><p>Há muitos usuários de banco de dados ativos</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCountry<br />
-1061</p></td>
<td><p>Há um código de país inválido ou desconhecido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId<br />
-1062</p></td>
<td><p>Há uma ID de idioma inválida ou desconhecida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCodePage<br />
-1063</p></td>
<td><p>Há uma página de código inválida ou desconhecida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLCMapStringFlags<br />
-1064</p></td>
<td><p>Há Sinalizadores inválidos sendo usados para <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreEntryTooBig<br />
-1065</p></td>
<td><p>Houve uma tentativa de criar uma entrada de repositório de versão (RCE) que era maior que um Bucket de versão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemoryAndCleanupTimedOut<br />
-1066</p></td>
<td><p>O repositório de versão está sem memória e a tentativa de limpeza não foi concluída.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errVersionStoreOutOfMemory<br />
-1069</p></td>
<td><p>O repositório de versão está sem memória e uma limpeza já foi tentada).</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotIndex<br />
-1071</p></td>
<td><p>As colunas caução e SLV não podem ser indexadas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotDeleted<br />
-1072</p></td>
<td><p>O registro não foi excluído.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyMempoolEntries<br />
-1073</p></td>
<td><p>Foram solicitadas muitas entradas mempool.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfObjectIDs<br />
-1074</p></td>
<td><p>O banco de dados está fora dos ObjectIDs da árvore B + e, portanto, uma desfragmentação offline deve ser executada para recuperar ObjectIds liberadas ou não utilizadas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfLongValueIDs<br />
-1075</p></td>
<td><p>O contador de ID de valor longo atingiu o valor máximo. Uma desfragmentação offline deve ser executada para recuperar LongValueIDs livres ou não utilizados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfAutoincrementValues<br />
-1076</p></td>
<td><p>O contador de incremento automático atingiu o valor máximo. Uma desfragmentação offline não será capaz de recuperar valores de incremento automáticos gratuitos ou não utilizados).</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfDbtimeValues<br />
-1077</p></td>
<td><p>O contador dbtime atingiu o valor máximo. Uma desfragmentação offline deve ser executada para recuperar valores de dbtime livres ou não utilizados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSequentialIndexValues<br />
-1078</p></td>
<td><p>Um contador de índice sequencial atingiu o valor máximo. Uma desfragmentação offline deve ser executada para recuperar valores de SequentialIndex livres ou não utilizados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode<br />
-1080</p></td>
<td><p>Esta chamada de várias instâncias tem o modo de instância única habilitado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode<br />
-1081</p></td>
<td><p>Esta chamada de instância única tem o modo de várias instâncias habilitado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSystemParamsAlreadySet<br />
-1082</p></td>
<td><p>Os parâmetros do sistema global já foram definidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemPathInUse<br />
-1083</p></td>
<td><p>O caminho do sistema já está sendo usado por outra instância de banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogFilePathInUse<br />
-1084</p></td>
<td><p>O caminho do arquivo de log já está sendo usado por outra instância de banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempPathInUse<br />
-1085</p></td>
<td><p>O caminho para o banco de dados temporário já está sendo usado por outra instância de banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceNameInUse<br />
-1086</p></td>
<td><p>O nome da instância já está em uso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable<br />
-1090</p></td>
<td><p>Esta instância não pode ser usada porque encontrou um erro fatal.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseUnavailable<br />
-1091</p></td>
<td><p>Este banco de dados não pode ser usado porque encontrou um erro fatal.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailableDueToFatalLogDiskFull<br />
-1092</p></td>
<td><p>Esta instância não pode ser usada porque encontrou um erro de disco cheio durante a execução de uma operação (como uma reversão de transação) que não pôde tolerar a falha.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfSessions<br />
-1101</p></td>
<td><p>O banco de dados está fora de sessões.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict<br />
-1102</p></td>
<td><p>Falha no bloqueio de gravação devido à existência de um bloqueio de gravação pendente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransTooDeep<br />
-1103</p></td>
<td><p>As transações estão aninhadas muito profundamente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSesid<br />
-1104</p></td>
<td><p>Identificador de sessão inválido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflictPrimaryIndex<br />
-1105</p></td>
<td><p>Houve uma tentativa de atualização em um índice primário não confirmado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction<br />
-1108</p></td>
<td><p>A operação não é permitida em uma transação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackRequired<br />
-1109</p></td>
<td><p>A transação atual deve ser revertida. Ele não pode ser confirmado e um novo não pode ser iniciado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly<br />
-1110</p></td>
<td><p>Uma transação somente leitura tentou modificar o banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionWriteConflict<br />
-1111</p></td>
<td><p>Houve uma tentativa de substituir o mesmo registro por dois cursores diferentes na mesma sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBigForBackwardCompatibility<br />
-1112</p></td>
<td><p>O registro será muito grande se for representado em um formato de banco de dados de uma versão anterior do Jet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotMaterializeForwardOnlySort<br />
-1113</p></td>
<td><p>Não foi possível criar a tabela temporária devido a parâmetros que entram em conflito com JET_bitTTForwardOnly.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSesidTableIdMismatch<br />
-1114</p></td>
<td><p>O identificador de sessão não pode ser usado com a ID de tabela porque não foi usado para criá-lo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidInstance<br />
-1115</p></td>
<td><p>O identificador de instância é inválido ou se refere a uma instância que foi desligada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadLostFlushVerifyFailure<br />
-1119</p></td>
<td><p>A página do banco de dados lida no disco tinha uma gravação anterior não representada na página. Disponível no Windows 8 e posterior para o cliente e o Windows Server 2012 e posterior para o servidor.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseDuplicate<br />
-1201</p></td>
<td><p>O banco de dados já existe.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse<br />
-1202</p></td>
<td><p>O banco de dados em uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseNotFound<br />
-1203</p></td>
<td><p>Não há nenhum banco de dados desse tipo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidName<br />
-1204</p></td>
<td><p>O nome do banco de dados é inválido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages<br />
-1205</p></td>
<td><p>Há um número inválido de páginas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseCorrupted<br />
-1206</p></td>
<td><p>Há um arquivo que não é de banco de dados ou um banco de dados corrompido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked<br />
-1207</p></td>
<td><p>O banco de dados está bloqueado exclusivamente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDisableVersioning<br />
-1208</p></td>
<td><p>O controle de versão deste banco de dados não pode ser desabilitado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseVersion<br />
-1209</p></td>
<td><p>O mecanismo de banco de dados é incompatível com o banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase200Format<br />
-1210</p></td>
<td><p>O banco de dados está em um formato mais antigo (200). Esse erro será retornado por <a href="gg294068(v=exchg.10).md">JetInit</a> se <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> estiver definido. Somente Windows NT Client.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format<br />
-1211</p></td>
<td><p>O banco de dados está em um formato mais antigo (400). Esse erro será retornado por <a href="gg294068(v=exchg.10).md">JetInit</a> se <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> estiver definido. Somente Windows NT Client.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format<br />
-1212</p></td>
<td><p>O banco de dados está em um formato mais antigo (500). Esse erro será retornado por <a href="gg294068(v=exchg.10).md">JetInit</a> se <a href="gg269337(v=exchg.10).md">JET_paramCheckFormatWhenOpenFail</a> estiver definido. Somente Windows NT Client.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch<br />
-1213</p></td>
<td><p>O tamanho da página do banco de dados não corresponde ao mecanismo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances<br />
-1214</p></td>
<td><p>Não é possível iniciar mais instâncias de banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation<br />
-1215</p></td>
<td><p>Uma instância de banco de dados diferente está usando este banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAttachedDatabaseMismatch<br />
-1216</p></td>
<td><p>Um anexo de banco de dados pendente foi detectado no início ou no fim da recuperação, mas o banco de dados está ausente ou não corresponde às informações de anexo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPath<br />
-1217</p></td>
<td><p>O caminho especificado para o arquivo de banco de dados é inválido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseIdInUse<br />
-1218</p></td>
<td><p>Um banco de dados está sendo atribuído a uma ID que já está em uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errForceDetachNotAllowed<br />
-1219</p></td>
<td><p>A desanexação forçada só é permitida depois que a desanexação normal foi interrompida devido a um erro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCatalogCorrupted<br />
-1220</p></td>
<td><p>Corrupção detectada no catálogo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPartiallyAttachedDB<br />
-1221</p></td>
<td><p>O banco de dados está parcialmente anexado e a operação de anexação não pode ser concluída.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseSignInUse<br />
-1222</p></td>
<td><p>O banco de dados com a mesma assinatura já está em uso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseCorruptedNoRepair<br />
-1224</p></td>
<td><p>O banco de dados está corrompido, mas não é permitido um reparo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateDbVersion<br />
-1225</p></td>
<td><p>O mecanismo de banco de dados tentou reproduzir uma operação criar banco de dados do log de transações, mas falhou devido a uma versão incompatível da operação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableLocked<br />
-1302</p></td>
<td><p>A tabela está bloqueada exclusivamente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate<br />
-1303</p></td>
<td><p>A tabela já existe.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse<br />
-1304</p></td>
<td><p>A tabela está em uso e não pode ser bloqueada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound<br />
-1305</p></td>
<td><p>Não há essa tabela ou objeto.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid<br />
-1307</p></td>
<td><p>Há um arquivo ou uma densidade de índice inválidos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableNotEmpty<br />
-1308</p></td>
<td><p>A tabela não está vazia.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidTableId<br />
-1310</p></td>
<td><p>A ID da tabela é inválida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables<br />
-1311</p></td>
<td><p>Não é possível abrir mais tabelas, mesmo após a execução da tarefa de limpeza interna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation<br />
-1312</p></td>
<td><p>Não há suporte para a operação na tabela.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTablesAndCleanupTimedOut<br />
-1313</p></td>
<td><p>Não é possível abrir mais tabelas porque a tentativa de limpeza não foi concluída.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectDuplicate<br />
-1314</p></td>
<td><p>O nome da tabela ou do objeto está em uso.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidObject<br />
-1316</p></td>
<td><p>O objeto é inválido para a operação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTempTable<br />
-1317</p></td>
<td><p><a href="gg294087(v=exchg.10).md">JetCloseTable</a> deve ser usado em vez de <a href="gg294128(v=exchg.10).md">JetDeleteTable</a> para excluir uma tabela temporária.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotDeleteSystemTable<br />
-1318</p></td>
<td><p>Houve uma tentativa inválida de excluir uma tabela do sistema.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable<br />
-1319</p></td>
<td><p>Houve uma tentativa inválida de excluir uma tabela de modelo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired<br />
-1322</p></td>
<td><p>Deve haver um bloqueio exclusivo na tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFixedDDL<br />
-1323</p></td>
<td><p>As operações DDL são proibidas nesta tabela.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFixedInheritedDDL<br />
-1324</p></td>
<td><p>Em uma tabela derivada, as operações DDL são proibidas na parte herdada do DDL.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL<br />
-1325</p></td>
<td><p>O aninhamento da DDL hierárquica não tem suporte no momento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable<br />
-1326</p></td>
<td><p>Houve uma tentativa de herdar um DDL de uma tabela que não está marcada como uma tabela de modelo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSettings<br />
-1328</p></td>
<td><p>Os parâmetros do sistema foram definidos incorretamente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService<br />
-1329</p></td>
<td><p>O cliente solicitou que o serviço seja interrompido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotAddFixedVarColumnToDerivedTable<br />
-1330</p></td>
<td><p>A tabela de modelo foi criada com o sinalizador NoFixedVarColumnsInDerivedTables definido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexCantBuild<br />
-1401</p></td>
<td><p>Falha na compilação do índice.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary<br />
-1402</p></td>
<td><p>O índice primário já está definido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate<br />
-1403</p></td>
<td><p>O índice já está definido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexNotFound<br />
-1404</p></td>
<td><p>Não há esse índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexMustStay<br />
-1405</p></td>
<td><p>O índice clusterizado não pode ser excluído.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef<br />
-1406</p></td>
<td><p>A definição do índice é inválida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidCreateIndex<br />
-1409</p></td>
<td><p>A criação da descrição do índice era inválida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes<br />
-1410</p></td>
<td><p>O banco de dados está sem blocos de descrição de índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedIndexViolation<br />
-1411</p></td>
<td><p>Chaves de índice entre registros não exclusivas foram geradas para um índice de valores múltiplos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexBuildCorrupted<br />
-1412</p></td>
<td><p>Um índice secundário que reflete corretamente o índice primário falhou ao compilar.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPrimaryIndexCorrupted<br />
-1413</p></td>
<td><p>O índice primário está corrompido e o banco de dados deve ser desfragmentado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSecondaryIndexCorrupted<br />
-1414</p></td>
<td><p>O índice secundário está corrompido e o banco de dados deve ser desfragmentado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidIndexId<br />
-1416</p></td>
<td><p>A ID do índice é inválida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly<br />
-1430</p></td>
<td><p>O índice de tupla só pode ser definido em um índice secundário.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTooManyColumns<br />
-1431</p></td>
<td><p>A definição de índice para o índice de tupla contém mais colunas de chave às quais o mecanismo de banco de dados pode dar suporte.</p>
<p><strong>Observação  </strong> O erro de JET_errIndexTuplesOneColumnOnly é obsoleto e foi substituído por JET_errIndexTuplesTooManyColumns.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly<br />
-1432</p></td>
<td><p>O índice de tupla deve ser um índice não exclusivo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextBinaryColumnsOnly<br />
-1433</p></td>
<td><p>Uma definição de índice de tupla só pode conter colunas de chave que têm tipos de texto ou de coluna binária.</p>
<p><strong>Observação  </strong> O erro de JET_errIndexTuplesTextColumnsOnly é obsoleto e foi substituído por JET_errIndexTuplesTextBinaryColumnsOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed<br />
-1434</p></td>
<td><p>O índice de tupla não permite a configuração de cbVarSegMac.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits<br />
-1435</p></td>
<td><p>O comprimento mínimo/máximo da tupla ou o número máximo de caracteres especificado para um índice são inválidos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex<br />
-1436</p></td>
<td><p><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> não pode ser chamado com o sinalizador JET_bitRetrieveFromIndex definido ao recuperar uma coluna em um índice de tupla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesKeyTooSmall<br />
-1437</p></td>
<td><p>A chave especificada não atende ao comprimento mínimo da tupla.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnLong<br />
-1501</p></td>
<td><p>O valor da coluna é longo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNoChunk<br />
-1502</p></td>
<td><p>Não há nenhuma parte desse tipo em um valor longo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDoesNotFit<br />
-1503</p></td>
<td><p>O campo não será ajustado no registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid<br />
-1504</p></td>
<td><p>NULL não é válido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull<br />
JET_errNullInvalid</p></td>
<td><p>NULL não é válido. Esse erro é retornado pelo Gerenciador de registros.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIndexed-1505</p></td>
<td><p>A coluna está indexada e não pode ser excluída.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig-1506</p></td>
<td><p>O tamanho do campo é maior que o comprimento máximo permitido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound-1507</p></td>
<td><p>Não há nenhuma coluna.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnDuplicate-1508</p></td>
<td><p>Este campo já está definido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged-1509</p></td>
<td><p>Foi feita uma tentativa de criar uma coluna com vários valores, mas a coluna não estava marcada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnRedundant-1510</p></td>
<td><p>Houve uma segunda coluna de versão ou incremento automático.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType-1511</p></td>
<td><p>O tipo de dados da coluna é inválido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTaggedNotNULL-1514</p></td>
<td><p>Não há colunas marcadas não nulas.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex-1515</p></td>
<td><p>O banco de dados é inválido porque não contém um índice atual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyIsMade-1516</p></td>
<td><p>A chave é completamente feita.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId-1517</p></td>
<td><p>A ID da coluna está incorreta.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadItagSequence-1518</p></td>
<td><p>Há um itagSequence inadequado para a coluna marcada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnInRelationship-1519</p></td>
<td><p>Não é possível excluir uma coluna porque ela faz parte de uma relação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged-1521</p></td>
<td><p>O incremento automático e a versão não podem ser marcados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDefaultValueTooBig-1524</p></td>
<td><p>O valor padrão excede o tamanho máximo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate-1525</p></td>
<td><p>Um valor duplicado foi detectado em uma coluna de valores múltiplos exclusiva.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLVCorrupted-1526</p></td>
<td><p>Corrupção encontrada em uma árvore de valor longo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicateAfterTruncation-1528</p></td>
<td><p>Um valor duplicado foi detectado em uma coluna com vários valores exclusivos depois que os dados foram normalizados e está normalizando truncamento dos dados antes da comparação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDerivedColumnCorruption-1529</p></td>
<td><p>Há uma coluna inválida na tabela derivada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPlaceholderColumn-1530</p></td>
<td><p>Foi feita uma tentativa de converter uma coluna em um espaço reservado de índice primário, mas a coluna não atende aos critérios necessários.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordNotFound-1601</p></td>
<td><p>A chave não foi encontrada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNoCopy-1602</p></td>
<td><p>Não há um buffer de trabalho.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord-1603</p></td>
<td><p>Não há nenhum registro atual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordPrimaryChanged-1604</p></td>
<td><p>A chave primária pode não ser alterada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyDuplicate-1605</p></td>
<td><p>Há uma chave duplicada ilegal.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyPrepared-1607</p></td>
<td><p>Foi feita uma tentativa de atualizar um registro enquanto uma atualização de registro já estava em andamento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyNotMade-1608</p></td>
<td><p>Não foi feita uma chamada para <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared-1609</p></td>
<td><p>Não foi feita uma chamada para <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDataHasChanged-1611</p></td>
<td><p>Os dados foram alterados e a operação foi anulada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLanguageNotSupported-1619</p></td>
<td><p>Esta instalação do Windows não oferece suporte ao idioma selecionado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts-1701</p></td>
<td><p>Há muitos processos de classificação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOnSort-1702</p></td>
<td><p>Ocorreu uma operação inválida durante uma classificação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTempFileOpenError-1803</p></td>
<td><p>Não foi possível abrir o arquivo temporário.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyAttachedDatabases-1805</p></td>
<td><p>Um número excessivo de bancos de dados está aberto.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskFull-1808</p></td>
<td><p>Não há espaço restante no disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied-1809</p></td>
<td><p>Permissão negada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileNotFound-1811</p></td>
<td><p>O arquivo não foi encontrado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileInvalidType-1812</p></td>
<td><p>O tipo de arquivo é inválido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errAfterInitialization-1850</p></td>
<td><p>Uma restauração não pode ser iniciada após a inicialização.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogCorrupted-1852</p></td>
<td><p>Não foi possível interpretar os logs.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation-1906</p></td>
<td><p>A operação é inválida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAccessDenied-1907</p></td>
<td><p>O acesso foi negado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySplits-1909</p></td>
<td><p>Uma divisão infinita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation-1910</p></td>
<td><p>Vários threads estão usando a mesma sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errEntryPointNotFound-1911</p></td>
<td><p>Não foi possível encontrar um ponto de entrada em uma DLL necessária.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionContextAlreadySet-1912</p></td>
<td><p>A sessão especificada já tem um contexto de sessão definido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionContextNotSetByThisThread-1913</p></td>
<td><p>Foi feita uma tentativa de redefinir o contexto da sessão, mas o thread atual não era o original que definiu o contexto da sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionInUse-1914</p></td>
<td><p>Foi feita uma tentativa de encerrar a sessão em uso no momento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordFormatConversionFailed-1915</p></td>
<td><p>Ocorreu um erro interno durante uma conversão de formato de registro dinâmico.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOneDatabasePerSession-1916</p></td>
<td><p>Somente um banco de dados de usuário aberto por sessão é permitido (conforme indicado pela configuração do sinalizador de <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> durante a criação do banco de dados).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError-1917</p></td>
<td><p>Ocorreu um erro durante a reversão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackFailed-2101</p></td>
<td><p>Falha em uma chamada de função de retorno.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCallbackNotResolved-2102</p></td>
<td><p>Não foi possível encontrar uma função de retorno de chamada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSequence-2401</p></td>
<td><p>A API de cópia de sombra do sistema operacional foi usada em uma sequência inválida.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut-2402</p></td>
<td><p>A cópia de sombra do sistema operacional terminou com um tempo limite.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotNotAllowed-2403</p></td>
<td><p>A cópia de sombra do sistema operacional não é permitida porque um backup ou uma recuperação em andamento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId-2404</p></td>
<td><p>A operação falhou porque o identificador de cópia de sombra do sistema operacional especificado era inválido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified-3000</p></td>
<td><p>Foi feita uma tentativa de usar o armazenamento local sem a especificação de uma função de retorno de chamada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet-3001</p></td>
<td><p>Foi feita uma tentativa de definir o armazenamento local para um objeto que já tinha sido definido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSNotSet-3002</p></td>
<td><p>Foi feita uma tentativa de recuperar o armazenamento local de um objeto que não tinha sido definido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOSparse-4000</p></td>
<td><p>Uma operação de e/s falhou porque foi tentada em relação a uma região não alocada de um arquivo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIOBeyondEOF-4001</p></td>
<td><p>Uma leitura foi emitida para um local além do EOF (as gravações expandirão o arquivo).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOAbort-4002</p></td>
<td><p>Esse sinalizador instrui o chamador JET_ABORTRETRYFAILCALLBACK a anular a e/s especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileIORetry-4003</p></td>
<td><p>Esse sinalizador instrui o chamador JET_ABORTRETRYFAILCALLBACK a repetir a e/s especificada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFileIOFail-4004</p></td>
<td><p>Esse sinalizador instrui o chamador JET_ABORTRETRYFAILCALLBACK a falhar na e/s especificada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errFileCompressed-4005</p></td>
<td><p>Não há suporte para acesso de leitura/gravação em arquivos compactados.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Comentários

Em geral, um valor maior que zero deve ser interpretado como um aviso, um valor de zero deve ser interpretado como êxito e um valor menor que zero deve ser interpretado como um erro. Nenhum outro padrão nesses valores, como intervalos de valores, deve ser confiado por um aplicativo.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erros](./error-handling-parameters.md)  
[Erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md)  
[Arquivos do mecanismo de armazenamento extensível](./extensible-storage-engine-files.md)
