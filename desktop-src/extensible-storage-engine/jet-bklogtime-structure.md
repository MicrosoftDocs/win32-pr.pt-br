---
description: 'Saiba mais sobre: estrutura de JET_BKLOGTIME'
title: Estrutura de JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: 0b3ebfd1c0b807a491695ba18d6735e0230a16fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790530"
---
# <a name="jet_bklogtime-structure"></a><span data-ttu-id="da285-103">Estrutura de JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="da285-103">JET_BKLOGTIME Structure</span></span>


<span data-ttu-id="da285-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="da285-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bklogtime-structure"></a><span data-ttu-id="da285-105">Estrutura de JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="da285-105">JET_BKLOGTIME Structure</span></span>

<span data-ttu-id="da285-106">A estrutura de **JET_BKLOGTIME** contém os elementos de data e hora de um evento.</span><span class="sxs-lookup"><span data-stu-id="da285-106">The **JET_BKLOGTIME** structure holds the date and time elements of an event.</span></span> <span data-ttu-id="da285-107">É uma extensão de [JET_LOGTIME](./jet-logtime-structure.md).</span><span class="sxs-lookup"><span data-stu-id="da285-107">It is an extension of [JET_LOGTIME](./jet-logtime-structure.md).</span></span>

<span data-ttu-id="da285-108">**Windows Vista: a JET_BKLOGTIME** é introduzida no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="da285-108">**Windows Vista:  JET_BKLOGTIME** is introduced in Windows Vista.</span></span>

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a><span data-ttu-id="da285-109">Membros</span><span class="sxs-lookup"><span data-stu-id="da285-109">Members</span></span>

<span data-ttu-id="da285-110">**bSeconds**</span><span class="sxs-lookup"><span data-stu-id="da285-110">**bSeconds**</span></span>

<span data-ttu-id="da285-111">A hora do evento em segundos.</span><span class="sxs-lookup"><span data-stu-id="da285-111">The time of the event in seconds.</span></span> <span data-ttu-id="da285-112">Isso pode ser 0 (zero) a 60.</span><span class="sxs-lookup"><span data-stu-id="da285-112">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="da285-113">0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".</span><span class="sxs-lookup"><span data-stu-id="da285-113">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="da285-114">**bMinutes**</span><span class="sxs-lookup"><span data-stu-id="da285-114">**bMinutes**</span></span>

<span data-ttu-id="da285-115">A hora do evento em minutos.</span><span class="sxs-lookup"><span data-stu-id="da285-115">The time of the event in minutes.</span></span> <span data-ttu-id="da285-116">Isso pode ser 0 (zero) a 60.</span><span class="sxs-lookup"><span data-stu-id="da285-116">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="da285-117">0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".</span><span class="sxs-lookup"><span data-stu-id="da285-117">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="da285-118">**bHours**</span><span class="sxs-lookup"><span data-stu-id="da285-118">**bHours**</span></span>

<span data-ttu-id="da285-119">A hora do evento em horas.</span><span class="sxs-lookup"><span data-stu-id="da285-119">The time of the event in hours.</span></span> <span data-ttu-id="da285-120">Isso pode ser 0 (zero) a 24.</span><span class="sxs-lookup"><span data-stu-id="da285-120">This can be 0 (zero) to 24.</span></span> <span data-ttu-id="da285-121">0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".</span><span class="sxs-lookup"><span data-stu-id="da285-121">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="da285-122">**bDay**</span><span class="sxs-lookup"><span data-stu-id="da285-122">**bDay**</span></span>

<span data-ttu-id="da285-123">O dia do mês do evento.</span><span class="sxs-lookup"><span data-stu-id="da285-123">The day of the month of the event.</span></span> <span data-ttu-id="da285-124">Isso pode ser 0 (zero) a 31.</span><span class="sxs-lookup"><span data-stu-id="da285-124">This can be 0 (zero) to 31.</span></span> <span data-ttu-id="da285-125">0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".</span><span class="sxs-lookup"><span data-stu-id="da285-125">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="da285-126">**bMonth**</span><span class="sxs-lookup"><span data-stu-id="da285-126">**bMonth**</span></span>

