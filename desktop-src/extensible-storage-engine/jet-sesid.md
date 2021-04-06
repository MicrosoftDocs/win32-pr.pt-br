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
ms.openlocfilehash: 542802c806bbea55aafb4fc1a0241a92b2842878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826934"
---
# <a name="jet_sesid"></a>JET_SESID


_**Aplica-se a:** Windows | Windows Server_

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
</tbody>
</table>


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
