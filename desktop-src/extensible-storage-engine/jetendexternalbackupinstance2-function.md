---
description: 'Saiba mais sobre: Função JetEndExternalBackupInstance2'
title: Função JetEndExternalBackupInstance2
TOCTitle: JetEndExternalBackupInstance2 Function
ms:assetid: a30961f7-a1fb-44fe-881a-d46bf8f743b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294047(v=EXCHG.10)
ms:contentKeyID: 32765646
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4235736d9933a510922e5fcc4ffc72c27cd0037
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477612"
---
# <a name="jetendexternalbackupinstance2-function"></a>Função JetEndExternalBackupInstance2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetendexternalbackupinstance2-function"></a>Função JetEndExternalBackupInstance2

A **função JetEndExternalBackupInstance2** encerra uma sessão de backup externa. Essa API é a última API em uma série de APIs que devem ser chamadas para executar um backup online bem-sucedido (não baseado em VSS).

**Windows XP: JetEndExternalBackupInstance2** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*Instância*

A instância a ser usada para essa chamada.

**Windows 2000:** Por Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância. O uso dessa instância global está implícito nesse caso.

**Windows XP:** Para Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo estiver no modo herdado (modo de compatibilidade do Windows 2000), em que há suporte para apenas uma instância. Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitBackupEndAbort<br />0x0002</p> | <p>O aplicativo cliente está anulando o backup.</p> | 
| <p>JET_bitBackupEndNormal<br />0x0001</p> | <p>O aplicativo cliente concluiu o backup completamente e está terminando normalmente.</p> | 
| <p>JET_bitBackupTruncateDone<br />0x0100</p> | <p><strong>Windows Vista:</strong> JET_bitBackupTruncateDone é introduzido no Windows Vista.</p><p>O mecanismo pode marcar os headers de banco de dados conforme apropriado (por exemplo, um backup completo concluído), mesmo que a chamada para truncar não tenha sido concluída.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupAbortByCaller</p> | <p><strong>Windows XP:</strong> Esse valor de retorno é introduzido no Windows XP.</p><p>O chamador finalizou um backup no meio da sequência de backup sem sinalizar a intenção com <a href="gg294067(v=exchg.10).md">JetStopBackup.</a> Esse erro é resultado de um bug no cliente de backup no Windows Server 2003 e posterior. No Windows XP, esse erro é retornado para uma terminação intencional da sequência de backup externa.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p><strong>Windows Server 2003:</strong> Esse valor de retorno é introduzido no Windows Server 2003.</p><p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p><strong>Windows XP:</strong> Esse valor de retorno é introduzido no Windows XP.</p><p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p> | 
| <p>JET_errNoBackup</p> | <p>A operação falhou porque nenhum backup externo está em andamento.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que há suporte para apenas uma instância, quando, na verdade, várias instâncias já existem.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo fechada.</p> | 



Se a função for bem-sucedida, o backup externo foi um sucesso. Êxito indica que todos os arquivos (por exemplo, bancos de dados e logs) apropriados para o tipo de backup (especificado em [JetBeginExternalBackup)](./jetbeginexternalbackup-function.md)foram recuperados do mecanismo de backup. Os arquivos de backup podem ser recuperados com recuperação em tempo de recuperação ([JetExternalRestore](./jetexternalrestore-function.md)).

Se essa função falhar, o backup externo geralmente termina. Falha significa que o backup é inválido devido a um cliente ou um erro de uso do aplicativo. É importante verificar o código de retorno dessa API para verificar se a sequência de backup foi bem-sucedida.

#### <a name="remarks"></a>Comentários

Se o mecanismo estiver configurado para registrar eventos, um evento será registrado para indicar a resolução do backup externo.

Se a sequência de backup não for concluída na ordem e com uma chamada bem-sucedida para [JetEndExternalBackup,](./jetendexternalbackup-function.md)os backups incrementais subsequentes poderão conter mais dados do que o aplicativo previsto.

Para obter mais informações sobre a sequência de API de backup externo, consulte [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

Antes Windows Vista, se o truncamento de log não foi feito, o mecanismo considerou que o backup era um backup de cópia. No entanto, o backup pode ser um backup normal para o qual o truncamento não foi feito (por exemplo, se houver bancos de dados desvinculados). A JET_bitBackupTruncateDone pode ser usada para informar o mecanismo sobre isso e permitir modificações de header de banco de dados apropriadas.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erro](./error-handling-parameters.md)  
[Erros extensíveis Armazenamento mecanismo](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
