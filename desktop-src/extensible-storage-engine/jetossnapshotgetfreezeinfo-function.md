---
description: 'Saiba mais sobre: função JetOSSnapshotGetFreezeInfo'
title: Função JetOSSnapshotGetFreezeInfo
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e737d6fe31dde43eeba7526e740ec096db20abc9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466203"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a>Função JetOSSnapshotGetFreezeInfo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetossnapshotgetfreezeinfo-function"></a>Função JetOSSnapshotGetFreezeInfo

A função **JetOSSnapshotGetFreezeInfo** recupera a lista de instâncias e bancos de dados que fazem parte da sessão de instantâneo em um determinado momento.

**Windows vista:** o **JetOSSnapshotGetFreezeInfo** é introduzido no Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*snapid*

O identificador da sessão de instantâneo a ser iniciada.

*pcInstanceInfo*

O número de instâncias em execução no momento que fazem parte da sessão de instantâneo.

*paInstanceInfo*

Uma matriz de estruturas, uma para cada instância em execução, descrevendo a instância e os bancos de dados que fazem parte dela.

*grbit*

As opções para esta chamada. Esse parâmetro é reservado para uso futuro. O único valor válido é 0 (zero).

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errOutOfMemory</p> | <p>A função falhou devido a uma condição de memória insuficiente.</p> | 
| <p>JET_errInvalidParameter</p> | <p><em>pcInstanceInfo</em> ou <em>paInstanceInfo</em> é <strong>nulo</strong>.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>O identificador da sessão de instantâneo não é válido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Uma sessão de instantâneo não está em andamento.</p> | 



Se essa função for bem sucedido, as informações da instância serão preenchidas corretamente e deverão ser liberadas mais tarde chamando [JetFreeBuffer](./jetfreebuffer-function.md) com o ponteiro para a matriz de informações da instância que foi retornada.

Se essa função falhar, nenhuma alteração no estado do mecanismo ocorrerá.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows Server 2008.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) e <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erros](./error-handling-parameters.md)  
[erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
