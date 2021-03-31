---
description: 'Saiba mais sobre: função JetOSSnapshotEnd'
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
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089881"
---
# <a name="jetossnapshotend-function"></a>Função JetOSSnapshotEnd


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetossnapshotend-function"></a>Função JetOSSnapshotEnd

A função **JetOSSnapshotEnd** notifica o mecanismo de que a sessão de instantâneo foi concluída.

**Windows Vista:** o **JetOSSnapshotEnd** é introduzido no Windows Vista:.  

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*snapid*

O identificador da sessão de instantâneo.

*grbit*

As opções para esta chamada. Esse parâmetro pode ter uma combinação dos valores a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>A extremidade bem-sucedida da sessão de instantâneo.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitAbortSnapshot</p></td>
<td><p>A sessão de instantâneo foi anulada.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Uma das opções solicitadas é inválida, usada incorretamente ou não implementada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Uma sessão de instantâneo já está em andamento. Isso não é permitido.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>O identificador da sessão de instantâneo não é válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut</p></td>
<td><p>A sessão de instantâneo tinha um tempo limite interno antes que essa chamada tivesse ocorrido. Como resultado, as operações de e/s retornadas para normal antes que essa chamada fosse feita.</p></td>
</tr>
</tbody>
</table>


Se essa função for bem sucedido, uma sessão de instantâneo será concluída e o comportamento normal do mecanismo será retomado. Uma nova sessão de instantâneo pode ser iniciada mais tarde.

Se essa função falhar, o JET_errOSSnapshotTimeOut retorno de código retornado e a sessão de instantâneo atual terminará, mas o congelamento do IOs durante o período de instantâneo não foi respeitado internamente. Para todos os outros erros, o estado da sessão de instantâneo não será alterado.

#### <a name="remarks"></a>Comentários

Essa função será chamada somente se [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) tiver sido chamado com JET_bitContinueAfterThaw.

A sessão de instantâneo deve ser concluída para que a verificação de instantâneo e o truncamento de log ocorram. As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.

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
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
