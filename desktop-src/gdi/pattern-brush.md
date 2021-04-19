---
description: Um pincel (ou personalizado) padrão é criado por meio de um bitmap definido pelo aplicativo ou DIB (bitmap independente de dispositivo). Os retângulos a seguir foram pintados usando pincéis de padrão diferentes.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Pincel de padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d39dd499d6a95b3fb61624b2aab8b421f51c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988319"
---
# <a name="pattern-brush"></a><span data-ttu-id="a9155-104">Pincel de padrão</span><span class="sxs-lookup"><span data-stu-id="a9155-104">Pattern Brush</span></span>

<span data-ttu-id="a9155-105">Um pincel (ou personalizado) padrão é criado por meio de um bitmap definido pelo aplicativo ou DIB (bitmap independente de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="a9155-105">A pattern (or custom) brush is created from an application-defined bitmap or device-independent bitmap (DIB).</span></span> <span data-ttu-id="a9155-106">Os retângulos a seguir foram pintados usando pincéis de padrão diferentes.</span><span class="sxs-lookup"><span data-stu-id="a9155-106">The following rectangles were painted by using different pattern brushes.</span></span>

![ilustração mostrando três caixas, cada uma preenchida com um padrão diferente](images/csbru-05.png)

<span data-ttu-id="a9155-108">Para criar um pincel de padrão lógico, um aplicativo deve primeiro criar um bitmap.</span><span class="sxs-lookup"><span data-stu-id="a9155-108">To create a logical pattern brush, an application must first create a bitmap.</span></span> <span data-ttu-id="a9155-109">Depois de criar o bitmap, o aplicativo pode criar o pincel de padrão lógico chamando a função [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) ou [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) , fornecendo um identificador que identifica o bitmap (ou DIB).</span><span class="sxs-lookup"><span data-stu-id="a9155-109">After creating the bitmap, the application can create the logical pattern brush by calling the [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) or [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) function, supplying a handle that identifies the bitmap (or DIB).</span></span> <span data-ttu-id="a9155-110">Os pincéis que aparecem na ilustração anterior foram criados a partir de bitmaps monocromáticos.</span><span class="sxs-lookup"><span data-stu-id="a9155-110">The brushes that appear in the preceding illustration were created from monochrome bitmaps.</span></span> <span data-ttu-id="a9155-111">Para obter uma descrição de bitmaps, DIBs e as funções que os criam, consulte [bitmaps](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="a9155-111">For a description of bitmaps, DIBs, and the functions that create them, see [Bitmaps](bitmaps.md).</span></span>

 

 



