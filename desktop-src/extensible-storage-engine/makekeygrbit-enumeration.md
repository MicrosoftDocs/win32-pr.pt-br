---
description: 'Saiba mais sobre: Enumeração MakeKeyGrbit'
title: Enumeração MakeKeyGrbit
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090109"
---
# <a name="makekeygrbit-enumeration"></a>Enumeração MakeKeyGrbit

Opções para JetMakeKey.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
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
<td>NewKey</td>
<td>Uma nova chave de pesquisa deve ser construída. Qualquer chave de pesquisa existente anteriormente é descartada.</td>
</tr>
<tr class="odd">
<td></td>
<td>NormalizedKey</td>
<td>Quando essa opção é especificada, todas as outras opções são ignoradas, qualquer chave de pesquisa existente anteriormente é descartada e o conteúdo do buffer de entrada é carregado como a nova chave de pesquisa.</td>
</tr>
<tr class="even">
<td></td>
<td>KeyDataZeroLength</td>
<td>Se o tamanho do buffer de entrada for zero e a coluna de chave atual for uma coluna de comprimento variável, essa opção indicará que o buffer de entrada contém um valor de comprimento zero. Caso contrário, um tamanho de buffer de entrada igual a zero indicaria um valor nulo.</td>
</tr>
<tr class="odd">
<td></td>
<td>StrLimit</td>
<td>Essa opção indica que a chave de pesquisa deve ser construída de modo que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas.</td>
</tr>
<tr class="even">
<td></td>
<td>SubStrLimit</td>
<td>Essa opção indica que a chave de pesquisa deve ser construída de modo que a coluna de chave atual seja considerada um curinga de prefixo e que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas.</td>
</tr>
<tr class="odd">
<td></td>
<td>FullColumnStartLimit</td>
<td>A chave de pesquisa deve ser construída de modo que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas.</td>
</tr>
<tr class="even">
<td></td>
<td>FullColumnEndLimit</td>
<td>A chave de pesquisa deve ser construída de forma que as colunas de chave que vierem após a coluna de chave atual sejam consideradas curingas.</td>
</tr>
<tr class="odd">
<td></td>
<td>PartialColumnStartLimit</td>
<td>A chave de pesquisa deve ser construída de modo que a coluna de chave atual seja considerada um curinga de prefixo e que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas.</td>
</tr>
<tr class="even">
<td></td>
<td>PartialColumnEndLimit</td>
<td>A chave de pesquisa deve ser construída de modo que a coluna de chave atual seja considerada um curinga de prefixo e que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
