---
description: 'Saiba mais sobre: função JetOSSnapshotPrepareInstance'
title: Função JetOSSnapshotPrepareInstance
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4997be8f268d676fbd4a164281061b488e948168
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474382"
---
# <a name="jetossnapshotprepareinstance-function"></a>Função JetOSSnapshotPrepareInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetossnapshotprepareinstance-function"></a>Função JetOSSnapshotPrepareInstance

A função **JetOSSnapshotPrepareInstance** seleciona uma instância específica para fazer parte da sessão de instantâneo.

**Windows vista:** o **JetOSSnapshotPrepareInstance** foi introduzido no Windows Vista.

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parâmetros

*snapid*

O identificador da sessão de instantâneo.

*cópia*

A instância que será usada para esta chamada.

*grbit*

As opções para esta chamada. Esse parâmetro é reservado para uso futuro. O único valor válido é 0 (zero).

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>O ponteiro da ID do instantâneo é <strong>nulo</strong> ou o parâmetro <em>grbit</em> é inválido.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Uma sessão de instantâneo já está em andamento.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>O identificador da sessão de instantâneo não é válido.</p> | 



Se essa função for realizada com sucesso, a instância especificada fará parte da sessão de instantâneo.

Se essa função falhar, nenhuma alteração no estado do mecanismo ocorrerá.

#### <a name="remarks"></a>Comentários

A chamada de sequência de API normal é: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), opcionalmente seguido por uma ou mais chamadas para **JetOSSnapshotPrepareInstance**, seguido por [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Quando o congelamento é iniciado, ele pode ser encerrado usando [JetOSSnapshotThaw](./jetossnapshotthaw-function.md). A qualquer momento após a preparação, a sessão de instantâneo pode ser encerrada abruptamente com [JetOSSnapshotAbort](./jetossnapshotabort-function.md). As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.

Se **JetOSSnapshotPrepareInstance** não for chamado entre o início da sessão ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) e o tempo de congelamento ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), todas as instâncias em execução no mecanismo serão congeladas e se tornarão parte da sessão de instantâneo. Isso ocorre por dois motivos:

  - Ele simplifica o código para os usuários que desejam todas as instâncias.

  - Ele permite compatibilidade com versões anteriores para os chamadores das APIs de instantâneo.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows Server 2008.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erros](./error-handling-parameters.md)  
[erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
