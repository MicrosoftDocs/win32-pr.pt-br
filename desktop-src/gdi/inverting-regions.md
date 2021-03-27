---
description: Um aplicativo inverte as cores que aparecem dentro de uma região chamando a função InvertRgn.
ms.assetid: bcd9fe61-0f92-41bc-b953-a66e01e43a75
title: Invertendo regiões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e3c4b4d01f9ed8f09e819d59bf3268a1ccae4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988801"
---
# <a name="inverting-regions"></a><span data-ttu-id="b2baf-103">Invertendo regiões</span><span class="sxs-lookup"><span data-stu-id="b2baf-103">Inverting Regions</span></span>

<span data-ttu-id="b2baf-104">Um aplicativo inverte as cores que aparecem dentro de uma região chamando a função [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) .</span><span class="sxs-lookup"><span data-stu-id="b2baf-104">An application inverts the colors that appear within a region by calling the [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) function.</span></span> <span data-ttu-id="b2baf-105">Em monitores monocromáticos, o **InvertRgn** torna branco pixels pretos e preto pixels brancos.</span><span class="sxs-lookup"><span data-stu-id="b2baf-105">On monochrome displays, **InvertRgn** makes white pixels black and black pixels white.</span></span> <span data-ttu-id="b2baf-106">Em telas de cores, essa inversão depende do tipo de tecnologia usado para gerar as cores da tela.</span><span class="sxs-lookup"><span data-stu-id="b2baf-106">On color screens, this inversion is dependent on the type of technology used to generate the colors for the screen.</span></span>

 

 



