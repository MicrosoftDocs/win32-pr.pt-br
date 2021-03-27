---
description: O exemplo em pincéis usa regiões para simular um &\# 0034; com zoom&\# 0034; exibição de um bitmap monocromático de 8 e 8 pixels.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Usando regiões para executar testes de clique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb50ca1f837213b85619af381b86c2bd76efcbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169135"
---
# <a name="using-regions-to-perform-hit-testing"></a><span data-ttu-id="b7ffa-103">Usando regiões para executar testes de clique</span><span class="sxs-lookup"><span data-stu-id="b7ffa-103">Using Regions to Perform Hit Testing</span></span>

<span data-ttu-id="b7ffa-104">O exemplo em [pincéis](brushes.md) usa regiões para simular uma exibição "ampliada" de um bitmap monocromático de 8 e 8 pixels.</span><span class="sxs-lookup"><span data-stu-id="b7ffa-104">The example in [Brushes](brushes.md) uses regions to simulate a "zoomed" view of an 8- by 8-pixel monochrome bitmap.</span></span> <span data-ttu-id="b7ffa-105">Ao clicar nos pixels neste bitmap, o usuário cria um pincel personalizado adequado para operações de desenho.</span><span class="sxs-lookup"><span data-stu-id="b7ffa-105">By clicking on the pixels in this bitmap, the user creates a custom brush suitable for drawing operations.</span></span> <span data-ttu-id="b7ffa-106">O exemplo mostra como usar a função [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) para executar testes de clique e a função [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) para inverter as cores em uma região.</span><span class="sxs-lookup"><span data-stu-id="b7ffa-106">The example shows how to use the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function to perform hit testing and the [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) function to invert the colors in a region.</span></span>

 

 



