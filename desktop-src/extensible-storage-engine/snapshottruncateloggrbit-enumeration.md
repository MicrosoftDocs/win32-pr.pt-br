---
description: 'Saiba mais sobre: Enumeração SnapshotTruncateLogGrbit'
title: Enumeração SnapshotTruncateLogGrbit (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: SnapshotTruncateLogGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.snapshottruncateloggrbit(v=EXCHG.10)
ms:contentKeyID: 39516474
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f18c8cdb69be2af6afee3dcd8e4cd492229526a4b5ad6de8d64f63365c9fc0b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107199"
---
# <a name="snapshottruncateloggrbit-enumeration"></a>Enumeração SnapshotTruncateLogGrbit

Opções para [JetOSSnapshotTruncateLog(JET_OSSNAPID, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncatelog-method.md) e [JetOSSnapshotTruncateLogInstance(JET_OSSNAPID, JET_INSTANCE, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncateloginstance-method.md).

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotTruncateLogGrbit
'Usage
Dim instance As SnapshotTruncateLogGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotTruncateLogGrbit
```

## <a name="members"></a>Membros

<table>
<thead>
<tr class="header">
<th></th>
<th>Nome do membro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Nenhum</td>
<td>Nenhum truncamento ocorrerá.</td>
</tr>
<tr class="even">
<td></td>
<td>AllDatabasesSnapshot</td>
<td>Todos os bancos de dados são anexados para que o mecanismo de armazenamento possa calcular e fazer o truncamento de log.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
