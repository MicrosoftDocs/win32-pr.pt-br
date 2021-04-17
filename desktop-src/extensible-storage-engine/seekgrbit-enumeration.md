---
description: 'Saiba mais sobre: Enumeração SeekGrbit'
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
ms.openlocfilehash: 9e59072055710676f5f7647130f42ad5acf50527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757987"
---
# <a name="seekgrbit-enumeration"></a>Enumeração SeekGrbit

Opções para JetSeek.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

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
<td>O cursor será posicionado na entrada de índice mais próxima do final do índice que for menor que uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekLE</td>
<td>O cursor será posicionado na entrada de índice mais próxima do final do índice que for menor ou igual a uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</td>
</tr>
<tr class="even">
<td></td>
<td>SeekGE</td>
<td>O cursor será posicionado na entrada de índice mais próxima do início do índice que seja maior ou igual a uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeekGT</td>
<td>O cursor será posicionado na entrada de índice mais próxima do início do índice que é maior que uma entrada de índice que corresponde exatamente aos critérios de pesquisa.</td>
</tr>
<tr class="even">
<td></td>
<td>SetIndexRange</td>
<td>Um intervalo de índice será automaticamente configurado para todas as chaves que correspondem exatamente à chave de pesquisa.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
