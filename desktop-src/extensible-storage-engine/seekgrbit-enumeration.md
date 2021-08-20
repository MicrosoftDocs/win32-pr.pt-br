---
description: 'Saiba mais sobre: enumeração SeekGrbit'
title: Enumeração SeekGrbit
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12a65021d8c224d2a0ed50082b3120c94fc8c83f25c9aaf3eaf6e71d3f3f45f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978586"
---
# <a name="seekgrbit-enumeration"></a>Enumeração SeekGrbit

Opções para JetSeek.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
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
<td>SeekEQ</td>
<td>O cursor será posicionado na entrada de índice mais próxima do início do índice que corresponde exatamente à chave de pesquisa.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekLT</td>
<td>O cursor será posicionado na entrada de índice mais próxima ao final do índice que é menor que uma entrada de índice que corresponderia exatamente aos critérios de pesquisa.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekLE</td>
<td>O cursor será posicionado na entrada de índice mais próxima ao final do índice que é menor ou igual a uma entrada de índice que corresponderia exatamente aos critérios de pesquisa.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekGE</td>
<td>O cursor será posicionado na entrada de índice mais próxima do início do índice que é maior ou igual a uma entrada de índice que corresponderia exatamente aos critérios de pesquisa.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekGT</td>
<td>O cursor será posicionado na entrada de índice mais próxima ao início do índice maior que uma entrada de índice que corresponderia exatamente aos critérios de pesquisa.</td>
</tr>
<tr class="even">
<td></td>
<td>SetIndexRange</td>
<td>Um intervalo de índice será configurado automaticamente para todas as chaves que corresponderem exatamente à chave de pesquisa.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
