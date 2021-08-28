---
description: 'Saiba mais sobre: função JetBeginExternalBackup'
title: Função JetBeginExternalBackup
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8d0e47a117c044899a8b078290be622cfecdae91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482902"
---
# <a name="jetbeginexternalbackup-function"></a>Função JetBeginExternalBackup


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetbeginexternalbackup-function"></a>Função JetBeginExternalBackup

A função **JetBeginExternalBackup** inicia um backup externo enquanto o mecanismo e o banco de dados estão online e ativos. **JetBeginExternalBackup** é o primeiro de uma série de funções que devem ser chamadas para executar um backup online (não baseado em VSS) com êxito.

Um backup externo pode ser usado para implementar backups completos, incrementais ou diferenciais.

O backup será difuso, pois o backup será consistente para um único ponto no histórico de transações, mas não é possível controlar o ponto exato no tempo.

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Esse sinalizador foi preterido. O uso desse bit resultará na JET_errInvalidgrbit retornando.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Cria um backup incremental em oposição a um backup completo. Isso significa que somente os arquivos de log desde o último backup completo ou incremental serão submetidos a backup.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Reservado para uso futuro. definido para Windows XP.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Se um backup externo ou backup de instantâneo já estiver em andamento, esse erro será retornado, até que <strong>JetBeginExternalBackup</strong> (ou uma das variantes de ti) seja chamado. O ESE permite apenas um backup online de cada vez.</p> | 
| <p>JET_errBackupNotAllowedYet</p> | <p>A instância ou o mecanismo de banco de dados está em recuperação ou em uma fase de desligamento ou término.</p> | 
| <p>JET_errCheckpointCorrupt</p> | <p>Em um backup completo, o arquivo de ponto de verificação não pôde ser lido ou o arquivo não pôde ser verificado.</p> | 
| <p>JET_errCheckpointFileNotFound</p> | <p>Em um backup completo, o arquivo de ponto de verificação não pôde ser encontrado.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong> esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errInvalidBackup</p> | <p>O log circular está habilitado e o tipo de backup especificado é JET_bitBackupIncremental. Consulte <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> nos <strong>erros do log de transações</strong> para obter informações sobre como controlar o registro em log circular ou não circular.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Um ou mais dos membros do <em>grbit</em> eram inválidos.</p> | 
| <p>JET_errLoggingDisabled</p> | <p>A recuperação ou o log está desabilitado. Você não poderá fazer um backup online se o log estiver desabilitado. Para obter mais informações sobre log e recuperação, consulte <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</p> | 
| <p>JET_errLogWriteFail</p> | <p>O mecanismo parou de gravar na unidade de log devido ao log estar cheio ou erros de e/s de disco.</p> | 
| <p>JET_errMissingFullBackup</p> | <p>O backup incremental foi especificado (com JET_bitBackupIncremental) e nunca foi feito um backup completo para um dos bancos de dados anexados para o conjunto de logs.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errOutOfMemory</p> | <p>A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>a operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (Windows modo de compatibilidade 2000) em que há suporte para apenas uma instância quando, na verdade, várias instâncias já existem.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p> | 



Se a função for realizada com sucesso, um backup externo será iniciado e o mecanismo de estado de backup será inicializado. As APIs subsequentes agora podem ser chamadas para concluir a sequência de backup externo e transmitir ou ler o arquivo de banco de dados, o arquivo de patch de banco de dados (se houver suporte) e o arquivo de log. Um evento pode ser registrado em log que um backup externo foi iniciado.

Se a função falhar, a sessão de backup não será iniciada. Se outra sessão de backup estiver em andamento, ela não será cancelada.

#### <a name="remarks"></a>Comentários

O processo de backup externo (como iniciado por **JetBeginExternalBackup**) foi projetado para permitir um backup online de transação difusa de toda a instância para um dispositivo de destino como um fluxo. O backup conterá todos os arquivos de banco de dados anexados à instância usando [JetAttachDatabase](./jetattachdatabase-function.md) (para um backup completo), seguidos por seus arquivos de patch de banco de dados associados (se houver suporte) e, por fim, pelos arquivos de log de transações que foram gerados durante o processo de backup. O resultado final será um conjunto de arquivos que podem ser restaurados do fluxo, possivelmente combinados com os arquivos de banco de dados e de log existentes e, por fim, recuperados para um estado consistente.

A ordem geral de operações para um backup completo consiste nas chamadas a seguir. Primeiro, **JetBeginExternalBackup** é chamado para iniciar o processo de backup. Em seguida, [JetGetAttachInfo](./jetgetattachinfo-function.md) é chamado para obter a lista de bancos de dados anexados à instância que precisa ser submetida a backup. Para cada um desses bancos de dados, [JetOpenFile](./jetopenfile-function.md) é chamado, seguido por uma série de chamadas [JetReadFile](./jetreadfile-function.md) e, em seguida, por uma chamada para [JetCloseFile](./jetclosefile-function.md). Em seguida, [JetGetLogInfo](./jetgetloginfo-function.md) é chamado para obter uma lista de arquivos de log e patch de banco de dados para backup. Para cada um desses arquivos, outra sequência de chamadas [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md)e [JetCloseFile](./jetclosefile-function.md) são feitas. Em seguida, todos os arquivos de log de transações indesejados são excluídos usando [JetTruncateLog](./jettruncatelog-function.md). Por fim, o backup é finalizado por uma chamada para [JetEndExternalBackup](./jetendexternalbackup-function.md).

Também é possível modificar esse conjunto de etapas para executar um backup incremental da instância. Um backup incremental enumera e faz backup dos arquivos de log. Os backups incrementais só serão possíveis se o log circular não estiver habilitado.

Também é possível modificar esse conjunto de etapas para permitir backups diferenciais subsequentes da instância a ser executada. Para executar um backup diferencial, não chame [JetTruncateLog](./jettruncatelog-function.md) no backup completo ou incremental anterior. Ao não chamar [JetTruncateLog](./jettruncatelog-function.md), você permite que os backups subsequentes sejam diferenciais em relação ao último backup completo ou incremental. Os backups diferenciais só serão possíveis se o registro em log circular não estiver habilitado.

O arquivo de patch de banco de dados é um arquivo auxiliar especial que é usado para armazenar imagens de página de banco de dados em determinadas circunstâncias durante o backup. Esse arquivo deve estar presente no mesmo local que seu banco de dados associado durante uma operação de restauração. este arquivo só é usado no Windows 2000. como resultado, qualquer aplicativo escrito para funcionar em Windows 2000 e outras versões deve dar suporte a arquivos de patch de banco de dados, se estiverem presentes, mas também não deverá falhar se não estiverem presentes.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
