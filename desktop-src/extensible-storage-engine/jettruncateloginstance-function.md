---
description: 'Saiba mais sobre: Função JetTruncateLogInstance'
title: Função JetTruncateLogInstance
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4fdf8f7c47baab70426ddf03cdbc666a13c08f3d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477852"
---
# <a name="jettruncateloginstance-function"></a>Função JetTruncateLogInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jettruncateloginstance-function"></a>Função JetTruncateLogInstance

A **função JetTruncateLogInstance** é usada durante um backup iniciado por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para excluir todos os arquivos de log de transações que não serão mais necessários depois que o backup atual for concluído com êxito.

**Windows XP:****JetTruncateLogInstance** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parâmetros

*Instância*

A instância a ser usada para essa chamada.

Por Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância. O uso dessa instância global está implícito nesse caso.

Para Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só poderá ser chamada quando o mecanismo estiver no modo herdado (modo de compatibilidade do Windows 2000), em que há suporte para apenas uma instância. Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p><strong>Windows Server 2003:</strong>  Esse valor de retorno é introduzido no Windows Server 2003.</p><p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidBackupSequence</p> | <p>A operação de backup falhou porque foi chamada fora de sequência. <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> retornará esse erro se houver quaisquer alças de arquivo pendentes que foram criadas usando <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para a instância.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários parâmetros gerou um resultado inesperado. Isso pode acontecer para <a href="gg269263(v=exchg.10).md">JetTruncateLog quando</a> o handle de instância especificado é inválido.</p> | 
| <p>JET_errNoBackup</p> | <p>A operação falhou porque nenhum backup externo está em andamento.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade Windows 2000), em que apenas uma instância tem suporte quando, na verdade, várias instâncias já existem.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo fechada.</p> | 



Se essa função for bem-sucedida, o conjunto de arquivos de log de transações que não serão mais necessários depois que o backup atual for concluído com êxito serão excluídos. O computador de estado de backup será avançado de forma que o backup de arquivos de banco de dados não seja mais permitido. Somente arquivos de patch de banco de dados e arquivos de log de transações têm permissão para serem abertos para backup além desse ponto.

Se essa função falhar, o computador de estado de backup poderá ser avançado de forma que o backup de arquivos de banco de dados não seja mais permitido. Alguns arquivos de log de transações podem ser excluídos que é menor que o número desejado, mas eles sempre serão excluídos do mais antigo para o mais novo.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[Arquivos extensíveis Armazenamento mecanismo](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)
