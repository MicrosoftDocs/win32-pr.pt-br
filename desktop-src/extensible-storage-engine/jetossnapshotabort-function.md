---
description: 'Saiba mais sobre: Função JetOSSnapshotAbort'
title: Função JetOSSnapshotAbort
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08e56bc95798559453c383549570f9470b55fa82
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474412"
---
# <a name="jetossnapshotabort-function"></a>Função JetOSSnapshotAbort


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetossnapshotabort-function"></a>Função JetOSSnapshotAbort

A **função JetOSSnapshotAbort** notifica o mecanismo de que ele pode retomar operações normais de E/S após um período de congelamento terminar com um instantâneo com falha.

**Windows Server 2003:****JetOSSnapshotAbort** foi introduzido no Windows Server 2003.  

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*snapId*

O identificador da sessão de instantâneo.

*grbit*

As opções para essa chamada. Esse parâmetro é reservado para uso futuro e o único valor válido com suporte é 0 (zero).

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>A sessão de instantâneo é inválida ou o parâmetro grbit é inválido.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>O identificador da sessão de instantâneo não é válido.</p> | 



Se essa função for bem-sucedida, a sessão de instantâneo será finalizada e o comportamento normal do mecanismo será retomado. Uma nova sessão de instantâneo pode ser iniciada em um ponto posterior.

Se essa função falhar, a sessão de instantâneo não será anulada.

#### <a name="remarks"></a>Comentários

Essa função deve ser chamada em vez de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) para informar o mecanismo de que o instantâneo foi anulado por motivos que não estão relacionados ao mecanismo. Essas informações podem ser usadas posteriormente para ajudar a emitir mensagens de log de eventos sobre a sessão de instantâneo ou para ajudar a determinar outras ações apropriadas.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
