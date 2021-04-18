---
description: 'Saiba mais sobre: função JetEndExternalBackup'
title: Função JetEndExternalBackup
TOCTitle: JetEndExternalBackup Function
ms:assetid: 058f903b-14b7-44b3-9ec7-7c05c9ec6363
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269176(v=EXCHG.10)
ms:contentKeyID: 32765479
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 91f3db40fef483114313bbaa5f01e592d860bde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764553"
---
# <a name="jetendexternalbackup-function"></a>Função JetEndExternalBackup


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetendexternalbackup-function"></a>Função JetEndExternalBackup

A função **JetEndExternalBackup** encerra uma sessão de backup externo. Essa função é o último elemento de API em uma série de elementos de API que devem ser chamados para executar um backup online (não baseado em VSS) com êxito.

```cpp
    JET_ERR JET_API JetEndExternalBackup(void);
```

### <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

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
<td><p>JET_errNotInitialized</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP</p>
<p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer acesso a todos os dados revogados para proteger a integridade desses dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>A operação falhou porque nenhum backup externo está em andamento.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p><strong>Windows Server 2003:  </strong> Esse valor de retorno é introduzido no Windows Server 2003.</p>
<p>A operação falhou porque o backup externo atual foi anulado por uma chamada para <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</p></td>
</tr>
<tr class="odd">
<td><p>errBackupAbortByCaller</p></td>
<td><p><strong>Windows XP:  </strong> Esse valor de retorno é introduzido no Windows XP.</p>
<p>O chamador encerrou um backup no meio da sequência de backup sem sinalizar a intenção com <a href="gg294067(v=exchg.10).md">JetStopBackup</a>. Esse erro é resultado de um bug no cliente de backup no Windows Server 2003 e posterior. No Windows XP, esse erro é retornado para um encerramento intencional da sequência de backup externo.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>A operação falhou porque foi feita uma tentativa de usar o mecanismo no modo herdado (modo de compatibilidade do Windows 2000) em que há suporte para apenas uma instância, quando, na verdade, várias instâncias já existem.</p></td>
</tr>
</tbody>
</table>


Se essa função for bem-sucedida, o backup externo foi um sucesso. Êxito indica que todos os arquivos (por exemplo, bancos de dados e logs) apropriados para o tipo de backup (especificado em [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) foram recuperados do mecanismo de backup. Os arquivos de backup podem ser recuperados com a[JetExternalRestore](./jetexternalrestore-function.md)(recuperação de hardware).

Se essa função falhar, o backup externo geralmente termina. Falha significa que o backup é inválido devido a um erro de uso do cliente ou do aplicativo. É importante verificar o código de retorno dessa API para verificar se a sequência de backup foi bem-sucedida.

#### <a name="remarks"></a>Comentários

Se o mecanismo estiver configurado para registrar eventos, um evento será registrado para indicar a resolução do backup externo.

Se a sequência de backup não for concluída na ordem e com uma chamada bem-sucedida para **JetEndExternalBackup**, os backups incrementais subsequentes poderão conter mais dados do que o aplicativo previsto.

Para obter mais informações sobre a sequência de API de backup externo, consulte [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

Antes do Windows Vista, se o truncamento de log não foi feito, o mecanismo considerou que o backup era um backup de cópia. No entanto, o backup pode ser um backup normal para o qual o truncamento não foi feito (por exemplo, se houver bancos de dados desanexados). A opção JET_bitBackupTruncateDone pode ser usada para informar o mecanismo sobre isso e permitir modificações apropriadas no cabeçalho do banco de dados.

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

[Parâmetros de tratamento de erros](./error-handling-parameters.md)  
[Erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JET_ERR](./jet-err.md)  
[JetExternalRestore](./jetexternalrestore-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
