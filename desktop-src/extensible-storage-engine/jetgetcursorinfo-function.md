---
description: 'Saiba mais sobre: função JetGetCursorInfo'
title: Função JetGetCursorInfo
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754066"
---
# <a name="jetgetcursorinfo-function"></a>Função JetGetCursorInfo


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetgetcursorinfo-function"></a>Função JetGetCursorInfo

A função **JetGetCursorInfo** é usada para determinar se uma atualização do registro atual de um cursor resultará em um conflito de gravação, com base no status de atualização atual do registro. É possível que um conflito de gravação seja retornado, mesmo se **JetGetCursorInfo** retornar JET_errSuccess, porque outra sessão pode atualizar o registro antes que a sessão atual seja capaz de atualizar o mesmo registro.

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão que será usada para esta chamada.

*TableID*

O cursor que será usado para esta chamada.

*pvResult*

Reservado para uso futuro.

*cbMax*

Deve ser definido como 0 (zero), caso contrário, não utilizado. Ele está presente para futuras funcionalidades.

*InfoLevel*

Deve ser definido como 0 (zero), caso contrário, não utilizado. Ele está presente para futuras funcionalidades.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>O <em>cbMax</em> não é 0 (zero) ou <em>InfoLevel</em> não é 0 (zero).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor não está atualmente em um registro e as informações em um registro lógico não podem ser retornadas como resultado.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
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
<td><p>JET_errWriteConflict</p></td>
<td><p>O registro atual do cursor foi atualizado por outra sessão e uma atualização desse registro por esta sessão resultará em um conflito de gravação.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, essa operação não tem efeito sobre o local do cursor, mas indica apenas que nenhuma outra sessão atualizou esse registro no momento.

Em caso de falha, se um código de erro negativo for retornado, não haverá efeitos para o cursor ou o banco de dados.

#### <a name="remarks"></a>Comentários

Esta operação não afeta o estado do cursor ou dos dados. Ele retorna apenas um código de erro que descreve se uma atualização para o registro atual pela sessão de chamada é conhecida por resultar em um JET_errWriteConflict ou é desconhecido para retornar JET_errWriteConflict. Se outra sessão já tiver atualizado esse registro para usá-lo, você terá certeza de que uma atualização desse registro por esta sessão resultará em um conflito de gravação. Isso será verdadeiro até que esta sessão confirme ou reverta suas transações para o nível de transação 0 (zero). No entanto, se **JetGetCursorInfo** retornar JET_errSuccess, ainda é possível que outra sessão atualize esse registro antes da sessão atual e, portanto, ainda é possível que uma atualização do registro atual por essa sessão em sua transação atual resulte em um conflito de gravação.

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
[JetGetLock](./jetgetlock-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
