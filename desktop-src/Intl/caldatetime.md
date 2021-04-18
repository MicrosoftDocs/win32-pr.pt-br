---
description: Preterido. Representa um instante no tempo, normalmente expresso como uma data e hora do dia e um calendário correspondente.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: Estrutura CALDATETIME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780138"
---
# <a name="caldatetime-structure"></a><span data-ttu-id="453bd-104">Estrutura CALDATETIME</span><span class="sxs-lookup"><span data-stu-id="453bd-104">CALDATETIME structure</span></span>

<span data-ttu-id="453bd-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="453bd-105">Deprecated.</span></span> <span data-ttu-id="453bd-106">Representa um instante no tempo, normalmente expresso como uma data e hora do dia e um calendário correspondente.</span><span class="sxs-lookup"><span data-stu-id="453bd-106">Represents an instant in time, typically expressed as a date and time of day and a corresponding calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="453bd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="453bd-107">Syntax</span></span>


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a><span data-ttu-id="453bd-108">Membros</span><span class="sxs-lookup"><span data-stu-id="453bd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="453bd-109">**CalId**</span><span class="sxs-lookup"><span data-stu-id="453bd-109">**CalId**</span></span>
</dt> <dd>

<span data-ttu-id="453bd-110">O [identificador de calendário](calendar-identifiers.md) para o instante no tempo.</span><span class="sxs-lookup"><span data-stu-id="453bd-110">The [calendar identifier](calendar-identifiers.md) for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="453bd-111">**Dourado**</span><span class="sxs-lookup"><span data-stu-id="453bd-111">**Era**</span></span>
</dt> <dd>

<span data-ttu-id="453bd-112">As informações de era para o instante em tempo.</span><span class="sxs-lookup"><span data-stu-id="453bd-112">The era information for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="453bd-113">**Year**</span><span class="sxs-lookup"><span data-stu-id="453bd-113">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="453bd-114">O ano para o instante no tempo.</span><span class="sxs-lookup"><span data-stu-id="453bd-114">The year for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="453bd-115">**Mês**</span><span class="sxs-lookup"><span data-stu-id="453bd-115">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="453bd-116">O mês para o instante no tempo.</span><span class="sxs-lookup"><span data-stu-id="453bd-116">The month for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="453bd-117">**Day**</span><span class="sxs-lookup"><span data-stu-id="453bd-117">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="453bd-118">O dia para o instante no tempo.</span><span class="sxs-lookup"><span data-stu-id="453bd-118">The day for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="453bd-119">**DayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="453bd-119">**DayOfWeek**</span></span>
</dt> <dd>

<span data-ttu-id="453bd-120">O dia da semana para o instante no tempo.</span><span class="sxs-lookup"><span data-stu-id="453bd-120">The day of the week for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="453bd-121">**Hora**</span><span class="sxs-lookup"><span data-stu-id="453bd-121">**Hour**</span></span>
</dt> <dd>

<span data-ttu-id="453bd-122">A hora para o instante no tempo.</span><span class="sxs-lookup"><span data-stu-id="453bd-122">The hour for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="453bd-123">**Demorar**</span><span class="sxs-lookup"><span data-stu-id="453bd-123">**Minute**</span></span>
</dt> <dd>

<span data-ttu-id="453bd-124">O minuto para o instante no tempo.</span><span class="sxs-lookup"><span data-stu-id="453bd-124">The minute for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="453bd-125">**Microssegundo**</span><span class="sxs-lookup"><span data-stu-id="453bd-125">**Second**</span></span>
</dt> <dd>

<span data-ttu-id="453bd-126">O segundo para o instante no tempo.</span><span class="sxs-lookup"><span data-stu-id="453bd-126">The second for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="453bd-127">**Traços**</span><span class="sxs-lookup"><span data-stu-id="453bd-127">**Tick**</span></span>
</dt> <dd>

<span data-ttu-id="453bd-128">O tique para o instante no tempo.</span><span class="sxs-lookup"><span data-stu-id="453bd-128">The tick for the instant in time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="453bd-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="453bd-129">Requirements</span></span>



| <span data-ttu-id="453bd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="453bd-130">Requirement</span></span> | <span data-ttu-id="453bd-131">Valor</span><span class="sxs-lookup"><span data-stu-id="453bd-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="453bd-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="453bd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="453bd-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="453bd-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="453bd-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="453bd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="453bd-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="453bd-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="453bd-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="453bd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="453bd-137">Estruturas de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="453bd-137">National Language Support Structures</span></span>](national-language-support-structures.md)
</dt> </dl>

 

 




