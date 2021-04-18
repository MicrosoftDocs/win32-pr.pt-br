---
description: '\_Constantes SMON de localidade \*'
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: Constantes LOCALE_SMON *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756751"
---
# <a name="locale_smon-constants"></a><span data-ttu-id="e17ba-103">\_Constantes SMON de localidade \*</span><span class="sxs-lookup"><span data-stu-id="e17ba-103">LOCALE\_SMON\* Constants</span></span>

<span data-ttu-id="e17ba-104">Este tópico define as constantes de SMON de localidade \_ \* usadas pelo NLS na representação de valores monetários.</span><span class="sxs-lookup"><span data-stu-id="e17ba-104">This topic defines the LOCALE\_SMON\* constants used by NLS in representing monetary values.</span></span>



| <span data-ttu-id="e17ba-105">Valor</span><span class="sxs-lookup"><span data-stu-id="e17ba-105">Value</span></span>                   | <span data-ttu-id="e17ba-106">Significado</span><span class="sxs-lookup"><span data-stu-id="e17ba-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e17ba-107">SMONDECIMALSEP de localidade \_</span><span class="sxs-lookup"><span data-stu-id="e17ba-107">LOCALE\_SMONDECIMALSEP</span></span>  | <span data-ttu-id="e17ba-108">Caracteres usados como separador decimal monetário.</span><span class="sxs-lookup"><span data-stu-id="e17ba-108">Character(s) used as the monetary decimal separator.</span></span> <span data-ttu-id="e17ba-109">O número máximo de caracteres permitido para essa cadeia de caracteres é quatro, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="e17ba-109">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="e17ba-110">Por exemplo, se um valor monetário for exibido como "$3.40", assim como "três dólares e 40 centavos" for exibido na Estados Unidos, o separador decimal monetário será ".".</span><span class="sxs-lookup"><span data-stu-id="e17ba-110">For example, if a monetary amount is displayed as "$3.40", just as "three dollars and forty cents" is displayed in the United States, then the monetary decimal separator is ".".</span></span>                                                                                                                                             |
| <span data-ttu-id="e17ba-111">SMONGROUPING de localidade \_</span><span class="sxs-lookup"><span data-stu-id="e17ba-111">LOCALE\_SMONGROUPING</span></span>    | <span data-ttu-id="e17ba-112">Tamanhos de cada grupo de dígitos Monetários à esquerda do decimal.</span><span class="sxs-lookup"><span data-stu-id="e17ba-112">Sizes for each group of monetary digits to the left of the decimal.</span></span> <span data-ttu-id="e17ba-113">O número máximo de caracteres permitido para essa cadeia de caracteres é dez, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="e17ba-113">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="e17ba-114">Um tamanho explícito é necessário para cada grupo, e os tamanhos são separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="e17ba-114">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="e17ba-115">Se o último valor for 0, o valor anterior será repetido.</span><span class="sxs-lookup"><span data-stu-id="e17ba-115">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="e17ba-116">Por exemplo, para agrupar milhares, especifique 3; 0.</span><span class="sxs-lookup"><span data-stu-id="e17ba-116">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="e17ba-117">Os idiomas índicos agrupam os primeiros mil e depois agrupam por centenas.</span><span class="sxs-lookup"><span data-stu-id="e17ba-117">Indic languages group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="e17ba-118">Por exemplo, 12, 34, 56789 é representado por 3; 2; 0.</span><span class="sxs-lookup"><span data-stu-id="e17ba-118">For example 12,34,56,789 is represented by 3;2;0.</span></span> |
| <span data-ttu-id="e17ba-119">SMONTHOUSANDSEP de localidade \_</span><span class="sxs-lookup"><span data-stu-id="e17ba-119">LOCALE\_SMONTHOUSANDSEP</span></span> | <span data-ttu-id="e17ba-120">Caracteres usados como separador monetário entre grupos de dígitos à esquerda do decimal.</span><span class="sxs-lookup"><span data-stu-id="e17ba-120">Character(s) used as the monetary separator between groups of digits to the left of the decimal.</span></span> <span data-ttu-id="e17ba-121">O número máximo de caracteres permitido para essa cadeia de caracteres é quatro, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="e17ba-121">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="e17ba-122">Normalmente, os grupos representam milhares.</span><span class="sxs-lookup"><span data-stu-id="e17ba-122">Typically, the groups represent thousands.</span></span> <span data-ttu-id="e17ba-123">No entanto, dependendo do valor especificado para SMONGROUPING de localidade \_ , eles podem representar outra coisa.</span><span class="sxs-lookup"><span data-stu-id="e17ba-123">However, depending on the value specified for LOCALE\_SMONGROUPING, they can represent something else.</span></span>                                                                                                                                 |



 

 

 



