---
description: 'Saiba mais sobre: Função JetOSSnapshotPrepareInstance'
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
ms.openlocfilehash: bfd4fc15f3ea7d4f6275f0d4dd31ed96729715b6089397fff7ee73fc7d0c6e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614927"
---
# <a name="jetossnapshotprepareinstance-function"></a>Função JetOSSnapshotPrepareInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetossnapshotprepareinstance-function"></a>Função JetOSSnapshotPrepareInstance

A **função JetOSSnapshotPrepareInstance** seleciona uma instância específica para fazer parte da sessão de instantâneo.

**Windows Vista:** **JetOSSnapshotPrepareInstance** foi introduzido no Windows Vista.

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
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

As opções para essa chamada. Esse parâmetro é reservado para uso futuro. O único valor válido é 0 (zero).

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) tipo de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

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
<td><p>O ponteiro de ID do instantâneo <strong>é NULL</strong> ou o <em>parâmetro grbit</em> é inválido.</p></td>
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


Se essa função for bem-sucedida, a instância especificada fará parte da sessão de instantâneo.

Se essa função falhar, nenhuma alteração no estado do mecanismo ocorrerá.

#### <a name="remarks"></a>Comentários

A chamada de sequência de API normal é: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), opcionalmente seguido por uma ou mais chamadas para **JetOSSnapshotPrepareInstance**, seguido por [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Depois que o congelamento for iniciado, ele poderá ser encerrado usando [JetOSSnapshotThaw](./jetossnapshotthaw-function.md). A qualquer momento após a preparação, a sessão de instantâneo pode ser encerrada com [JetOSSnapshotAbort .](./jetossnapshotabort-function.md) As entradas do log de eventos serão geradas para as diferentes etapas do instantâneo.

Se **JetOSSnapshotPrepareInstance** não for chamado entre o início da sessão ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) e o momento de congelamento ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), todas as instâncias em execução no mecanismo congelarão e se tornarão parte da sessão de instantâneo. Isso ocorre por dois motivos:

  - Ele simplifica o código para usuários que querem todas as instâncias.

  - Ele permite compatibilidade com compatibilidade com backward para os chamadores das APIs de instantâneo.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erro](./error-handling-parameters.md)  
[Erros extensíveis Armazenamento mecanismo](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
