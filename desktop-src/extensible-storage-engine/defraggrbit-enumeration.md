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
ms.openlocfilehash: faf2187a47f7a3cd519d69c8cf45f377a4e0f0941d4e9a83bd50653cc4236504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118083433"
---
# <a name="defraggrbit-enumeration"></a>Enumeração DefragGrbit

Opções para [JetDefragment(JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

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
<td>Desfragmenta a parte de espaço disponível da alocação de espaço do banco de dados ESE. O espaço do banco de dados é dividido em dois tipos, espaço de propriedade e espaço disponível. O espaço de propriedade é alocado a uma tabela ou índice enquanto o espaço disponível está pronto para uso na tabela ou índice, respectivamente. O espaço disponível é muito mais dinâmico no comportamento e requer desfragmentação online mais do que o espaço ou dados de tabela ou índice de propriedade.</td>
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

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
