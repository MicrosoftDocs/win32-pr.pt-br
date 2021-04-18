---
description: 'Saiba mais sobre: Enumeração BeginExternalBackupGrbit'
title: Enumeração BeginExternalBackupGrbit
TOCTitle: BeginExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.beginexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39509773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b68cbfc75d0a71eacedb4bbd462fcd8a93d43690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781009"
---
# <a name="beginexternalbackupgrbit-enumeration"></a>Enumeração BeginExternalBackupGrbit

Opções para [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md).

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginExternalBackupGrbit
'Usage
Dim instance As BeginExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginExternalBackupGrbit
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
<td>Opções padrão.</td>
</tr>
<tr class="even">
<td></td>
<td>Incremental</td>
<td>Cria um backup incremental em oposição a um backup completo. Isso significa que somente os arquivos de log desde o último backup completo ou incremental serão submetidos a backup.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
