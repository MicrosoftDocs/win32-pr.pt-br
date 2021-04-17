---
description: 'Saiba mais sobre: estrutura de JET_INDEXID'
title: Estrutura de JET_INDEXID
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: e1a9c6a971e44604240d750163f0570937f9d4db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812009"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="d32bd-103">Estrutura de JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="d32bd-103">JET_INDEXID Structure</span></span>


<span data-ttu-id="d32bd-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d32bd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexid-structure"></a><span data-ttu-id="d32bd-105">Estrutura de JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="d32bd-105">JET_INDEXID Structure</span></span>

<span data-ttu-id="d32bd-106">A estrutura de **JET_INDEXID** contém uma ID de índice.</span><span class="sxs-lookup"><span data-stu-id="d32bd-106">The **JET_INDEXID** structure holds an index ID.</span></span> <span data-ttu-id="d32bd-107">Uma ID de índice é uma dica usada para acelerar a seleção do índice atual usando [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="d32bd-107">An index ID is a hint that is used to accelerate the selection of the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="d32bd-108">Ele é mais útil quando há um número muito grande de índices em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="d32bd-108">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="d32bd-109">A ID do índice pode ser recuperada usando [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="d32bd-109">The index ID can be retrieved using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a><span data-ttu-id="d32bd-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d32bd-110">Members</span></span>

<span data-ttu-id="d32bd-111">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="d32bd-111">**cbStruct**</span></span>

<span data-ttu-id="d32bd-112">O tamanho, em bytes, da ID do índice.</span><span class="sxs-lookup"><span data-stu-id="d32bd-112">The size, in bytes, of the index ID.</span></span>

<span data-ttu-id="d32bd-113">Esse é o tamanho real da ID de índice que é retornada no buffer de saída de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="d32bd-113">This is the actual size of the index ID that is returned in the output buffer from [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

<span data-ttu-id="d32bd-114">**rgbIndexId**</span><span class="sxs-lookup"><span data-stu-id="d32bd-114">**rgbIndexId**</span></span>

<span data-ttu-id="d32bd-115">Um BLOB opaco de informações que é usado pelo mecanismo para identificar rapidamente um índice em seu cache de esquema.</span><span class="sxs-lookup"><span data-stu-id="d32bd-115">An opaque BLOB of information that is used by the engine to quickly identify an index in its schema cache.</span></span>

<span data-ttu-id="d32bd-116">Não tente interpretar o BLOB de informações.</span><span class="sxs-lookup"><span data-stu-id="d32bd-116">Do not attempt to interpret the BLOB of information.</span></span> <span data-ttu-id="d32bd-117">Não é um tamanho definido.</span><span class="sxs-lookup"><span data-stu-id="d32bd-117">It is not a set size.</span></span>

### <a name="requirements"></a><span data-ttu-id="d32bd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d32bd-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d32bd-119"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d32bd-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d32bd-120">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d32bd-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d32bd-121"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="d32bd-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d32bd-122">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d32bd-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d32bd-123"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="d32bd-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d32bd-124">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d32bd-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d32bd-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d32bd-125">See Also</span></span>

[<span data-ttu-id="d32bd-126">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="d32bd-126">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="d32bd-127">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="d32bd-127">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="d32bd-128">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="d32bd-128">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="d32bd-129">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="d32bd-129">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
