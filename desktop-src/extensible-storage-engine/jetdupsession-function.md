---
description: 'Saiba mais sobre: Função JetDupSession'
title: Função JetDupSession
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c22be08630c446f6c5ba106b38be6bc24415325
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466623"
---
# <a name="jetdupsession-function"></a>Função JetDupSession


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdupsession-function"></a>Função JetDupSession

A **função JetDupSession** inicia uma sessão e inicializa e retorna um handle de sessão ESE ([JET_SESID](./jet-sesid.md)). As sessões controlam todo o acesso ao banco de dados e são usadas para controlar o escopo das transações. A sessão pode ser usada para iniciar, fazer commit ou anular transações. A sessão também é usada para anexar, criar ou abrir um banco de dados. A sessão é usada como o contexto para todas as operações DDL e DML. Para aumentar a simultrreidade e o acesso paralelo ao banco de dados, várias sessões podem ser iniciadas.

**Observação** Essa API atuará de todas as maneiras como [uma JetBeginSession](./jetbeginsession-function.md) chamada na instância da sessão passada. Essa função não é recomendada, [JetBeginSession](./jetbeginsession-function.md) é preferencial.

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada como a origem para duplicar ou iniciar a sessão.

*psesid*

Um ponteiro para a variável que o alça de sessão inicializa no retorno bem-sucedido.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errOutOfMemory</p> | <p>A operação falhou porque não foi possível alocar memória.</p> | 
| <p>JET_errOutOfSessions</p> | <p>O número de sessões que o mecanismo permitirá que o cliente inicie é limitado. Esse valor pode ser alterado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> com a <em>JET_paramMaxSessions</em> constante. O número padrão de sessões é 16. Consulte <a href="gg294139(v=exchg.10).md">Parâmetros do sistema</a> para obter detalhes sobre <em>JET_paramMaxSessions</em>.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 



Em caso de êxito, o alça de sessão é inicializado e pode ser usado para operações de banco de dados.

Em caso de falha, não há sessões disponíveis ou uma nova sessão não pôde ser inicializada.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
