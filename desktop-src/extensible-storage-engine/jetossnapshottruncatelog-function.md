---
description: 'Saiba mais sobre: Função JetOSSnapshotTruncateLog'
title: Função JetOSSnapshotTruncateLog
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4da8e76b1c735f6249f1d7e3893acd1db1743b65
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985859"
---
# <a name="jetossnapshottruncatelog-function"></a>Função JetOSSnapshotTruncateLog


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetossnapshottruncatelog-function"></a>Função JetOSSnapshotTruncateLog

A **função JetOSSnapshotTruncateLog** permite o truncamento de log para todas as instâncias que fazem parte da sessão de instantâneo.

**Windows Vista:****JetOSSnapshotTruncateLog** é introduzido no Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
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
| <p>JET_bitAllDatabasesSnapshot</p> | <p>Todos os bancos de dados são anexados para que o mecanismo de armazenamento possa calcular e fazer o truncamento de log.</p> | 
| <p>0 (zero)</p> | <p>Nenhum truncamento ocorrerá.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidGrbit</p> | <p>O <em>parâmetro grbit</em> é inválido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>A sessão de instantâneo não está no estado em que um truncamento pode ocorrer. Causas possíveis:</p><ul><li><p>a chamada é feita após a sessão de instantâneo ter terminado</p></li><li><p>a sessão foi especificada como um instantâneo de cópia</p></li></ul> | 



Em caso de êxito, os arquivos de log de uma ou todas as instâncias que fazem parte da sessão de instantâneo serão truncados, se possível.

#### <a name="remarks"></a>Comentários

Essa função deverá ser chamada somente se o instantâneo tiver sido criado com a JET_bitContinueAfterThaw opção. Caso contrário, a sessão de instantâneo teria terminado após a [chamada JetOSSnapshotThaw.](./jetossnapshotthaw-function.md)

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
[Erros de mecanismo Armazenamento extensível](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
