---
description: 'Saiba mais sobre: função JetCommitTransaction2'
title: Função JetCommitTransaction2
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24dfecd091de027f51ed8f69c0441fbc7cbd57af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812362"
---
# <a name="jetcommittransaction2-function"></a>Função JetCommitTransaction2


_**Aplica-se a:** Windows | Windows Server_

A função **JetCommitTransaction2** confirma as alterações feitas no estado do banco de dados durante o ponto de salvamento atual e os migra para o ponto de salvamento anterior. Se o ponto de salvamento mais externo for confirmado, as alterações feitas durante esse ponto de salvamento serão confirmadas no estado do banco de dados e a sessão sairá da transação.

A função **JetCommitTransaction2** foi introduzida no sistema operacional Windows 8.

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*grbit*

Um grupo de bits que especifica zero ou mais valores listados na tabela a seguir.

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
<td><p>JET_bitCommitLazyFlush</p></td>
<td><p>A transação é confirmada normalmente, mas essa API não espera que a transação seja liberada para o arquivo de log de transações antes de retornar ao chamador. Isso reduz drasticamente a duração de uma operação de confirmação no custo da durabilidade. Qualquer transação que não seja liberada para o log antes de uma falha será abortada automaticamente durante a recuperação de falha durante a próxima chamada para a função <a href="gg294068(v=exchg.10).md">JetInit</a> .</p>
<p>Se JET_bitWaitLastLevel0Commit ou JET_bitWaitAllLevel0Commit forem especificadas, essa opção será ignorada.</p>
<p>Se essa chamada para <strong>JetCommitTransaction2</strong> não corresponder à primeira chamada para a função <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> para essa sessão, essa opção será ignorada. Isso acontece porque a ação final que ocorre no ponto de salvamento mais externo é o fator determinante em que toda a transação está realmente comprometida com o disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWaitAllLevel0Commit</p></td>
<td><p>Todas as transações confirmadas anteriormente por qualquer sessão que ainda não foram liberadas para o arquivo de log de transações serão liberadas imediatamente. Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador.</p>
<p>Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</p>
<p>Essa opção não pode ser usada em combinação com nenhuma outra opção.</p>
<p>Essa opção está disponível em versões do sistema operacional Windows Server a partir do Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitWaitLastLevel0Commit</p></td>
<td><p>Se a sessão tiver confirmado anteriormente quaisquer transações e elas ainda não tiverem sido liberadas para o arquivo de log de transações, elas deverão ser liberadas imediatamente. Essa API aguardará até que as transações sejam liberadas antes de retornar ao chamador. Isso será útil se o aplicativo tiver confirmado anteriormente várias transações usando JET_bitCommitLazyFlush e agora quiser liberar todas elas para o disco.</p>
<p>Essa opção pode ser usada mesmo que a sessão não esteja em uma transação no momento.</p>
<p>Essa opção não pode ser usada em combinação com nenhuma outra opção.</p></td>
</tr>
</tbody>
</table>


*cmsecDurableCommit*

A duração da confirmação de uma transação lenta.

*pCommitID*

A ID de confirmação associada a este registro de confirmação.

### <a name="return-value"></a>Retornar valor

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir. Para obter mais informações sobre os possíveis erros do ESE (mecanismo de armazenamento extensível), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

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
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para a função <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p>Esse erro só será retornado pelas versões do sistema operacional Windows a partir do Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Uma das opções solicitadas era inválida ou não foi implementada. Esse erro será retornado pela função <strong>JetCommitTransaction2</strong> quando ocorrer o seguinte:</p>
<ul>
<li><p>Um <em>grbit</em> inválido foi especificado.</p></li>
<li><p>JET_bitWaitLastLevel0Commit foi especificado em combinação com outro <em>grbit</em>.</p></li>
<li><p>JET_bitWaitAllLevel0Commit foi especificado em combinação com outro <em>grbit</em>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>A operação falhou porque a sessão especificada não está em uma transação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p>Esse erro só será retornado pelas versões do sistema operacional Windows a partir do Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, as alterações feitas no banco de dados durante o ponto de salvamento atual para a sessão especificada serão confirmadas e o ponto de salvamento será encerrado. Se o último ponto de salvamento da sessão for encerrado, a transação será, opcionalmente, liberada para o arquivo de log de transações e a sessão sairá da transação.

Se houver falha, o estado transacional da sessão permanecerá inalterado. Nenhuma alteração no estado do banco de dados ocorrerá. O aplicativo deve chamar a função [JetRollback](./jetrollback-function.md) para anular a transação.

#### <a name="remarks"></a>Comentários

Deve haver uma chamada para **JetCommitTransaction2** ou [JetRollback](./jetrollback-function.md) para corresponder a cada chamada para [JetBeginTransaction](./jetbegintransaction-function.md) para uma determinada sessão.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2012.</p></td>
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


#### <a name="see-also"></a>Confira também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
