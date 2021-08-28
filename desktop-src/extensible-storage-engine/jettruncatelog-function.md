---
description: 'Saiba mais sobre: função JetTruncateLog'
title: Função JetTruncateLog
TOCTitle: JetTruncateLog Function
ms:assetid: 60cbf563-4228-452a-9b20-c7b1330c4514
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269263(v=EXCHG.10)
ms:contentKeyID: 32765565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 038a07a5781c9b38d729b63af0bd9f9cce52c75e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982349"
---
# <a name="jettruncatelog-function"></a>Função JetTruncateLog


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jettruncatelog-function"></a>Função JetTruncateLog

A função **JetTruncateLog** é usada durante um backup que é iniciado pelo [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para excluir todos os arquivos de log de transações que não serão mais necessários quando o backup atual for concluído com êxito.

```cpp
    JET_ERR JET_API JetTruncateLog(void);
```

### <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p><p><strong>Windows Server 2003:</strong>  esse valor de retorno é introduzido no Windows Server 2003.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>A operação de backup falhou porque ela foi chamada fora de sequência. <strong>JetTruncateLog</strong> retornará esse erro se houver identificadores de arquivo pendentes que foram criados usando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para a instância.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários parâmetros gerou um resultado inesperado. Isso pode ocorrer para <strong>JetTruncateLog</strong> quando o identificador de instância especificado é inválido.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errNoBackup</p> | <p>A operação falhou porque nenhum backup externo está em andamento.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>a operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (Windows modo de compatibilidade 2000) em que há suporte para apenas uma instância, quando, na verdade, várias instâncias já existem.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p> | 



Se essa função for bem-sucedida, o conjunto de arquivos de log de transações que não será mais necessário quando o backup atual for concluído com êxito será excluído. O computador de estado de backup será avançado de modo que o backup de arquivos de banco de dados não seja mais permitido. Somente arquivos de patch de banco de dados e arquivos de log de transações podem ser abertos para backup além desse ponto.

Se essa função falhar, o computador de estado de backup poderá ser avançado, de modo que o backup de arquivos de banco de dados não seja mais permitido. Um número de arquivos de log de transações pode ser excluído, que é menor que o número desejado, mas eles sempre serão excluídos do mais antigo para o mais recente.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
