---
description: Este tópico descreve os tipos de formato para cadeias de caracteres usadas para compor a imagem de formato para uma cadeia de tempo. Cada imagem de formato consiste em uma combinação de uma cadeia de caracteres de cada um dos tipos de formato.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Imagens de formato de hora, minuto e segundo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589c04fea0d6ce2f522436c30c39c873e3a7165e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011848"
---
# <a name="hour-minute-and-second-format-pictures"></a><span data-ttu-id="faded-104">Imagens de formato de hora, minuto e segundo</span><span class="sxs-lookup"><span data-stu-id="faded-104">Hour, Minute, and Second Format Pictures</span></span>

<span data-ttu-id="faded-105">Este tópico descreve os tipos de formato para cadeias de caracteres usadas para compor a imagem de formato para uma cadeia de tempo.</span><span class="sxs-lookup"><span data-stu-id="faded-105">This topic describes the format types for strings used to compose the format picture for a time string.</span></span> <span data-ttu-id="faded-106">Cada imagem de formato consiste em uma combinação de uma cadeia de caracteres de cada um dos tipos de formato.</span><span class="sxs-lookup"><span data-stu-id="faded-106">Each format picture consists of a combination of one string of each of the format types.</span></span>

> [!Note]  
> <span data-ttu-id="faded-107">Nos tipos de formato, as letras "m", "s" e "t" devem estar em minúsculas e a letra "h" deve ser minúscula para indicar o relógio de 12 horas ou maiúsculas ("H") para denotar o relógio de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="faded-107">In the format types, the letters "m", "s", and "t" must be lowercase, and the letter "h" must be lowercase to denote the 12-hour clock or uppercase ("H") to denote the 24-hour clock.</span></span>

<span data-ttu-id="faded-108">Aspas simples podem ser usadas para marcar caracteres que devem ser exibidos exatamente como especificado.</span><span class="sxs-lookup"><span data-stu-id="faded-108">Single quotation marks can be used to mark characters that should be displayed exactly as specified.</span></span> <span data-ttu-id="faded-109">Se o aplicativo precisar exibir uma aspa simples, ele deverá posicionar duas aspas simples em uma linha.</span><span class="sxs-lookup"><span data-stu-id="faded-109">If the application must display a single quotation mark, it should place two single quotation marks in a row.</span></span> <span data-ttu-id="faded-110">Por exemplo, ' abc ' ' bar ', é exibido como "abc'bar".</span><span class="sxs-lookup"><span data-stu-id="faded-110">For example, 'abc''bar', is displayed as "abc'bar".</span></span>

<span data-ttu-id="faded-111">A tabela a seguir define os tipos de formato usados para representar horas.</span><span class="sxs-lookup"><span data-stu-id="faded-111">The following table defines the format types used to represent hours.</span></span>

