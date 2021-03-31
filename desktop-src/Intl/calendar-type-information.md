---
description: Este tópico descreve as informações de tipo de calendário (tipo de dados CALTYPE) usadas nas funções EnumCalendarInfo, EnumCalendarInfoEx, EnumCalendarInfoExEx, GetCalendarInfo e GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Informações de tipo de calendário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836853"
---
# <a name="calendar-type-information"></a><span data-ttu-id="70f2e-103">Informações de tipo de calendário</span><span class="sxs-lookup"><span data-stu-id="70f2e-103">Calendar Type Information</span></span>

<span data-ttu-id="70f2e-104">Este tópico descreve as informações de tipo de calendário (tipo de dados CALTYPE) usadas nas funções [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)e [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="70f2e-104">This topic describes the calendar type information (CALTYPE data type) used in the [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), and [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) functions.</span></span> <span data-ttu-id="70f2e-105">Alguns desses valores também são usados pela função [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) .</span><span class="sxs-lookup"><span data-stu-id="70f2e-105">Some of these values are also used by the [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) function.</span></span>

<span data-ttu-id="70f2e-106">As constantes CALTYPE a seguir podem ser usadas em combinação com quaisquer outras constantes CALTYPE.</span><span class="sxs-lookup"><span data-stu-id="70f2e-106">The following CALTYPE constants can be used in combination with any other CALTYPE constants.</span></span>



| <span data-ttu-id="70f2e-107">Constante</span><span class="sxs-lookup"><span data-stu-id="70f2e-107">Constant</span></span>                     | <span data-ttu-id="70f2e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="70f2e-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f2e-109">\_NOUSEROVERRIDE Cal</span><span class="sxs-lookup"><span data-stu-id="70f2e-109">CAL\_NOUSEROVERRIDE</span></span>          | <span data-ttu-id="70f2e-110">**Windows me/98, windows 2000:** Use o padrão do sistema em vez da opção do usuário.</span><span class="sxs-lookup"><span data-stu-id="70f2e-110">**Windows Me/98, Windows 2000:** Use the system default instead of the user's choice.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="70f2e-111">CAL \_ retornar \_ nomes de GENITIVE \_</span><span class="sxs-lookup"><span data-stu-id="70f2e-111">CAL\_RETURN\_GENITIVE\_NAMES</span></span> | <span data-ttu-id="70f2e-112">**Windows 7 e posterior:** Recupere o resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) na forma de nomes de genitive de meses, que são os nomes usados quando os nomes de mês são combinados com outros itens.</span><span class="sxs-lookup"><span data-stu-id="70f2e-112">**Windows 7 and later:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) in the form of genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="70f2e-113">Por exemplo, em ucraniano, o equivalente a janeiro é escrito "Січень" quando o mês é nomeado sozinho.</span><span class="sxs-lookup"><span data-stu-id="70f2e-113">For example, in Ukrainian the equivalent of January is written "Січень" when the month is named alone.</span></span> <span data-ttu-id="70f2e-114">No entanto, quando o nome do mês é usado em combinação, por exemplo, em uma data como 5 de janeiro de 2003, a forma genitive do nome é usada.</span><span class="sxs-lookup"><span data-stu-id="70f2e-114">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="70f2e-115">Para o exemplo ucraniano, o nome do mês genitive é exibido como "5 січня 2003".</span><span class="sxs-lookup"><span data-stu-id="70f2e-115">For the Ukrainian example, the genitive month name is displayed as "5 січня 2003".</span></span> <span data-ttu-id="70f2e-116">Para obter mais informações, consulte [localidade \_ Return \_ GENITIVE \_ Names](locale-return-constants.md).</span><span class="sxs-lookup"><span data-stu-id="70f2e-116">For more information, see [LOCALE\_RETURN\_GENITIVE\_NAMES](locale-return-constants.md).</span></span> |
| <span data-ttu-id="70f2e-117">\_número de retorno da Cal \_</span><span class="sxs-lookup"><span data-stu-id="70f2e-117">CAL\_RETURN\_NUMBER</span></span>          | <span data-ttu-id="70f2e-118">**Windows me/98, windows 2000:** Recupere o resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) como um número em vez de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="70f2e-118">**Windows Me/98, Windows 2000:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) as a number instead of a string.</span></span> <span data-ttu-id="70f2e-119">Isso só é válido para valores que começam com CAL \_ I.</span><span class="sxs-lookup"><span data-stu-id="70f2e-119">This is only valid for values beginning with CAL\_I.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="70f2e-120">CAL \_ usar \_ CP \_ ACP</span><span class="sxs-lookup"><span data-stu-id="70f2e-120">CAL\_USE\_CP\_ACP</span></span>            | <span data-ttu-id="70f2e-121">**Windows me/98, windows 2000:** Use a página de código ANSI (ACP) do sistema em vez da página de código de localidade para conversão de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="70f2e-121">**Windows Me/98, Windows 2000:** Use the system ANSI code page (ACP) instead of the locale code page for string translation.</span></span> <span data-ttu-id="70f2e-122">Isso só é relevante para versões ANSI de funções, por exemplo, **EnumCalendarInfoA**.</span><span class="sxs-lookup"><span data-stu-id="70f2e-122">This is only relevant for ANSI versions of functions, for example, **EnumCalendarInfoA**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="70f2e-123">As constantes CALTYPE a seguir são mutuamente exclusivas e não podem ser usadas em combinação umas com as outras em uma chamada de função.</span><span class="sxs-lookup"><span data-stu-id="70f2e-123">The following CALTYPE constants are mutually exclusive and cannot be used in combination with each other in a function call.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70f2e-124">Constante</span><span class="sxs-lookup"><span data-stu-id="70f2e-124">Constant</span></span></th>
<th><span data-ttu-id="70f2e-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="70f2e-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70f2e-126">CAL_ICALINTVALUE</span><span class="sxs-lookup"><span data-stu-id="70f2e-126">CAL_ICALINTVALUE</span></span></td>
<td><span data-ttu-id="70f2e-127">Um valor inteiro que indica o tipo de calendário do calendário alternativo.</span><span class="sxs-lookup"><span data-stu-id="70f2e-127">An integer value indicating the calendar type of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-128">CAL_ITWODIGITYEARMAX</span><span class="sxs-lookup"><span data-stu-id="70f2e-128">CAL_ITWODIGITYEARMAX</span></span></td>
<td><span data-ttu-id="70f2e-129"><strong>Windows me/98, windows 2000:</strong> Um valor inteiro que indica o limite superior do intervalo de anos de dois dígitos.</span><span class="sxs-lookup"><span data-stu-id="70f2e-129"><strong>Windows Me/98, Windows 2000:</strong> An integer value indicating the upper boundary of the two-digit year range.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-130">CAL_IYEAROFFSETRANGE</span><span class="sxs-lookup"><span data-stu-id="70f2e-130">CAL_IYEAROFFSETRANGE</span></span></td>
<td><span data-ttu-id="70f2e-131">Uma ou mais cadeias de caracteres terminadas em nulo que especificam os deslocamentos de ano para cada um dos intervalos de era.</span><span class="sxs-lookup"><span data-stu-id="70f2e-131">One or more null-terminated strings that specify the year offsets for each of the era ranges.</span></span> <span data-ttu-id="70f2e-132">A última cadeia de caracteres tem um caractere nulo de terminação extra.</span><span class="sxs-lookup"><span data-stu-id="70f2e-132">The last string has an extra terminating null character.</span></span> <span data-ttu-id="70f2e-133">Esse valor varia em formato, dependendo do tipo de calendário opcional.</span><span class="sxs-lookup"><span data-stu-id="70f2e-133">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-134">CAL_SABBREVDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="70f2e-134">CAL_SABBREVDAYNAME1</span></span></td>
<td><span data-ttu-id="70f2e-135">Nome nativo abreviado do primeiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-135">Abbreviated native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-136">CAL_SABBREVDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="70f2e-136">CAL_SABBREVDAYNAME2</span></span></td>
<td><span data-ttu-id="70f2e-137">Nome nativo abreviado do segundo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-137">Abbreviated native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-138">CAL_SABBREVDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="70f2e-138">CAL_SABBREVDAYNAME3</span></span></td>
<td><span data-ttu-id="70f2e-139">Nome nativo abreviado do terceiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-139">Abbreviated native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-140">CAL_SABBREVDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="70f2e-140">CAL_SABBREVDAYNAME4</span></span></td>
<td><span data-ttu-id="70f2e-141">Nome nativo abreviado do quarto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-141">Abbreviated native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-142">CAL_SABBREVDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="70f2e-142">CAL_SABBREVDAYNAME5</span></span></td>
<td><span data-ttu-id="70f2e-143">Nome nativo abreviado do quinto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-143">Abbreviated native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-144">CAL_SABBREVDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="70f2e-144">CAL_SABBREVDAYNAME6</span></span></td>
<td><span data-ttu-id="70f2e-145">Nome nativo abreviado do sexto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-145">Abbreviated native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-146">CAL_SABBREVDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="70f2e-146">CAL_SABBREVDAYNAME7</span></span></td>
<td><span data-ttu-id="70f2e-147">Nome nativo abreviado do sétimo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-147">Abbreviated native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-148">CAL_SABBREVERASTRING</span><span class="sxs-lookup"><span data-stu-id="70f2e-148">CAL_SABBREVERASTRING</span></span></td>
<td><span data-ttu-id="70f2e-149"><strong>Windows 7 e posterior:</strong> Nome nativo abreviado de uma era.</span><span class="sxs-lookup"><span data-stu-id="70f2e-149"><strong>Windows 7 and later:</strong> Abbreviated native name of an era.</span></span> <span data-ttu-id="70f2e-150">A era completa é representada pela constante de CAL_SERASTRING.</span><span class="sxs-lookup"><span data-stu-id="70f2e-150">The full era is represented by the CAL_SERASTRING constant.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-151">CAL_SABBREVMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="70f2e-151">CAL_SABBREVMONTHNAME1</span></span></td>
<td><span data-ttu-id="70f2e-152">Nome nativo abreviado do primeiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-152">Abbreviated native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-153">CAL_SABBREVMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="70f2e-153">CAL_SABBREVMONTHNAME2</span></span></td>
<td><span data-ttu-id="70f2e-154">Nome nativo abreviado do segundo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-154">Abbreviated native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-155">CAL_SABBREVMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="70f2e-155">CAL_SABBREVMONTHNAME3</span></span></td>
<td><span data-ttu-id="70f2e-156">Nome nativo abreviado do terceiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-156">Abbreviated native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-157">CAL_SABBREVMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="70f2e-157">CAL_SABBREVMONTHNAME4</span></span></td>
<td><span data-ttu-id="70f2e-158">Nome nativo abreviado do quarto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-158">Abbreviated native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-159">CAL_SABBREVMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="70f2e-159">CAL_SABBREVMONTHNAME5</span></span></td>
<td><span data-ttu-id="70f2e-160">Nome nativo abreviado do quinto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-160">Abbreviated native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-161">CAL_SABBREVMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="70f2e-161">CAL_SABBREVMONTHNAME6</span></span></td>
<td><span data-ttu-id="70f2e-162">Nome nativo abreviado do sexto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-162">Abbreviated native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-163">CAL_SABBREVMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="70f2e-163">CAL_SABBREVMONTHNAME7</span></span></td>
<td><span data-ttu-id="70f2e-164">Nome nativo abreviado do sétimo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-164">Abbreviated native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-165">CAL_SABBREVMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="70f2e-165">CAL_SABBREVMONTHNAME8</span></span></td>
<td><span data-ttu-id="70f2e-166">Nome nativo abreviado do oitavo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-166">Abbreviated native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-167">CAL_SABBREVMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="70f2e-167">CAL_SABBREVMONTHNAME9</span></span></td>
<td><span data-ttu-id="70f2e-168">Nome nativo abreviado do nono mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-168">Abbreviated native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-169">CAL_SABBREVMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="70f2e-169">CAL_SABBREVMONTHNAME10</span></span></td>
<td><span data-ttu-id="70f2e-170">Nome nativo abreviado do décimo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-170">Abbreviated native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-171">CAL_SABBREVMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="70f2e-171">CAL_SABBREVMONTHNAME11</span></span></td>
<td><span data-ttu-id="70f2e-172">Nome nativo abreviado do décimo primeiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-172">Abbreviated native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-173">CAL_SABBREVMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="70f2e-173">CAL_SABBREVMONTHNAME12</span></span></td>
<td><span data-ttu-id="70f2e-174">Nome nativo abreviado do décimo-mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-174">Abbreviated native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-175">CAL_SABBREVMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="70f2e-175">CAL_SABBREVMONTHNAME13</span></span></td>
<td><span data-ttu-id="70f2e-176">Nome nativo abreviado do décimo terceiro mês do ano, se existir.</span><span class="sxs-lookup"><span data-stu-id="70f2e-176">Abbreviated native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-177">CAL_SCALNAME</span><span class="sxs-lookup"><span data-stu-id="70f2e-177">CAL_SCALNAME</span></span></td>
<td><span data-ttu-id="70f2e-178">Nome nativo do calendário alternativo.</span><span class="sxs-lookup"><span data-stu-id="70f2e-178">Native name of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-179">CAL_SDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="70f2e-179">CAL_SDAYNAME1</span></span></td>
<td><span data-ttu-id="70f2e-180">Nome nativo do primeiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-180">Native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-181">CAL_SDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="70f2e-181">CAL_SDAYNAME2</span></span></td>
<td><span data-ttu-id="70f2e-182">Nome nativo do segundo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-182">Native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-183">CAL_SDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="70f2e-183">CAL_SDAYNAME3</span></span></td>
<td><span data-ttu-id="70f2e-184">Nome nativo do terceiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-184">Native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-185">CAL_SDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="70f2e-185">CAL_SDAYNAME4</span></span></td>
<td><span data-ttu-id="70f2e-186">Nome nativo do quarto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-186">Native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-187">CAL_SDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="70f2e-187">CAL_SDAYNAME5</span></span></td>
<td><span data-ttu-id="70f2e-188">Nome nativo do quinto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-188">Native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-189">CAL_SDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="70f2e-189">CAL_SDAYNAME6</span></span></td>
<td><span data-ttu-id="70f2e-190">Nome nativo do sexto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-190">Native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-191">CAL_SDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="70f2e-191">CAL_SDAYNAME7</span></span></td>
<td><span data-ttu-id="70f2e-192">Nome nativo do sétimo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-192">Native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-193">CAL_SERASTRING</span><span class="sxs-lookup"><span data-stu-id="70f2e-193">CAL_SERASTRING</span></span></td>
<td><span data-ttu-id="70f2e-194">Uma ou mais cadeias de caracteres terminadas em nulo que especificam cada um dos pontos de código Unicode especificando a era associada a CAL_IYEAROFFSETRANGE.</span><span class="sxs-lookup"><span data-stu-id="70f2e-194">One or more null-terminated strings that specify each of the Unicode code points specifying the era associated with CAL_IYEAROFFSETRANGE.</span></span> <span data-ttu-id="70f2e-195">A última cadeia de caracteres tem um caractere nulo de terminação extra.</span><span class="sxs-lookup"><span data-stu-id="70f2e-195">The last string has an extra terminating null character.</span></span> <span data-ttu-id="70f2e-196">Esse valor varia em formato, dependendo do tipo de calendário opcional.</span><span class="sxs-lookup"><span data-stu-id="70f2e-196">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-197">CAL_SLONGDATE</span><span class="sxs-lookup"><span data-stu-id="70f2e-197">CAL_SLONGDATE</span></span></td>
<td><span data-ttu-id="70f2e-198">Formatos de data por extenso para o tipo de calendário.</span><span class="sxs-lookup"><span data-stu-id="70f2e-198">Long date formats for the calendar type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-199">CAL_SMONTHDAY</span><span class="sxs-lookup"><span data-stu-id="70f2e-199">CAL_SMONTHDAY</span></span></td>
<td><span data-ttu-id="70f2e-200"><strong>Windows 7 e posterior:</strong> Formato do mês e dia para o tipo de calendário.</span><span class="sxs-lookup"><span data-stu-id="70f2e-200"><strong>Windows 7 and later:</strong> Format of the month and day for the calendar type.</span></span> <span data-ttu-id="70f2e-201">A formatação é semelhante à CAL_SLONGDATE.</span><span class="sxs-lookup"><span data-stu-id="70f2e-201">The formatting is similar to that for CAL_SLONGDATE.</span></span> <span data-ttu-id="70f2e-202">Por exemplo, se o padrão mês/dia for o nome completo do mês seguido do número do dia com zeros à esquerda, por exemplo, de &quot; setembro de 03 &quot; , o formato será &quot; MMMM dd &quot; .</span><span class="sxs-lookup"><span data-stu-id="70f2e-202">For example, if the Month/Day pattern is the full month name followed by the day number with leading zeros, for example, &quot;September 03&quot;, the format is &quot;MMMM dd&quot;.</span></span> <span data-ttu-id="70f2e-203">Aspas simples podem ser usadas para inserir caracteres que não são de formato, por exemplo, ' de ' em espanhol.</span><span class="sxs-lookup"><span data-stu-id="70f2e-203">Single quotation marks can be used to insert non-format characters, for example, 'de' in Spanish.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="70f2e-204">Este tipo de calendário dá suporte a apenas um formato.</span><span class="sxs-lookup"><span data-stu-id="70f2e-204">This calendar type supports only one format.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-205">CAL_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="70f2e-205">CAL_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="70f2e-206">Nome nativo do primeiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-206">Native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-207">CAL_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="70f2e-207">CAL_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="70f2e-208">Nome nativo do segundo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-208">Native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-209">CAL_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="70f2e-209">CAL_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="70f2e-210">Nome nativo do terceiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-210">Native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-211">CAL_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="70f2e-211">CAL_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="70f2e-212">Nome nativo do quarto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-212">Native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-213">CAL_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="70f2e-213">CAL_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="70f2e-214">Nome nativo do quinto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-214">Native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-215">CAL_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="70f2e-215">CAL_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="70f2e-216">Nome nativo do sexto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-216">Native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-217">CAL_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="70f2e-217">CAL_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="70f2e-218">Nome nativo do sétimo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-218">Native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-219">CAL_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="70f2e-219">CAL_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="70f2e-220">Nome nativo do oitavo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-220">Native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-221">CAL_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="70f2e-221">CAL_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="70f2e-222">Nome nativo do nono mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-222">Native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-223">CAL_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="70f2e-223">CAL_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="70f2e-224">Nome nativo do décimo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-224">Native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-225">CAL_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="70f2e-225">CAL_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="70f2e-226">Nome nativo do décimo primeiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-226">Native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-227">CAL_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="70f2e-227">CAL_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="70f2e-228">Nome nativo do décimo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="70f2e-228">Native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-229">CAL_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="70f2e-229">CAL_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="70f2e-230">Nome nativo do décimo terceiro mês do ano, se existir.</span><span class="sxs-lookup"><span data-stu-id="70f2e-230">Native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-231">CAL_SSHORTDATE</span><span class="sxs-lookup"><span data-stu-id="70f2e-231">CAL_SSHORTDATE</span></span></td>
<td><span data-ttu-id="70f2e-232">Formatos de data abreviada para o tipo de calendário.</span><span class="sxs-lookup"><span data-stu-id="70f2e-232">Short date formats for the calendar type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-233">CAL_SSHORTESTDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="70f2e-233">CAL_SSHORTESTDAYNAME1</span></span></td>
<td><span data-ttu-id="70f2e-234"><strong>Windows Vista e posterior:</strong> Nome nativo curto do primeiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-234"><strong>Windows Vista and later:</strong> Short native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-235">CAL_SSHORTESTDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="70f2e-235">CAL_SSHORTESTDAYNAME2</span></span></td>
<td><span data-ttu-id="70f2e-236"><strong>Windows Vista e posterior:</strong> Nome nativo curto do segundo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-236"><strong>Windows Vista and later:</strong> Short native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-237">CAL_SSHORTESTDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="70f2e-237">CAL_SSHORTESTDAYNAME3</span></span></td>
<td><span data-ttu-id="70f2e-238"><strong>Windows Vista e posterior:</strong> Nome nativo curto do terceiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-238"><strong>Windows Vista and later:</strong> Short native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-239">CAL_SSHORTESTDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="70f2e-239">CAL_SSHORTESTDAYNAME4</span></span></td>
<td><span data-ttu-id="70f2e-240"><strong>Windows Vista e posterior:</strong> Nome nativo curto do quarto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-240"><strong>Windows Vista and later:</strong> Short native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-241">CAL_SSHORTESTDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="70f2e-241">CAL_SSHORTESTDAYNAME5</span></span></td>
<td><span data-ttu-id="70f2e-242"><strong>Windows Vista e posterior:</strong> Nome nativo curto do quinto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-242"><strong>Windows Vista and later:</strong> Short native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-243">CAL_SSHORTESTDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="70f2e-243">CAL_SSHORTESTDAYNAME6</span></span></td>
<td><span data-ttu-id="70f2e-244"><strong>Windows Vista e posterior:</strong> Nome nativo curto do sexto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-244"><strong>Windows Vista and later:</strong> Short native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70f2e-245">CAL_SSHORTESTDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="70f2e-245">CAL_SSHORTESTDAYNAME7</span></span></td>
<td><span data-ttu-id="70f2e-246"><strong>Windows Vista e posterior:</strong> Nome nativo curto do sétimo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="70f2e-246"><strong>Windows Vista and later:</strong> Short native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70f2e-247">CAL_SYEARMONTH</span><span class="sxs-lookup"><span data-stu-id="70f2e-247">CAL_SYEARMONTH</span></span></td>
<td><span data-ttu-id="70f2e-248"><strong>Windows me/98, windows 2000:</strong> Os formatos de ano/mês para os calendários especificados.</span><span class="sxs-lookup"><span data-stu-id="70f2e-248"><strong>Windows Me/98, Windows 2000:</strong> The year/month formats for the specified calendars.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="70f2e-249">Se o nome nativo do dia da semana ou de um mês for uma cadeia de caracteres vazia, esse nome será idêntico ao nome especificado nas informações de localidade correspondentes e, portanto, não será duplicado aqui.</span><span class="sxs-lookup"><span data-stu-id="70f2e-249">If the native name for the day of the week or for a month is an empty string, that name is identical to the name specified in the corresponding locale information and therefore is not duplicated here.</span></span>

 

 

 




