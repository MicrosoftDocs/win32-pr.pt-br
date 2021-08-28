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
ms.openlocfilehash: 60920995e72fdc1f45dcc6c083be7bcc1a91b3fa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466403"
---
# <a name="jet_sesid"></a>JET_SESID


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_sesid"></a>JET_SESID

O tipo de dados **JET_SESID** contém um identificador para a sessão a ser usado para uma chamada para a API do Jet.

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>Tipos de dados

JET_SESID

**Nulo** ou [JET_sesidNil](./invalid-handle-constants.md) pode ser usado para indicar um identificador de sessão inválido.

### <a name="remarks"></a>Comentários

Uma sessão é o contexto de transação do mecanismo de banco de dados. Ele pode ser usado para iniciar, confirmar ou anular transações que afetam a visibilidade e a durabilidade das alterações feitas por esta ou outras sessões.

Uma transação pode ser iniciada usando [JetBeginTransaction](./jetbegintransaction-function.md). Uma sessão pode ser criada usando [JetBeginSession](./jetbeginsession-function.md). O número máximo de sessões que podem ser criadas a qualquer momento é controlado por [JET_paramMaxSessions](./resource-parameters.md), que pode ser configurado por meio de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Uma sessão é encerrada explicitamente por uma chamada para [JetEndSession](./jetendsession-function.md) ou encerrada implicitamente por uma chamada para [JetTerm](./jetterm-function.md).

Cada sessão só pode ser usada por um thread por vez. Além disso, o comportamento padrão do mecanismo é restringir o uso de uma sessão para o mesmo thread a partir do momento em que a primeira chamada para [JetBeginTransaction](./jetbegintransaction-function.md) é feita até o momento em que a chamada de correspondência para [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) é feita. Esse comportamento pode ser alterado para remover essa segunda restrição definindo um contexto de sessão personalizado usando [JetSetSessionContext](./jetsetsessioncontext-function.md) e [JetResetSessionContext](./jetresetsessioncontext-function.md).

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



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
