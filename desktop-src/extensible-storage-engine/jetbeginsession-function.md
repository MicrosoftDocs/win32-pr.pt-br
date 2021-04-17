---
description: 'Saiba mais sobre: função JetBeginSession'
title: Função JetBeginSession
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfe0cf06e86b19d16284b704697c65b1f38a167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785254"
---
# <a name="jetbeginsession-function"></a>Função JetBeginSession


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetbeginsession-function"></a>Função JetBeginSession

A função **JetBeginSession** inicia uma sessão e inicializa e retorna um identificador de sessão do ESE ([JET_SESID](./jet-sesid.md)). As sessões controlam todo o acesso ao banco de dados e são usadas para controlar o escopo das transações. A sessão pode ser usada para iniciar, confirmar ou anular transações. A sessão também é usada para anexar, criar ou abrir um banco de dados. A sessão é usada como contexto para todas as operações DDL e DML. Para aumentar a simultaneidade e o acesso paralelo ao banco de dados, várias sessões podem ser iniciadas.

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância do banco de dados a ser usada para esta chamada.

*psesid*

Ponteiro para a variável que o identificador de sessão Inicializa no retorno bem-sucedido.

*szUserName*

Esse parâmetro é reservado.

*szPassword*

Esse parâmetro é reservado.

### <a name="return-value"></a>Valor Retornado

Essa função permite o retorno de qualquer [JET_ERR](./jet-err.md)s que são definidos nesta API. Para obter mais informações sobre erros do Jet, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

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
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p>Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>A operação falhou porque não foi possível alocar memória.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSessions</p></td>
<td><p>O número de sessões que o mecanismo permitirá que o cliente inicie é limitado. Esse valor pode ser alterado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com a constante JET_paramMaxSessions. O número padrão de sessões é 16. Consulte <a href="gg294139(v=exchg.10).md">parâmetros do sistema</a> para obter detalhes sobre JET_paramMaxSessions.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, o identificador de sessão é inicializado e pode ser usado para operações de banco de dados.

Em caso de falha, não há sessões disponíveis ou não foi possível inicializar uma nova sessão.

#### <a name="remarks"></a>Comentários

É necessário usar atenção cuidadosa ao usar sessões em threads diferentes. Uma sessão controla em qual thread ele foi usado durante [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md)ou [JetRollback](./jetrollback-function.md), e gerará um erro se usado em vários threads com uma transação aberta. O [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) pode alterar esse comportamento. Como a sessão ainda é um contexto serializado, e várias operações de banco de dados não podem ser executadas em uma única sessão simultaneamente, apenas em série. No entanto, você pode usar várias sessões para obter acesso simultâneo ao banco de dados. As sessões podem ser usadas dentro de uma transação entre threads definindo e redefinindo os contextos de sessão.

O identificador de sessão deve ser fechado com [JetEndSession](./jetendsession-function.md).

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetBeginSessionW</strong> (Unicode) e <strong>JetBeginSessionA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetDupSession](./jetdupsession-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
