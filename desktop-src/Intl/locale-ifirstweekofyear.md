---
description: IFIRSTWEEKOFYEAR de localidade \_
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 7f391fb167a9362fc8770bbcc5a495170148b489
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "105751464"
---
# <a name="locale_ifirstweekofyear"></a><span data-ttu-id="44921-103">IFIRSTWEEKOFYEAR de localidade \_</span><span class="sxs-lookup"><span data-stu-id="44921-103">LOCALE\_IFIRSTWEEKOFYEAR</span></span>

<span data-ttu-id="44921-104">A primeira semana do ano.</span><span class="sxs-lookup"><span data-stu-id="44921-104">The first week of the year.</span></span>



| <span data-ttu-id="44921-105">Valor</span><span class="sxs-lookup"><span data-stu-id="44921-105">Value</span></span> | <span data-ttu-id="44921-106">Significado</span><span class="sxs-lookup"><span data-stu-id="44921-106">Meaning</span></span>                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44921-107">0</span><span class="sxs-lookup"><span data-stu-id="44921-107">0</span></span>     | <span data-ttu-id="44921-108">A semana que contém 1/1 é a primeira semana do ano.</span><span class="sxs-lookup"><span data-stu-id="44921-108">Week containing 1/1 is the first week of the year.</span></span> <span data-ttu-id="44921-109">Observe que isso pode ser um único dia, se 1/1 estiver no último dia da semana.</span><span class="sxs-lookup"><span data-stu-id="44921-109">Note that this can be a single day, if 1/1 falls on the last day of the week.</span></span> |
| <span data-ttu-id="44921-110">1</span><span class="sxs-lookup"><span data-stu-id="44921-110">1</span></span>     | <span data-ttu-id="44921-111">A primeira semana completa após 1/1 é a primeira semana do ano.</span><span class="sxs-lookup"><span data-stu-id="44921-111">First full week following 1/1 is the first week of the year.</span></span>                                                                     |
| <span data-ttu-id="44921-112">2</span><span class="sxs-lookup"><span data-stu-id="44921-112">2</span></span>     | <span data-ttu-id="44921-113">A primeira semana que contém pelo menos quatro dias é a primeira semana do ano.</span><span class="sxs-lookup"><span data-stu-id="44921-113">First week containing at least four days is the first week of the year.</span></span> <span data-ttu-id="44921-114">ISO 8601 compatível.</span><span class="sxs-lookup"><span data-stu-id="44921-114">ISO 8601 compatible.</span></span>                                     |

<span data-ttu-id="44921-115">Se LOCALE_IFIRSTWEEKOFYEAR for 2, LOCALE_IFIRSTDAYOFWEEK for 0 (segunda-feira) e LOCALE_ICALENDARTYPE for Gregoriano, a primeira semana seguirá a definição de ISO 8601, na qual a primeira semana é a semana com a primeira quinta-feira do ano gregoriano.</span><span class="sxs-lookup"><span data-stu-id="44921-115">If LOCALE_IFIRSTWEEKOFYEAR is 2, LOCALE_IFIRSTDAYOFWEEK is 0 (Monday), and LOCALE_ICALENDARTYPE is Gregorian, then the first week follows the ISO 8601 definition where the first week is the week with the first Thursday of the Gregorian year in it.</span></span>


 

 

 



