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
# <a name="jet_enumcolumn-structure"></a><span data-ttu-id="bf4dc-103">Estrutura JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="bf4dc-103">JET_ENUMCOLUMN Structure</span></span>


<span data-ttu-id="bf4dc-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bf4dc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumn-structure"></a><span data-ttu-id="bf4dc-105">Estrutura JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="bf4dc-105">JET_ENUMCOLUMN Structure</span></span>

<span data-ttu-id="bf4dc-106">A estrutura de **JET_ENUMCOLUMN** enumera os valores de coluna de um registro quando a função [JetEnumerateColumns](./jetenumeratecolumns-function.md) é usada.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-106">The **JET_ENUMCOLUMN** structure enumerates the column values of a record when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="bf4dc-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) retorna uma matriz de estruturas de **JET_ENUMCOLUMN** .</span><span class="sxs-lookup"><span data-stu-id="bf4dc-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMN** structures.</span></span> <span data-ttu-id="bf4dc-108">A matriz é retornada na memória que é alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para essa API.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-108">The array is returned in memory that is allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that API.</span></span>

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

### <a name="members"></a><span data-ttu-id="bf4dc-109">Membros</span><span class="sxs-lookup"><span data-stu-id="bf4dc-109">Members</span></span>

<span data-ttu-id="bf4dc-110">**columnid**</span><span class="sxs-lookup"><span data-stu-id="bf4dc-110">**columnid**</span></span>

<span data-ttu-id="bf4dc-111">A ID da coluna que foi enumerada.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-111">The column ID that was enumerated.</span></span>

<span data-ttu-id="bf4dc-112">**erra**</span><span class="sxs-lookup"><span data-stu-id="bf4dc-112">**err**</span></span>

<span data-ttu-id="bf4dc-113">O código de status da coluna que resulta da enumeração da coluna.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-113">The column status code that results from the enumeration of the column.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf4dc-114">Códigos de erro</span><span class="sxs-lookup"><span data-stu-id="bf4dc-114">Error Codes</span></span></p></th>
<th><p><span data-ttu-id="bf4dc-115">Significado</span><span class="sxs-lookup"><span data-stu-id="bf4dc-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf4dc-116">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="bf4dc-116">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="bf4dc-117">A ID da coluna está fora dos limites legais de uma ID de coluna.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-117">The column ID is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf4dc-118">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="bf4dc-118">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="bf4dc-119">A coluna descrita pela ID da coluna não existe na tabela.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-119">The column described by the column ID does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf4dc-120">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="bf4dc-120">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="bf4dc-121">Todos os valores desta coluna são nulos.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-121">All values for this column are NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf4dc-122">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="bf4dc-122">JET_wrnColumnPresent</span></span></p></td>
<td><p><span data-ttu-id="bf4dc-123">JET_bitEnumeratePresenceOnly foi especificado e pelo menos um valor de coluna não nulo teria sido retornado para esta coluna.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-123">JET_bitEnumeratePresenceOnly was specified and at least one non-NULL column value would have been returned for this column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf4dc-124">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="bf4dc-124">JET_wrnColumnSingleValue</span></span></p></td>
<td><p><span data-ttu-id="bf4dc-125">JET_bitEnumerateCompressOutput foi especificado e exatamente um valor de coluna não nulo foi retornado para esta coluna.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-125">JET_bitEnumerateCompressOutput was specified and exactly one non-NULL column value has been returned for this column.</span></span> <span data-ttu-id="bf4dc-126">Como resultado, a forma compactada de <strong>JET_ENUMCOLUMN</strong> foi retornada.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-126">As a result, the compressed form of <strong>JET_ENUMCOLUMN</strong> has been returned.</span></span> <span data-ttu-id="bf4dc-127">Consulte <strong>JET_ENUMCOLUMN</strong> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-127">See <strong>JET_ENUMCOLUMN</strong> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf4dc-128">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="bf4dc-128">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="bf4dc-129">A ID da coluna no struct <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> correspondente a este <strong>JET_ENUMCOLUMN</strong> struct era zero.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-129">The column ID in the <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> struct corresponding to this <strong>JET_ENUMCOLUMN</strong> struct was zero.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf4dc-130">**cEnumColumnValue**</span><span class="sxs-lookup"><span data-stu-id="bf4dc-130">**cEnumColumnValue**</span></span>

<span data-ttu-id="bf4dc-131">A matriz de valores de coluna que foi enumerada para a coluna.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-131">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="bf4dc-132">O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="bf4dc-132">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="bf4dc-133">Esse buffer de saída é usado quando o código de status da coluna não é igual a JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-133">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="bf4dc-134">Para obter mais informações, consulte [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="bf4dc-134">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="bf4dc-135">Isso será retornado se "Err \! = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="bf4dc-135">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="bf4dc-136">**rgEnumColumnValue**</span><span class="sxs-lookup"><span data-stu-id="bf4dc-136">**rgEnumColumnValue**</span></span>

<span data-ttu-id="bf4dc-137">A matriz de valores de coluna que foi enumerada para a coluna.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-137">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="bf4dc-138">O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="bf4dc-138">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="bf4dc-139">Esse buffer de saída é usado quando o código de status da coluna não é igual a JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-139">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="bf4dc-140">Para obter mais informações, consulte [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="bf4dc-140">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="bf4dc-141">Isso será retornado se "Err \! = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="bf4dc-141">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="bf4dc-142">**cbData**</span><span class="sxs-lookup"><span data-stu-id="bf4dc-142">**cbData**</span></span>

<span data-ttu-id="bf4dc-143">O valor da coluna que foi enumerado para a coluna.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-143">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="bf4dc-144">O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="bf4dc-144">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="bf4dc-145">Esse buffer de saída só é usado quando o código de status da coluna é JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-145">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="bf4dc-146">Para obter mais informações, consulte [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="bf4dc-146">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="bf4dc-147">Isso será retornado se "Err = = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="bf4dc-147">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="bf4dc-148">**pvData**</span><span class="sxs-lookup"><span data-stu-id="bf4dc-148">**pvData**</span></span>

<span data-ttu-id="bf4dc-149">O valor da coluna que foi enumerado para a coluna.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-149">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="bf4dc-150">O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="bf4dc-150">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="bf4dc-151">Esse buffer de saída só é usado quando o código de status da coluna é JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-151">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="bf4dc-152">Para obter mais informações, consulte [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="bf4dc-152">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="bf4dc-153">Isso será retornado se "Err = = JET_wrnColumnSingleValue".</span><span class="sxs-lookup"><span data-stu-id="bf4dc-153">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

### <a name="requirements"></a><span data-ttu-id="bf4dc-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf4dc-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf4dc-155"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="bf4dc-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bf4dc-156">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-156">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf4dc-157"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="bf4dc-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bf4dc-158">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-158">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf4dc-159"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="bf4dc-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bf4dc-160">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="bf4dc-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="bf4dc-161">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="bf4dc-161">See Also</span></span>

[<span data-ttu-id="bf4dc-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="bf4dc-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="bf4dc-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bf4dc-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bf4dc-164">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="bf4dc-164">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="bf4dc-165">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="bf4dc-165">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="bf4dc-166">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="bf4dc-166">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="bf4dc-167">realloc</span><span class="sxs-lookup"><span data-stu-id="bf4dc-167">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
