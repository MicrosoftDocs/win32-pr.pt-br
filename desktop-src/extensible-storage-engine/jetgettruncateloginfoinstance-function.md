---
description: 'Saiba mais sobre: função JetGetTruncateLogInfoInstance'
title: Função JetGetTruncateLogInfoInstance
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36583267277f7c5254adc85047ce99631f6c03ef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479072"
---
# <a name="jetgettruncateloginfoinstance-function"></a>Função JetGetTruncateLogInfoInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgettruncateloginfoinstance-function"></a>Função JetGetTruncateLogInfoInstance

A função **JetGetTruncateLogInfoInstance** é usada durante um backup iniciado pelo [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar uma instância para obter os nomes dos arquivos de log de transações que podem ser excluídos com segurança depois que o backup for concluído com êxito.

**Windows xp:** o **JetGetTruncateLogInfoInstance** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância a ser usada para esta chamada.

*szz*

O buffer de saída que recebe a lista de cadeias de caracteres terminadas em nulo que descreve o conjunto de arquivos de log de transações que podem ser excluídos com segurança após a conclusão bem-sucedida do backup.

A lista de cadeias de caracteres que são retornadas nesse buffer está no mesmo formato que uma cadeia de caracteres múltipla usada pelo registro. Cada cadeia de caracteres terminada em nulo é retornada em sequência e seguida por um terminador nulo final.

*cbMax*

O tamanho máximo em bytes do buffer de saída.

*pcbActual*

Ponteiro para o buffer de saída que recebe a quantidade real de dados de cadeia de caracteres.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro resultou em um resultado inesperado.</p><p><strong>Windows XP e posterior:</strong>  Isso pode ocorrer para <strong>JetGetTruncateLogInfoInstance</strong> quando o identificador de instância especificado é inválido.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  esse valor de retorno foi introduzido no Windows XP.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p><p><strong>Windows XP:</strong>  esse valor de retorno foi introduzido no Windows XP.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>A operação de backup falhou porque ela foi chamada fora de sequência.</p> | 
| <p>JET_errNoBackup</p> | <p>A operação falhou porque nenhum backup externo está em andamento.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p> | 
| <p><strong>JetGetTruncateLogInfoInstance</strong></p> | <p>Há identificadores de arquivo pendentes que foram criados usando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para a instância.</p> | 



Se essa função for bem-sucedida, as informações solicitadas sobre o conjunto de arquivos de log de transações que podem ser excluídas com segurança após a conclusão bem-sucedida do backup serão colocadas nos buffers de saída em que são fornecidas. O computador de estado de backup será avançado de modo que o backup de arquivos de banco de dados não seja mais permitido. Somente arquivos de patch de banco de dados e arquivos de log de transações podem ser abertos para backup além desse ponto.

Se essa função falhar, o estado dos buffers de saída será indefinido. A falha resultará no cancelamento de todo o processo de backup da instância.

#### <a name="remarks"></a>Comentários

Essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup. O aplicativo sempre deve fornecer um buffer para receber o tamanho real dessa lista e usar essas informações para determinar se a lista foi truncada.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) e <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
