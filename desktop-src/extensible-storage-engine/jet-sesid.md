---
description: 'Saiba mais sobre: JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da7acc706017c0346e5a701144d60bcbbfd7cf40
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983789"
---
# <a name="jet_sesid"></a>JET_SESID


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_sesid"></a>JET_SESID

O **JET_SESID** de dados contém um identificador para a sessão a ser usada para uma chamada à API jet.

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>Tipos de dados

JET_SESID

NULL  ou [JET_sesidNil](./invalid-handle-constants.md) pode ser usado para indicar um alça de sessão inválido.

### <a name="remarks"></a>Comentários

Uma sessão é o contexto de transação do mecanismo de banco de dados. Ele pode ser usado para iniciar, fazer commit ou anular transações que afetam a visibilidade e a durabilidade das alterações feitas por esta ou outras sessões.

Uma transação pode ser iniciada usando [JetBeginTransaction](./jetbegintransaction-function.md). Uma sessão pode ser criada usando [JetBeginSession](./jetbeginsession-function.md). O número máximo de sessões que podem ser criadas a qualquer momento é controlado pelo [JET_paramMaxSessions](./resource-parameters.md), que pode ser configurado por meio de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Uma sessão é encerrada explicitamente por uma chamada para [JetEndSession](./jetendsession-function.md) ou termina implicitamente por uma chamada para [JetTerm](./jetterm-function.md).

Cada sessão só pode ser usada por um thread por vez. Além disso, o comportamento padrão do mecanismo é restringir o uso de uma sessão para o mesmo thread desde o momento em que a primeira chamada para [JetBeginTransaction](./jetbegintransaction-function.md) é feita até o momento em que a chamada correspondente para [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) é feita. Esse comportamento pode ser alterado para remover essa segunda restrição definindo um contexto de sessão personalizado usando [JetSetSessionContext](./jetsetsessioncontext-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_paramMaxSessions](./resource-parameters.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionContext](./jetsetsessioncontext-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
