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
ms.openlocfilehash: e6c26aa69f1ac51cdd9d70ca93c4fc42df5356ee
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987659"
---
# <a name="jetgetcursorinfo-function"></a>Função JetGetCursorInfo


_**Aplica-se a:** Windows | Windows Servidor_

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

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>O <em>cbMax</em> não é 0 (zero) ou <em>InfoLevel</em> não é 0 (zero).</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor não está atualmente em um registro e as informações em um registro lógico não podem ser retornadas como resultado.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 
| <p>JET_errWriteConflict</p> | <p>O registro atual do cursor foi atualizado por outra sessão e uma atualização desse registro por esta sessão resultará em um conflito de gravação.</p> | 



Em caso de sucesso, essa operação não tem efeito sobre o local do cursor, mas indica apenas que nenhuma outra sessão atualizou esse registro no momento.

Em caso de falha, se um código de erro negativo for retornado, não haverá efeitos para o cursor ou o banco de dados.

#### <a name="remarks"></a>Comentários

Esta operação não afeta o estado do cursor ou dos dados. Ele retorna apenas um código de erro que descreve se uma atualização para o registro atual pela sessão de chamada é conhecida por resultar em um JET_errWriteConflict ou é desconhecido para retornar JET_errWriteConflict. Se outra sessão já tiver atualizado esse registro para usá-lo, você terá certeza de que uma atualização desse registro por esta sessão resultará em um conflito de gravação. Isso será verdadeiro até que esta sessão confirme ou reverta suas transações para o nível de transação 0 (zero). No entanto, se **JetGetCursorInfo** retornar JET_errSuccess, ainda é possível que outra sessão atualize esse registro antes da sessão atual e, portanto, ainda é possível que uma atualização do registro atual por essa sessão em sua transação atual resulte em um conflito de gravação.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLock](./jetgetlock-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
