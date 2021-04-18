---
description: 'Saiba mais sobre: Enumeração ColumndefGrbit'
title: Enumeração ColumndefGrbit
TOCTitle: ColumndefGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumndefGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columndefgrbit(v=EXCHG.10)
ms:contentKeyID: 39513005
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c94dcf7d454c5f0ea11fcee0bd46655099dfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761614"
---
# <a name="columndefgrbit-enumeration"></a>Enumeração ColumndefGrbit

Opções para a estrutura de JET_COLUMNDEF.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ColumndefGrbit
'Usage
Dim instance As ColumndefGrbit
```

``` csharp
[FlagsAttribute]
public enum ColumndefGrbit
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
<td>ColumnFixed</td>
<td>A coluna será corrigida. Ele sempre usará a mesma quantidade de espaço em uma linha, independentemente da quantidade de dados que está sendo armazenada na coluna. ColumnFixed não pode ser usado com ColumnTagged. Esse bit não pode ser usado com valores longos (JET_coltyp. LongText e JET_coltyp. LongBinary).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnTagged</td>
<td>A coluna será marcada. As colunas marcadas não ocupam nenhum espaço no banco de dados se não contiverem. Esse bit não pode ser usado com ColumnFixed.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnNotNULL</td>
<td>A coluna nunca deve ser definida como um valor nulo. No Windows XP, isso só pode ser aplicado a colunas fixas (bit, byte, inteiro, etc.).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnVersion</td>
<td>A coluna é uma coluna de versão que especifica a versão da linha. O valor desta coluna começa em zero e será incrementado automaticamente para cada atualização na linha. Esta opção só pode ser aplicada a JET_coltyp. Colunas longas. Essa opção não pode ser usada com ColumnAutoincrement, ColumnEscrowUpdate ou ColumnTagged.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnAutoincrement</td>
<td>A coluna será incrementada automaticamente. O número é um número cada vez maior e é garantido que seja exclusivo dentro de uma tabela. No entanto, os números podem não ser contínuos. Por exemplo, se cinco linhas forem inseridas em uma tabela, a &quot; coluna AutoIncrement &quot; poderá conter os valores {1, 2, 6, 7, 8}. Esse bit só pode ser usado em colunas do tipo JET_coltyp. Longo ou JET_coltyp. Moeda.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnMultiValued</td>
<td>A coluna pode ter valores múltiplos. Uma coluna com valores múltiplos pode ter zero, um ou mais valores associados a ela. Os vários valores em uma coluna com valores múltiplos são identificados por um número chamado membro itagSequence, que pertence a várias estruturas, incluindo: JET_RETINFO, JET_SETINFO, JET_SETCOLUMN, JET_RETRIEVECOLUMN e JET_ENUMCOLUMNVALUE. Colunas com valores múltiplos devem ser colunas marcadas; ou seja, eles não podem ter colunas de comprimento fixo ou de comprimento variável.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnEscrowUpdate</td>
<td>Especifica que uma coluna é uma coluna de atualização de caução. Uma coluna de atualização de caução pode ser atualizada simultaneamente por sessões diferentes com JetEscrowUpdate e manterá a consistência transacional. Uma coluna de atualização de caução também deve atender às seguintes condições: uma coluna de atualização de caução só pode ser criada quando a tabela está vazia. Uma coluna de atualização de caução deve ser do tipo JET_coltypLong. Uma coluna de atualização de caução deve ter um valor padrão. JET_bitColumnEscrowUpdate não pode ser usado em conjunto com ColumnTagged, ColumnVersion ou ColumnAutoincrement.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUnversioned</td>
<td>A coluna será criada em uma sem informações de versão. Isso significa que outras transações que tentam adicionar uma coluna com o mesmo nome falharão. Esse bit só é útil com JetAddColumn. Ele não pode ser usado em uma transação.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnMaybeNull</td>
<td>Ao fazer uma junção externa, a operação de recuperação de coluna pode não ter uma correspondência da tabela interna.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUserDefinedDefault</td>
<td>O valor padrão de uma coluna será fornecido por uma função de retorno de chamada. Uma coluna que tem um padrão definido pelo usuário deve ser uma coluna marcada. Especificar JET_bitColumnUserDefinedDefault significa que pvDefault deve apontar para uma estrutura de JET_USERDEFINEDDEFAULT e cbDefault deve ser definido como sizeof (JET_USERDEFINEDDEFAULT).</td>
</tr>
<tr class="even">
<td></td>
<td>TTKey</td>
<td>A coluna será uma coluna de chave para a tabela temporária. A ordem das definições de coluna com essa opção especificada na matriz de entrada determinará a precedência de cada coluna de chave para a tabela temporária. A primeira definição de coluna na matriz que tem esse conjunto de opções será a coluna de chave mais significativa e assim por diante. Se mais colunas de chave forem solicitadas do que o mecanismo de banco de dados pode ter suporte, essa opção será ignorada para as colunas de chave sem suporte.</td>
</tr>
<tr class="odd">
<td></td>
<td>TTDescending</td>
<td>A ordem de classificação da coluna de chave para a tabela temporária deve ser decrescente em vez de crescente. Se essa opção for especificada sem TTKey, essa opção será ignorada.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

[ColumnCompressed](./windows7grbits.columncompressed-field.md)
