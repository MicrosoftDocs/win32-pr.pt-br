---
description: A cor é definida como uma combinação de três cores primárias, vermelho, verde e azul.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Valores de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e46cd7ee87871c660702bed120958e7096745d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091201"
---
# <a name="color-values"></a><span data-ttu-id="6d457-103">Valores de cor</span><span class="sxs-lookup"><span data-stu-id="6d457-103">Color Values</span></span>

<span data-ttu-id="6d457-104">A cor é definida como uma combinação de três cores primárias, vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="6d457-104">Color is defined as a combination of three primary colors red, green, and blue.</span></span> <span data-ttu-id="6d457-105">o sistema identifica uma cor, dando a ela um valor de cor (às vezes chamado de terceto RGB), que consiste em valores de 3 8 bits especificando as intensidades de seus componentes de cor.</span><span class="sxs-lookup"><span data-stu-id="6d457-105">the system identifies a color by giving it a color value (sometimes called an RGB triplet), which consists of three 8-bit values specifying the intensities of its color components.</span></span> <span data-ttu-id="6d457-106">Preto tem a intensidade mínima para vermelho, verde e azul, portanto, o valor de cor para preto é (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="6d457-106">Black has the minimum intensity for red, green, and blue, so the color value for black is (0, 0, 0).</span></span> <span data-ttu-id="6d457-107">O branco tem a intensidade máxima para vermelho, verde e azul, portanto, seu valor de cor é (255, 255, 255).</span><span class="sxs-lookup"><span data-stu-id="6d457-107">White has the maximum intensity for red, green, and blue, so its color value is (255, 255, 255).</span></span>

> [!Note]  
> <span data-ttu-id="6d457-108">Se a correspondência de cores da imagem estiver habilitada, a definição de cor e o significado de um valor de cor dependerá do tipo de espaço de cor definido atualmente para o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d457-108">If image color matching is enabled, the definition of color and the meaning of a color value depends on the type of color space that is currently set for the device context.</span></span>

 

<span data-ttu-id="6d457-109">O sistema e os aplicativos usam parâmetros e variáveis que têm o tipo [COLORREF](colorref.md) para passar e armazenar valores de cor.</span><span class="sxs-lookup"><span data-stu-id="6d457-109">The system and applications use parameters and variables having the [COLORREF](colorref.md) type to pass and store color values.</span></span> <span data-ttu-id="6d457-110">Por exemplo, a função [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) identifica a cor de cada caneta definindo o membro **lopnColor** em uma estrutura [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) como um valor de cor.</span><span class="sxs-lookup"><span data-stu-id="6d457-110">For example, the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function identifies the color of each pen by setting the **lopnColor** member in a [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) structure to a color value.</span></span> <span data-ttu-id="6d457-111">Os aplicativos podem extrair os valores individuais dos componentes vermelho, verde e azul de um valor de cor usando as macros [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)e [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6d457-111">Applications can extract the individual values of the red, green, and blue components from a color value by using the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span> <span data-ttu-id="6d457-112">Os aplicativos podem criar um valor de cor de valores de componentes individuais usando a macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="6d457-112">Applications can create a color value from individual component values by using the [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="6d457-113">Ao criar ou examinar uma paleta lógica, um aplicativo usa a estrutura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) para definir valores de cor e para examinar valores de componentes individuais.</span><span class="sxs-lookup"><span data-stu-id="6d457-113">When creating or examining a logical palette, an application uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure to define color values and to examine individual component values.</span></span>

 

 



