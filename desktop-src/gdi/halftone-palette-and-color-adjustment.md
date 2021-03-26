---
description: As paletas de meio-tom devem ser usadas sempre que o modo de alongamento de um contexto de dispositivo for definido como meio-tom.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Paleta de retícula e ajuste de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e6708aff92387b792424f07e9b82a1f6125ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502418"
---
# <a name="halftone-palette-and-color-adjustment"></a><span data-ttu-id="4284e-103">Paleta de retícula e ajuste de cor</span><span class="sxs-lookup"><span data-stu-id="4284e-103">Halftone Palette and Color Adjustment</span></span>

<span data-ttu-id="4284e-104">As paletas de meio-tom devem ser usadas sempre que o modo de alongamento de um contexto de dispositivo for definido como meio-tom.</span><span class="sxs-lookup"><span data-stu-id="4284e-104">Halftone palettes are intended to be used whenever the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="4284e-105">Um aplicativo cria uma paleta de meio-tom usando a função [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) .</span><span class="sxs-lookup"><span data-stu-id="4284e-105">An application creates a halftone palette by using the [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) function.</span></span> <span data-ttu-id="4284e-106">O aplicativo deve selecionar e perceber essa paleta no contexto do dispositivo antes de chamar a função [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) ou [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) .</span><span class="sxs-lookup"><span data-stu-id="4284e-106">The application must select and realize this palette into the device context before calling the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) or [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) function.</span></span>

<span data-ttu-id="4284e-107">O sistema ajusta automaticamente a cor de entrada dos bitmaps de origem sempre que os aplicativos chamam as funções [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) e [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) e o modo de alongamento de um contexto de dispositivo é definido como meio-tom.</span><span class="sxs-lookup"><span data-stu-id="4284e-107">The system automatically adjusts the input color of source bitmaps whenever applications call the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) and [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) functions and the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="4284e-108">Esses ajustes de cor afetam determinados atributos da imagem, como contraste e brilho.</span><span class="sxs-lookup"><span data-stu-id="4284e-108">These color adjustments affect certain attributes of the image, such as contrast and brightness.</span></span> <span data-ttu-id="4284e-109">Um aplicativo pode definir os valores de ajuste de cor usando a função [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) .</span><span class="sxs-lookup"><span data-stu-id="4284e-109">An application can set the color adjustment values by using the [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) function.</span></span> <span data-ttu-id="4284e-110">O aplicativo pode recuperar os valores de ajuste de cor para o contexto de dispositivo especificado usando a função [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) .</span><span class="sxs-lookup"><span data-stu-id="4284e-110">The application can retrieve the color adjustment values for the specified device context by using the [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) function.</span></span>

 

 



