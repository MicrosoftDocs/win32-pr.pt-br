---
title: Macros para valores CMYK e cores
description: As macros a seguir são úteis na manipulação de valores CMYK.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- WCS (sistema de cores do Windows), macros CMYK
- WCS (sistema de cores do Windows), macros CMYK
- gerenciamento de cores de imagem, macros CMYK
- gerenciamento de cores, macros CMYK
- cores, macros CMYK
- Referência do WCS, macros CMYK
- referência para WCS, macros CMYK
- Macros CMYK
- preto-magenta amarelo ciano (CMYK)
- CMYK (ciano magenta amarelo preto)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0efcbb6b0dc25f8f93f420113cc8c0797cba46
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105785996"
---
# <a name="macros-for-cmyk-values-and-colors"></a><span data-ttu-id="5f7e9-113">Macros para valores CMYK e cores</span><span class="sxs-lookup"><span data-stu-id="5f7e9-113">Macros for CMYK Values and Colors</span></span>

<span data-ttu-id="5f7e9-114">As macros a seguir são úteis na manipulação de valores CMYK.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-114">The following macros are useful in manipulating CMYK values.</span></span>



| <span data-ttu-id="5f7e9-115">Macro</span><span class="sxs-lookup"><span data-stu-id="5f7e9-115">Macro</span></span>                          | <span data-ttu-id="5f7e9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f7e9-116">Description</span></span>                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="5f7e9-117">**CMYK**</span><span class="sxs-lookup"><span data-stu-id="5f7e9-117">**CMYK**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | <span data-ttu-id="5f7e9-118">Cria um valor CMYK de valores de ciano, magenta, amarelo e preto individuais.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-118">Builds a CMYK value from individual cyan, magenta, yellow, and black values.</span></span> |
| [<span data-ttu-id="5f7e9-119">**GetCValue**</span><span class="sxs-lookup"><span data-stu-id="5f7e9-119">**GetCValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | <span data-ttu-id="5f7e9-120">Recupera o valor de cor ciano de um valor de cor CMYK.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-120">Retrieves the cyan color value from a CMYK color value.</span></span>                      |
| [<span data-ttu-id="5f7e9-121">**GetKValue**</span><span class="sxs-lookup"><span data-stu-id="5f7e9-121">**GetKValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | <span data-ttu-id="5f7e9-122">Recupera o valor de cor preta de um valor de cor CMYK.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-122">Retrieves the black color value from a CMYK color value.</span></span>                     |
| [<span data-ttu-id="5f7e9-123">**GetMValue**</span><span class="sxs-lookup"><span data-stu-id="5f7e9-123">**GetMValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | <span data-ttu-id="5f7e9-124">Recupera o valor magenta de um valor de cor CMYK.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-124">Retrieves the magenta value from a CMYK color value.</span></span>                         |
| [<span data-ttu-id="5f7e9-125">**GetYValue**</span><span class="sxs-lookup"><span data-stu-id="5f7e9-125">**GetYValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | <span data-ttu-id="5f7e9-126">Recupera o valor de cor amarela de um valor de cor CMYK.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-126">Retrieves the yellow color value from a CMYK color value.</span></span>                    |



 

<span data-ttu-id="5f7e9-127">As macros a seguir são usadas com cores.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-127">The following macros are used with color.</span></span>



| <span data-ttu-id="5f7e9-128">Macro</span><span class="sxs-lookup"><span data-stu-id="5f7e9-128">Macro</span></span>                                | <span data-ttu-id="5f7e9-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f7e9-129">Description</span></span>                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f7e9-130">**GetBValue**</span><span class="sxs-lookup"><span data-stu-id="5f7e9-130">**GetBValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | <span data-ttu-id="5f7e9-131">Obtém um valor azul RGB.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-131">Gets an RGB blue value.</span></span>                                                                                                                               |
| [<span data-ttu-id="5f7e9-132">**GetGValue**</span><span class="sxs-lookup"><span data-stu-id="5f7e9-132">**GetGValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | <span data-ttu-id="5f7e9-133">Obtém um valor verde RGB.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-133">Gets an RGB green value.</span></span>                                                                                                                              |
| [<span data-ttu-id="5f7e9-134">**GetRValue**</span><span class="sxs-lookup"><span data-stu-id="5f7e9-134">**GetRValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | <span data-ttu-id="5f7e9-135">Obtém um valor vermelho RGB.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-135">Gets an RGB red value.</span></span>                                                                                                                                |
| <span data-ttu-id="5f7e9-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5f7e9-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span></span> | <span data-ttu-id="5f7e9-137">Aceita um índice para uma entrada de paleta de cores lógicas e retorna um especificador de entrada de paleta.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-137">Accepts an index to a logical-color palette entry and returns a palette-entry specifier.</span></span>                                                              |
| [<span data-ttu-id="5f7e9-138">**PALETTERGB**</span><span class="sxs-lookup"><span data-stu-id="5f7e9-138">**PALETTERGB**</span></span>](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | <span data-ttu-id="5f7e9-139">Aceita três valores que representam as intensidades relativas de vermelho, verde e azul e retorna um especificador vermelho, verde, azul (RGB) relativo à paleta.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-139">Accepts three values that represent the relative intensities of red, green, and blue and returns a palette-relative red, green, blue (RGB) specifier.</span></span> |
| [<span data-ttu-id="5f7e9-140">RGB</span><span class="sxs-lookup"><span data-stu-id="5f7e9-140">RGB</span></span>](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | <span data-ttu-id="5f7e9-141">Seleciona uma cor vermelha, verde, azul (RGB) com base nos argumentos fornecidos e nos recursos de cores do dispositivo de saída.</span><span class="sxs-lookup"><span data-stu-id="5f7e9-141">Selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.</span></span>                               |



 

 

 