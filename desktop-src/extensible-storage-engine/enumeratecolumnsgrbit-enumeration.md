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
# <a name="enumeratecolumnsgrbit-enumeration"></a><span data-ttu-id="c9439-103">Enumeração EnumerateColumnsGrbit</span><span class="sxs-lookup"><span data-stu-id="c9439-103">EnumerateColumnsGrbit enumeration</span></span>

<span data-ttu-id="c9439-104">Opções para JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="c9439-104">Options for JetEnumerateColumns.</span></span>

<span data-ttu-id="c9439-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="c9439-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="c9439-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c9439-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c9439-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c9439-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c9439-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9439-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="c9439-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c9439-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c9439-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="c9439-110">Member name</span></span></th>
<th><span data-ttu-id="c9439-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9439-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c9439-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9439-112">None</span></span></td>
<td><span data-ttu-id="c9439-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="c9439-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c9439-114">EnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="c9439-114">EnumerateCompressOutput</span></span></td>
<td><span data-ttu-id="c9439-115">Ao enumerar valores de coluna, todas as colunas para as quais estamos recuperando todos os valores e que têm apenas um valor de coluna não nula podem ser retornadas em um formato compactado.</span><span class="sxs-lookup"><span data-stu-id="c9439-115">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="c9439-116">O status dessas colunas será definido como <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> e o tamanho do valor da coluna e a memória que contém o valor da coluna serão retornados diretamente na estrutura de <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="c9439-116">The status for such columns will be set to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> and the size of the column value and the memory containing the column value will be returned directly in the <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="c9439-117">Não há garantia de que todas as colunas qualificadas sejam compactadas dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="c9439-117">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="c9439-118">Consulte <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c9439-118">See <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c9439-119">EnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="c9439-119">EnumerateCopy</span></span></td>
<td><span data-ttu-id="c9439-120">Essa opção indica que os valores de coluna modificados do registro devem ser enumerados em vez dos valores de coluna originais.</span><span class="sxs-lookup"><span data-stu-id="c9439-120">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="c9439-121">Se um valor de coluna não tiver sido modificado, o valor da coluna original será enumerado.</span><span class="sxs-lookup"><span data-stu-id="c9439-121">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="c9439-122">Dessa forma, um valor de coluna que ainda não foi inserido ou atualizado pode ser enumerado ao inserir ou atualizar um registro.</span><span class="sxs-lookup"><span data-stu-id="c9439-122">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span>
<p><span data-ttu-id="c9439-123">Essa opção é idêntica a <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</span><span class="sxs-lookup"><span data-stu-id="c9439-123">This option is identical to <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c9439-124">EnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="c9439-124">EnumerateIgnoreDefault</span></span></td>
<td><span data-ttu-id="c9439-125">Se uma determinada coluna não estiver presente no registro, nenhum valor de coluna será retornado.</span><span class="sxs-lookup"><span data-stu-id="c9439-125">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="c9439-126">Normalmente, o valor padrão para a coluna, se houver, seria retornado nesse caso.</span><span class="sxs-lookup"><span data-stu-id="c9439-126">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="c9439-127">É garantido que, se a coluna for definida como um valor diferente do valor padrão, esse valor diferente será retornado (ou seja, se uma coluna com um valor padrão for explicitamente definida como NULL, um NULL será retornado como o valor dessa coluna).</span><span class="sxs-lookup"><span data-stu-id="c9439-127">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to NULL then a NULL will be returned as the value for that column).</span></span> <span data-ttu-id="c9439-128">Mesmo que essa opção seja solicitada, ainda é possível ver um valor de coluna que é igual ao valor padrão.</span><span class="sxs-lookup"><span data-stu-id="c9439-128">Even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="c9439-129">Nenhum esforço é feito para remover valores de coluna que correspondam aos valores padrão.</span><span class="sxs-lookup"><span data-stu-id="c9439-129">No effort is made to remove column values that match their default values.</span></span> <span data-ttu-id="c9439-130">É importante lembrar que essa opção afeta a saída de <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> quando usada com EnumeratePresenceOnly ou EnumerateTaggedOnly.</span><span class="sxs-lookup"><span data-stu-id="c9439-130">It is important to remember that this option affects the output of <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> when used with EnumeratePresenceOnly or EnumerateTaggedOnly.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c9439-131">EnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="c9439-131">EnumeratePresenceOnly</span></span></td>
<td><span data-ttu-id="c9439-132">Se existir um valor não nulo para o valor de coluna ou coluna solicitado, os dados associados não serão retornados.</span><span class="sxs-lookup"><span data-stu-id="c9439-132">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="c9439-133">Em vez disso, o status associado para essa coluna ou valor de coluna será definido como <a href="hh557250(v=exchg.10).md">ColumnPresent</a>.</span><span class="sxs-lookup"><span data-stu-id="c9439-133">Instead, the associated status for that column or column value will be set to <a href="hh557250(v=exchg.10).md">ColumnPresent</a>.</span></span> <span data-ttu-id="c9439-134">Se o valor da coluna ou coluna for nulo, <a href="hh557250(v=exchg.10).md">ColumnNull</a> será retornado como de costume.</span><span class="sxs-lookup"><span data-stu-id="c9439-134">If the column or column value is NULL then <a href="hh557250(v=exchg.10).md">ColumnNull</a> will be returned as usual.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c9439-135">EnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="c9439-135">EnumerateTaggedOnly</span></span></td>
<td><span data-ttu-id="c9439-136">Ao enumerar todos os valores de coluna no registro (por exemplo, ou seja, quando numColumnids for zero), somente os valores de coluna marcados serão retornados.</span><span class="sxs-lookup"><span data-stu-id="c9439-136">When enumerating all column values in the record (for example,that is when numColumnids is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="c9439-137">Essa opção não é permitida ao enumerar uma matriz específica de IDs de coluna.</span><span class="sxs-lookup"><span data-stu-id="c9439-137">This option is not allowed when enumerating a specific array of column IDs.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c9439-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9439-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c9439-139">Referência</span><span class="sxs-lookup"><span data-stu-id="c9439-139">Reference</span></span>

[<span data-ttu-id="c9439-140">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c9439-140">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="c9439-141">EnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="c9439-141">EnumerateIgnoreUserDefinedDefault</span></span>](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[<span data-ttu-id="c9439-142">EnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="c9439-142">EnumerateInRecordOnly</span></span>](./windows7grbits.enumerateinrecordonly-field.md)
