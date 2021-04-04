---
description: 'Saiba mais sobre: enumeração de JET_dbstate'
title: Enumeração de JET_dbstate
TOCTitle: JET_dbstate enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_dbstate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbstate(v=EXCHG.10)
ms:contentKeyID: 39511841
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_dbstate
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a83c8a4313e5e6f21ee885ee7936c90503bfbd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646745"
---
# <a name="jet_dbstate-enumeration"></a>Enumeração de JET_dbstate

Estados de banco de dados (usados em [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Enumeration JET_dbstate
'Usage
Dim instance As JET_dbstate
```

``` csharp
public enum JET_dbstate
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
<td>JustCreated</td>
<td>O banco de dados acabou de ser criado.</td>
</tr>
<tr class="even">
<td></td>
<td>DirtyShutdown</td>
<td>Banco de dados de desligamento anormal (inconsistente).</td>
</tr>
<tr class="odd">
<td></td>
<td>CleanShutdown</td>
<td>Banco de dados de desligamento normal (consistente).</td>
</tr>
<tr class="even">
<td></td>
<td>BeingConverted</td>
<td>O banco de dados está sendo convertido.</td>
</tr>
<tr class="odd">
<td></td>
<td>ForceDetach</td>
<td>O banco de dados foi desanexado.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
