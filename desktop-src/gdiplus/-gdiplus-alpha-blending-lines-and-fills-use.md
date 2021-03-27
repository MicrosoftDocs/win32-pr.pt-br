---
description: No Windows GDI+, uma cor é um valor de 32 bits com 8 bits cada para alfa, vermelho, verde e azul.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Combinação alfa em linhas e preenchimentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13fe306dbf31c2a60a0bd38bf71b9e96edb201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827972"
---
# <a name="alpha-blending-lines-and-fills"></a><span data-ttu-id="dfccc-103">Combinação alfa em linhas e preenchimentos</span><span class="sxs-lookup"><span data-stu-id="dfccc-103">Alpha Blending Lines and Fills</span></span>

<span data-ttu-id="dfccc-104">No Windows GDI+, uma cor é um valor de 32 bits com 8 bits cada para alfa, vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="dfccc-104">In Windows GDI+, a color is a 32-bit value with 8 bits each for alpha, red, green, and blue.</span></span> <span data-ttu-id="dfccc-105">O valor alfa indica a transparência da cor – a extensão a qual a cor é combinada com a cor da tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="dfccc-105">The alpha value indicates the transparency of the color — the extent to which the color is blended with the background color.</span></span> <span data-ttu-id="dfccc-106">Os valores alfa variam de 0 a 255, em que 0 representa uma cor totalmente transparente e 255 representa uma cor totalmente opaca.</span><span class="sxs-lookup"><span data-stu-id="dfccc-106">Alpha values range from 0 through 255, where 0 represents a fully transparent color, and 255 represents a fully opaque color.</span></span>

<span data-ttu-id="dfccc-107">A combinação alfa é uma combinação de pixel por pixel da fonte e dos dados de cor da tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="dfccc-107">Alpha blending is a pixel-by-pixel blending of source and background color data.</span></span> <span data-ttu-id="dfccc-108">Cada um dos três componentes (vermelho, verde, azul) de uma cor de origem é combinado com o componente correspondente da cor da tela de fundo de acordo com a seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="dfccc-108">Each of the three components (red, green, blue) of a given source color is blended with the corresponding component of the background color according to the following formula:</span></span>

<span data-ttu-id="dfccc-109">displayColor = sourceColor × alfa / 255 + backgroundColor × (255 – alfa) / 255</span><span class="sxs-lookup"><span data-stu-id="dfccc-109">displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255</span></span>

<span data-ttu-id="dfccc-110">Por exemplo, suponha que o componente vermelho da cor da fonte é 150 e o componente vermelho da cor da tela de fundo é 100.</span><span class="sxs-lookup"><span data-stu-id="dfccc-110">For example, suppose the red component of the source color is 150 and the red component of the background color is 100.</span></span> <span data-ttu-id="dfccc-111">Se o valor alfa for 200, o componente vermelho da cor resultante será calculado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="dfccc-111">If the alpha value is 200, the red component of the resultant color is calculated as follows:</span></span>

<span data-ttu-id="dfccc-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span><span class="sxs-lookup"><span data-stu-id="dfccc-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span></span>

<span data-ttu-id="dfccc-113">Os tópicos a seguir abordam a mistura alfa em mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="dfccc-113">The following topics cover alpha blending in more detail:</span></span>

-   [<span data-ttu-id="dfccc-114">Desenhar linhas opacas e semitransparentes</span><span class="sxs-lookup"><span data-stu-id="dfccc-114">Drawing Opaque and Semitransparent Lines</span></span>](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [<span data-ttu-id="dfccc-115">Desenho com pincéis opacos e semitransparentes</span><span class="sxs-lookup"><span data-stu-id="dfccc-115">Drawing with Opaque and Semitransparent Brushes</span></span>](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [<span data-ttu-id="dfccc-116">Usando o modo de composição para controlar a mesclagem alfa</span><span class="sxs-lookup"><span data-stu-id="dfccc-116">Using Compositing Mode to Control Alpha Blending</span></span>](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [<span data-ttu-id="dfccc-117">Uso de uma matriz de cores para definir valores alfa em imagens</span><span class="sxs-lookup"><span data-stu-id="dfccc-117">Using a Color Matrix to Set Alpha Values in Images</span></span>](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [<span data-ttu-id="dfccc-118">Definindo os valores Alfa de pixels individuais</span><span class="sxs-lookup"><span data-stu-id="dfccc-118">Setting the Alpha Values of Individual Pixels</span></span>](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



