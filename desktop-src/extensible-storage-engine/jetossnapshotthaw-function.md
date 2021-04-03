---
description: 'Saiba mais sobre: função JetOSSnapshotThaw'
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
ms.openlocfilehash: da7d5037cfc6b9a5f001dede57581127e4de60b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837350"
---
# <a name="jetossnapshotthaw-function"></a>Função JetOSSnapshotThaw


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetossnapshotthaw-function"></a>Função JetOSSnapshotThaw

A função **JetOSSnapshotThaw** notifica o mecanismo de que ele pode retomar as operações de e/s normais após um período de congelamento e um instantâneo bem-sucedido.

**Windows XP:** o **JetOSSnapshotThaw** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*snapid*

O identificador da sessão de instantâneo.

*grbit*

Esse parâmetro é reservado para uso futuro e o único valor válido com suporte é 0.

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
<td><p>A sessão de instantâneo é inválida ou o parâmetro <em>grbit</em> é inválido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut</p></td>
<td><p>A sessão de instantâneo tinha um tempo limite interno antes que essa chamada tivesse ocorrido. Consequentemente, as operações de e/s retornadas para normal antes que essa chamada fosse feita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>O identificador da sessão de instantâneo não é válido.</p></td>
</tr>
</tbody>
</table>


Se essa função for bem sucedido, uma sessão de instantâneo terminará e o comportamento normal do mecanismo será retomado. Uma nova sessão de instantâneo pode ser iniciada mais tarde.

Se essa função falhar, a sessão de instantâneo atual terminará, mas o congelamento do IOs durante o período de instantâneo não foi respeitado internamente.

#### <a name="remarks"></a>Comentários

As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista ou o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008 ou o Windows Server 2003.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)
