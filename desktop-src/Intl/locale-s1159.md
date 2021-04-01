---
description: LOCALIDADE \_ S1159 e Sam de localidade \_
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 e LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b41f98ea5c07f1d88534c1e47acecfa81a4e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829356"
---
# <a name="locale_s1159-and-locale_sam"></a><span data-ttu-id="c3c8b-103">LOCALIDADE \_ S1159 e Sam de localidade \_</span><span class="sxs-lookup"><span data-stu-id="c3c8b-103">LOCALE\_S1159 and LOCALE\_SAM</span></span>

<span data-ttu-id="c3c8b-104">Cadeia de caracteres do designador AM (primeiras 12 horas do dia).</span><span class="sxs-lookup"><span data-stu-id="c3c8b-104">String for the AM designator (first 12 hours of the day).</span></span> <span data-ttu-id="c3c8b-105">O número máximo de caracteres permitido para essa cadeia de caracteres, incluindo um caractere nulo de terminação, é diferente para diferentes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="c3c8b-105">The maximum number of characters allowed for this string, including a terminating null character, is different for different releases of Windows.</span></span>

<span data-ttu-id="c3c8b-106">**Windows XP:** Treze incluindo um caractere nulo de terminação para [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="c3c8b-106">**Windows XP:** Thirteen including a terminating null character for [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="c3c8b-107">Quinze incluindo um caractere nulo de terminação para [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="c3c8b-107">Fifteen including a terminating null character for [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span></span>

<span data-ttu-id="c3c8b-108">**Windows me/98/95, Windows NT 4,0, windows 2000:** Nove incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c3c8b-108">**Windows Me/98/95, Windows NT 4.0, Windows 2000:** Nine including a terminating null character.</span></span>

<span data-ttu-id="c3c8b-109">**Windows Server 2003 e posterior:** Quinze incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c3c8b-109">**Windows Server 2003 and later:** Fifteen including a terminating null character.</span></span>

<span data-ttu-id="c3c8b-110">O Windows 10 adicionou a **localidade \_** de valor Sam como um sinônimo mais legível para a **localidade \_ S1159**.</span><span class="sxs-lookup"><span data-stu-id="c3c8b-110">Windows 10 added the value **LOCALE\_SAM** as a more readable synonym for **LOCALE\_S1159**.</span></span>

 

 



