---
description: 'Saiba mais sobre: Função JetOSSnapshotTruncateLogInstance'
title: Função JetOSSnapshotTruncateLogInstance
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da5c999f9fcec38878f339cfb2a927c2be2e5b70
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479022"
---
# <a name="jetossnapshottruncateloginstance-function"></a>Função JetOSSnapshotTruncateLogInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetossnapshottruncateloginstance-function"></a>Função JetOSSnapshotTruncateLogInstance

A **função JetOSSnapshotTruncateLogInstance** trunca o log de uma instância especificada durante uma sessão de instantâneo.

**Windows Vista:****JetOSSnapshotTruncateLogInstance** é introduzido no Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*snapId*

O identificador da sessão de instantâneo.

*Instância*

A instância que será usada para essa chamada.

*grbit*

As opções para essa chamada. Esse parâmetro pode ter uma combinação dos valores a seguir.

*grbit* pode ser um dos seguintes valores:


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
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>A sessão de instantâneo não está no estado em que um truncamento pode ocorrer. Causas possíveis:</p><ul><li><p>A chamada é concluída depois que a sessão de instantâneo foi concluída.</p></li><li><p>A sessão foi especificada como um instantâneo de cópia.</p></li></ul> | 



Se essa função for bem-sucedida, os arquivos de log de uma ou todas as instâncias que fazem parte da sessão de instantâneo serão truncados, se possível.

#### <a name="remarks"></a>Comentários

Essa função deverá ser chamada somente se o instantâneo tiver sido criado com a JET_bitContinueAfterThaw opção . Caso contrário, a sessão de instantâneo termina após a chamada para [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erro](./error-handling-parameters.md)  
[Erros extensíveis Armazenamento mecanismo](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
