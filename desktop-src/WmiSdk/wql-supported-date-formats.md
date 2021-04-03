---
description: Descreve os formatos de data com suporte para uso na cláusula WHERE do WQL.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: Formatos de data WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828656"
---
# <a name="wql-supported-date-formats"></a><span data-ttu-id="ff557-103">Formatos de data WQL-Supported</span><span class="sxs-lookup"><span data-stu-id="ff557-103">WQL-Supported Date Formats</span></span>

<span data-ttu-id="ff557-104">Além do formato de data e **hora** do WMI, os seguintes formatos de datas têm suporte para uso na cláusula **Where** do WQL.</span><span class="sxs-lookup"><span data-stu-id="ff557-104">In addition to the WMI **DATETIME** format, the following date formats are supported for use in the WQL **WHERE** clause.</span></span>

<span data-ttu-id="ff557-105">O formato de hora exibido é diferente para localidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="ff557-105">The displayed time format is different for different locales.</span></span> <span data-ttu-id="ff557-106">Os scripts que se conectam a computadores remotos devem especificar a hora no formato apropriado para a localidade do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="ff557-106">Scripts that connect to remote computers must specify time in the format appropriate for the locale of the target computer.</span></span>

<span data-ttu-id="ff557-107">Por exemplo, o Estados Unidos formato de data e hora é MM-DD-AAAA.</span><span class="sxs-lookup"><span data-stu-id="ff557-107">For example, the United States date and time format is MM-DD-YYYY.</span></span> <span data-ttu-id="ff557-108">Se um script em um computador dos EUA se conecta a um computador de destino em uma localidade onde o formato é DD-MM-AAAA, as consultas são processadas no computador de destino como DD-MM-AAAA.</span><span class="sxs-lookup"><span data-stu-id="ff557-108">If a script on a US computer connects to a target computer in a locale where the format is DD-MM-YYYY, then queries are processed on the target computer as DD-MM-YYYY.</span></span> <span data-ttu-id="ff557-109">Para evitar resultados diferentes entre as localidades, use o formato [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="ff557-109">To avoid different results between locales, use the [**DATETIME**](datetime.md) format.</span></span> <span data-ttu-id="ff557-110">Para obter mais informações, consulte [formato de data e hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="ff557-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ff557-111">Formatar</span><span class="sxs-lookup"><span data-stu-id="ff557-111">Format</span></span></th>
<th><span data-ttu-id="ff557-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff557-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff557-113">Mon [th] dd [,] [AA] AA</span><span class="sxs-lookup"><span data-stu-id="ff557-113">Mon[th] dd[,] [yy]yy</span></span></td>
<td><span data-ttu-id="ff557-114">Mês (escrito ou abreviado em três letras), dia, vírgula opcional e dois ou ano de quatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="ff557-114">Month (either spelled-out or abbreviated in three letters), day, optional comma, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="ff557-115">21 de janeiro de 1932</span><span class="sxs-lookup"><span data-stu-id="ff557-115">January 21, 1932</span></span><br />
<span data-ttu-id="ff557-116">21 de janeiro de 32</span><span class="sxs-lookup"><span data-stu-id="ff557-116">January 21, 32</span></span><br />
<span data-ttu-id="ff557-117">Jan 21 1932</span><span class="sxs-lookup"><span data-stu-id="ff557-117">Jan 21 1932</span></span><br />
<span data-ttu-id="ff557-118">Jan 21 32</span><span class="sxs-lookup"><span data-stu-id="ff557-118">Jan 21 32</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff557-119">Mon [th] [,] aaaa</span><span class="sxs-lookup"><span data-stu-id="ff557-119">Mon[th][,] yyyy</span></span></td>
<td><span data-ttu-id="ff557-120">Mês (escrito ou abreviado em três letras), vírgula opcional e ano de quatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="ff557-120">Month (either spelled-out or abbreviated in three letters), optional comma, and four-digit year.</span></span><br/> <dl> <span data-ttu-id="ff557-121">Janeiro de 1932</span><span class="sxs-lookup"><span data-stu-id="ff557-121">January 1932</span></span><br />
<span data-ttu-id="ff557-122">Jan 1932</span><span class="sxs-lookup"><span data-stu-id="ff557-122">Jan 1932</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff557-123">Mon [th] [AA] aa dd</span><span class="sxs-lookup"><span data-stu-id="ff557-123">Mon[th] [yy]yy dd</span></span></td>
<td><span data-ttu-id="ff557-124">Mês (escrito ou abreviado em três letras), dois ou quatro dígitos de ano e dia.</span><span class="sxs-lookup"><span data-stu-id="ff557-124">Month (either spelled-out or abbreviated in three letters), two or four digit year, and day.</span></span><br/> <dl> <span data-ttu-id="ff557-125">Janeiro de 1932 21</span><span class="sxs-lookup"><span data-stu-id="ff557-125">January 1932 21</span></span><br />
<span data-ttu-id="ff557-126">Jan 32 21</span><span class="sxs-lookup"><span data-stu-id="ff557-126">Jan 32 21</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff557-127">DD MON [th] [,] [] [AA] AA</span><span class="sxs-lookup"><span data-stu-id="ff557-127">dd Mon[th][,][ ][yy]yy</span></span></td>
<td><span data-ttu-id="ff557-128">Dia do mês, mês (escrito ou abreviado em três letras), vírgula opcional, espaço opcional e dois ou ano de quatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="ff557-128">Day of the month, month (either spelled-out or abbreviated in three letters), optional comma, optional space, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="ff557-129">21 de janeiro de 1932</span><span class="sxs-lookup"><span data-stu-id="ff557-129">21 January, 1932</span></span><br />
<span data-ttu-id="ff557-130">21 Jan32</span><span class="sxs-lookup"><span data-stu-id="ff557-130">21 Jan32</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff557-131">DD [AA] AA Mon [th]</span><span class="sxs-lookup"><span data-stu-id="ff557-131">dd [yy]yy Mon[th]</span></span></td>
<td><span data-ttu-id="ff557-132">Dia do mês, dois ou quatro dígitos de ano e mês (a grafia ou abreviada em três letras).</span><span class="sxs-lookup"><span data-stu-id="ff557-132">Day of the month, two or four-digit year, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="ff557-133">21 1932 de janeiro</span><span class="sxs-lookup"><span data-stu-id="ff557-133">21 1932 January</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff557-134">[AA] AA Mon [th] dd</span><span class="sxs-lookup"><span data-stu-id="ff557-134">[yy]yy Mon[th] dd</span></span></td>
<td><span data-ttu-id="ff557-135">Ano de dois ou quatro dígitos, mês (escrito ou abreviado em três letras) e dia.</span><span class="sxs-lookup"><span data-stu-id="ff557-135">Two or four-digit year, month (either spelled-out or abbreviated in three letters), and day.</span></span><br/> <dl> <span data-ttu-id="ff557-136">21 a 1932 de janeiro</span><span class="sxs-lookup"><span data-stu-id="ff557-136">1932 January 21</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff557-137">aaaa Mon [th]</span><span class="sxs-lookup"><span data-stu-id="ff557-137">yyyy Mon[th]</span></span></td>
<td><span data-ttu-id="ff557-138">Ano e mês de dois ou quatro dígitos (ou seja, escrito ou abreviado em três letras).</span><span class="sxs-lookup"><span data-stu-id="ff557-138">Two or four-digit year and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="ff557-139">1932 de janeiro</span><span class="sxs-lookup"><span data-stu-id="ff557-139">1932 Jan</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff557-140">aaaa DD MON [th]</span><span class="sxs-lookup"><span data-stu-id="ff557-140">yyyy dd Mon[th]</span></span></td>
<td><span data-ttu-id="ff557-141">Ano, dia e mês de dois ou quatro dígitos (por escrito ou abreviado em três letras).</span><span class="sxs-lookup"><span data-stu-id="ff557-141">Two or four-digit year, day, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="ff557-142">1932 21 de janeiro</span><span class="sxs-lookup"><span data-stu-id="ff557-142">1932 21 January</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff557-143">D M {/-.} DD {/-.} [AA] AA</span><span class="sxs-lookup"><span data-stu-id="ff557-143">[M]M{/-.}dd{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="ff557-144">Mês, dia e dois ou um ano de quatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="ff557-144">Month, day, and two or four-digit year.</span></span> <span data-ttu-id="ff557-145">Observe que os separadores devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="ff557-145">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff557-146">DD {/-.} D M {/-.} [AA] AA</span><span class="sxs-lookup"><span data-stu-id="ff557-146">dd{/-.}[M]M{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="ff557-147">Dia do mês, mês e dois ou ano de quatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="ff557-147">Day of the month, month, and two or four-digit year.</span></span> <span data-ttu-id="ff557-148">Observe que os separadores devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="ff557-148">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff557-149">D M {/-.} [AA] AA {/-.} yyyy</span><span class="sxs-lookup"><span data-stu-id="ff557-149">[M]M{/-.}[yy]yy{/-.}dd</span></span></td>
<td><span data-ttu-id="ff557-150">Mês, dois ou quatro dígitos de ano e dia.</span><span class="sxs-lookup"><span data-stu-id="ff557-150">Month, two or four-digit year, and day.</span></span> <span data-ttu-id="ff557-151">Observe que os separadores devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="ff557-151">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff557-152">DD {/-.} [AA] AA {/-.} D D</span><span class="sxs-lookup"><span data-stu-id="ff557-152">dd{/-.}[yy]yy{/-.}[M]M</span></span></td>
<td><span data-ttu-id="ff557-153">Dia do mês, dois ou quatro dígitos de ano e mês.</span><span class="sxs-lookup"><span data-stu-id="ff557-153">Day of the month, two or four-digit year, and month.</span></span> <span data-ttu-id="ff557-154">Observe que os separadores devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="ff557-154">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff557-155">[AA] AA {/-.} DD {/-.} D D</span><span class="sxs-lookup"><span data-stu-id="ff557-155">[yy]yy{/-.}dd{/-.}[M]M</span></span></td>
<td><span data-ttu-id="ff557-156">Ano, dia e mês de dois ou quatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="ff557-156">Two or four digit year, day, and month.</span></span> <span data-ttu-id="ff557-157">Observe que os separadores devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="ff557-157">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff557-158">[AA] AA {/-.} D M {/-.} yyyy</span><span class="sxs-lookup"><span data-stu-id="ff557-158">[yy]yy{/-.}[M]M{/-.}dd</span></span></td>
<td><span data-ttu-id="ff557-159">Ano, mês e dia de dois ou quatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="ff557-159">Two or four digit year, month, and day.</span></span> <span data-ttu-id="ff557-160">Observe que os separadores devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="ff557-160">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff557-161">[AA] yyMMdd</span><span class="sxs-lookup"><span data-stu-id="ff557-161">[yy]yyMMdd</span></span></td>
<td><span data-ttu-id="ff557-162">Ano, mês e dia de dois ou quatro dígitos, sem espaços.</span><span class="sxs-lookup"><span data-stu-id="ff557-162">Two or four digit year, month, and day, without spaces.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff557-163">aaaa [MM [DD]]</span><span class="sxs-lookup"><span data-stu-id="ff557-163">yyyy[MM[dd]]</span></span></td>
<td><span data-ttu-id="ff557-164">Ano de dois ou quatro dígitos, mês opcional e dia opcional, sem espaços.</span><span class="sxs-lookup"><span data-stu-id="ff557-164">Two or four digit year, optional month, and optional day, without spaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ff557-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff557-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff557-166">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="ff557-166">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




