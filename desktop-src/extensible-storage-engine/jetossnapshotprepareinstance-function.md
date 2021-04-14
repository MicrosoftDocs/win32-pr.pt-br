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
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104371032"
---
# <a name="jetossnapshotprepareinstance-function"></a>Função JetOSSnapshotPrepareInstance


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetossnapshotprepareinstance-function"></a>Função JetOSSnapshotPrepareInstance

A função **JetOSSnapshotPrepareInstance** seleciona uma instância específica para fazer parte da sessão de instantâneo.

**Windows Vista:** o **JetOSSnapshotPrepareInstance** foi introduzido no Windows Vista.

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

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>O ponteiro da ID do instantâneo é <strong>nulo</strong> ou o parâmetro <em>grbit</em> é inválido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Uma sessão de instantâneo já está em andamento.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>O identificador da sessão de instantâneo não é válido.</p></td>
</tr>
</tbody>
</table>


Se essa função for realizada com sucesso, a instância especificada fará parte da sessão de instantâneo.

Se essa função falhar, nenhuma alteração no estado do mecanismo ocorrerá.

#### <a name="remarks"></a>Comentários

A chamada de sequência de API normal é: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), opcionalmente seguido por uma ou mais chamadas para **JetOSSnapshotPrepareInstance**, seguido por [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Quando o congelamento é iniciado, ele pode ser encerrado usando [JetOSSnapshotThaw](./jetossnapshotthaw-function.md). A qualquer momento após a preparação, a sessão de instantâneo pode ser encerrada abruptamente com [JetOSSnapshotAbort](./jetossnapshotabort-function.md). As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.

Se **JetOSSnapshotPrepareInstance** não for chamado entre o início da sessão ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) e o tempo de congelamento ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), todas as instâncias em execução no mecanismo serão congeladas e se tornarão parte da sessão de instantâneo. Isso ocorre por dois motivos:

  - Ele simplifica o código para os usuários que desejam todas as instâncias.

  - Ele permite compatibilidade com versões anteriores para os chamadores das APIs de instantâneo.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erros](./error-handling-parameters.md)  
[Erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
