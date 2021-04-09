---
description: '\_Constantes de retorno de localidade \*'
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: Constantes LOCALE_RETURN *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171292"
---
# <a name="locale_return-constants"></a><span data-ttu-id="76431-103">\_Constantes de retorno de localidade \*</span><span class="sxs-lookup"><span data-stu-id="76431-103">LOCALE\_RETURN\* Constants</span></span>

<span data-ttu-id="76431-104">Este tópico define as constantes de retorno de localidade \_ \* usadas pelo NLS.</span><span class="sxs-lookup"><span data-stu-id="76431-104">This topic defines the LOCALE\_RETURN\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="76431-105">Valor</span><span class="sxs-lookup"><span data-stu-id="76431-105">Value</span></span></th>
<th><span data-ttu-id="76431-106">Significado</span><span class="sxs-lookup"><span data-stu-id="76431-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76431-107">LOCALE_RETURN_GENITIVE_NAMES</span><span class="sxs-lookup"><span data-stu-id="76431-107">LOCALE_RETURN_GENITIVE_NAMES</span></span></td>
<td><span data-ttu-id="76431-108"><strong>Windows 7 e posterior:</strong> Recupere os nomes de genitive de meses, que são os nomes usados quando os nomes de mês são combinados com outros itens.</span><span class="sxs-lookup"><span data-stu-id="76431-108"><strong>Windows 7 and later:</strong> Retrieve the genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="76431-109">Por exemplo, em ucraniano, o equivalente a janeiro é escrito &quot; Січень &quot; quando o mês é nomeado sozinho.</span><span class="sxs-lookup"><span data-stu-id="76431-109">For example, in Ukrainian the equivalent of January is written &quot;Січень&quot; when the month is named alone.</span></span> <span data-ttu-id="76431-110">No entanto, quando o nome do mês é usado em combinação, por exemplo, em uma data como 5 de janeiro de 2003, a forma genitive do nome é usada.</span><span class="sxs-lookup"><span data-stu-id="76431-110">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="76431-111">Para o exemplo ucraniano, o nome do mês genitive é exibido como &quot; 5 січня 2003 &quot; .</span><span class="sxs-lookup"><span data-stu-id="76431-111">For the Ukrainian example, the genitive month name is displayed as &quot;5 січня 2003&quot;.</span></span> <span data-ttu-id="76431-112">A lista de nomes de meses genitive começa com janeiro e é delimitada por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="76431-112">The list of genitive month names begins with January and is semicolon-delimited.</span></span> <span data-ttu-id="76431-113">Se não houver nenhum mês 13, use um ponto e vírgula em seu lugar no final da lista.</span><span class="sxs-lookup"><span data-stu-id="76431-113">If there is no 13th month, use a semicolon in its place at the end of the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="76431-114">Os nomes de meses genitive não existem em todos os idiomas.</span><span class="sxs-lookup"><span data-stu-id="76431-114">Genitive month names do not exist in all languages.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76431-115">LOCALE_RETURN_NUMBER</span><span class="sxs-lookup"><span data-stu-id="76431-115">LOCALE_RETURN_NUMBER</span></span></td>
<td><span data-ttu-id="76431-116"><strong>Windows me/98, Windows NT 4,0 e posterior:</strong> Recupere um número.</span><span class="sxs-lookup"><span data-stu-id="76431-116"><strong>Windows Me/98, Windows NT 4.0 and later:</strong> Retrieve a number.</span></span> <span data-ttu-id="76431-117">Essa constante faz com que <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> ou <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> recupere um valor como um número em vez de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="76431-117">This constant causes <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> to retrieve a value as a number instead of as a string.</span></span> <span data-ttu-id="76431-118">O buffer que recebe o valor deve ser pelo menos o comprimento de um valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="76431-118">The buffer that receives the value must be at least the length of a DWORD value.</span></span> <span data-ttu-id="76431-119">Essa constante pode ser combinada com qualquer outra constante com um nome que comece com &quot; LOCALE_I &quot; .</span><span class="sxs-lookup"><span data-stu-id="76431-119">This constant can be combined with any other constant having a name that begins with &quot;LOCALE_I&quot;.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




