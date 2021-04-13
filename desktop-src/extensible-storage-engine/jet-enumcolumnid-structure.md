---
description: 'Saiba mais sobre: estrutura de JET_ENUMCOLUMNID'
title: Estrutura de JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: 356b2a31c682a6ed0392a875c606cfaf20f1aeea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501666"
---
# <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="3cf07-103">Estrutura de JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="3cf07-103">JET_ENUMCOLUMNID Structure</span></span>


<span data-ttu-id="3cf07-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3cf07-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="3cf07-105">Estrutura de JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="3cf07-105">JET_ENUMCOLUMNID Structure</span></span>

<span data-ttu-id="3cf07-106">A estrutura de **JET_ENUMCOLUMNID** enumera um conjunto específico de colunas e, opcionalmente, um conjunto específico de vários valores para essas colunas quando a função [JetEnumerateColumns](./jetenumeratecolumns-function.md) é usada.</span><span class="sxs-lookup"><span data-stu-id="3cf07-106">The **JET_ENUMCOLUMNID** structure enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="3cf07-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) retorna uma matriz de estruturas de **JET_ENUMCOLUMNID** .</span><span class="sxs-lookup"><span data-stu-id="3cf07-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNID** structures.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a><span data-ttu-id="3cf07-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3cf07-108">Members</span></span>

<span data-ttu-id="3cf07-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="3cf07-109">**columnid**</span></span>

<span data-ttu-id="3cf07-110">A ID da coluna a ser enumerada.</span><span class="sxs-lookup"><span data-stu-id="3cf07-110">The column ID to enumerate.</span></span>

<span data-ttu-id="3cf07-111">Se a ID da coluna for 0 (zero), a enumeração dessa coluna será ignorada e um slot correspondente na matriz de saída de estruturas de [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) será gerado com um estado de coluna de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="3cf07-111">If the column ID is 0 (zero) then the enumeration of this column is skipped and a corresponding slot in the output array of [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) structures will be generated with a column state of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="3cf07-112">**ctagSequence**</span><span class="sxs-lookup"><span data-stu-id="3cf07-112">**ctagSequence**</span></span>

<span data-ttu-id="3cf07-113">Opcionalmente, identifica uma matriz de valores de coluna (por índice baseado em um) para enumerar para a ID de coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="3cf07-113">Optionally identifies an array of column values (by one-based index) to enumerate for the specified column ID.</span></span>

<span data-ttu-id="3cf07-114">Se **ctagSequence** for 0 (zero), **rgtagSequence** será ignorado e todos os valores de coluna para a ID de coluna especificada serão enumerados.</span><span class="sxs-lookup"><span data-stu-id="3cf07-114">If **ctagSequence** is 0 (zero) then **rgtagSequence** is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="3cf07-115">Se um elemento de **rgtagSequence** for 0 (zero), a enumeração desse valor de coluna (por índice baseado em um) será ignorada.</span><span class="sxs-lookup"><span data-stu-id="3cf07-115">If an element of **rgtagSequence** is 0 (zero), then the enumeration of that column value (by one-based index) will be skipped.</span></span> <span data-ttu-id="3cf07-116">Um slot correspondente na matriz de saída da estrutura de **JET_ENUMCOLUMNID** será gerado com um valor de status de coluna de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="3cf07-116">A corresponding slot in the output array of the **JET_ENUMCOLUMNID** structure will be generated with a column status value of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="3cf07-117">**rgtagSequence**</span><span class="sxs-lookup"><span data-stu-id="3cf07-117">**rgtagSequence**</span></span>

<span data-ttu-id="3cf07-118">Uma matriz de índices baseados em um na matriz de valores de coluna para uma determinada coluna.</span><span class="sxs-lookup"><span data-stu-id="3cf07-118">An array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="3cf07-119">Um único elemento é um **itagSequence** que é definido em [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span><span class="sxs-lookup"><span data-stu-id="3cf07-119">A single element is an **itagSequence** which is defined in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="3cf07-120">Um **itagSequence** de 0 (zero) significa "ignorar".</span><span class="sxs-lookup"><span data-stu-id="3cf07-120">An **itagSequence** of 0 (zero) means "skip".</span></span> <span data-ttu-id="3cf07-121">Um **itagSequence** de 1 significa retornar o primeiro valor de coluna da coluna, 2 significa o segundo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3cf07-121">An **itagSequence** of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

### <a name="requirements"></a><span data-ttu-id="3cf07-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cf07-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cf07-123"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="3cf07-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3cf07-124">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3cf07-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cf07-125"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="3cf07-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3cf07-126">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3cf07-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cf07-127"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="3cf07-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3cf07-128">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="3cf07-128">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3cf07-129">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3cf07-129">See Also</span></span>

[<span data-ttu-id="3cf07-130">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="3cf07-130">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="3cf07-131">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="3cf07-131">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="3cf07-132">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="3cf07-132">JET_ENUMCOLUMNID</span></span>]()  
[<span data-ttu-id="3cf07-133">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="3cf07-133">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="3cf07-134">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="3cf07-134">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
