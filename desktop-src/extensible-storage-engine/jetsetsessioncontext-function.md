---
description: 'Saiba mais sobre: função JetSetSessionContext'
title: Função JetSetSessionContext
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4aafafa17499b76282599586f7477ac1ef6f878d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815593"
---
# <a name="jetsetsessioncontext-function"></a>Função JetSetSessionContext


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetsetsessioncontext-function"></a>Função JetSetSessionContext

A função **JetSetSessionContext** associa uma sessão ao thread atual usando o identificador de contexto fornecido. Essa associação substitui o requisito de mecanismo padrão que uma transação para uma determinada sessão deve ocorrer inteiramente no mesmo thread.

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*ulContext*

Um identificador exclusivo ao qual esta sessão será associada.

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
<td><p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro gerou um resultado inesperado. Esse erro será retornado por <strong>JetSetSessionContext</strong> sob as seguintes condições:</p>
<ul>
<li><p><em>ulContext</em> é nulo</p></li>
<li><p><em>ulContext</em> é-1</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionContextAlreadySet</p></td>
<td><p>Não foi possível associar a sessão ao thread atual porque ela já foi associada a um thread.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
</tbody>
</table>


Se essa função for realizada com sucesso, a sessão será associada ao thread atual. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, o estado da sessão permanecerá inalterado. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Geralmente, uma sessão é associada a um thread específico durante uma transação. Esse comportamento foi projetado para ajudar os aplicativos a detectar e impedir o compartilhamento de uma única sessão informada de forma conceitual entre vários threads. Às vezes, essa verificação simples não funciona com a arquitetura do aplicativo. Por exemplo, se o aplicativo estiver hospedando objetos do lado do servidor usando um pool de threads e as transações abrangerem várias chamadas de servidor para um determinado objeto, essa proteção poderá fazer com que algumas dessas chamadas falhem com JET_errSessionSharingViolation embora o padrão de uso esteja correto. Essa situação é comum para servidores de objetos COM.

**JetSetSessionContext** e [JetResetSessionContext](./jetresetsessioncontext-function.md) resolvem esse problema tornando a verificação de compartilhamento de sessão um pouco mais flexível. Quando o aplicativo começa a fazer uma série de chamadas de API do ESE usando uma sessão específica, ele primeiro define o contexto da sessão para um determinado valor. Essa ação associa a sessão ao thread de chamada. No exemplo fornecido, esse contexto pode ser o endereço do objeto que contém o identificador de sessão do JET. Depois que as chamadas à API do ESE tiverem sido feitas, o aplicativo redefinirá o contexto da sessão. Essa ação desassocia a sessão do thread de chamada. O objeto e sua sessão podem ser usados por outro thread, mesmo que a sessão tenha uma transação ativa.

É importante observar que **JetSetSessionContext** deve ser chamado antes da abertura de uma transação nessa sessão, ou a associação não funcionará.

**JetSetSessionContext** é thread-safe. Vários threads podem tentar definir um contexto de thread na mesma sessão ao mesmo tempo e apenas um ganhará. Esse fato pode ser usado pelo aplicativo como um meio de alocar uma sessão de um pool sem armazenar o estado externo sobre sua alocação.

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

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[JetStopService](./jetstopservice-function.md)
