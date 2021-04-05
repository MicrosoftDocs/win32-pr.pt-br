---
description: '\_Constantes SMONTHNAME de localidade \*'
ms.assetid: 81269282-bea8-4a5d-929d-c68af34bd1ac
title: Constantes LOCALE_SMONTHNAME *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4b45a84ea31d7d8c3d5de6e2f3f3a452c7a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647475"
---
# <a name="locale_smonthname-constants"></a><span data-ttu-id="fc858-103">\_Constantes SMONTHNAME de localidade \*</span><span class="sxs-lookup"><span data-stu-id="fc858-103">LOCALE\_SMONTHNAME\* Constants</span></span>

<span data-ttu-id="fc858-104">Este tópico define as constantes de SMONTHNAME de localidade \_ \* usadas pelo NLS.</span><span class="sxs-lookup"><span data-stu-id="fc858-104">This topic defines the LOCALE\_SMONTHNAME\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc858-105">Valor</span><span class="sxs-lookup"><span data-stu-id="fc858-105">Value</span></span></th>
<th><span data-ttu-id="fc858-106">Significado</span><span class="sxs-lookup"><span data-stu-id="fc858-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc858-107">LOCALE_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="fc858-107">LOCALE_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="fc858-108">Nome longo nativo de Janeiro.</span><span class="sxs-lookup"><span data-stu-id="fc858-108">Native long name for January.</span></span> <span data-ttu-id="fc858-109">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-109">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fc858-110">Chamar a função <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> ou <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> com uma constante LOCALE_SMONTHNAME \* retorna a forma autônoma ou nomeada do nome do mês.</span><span class="sxs-lookup"><span data-stu-id="fc858-110">Calling the <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> function with a LOCALE_SMONTHNAME\* constant returns the standalone, or nominative, form of the month name.</span></span> <span data-ttu-id="fc858-111">Para obter a forma genitive do nome do mês, o aplicativo chama <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> ou <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> com uma imagem de data de ddMMMM e remove os dois dígitos do início da cadeia de caracteres recuperada.</span><span class="sxs-lookup"><span data-stu-id="fc858-111">To get the genitive form of the month name, the application calls <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> or <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> with a date picture of ddMMMM and removes the two digits from the beginning of the retrieved string.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc858-112">LOCALE_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="fc858-112">LOCALE_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="fc858-113">Nome longo nativo de fevereiro.</span><span class="sxs-lookup"><span data-stu-id="fc858-113">Native long name for February.</span></span> <span data-ttu-id="fc858-114">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-114">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-115">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-115">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc858-116">LOCALE_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="fc858-116">LOCALE_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="fc858-117">Nome longo nativo de março.</span><span class="sxs-lookup"><span data-stu-id="fc858-117">Native long name for March.</span></span> <span data-ttu-id="fc858-118">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-118">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-119">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-119">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc858-120">LOCALE_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="fc858-120">LOCALE_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="fc858-121">Nome longo nativo para abril.</span><span class="sxs-lookup"><span data-stu-id="fc858-121">Native long name for April.</span></span> <span data-ttu-id="fc858-122">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-122">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-123">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-123">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc858-124">LOCALE_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="fc858-124">LOCALE_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="fc858-125">Nome longo nativo para maio.</span><span class="sxs-lookup"><span data-stu-id="fc858-125">Native long name for May.</span></span> <span data-ttu-id="fc858-126">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-126">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-127">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-127">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc858-128">LOCALE_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="fc858-128">LOCALE_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="fc858-129">Nome longo nativo para junho.</span><span class="sxs-lookup"><span data-stu-id="fc858-129">Native long name for June.</span></span> <span data-ttu-id="fc858-130">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-130">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-131">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-131">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc858-132">LOCALE_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="fc858-132">LOCALE_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="fc858-133">Nome longo nativo para julho.</span><span class="sxs-lookup"><span data-stu-id="fc858-133">Native long name for July.</span></span> <span data-ttu-id="fc858-134">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-134">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-135">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-135">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc858-136">LOCALE_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="fc858-136">LOCALE_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="fc858-137">Nome longo nativo de agosto.</span><span class="sxs-lookup"><span data-stu-id="fc858-137">Native long name for August.</span></span> <span data-ttu-id="fc858-138">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-138">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-139">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-139">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc858-140">LOCALE_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="fc858-140">LOCALE_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="fc858-141">Nome longo nativo para setembro.</span><span class="sxs-lookup"><span data-stu-id="fc858-141">Native long name for September.</span></span> <span data-ttu-id="fc858-142">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-142">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-143">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-143">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc858-144">LOCALE_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="fc858-144">LOCALE_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="fc858-145">Nome longo nativo para outubro.</span><span class="sxs-lookup"><span data-stu-id="fc858-145">Native long name for October.</span></span> <span data-ttu-id="fc858-146">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-146">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-147">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-147">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc858-148">LOCALE_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="fc858-148">LOCALE_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="fc858-149">Nome longo nativo para novembro.</span><span class="sxs-lookup"><span data-stu-id="fc858-149">Native long name for November.</span></span> <span data-ttu-id="fc858-150">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-150">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-151">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-151">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc858-152">LOCALE_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="fc858-152">LOCALE_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="fc858-153">Nome longo nativo de dezembro.</span><span class="sxs-lookup"><span data-stu-id="fc858-153">Native long name for December.</span></span> <span data-ttu-id="fc858-154">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-154">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-155">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-155">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc858-156">LOCALE_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="fc858-156">LOCALE_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="fc858-157">Nome nativo de um mês 13, se existir.</span><span class="sxs-lookup"><span data-stu-id="fc858-157">Native name for a 13th month, if it exists.</span></span> <span data-ttu-id="fc858-158">O número máximo de caracteres permitido para essa cadeia de caracteres é 80, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc858-158">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="fc858-159">Consulte a observação para LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="fc858-159">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




