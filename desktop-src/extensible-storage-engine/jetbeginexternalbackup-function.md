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
ms.openlocfilehash: d410adb592c3d56d2f9880ec809749396318258a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766933"
---
# <a name="jetbeginexternalbackup-function"></a>Função JetBeginExternalBackup


_**Aplica-se a:** Windows | Windows Server_

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Esse sinalizador foi preterido. O uso desse bit resultará na JET_errInvalidgrbit retornando.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Cria um backup incremental em oposição a um backup completo. Isso significa que somente os arquivos de log desde o último backup completo ou incremental serão submetidos a backup.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Reservado para uso futuro. Definido para o Windows XP.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupInProgress</p></td>
<td><p>Se um backup externo ou backup de instantâneo já estiver em andamento, esse erro será retornado, até que <strong>JetBeginExternalBackup</strong> (ou uma das variantes de ti) seja chamado. O ESE permite apenas um backup online de cada vez.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>A instância ou o mecanismo de banco de dados está em recuperação ou em uma fase de desligamento ou término.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCheckpointCorrupt</p></td>
<td><p>Em um backup completo, o arquivo de ponto de verificação não pôde ser lido ou o arquivo não pôde ser verificado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCheckpointFileNotFound</p></td>
<td><p>Em um backup completo, o arquivo de ponto de verificação não pôde ser encontrado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>O log circular está habilitado e o tipo de backup especificado é JET_bitBackupIncremental. Consulte <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> nos <strong>erros do log de transações</strong> para obter informações sobre como controlar o registro em log circular ou não circular.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Um ou mais dos membros do <em>grbit</em> eram inválidos.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLoggingDisabled</p></td>
<td><p>A recuperação ou o log está desabilitado. Você não poderá fazer um backup online se o log estiver desabilitado. Para obter mais informações sobre log e recuperação, consulte <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogWriteFail</p></td>
<td><p>O mecanismo parou de gravar na unidade de log devido ao log estar cheio ou erros de e/s de disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMissingFullBackup</p></td>
<td><p>O backup incremental foi especificado (com JET_bitBackupIncremental) e nunca foi feito um backup completo para um dos bancos de dados anexados para o conjunto de logs.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>A operação falhou porque não foi possível alocar memória suficiente para concluí-la.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Se a função for realizada com sucesso, um backup externo será iniciado e o mecanismo de estado de backup será inicializado. As APIs subsequentes agora podem ser chamadas para concluir a sequência de backup externo e transmitir ou ler o arquivo de banco de dados, o arquivo de patch de banco de dados (se houver suporte) e o arquivo de log. Um evento pode ser registrado em log que um backup externo foi iniciado.

Se a função falhar, a sessão de backup não será iniciada. Se outra sessão de backup estiver em andamento, ela não será cancelada.

#### <a name="remarks"></a>Comentários

O processo de backup externo (como iniciado por **JetBeginExternalBackup**) foi projetado para permitir um backup online de transação difusa de toda a instância para um dispositivo de destino como um fluxo. O backup conterá todos os arquivos de banco de dados anexados à instância usando [JetAttachDatabase](./jetattachdatabase-function.md) (para um backup completo), seguidos por seus arquivos de patch de banco de dados associados (se houver suporte) e, por fim, pelos arquivos de log de transações que foram gerados durante o processo de backup. O resultado final será um conjunto de arquivos que podem ser restaurados do fluxo, possivelmente combinados com os arquivos de banco de dados e de log existentes e, por fim, recuperados para um estado consistente.

A ordem geral de operações para um backup completo consiste nas chamadas a seguir. Primeiro, **JetBeginExternalBackup** é chamado para iniciar o processo de backup. Em seguida, [JetGetAttachInfo](./jetgetattachinfo-function.md) é chamado para obter a lista de bancos de dados anexados à instância que precisa ser submetida a backup. Para cada um desses bancos de dados, [JetOpenFile](./jetopenfile-function.md) é chamado, seguido por uma série de chamadas [JetReadFile](./jetreadfile-function.md) e, em seguida, por uma chamada para [JetCloseFile](./jetclosefile-function.md). Em seguida, [JetGetLogInfo](./jetgetloginfo-function.md) é chamado para obter uma lista de arquivos de log e patch de banco de dados para backup. Para cada um desses arquivos, outra sequência de chamadas [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md)e [JetCloseFile](./jetclosefile-function.md) são feitas. Em seguida, todos os arquivos de log de transações indesejados são excluídos usando [JetTruncateLog](./jettruncatelog-function.md). Por fim, o backup é finalizado por uma chamada para [JetEndExternalBackup](./jetendexternalbackup-function.md).

Também é possível modificar esse conjunto de etapas para executar um backup incremental da instância. Um backup incremental enumera e faz backup dos arquivos de log. Os backups incrementais só serão possíveis se o log circular não estiver habilitado.

Também é possível modificar esse conjunto de etapas para permitir backups diferenciais subsequentes da instância a ser executada. Para executar um backup diferencial, não chame [JetTruncateLog](./jettruncatelog-function.md) no backup completo ou incremental anterior. Ao não chamar [JetTruncateLog](./jettruncatelog-function.md), você permite que os backups subsequentes sejam diferenciais em relação ao último backup completo ou incremental. Os backups diferenciais só serão possíveis se o registro em log circular não estiver habilitado.

O arquivo de patch de banco de dados é um arquivo auxiliar especial que é usado para armazenar imagens de página de banco de dados em determinadas circunstâncias durante o backup. Esse arquivo deve estar presente no mesmo local que seu banco de dados associado durante uma operação de restauração. Esse arquivo só é usado no Windows 2000. Como resultado, qualquer aplicativo escrito para funcionar no Windows 2000 e em outras versões deve dar suporte a arquivos de patch de banco de dados, se estiverem presentes, mas também não deverá falhar se não estiverem presentes.

#### <a name="requirements"></a>Requisitos

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
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


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
