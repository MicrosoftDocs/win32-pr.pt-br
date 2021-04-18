---
description: 'Saiba mais sobre: função JetOSSnapshotTruncateLog'
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
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750113"
---
# <a name="jetossnapshottruncatelog-function"></a>Função JetOSSnapshotTruncateLog


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetossnapshottruncatelog-function"></a>Função JetOSSnapshotTruncateLog

A função **JetOSSnapshotTruncateLog** habilita o truncamento de log para todas as instâncias que fazem parte da sessão de instantâneo.

**Windows Vista:** o **JetOSSnapshotTruncateLog** é introduzido no Windows Vista.  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
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
<td><p>JET_bitAllDatabasesSnapshot</p></td>
<td><p>Todos os bancos de dados são anexados para que o mecanismo de armazenamento possa computar e fazer o truncamento de log.</p></td>
</tr>
<tr class="even">
<td><p>0 (zero)</p></td>
<td><p>Nenhum truncamento ocorrerá.</p></td>
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
<td><p>O parâmetro <em>grbit</em> é inválido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>A sessão de instantâneo não está no estado em que pode ocorrer um truncamento. Causas possíveis:</p>
<ul>
<li><p>a chamada é feita depois que o tempo limite da sessão de instantâneo for atingido</p></li>
<li><p>a sessão foi especificada como um instantâneo de cópia</p></li>
</ul></td>
</tr>
</tbody>
</table>


Em caso de êxito, os arquivos de log de uma ou todas as instâncias que fazem parte da sessão de instantâneo serão truncados, se possível.

#### <a name="remarks"></a>Comentários

Essa função deve ser chamada somente se o instantâneo tiver sido criado com a opção JET_bitContinueAfterThaw. Caso contrário, a sessão de instantâneo teria terminado após a chamada [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) .

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
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