| <span data-ttu-id="faded-112">String</span><span class="sxs-lookup"><span data-stu-id="faded-112">String</span></span> | <span data-ttu-id="faded-113">Significado</span><span class="sxs-lookup"><span data-stu-id="faded-113">Meaning</span></span>                                                             |
|--------|---------------------------------------------------------------------|
| <span data-ttu-id="faded-114">h</span><span class="sxs-lookup"><span data-stu-id="faded-114">h</span></span>      | <span data-ttu-id="faded-115">Horas sem zeros à esquerda para horas de dígito único (relógio de 12 horas).</span><span class="sxs-lookup"><span data-stu-id="faded-115">Hours without leading zeros for single-digit hours (12-hour clock).</span></span> |
| <span data-ttu-id="faded-116">hh</span><span class="sxs-lookup"><span data-stu-id="faded-116">hh</span></span>     | <span data-ttu-id="faded-117">Horas com zeros à esquerda para horas de dígito único (relógio de 12 horas).</span><span class="sxs-lookup"><span data-stu-id="faded-117">Hours with leading zeros for single-digit hours (12-hour clock).</span></span>    |
| <span data-ttu-id="faded-118">H</span><span class="sxs-lookup"><span data-stu-id="faded-118">H</span></span>      | <span data-ttu-id="faded-119">Horas sem zeros à esquerda para horas de dígito único (relógio de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="faded-119">Hours without leading zeros for single-digit hours (24-hour clock).</span></span> |
| <span data-ttu-id="faded-120">HH</span><span class="sxs-lookup"><span data-stu-id="faded-120">HH</span></span>     | <span data-ttu-id="faded-121">Horas com zeros à esquerda para horas de dígito único (relógio de 24 horas).</span><span class="sxs-lookup"><span data-stu-id="faded-121">Hours with leading zeros for single-digit hours (24-hour clock).</span></span>    |

<span data-ttu-id="faded-122">A tabela a seguir define os tipos de formato usados para representar minutos.</span><span class="sxs-lookup"><span data-stu-id="faded-122">The following table defines the format types used to represent minutes.</span></span>

| <span data-ttu-id="faded-123">String</span><span class="sxs-lookup"><span data-stu-id="faded-123">String</span></span> | <span data-ttu-id="faded-124">Significado</span><span class="sxs-lookup"><span data-stu-id="faded-124">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="faded-125">m</span><span class="sxs-lookup"><span data-stu-id="faded-125">m</span></span>      | <span data-ttu-id="faded-126">Minutos sem zeros à esquerda para minutos de dígito único.</span><span class="sxs-lookup"><span data-stu-id="faded-126">Minutes without leading zeros for single-digit minutes.</span></span> |
| <span data-ttu-id="faded-127">MM</span><span class="sxs-lookup"><span data-stu-id="faded-127">mm</span></span>     | <span data-ttu-id="faded-128">Minutos com zeros à esquerda para minutos de dígito único.</span><span class="sxs-lookup"><span data-stu-id="faded-128">Minutes with leading zeros for single-digit minutes.</span></span>    |

<span data-ttu-id="faded-129">A tabela a seguir define os tipos de formato usados para representar segundos.</span><span class="sxs-lookup"><span data-stu-id="faded-129">The following table defines the format types used to represent seconds.</span></span>

| <span data-ttu-id="faded-130">String</span><span class="sxs-lookup"><span data-stu-id="faded-130">String</span></span> | <span data-ttu-id="faded-131">Significado</span><span class="sxs-lookup"><span data-stu-id="faded-131">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="faded-132">s</span><span class="sxs-lookup"><span data-stu-id="faded-132">s</span></span>      | <span data-ttu-id="faded-133">Segundos sem zeros à esquerda para segundos de dígito único.</span><span class="sxs-lookup"><span data-stu-id="faded-133">Seconds without leading zeros for single-digit seconds.</span></span> |
| <span data-ttu-id="faded-134">ss</span><span class="sxs-lookup"><span data-stu-id="faded-134">ss</span></span>     | <span data-ttu-id="faded-135">Segundos com zeros à esquerda para segundos de dígito único.</span><span class="sxs-lookup"><span data-stu-id="faded-135">Seconds with leading zeros for single-digit seconds.</span></span>    |

<span data-ttu-id="faded-136">A tabela a seguir define os tipos de formato usados para representar um marcador de tempo.</span><span class="sxs-lookup"><span data-stu-id="faded-136">The following table defines the format types used to represent a time marker.</span></span>

| <span data-ttu-id="faded-137">String</span><span class="sxs-lookup"><span data-stu-id="faded-137">String</span></span> | <span data-ttu-id="faded-138">Significado</span><span class="sxs-lookup"><span data-stu-id="faded-138">Meaning</span></span>|
| ---    | ---    |
| <span data-ttu-id="faded-139">t</span><span class="sxs-lookup"><span data-stu-id="faded-139">t</span></span>      | <span data-ttu-id="faded-140">Cadeia de caracteres do marcador de tempo de um caractere.</span><span class="sxs-lookup"><span data-stu-id="faded-140">One-character time marker string.</span></span><br /><span data-ttu-id="faded-141">**Observação:** Esse formato não é recomendado para uso com determinados idiomas, como japonês (Japão).</span><span class="sxs-lookup"><span data-stu-id="faded-141">**Note:** This format is not recommended for use with certain languages, such as Japanese (Japan).</span></span> <span data-ttu-id="faded-142">Com esse formato, um aplicativo sempre usa o primeiro caractere da cadeia de caracteres do marcador de tempo, definido por [LOCALE_S1159](locale-s1159.md) (AM) e [LOCALE_S2359](locale-s2359.md) (PM).</span><span class="sxs-lookup"><span data-stu-id="faded-142">With this format, an application always takes the first character from the time marker string, defined by [LOCALE_S1159](locale-s1159.md) (AM) and [LOCALE_S2359](locale-s2359.md) (PM).</span></span> <span data-ttu-id="faded-143">Por isso, o aplicativo pode criar formatação incorreta com a mesma cadeia de caracteres usada para AM e PM.</span><span class="sxs-lookup"><span data-stu-id="faded-143">Because of this, the application can create incorrect formatting with the same string used for both AM and PM.</span></span>|
| <span data-ttu-id="faded-144">tt</span><span class="sxs-lookup"><span data-stu-id="faded-144">tt</span></span>     | <span data-ttu-id="faded-145">Cadeia de caracteres do marcador de tempo de vários caracteres.</span><span class="sxs-lookup"><span data-stu-id="faded-145">Multi-character time marker string.</span></span> |
