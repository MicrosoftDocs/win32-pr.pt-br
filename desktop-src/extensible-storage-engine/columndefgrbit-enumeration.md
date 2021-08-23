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
ms.openlocfilehash: f2bd26a3dac291d78b101aa56f186d9b31f7a927b1eca3e29febc7773e3c0939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042454"
---
# <a name="columndefgrbit-enumeration"></a>Enumeração ColumndefGrbit

Opções para a estrutura JET_COLUMNDEF configuração.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

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
<td>A coluna será corrigida. Ele sempre usará a mesma quantidade de espaço em uma linha, independentemente de quantos dados estão sendo armazenados na coluna. ColumnFixed não pode ser usado com ColumnTagged. Esse bit não pode ser usado com valores longos (ou seja, JET_coltyp. LongText e JET_coltyp. LongBinary).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnTagged</td>
<td>A coluna será marcada. As colunas marcadas não assumirão nenhum espaço no banco de dados se não contêm dados. Esse bit não pode ser usado com ColumnFixed.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnNotNULL</td>
<td>A coluna nunca deve ser definida como um valor NULL. No Windows XP, isso só pode ser aplicado a colunas fixas (bit, byte, inteiro etc.).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnVersion</td>
<td>A coluna é uma coluna de versão que especifica a versão da linha. O valor dessa coluna começa em zero e será incrementado automaticamente para cada atualização na linha. Essa opção só pode ser aplicada a JET_coltyp. Colunas longas. Essa opção não pode ser usada com ColumnAutoincrement, ColumnEscrowUpdate ou ColumnTagged.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnAutoincrement</td>
<td>A coluna será incrementada automaticamente. O número é um número crescente e tem a garantia de ser exclusivo em uma tabela. No entanto, os números podem não ser contínuos. Por exemplo, se cinco linhas são inseridas em uma tabela, a coluna de decremento automático pode conter os valores &quot; &quot; { 1, 2, 6, 7, 8 }. Esse bit só pode ser usado em colunas do tipo JET_coltyp. Long ou JET_coltyp. Conversor de Moedas.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnMultiValued</td>
<td>A coluna pode ter vários valores. Uma coluna com vários valores pode ter zero, um ou mais valores associados a ela. Os vários valores em uma coluna com vários valores são identificados por um número chamado membro itagSequence, que pertence a várias estruturas, incluindo: JET_RETINFO, JET_SETINFO, JET_SETCOLUMN, JET_RETRIEVECOLUMN e JET_ENUMCOLUMNVALUE. Colunas com valores múltiplos devem ser colunas marcadas; ou seja, eles não podem ser colunas de comprimento fixo ou de comprimento variável.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnEscrowUpdate</td>
<td>Especifica que uma coluna é uma coluna de atualização de escrow. Uma coluna de atualização de escrow pode ser atualizada simultaneamente por sessões diferentes com JetEscrowUpdate e manterá a consistência transacional. Uma coluna de atualização de escrow também deve atender às seguintes condições: uma coluna de atualização de escrow só pode ser criada quando a tabela está vazia. Uma coluna de atualização de escrow deve ser do tipo JET_coltypLong. Uma coluna de atualização de escrow deve ter um valor padrão. JET_bitColumnEscrowUpdate pode ser usado em conjunto com ColumnTagged, ColumnVersion ou ColumnAutoincrement.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUnversioned</td>
<td>A coluna será criada em uma sem informações de versão. Isso significa que outras transações que tentam adicionar uma coluna com o mesmo nome falharão. Esse bit só é útil com JetAddColumn. Ele não pode ser usado em uma transação.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnMaybeNull</td>
<td>Ao fazer uma junção externa, a operação de recuperação de coluna pode não ter uma combinação da tabela interna.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUserDefinedDefault</td>
<td>O valor padrão de uma coluna será fornecido por uma função de retorno de chamada. Uma coluna que tem um padrão definido pelo usuário deve ser uma coluna marcada. Especificar JET_bitColumnUserDefinedDefault significa que pvDefault deve apontar para uma estrutura JET_USERDEFINEDDEFAULT e cbDefault deve ser definido como sizeof( JET_USERDEFINEDDEFAULT ).</td>
</tr>
<tr class="even">
<td></td>
<td>TTKey</td>
<td>A coluna será uma coluna de chave para a tabela temporária. A ordem das definições de coluna com essa opção especificada na matriz de entrada determinará a precedência de cada coluna de chave para a tabela temporária. A primeira definição de coluna na matriz que tem essa opção definida será a coluna de chave mais significativa e assim por diante. Se mais colunas de chave são solicitadas do que o mecanismo de banco de dados pode dar suporte, essa opção é ignorada para as colunas de chave sem suporte.</td>
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

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

[ColumnCompressed](./windows7grbits.columncompressed-field.md)
