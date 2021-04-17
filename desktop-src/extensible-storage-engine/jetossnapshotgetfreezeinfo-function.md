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
ms.openlocfilehash: 2fbfd3fb31567ea73b8266b5aeba506d62be7714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812221"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a>Função JetOSSnapshotGetFreezeInfo


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetossnapshotgetfreezeinfo-function"></a>Função JetOSSnapshotGetFreezeInfo

A função **JetOSSnapshotGetFreezeInfo** recupera a lista de instâncias e bancos de dados que fazem parte da sessão de instantâneo em um determinado momento.

**Windows Vista:** o **JetOSSnapshotGetFreezeInfo** é introduzido no Windows Vista.  

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>A função falhou devido a uma condição de memória insuficiente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p><em>pcInstanceInfo</em> ou <em>paInstanceInfo</em> é <strong>nulo</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>O identificador da sessão de instantâneo não é válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Uma sessão de instantâneo não está em andamento.</p></td>
</tr>
</tbody>
</table>


Se essa função for bem sucedido, as informações da instância serão preenchidas corretamente e deverão ser liberadas mais tarde chamando [JetFreeBuffer](./jetfreebuffer-function.md) com o ponteiro para a matriz de informações da instância que foi retornada.

Se essa função falhar, nenhuma alteração no estado do mecanismo ocorrerá.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) e <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erros](./error-handling-parameters.md)  
[Erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
