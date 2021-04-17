---
description: 'Saiba mais sobre: Enumeração EnumerateColumnsGrbit'
title: Enumeração EnumerateColumnsGrbit
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812363"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>Enumeração EnumerateColumnsGrbit

Opções para JetEnumerateColumns.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a>Membros

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
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
<td>EnumerateCompressOutput</td>
<td>Ao enumerar valores de coluna, todas as colunas para as quais estamos recuperando todos os valores e que têm apenas um valor de coluna não nula podem ser retornadas em um formato compactado. O status dessas colunas será definido como <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> e o tamanho do valor da coluna e a memória que contém o valor da coluna serão retornados diretamente na estrutura de <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> . Não há garantia de que todas as colunas qualificadas sejam compactadas dessa maneira. Consulte <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> para obter mais informações.</td>
</tr>
<tr class="odd">
<td></td>
<td>EnumerateCopy</td>
<td>Essa opção indica que os valores de coluna modificados do registro devem ser enumerados em vez dos valores de coluna originais. Se um valor de coluna não tiver sido modificado, o valor da coluna original será enumerado. Dessa forma, um valor de coluna que ainda não foi inserido ou atualizado pode ser enumerado ao inserir ou atualizar um registro.
<p>Essa opção é idêntica a <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</p></td>
</tr>
<tr class="even">
<td></td>
<td>EnumerateIgnoreDefault</td>
<td>Se uma determinada coluna não estiver presente no registro, nenhum valor de coluna será retornado. Normalmente, o valor padrão para a coluna, se houver, seria retornado nesse caso. É garantido que, se a coluna for definida como um valor diferente do valor padrão, esse valor diferente será retornado (ou seja, se uma coluna com um valor padrão for explicitamente definida como NULL, um NULL será retornado como o valor dessa coluna). Mesmo que essa opção seja solicitada, ainda é possível ver um valor de coluna que é igual ao valor padrão. Nenhum esforço é feito para remover valores de coluna que correspondam aos valores padrão. É importante lembrar que essa opção afeta a saída de <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> quando usada com EnumeratePresenceOnly ou EnumerateTaggedOnly.</td>
</tr>
<tr class="odd">
<td></td>
<td>EnumeratePresenceOnly</td>
<td>Se existir um valor não nulo para o valor de coluna ou coluna solicitado, os dados associados não serão retornados. Em vez disso, o status associado para essa coluna ou valor de coluna será definido como <a href="hh557250(v=exchg.10).md">ColumnPresent</a>. Se o valor da coluna ou coluna for nulo, <a href="hh557250(v=exchg.10).md">ColumnNull</a> será retornado como de costume.</td>
</tr>
<tr class="even">
<td></td>
<td>EnumerateTaggedOnly</td>
<td>Ao enumerar todos os valores de coluna no registro (por exemplo, ou seja, quando numColumnids for zero), somente os valores de coluna marcados serão retornados. Essa opção não é permitida ao enumerar uma matriz específica de IDs de coluna.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

[EnumerateIgnoreUserDefinedDefault](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[EnumerateInRecordOnly](./windows7grbits.enumerateinrecordonly-field.md)
