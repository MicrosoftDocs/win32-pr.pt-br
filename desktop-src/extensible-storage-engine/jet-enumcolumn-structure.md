---
description: 'Saiba mais sobre: estrutura de JET_ENUMCOLUMN'
title: Estrutura JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca204fef4e67e6883584511b1ac424149a137b79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089908"
---
# <a name="jet_enumcolumn-structure"></a><span data-ttu-id="c4804-103">Estrutura JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="c4804-103">JET_ENUMCOLUMN Structure</span></span>


<span data-ttu-id="c4804-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c4804-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumn-structure"></a><span data-ttu-id="c4804-105">Estrutura JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="c4804-105">JET_ENUMCOLUMN Structure</span></span>

<span data-ttu-id="c4804-106">A estrutura de **JET_ENUMCOLUMN** enumera os valores de coluna de um registro quando a função [JetEnumerateColumns](./jetenumeratecolumns-function.md) é usada.</span><span class="sxs-lookup"><span data-stu-id="c4804-106">The **JET_ENUMCOLUMN** structure enumerates the column values of a record when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="c4804-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) retorna uma matriz de estruturas de **JET_ENUMCOLUMN** .</span><span class="sxs-lookup"><span data-stu-id="c4804-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMN** structures.</span></span> <span data-ttu-id="c4804-108">A matriz é retornada na memória que é alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para essa API.</span><span class="sxs-lookup"><span data-stu-id="c4804-108">The array is returned in memory that is allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that API.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a><span data-ttu-id="c4804-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c4804-109">Members</span></span>

<span data-ttu-id="c4804-110">**columnid**</span><span class="sxs-lookup"><span data-stu-id="c4804-110">**columnid**</span></span>

<span data-ttu-id="c4804-111">A ID da coluna que foi enumerada.</span><span class="sxs-lookup"><span data-stu-id="c4804-111">The column ID that was enumerated.</span></span>

<span data-ttu-id="c4804-112">**erra**</span><span class="sxs-lookup"><span data-stu-id="c4804-112">**err**</span></span>

<span data-ttu-id="c4804-113">O código de status da coluna que resulta da enumeração da coluna.</span><span class="sxs-lookup"><span data-stu-id="c4804-113">The column status code that results from the enumeration of the column.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4804-114">Códigos de erro</span><span class="sxs-lookup"><span data-stu-id="c4804-114">Error Codes</span></span></p></th>
<th><p><span data-ttu-id="c4804-115">Significado</span><span class="sxs-lookup"><span data-stu-id="c4804-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4804-116">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="c4804-116">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="c4804-117">A ID da coluna está fora dos limites legais de uma ID de coluna.</span><span class="sxs-lookup"><span data-stu-id="c4804-117">The column ID is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4804-118">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="c4804-118">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="c4804-119">A coluna descrita pela ID da coluna não existe na tabela.</span><span class="sxs-lookup"><span data-stu-id="c4804-119">The column described by the column ID does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4804-120">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="c4804-120">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="c4804-121">Todos os valores desta coluna são nulos.</span><span class="sxs-lookup"><span data-stu-id="c4804-121">All values for this column are NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4804-122">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="c4804-122">JET_wrnColumnPresent</span></span></p></td>
<td><p><span data-ttu-id="c4804-123">JET_bitEnumeratePresenceOnly foi especificado e pelo menos um valor de coluna não nulo teria sido retornado para esta coluna.</span><span class="sxs-lookup"><span data-stu-id="c4804-123">JET_bitEnumeratePresenceOnly was specified and at least one non-NULL column value would have been returned for this column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4804-124">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="c4804-124">JET_wrnColumnSingleValue</span></span></p></td>
<td><p><span data-ttu-id="c4804-125">JET_bitEnumerateCompressOutput foi especificado e exatamente um valor de coluna não nulo foi retornado para esta coluna.</span><span class="sxs-lookup"><span data-stu-id="c4804-125">JET_bitEnumerateCompressOutput was specified and exactly one non-NULL column value has been returned for this column.</span></span> <span data-ttu-id="c4804-126">Como resultado, a forma compactada de <strong>JET_ENUMCOLUMN</strong> foi retornada.</span><span class="sxs-lookup"><span data-stu-id="c4804-126">As a result, the compressed form of <strong>JET_ENUMCOLUMN</strong> has been returned.</span></span> <span data-ttu-id="c4804-127">Consulte <strong>JET_ENUMCOLUMN</strong> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c4804-127">See <strong>JET_ENUMCOLUMN</strong> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4804-128">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="c4804-128">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="c4804-129">A ID da coluna no struct <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> correspondente a este <strong>JET_ENUMCOLUMN</strong> struct era zero.</span><span class="sxs-lookup"><span data-stu-id="c4804-129">The column ID in the <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> struct corresponding to this <strong>JET_ENUMCOLUMN</strong> struct was zero.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c4804-130">**cEnumColumnValue**</span><span class="sxs-lookup"><span data-stu-id="c4804-130">**cEnumColumnValue**</span></span>

