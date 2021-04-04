---
description: 'Saiba mais sobre: estrutura de JET_RECORDLIST'
title: Estrutura de JET_RECORDLIST
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837066"
---
# <a name="jet_recordlist-structure"></a><span data-ttu-id="ee157-103">Estrutura de JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="ee157-103">JET_RECORDLIST Structure</span></span>


<span data-ttu-id="ee157-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ee157-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recordlist-structure"></a><span data-ttu-id="ee157-105">Estrutura de JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="ee157-105">JET_RECORDLIST Structure</span></span>

<span data-ttu-id="ee157-106">A estrutura de **JET_RECORDLIST** localiza os registros que estão na interseção de intervalos de índice especificados quando eles são usados com a função [JetIntersectIndexes](./jetintersectindexes-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ee157-106">The **JET_RECORDLIST** structure finds records that are in the intersection of specified index ranges when they are used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a><span data-ttu-id="ee157-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ee157-107">Members</span></span>

<span data-ttu-id="ee157-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="ee157-108">**cbStruct**</span></span>

<span data-ttu-id="ee157-109">O tamanho da estrutura de **JET_RECORDLIST** , em bytes.</span><span class="sxs-lookup"><span data-stu-id="ee157-109">The size of the **JET_RECORDLIST** structure, in bytes.</span></span>

<span data-ttu-id="ee157-110">**TableID**</span><span class="sxs-lookup"><span data-stu-id="ee157-110">**tableid**</span></span>

<span data-ttu-id="ee157-111">O identificador de tabela de uma tabela temporária que contém os indicadores para os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="ee157-111">The table identifier of a temporary table that contains the bookmarks for the results of the query.</span></span> <span data-ttu-id="ee157-112">A tabela será fechada automaticamente se a transação atual for revertida com [JetRollback](./jetrollback-function.md); caso contrário, ele deve ser fechado com [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="ee157-112">The table will automatically be closed if the current transaction is rolled back with [JetRollback](./jetrollback-function.md); otherwise, it must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="ee157-113">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="ee157-113">**cRecord**</span></span>

<span data-ttu-id="ee157-114">O número de linhas na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="ee157-114">The number of rows in the temporary table.</span></span>

<span data-ttu-id="ee157-115">**columnidBookmark**</span><span class="sxs-lookup"><span data-stu-id="ee157-115">**columnidBookmark**</span></span>

<span data-ttu-id="ee157-116">O identificador de coluna da coluna de indicadores na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="ee157-116">The column identifier of the bookmark column in the temporary table.</span></span>

### <a name="remarks"></a><span data-ttu-id="ee157-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee157-117">Remarks</span></span>

<span data-ttu-id="ee157-118">A tabela temporária que é identificada por **TableName** tem uma única coluna.</span><span class="sxs-lookup"><span data-stu-id="ee157-118">The temporary table that is identified by **tableid** has a single column.</span></span> <span data-ttu-id="ee157-119">Essa única coluna contém indicadores, e cada registro deve caber em um buffer de tamanho JET_cbBookmarkMost bytes.</span><span class="sxs-lookup"><span data-stu-id="ee157-119">That single column holds bookmarks, and each record should fit in a buffer of size JET_cbBookmarkMost bytes.</span></span>

### <a name="requirements"></a><span data-ttu-id="ee157-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee157-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee157-121"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="ee157-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ee157-122">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ee157-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee157-123"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="ee157-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ee157-124">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ee157-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee157-125"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="ee157-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ee157-126">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ee157-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ee157-127">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ee157-127">See Also</span></span>

[<span data-ttu-id="ee157-128">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="ee157-128">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="ee157-129">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="ee157-129">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="ee157-130">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ee157-130">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="ee157-131">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="ee157-131">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="ee157-132">JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="ee157-132">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="ee157-133">JetRollback</span><span class="sxs-lookup"><span data-stu-id="ee157-133">JetRollback</span></span>](./jetrollback-function.md)
