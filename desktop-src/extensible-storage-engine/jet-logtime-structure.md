---
description: 'Saiba mais sobre: estrutura de JET_LOGTIME'
title: Estrutura de JET_LOGTIME
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
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
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103664131"
---
# <a name="jet_logtime-structure"></a><span data-ttu-id="c631f-103">Estrutura de JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="c631f-103">JET_LOGTIME Structure</span></span>


<span data-ttu-id="c631f-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c631f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_logtime-structure"></a><span data-ttu-id="c631f-105">Estrutura de JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="c631f-105">JET_LOGTIME Structure</span></span>

<span data-ttu-id="c631f-106">A estrutura de **JET_LOGTIME** contém elementos da data e hora de um evento.</span><span class="sxs-lookup"><span data-stu-id="c631f-106">The **JET_LOGTIME** structure holds elements of the date and time of an event.</span></span>

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a><span data-ttu-id="c631f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c631f-107">Members</span></span>

<span data-ttu-id="c631f-108">**bSeconds**</span><span class="sxs-lookup"><span data-stu-id="c631f-108">**bSeconds**</span></span>

<span data-ttu-id="c631f-109">A hora do evento em segundos.</span><span class="sxs-lookup"><span data-stu-id="c631f-109">The time of the event in seconds.</span></span> <span data-ttu-id="c631f-110">Esse valor pode ser de 0 a 59.</span><span class="sxs-lookup"><span data-stu-id="c631f-110">This value can be 0 to 59.</span></span> <span data-ttu-id="c631f-111">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="c631f-111">0 is used when the structure is null.</span></span>

<span data-ttu-id="c631f-112">**bMinutes**</span><span class="sxs-lookup"><span data-stu-id="c631f-112">**bMinutes**</span></span>

<span data-ttu-id="c631f-113">A hora do evento em minutos.</span><span class="sxs-lookup"><span data-stu-id="c631f-113">The time of the event in minutes.</span></span> <span data-ttu-id="c631f-114">Esse valor pode ser de 0 a 59.</span><span class="sxs-lookup"><span data-stu-id="c631f-114">This value can be 0 to 59.</span></span> <span data-ttu-id="c631f-115">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="c631f-115">0 is used when the structure is null.</span></span>

<span data-ttu-id="c631f-116">**bHours**</span><span class="sxs-lookup"><span data-stu-id="c631f-116">**bHours**</span></span>

<span data-ttu-id="c631f-117">A hora do evento em horas.</span><span class="sxs-lookup"><span data-stu-id="c631f-117">The time of the event in hours.</span></span> <span data-ttu-id="c631f-118">Esse valor pode ser de 0 a 23.</span><span class="sxs-lookup"><span data-stu-id="c631f-118">This value can be 0 to 23.</span></span> <span data-ttu-id="c631f-119">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="c631f-119">0 is used when the structure is null.</span></span>

<span data-ttu-id="c631f-120">**bDay**</span><span class="sxs-lookup"><span data-stu-id="c631f-120">**bDay**</span></span>

<span data-ttu-id="c631f-121">O dia do mês do evento.</span><span class="sxs-lookup"><span data-stu-id="c631f-121">The day of the month of the event.</span></span> <span data-ttu-id="c631f-122">Esse valor pode ser de 0 a 31.</span><span class="sxs-lookup"><span data-stu-id="c631f-122">This value can be 0 to 31.</span></span> <span data-ttu-id="c631f-123">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="c631f-123">0 is used when the structure is null.</span></span>

<span data-ttu-id="c631f-124">**bMonth**</span><span class="sxs-lookup"><span data-stu-id="c631f-124">**bMonth**</span></span>

<span data-ttu-id="c631f-125">O mês do ano do evento.</span><span class="sxs-lookup"><span data-stu-id="c631f-125">The month of the year of the event.</span></span> <span data-ttu-id="c631f-126">Esse valor pode ser de 0 a 12.</span><span class="sxs-lookup"><span data-stu-id="c631f-126">This value can be 0 to 12.</span></span> <span data-ttu-id="c631f-127">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="c631f-127">0 is used when the structure is null.</span></span>

<span data-ttu-id="c631f-128">**bYear**</span><span class="sxs-lookup"><span data-stu-id="c631f-128">**bYear**</span></span>

<span data-ttu-id="c631f-129">O ano do evento (offset de 1900).</span><span class="sxs-lookup"><span data-stu-id="c631f-129">The year of the event (offset by 1900).</span></span> <span data-ttu-id="c631f-130">Para obter o ano real, adicione 1900 a esse valor.</span><span class="sxs-lookup"><span data-stu-id="c631f-130">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="c631f-131">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="c631f-131">0 is used when the structure is null.</span></span>

<span data-ttu-id="c631f-132">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="c631f-132">**bFiller1**</span></span>

<span data-ttu-id="c631f-133">Esse campo deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c631f-133">This field should be ignored.</span></span>

<span data-ttu-id="c631f-134">**fTimeIsUTC**</span><span class="sxs-lookup"><span data-stu-id="c631f-134">**fTimeIsUTC**</span></span>

<span data-ttu-id="c631f-135">A hora está no formato UTC.</span><span class="sxs-lookup"><span data-stu-id="c631f-135">The time is in UTC format.</span></span>

<span data-ttu-id="c631f-136">**fUnused**</span><span class="sxs-lookup"><span data-stu-id="c631f-136">**fUnused**</span></span>

<span data-ttu-id="c631f-137">Esse campo deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c631f-137">This field should be ignored.</span></span>

<span data-ttu-id="c631f-138">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="c631f-138">**bFiller2**</span></span>

<span data-ttu-id="c631f-139">Esse campo deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c631f-139">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="c631f-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="c631f-140">Remarks</span></span>

<span data-ttu-id="c631f-141">Essa estrutura destina-se principalmente ao uso na depuração.</span><span class="sxs-lookup"><span data-stu-id="c631f-141">This structure is meant primarily for usage in debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="c631f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c631f-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c631f-143"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c631f-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c631f-144">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c631f-144">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c631f-145"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="c631f-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c631f-146">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c631f-146">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c631f-147"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="c631f-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c631f-148">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c631f-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c631f-149">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c631f-149">See Also</span></span>

[<span data-ttu-id="c631f-150">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="c631f-150">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
