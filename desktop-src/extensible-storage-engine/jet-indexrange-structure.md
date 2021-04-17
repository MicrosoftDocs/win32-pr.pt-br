---
description: 'Saiba mais sobre: estrutura de JET_INDEXRANGE'
title: Estrutura de JET_INDEXRANGE
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: ecbd8151be8ef278fc1bddc12323f41abd05b09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790248"
---
# <a name="jet_indexrange-structure"></a><span data-ttu-id="f0c04-103">Estrutura de JET_INDEXRANGE</span><span class="sxs-lookup"><span data-stu-id="f0c04-103">JET_INDEXRANGE Structure</span></span>


<span data-ttu-id="f0c04-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f0c04-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexrange-structure"></a><span data-ttu-id="f0c04-105">Estrutura de JET_INDEXRANGE</span><span class="sxs-lookup"><span data-stu-id="f0c04-105">JET_INDEXRANGE Structure</span></span>

<span data-ttu-id="f0c04-106">A estrutura de **JET_INDEXRANGE** identifica um intervalo de índice quando ele é usado com a função [JetIntersectIndexes](./jetintersectindexes-function.md) .</span><span class="sxs-lookup"><span data-stu-id="f0c04-106">The **JET_INDEXRANGE** structure identifies an index range when it is used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a><span data-ttu-id="f0c04-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f0c04-107">Members</span></span>

<span data-ttu-id="f0c04-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="f0c04-108">**cbStruct**</span></span>

<span data-ttu-id="f0c04-109">O tamanho, em bytes, do **JET_INDEXRANGE**.</span><span class="sxs-lookup"><span data-stu-id="f0c04-109">The size, in bytes, of the **JET_INDEXRANGE**.</span></span>

<span data-ttu-id="f0c04-110">**TableID**</span><span class="sxs-lookup"><span data-stu-id="f0c04-110">**tableid**</span></span>

<span data-ttu-id="f0c04-111">Um cursor que anteriormente tinha um intervalo de índice definido com [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="f0c04-111">A cursor that has previously had an index range set with [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="f0c04-112">**grbit**</span><span class="sxs-lookup"><span data-stu-id="f0c04-112">**grbit**</span></span>

<span data-ttu-id="f0c04-113">Um bitmask composto de exatamente um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="f0c04-113">A bitmask composed of exactly one of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0c04-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f0c04-114">Value</span></span></p></th>
<th><p><span data-ttu-id="f0c04-115">Significado</span><span class="sxs-lookup"><span data-stu-id="f0c04-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0c04-116">JET_bitRecordInIndex</span><span class="sxs-lookup"><span data-stu-id="f0c04-116">JET_bitRecordInIndex</span></span></p></td>
<td><p><span data-ttu-id="f0c04-117">Especifica que o intervalo de índice deve ser tratado normalmente.</span><span class="sxs-lookup"><span data-stu-id="f0c04-117">Specifies that the index range should be treated normally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0c04-118">JET_bitRecordNotInIndex</span><span class="sxs-lookup"><span data-stu-id="f0c04-118">JET_bitRecordNotInIndex</span></span></p></td>
<td><p><span data-ttu-id="f0c04-119">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f0c04-119">Reserved for future use.</span></span> <span data-ttu-id="f0c04-120">Não use.</span><span class="sxs-lookup"><span data-stu-id="f0c04-120">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="f0c04-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0c04-121">Remarks</span></span>

<span data-ttu-id="f0c04-122">Cada estrutura de **JET_INDEXRANGE** que é passada para [JetIntersectIndexes](./jetintersectindexes-function.md) representa um intervalo de índice, que será interseccionado pela chamada à API.</span><span class="sxs-lookup"><span data-stu-id="f0c04-122">Each **JET_INDEXRANGE** structure that is passed to [JetIntersectIndexes](./jetintersectindexes-function.md) represents an index range, which will be intersected by the API call.</span></span> <span data-ttu-id="f0c04-123">O cursor que é fornecido em **JET_INDEXRANGE** deve ter um conjunto de intervalos de índice válido já, com uma chamada bem-sucedida para [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="f0c04-123">The cursor that is given in **JET_INDEXRANGE** must have a valid index range set on it already, with a successful call to [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="f0c04-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0c04-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0c04-125"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f0c04-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f0c04-126">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f0c04-126">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0c04-127"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="f0c04-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f0c04-128">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f0c04-128">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0c04-129"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="f0c04-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f0c04-130">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f0c04-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f0c04-131">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f0c04-131">See Also</span></span>

[<span data-ttu-id="f0c04-132">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="f0c04-132">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="f0c04-133">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f0c04-133">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f0c04-134">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f0c04-134">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f0c04-135">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="f0c04-135">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="f0c04-136">JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="f0c04-136">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="f0c04-137">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="f0c04-137">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
