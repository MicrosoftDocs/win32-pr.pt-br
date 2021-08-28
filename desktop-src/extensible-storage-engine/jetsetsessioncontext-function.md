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
ms.openlocfilehash: 7ac368caaff5ec652a6dc7ad490e7418e62888b7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986629"
---
# <a name="jetsetsessioncontext-function"></a>Função JetSetSessionContext


_**Aplica-se a:** Windows | Windows Servidor_

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

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários valores de parâmetro gerou um resultado inesperado. Esse erro será retornado por <strong>JetSetSessionContext</strong> sob as seguintes condições:</p><ul><li><p><em>ulContext</em> é nulo</p></li><li><p><em>ulContext</em> é-1</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionContextAlreadySet</p> | <p>Não foi possível associar a sessão ao thread atual porque ela já foi associada a um thread.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p> | 



Se essa função for realizada com sucesso, a sessão será associada ao thread atual. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, o estado da sessão permanecerá inalterado. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Geralmente, uma sessão é associada a um thread específico durante uma transação. Esse comportamento foi projetado para ajudar os aplicativos a detectar e impedir o compartilhamento de uma única sessão informada de forma conceitual entre vários threads. Às vezes, essa verificação simples não funciona com a arquitetura do aplicativo. Por exemplo, se o aplicativo estiver hospedando objetos do lado do servidor usando um pool de threads e as transações abrangerem várias chamadas de servidor para um determinado objeto, essa proteção poderá fazer com que algumas dessas chamadas falhem com JET_errSessionSharingViolation embora o padrão de uso esteja correto. Essa situação é comum para servidores de objetos COM.

**JetSetSessionContext** e [JetResetSessionContext](./jetresetsessioncontext-function.md) resolvem esse problema tornando a verificação de compartilhamento de sessão um pouco mais flexível. Quando o aplicativo começa a fazer uma série de chamadas de API do ESE usando uma sessão específica, ele primeiro define o contexto da sessão para um determinado valor. Essa ação associa a sessão ao thread de chamada. No exemplo fornecido, esse contexto pode ser o endereço do objeto que contém o identificador de sessão do JET. Depois que as chamadas à API do ESE tiverem sido feitas, o aplicativo redefinirá o contexto da sessão. Essa ação desassocia a sessão do thread de chamada. O objeto e sua sessão podem ser usados por outro thread, mesmo que a sessão tenha uma transação ativa.

É importante observar que **JetSetSessionContext** deve ser chamado antes da abertura de uma transação nessa sessão, ou a associação não funcionará.

**JetSetSessionContext** é thread-safe. Vários threads podem tentar definir um contexto de thread na mesma sessão ao mesmo tempo e apenas um ganhará. Esse fato pode ser usado pelo aplicativo como um meio de alocar uma sessão de um pool sem armazenar o estado externo sobre sua alocação.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[JetStopService](./jetstopservice-function.md)
