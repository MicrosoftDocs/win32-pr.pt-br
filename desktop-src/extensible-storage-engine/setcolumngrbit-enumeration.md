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
# <a name="setcolumngrbit-enumeration"></a><span data-ttu-id="ac298-103">Enumeração SetColumnGrbit</span><span class="sxs-lookup"><span data-stu-id="ac298-103">SetColumnGrbit enumeration</span></span>

<span data-ttu-id="ac298-104">Opções para JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="ac298-104">Options for JetSetColumn.</span></span>

<span data-ttu-id="ac298-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="ac298-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="ac298-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ac298-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ac298-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ac298-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ac298-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac298-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="ac298-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ac298-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ac298-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="ac298-110">Member name</span></span></th>
<th><span data-ttu-id="ac298-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac298-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ac298-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac298-112">None</span></span></td>
<td><span data-ttu-id="ac298-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="ac298-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ac298-114">AppendLV</span><span class="sxs-lookup"><span data-stu-id="ac298-114">AppendLV</span></span></td>
<td><span data-ttu-id="ac298-115">Essa opção é usada para acrescentar dados a uma coluna do tipo JET_coltypLongText ou JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="ac298-115">This option is used to append data to a column of type JET_coltypLongText or JET_coltypLongBinary.</span></span> <span data-ttu-id="ac298-116">O mesmo comportamento pode ser obtido determinando o tamanho do valor longo existente e especificando ibLongValue em psetinfo.</span><span class="sxs-lookup"><span data-stu-id="ac298-116">The same behavior can be achieved by determining the size of the existing long value and specifying ibLongValue in psetinfo.</span></span> <span data-ttu-id="ac298-117">No entanto, sua mais simples de usar esse grbit, pois saber o tamanho do valor da coluna existente não é necessário.</span><span class="sxs-lookup"><span data-stu-id="ac298-117">However, its simpler to use this grbit since knowing the size of the existing column value is not necessary.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ac298-118">OverwriteLV</span><span class="sxs-lookup"><span data-stu-id="ac298-118">OverwriteLV</span></span></td>
<td><span data-ttu-id="ac298-119">Essa opção é usada para substituir o valor longo existente pelos dados fornecidos recentemente.</span><span class="sxs-lookup"><span data-stu-id="ac298-119">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="ac298-120">Quando essa opção é usada, é como se o valor longo existente tiver sido definido como 0 (zero) comprimento antes da definição dos novos dados.</span><span class="sxs-lookup"><span data-stu-id="ac298-120">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ac298-121">RevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="ac298-121">RevertToDefaultValue</span></span></td>
<td><span data-ttu-id="ac298-122">Essa opção só é aplicável a colunas marcadas, esparsas ou com vários valores.</span><span class="sxs-lookup"><span data-stu-id="ac298-122">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="ac298-123">Faz com que a coluna retorne o valor de coluna padrão em operações de recuperação de coluna subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ac298-123">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="ac298-124">Todos os valores de coluna existentes são removidos.</span><span class="sxs-lookup"><span data-stu-id="ac298-124">All existing column values are removed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ac298-125">SeparateLV</span><span class="sxs-lookup"><span data-stu-id="ac298-125">SeparateLV</span></span></td>
<td><span data-ttu-id="ac298-126">Essa opção é usada para forçar um valor longo, colunas do tipo JET_coltyp. LongText ou JET_coltyp. LongBinary, a ser armazenado separadamente do restante dos dados de registro.</span><span class="sxs-lookup"><span data-stu-id="ac298-126">This option is used to force a long value, columns of type JET_coltyp.LongText or JET_coltyp.LongBinary, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="ac298-127">Isso ocorre normalmente quando o tamanho do valor longo impede que ele seja armazenado com os dados de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="ac298-127">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="ac298-128">No entanto, essa opção pode ser usada para forçar o valor longo a ser armazenado separadamente.</span><span class="sxs-lookup"><span data-stu-id="ac298-128">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="ac298-129">Observe que valores longos de quatro bytes de tamanho menor não podem ser forçados a serem separados.</span><span class="sxs-lookup"><span data-stu-id="ac298-129">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="ac298-130">Nesses casos, a opção é ignorada.</span><span class="sxs-lookup"><span data-stu-id="ac298-130">In such cases, the option is ignored.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ac298-131">SizeLV</span><span class="sxs-lookup"><span data-stu-id="ac298-131">SizeLV</span></span></td>
<td><span data-ttu-id="ac298-132">Essa opção é usada para interpretar o buffer de entrada como um número inteiro de bytes a serem definidos como o comprimento do valor longo descrito pelo columnid fornecido e, se fornecido, o número de sequência em psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="ac298-132">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="ac298-133">Se o tamanho fornecido for maior que o valor da coluna existente, a coluna será estendida com 0s.</span><span class="sxs-lookup"><span data-stu-id="ac298-133">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="ac298-134">Se o tamanho for menor do que o valor da coluna existente, o valor será truncado.</span><span class="sxs-lookup"><span data-stu-id="ac298-134">If the size is smaller than the existing column value then the value will be truncated.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ac298-135">UniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="ac298-135">UniqueMultiValues</span></span></td>
<td><span data-ttu-id="ac298-136">Essa opção é usada para impor que todos os valores em uma coluna com valores múltiplos sejam distintos.</span><span class="sxs-lookup"><span data-stu-id="ac298-136">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="ac298-137">Essa opção compara os dados da coluna de origem, sem nenhuma transformação, com outros valores de coluna existentes e um erro será retornado se uma duplicata for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ac298-137">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="ac298-138">Se essa opção for fornecida, AppendLV, OverwriteLV e SizeLV também não poderão ser fornecidos.</span><span class="sxs-lookup"><span data-stu-id="ac298-138">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ac298-139">UniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="ac298-139">UniqueNormalizedMultiValues</span></span></td>
<td><span data-ttu-id="ac298-140">Essa opção é usada para impor que todos os valores em uma coluna com valores múltiplos sejam distintos.</span><span class="sxs-lookup"><span data-stu-id="ac298-140">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="ac298-141">Essa opção compara a transformação normalizada da chave de dados de coluna com outros valores de coluna existentes transformados de forma semelhante e um erro será retornado se uma duplicata for encontrada.</span><span class="sxs-lookup"><span data-stu-id="ac298-141">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="ac298-142">Se essa opção for fornecida, AppendLV, OverwriteLV e SizeLV também não poderão ser fornecidos.</span><span class="sxs-lookup"><span data-stu-id="ac298-142">If this option is given, then AppendLV, OverwriteLV and SizeLV cannot also be given.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ac298-143">ZeroLength</span><span class="sxs-lookup"><span data-stu-id="ac298-143">ZeroLength</span></span></td>
<td><span data-ttu-id="ac298-144">Essa opção é usada para definir um valor de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="ac298-144">This option is used to set a value to zero length.</span></span> <span data-ttu-id="ac298-145">Normalmente, um valor de coluna é definido como NULL passando um cbMax de 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="ac298-145">Normally, a column value is set to NULL by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="ac298-146">No entanto, para alguns tipos, como JET_coltyp. Text, um valor de coluna pode ser 0 (zero) comprimento em vez de NULL, e essa opção é usada para diferenciar entre NULL e 0 (zero) comprimento.</span><span class="sxs-lookup"><span data-stu-id="ac298-146">However, for some types, like JET_coltyp.Text, a column value can be 0 (zero) length instead of NULL, and this option is used to differentiate between NULL and 0 (zero) length.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ac298-147">IntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="ac298-147">IntrinsicLV</span></span></td>
<td><span data-ttu-id="ac298-148">Tente armazenar colunas de valor longo no registro, mesmo se elas excederem o tamanho de separação padrão.</span><span class="sxs-lookup"><span data-stu-id="ac298-148">Try to store long-value columns in the record, even if they exceed the default separation size.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ac298-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac298-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ac298-150">Referência</span><span class="sxs-lookup"><span data-stu-id="ac298-150">Reference</span></span>

[<span data-ttu-id="ac298-151">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ac298-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="ac298-152">Compactado</span><span class="sxs-lookup"><span data-stu-id="ac298-152">Compressed</span></span>](./windows7grbits.compressed-field.md)

[<span data-ttu-id="ac298-153">Não compactado</span><span class="sxs-lookup"><span data-stu-id="ac298-153">Uncompressed</span></span>](./windows7grbits.uncompressed-field.md)
