---
description: 'Saiba mais sobre: Enumeração SetColumnGrbit'
title: Enumeração SetColumnGrbit
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893f8e79b910a305bf6caccacd2d928e947be693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461186"
---
# <a name="setcolumngrbit-enumeration"></a>Enumeração SetColumnGrbit

Opções para JetSetColumn.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
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
<td>AppendLV</td>
<td>Essa opção é usada para acrescentar dados a uma coluna do tipo JET_coltypLongText ou JET_coltypLongBinary. O mesmo comportamento pode ser obtido determinando o tamanho do valor longo existente e especificando ibLongValue em psetinfo. No entanto, sua mais simples de usar esse grbit, pois saber o tamanho do valor da coluna existente não é necessário.</td>
</tr>
<tr class="odd">
<td></td>
<td>OverwriteLV</td>
<td>Essa opção é usada para substituir o valor longo existente pelos dados fornecidos recentemente. Quando essa opção é usada, é como se o valor longo existente tiver sido definido como 0 (zero) comprimento antes da definição dos novos dados.</td>
</tr>
<tr class="even">
<td></td>
<td>RevertToDefaultValue</td>
<td>Essa opção só é aplicável a colunas marcadas, esparsas ou com vários valores. Faz com que a coluna retorne o valor de coluna padrão em operações de recuperação de coluna subsequentes. Todos os valores de coluna existentes são removidos.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeparateLV</td>
<td>Essa opção é usada para forçar um valor longo, colunas do tipo JET_coltyp. LongText ou JET_coltyp. LongBinary, a ser armazenado separadamente do restante dos dados de registro. Isso ocorre normalmente quando o tamanho do valor longo impede que ele seja armazenado com os dados de registro restantes. No entanto, essa opção pode ser usada para forçar o valor longo a ser armazenado separadamente. Observe que valores longos de quatro bytes de tamanho menor não podem ser forçados a serem separados. Nesses casos, a opção é ignorada.</td>
</tr>
<tr class="even">
<td></td>
<td>SizeLV</td>
<td>Essa opção é usada para interpretar o buffer de entrada como um número inteiro de bytes a serem definidos como o comprimento do valor longo descrito pelo columnid fornecido e, se fornecido, o número de sequência em psetinfo- &gt; itagSequence. Se o tamanho fornecido for maior que o valor da coluna existente, a coluna será estendida com 0s. Se o tamanho for menor do que o valor da coluna existente, o valor será truncado.</td>
</tr>
<tr class="odd">
<td></td>
<td>UniqueMultiValues</td>
<td>Essa opção é usada para impor que todos os valores em uma coluna com valores múltiplos sejam distintos. Essa opção compara os dados da coluna de origem, sem nenhuma transformação, com outros valores de coluna existentes e um erro será retornado se uma duplicata for encontrada. Se essa opção for fornecida, AppendLV, OverwriteLV e SizeLV também não poderão ser fornecidos.</td>
</tr>
<tr class="even">
<td></td>
<td>UniqueNormalizedMultiValues</td>
<td>Essa opção é usada para impor que todos os valores em uma coluna com valores múltiplos sejam distintos. Essa opção compara a transformação normalizada da chave de dados de coluna com outros valores de coluna existentes transformados de forma semelhante e um erro será retornado se uma duplicata for encontrada. Se essa opção for fornecida, AppendLV, OverwriteLV e SizeLV também não poderão ser fornecidos.</td>
</tr>
<tr class="odd">
<td></td>
<td>ZeroLength</td>
<td>Essa opção é usada para definir um valor de comprimento zero. Normalmente, um valor de coluna é definido como NULL passando um cbMax de 0 (zero). No entanto, para alguns tipos, como JET_coltyp. Text, um valor de coluna pode ser 0 (zero) comprimento em vez de NULL, e essa opção é usada para diferenciar entre NULL e 0 (zero) comprimento.</td>
</tr>
<tr class="even">
<td></td>
<td>IntrinsicLV</td>
<td>Tente armazenar colunas de valor longo no registro, mesmo se elas excederem o tamanho de separação padrão.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

[Compactado](./windows7grbits.compressed-field.md)

[Não compactado](./windows7grbits.uncompressed-field.md)
