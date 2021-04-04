---
description: Este tópico define os identificadores de calendário (tipo de dados CALID) que são usados para especificar calendários diferentes.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Identificadores de calendário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647063"
---
# <a name="calendar-identifiers"></a><span data-ttu-id="1141d-103">Identificadores de calendário</span><span class="sxs-lookup"><span data-stu-id="1141d-103">Calendar Identifiers</span></span>

<span data-ttu-id="1141d-104">Este tópico define os identificadores de calendário (tipo de dados CALID) que são usados para especificar calendários diferentes.</span><span class="sxs-lookup"><span data-stu-id="1141d-104">This topic defines the calendar identifiers (data type CALID) that are used to specify different calendars.</span></span> <span data-ttu-id="1141d-105">Seus aplicativos podem usar esses identificadores ao usar as seguintes funções NLS e funções de retorno de chamada, que têm parâmetros que usam o tipo de dados CALID:</span><span class="sxs-lookup"><span data-stu-id="1141d-105">Your applications can use these identifiers when using the following NLS functions and callback functions, which have parameters that take the CALID data type:</span></span>

-   [<span data-ttu-id="1141d-106">**ConvertSystemTimeToCalDateTime**</span><span class="sxs-lookup"><span data-stu-id="1141d-106">**ConvertSystemTimeToCalDateTime**</span></span>](convertsystemtimetocaldatetime.md)
-   [<span data-ttu-id="1141d-107">**EnumCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="1141d-107">**EnumCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [<span data-ttu-id="1141d-108">**EnumCalendarInfoEx**</span><span class="sxs-lookup"><span data-stu-id="1141d-108">**EnumCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [<span data-ttu-id="1141d-109">**EnumCalendarInfoExEx**</span><span class="sxs-lookup"><span data-stu-id="1141d-109">**EnumCalendarInfoExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   <span data-ttu-id="1141d-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1141d-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span></span>
-   <span data-ttu-id="1141d-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1141d-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span></span>
-   [<span data-ttu-id="1141d-112">**GetCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="1141d-112">**GetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [<span data-ttu-id="1141d-113">**GetCalendarInfoEx**</span><span class="sxs-lookup"><span data-stu-id="1141d-113">**GetCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [<span data-ttu-id="1141d-114">**GetCalendarSupportedDateRange**</span><span class="sxs-lookup"><span data-stu-id="1141d-114">**GetCalendarSupportedDateRange**</span></span>](getcalendarsupporteddaterange.md)
-   [<span data-ttu-id="1141d-115">**IsCalendarLeapYear**</span><span class="sxs-lookup"><span data-stu-id="1141d-115">**IsCalendarLeapYear**</span></span>](iscalendarleapyear.md)
-   [<span data-ttu-id="1141d-116">**SetCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="1141d-116">**SetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

<span data-ttu-id="1141d-117">Os valores a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="1141d-117">The following values are defined.</span></span> <span data-ttu-id="1141d-118">Todos os outros valores são reservados.</span><span class="sxs-lookup"><span data-stu-id="1141d-118">All other values are reserved.</span></span> <span data-ttu-id="1141d-119">Esses valores não podem ser combinados entre si.</span><span class="sxs-lookup"><span data-stu-id="1141d-119">These values cannot be combined with one another.</span></span>



<span data-ttu-id="1141d-120">Identificador de calendário</span><span class="sxs-lookup"><span data-stu-id="1141d-120">Calendar identifier</span></span>

<span data-ttu-id="1141d-121">Significado</span><span class="sxs-lookup"><span data-stu-id="1141d-121">Meaning</span></span>

<span data-ttu-id="1141d-122">1</span><span class="sxs-lookup"><span data-stu-id="1141d-122">1</span></span>

<span data-ttu-id="1141d-123">CAL \_ gregoriano</span><span class="sxs-lookup"><span data-stu-id="1141d-123">CAL\_GREGORIAN</span></span>

<span data-ttu-id="1141d-124">Gregoriano (localizado)</span><span class="sxs-lookup"><span data-stu-id="1141d-124">Gregorian (localized)</span></span>

<span data-ttu-id="1141d-125">2</span><span class="sxs-lookup"><span data-stu-id="1141d-125">2</span></span>

<span data-ttu-id="1141d-126">CAL \_ gregoriano \_ dos EUA</span><span class="sxs-lookup"><span data-stu-id="1141d-126">CAL\_GREGORIAN\_US</span></span>

<span data-ttu-id="1141d-127">Gregoriano (sempre, cadeias de caracteres em inglês)</span><span class="sxs-lookup"><span data-stu-id="1141d-127">Gregorian (English strings always)</span></span>

<span data-ttu-id="1141d-128">3</span><span class="sxs-lookup"><span data-stu-id="1141d-128">3</span></span>

<span data-ttu-id="1141d-129">CAL do \_ Japão</span><span class="sxs-lookup"><span data-stu-id="1141d-129">CAL\_JAPAN</span></span>

<span data-ttu-id="1141d-130">Era do imperador japonês</span><span class="sxs-lookup"><span data-stu-id="1141d-130">Japanese Emperor Era</span></span>

<span data-ttu-id="1141d-131">4</span><span class="sxs-lookup"><span data-stu-id="1141d-131">4</span></span>

<span data-ttu-id="1141d-132">CAL \_ Taiwan</span><span class="sxs-lookup"><span data-stu-id="1141d-132">CAL\_TAIWAN</span></span>

<span data-ttu-id="1141d-133">Calendário de Taiwan</span><span class="sxs-lookup"><span data-stu-id="1141d-133">Taiwan calendar</span></span>

<span data-ttu-id="1141d-134">5</span><span class="sxs-lookup"><span data-stu-id="1141d-134">5</span></span>

<span data-ttu-id="1141d-135">Coreia do CAL \_</span><span class="sxs-lookup"><span data-stu-id="1141d-135">CAL\_KOREA</span></span>

<span data-ttu-id="1141d-136">Era coreano Tangun</span><span class="sxs-lookup"><span data-stu-id="1141d-136">Korean Tangun Era</span></span>

<span data-ttu-id="1141d-137">6</span><span class="sxs-lookup"><span data-stu-id="1141d-137">6</span></span>

<span data-ttu-id="1141d-138">HIJRI do CAL \_</span><span class="sxs-lookup"><span data-stu-id="1141d-138">CAL\_HIJRI</span></span>

<span data-ttu-id="1141d-139">Hijri (lunar árabe)</span><span class="sxs-lookup"><span data-stu-id="1141d-139">Hijri (Arabic Lunar)</span></span>

<span data-ttu-id="1141d-140">7</span><span class="sxs-lookup"><span data-stu-id="1141d-140">7</span></span>

<span data-ttu-id="1141d-141">CAL \_ tailandês</span><span class="sxs-lookup"><span data-stu-id="1141d-141">CAL\_THAI</span></span>

<span data-ttu-id="1141d-142">Tailandês</span><span class="sxs-lookup"><span data-stu-id="1141d-142">Thai</span></span>

<span data-ttu-id="1141d-143">8</span><span class="sxs-lookup"><span data-stu-id="1141d-143">8</span></span>

<span data-ttu-id="1141d-144">Hebraico da CAL \_</span><span class="sxs-lookup"><span data-stu-id="1141d-144">CAL\_HEBREW</span></span>

<span data-ttu-id="1141d-145">Hebraico (lunar)</span><span class="sxs-lookup"><span data-stu-id="1141d-145">Hebrew (Lunar)</span></span>

<span data-ttu-id="1141d-146">9</span><span class="sxs-lookup"><span data-stu-id="1141d-146">9</span></span>

<span data-ttu-id="1141d-147">CAL \_ gregoriano \_ me \_ francês</span><span class="sxs-lookup"><span data-stu-id="1141d-147">CAL\_GREGORIAN\_ME\_FRENCH</span></span>

<span data-ttu-id="1141d-148">Gregorian Middle East French</span><span class="sxs-lookup"><span data-stu-id="1141d-148">Gregorian Middle East French</span></span>

<span data-ttu-id="1141d-149">10</span><span class="sxs-lookup"><span data-stu-id="1141d-149">10</span></span>

<span data-ttu-id="1141d-150">CAL \_ gregoriano \_ árabe</span><span class="sxs-lookup"><span data-stu-id="1141d-150">CAL\_GREGORIAN\_ARABIC</span></span>

<span data-ttu-id="1141d-151">Gregorian Arabic</span><span class="sxs-lookup"><span data-stu-id="1141d-151">Gregorian Arabic</span></span>

<span data-ttu-id="1141d-152">11</span><span class="sxs-lookup"><span data-stu-id="1141d-152">11</span></span>

<span data-ttu-id="1141d-153">CAL \_ gregoriano \_ XLIT \_ Inglês</span><span class="sxs-lookup"><span data-stu-id="1141d-153">CAL\_GREGORIAN\_XLIT\_ENGLISH</span></span>

<span data-ttu-id="1141d-154">Gregoriano de transliteração em inglês</span><span class="sxs-lookup"><span data-stu-id="1141d-154">Gregorian transliterated English</span></span>

<span data-ttu-id="1141d-155">12</span><span class="sxs-lookup"><span data-stu-id="1141d-155">12</span></span>

<span data-ttu-id="1141d-156">CAL \_ gregoriano \_ XLIT \_ francês</span><span class="sxs-lookup"><span data-stu-id="1141d-156">CAL\_GREGORIAN\_XLIT\_FRENCH</span></span>

<span data-ttu-id="1141d-157">Gregoriano de transliteração francesa</span><span class="sxs-lookup"><span data-stu-id="1141d-157">Gregorian transliterated French</span></span>

<span data-ttu-id="1141d-158">23</span><span class="sxs-lookup"><span data-stu-id="1141d-158">23</span></span>

<span data-ttu-id="1141d-159">\_UMALQURA Cal</span><span class="sxs-lookup"><span data-stu-id="1141d-159">CAL\_UMALQURA</span></span>

<span data-ttu-id="1141d-160">**Windows Vista e posterior:** Calendário do um Al Qura (lunar árabe)</span><span class="sxs-lookup"><span data-stu-id="1141d-160">**Windows Vista and later:** Um Al Qura (Arabic lunar) calendar</span></span>



 

> [!Note]  
> <span data-ttu-id="1141d-161">A lacuna na numeração entre os identificadores CAL \_ gregoriano \_ XLIT \_ francês e Cal \_ UMALQURA é intencional.</span><span class="sxs-lookup"><span data-stu-id="1141d-161">The gap in numbering between the identifiers CAL\_GREGORIAN\_XLIT\_FRENCH and CAL\_UMALQURA is intentional.</span></span> <span data-ttu-id="1141d-162">O designador para CAL \_ UMALQURA é 23, e não 13.</span><span class="sxs-lookup"><span data-stu-id="1141d-162">The designator for CAL\_UMALQURA is 23, not 13.</span></span>

 

<span data-ttu-id="1141d-163">Além disso, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) e [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) permitem o uso do valor enumerar \_ todos os \_ calendários para solicitar uma enumeração de todos os calendários aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="1141d-163">In addition, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) and [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) allow the use of the value ENUM\_ALL\_CALENDARS to request an enumeration of all applicable calendars.</span></span>

<span data-ttu-id="1141d-164">Valor</span><span class="sxs-lookup"><span data-stu-id="1141d-164">Value</span></span>

<span data-ttu-id="1141d-165">Significado</span><span class="sxs-lookup"><span data-stu-id="1141d-165">Meaning</span></span>

<span data-ttu-id="1141d-166">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="1141d-166">0xffffffff</span></span>

<span data-ttu-id="1141d-167">ENUMERAr \_ todos os \_ calendários</span><span class="sxs-lookup"><span data-stu-id="1141d-167">ENUM\_ALL\_CALENDARS</span></span>

<span data-ttu-id="1141d-168">Todos os calendários aplicáveis para a localidade especificada</span><span class="sxs-lookup"><span data-stu-id="1141d-168">All applicable calendars for the specified locale</span></span>



 

 

 
