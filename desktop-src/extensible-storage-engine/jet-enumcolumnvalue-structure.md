---
description: 'Saiba mais sobre: estrutura de JET_ENUMCOLUMNVALUE'
title: Estrutura de JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788917"
---
# <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="6fc57-103">Estrutura de JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="6fc57-103">JET_ENUMCOLUMNVALUE Structure</span></span>


<span data-ttu-id="6fc57-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6fc57-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="6fc57-105">Estrutura de JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="6fc57-105">JET_ENUMCOLUMNVALUE Structure</span></span>

<span data-ttu-id="6fc57-106">A estrutura de **JET_ENUMCOLUMNVALUE** enumera os valores de coluna de um registro usando a função [JetEnumerateColumns](./jetenumeratecolumns-function.md) .</span><span class="sxs-lookup"><span data-stu-id="6fc57-106">The **JET_ENUMCOLUMNVALUE** structure enumerates the column values of a record using the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function.</span></span> <span data-ttu-id="6fc57-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) retorna uma matriz de estruturas de **JET_ENUMCOLUMNVALUE** .</span><span class="sxs-lookup"><span data-stu-id="6fc57-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNVALUE** structures.</span></span> <span data-ttu-id="6fc57-108">A matriz é retornada na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para essa função.</span><span class="sxs-lookup"><span data-stu-id="6fc57-108">The array is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that function.</span></span>

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a><span data-ttu-id="6fc57-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6fc57-109">Members</span></span>

<span data-ttu-id="6fc57-110">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="6fc57-110">**itagSequence**</span></span>

<span data-ttu-id="6fc57-111">O valor da coluna (por índice baseado em um) que foi enumerado.</span><span class="sxs-lookup"><span data-stu-id="6fc57-111">The column value (by one-based index) that was enumerated.</span></span>

<span data-ttu-id="6fc57-112">**erra**</span><span class="sxs-lookup"><span data-stu-id="6fc57-112">**err**</span></span>

<span data-ttu-id="6fc57-113">O código de status da coluna resultante da enumeração do valor da coluna.</span><span class="sxs-lookup"><span data-stu-id="6fc57-113">The column status code resulting from the enumeration of the column value.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6fc57-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6fc57-114">Value</span></span></p></th>
<th><p><span data-ttu-id="6fc57-115">Significado</span><span class="sxs-lookup"><span data-stu-id="6fc57-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fc57-116">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="6fc57-116">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="6fc57-117">O valor da coluna solicitada é nulo.</span><span class="sxs-lookup"><span data-stu-id="6fc57-117">The requested column value is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fc57-118">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="6fc57-118">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="6fc57-119">O <em>itagSequence</em> especificado no elemento da matriz <em>rgtagSequence</em> no struct <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> correspondente a este <strong>JET_ENUMCOLUMNVALUE</strong> struct era zero.</span><span class="sxs-lookup"><span data-stu-id="6fc57-119">The <em>itagSequence</em> that is specified in the element of the <em>rgtagSequence</em> array in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> struct corresponding to this <strong>JET_ENUMCOLUMNVALUE</strong> struct was zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fc57-120">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="6fc57-120">JET_wrnColumnTruncated</span></span></p></td>
<td><p><span data-ttu-id="6fc57-121">O valor da coluna solicitada foi truncado para o tamanho especificado antes de ser retornado.</span><span class="sxs-lookup"><span data-stu-id="6fc57-121">The requested column value was truncated to the specified size before being returned.</span></span></p>
<p><span data-ttu-id="6fc57-122">Esse truncamento ocorre apenas para longas colunas de texto e binários longos que contêm grandes quantidades de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc57-122">This truncation occurs only for long text and long binary columns that contain large amounts of data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6fc57-123">**cbData**</span><span class="sxs-lookup"><span data-stu-id="6fc57-123">**cbData**</span></span>

<span data-ttu-id="6fc57-124">O valor da coluna que foi enumerado para a coluna.</span><span class="sxs-lookup"><span data-stu-id="6fc57-124">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="6fc57-125">O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="6fc57-125">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="6fc57-126">**pvData**</span><span class="sxs-lookup"><span data-stu-id="6fc57-126">**pvData**</span></span>

<span data-ttu-id="6fc57-127">O valor da coluna que foi enumerado para a coluna.</span><span class="sxs-lookup"><span data-stu-id="6fc57-127">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="6fc57-128">O buffer de saída é retornado na memória que foi alocada usando o retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que foi fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="6fc57-128">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="6fc57-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fc57-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fc57-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6fc57-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc57-131">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="6fc57-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6fc57-132"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="6fc57-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc57-133">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="6fc57-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6fc57-134"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="6fc57-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6fc57-135">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6fc57-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="6fc57-136">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6fc57-136">See Also</span></span>

[<span data-ttu-id="6fc57-137">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="6fc57-137">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="6fc57-138">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="6fc57-138">JET_ENUMCOLUMNVALUE</span></span>]()  
[<span data-ttu-id="6fc57-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6fc57-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6fc57-140">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="6fc57-140">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="6fc57-141">realloc</span><span class="sxs-lookup"><span data-stu-id="6fc57-141">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
