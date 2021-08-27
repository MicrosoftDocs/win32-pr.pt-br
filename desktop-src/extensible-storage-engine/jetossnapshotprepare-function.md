---
description: 'Saiba mais sobre: Função JetOSSnapshotPrepare'
title: Função JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 010cafd19ffde09b3083dd3cb6e6a69fa2268f11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470323"
---
# <a name="jetossnapshotprepare-function"></a>Função JetOSSnapshotPrepare


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetossnapshotprepare-function"></a>Função JetOSSnapshotPrepare

A **função JetOSSnapshotPrepare** inicia as preparações para uma sessão de instantâneo. Uma sessão de instantâneo é um intervalo de tempo curto no qual o mecanismo não em emitida nenhuma E/S de gravação no disco, para que o mecanismo possa participar de uma sessão de instantâneo de volume (quando controlado por um snapshot writer).

**Windows XP:****JetOSSnapshotPrepare** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*psnapId*

O identificador da sessão de instantâneo a ser iniciada.

*grbit*

As opções para essa chamada. Esse parâmetro pode ter uma combinação dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>0</p> | <p>Instantâneo normal.</p> | 
| <p>JET_bitIncrementalSnapshot</p> | <p>Somente arquivos de log serão tirados.</p> | 
| <p>JET_bitCopySnapshot</p> | <p>Um instantâneo de cópia (normal ou incremental) sem truncamento de log.</p> | 
| <p>JET_bitContinueAfterThaw</p> | <p>A sessão de instantâneo ocorre após <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> e exigirá uma chamada de função <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd.</a></p> | 
| <p>JET_bitExplicitPrepare</p> | <p>Nenhuma instância será preparada por padrão.</p><p><strong>Windows 7:</strong>  JET_bitExplicitPrepare é introduzido no Windows 7.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>O ponteiro de ID do instantâneo é NULL ou o <em>parâmetro grbit</em> é inválido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Uma sessão de instantâneo já está em andamento e a operação não tem permissão para ter mais de uma sessão de instantâneo em um determinado momento.</p> | 



Se essa função for bem-sucedida, uma sessão de instantâneo poderá iniciar a qualquer momento com a fase de congelamento de E/S. O identificador da sessão será retornado e deve ser usado nas chamadas subsequentes para a sessão de instantâneo.

As instâncias em execução do mecanismo agora serão consideradas parte da sessão de instantâneo.

**Windows Vista:**  Para especificar um subconjunto diferente de instâncias, [o JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) pode ser chamado.

A chamada de sequência de API normal é: **JetOSSnapshotPrepare**, opcionalmente seguido por uma ou mais chamadas para [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), seguido por [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Depois que o congelamento for iniciado, ele poderá ser encerrado usando [JetOSSnapshotThaw](./jetossnapshotthaw-function.md). A qualquer momento após a preparação, a sessão de instantâneo pode ser encerrada com [JetOSSnapshotAbort .](./jetossnapshotabort-function.md)

Se JET_bitContinueAfterThaw for especificado após [JetOSSnapshotThaw,](./jetossnapshotthaw-function.md)a sessão de instantâneo permanecerá (embora a E/S seja retomada). Isso habilitará uma verificação do instantâneo e, se necessário, habilitará o truncamento de log usando [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) e exigirá uma chamada para [JetOSSnapshotEnd](./jetossnapshotend-function.md).

Se essa função falhar, nenhuma alteração no estado do mecanismo ocorrerá.

#### <a name="remarks"></a>Comentários

As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)  
[JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md)
