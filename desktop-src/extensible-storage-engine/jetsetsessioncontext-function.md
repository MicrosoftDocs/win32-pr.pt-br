---
description: 'Saiba mais sobre: Função JetSetSessionContext'
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
ms.openlocfilehash: 61df6b5396a5bffcef4f7e32e9a2c32477d019e0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465283"
---
# <a name="jetsetsessioncontext-function"></a>Função JetSetSessionContext


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetsetsessioncontext-function"></a>Função JetSetSessionContext

A **função JetSetSessionContext** associa uma sessão ao thread atual usando o alça de contexto determinado. Essa associação substitui o requisito de mecanismo padrão de que uma transação para uma determinada sessão deve ocorrer inteiramente no mesmo thread.

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*ulContext*

Um identificador exclusivo ao qual esta sessão será associada.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro gerou um resultado inesperado. Esse erro será retornado por <strong>JetSetSessionContext nas</strong> seguintes condições:</p><ul><li><p><em>ulContext</em> é NULL</p></li><li><p><em>ulContext</em> é -1</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionContextAlreadySet</p> | <p>A sessão não pôde ser associada ao thread atual porque ela já foi associada a um thread.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo fechada.</p> | 



Se essa função for bem-sucedida, a sessão será associada ao thread atual. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, o estado da sessão permanecerá inalterado. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Uma sessão geralmente é vinculada a um thread específico durante uma transação. Esse comportamento foi projetado para ajudar os aplicativos a detectar e impedir o compartilhamento conceitualmente mal-aconselhado de uma única sessão entre vários threads. Às vezes, essa verificação simples não funciona com a arquitetura do aplicativo. Por exemplo, se o aplicativo estiver hospedando objetos do lado do servidor usando um pool de threads e as transações abrangem várias chamadas de servidor para um determinado objeto, essa proteção poderá fazer com que algumas dessas chamadas falhem com JET_errSessionSharingViolation mesmo que o padrão de uso seja correto. Essa situação é comum para servidores de objeto COM.

**JetSetSessionContext** e [JetResetSessionContext](./jetresetsessioncontext-function.md) resolvem esse problema, tornando essa verificação de compartilhamento de sessão um pouco mais flexível. Quando o aplicativo começa a fazer uma série de chamadas à API de ESE usando uma sessão específica, ele primeiro define o contexto de sessão para um determinado valor. Essa ação associa a sessão ao thread de chamada. No exemplo determinado, esse contexto pode ser o endereço do objeto que contém o identificador de sessão JET. Depois que as chamadas à API do ESE são feitas, o aplicativo redefine o contexto de sessão. Essa ação desassocia a sessão do thread de chamada. O objeto e sua sessão poderão ser usados por outro thread mesmo que a sessão tenha uma transação ativa.

É importante observar que **JetSetSessionContext** deve ser chamado antes de abrir uma transação nessa sessão ou a associação não funcionará.

**JetSetSessionContext** é thread-safe. Vários threads podem tentar definir um contexto de thread na mesma sessão ao mesmo tempo e apenas um vencerá. Esse fato pode ser usado pelo aplicativo como um meio de alocar uma sessão de um pool sem armazenar o estado externo sobre sua alocação.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[JetStopService](./jetstopservice-function.md)
