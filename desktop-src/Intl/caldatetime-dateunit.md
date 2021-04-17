---
description: Preterido. Especifica as unidades de data para ajustar a estrutura CALDATETIME.
ms.assetid: 20d0cd7a-6e6b-4c82-9cfa-e4f4315d6362
title: Enumeração de CALDATETIME_DATEUNIT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME_DATEUNIT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6ce1f8929dd6e2f7de59d32d66229f73c062505c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761978"
---
# <a name="caldatetime_dateunit-enumeration"></a><span data-ttu-id="d11b0-104">\_Enumeração CALDATETIME DATEUNIT</span><span class="sxs-lookup"><span data-stu-id="d11b0-104">CALDATETIME\_DATEUNIT enumeration</span></span>

<span data-ttu-id="d11b0-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="d11b0-105">Deprecated.</span></span> <span data-ttu-id="d11b0-106">Especifica as unidades de data para ajustar a estrutura [**CALDATETIME**](caldatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="d11b0-106">Specifies the date units for adjusting the [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d11b0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d11b0-107">Syntax</span></span>


```C++
enum CALDATETIME_DATEUNIT {
  EraUnit, 
  YearUnit, 
  MonthUnit, 
  WeekUnit, 
  DayUnit, 
  HourUnit, 
  MinuteUnit, 
  SecondUnit, 
  TickUnit 

};
```



## <a name="constants"></a><span data-ttu-id="d11b0-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="d11b0-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d11b0-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**</span><span class="sxs-lookup"><span data-stu-id="d11b0-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d11b0-110">A unidade de data e hora da era.</span><span class="sxs-lookup"><span data-stu-id="d11b0-110">The era date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d11b0-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**</span><span class="sxs-lookup"><span data-stu-id="d11b0-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d11b0-112">A unidade de data e hora do ano.</span><span class="sxs-lookup"><span data-stu-id="d11b0-112">The year date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d11b0-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**</span><span class="sxs-lookup"><span data-stu-id="d11b0-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d11b0-114">A unidade de tempo de data do mês.</span><span class="sxs-lookup"><span data-stu-id="d11b0-114">The month date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d11b0-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**</span><span class="sxs-lookup"><span data-stu-id="d11b0-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d11b0-116">A unidade de data e hora da semana.</span><span class="sxs-lookup"><span data-stu-id="d11b0-116">The week date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d11b0-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**</span><span class="sxs-lookup"><span data-stu-id="d11b0-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d11b0-118">A unidade de data e hora do dia.</span><span class="sxs-lookup"><span data-stu-id="d11b0-118">The day date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d11b0-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**</span><span class="sxs-lookup"><span data-stu-id="d11b0-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d11b0-120">A unidade de data e hora.</span><span class="sxs-lookup"><span data-stu-id="d11b0-120">The hour date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d11b0-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**</span><span class="sxs-lookup"><span data-stu-id="d11b0-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d11b0-122">A unidade de data e hora do minuto.</span><span class="sxs-lookup"><span data-stu-id="d11b0-122">The minute date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d11b0-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**</span><span class="sxs-lookup"><span data-stu-id="d11b0-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d11b0-124">A segunda unidade de data e hora.</span><span class="sxs-lookup"><span data-stu-id="d11b0-124">The second date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="d11b0-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**</span><span class="sxs-lookup"><span data-stu-id="d11b0-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**</span></span>
</dt> <dd>

<span data-ttu-id="d11b0-126">A unidade de data e hora de tique.</span><span class="sxs-lookup"><span data-stu-id="d11b0-126">The tick date time unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d11b0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d11b0-127">Requirements</span></span>



| <span data-ttu-id="d11b0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d11b0-128">Requirement</span></span> | <span data-ttu-id="d11b0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d11b0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d11b0-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d11b0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d11b0-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d11b0-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d11b0-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d11b0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d11b0-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d11b0-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d11b0-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d11b0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d11b0-135">Tipos de enumeração de suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="d11b0-135">National Language Support Enumeration Types</span></span>](national-language-support-enumeration-types.md)
</dt> </dl>

 

 




