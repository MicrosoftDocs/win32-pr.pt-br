---
description: Os arquivos de fonte TrueType incluem números de PANOse, que os aplicativos podem usar para escolher uma fonte que corresponda de acordo com suas especificações.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Usando números de PANOse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfa6a185e2afb05aec5fdf0e200300c7cf686a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171196"
---
# <a name="using-panose-numbers"></a><span data-ttu-id="612d3-103">Usando números de PANOse</span><span class="sxs-lookup"><span data-stu-id="612d3-103">Using PANOSE Numbers</span></span>

<span data-ttu-id="612d3-104">Os arquivos de fonte TrueType incluem números de PANOse, que os aplicativos podem usar para escolher uma fonte que corresponda de acordo com suas especificações.</span><span class="sxs-lookup"><span data-stu-id="612d3-104">TrueType font files include PANOSE numbers, which applications can use to choose a font that closely matches their specifications.</span></span> <span data-ttu-id="612d3-105">O sistema PANOse classifica faces por 10 atributos diferentes.</span><span class="sxs-lookup"><span data-stu-id="612d3-105">The PANOSE system classifies faces by 10 different attributes.</span></span> <span data-ttu-id="612d3-106">Para obter mais informações sobre esses atributos, consulte [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose).</span><span class="sxs-lookup"><span data-stu-id="612d3-106">For more information about these attributes, see [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose).</span></span> <span data-ttu-id="612d3-107">Uma estrutura **Panose** faz parte da estrutura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (cujos valores são preenchidos chamando a função [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) ).</span><span class="sxs-lookup"><span data-stu-id="612d3-107">A **PANOSE** structure is part of the [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) structure (whose values are filled in by calling the [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) function).</span></span>

<span data-ttu-id="612d3-108">Os atributos PANOse são classificados individualmente em uma escala.</span><span class="sxs-lookup"><span data-stu-id="612d3-108">The PANOSE attributes are rated individually on a scale.</span></span> <span data-ttu-id="612d3-109">Os valores resultantes são concatenados para produzir um número.</span><span class="sxs-lookup"><span data-stu-id="612d3-109">The resulting values are concatenated to produce a number.</span></span> <span data-ttu-id="612d3-110">Considerando esse número para uma fonte e uma métrica matemática para medir as distâncias no espaço PANOse, um aplicativo pode determinar os vizinhos mais próximos.</span><span class="sxs-lookup"><span data-stu-id="612d3-110">Given this number for a font and a mathematical metric to measure distances in the PANOSE space, an application can determine the nearest neighbors.</span></span>

 

 



