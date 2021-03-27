---
description: Para copiar um bitmap em um paralelogramo; Use a função PlgBlt, que executa uma transferência de bloco de bits de um retângulo em um contexto de dispositivo de origem para um paralelogramo em um contexto de dispositivo de destino.
ms.assetid: fd5b3d9f-fdce-485e-bff8-464d96b8db34
title: Rotação de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c8711189182646c55aee414ef92409a6de20ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988843"
---
# <a name="bitmap-rotation"></a><span data-ttu-id="958fb-103">Rotação de bitmap</span><span class="sxs-lookup"><span data-stu-id="958fb-103">Bitmap Rotation</span></span>

<span data-ttu-id="958fb-104">Para copiar um bitmap em um paralelogramo; Use a função [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) , que executa uma transferência de bloco de bits de um retângulo em um contexto de dispositivo de origem para um paralelogramo em um contexto de dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="958fb-104">To copy a bitmap into a parallelogram; use the [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) function, which performs a bit-block transfer from a rectangle in a source device context into a parallelogram in a destination device context.</span></span> <span data-ttu-id="958fb-105">Para girar o bitmap, um aplicativo deve fornecer as coordenadas, em unidades mundiais, a serem usadas para os cantos do paralelogramo.</span><span class="sxs-lookup"><span data-stu-id="958fb-105">To rotate the bitmap, an application must provide the coordinates, in world units, to be used for the corners of the parallelogram.</span></span> <span data-ttu-id="958fb-106">(Para obter mais informações sobre rotação e unidades mundiais, consulte [espaços de coordenadas e transformações](coordinate-spaces-and-transformations.md).)</span><span class="sxs-lookup"><span data-stu-id="958fb-106">(For more information about rotation and world units, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).)</span></span>

 

 