<span data-ttu-id="da285-127">O mês do ano do evento.</span><span class="sxs-lookup"><span data-stu-id="da285-127">The month of the year of the event.</span></span> <span data-ttu-id="da285-128">Isso pode ser 0 (zero) a 12.</span><span class="sxs-lookup"><span data-stu-id="da285-128">This can be 0 (zero) to 12.</span></span> <span data-ttu-id="da285-129">0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".</span><span class="sxs-lookup"><span data-stu-id="da285-129">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="da285-130">**bYear**</span><span class="sxs-lookup"><span data-stu-id="da285-130">**bYear**</span></span>

<span data-ttu-id="da285-131">O ano (deslocamento de 1900) do evento.</span><span class="sxs-lookup"><span data-stu-id="da285-131">The year (offset by 1900) of the event.</span></span> <span data-ttu-id="da285-132">Para obter o ano real, adicione 1900 a esse valor.</span><span class="sxs-lookup"><span data-stu-id="da285-132">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="da285-133">0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".</span><span class="sxs-lookup"><span data-stu-id="da285-133">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="da285-134">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="da285-134">**bFiller1**</span></span>

<span data-ttu-id="da285-135">Esse campo deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="da285-135">This field should be ignored.</span></span>

<span data-ttu-id="da285-136">**fTimeIsUTC**</span><span class="sxs-lookup"><span data-stu-id="da285-136">**fTimeIsUTC**</span></span>

<span data-ttu-id="da285-137">A hora está no formato UTC.</span><span class="sxs-lookup"><span data-stu-id="da285-137">The time is in UTC format.</span></span>

<span data-ttu-id="da285-138">**fUnused**</span><span class="sxs-lookup"><span data-stu-id="da285-138">**fUnused**</span></span>

<span data-ttu-id="da285-139">Esse campo deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="da285-139">This field should be ignored.</span></span>

<span data-ttu-id="da285-140">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="da285-140">**bFiller2**</span></span>

<span data-ttu-id="da285-141">Esse campo deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="da285-141">This field should be ignored.</span></span>

<span data-ttu-id="da285-142">**fOSSnapshot**</span><span class="sxs-lookup"><span data-stu-id="da285-142">**fOSSnapshot**</span></span>

<span data-ttu-id="da285-143">Se esse evento for um backup, esse sinalizador conterá um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="da285-143">If this event is a backup, this flag contains one of the following possible values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da285-144">Nome</span><span class="sxs-lookup"><span data-stu-id="da285-144">Name</span></span></p></th>
<th><p><span data-ttu-id="da285-145">Valor</span><span class="sxs-lookup"><span data-stu-id="da285-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da285-146">backup de streaming</span><span class="sxs-lookup"><span data-stu-id="da285-146">streaming backup</span></span></p></td>
<td><p><span data-ttu-id="da285-147">0 (zero)</span><span class="sxs-lookup"><span data-stu-id="da285-147">0 (zero)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da285-148">backup de instantâneo</span><span class="sxs-lookup"><span data-stu-id="da285-148">snapshot backup</span></span></p></td>
<td><p><span data-ttu-id="da285-149">1</span><span class="sxs-lookup"><span data-stu-id="da285-149">1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="da285-150">**fReserved**</span><span class="sxs-lookup"><span data-stu-id="da285-150">**fReserved**</span></span>

<span data-ttu-id="da285-151">Esse campo deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="da285-151">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="da285-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="da285-152">Remarks</span></span>

<span data-ttu-id="da285-153">Essa estrutura é usada durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="da285-153">This structure is used when debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="da285-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da285-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da285-155"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="da285-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="da285-156">Requer o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="da285-156">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da285-157"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="da285-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="da285-158">Requer o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="da285-158">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da285-159"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="da285-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="da285-160">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="da285-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="da285-161">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="da285-161">See Also</span></span>

[<span data-ttu-id="da285-162">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="da285-162">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="da285-163">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="da285-163">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
