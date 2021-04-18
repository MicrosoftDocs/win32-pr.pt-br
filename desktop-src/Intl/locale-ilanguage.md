---
description: ILANGUAGE de localidade \_
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b68ccd270319fa00cd2e983b5f9159d454f160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812927"
---
# <a name="locale_ilanguage"></a><span data-ttu-id="6d3c5-103">ILANGUAGE de localidade \_</span><span class="sxs-lookup"><span data-stu-id="6d3c5-103">LOCALE\_ILANGUAGE</span></span>

<span data-ttu-id="6d3c5-104">[Identificador de idioma](language-identifiers.md) com um valor hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="6d3c5-104">[Language identifier](language-identifiers.md) with a hexadecimal value.</span></span> <span data-ttu-id="6d3c5-105">Por exemplo, inglês (Estados Unidos) tem o valor 0409, que indica o hexadecimal 0x0409, e é equivalente a 1033 decimal.</span><span class="sxs-lookup"><span data-stu-id="6d3c5-105">For example, English (United States) has the value 0409, which indicates 0x0409 hexadecimal, and is equivalent to 1033 decimal.</span></span> <span data-ttu-id="6d3c5-106">O número máximo de caracteres permitido para essa cadeia de caracteres é cinco, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="6d3c5-106">The maximum number of characters allowed for this string is five, including a terminating null character.</span></span>

<span data-ttu-id="6d3c5-107">**Windows Vista e posterior:** O uso dessa constante pode fazer com que [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) retorne um identificador de localidade inválido.</span><span class="sxs-lookup"><span data-stu-id="6d3c5-107">**Windows Vista and later:** Use of this constant can cause [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) to return an invalid locale identifier.</span></span> <span data-ttu-id="6d3c5-108">Seu aplicativo deve usar a [constante \_ SNAME de localidade](locale-sname.md) ao chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="6d3c5-108">Your application should use the [LOCALE\_SNAME](locale-sname.md) constant when calling this function.</span></span>

 

 



