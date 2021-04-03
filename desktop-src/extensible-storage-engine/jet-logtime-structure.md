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
# <a name="jet_logtime-structure"></a><span data-ttu-id="edf79-103">Estrutura de JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="edf79-103">JET_LOGTIME Structure</span></span>


<span data-ttu-id="edf79-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="edf79-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_logtime-structure"></a><span data-ttu-id="edf79-105">Estrutura de JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="edf79-105">JET_LOGTIME Structure</span></span>

<span data-ttu-id="edf79-106">A estrutura de **JET_LOGTIME** contém elementos da data e hora de um evento.</span><span class="sxs-lookup"><span data-stu-id="edf79-106">The **JET_LOGTIME** structure holds elements of the date and time of an event.</span></span>

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

### <a name="members"></a><span data-ttu-id="edf79-107">Membros</span><span class="sxs-lookup"><span data-stu-id="edf79-107">Members</span></span>

<span data-ttu-id="edf79-108">**bSeconds**</span><span class="sxs-lookup"><span data-stu-id="edf79-108">**bSeconds**</span></span>

<span data-ttu-id="edf79-109">A hora do evento em segundos.</span><span class="sxs-lookup"><span data-stu-id="edf79-109">The time of the event in seconds.</span></span> <span data-ttu-id="edf79-110">Esse valor pode ser de 0 a 59.</span><span class="sxs-lookup"><span data-stu-id="edf79-110">This value can be 0 to 59.</span></span> <span data-ttu-id="edf79-111">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="edf79-111">0 is used when the structure is null.</span></span>

<span data-ttu-id="edf79-112">**bMinutes**</span><span class="sxs-lookup"><span data-stu-id="edf79-112">**bMinutes**</span></span>

<span data-ttu-id="edf79-113">A hora do evento em minutos.</span><span class="sxs-lookup"><span data-stu-id="edf79-113">The time of the event in minutes.</span></span> <span data-ttu-id="edf79-114">Esse valor pode ser de 0 a 59.</span><span class="sxs-lookup"><span data-stu-id="edf79-114">This value can be 0 to 59.</span></span> <span data-ttu-id="edf79-115">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="edf79-115">0 is used when the structure is null.</span></span>

<span data-ttu-id="edf79-116">**bHours**</span><span class="sxs-lookup"><span data-stu-id="edf79-116">**bHours**</span></span>

<span data-ttu-id="edf79-117">A hora do evento em horas.</span><span class="sxs-lookup"><span data-stu-id="edf79-117">The time of the event in hours.</span></span> <span data-ttu-id="edf79-118">Esse valor pode ser de 0 a 23.</span><span class="sxs-lookup"><span data-stu-id="edf79-118">This value can be 0 to 23.</span></span> <span data-ttu-id="edf79-119">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="edf79-119">0 is used when the structure is null.</span></span>

<span data-ttu-id="edf79-120">**bDay**</span><span class="sxs-lookup"><span data-stu-id="edf79-120">**bDay**</span></span>

<span data-ttu-id="edf79-121">O dia do mês do evento.</span><span class="sxs-lookup"><span data-stu-id="edf79-121">The day of the month of the event.</span></span> <span data-ttu-id="edf79-122">Esse valor pode ser de 0 a 31.</span><span class="sxs-lookup"><span data-stu-id="edf79-122">This value can be 0 to 31.</span></span> <span data-ttu-id="edf79-123">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="edf79-123">0 is used when the structure is null.</span></span>

<span data-ttu-id="edf79-124">**bMonth**</span><span class="sxs-lookup"><span data-stu-id="edf79-124">**bMonth**</span></span>

<span data-ttu-id="edf79-125">O mês do ano do evento.</span><span class="sxs-lookup"><span data-stu-id="edf79-125">The month of the year of the event.</span></span> <span data-ttu-id="edf79-126">Esse valor pode ser de 0 a 12.</span><span class="sxs-lookup"><span data-stu-id="edf79-126">This value can be 0 to 12.</span></span> <span data-ttu-id="edf79-127">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="edf79-127">0 is used when the structure is null.</span></span>

<span data-ttu-id="edf79-128">**bYear**</span><span class="sxs-lookup"><span data-stu-id="edf79-128">**bYear**</span></span>

<span data-ttu-id="edf79-129">O ano do evento (offset de 1900).</span><span class="sxs-lookup"><span data-stu-id="edf79-129">The year of the event (offset by 1900).</span></span> <span data-ttu-id="edf79-130">Para obter o ano real, adicione 1900 a esse valor.</span><span class="sxs-lookup"><span data-stu-id="edf79-130">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="edf79-131">0 é usado quando a estrutura é nula.</span><span class="sxs-lookup"><span data-stu-id="edf79-131">0 is used when the structure is null.</span></span>

<span data-ttu-id="edf79-132">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="edf79-132">**bFiller1**</span></span>

<span data-ttu-id="edf79-133">Esse campo deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="edf79-133">This field should be ignored.</span></span>

<span data-ttu-id="edf79-134">**fTimeIsUTC**</span><span class="sxs-lookup"><span data-stu-id="edf79-134">**fTimeIsUTC**</span></span>

<span data-ttu-id="edf79-135">A hora está no formato UTC.</span><span class="sxs-lookup"><span data-stu-id="edf79-135">The time is in UTC format.</span></span>

<span data-ttu-id="edf79-136">**fUnused**</span><span class="sxs-lookup"><span data-stu-id="edf79-136">**fUnused**</span></span>

<span data-ttu-id="edf79-137">Esse campo deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="edf79-137">This field should be ignored.</span></span>

<span data-ttu-id="edf79-138">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="edf79-138">**bFiller2**</span></span>

<span data-ttu-id="edf79-139">Esse campo deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="edf79-139">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="edf79-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="edf79-140">Remarks</span></span>

<span data-ttu-id="edf79-141">Essa estrutura destina-se principalmente ao uso na depuração.</span><span class="sxs-lookup"><span data-stu-id="edf79-141">This structure is meant primarily for usage in debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="edf79-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edf79-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="edf79-143"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="edf79-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="edf79-144">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="edf79-144">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edf79-145"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="edf79-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="edf79-146">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="edf79-146">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edf79-147"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="edf79-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="edf79-148">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="edf79-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="edf79-149">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="edf79-149">See Also</span></span>

[<span data-ttu-id="edf79-150">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="edf79-150">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
