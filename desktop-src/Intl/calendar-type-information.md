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
# <a name="calendar-type-information"></a><span data-ttu-id="54e01-103">Informações de tipo de calendário</span><span class="sxs-lookup"><span data-stu-id="54e01-103">Calendar Type Information</span></span>

<span data-ttu-id="54e01-104">Este tópico descreve as informações de tipo de calendário (tipo de dados CALTYPE) usadas nas funções [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)e [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="54e01-104">This topic describes the calendar type information (CALTYPE data type) used in the [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), and [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) functions.</span></span> <span data-ttu-id="54e01-105">Alguns desses valores também são usados pela função [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) .</span><span class="sxs-lookup"><span data-stu-id="54e01-105">Some of these values are also used by the [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) function.</span></span>

<span data-ttu-id="54e01-106">As constantes CALTYPE a seguir podem ser usadas em combinação com quaisquer outras constantes CALTYPE.</span><span class="sxs-lookup"><span data-stu-id="54e01-106">The following CALTYPE constants can be used in combination with any other CALTYPE constants.</span></span>



| <span data-ttu-id="54e01-107">Constante</span><span class="sxs-lookup"><span data-stu-id="54e01-107">Constant</span></span>                     | <span data-ttu-id="54e01-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="54e01-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54e01-109">\_NOUSEROVERRIDE Cal</span><span class="sxs-lookup"><span data-stu-id="54e01-109">CAL\_NOUSEROVERRIDE</span></span>          | <span data-ttu-id="54e01-110">**Windows me/98, windows 2000:** Use o padrão do sistema em vez da opção do usuário.</span><span class="sxs-lookup"><span data-stu-id="54e01-110">**Windows Me/98, Windows 2000:** Use the system default instead of the user's choice.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="54e01-111">CAL \_ retornar \_ nomes de GENITIVE \_</span><span class="sxs-lookup"><span data-stu-id="54e01-111">CAL\_RETURN\_GENITIVE\_NAMES</span></span> | <span data-ttu-id="54e01-112">**Windows 7 e posterior:** Recupere o resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) na forma de nomes de genitive de meses, que são os nomes usados quando os nomes de mês são combinados com outros itens.</span><span class="sxs-lookup"><span data-stu-id="54e01-112">**Windows 7 and later:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) in the form of genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="54e01-113">Por exemplo, em ucraniano, o equivalente a janeiro é escrito "Січень" quando o mês é nomeado sozinho.</span><span class="sxs-lookup"><span data-stu-id="54e01-113">For example, in Ukrainian the equivalent of January is written "Січень" when the month is named alone.</span></span> <span data-ttu-id="54e01-114">No entanto, quando o nome do mês é usado em combinação, por exemplo, em uma data como 5 de janeiro de 2003, a forma genitive do nome é usada.</span><span class="sxs-lookup"><span data-stu-id="54e01-114">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="54e01-115">Para o exemplo ucraniano, o nome do mês genitive é exibido como "5 січня 2003".</span><span class="sxs-lookup"><span data-stu-id="54e01-115">For the Ukrainian example, the genitive month name is displayed as "5 січня 2003".</span></span> <span data-ttu-id="54e01-116">Para obter mais informações, consulte [localidade \_ Return \_ GENITIVE \_ Names](locale-return-constants.md).</span><span class="sxs-lookup"><span data-stu-id="54e01-116">For more information, see [LOCALE\_RETURN\_GENITIVE\_NAMES](locale-return-constants.md).</span></span> |
| <span data-ttu-id="54e01-117">\_número de retorno da Cal \_</span><span class="sxs-lookup"><span data-stu-id="54e01-117">CAL\_RETURN\_NUMBER</span></span>          | <span data-ttu-id="54e01-118">**Windows me/98, windows 2000:** Recupere o resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) como um número em vez de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="54e01-118">**Windows Me/98, Windows 2000:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) as a number instead of a string.</span></span> <span data-ttu-id="54e01-119">Isso só é válido para valores que começam com CAL \_ I.</span><span class="sxs-lookup"><span data-stu-id="54e01-119">This is only valid for values beginning with CAL\_I.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="54e01-120">CAL \_ usar \_ CP \_ ACP</span><span class="sxs-lookup"><span data-stu-id="54e01-120">CAL\_USE\_CP\_ACP</span></span>            | <span data-ttu-id="54e01-121">**Windows me/98, windows 2000:** Use a página de código ANSI (ACP) do sistema em vez da página de código de localidade para conversão de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="54e01-121">**Windows Me/98, Windows 2000:** Use the system ANSI code page (ACP) instead of the locale code page for string translation.</span></span> <span data-ttu-id="54e01-122">Isso só é relevante para versões ANSI de funções, por exemplo, **EnumCalendarInfoA**.</span><span class="sxs-lookup"><span data-stu-id="54e01-122">This is only relevant for ANSI versions of functions, for example, **EnumCalendarInfoA**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="54e01-123">As constantes CALTYPE a seguir são mutuamente exclusivas e não podem ser usadas em combinação umas com as outras em uma chamada de função.</span><span class="sxs-lookup"><span data-stu-id="54e01-123">The following CALTYPE constants are mutually exclusive and cannot be used in combination with each other in a function call.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54e01-124">Constante</span><span class="sxs-lookup"><span data-stu-id="54e01-124">Constant</span></span></th>
<th><span data-ttu-id="54e01-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="54e01-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54e01-126">CAL_ICALINTVALUE</span><span class="sxs-lookup"><span data-stu-id="54e01-126">CAL_ICALINTVALUE</span></span></td>
<td><span data-ttu-id="54e01-127">Um valor inteiro que indica o tipo de calendário do calendário alternativo.</span><span class="sxs-lookup"><span data-stu-id="54e01-127">An integer value indicating the calendar type of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-128">CAL_ITWODIGITYEARMAX</span><span class="sxs-lookup"><span data-stu-id="54e01-128">CAL_ITWODIGITYEARMAX</span></span></td>
<td><span data-ttu-id="54e01-129"><strong>Windows me/98, windows 2000:</strong> Um valor inteiro que indica o limite superior do intervalo de anos de dois dígitos.</span><span class="sxs-lookup"><span data-stu-id="54e01-129"><strong>Windows Me/98, Windows 2000:</strong> An integer value indicating the upper boundary of the two-digit year range.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-130">CAL_IYEAROFFSETRANGE</span><span class="sxs-lookup"><span data-stu-id="54e01-130">CAL_IYEAROFFSETRANGE</span></span></td>
<td><span data-ttu-id="54e01-131">Uma ou mais cadeias de caracteres terminadas em nulo que especificam os deslocamentos de ano para cada um dos intervalos de era.</span><span class="sxs-lookup"><span data-stu-id="54e01-131">One or more null-terminated strings that specify the year offsets for each of the era ranges.</span></span> <span data-ttu-id="54e01-132">A última cadeia de caracteres tem um caractere nulo de terminação extra.</span><span class="sxs-lookup"><span data-stu-id="54e01-132">The last string has an extra terminating null character.</span></span> <span data-ttu-id="54e01-133">Esse valor varia em formato, dependendo do tipo de calendário opcional.</span><span class="sxs-lookup"><span data-stu-id="54e01-133">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-134">CAL_SABBREVDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="54e01-134">CAL_SABBREVDAYNAME1</span></span></td>
<td><span data-ttu-id="54e01-135">Nome nativo abreviado do primeiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-135">Abbreviated native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-136">CAL_SABBREVDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="54e01-136">CAL_SABBREVDAYNAME2</span></span></td>
<td><span data-ttu-id="54e01-137">Nome nativo abreviado do segundo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-137">Abbreviated native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-138">CAL_SABBREVDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="54e01-138">CAL_SABBREVDAYNAME3</span></span></td>
<td><span data-ttu-id="54e01-139">Nome nativo abreviado do terceiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-139">Abbreviated native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-140">CAL_SABBREVDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="54e01-140">CAL_SABBREVDAYNAME4</span></span></td>
<td><span data-ttu-id="54e01-141">Nome nativo abreviado do quarto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-141">Abbreviated native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-142">CAL_SABBREVDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="54e01-142">CAL_SABBREVDAYNAME5</span></span></td>
<td><span data-ttu-id="54e01-143">Nome nativo abreviado do quinto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-143">Abbreviated native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-144">CAL_SABBREVDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="54e01-144">CAL_SABBREVDAYNAME6</span></span></td>
<td><span data-ttu-id="54e01-145">Nome nativo abreviado do sexto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-145">Abbreviated native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-146">CAL_SABBREVDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="54e01-146">CAL_SABBREVDAYNAME7</span></span></td>
<td><span data-ttu-id="54e01-147">Nome nativo abreviado do sétimo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-147">Abbreviated native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-148">CAL_SABBREVERASTRING</span><span class="sxs-lookup"><span data-stu-id="54e01-148">CAL_SABBREVERASTRING</span></span></td>
<td><span data-ttu-id="54e01-149"><strong>Windows 7 e posterior:</strong> Nome nativo abreviado de uma era.</span><span class="sxs-lookup"><span data-stu-id="54e01-149"><strong>Windows 7 and later:</strong> Abbreviated native name of an era.</span></span> <span data-ttu-id="54e01-150">A era completa é representada pela constante de CAL_SERASTRING.</span><span class="sxs-lookup"><span data-stu-id="54e01-150">The full era is represented by the CAL_SERASTRING constant.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-151">CAL_SABBREVMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="54e01-151">CAL_SABBREVMONTHNAME1</span></span></td>
<td><span data-ttu-id="54e01-152">Nome nativo abreviado do primeiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-152">Abbreviated native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-153">CAL_SABBREVMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="54e01-153">CAL_SABBREVMONTHNAME2</span></span></td>
<td><span data-ttu-id="54e01-154">Nome nativo abreviado do segundo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-154">Abbreviated native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-155">CAL_SABBREVMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="54e01-155">CAL_SABBREVMONTHNAME3</span></span></td>
<td><span data-ttu-id="54e01-156">Nome nativo abreviado do terceiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-156">Abbreviated native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-157">CAL_SABBREVMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="54e01-157">CAL_SABBREVMONTHNAME4</span></span></td>
<td><span data-ttu-id="54e01-158">Nome nativo abreviado do quarto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-158">Abbreviated native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-159">CAL_SABBREVMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="54e01-159">CAL_SABBREVMONTHNAME5</span></span></td>
<td><span data-ttu-id="54e01-160">Nome nativo abreviado do quinto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-160">Abbreviated native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-161">CAL_SABBREVMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="54e01-161">CAL_SABBREVMONTHNAME6</span></span></td>
<td><span data-ttu-id="54e01-162">Nome nativo abreviado do sexto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-162">Abbreviated native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-163">CAL_SABBREVMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="54e01-163">CAL_SABBREVMONTHNAME7</span></span></td>
<td><span data-ttu-id="54e01-164">Nome nativo abreviado do sétimo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-164">Abbreviated native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-165">CAL_SABBREVMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="54e01-165">CAL_SABBREVMONTHNAME8</span></span></td>
<td><span data-ttu-id="54e01-166">Nome nativo abreviado do oitavo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-166">Abbreviated native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-167">CAL_SABBREVMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="54e01-167">CAL_SABBREVMONTHNAME9</span></span></td>
<td><span data-ttu-id="54e01-168">Nome nativo abreviado do nono mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-168">Abbreviated native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-169">CAL_SABBREVMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="54e01-169">CAL_SABBREVMONTHNAME10</span></span></td>
<td><span data-ttu-id="54e01-170">Nome nativo abreviado do décimo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-170">Abbreviated native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-171">CAL_SABBREVMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="54e01-171">CAL_SABBREVMONTHNAME11</span></span></td>
<td><span data-ttu-id="54e01-172">Nome nativo abreviado do décimo primeiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-172">Abbreviated native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-173">CAL_SABBREVMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="54e01-173">CAL_SABBREVMONTHNAME12</span></span></td>
<td><span data-ttu-id="54e01-174">Nome nativo abreviado do décimo-mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-174">Abbreviated native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-175">CAL_SABBREVMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="54e01-175">CAL_SABBREVMONTHNAME13</span></span></td>
<td><span data-ttu-id="54e01-176">Nome nativo abreviado do décimo terceiro mês do ano, se existir.</span><span class="sxs-lookup"><span data-stu-id="54e01-176">Abbreviated native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-177">CAL_SCALNAME</span><span class="sxs-lookup"><span data-stu-id="54e01-177">CAL_SCALNAME</span></span></td>
<td><span data-ttu-id="54e01-178">Nome nativo do calendário alternativo.</span><span class="sxs-lookup"><span data-stu-id="54e01-178">Native name of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-179">CAL_SDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="54e01-179">CAL_SDAYNAME1</span></span></td>
<td><span data-ttu-id="54e01-180">Nome nativo do primeiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-180">Native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-181">CAL_SDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="54e01-181">CAL_SDAYNAME2</span></span></td>
<td><span data-ttu-id="54e01-182">Nome nativo do segundo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-182">Native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-183">CAL_SDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="54e01-183">CAL_SDAYNAME3</span></span></td>
<td><span data-ttu-id="54e01-184">Nome nativo do terceiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-184">Native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-185">CAL_SDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="54e01-185">CAL_SDAYNAME4</span></span></td>
<td><span data-ttu-id="54e01-186">Nome nativo do quarto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-186">Native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-187">CAL_SDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="54e01-187">CAL_SDAYNAME5</span></span></td>
<td><span data-ttu-id="54e01-188">Nome nativo do quinto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-188">Native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-189">CAL_SDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="54e01-189">CAL_SDAYNAME6</span></span></td>
<td><span data-ttu-id="54e01-190">Nome nativo do sexto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-190">Native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-191">CAL_SDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="54e01-191">CAL_SDAYNAME7</span></span></td>
<td><span data-ttu-id="54e01-192">Nome nativo do sétimo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-192">Native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-193">CAL_SERASTRING</span><span class="sxs-lookup"><span data-stu-id="54e01-193">CAL_SERASTRING</span></span></td>
<td><span data-ttu-id="54e01-194">Uma ou mais cadeias de caracteres terminadas em nulo que especificam cada um dos pontos de código Unicode especificando a era associada a CAL_IYEAROFFSETRANGE.</span><span class="sxs-lookup"><span data-stu-id="54e01-194">One or more null-terminated strings that specify each of the Unicode code points specifying the era associated with CAL_IYEAROFFSETRANGE.</span></span> <span data-ttu-id="54e01-195">A última cadeia de caracteres tem um caractere nulo de terminação extra.</span><span class="sxs-lookup"><span data-stu-id="54e01-195">The last string has an extra terminating null character.</span></span> <span data-ttu-id="54e01-196">Esse valor varia em formato, dependendo do tipo de calendário opcional.</span><span class="sxs-lookup"><span data-stu-id="54e01-196">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-197">CAL_SLONGDATE</span><span class="sxs-lookup"><span data-stu-id="54e01-197">CAL_SLONGDATE</span></span></td>
<td><span data-ttu-id="54e01-198">Formatos de data por extenso para o tipo de calendário.</span><span class="sxs-lookup"><span data-stu-id="54e01-198">Long date formats for the calendar type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-199">CAL_SMONTHDAY</span><span class="sxs-lookup"><span data-stu-id="54e01-199">CAL_SMONTHDAY</span></span></td>
<td><span data-ttu-id="54e01-200"><strong>Windows 7 e posterior:</strong> Formato do mês e dia para o tipo de calendário.</span><span class="sxs-lookup"><span data-stu-id="54e01-200"><strong>Windows 7 and later:</strong> Format of the month and day for the calendar type.</span></span> <span data-ttu-id="54e01-201">A formatação é semelhante à CAL_SLONGDATE.</span><span class="sxs-lookup"><span data-stu-id="54e01-201">The formatting is similar to that for CAL_SLONGDATE.</span></span> <span data-ttu-id="54e01-202">Por exemplo, se o padrão mês/dia for o nome completo do mês seguido do número do dia com zeros à esquerda, por exemplo, de &quot; setembro de 03 &quot; , o formato será &quot; MMMM dd &quot; .</span><span class="sxs-lookup"><span data-stu-id="54e01-202">For example, if the Month/Day pattern is the full month name followed by the day number with leading zeros, for example, &quot;September 03&quot;, the format is &quot;MMMM dd&quot;.</span></span> <span data-ttu-id="54e01-203">Aspas simples podem ser usadas para inserir caracteres que não são de formato, por exemplo, ' de ' em espanhol.</span><span class="sxs-lookup"><span data-stu-id="54e01-203">Single quotation marks can be used to insert non-format characters, for example, 'de' in Spanish.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="54e01-204">Este tipo de calendário dá suporte a apenas um formato.</span><span class="sxs-lookup"><span data-stu-id="54e01-204">This calendar type supports only one format.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-205">CAL_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="54e01-205">CAL_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="54e01-206">Nome nativo do primeiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-206">Native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-207">CAL_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="54e01-207">CAL_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="54e01-208">Nome nativo do segundo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-208">Native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-209">CAL_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="54e01-209">CAL_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="54e01-210">Nome nativo do terceiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-210">Native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-211">CAL_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="54e01-211">CAL_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="54e01-212">Nome nativo do quarto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-212">Native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-213">CAL_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="54e01-213">CAL_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="54e01-214">Nome nativo do quinto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-214">Native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-215">CAL_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="54e01-215">CAL_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="54e01-216">Nome nativo do sexto mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-216">Native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-217">CAL_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="54e01-217">CAL_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="54e01-218">Nome nativo do sétimo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-218">Native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-219">CAL_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="54e01-219">CAL_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="54e01-220">Nome nativo do oitavo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-220">Native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-221">CAL_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="54e01-221">CAL_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="54e01-222">Nome nativo do nono mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-222">Native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-223">CAL_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="54e01-223">CAL_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="54e01-224">Nome nativo do décimo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-224">Native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-225">CAL_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="54e01-225">CAL_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="54e01-226">Nome nativo do décimo primeiro mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-226">Native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-227">CAL_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="54e01-227">CAL_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="54e01-228">Nome nativo do décimo mês do ano.</span><span class="sxs-lookup"><span data-stu-id="54e01-228">Native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-229">CAL_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="54e01-229">CAL_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="54e01-230">Nome nativo do décimo terceiro mês do ano, se existir.</span><span class="sxs-lookup"><span data-stu-id="54e01-230">Native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-231">CAL_SSHORTDATE</span><span class="sxs-lookup"><span data-stu-id="54e01-231">CAL_SSHORTDATE</span></span></td>
<td><span data-ttu-id="54e01-232">Formatos de data abreviada para o tipo de calendário.</span><span class="sxs-lookup"><span data-stu-id="54e01-232">Short date formats for the calendar type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-233">CAL_SSHORTESTDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="54e01-233">CAL_SSHORTESTDAYNAME1</span></span></td>
<td><span data-ttu-id="54e01-234"><strong>Windows Vista e posterior:</strong> Nome nativo curto do primeiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-234"><strong>Windows Vista and later:</strong> Short native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-235">CAL_SSHORTESTDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="54e01-235">CAL_SSHORTESTDAYNAME2</span></span></td>
<td><span data-ttu-id="54e01-236"><strong>Windows Vista e posterior:</strong> Nome nativo curto do segundo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-236"><strong>Windows Vista and later:</strong> Short native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-237">CAL_SSHORTESTDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="54e01-237">CAL_SSHORTESTDAYNAME3</span></span></td>
<td><span data-ttu-id="54e01-238"><strong>Windows Vista e posterior:</strong> Nome nativo curto do terceiro dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-238"><strong>Windows Vista and later:</strong> Short native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-239">CAL_SSHORTESTDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="54e01-239">CAL_SSHORTESTDAYNAME4</span></span></td>
<td><span data-ttu-id="54e01-240"><strong>Windows Vista e posterior:</strong> Nome nativo curto do quarto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-240"><strong>Windows Vista and later:</strong> Short native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-241">CAL_SSHORTESTDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="54e01-241">CAL_SSHORTESTDAYNAME5</span></span></td>
<td><span data-ttu-id="54e01-242"><strong>Windows Vista e posterior:</strong> Nome nativo curto do quinto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-242"><strong>Windows Vista and later:</strong> Short native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-243">CAL_SSHORTESTDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="54e01-243">CAL_SSHORTESTDAYNAME6</span></span></td>
<td><span data-ttu-id="54e01-244"><strong>Windows Vista e posterior:</strong> Nome nativo curto do sexto dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-244"><strong>Windows Vista and later:</strong> Short native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54e01-245">CAL_SSHORTESTDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="54e01-245">CAL_SSHORTESTDAYNAME7</span></span></td>
<td><span data-ttu-id="54e01-246"><strong>Windows Vista e posterior:</strong> Nome nativo curto do sétimo dia da semana.</span><span class="sxs-lookup"><span data-stu-id="54e01-246"><strong>Windows Vista and later:</strong> Short native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54e01-247">CAL_SYEARMONTH</span><span class="sxs-lookup"><span data-stu-id="54e01-247">CAL_SYEARMONTH</span></span></td>
<td><span data-ttu-id="54e01-248"><strong>Windows me/98, windows 2000:</strong> Os formatos de ano/mês para os calendários especificados.</span><span class="sxs-lookup"><span data-stu-id="54e01-248"><strong>Windows Me/98, Windows 2000:</strong> The year/month formats for the specified calendars.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="54e01-249">Se o nome nativo do dia da semana ou de um mês for uma cadeia de caracteres vazia, esse nome será idêntico ao nome especificado nas informações de localidade correspondentes e, portanto, não será duplicado aqui.</span><span class="sxs-lookup"><span data-stu-id="54e01-249">If the native name for the day of the week or for a month is an empty string, that name is identical to the name specified in the corresponding locale information and therefore is not duplicated here.</span></span>

 

 

 




