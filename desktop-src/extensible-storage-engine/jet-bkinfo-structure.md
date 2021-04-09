---
description: 'Saiba mais sobre: estrutura de JET_BKINFO'
title: Estrutura de JET_BKINFO
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171358"
---
# <a name="jet_bkinfo-structure"></a><span data-ttu-id="9d72b-103">Estrutura de JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="9d72b-103">JET_BKINFO Structure</span></span>


<span data-ttu-id="9d72b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9d72b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bkinfo-structure"></a><span data-ttu-id="9d72b-105">Estrutura de JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="9d72b-105">JET_BKINFO Structure</span></span>

<span data-ttu-id="9d72b-106">A estrutura de **JET_BKINFO** contém uma coleção de dados sobre um evento de backup específico.</span><span class="sxs-lookup"><span data-stu-id="9d72b-106">The **JET_BKINFO** structure holds a collection of data about a specific backup event.</span></span>

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a><span data-ttu-id="9d72b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9d72b-107">Members</span></span>

<span data-ttu-id="9d72b-108">**lgposMark**</span><span class="sxs-lookup"><span data-stu-id="9d72b-108">**lgposMark**</span></span>

<span data-ttu-id="9d72b-109">A ID deste backup.</span><span class="sxs-lookup"><span data-stu-id="9d72b-109">The ID of this backup.</span></span>

<span data-ttu-id="9d72b-110">**logtimeMark**</span><span class="sxs-lookup"><span data-stu-id="9d72b-110">**logtimeMark**</span></span>

<span data-ttu-id="9d72b-111">A hora deste evento de backup.</span><span class="sxs-lookup"><span data-stu-id="9d72b-111">The time of this backup event.</span></span>

<span data-ttu-id="9d72b-112">**bklogtimeMark**</span><span class="sxs-lookup"><span data-stu-id="9d72b-112">**bklogtimeMark**</span></span>

<span data-ttu-id="9d72b-113">A hora desse evento de backup, com bits adicionais para indicar um backup de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="9d72b-113">The time of this backup event, with additional bits to indicate a snapshot backup.</span></span>

<span data-ttu-id="9d72b-114">**Windows Vista: o bklogtimeMark** é introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9d72b-114">**Windows Vista:  bklogtimeMark** is introduced in Windows Vista.</span></span>

<span data-ttu-id="9d72b-115">**genLow**</span><span class="sxs-lookup"><span data-stu-id="9d72b-115">**genLow**</span></span>

<span data-ttu-id="9d72b-116">O número de geração de log baixo associado a este evento de backup.</span><span class="sxs-lookup"><span data-stu-id="9d72b-116">The low log generation number associated with this backup event.</span></span>

<span data-ttu-id="9d72b-117">**genHigh**</span><span class="sxs-lookup"><span data-stu-id="9d72b-117">**genHigh**</span></span>

<span data-ttu-id="9d72b-118">O número de geração de log alto associado a este evento de backup.</span><span class="sxs-lookup"><span data-stu-id="9d72b-118">The high log generation number associated with this backup event.</span></span>

### <a name="remarks"></a><span data-ttu-id="9d72b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d72b-119">Remarks</span></span>

<span data-ttu-id="9d72b-120">Essa estrutura é usada dentro da estrutura de [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) para representar dados sobre o evento de backup do banco de dado.</span><span class="sxs-lookup"><span data-stu-id="9d72b-120">This structure is used inside the [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) structure to represent data about the database backup event.</span></span>

### <a name="requirements"></a><span data-ttu-id="9d72b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d72b-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d72b-122"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9d72b-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9d72b-123">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9d72b-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d72b-124"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9d72b-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9d72b-125">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9d72b-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d72b-126"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9d72b-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9d72b-127">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9d72b-127">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9d72b-128">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9d72b-128">See Also</span></span>

[<span data-ttu-id="9d72b-129">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="9d72b-129">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="9d72b-130">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="9d72b-130">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="9d72b-131">JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="9d72b-131">JET_BKLOGTIME</span></span>](./jet-bklogtime-structure.md)  
[<span data-ttu-id="9d72b-132">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="9d72b-132">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
