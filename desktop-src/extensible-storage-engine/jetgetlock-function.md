---
description: 'Saiba mais sobre: função JetGetLock'
title: Função JetGetLock
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5757616214336de25ce30ca49755ac229b10afbe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104092013"
---
# <a name="jetgetlock-function"></a>Função JetGetLock


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetgetlock-function"></a>Função JetGetLock

A função **JetGetLock** fornece um meio para reservar explicitamente a capacidade de atualizar uma linha, bloqueio de gravação ou impedir explicitamente que uma linha seja atualizada por qualquer outra sessão, bloqueio de leitura. Normalmente, os bloqueios de gravação de linha são adquiridos implicitamente como resultado da atualização de linhas. Os bloqueios de leitura geralmente não são necessários devido ao controle de versão de registro. No entanto, em alguns casos, uma transação pode desejar bloquear explicitamente uma linha para impor a serialização, ou para garantir que uma operação subsequente terá sucesso em virtude de que os bloqueios necessários já foram feitos.

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão que será usada para esta chamada.

*TableID*

O cursor que será usado para esta chamada.

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes:

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
<td><p>JET_bitReadLock</p></td>
<td><p>Esse sinalizador faz com que um bloqueio de leitura seja adquirido no registro atual. Os bloqueios de leitura são incompatíveis com os bloqueios de gravação já mantidos por outras sessões, mas são compatíveis com bloqueios de leitura mantidos por outras sessões.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWriteLock</p></td>
<td><p>Esse sinalizador faz com que um bloqueio de gravação seja adquirido no registro atual. Os bloqueios de gravação não são compatíveis com bloqueios de gravação ou leitura mantidos por outras sessões, mas são compatíveis com bloqueios de leitura mantidos pela mesma sessão.</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>O <em>grbit</em> fornecido não é JET_bitReadLock ou JET_bitWriteLock. Ele deve ser um desses dois sinalizadores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor deve estar em um registro para adquirir um bloqueio. Os bloqueios estão sempre em registros.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Os bloqueios só podem ser adquiridos por sessões em uma transação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>O cursor não pode ser somente leitura e adquirir um bloqueio de gravação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>A sessão deve ter permissões de gravação para adquirir o bloqueio de gravação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>O erro retornado quando um bloqueio conflitante é solicitado.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, a sessão adquiriu o bloqueio solicitado.

Em caso de falha, a sessão não adquiriu o bloqueio solicitado.

#### <a name="remarks"></a>Comentários

Os bloqueios de gravação não podem ser adquiridos com sessões ou cursores que têm permissões somente leitura, mesmo que a sessão e o cursor, em última instância, não executem uma operação de atualização. Tanto a sessão quanto o cursor devem ter privilégios de gravação para adquirir um bloqueio de gravação.

Bloqueios de leitura e gravação são um meio de bloqueio pessimista. O bloqueio pessimista espera que várias sessões simultâneas entrem em conflito e adquiram bloqueios antecipadamente para garantir que suas operações tenham sucesso.

A maioria das operações será serializável em virtude de bloqueios implicitamente feitos. No entanto, algumas operações não serão. Para ilustrar isso, considere as duas transações,

T1: R (A), U (B)

T2: R (B), U (A)

O controle de versão em nível de registro garantirá que cada transação, quando executada simultaneamente, verá os valores originais para A e B. Não há nenhuma ordem de série de execução que possa produzir os mesmos resultados para A e B no caso de os resultados dependerem dos dados lidos. Para que o aplicativo faça essa transação serializável, ele deve adquirir um bloqueio de leitura explícito em A e B em cada transação quando o valor for lido.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
