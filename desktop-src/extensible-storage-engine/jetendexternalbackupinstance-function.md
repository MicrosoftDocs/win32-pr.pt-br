---
description: 'Saiba mais sobre: função JetEndExternalBackupInstance'
title: Função JetEndExternalBackupInstance
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f82af0be3185db36498d9a5888da190e92314184
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479172"
---
# <a name="jetendexternalbackupinstance-function"></a>Função JetEndExternalBackupInstance


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetendexternalbackupinstance-function"></a>Função JetEndExternalBackupInstance

A função **JetEndExternalBackupInstance** encerra uma sessão de backup externo. Essa API é a última API em uma série de APIs que devem ser chamadas para executar um backup online (não baseado em VSS) com êxito.

**Windows XP: o JetEndExternalBackupInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância a ser usada para esta chamada.

**Windows 2000:** Para o Windows 2000, a variante de API que aceita esse parâmetro não está disponível porque há suporte para apenas uma instância. O uso dessa instância global é implícito nesse caso.

**Windows XP:** Para o Windows XP e versões posteriores, a variante de API que não aceita esse parâmetro só pode ser chamada quando o mecanismo está no modo herdado (modo de compatibilidade do Windows 2000), em que apenas uma instância tem suporte. Caso contrário, a operação falhará com JET_errRunningInMultiInstanceMode.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupAbortByCaller</p> | <p><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</p><p>O chamador encerrou um backup no meio da sequência de backup sem sinalizar a intenção com <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Esse erro é o resultado de um bug no cliente de backup no Windows Server 2003 e posterior. No Windows XP, esse erro é retornado para um encerramento intencional da sequência de backup externo.</p> | 
| <p>JET_errBackupAbortByServer</p> | <p><strong>Windows Server 2003:  </strong> Esse valor de retorno é introduzido no Windows Server 2003.</p><p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</p><p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p> | 
| <p>JET_errNoBackup</p> | <p>A operação falhou porque nenhum backup externo está em andamento.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que há suporte para apenas uma instância, quando, na verdade, várias instâncias já existem.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p> | 



Se a função for bem-sucedida, o backup externo foi um sucesso. Êxito indica que todos os arquivos (por exemplo, bancos de dados e logs) apropriados para o tipo de backup (especificado em [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) foram recuperados do mecanismo de backup. Os arquivos de backup podem ser recuperados com a[JetExternalRestore](./jetexternalrestore-function.md)(recuperação de hardware).

Se essa função falhar, o backup externo geralmente termina. Falha significa que o backup é inválido devido a um erro de uso do cliente ou do aplicativo. É importante verificar o código de retorno dessa API para verificar se a sequência de backup foi bem-sucedida.

#### <a name="remarks"></a>Comentários

Se o mecanismo estiver configurado para registrar eventos, um evento será registrado para indicar a resolução do backup externo.

Se a sequência de backup não for concluída na ordem e com uma chamada bem-sucedida para [JetEndExternalBackup](./jetendexternalbackup-function.md), os backups incrementais subsequentes poderão conter mais dados do que o aplicativo previsto.

Para obter mais informações sobre a sequência de API de backup externo, consulte [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

Antes do Windows Vista, se o truncamento de log não foi feito, o mecanismo considerou que o backup era um backup de cópia. No entanto, o backup pode ser um backup normal para o qual o truncamento não foi feito (por exemplo, se houver bancos de dados desanexados). A opção JET_bitBackupTruncateDone pode ser usada para informar o mecanismo sobre isso e permitir modificações adequadas no cabeçalho do banco de dados.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer o Windows Vista ou o Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer o Windows Server 2008 ou o Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erros](./error-handling-parameters.md)  
[Erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JET_ERR](./jet-err.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
