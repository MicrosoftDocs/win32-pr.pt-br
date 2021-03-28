---
description: Um pincel sólido é um pincel lógico que contém 64 pixels da mesma cor.
ms.assetid: 920014c7-d1ef-4b98-8c92-c4169be52cb9
title: Pincel sólido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7cd7a2140ece4bf93ac6f8525be461b70e28fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967871"
---
# <a name="solid-brush"></a><span data-ttu-id="ef7af-103">Pincel sólido</span><span class="sxs-lookup"><span data-stu-id="ef7af-103">Solid Brush</span></span>

<span data-ttu-id="ef7af-104">Um *pincel sólido* é um pincel lógico que contém 64 pixels da mesma cor.</span><span class="sxs-lookup"><span data-stu-id="ef7af-104">A *solid brush* is a logical brush that contains 64 pixels of the same color.</span></span> <span data-ttu-id="ef7af-105">Um aplicativo pode criar um pincel lógico sólido chamando a função [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) , especificando a cor do pincel necessário.</span><span class="sxs-lookup"><span data-stu-id="ef7af-105">An application can create a solid logical brush by calling the [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) function, specifying the color of the brush required.</span></span> <span data-ttu-id="ef7af-106">Depois de criar o pincel sólido, o aplicativo pode selecioná-lo em seu contexto de dispositivo e usá-lo para pintar formas preenchidas.</span><span class="sxs-lookup"><span data-stu-id="ef7af-106">After creating the solid brush, the application can select it into its device context and use it to paint filled shapes.</span></span>

 

 



