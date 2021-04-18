---
title: Espaços de cores dependentes do dispositivo
description: A maioria dos espaços de cores são dependentes do dispositivo.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- WCS (sistema de cores do Windows), espaços de cores dependentes do dispositivo
- WCS (sistema de cores do Windows), espaços de cores dependentes do dispositivo
- gerenciamento de cores de imagem, espaços de cores dependentes do dispositivo
- gerenciamento de cores, espaços de cores dependentes do dispositivo
- cores, espaços de cores dependentes do dispositivo
- espaços de cores, dependentes do dispositivo
- espaços de cores dependentes do dispositivo
- ponto branco
- colorants
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1523ee6ba81dcdc3b69a468546871cfd21913
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105769669"
---
# <a name="device-dependent-color-spaces"></a><span data-ttu-id="aa8b7-112">Espaços de cores dependentes do dispositivo</span><span class="sxs-lookup"><span data-stu-id="aa8b7-112">Device-Dependent Color Spaces</span></span>

<span data-ttu-id="aa8b7-113">A maioria dos [espaços de cores](c.md) são dependentes do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-113">Most [color spaces](c.md) are device dependent.</span></span> <span data-ttu-id="aa8b7-114">Embora um dispositivo específico, como uma impressora, possa usar o espaço de cores CMYK, as cores que ele renderiza para valores CMYK específicos geralmente são um pouco diferentes de todos os outros tipos de impressoras.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-114">Even though a particular device, such as a printer, may use the CMYK color space, the colors it renders for specific CMYK values are often slightly different than all other types of printers..</span></span> <span data-ttu-id="aa8b7-115">É precisamente por esse motivo que o sistema de gerenciamento de cores WCS 1,0 é tão útil.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-115">It is precisely for this reason that the WCS 1.0 color management system is so useful.</span></span>

<span data-ttu-id="aa8b7-116">Todos os espaços de cores têm um *ponto branco*, que é definido como o branco mais branco que pode ser produzido nesse espaço de cores.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-116">All color spaces have a *white point*, which is defined as the whitest white that can be produced in that color space.</span></span> <span data-ttu-id="aa8b7-117">Como os dispositivos podem diferir um do outro, seus pontos brancos também podem diferir.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-117">Since devices can differ from one another, their white points can also differ.</span></span> <span data-ttu-id="aa8b7-118">Todas as cores que um dispositivo pode produzir são relativas a seu ponto branco.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-118">All colors that a device can produce are relative to its white point.</span></span> <span data-ttu-id="aa8b7-119">Portanto, um sistema de gerenciamento de cores deve ser capaz de mapear o ponto branco de um espaço de cor para outro e preservar os locais relativos de todas as cores.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-119">Therefore, a color management system must be able to map the white point of one color space into another and preserve the relative locations of all colors.</span></span> <span data-ttu-id="aa8b7-120">Ele também deve ser capaz de mapear uma cor em um espaço de cor para sua correspondência mais próxima em outro espaço de cores, independentemente das diferenças nos pontos brancos.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-120">It must also be able to map a color in one color space to its closest match in another color space regardless of the differences in the white points.</span></span> <span data-ttu-id="aa8b7-121">O WCS 1,0 é capaz de realizar essas duas tarefas.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-121">WCS 1.0 is able to accomplish both of these tasks.</span></span>

<span data-ttu-id="aa8b7-122">O espaço de cores RGB geralmente é usado em monitores de computador.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-122">The RGB color space is often used on computer monitors.</span></span> <span data-ttu-id="aa8b7-123">Como tal, é dependente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-123">As such, it is device dependent.</span></span> <span data-ttu-id="aa8b7-124">As impressoras normalmente usam [COLORANTS](c.md)CMYK.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-124">Printers typically use CMYK [colorants](c.md).</span></span> <span data-ttu-id="aa8b7-125">Cada impressora implementa sua própria versão do espaço de cores CMYK.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-125">Each printer implements its own version of the CMYK color space.</span></span> <span data-ttu-id="aa8b7-126">As imagens digitais podem, na verdade, armazenar as cores nelas.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-126">Digital images may not actually store colors in them.</span></span> <span data-ttu-id="aa8b7-127">Eles podem armazenar números de índice em uma paleta de cores.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-127">They may store index numbers into a palette of colors.</span></span> <span data-ttu-id="aa8b7-128">O resultado é que é muito difícil para os desenvolvedores de aplicativos individuais usarem ou fornecerem um método padronizado de movimentação de imagens coloridas de um dispositivo para outro.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-128">The result is that it is very hard for individual application developers to use or provide a standardized method of moving color images from one device to another.</span></span> <span data-ttu-id="aa8b7-129">Os profissionais de geração de imagens normalmente experimentam a frustração de criar uma imagem gráfica em uma tela de computador e fazer com que ela se transforme de maneira muito diferente quando impressa.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-129">Imaging professionals commonly experience the frustration of creating a graphic image on a computer screen and having it turn out very differently when it is printed.</span></span> <span data-ttu-id="aa8b7-130">O WCS 1,0 aborda essas necessidades de geração de imagens.</span><span class="sxs-lookup"><span data-stu-id="aa8b7-130">WCS 1.0 addresses these imaging needs.</span></span>

 

 




