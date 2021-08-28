---
description: 'Saiba mais sobre: Função JetGetLogInfoInstance2'
title: Função JetGetLogInfoInstance2
TOCTitle: JetGetLogInfoInstance2 Function
ms:assetid: 50fdae92-611c-4dbf-846e-86cc836a23db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269247(v=EXCHG.10)
ms:contentKeyID: 32765549
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance2W
- JetGetLogInfoInstance2
- JetGetLogInfoInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec8bf0a4cee4e89f8252e53ed0ffbeb3aed4bcdf
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982529"
---
# <a name="jetgetloginfoinstance2-function"></a>Função JetGetLogInfoInstance2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetloginfoinstance2-function"></a>Função JetGetLogInfoInstance2

A **função JetGetLogInfoInstance2** é usada durante um backup iniciado por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar uma instância para os nomes de arquivos de patch de banco de dados e arquivos de log de transações que devem se tornar parte do conjunto de arquivos de backup. Esses arquivos podem ser abertos posteriormente usando [JetOpenFile](./jetopenfile-function.md) e lidos usando [JetReadFile](./jetreadfile-function.md).

**Windows XP: JetGetLogInfoInstance2** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetGetLogInfoInstance2(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in_out_opt  JET_LOGINFO* pLogInfo
    );
```

### <a name="parameters"></a>Parâmetros

*Instância*

A instância a ser usada para essa chamada.

Por Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância. O uso dessa instância global está implícito nesse caso.

Para Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só poderá ser chamada quando o mecanismo estiver no modo herdado (modo de compatibilidade do Windows 2000), em que há suporte para apenas uma instância. Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.

*Szz*

O buffer de saída que receberá a lista de cadeias de caracteres terminadas em nulo que descrevem o conjunto de arquivos de patch de banco de dados e arquivos de log de transações que devem fazer parte do conjunto de arquivos de backup.

A lista de cadeias de caracteres retornadas nesse buffer está no mesmo formato que uma cadeia de caracteres multi-cadeia de caracteres usada pelo Registro. Cada cadeia de caracteres terminada em nulo é retornada em sequência seguida por um terminador nulo final.

*cbMax*

O tamanho máximo em bytes do buffer de saída.

*pcbActual*

Recebe a quantidade real de dados de cadeia de caracteres recebidos no buffer de saída.

*pLogInfo*

Recebe informações estruturadas sobre os arquivos de log de transações que devem fazer parte do conjunto de arquivos de backup.

Quando esse parâmetro não está presente, presume-se que seu valor seja NULL.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>A operação de backup falhou porque foi chamada fora de sequência. <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> retornará esse erro se houver quaisquer alças de arquivo pendentes criadas usando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para a instância.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> quando o alçamento de instância especificado é inválido (Windows XP e versões posteriores).</p> | 
| <p>JET_errNoBackup</p> | <p>A operação falhou porque nenhum backup externo está em andamento.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (Windows modo de compatibilidade 2000), em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 



Em caso de êxito, as informações solicitadas sobre o conjunto de arquivos de patch de banco de dados e arquivos de log de transações que devem fazer parte do conjunto de arquivos de backup serão colocadas nos buffers de saída quando fornecidos. O computador de estado de backup será avançado de forma que o backup de arquivos de banco de dados não seja mais permitido. Somente arquivos de patch de banco de dados e arquivos de log de transações têm permissão para serem abertos para backup além desse ponto.

Em caso de falha, o estado dos buffers de saída é indefinido. A falha resultará no cancelamento de todo o processo de backup para a instância.

#### <a name="remarks"></a>Comentários

É importante observar que essa API não retornará um erro ou aviso se o buffer de saída for muito pequeno para aceitar a lista completa de arquivos que devem fazer parte do conjunto de arquivos de backup. O aplicativo sempre deve fornecer um buffer para receber o tamanho real dessa lista e usar essas informações para determinar se a lista foi truncada.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetLogInfoInstance2W</strong> (Unicode) e <strong>JetGetLogInfoInstance2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_LOGINFO](./jet-loginfo-structure.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)
