---
description: A função StretchBlt dimensiona um bitmap executando uma transferência de bloco de bits de um retângulo em um contexto de dispositivo de origem em um retângulo em um contexto de dispositivo de destino.
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: Dimensionamento de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4011b06e6a7269be29e1834e90928c4f531b1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091220"
---
# <a name="bitmap-scaling"></a><span data-ttu-id="a508e-103">Dimensionamento de bitmap</span><span class="sxs-lookup"><span data-stu-id="a508e-103">Bitmap Scaling</span></span>

<span data-ttu-id="a508e-104">A função [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) dimensiona um bitmap executando uma transferência de bloco de bits de um retângulo em um contexto de dispositivo de origem em um retângulo em um contexto de dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="a508e-104">The [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) function scales a bitmap by performing a bit-block transfer from a rectangle in a source device context into a rectangle in a destination device context.</span></span> <span data-ttu-id="a508e-105">No entanto, ao contrário da função [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) , que duplica as dimensões do retângulo de origem no retângulo de destino, o **StretchBlt** permite que um aplicativo especifique as dimensões dos retângulos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="a508e-105">However, unlike the [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) function, which duplicates the source rectangle dimensions in the destination rectangle, **StretchBlt** allows an application to specify the dimensions of both the source and the destination rectangles.</span></span> <span data-ttu-id="a508e-106">Quando o bitmap de destino é menor do que o bitmap de origem, o sistema combina linhas ou colunas de dados de cor (ou ambos) no bitmap antes de renderizar a imagem correspondente no dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a508e-106">When the destination bitmap is smaller than the source bitmap, the system combines rows or columns of color data (or both) in the bitmap before rendering the corresponding image on the display device.</span></span> <span data-ttu-id="a508e-107">O sistema combina os dados de cor de acordo com o modo de ampliação especificado, que o aplicativo define chamando a função [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) .</span><span class="sxs-lookup"><span data-stu-id="a508e-107">The system combines the color data according to the specified stretch mode, which the application defines by calling the [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) function.</span></span> <span data-ttu-id="a508e-108">Quando o bitmap de destino é maior do que o bitmap de origem, o sistema dimensiona ou amplia cada pixel na imagem resultante de acordo.</span><span class="sxs-lookup"><span data-stu-id="a508e-108">When the destination bitmap is larger than the source bitmap, the system scales or magnifies each pixel in the resultant image accordingly.</span></span>

 

 



