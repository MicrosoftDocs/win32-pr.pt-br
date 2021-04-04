---
description: SGROUPING de localidade \_
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922988"
---
# <a name="locale_sgrouping"></a><span data-ttu-id="27de1-103">SGROUPING de localidade \_</span><span class="sxs-lookup"><span data-stu-id="27de1-103">LOCALE\_SGROUPING</span></span>

<span data-ttu-id="27de1-104">Tamanhos de cada grupo de dígitos à esquerda do decimal.</span><span class="sxs-lookup"><span data-stu-id="27de1-104">Sizes for each group of digits to the left of the decimal.</span></span> <span data-ttu-id="27de1-105">O número máximo de caracteres permitido para essa cadeia de caracteres é dez, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="27de1-105">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="27de1-106">Um tamanho explícito é necessário para cada grupo, e os tamanhos são separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="27de1-106">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="27de1-107">Se o último valor for 0, o valor anterior será repetido.</span><span class="sxs-lookup"><span data-stu-id="27de1-107">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="27de1-108">Por exemplo, para agrupar milhares, especifique 3; 0.</span><span class="sxs-lookup"><span data-stu-id="27de1-108">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="27de1-109">As localidades em Índico agrupam os primeiros mil e depois agrupam por centenas.</span><span class="sxs-lookup"><span data-stu-id="27de1-109">Indic locales group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="27de1-110">Por exemplo, 12, 34, 56789 é representado por 3; 2; 0.</span><span class="sxs-lookup"><span data-stu-id="27de1-110">For example, 12,34,56,789 is represented by 3;2;0.</span></span>

<span data-ttu-id="27de1-111">Exemplos adicionais:</span><span class="sxs-lookup"><span data-stu-id="27de1-111">Further examples:</span></span>



| <span data-ttu-id="27de1-112">Especificação</span><span class="sxs-lookup"><span data-stu-id="27de1-112">Specification</span></span> | <span data-ttu-id="27de1-113">Cadeia de caracteres resultante</span><span class="sxs-lookup"><span data-stu-id="27de1-113">Resulting string</span></span>   |
|---------------|--------------------|
| <span data-ttu-id="27de1-114">3; 0</span><span class="sxs-lookup"><span data-stu-id="27de1-114">3;0</span></span>           | <span data-ttu-id="27de1-115">3.000.000.000.000</span><span class="sxs-lookup"><span data-stu-id="27de1-115">3,000,000,000,000</span></span>  |
| <span data-ttu-id="27de1-116">3; 2; 0</span><span class="sxs-lookup"><span data-stu-id="27de1-116">3;2;0</span></span>         | <span data-ttu-id="27de1-117">30, 00, 00, 00, 00000</span><span class="sxs-lookup"><span data-stu-id="27de1-117">30,00,00,00,00,000</span></span> |
| <span data-ttu-id="27de1-118">3</span><span class="sxs-lookup"><span data-stu-id="27de1-118">3</span></span>             | <span data-ttu-id="27de1-119">3.000.000.000.000</span><span class="sxs-lookup"><span data-stu-id="27de1-119">3000000000,000</span></span>     |
| <span data-ttu-id="27de1-120">3; 2</span><span class="sxs-lookup"><span data-stu-id="27de1-120">3;2</span></span>           | <span data-ttu-id="27de1-121">30000000, 00000</span><span class="sxs-lookup"><span data-stu-id="27de1-121">30000000,00,000</span></span>    |



 

 

 



