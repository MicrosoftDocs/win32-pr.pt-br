---
description: SSCRIPTS de localidade \_
ms.assetid: d15c501a-b77b-4446-bee6-6dbbd714b4e0
title: LOCALE_SSCRIPTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb79f78626e7afb54229d8e0619e26d94250f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770390"
---
# <a name="locale_sscripts"></a><span data-ttu-id="0b76f-103">SSCRIPTS de localidade \_</span><span class="sxs-lookup"><span data-stu-id="0b76f-103">LOCALE\_SSCRIPTS</span></span>

<span data-ttu-id="0b76f-104">**Windows Vista e posterior:** Uma cadeia de caracteres que representa uma lista de scripts, usando a notação de 4 caracteres usada no [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="0b76f-104">**Windows Vista and later:** A string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="0b76f-105">Cada nome de script consiste em quatro caracteres latinos e a lista é organizada em ordem alfabética com cada nome, incluindo o último, seguido por um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="0b76f-105">Each script name consists of four Latin characters and the list is arranged in alphabetical order with each name, including the last, followed by a semicolon.</span></span>

<span data-ttu-id="0b76f-106">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) podem ser chamados com *LCTYPE* definido como localidade \_ SSCRIPTS como parte de uma estratégia para atenuar problemas de segurança relacionados a IDNs (nomes de domínio internacionalizados).</span><span class="sxs-lookup"><span data-stu-id="0b76f-106">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) can be called with *LCType* set to LOCALE\_SSCRIPTS as part of a strategy to mitigate security issues related to Internationalized Domain Names (IDNs).</span></span> <span data-ttu-id="0b76f-107">Aqui estão alguns exemplos de valores:</span><span class="sxs-lookup"><span data-stu-id="0b76f-107">Here are some example values:</span></span>



| <span data-ttu-id="0b76f-108">Locale</span><span class="sxs-lookup"><span data-stu-id="0b76f-108">Locale</span></span>                  | <span data-ttu-id="0b76f-109">Nome da localidade/idioma</span><span class="sxs-lookup"><span data-stu-id="0b76f-109">Locale/language name</span></span> | <span data-ttu-id="0b76f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="0b76f-110">Value</span></span>                                                                                                  |
|-------------------------|----------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b76f-111">Inglês (Estados Unidos)</span><span class="sxs-lookup"><span data-stu-id="0b76f-111">English (United States)</span></span> | <span data-ttu-id="0b76f-112">pt-BR</span><span class="sxs-lookup"><span data-stu-id="0b76f-112">en-US</span></span>                | <span data-ttu-id="0b76f-113">Latn</span><span class="sxs-lookup"><span data-stu-id="0b76f-113">Latn;</span></span>                                                                                                  |
| <span data-ttu-id="0b76f-114">Híndi (Índia)</span><span class="sxs-lookup"><span data-stu-id="0b76f-114">Hindi (India)</span></span>           | <span data-ttu-id="0b76f-115">hi-IN</span><span class="sxs-lookup"><span data-stu-id="0b76f-115">hi-IN</span></span>                | <span data-ttu-id="0b76f-116">DESVPADPA</span><span class="sxs-lookup"><span data-stu-id="0b76f-116">Deva;</span></span>                                                                                                  |
| <span data-ttu-id="0b76f-117">Japonês (Japão)</span><span class="sxs-lookup"><span data-stu-id="0b76f-117">Japanese (Japan)</span></span>        | <span data-ttu-id="0b76f-118">ja-JP</span><span class="sxs-lookup"><span data-stu-id="0b76f-118">ja-JP</span></span>                | <span data-ttu-id="0b76f-119">**Windows 7 e posterior:** Hani; Hira; Jpan; Kana</span><span class="sxs-lookup"><span data-stu-id="0b76f-119">**Windows 7 and later:** Hani;Hira;Jpan;Kana;</span></span><br/> <span data-ttu-id="0b76f-120">**Windows Vista:** Hani; Hira; Kana</span><span class="sxs-lookup"><span data-stu-id="0b76f-120">**Windows Vista:** Hani;Hira;Kana;</span></span><br/> |



 

<span data-ttu-id="0b76f-121">Um valor de script composto não inclui o script latino, a menos que seja uma parte essencial do sistema de escrita usado para a localidade específica.</span><span class="sxs-lookup"><span data-stu-id="0b76f-121">A compound script value does not include the Latin script unless it is an essential part of the writing system used for the particular locale.</span></span> <span data-ttu-id="0b76f-122">Os caracteres latinos são geralmente usados no contexto de localidades para os quais não são nativos, por exemplo, para um nome comercial estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="0b76f-122">Latin characters are often used in the context of locales for which they are not native, for example, for a foreign business name.</span></span> <span data-ttu-id="0b76f-123">No exemplo acima para Hindi na Índia, o único valor de script é "DESVPADA" (para "Devanágari"), embora os caracteres latinos também possam aparecer em texto em Híndi.</span><span class="sxs-lookup"><span data-stu-id="0b76f-123">In the example above for Hindi in India, the only script value is "Deva" (for "Devanagari"), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="0b76f-124">A função [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) tem um sinalizador especial para resolver esse caso.</span><span class="sxs-lookup"><span data-stu-id="0b76f-124">The [VerifyScripts](/windows/desktop/api/Winnls/nf-winnls-verifyscripts) function has a special flag to address this case.</span></span>

 

 




