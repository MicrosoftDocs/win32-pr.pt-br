---
description: 'Saiba mais sobre: Enumeração DefragGrbit'
title: Enumeração DefragGrbit
TOCTitle: DefragGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DefragGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.defraggrbit(v=EXCHG.10)
ms:contentKeyID: 39516122
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5da047fbdad20ac40d780dc5b0bba9e986e7672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787632"
---
# <a name="defraggrbit-enumeration"></a>Enumeração DefragGrbit

Opções para [JetDefragment (JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DefragGrbit
'Usage
Dim instance As DefragGrbit
```

``` csharp
[FlagsAttribute]
public enum DefragGrbit
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
<td>AvailSpaceTreesOnly</td>
<td>Desfragmenta a parte de espaço disponível da alocação de espaço do banco de dados ESE. O espaço do banco de dados é dividido em dois tipos, espaço de propriedade e espaço disponível. O espaço de propriedade é alocado para uma tabela ou índice enquanto o espaço disponível está pronto para uso dentro da tabela ou índice, respectivamente. O espaço disponível é muito mais dinâmico no comportamento e requer a desfragmentação online mais do que o espaço de propriedade ou os dados de índice ou de tabela.</td>
</tr>
<tr class="even">
<td></td>
<td>BatchStart</td>
<td>Inicia uma nova tarefa de desfragmentação.</td>
</tr>
<tr class="odd">
<td></td>
<td>BatchStop</td>
<td>Interrompe uma tarefa de desfragmentação.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