<span data-ttu-id="c4804-131">A matriz de valores de coluna que foi enumerada para a coluna.</span><span class="sxs-lookup"><span data-stu-id="c4804-131">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="c4804-132">O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4804-132">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="c4804-133">Esse buffer de saída é usado quando o código de status da coluna não é igual a JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="c4804-133">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="c4804-134">Para obter mais informações, consulte [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4804-134">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="c4804-135">Isso será retornado se "Err \! = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="c4804-135">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="c4804-136">**rgEnumColumnValue**</span><span class="sxs-lookup"><span data-stu-id="c4804-136">**rgEnumColumnValue**</span></span>

<span data-ttu-id="c4804-137">A matriz de valores de coluna que foi enumerada para a coluna.</span><span class="sxs-lookup"><span data-stu-id="c4804-137">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="c4804-138">O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4804-138">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="c4804-139">Esse buffer de saída é usado quando o código de status da coluna não é igual a JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="c4804-139">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="c4804-140">Para obter mais informações, consulte [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4804-140">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="c4804-141">Isso será retornado se "Err \! = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="c4804-141">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="c4804-142">**cbData**</span><span class="sxs-lookup"><span data-stu-id="c4804-142">**cbData**</span></span>

<span data-ttu-id="c4804-143">O valor da coluna que foi enumerado para a coluna.</span><span class="sxs-lookup"><span data-stu-id="c4804-143">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="c4804-144">O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4804-144">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="c4804-145">Esse buffer de saída só é usado quando o código de status da coluna é JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="c4804-145">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="c4804-146">Para obter mais informações, consulte [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4804-146">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="c4804-147">Isso será retornado se "Err = = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="c4804-147">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="c4804-148">**pvData**</span><span class="sxs-lookup"><span data-stu-id="c4804-148">**pvData**</span></span>

<span data-ttu-id="c4804-149">O valor da coluna que foi enumerado para a coluna.</span><span class="sxs-lookup"><span data-stu-id="c4804-149">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="c4804-150">O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4804-150">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="c4804-151">Esse buffer de saída só é usado quando o código de status da coluna é JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="c4804-151">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="c4804-152">Para obter mais informações, consulte [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="c4804-152">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="c4804-153">Isso será retornado se "Err = = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="c4804-153">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

### <a name="requirements"></a><span data-ttu-id="c4804-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4804-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4804-155"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c4804-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c4804-156">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c4804-156">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4804-157"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="c4804-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c4804-158">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c4804-158">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4804-159"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="c4804-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c4804-160">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c4804-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c4804-161">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c4804-161">See Also</span></span>

[<span data-ttu-id="c4804-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="c4804-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="c4804-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c4804-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c4804-164">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="c4804-164">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="c4804-165">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="c4804-165">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="c4804-166">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="c4804-166">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="c4804-167">realloc</span><span class="sxs-lookup"><span data-stu-id="c4804-167">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
