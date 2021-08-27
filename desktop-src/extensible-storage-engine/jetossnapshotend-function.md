---
description: 'Saiba mais sobre: Função JetOSSnapshotEnd'
title: Função JetOSSnapshotEnd
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b57528899b8d78ecee31f6dd54c2ac8decece383
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984429"
---
# <a name="jetossnapshotend-function"></a>Função JetOSSnapshotEnd


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetossnapshotend-function"></a>Função JetOSSnapshotEnd

A **função JetOSSnapshotEnd** notifica o mecanismo de que a sessão de instantâneo foi concluída.

**Windows Vista:****JetOSSnapshotEnd** é introduzido no Windows Vista:.  

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*snapId*

O identificador da sessão de instantâneo.

*grbit*

As opções para essa chamada. Esse parâmetro pode ter uma combinação dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>0</p> | <p>O fim bem-sucedido da sessão de instantâneo.</p> | 
| <p>JET_bitAbortSnapshot</p> | <p>A sessão de instantâneo anulada.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) tipo de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>Uma das opções solicitadas é inválida, usada incorretamente ou não implementada.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Uma sessão de instantâneo já está em andamento. Isso não é permitido.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>O identificador da sessão de instantâneo não é válido.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>A sessão de instantâneo tinha um tempo decorrida internamente antes da chamada. Como resultado, as operações de E/S retornaram ao normal antes que essa chamada fosse feita.</p> | 



Se essa função for bem-sucedida, uma sessão de instantâneo será concluída e o comportamento normal do mecanismo será retomado. Uma nova sessão de instantâneo pode ser iniciada posteriormente.

Se essa função falhar, o JET_errOSSnapshotTimeOut retornará e a sessão de instantâneo atual terminará, mas o congelamento de E/S durante o período de instantâneo não foi respeitado internamente. Para todos os outros erros, o estado da sessão de instantâneo não será alterado.

#### <a name="remarks"></a>Comentários

Essa função será chamada somente se [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) tiver sido chamado com JET_bitContinueAfterThaw.

A sessão de instantâneo deve ser concluída para que a verificação de instantâneo e o truncamento de log ocorrem. As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erro](./error-handling-parameters.md)  
[Erros extensíveis Armazenamento mecanismo](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
