---
description: 'Saiba mais sobre: Função JetOSSnapshotThaw'
title: Função JetOSSnapshotThaw
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9be4bcff435fe30186b3b7585c79e3066987cc5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479052"
---
# <a name="jetossnapshotthaw-function"></a>Função JetOSSnapshotThaw


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetossnapshotthaw-function"></a>Função JetOSSnapshotThaw

A **função JetOSSnapshotThaw** notifica o mecanismo de que ele pode retomar operações normais de E/S após um período de congelamento e um instantâneo bem-sucedido.

**Windows XP:****JetOSSnapshotThaw** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*snapId*

O identificador da sessão de instantâneo.

*grbit*

Esse parâmetro é reservado para uso futuro e o único valor válido com suporte é 0.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>A sessão de instantâneo é inválida ou o <em>parâmetro grbit</em> é inválido.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>A sessão de instantâneo tinha um tempo decorrida internamente antes da chamada. Consequentemente, as operações de E/S retornaram ao normal antes que essa chamada fosse feita.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>O identificador da sessão de instantâneo não é válido.</p> | 



Se essa função for bem-sucedida, uma sessão de instantâneo será finalizada e o comportamento normal do mecanismo será retomado. Uma nova sessão de instantâneo pode ser iniciada posteriormente.

Se essa função falhar, a sessão de instantâneo atual terminará, mas o congelamento de E/S durante o período de instantâneo não foi respeitado internamente.

#### <a name="remarks"></a>Comentários

As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)
