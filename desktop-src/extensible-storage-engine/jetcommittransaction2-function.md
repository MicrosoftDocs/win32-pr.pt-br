---
description: 'Saiba mais sobre: Função JetCommitTransaction2'
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
ms.openlocfilehash: 697a3760dc3312230bb2fe755dbfc881c1fdbacd7d21c98e64d8aa83a271ecdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118251368"
---
# <a name="jetcommittransaction2-function"></a>Função JetCommitTransaction2


_**Aplica-se a:** Windows | Windows Servidor_

A **função JetCommitTransaction2** confirma as alterações feitas no estado do banco de dados durante o ponto de economia atual e as migra para o ponto de economia anterior. Se o ponto de economia mais externo for confirmado, as alterações feitas durante esse ponto de salvar serão comprometidas no estado do banco de dados e a sessão sairá da transação.

A **função JetCommitTransaction2** foi introduzida no Windows 8 operacional.

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

A sessão a ser usada para essa chamada.

*grbit*

Um grupo de bits que especificam zero ou mais dos valores listados na tabela a seguir.

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
<td><p>A transação é comprometida normalmente, mas essa API não aguarda a liberação da transação para o arquivo de log de transações antes de retornar ao chamador. Isso reduz drasticamente a duração de uma operação de confirmação às custas da durabilidade. Qualquer transação que não for liberado para o log antes de uma falha será anulada automaticamente durante a recuperação de falha durante a próxima chamada para a <a href="gg294068(v=exchg.10).md">função JetInit.</a></p>
<p>Se JET_bitWaitLastLevel0Commit ou JET_bitWaitAllLevel0Commit for especificado, essa opção será ignorada.</p>
<p>Se essa chamada para <strong>JetCommitTransaction2</strong> não corresponder à primeira chamada à <a href="gg294083(v=exchg.10).md">função JetBeginTransaction</a> para esta sessão, essa opção será ignorada. Isso ocorre porque a ação final que ocorre no ponto de salvar mais externo é o fator determinante em se toda a transação é realmente comprometida no disco.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWaitAllLevel0Commit</p></td>
<td><p>Todas as transações confirmadas anteriormente por qualquer sessão que ainda não foram liberados para o arquivo de log de transações serão liberados imediatamente. Essa API aguardará até que as transações tenham sido liberados antes de retornar ao chamador.</p>
<p>Essa opção pode ser usada mesmo se a sessão não estiver atualmente em uma transação.</p>
<p>Essa opção não pode ser usada em combinação com qualquer outra opção.</p>
<p>Essa opção está disponível em versões do sistema operacional Windows Server a partir do Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitWaitLastLevel0Commit</p></td>
<td><p>Se a sessão tiver confirmado transações anteriormente e elas ainda não foram liberados para o arquivo de log de transações, elas deverão ser liberados imediatamente. Essa API aguardará até que as transações tenham sido liberados antes de retornar ao chamador. Isso será útil se o aplicativo já tiver confirmado várias transações usando JET_bitCommitLazyFlush e agora quiser liberar todas elas para o disco.</p>
<p>Essa opção pode ser usada mesmo se a sessão não estiver atualmente em uma transação.</p>
<p>Essa opção não pode ser usada em combinação com qualquer outra opção.</p></td>
</tr>
</tbody>
</table>


*cmsecDurableCommit*

A duração para fazer commit de uma transação lento.

*pCommitID*

A ID de confirmação associada a esse registro de confirmação.

### <a name="return-value"></a>Retornar valor

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno listados na tabela a seguir. Para obter mais informações sobre os possíveis erros de ESE (Extensible Armazenamento Engine), consulte [Extensible Armazenamento Engine Error](./extensible-storage-engine-errors.md) [Handling Parameters](./error-handling-parameters.md).

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
<td><p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para a <a href="gg269240(v=exchg.10).md">função JetStopService.</a></p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p>Esse erro só será retornado por versões do sistema operacional Windows a partir do Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Uma das opções solicitadas era inválida ou não implementada. Esse erro será retornado pela função <strong>JetCommitTransaction2</strong> quando ocorrer o seguinte:</p>
<ul>
<li><p>Um <em>grbit ilegal</em> é especificado.</p></li>
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
<td><p>A operação falhou porque a sessão determinada não está em uma transação.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p>Esse erro só será retornado por versões do sistema operacional Windows a partir do Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p></td>
</tr>
</tbody>
</table>


Em caso de êxito, todas as alterações feitas no banco de dados durante o ponto de economia atual para a sessão determinada serão confirmados e esse ponto de salvar será encerrado. Se o último ponto de salvar para a sessão tiver sido encerrado, a transação opcionalmente será liberado para o arquivo de log de transações e a sessão sairá da transação.

Em caso de falha, o estado transacional da sessão permanecerá inalterado. Nenhuma alteração no estado do banco de dados ocorrerá. O aplicativo deve chamar a [função JetRollback](./jetrollback-function.md) para anular a transação.

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
<td><p>Requer Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Veja também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
