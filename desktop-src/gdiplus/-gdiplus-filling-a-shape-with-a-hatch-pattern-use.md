---
description: 'Um padrão de hachura é feito de duas cores: um para o plano de fundo e outro para as linhas que formam o padrão em segundo plano.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Preenchendo uma forma com um padrão de hachura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37f06c93a6ac66a4a6066874c99b88652a0819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987873"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a><span data-ttu-id="2516d-103">Preenchendo uma forma com um padrão de hachura</span><span class="sxs-lookup"><span data-stu-id="2516d-103">Filling a Shape with a Hatch Pattern</span></span>

<span data-ttu-id="2516d-104">Um padrão de hachura é feito de duas cores: um para o plano de fundo e outro para as linhas que formam o padrão em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2516d-104">A hatch pattern is made from two colors: one for the background and one for the lines that form the pattern over the background.</span></span> <span data-ttu-id="2516d-105">Para preencher uma forma fechada com um padrão de hachura, use um objeto [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) .</span><span class="sxs-lookup"><span data-stu-id="2516d-105">To fill a closed shape with a hatch pattern, use a [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) object.</span></span> <span data-ttu-id="2516d-106">O exemplo a seguir demonstra como preencher uma elipse com um padrão de hachura:</span><span class="sxs-lookup"><span data-stu-id="2516d-106">The following example demonstrates how to fill an ellipse with a hatch pattern:</span></span>


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



<span data-ttu-id="2516d-107">A ilustração a seguir mostra a elipse preenchida.</span><span class="sxs-lookup"><span data-stu-id="2516d-107">The following illustration shows the filled ellipse.</span></span>

![ilustração de uma elipse preenchida com um padrão de hachura de linhas horizontais em um plano de fundo sólido](images/hatch1.png)

<span data-ttu-id="2516d-109">O construtor [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) usa três argumentos: o estilo de hachura, a cor da linha de hachura e a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="2516d-109">The [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) constructor takes three arguments: the hatch style, the color of the hatch line, and the color of the background.</span></span> <span data-ttu-id="2516d-110">O argumento de estilo de hachura pode ser qualquer elemento da enumeração [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) .</span><span class="sxs-lookup"><span data-stu-id="2516d-110">The hatch style argument can be any element of the [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) enumeration.</span></span> <span data-ttu-id="2516d-111">Há mais de 50 elementos na enumeração **HatchStyle** ; alguns desses elementos são mostrados na lista a seguir:</span><span class="sxs-lookup"><span data-stu-id="2516d-111">There are more than fifty elements in the **HatchStyle** enumeration; a few of those elements are shown in the following list:</span></span>

-   <span data-ttu-id="2516d-112">**HatchStyleHorizontal**</span><span class="sxs-lookup"><span data-stu-id="2516d-112">**HatchStyleHorizontal**</span></span>
-   <span data-ttu-id="2516d-113">**HatchStyleVertical**</span><span class="sxs-lookup"><span data-stu-id="2516d-113">**HatchStyleVertical**</span></span>
-   <span data-ttu-id="2516d-114">**HatchStyleForwardDiagonal**</span><span class="sxs-lookup"><span data-stu-id="2516d-114">**HatchStyleForwardDiagonal**</span></span>
-   <span data-ttu-id="2516d-115">**HatchStyleBackwardDiagonal**</span><span class="sxs-lookup"><span data-stu-id="2516d-115">**HatchStyleBackwardDiagonal**</span></span>
-   <span data-ttu-id="2516d-116">**HatchStyleCross**</span><span class="sxs-lookup"><span data-stu-id="2516d-116">**HatchStyleCross**</span></span>
-   <span data-ttu-id="2516d-117">**HatchStyleDiagonalCross**</span><span class="sxs-lookup"><span data-stu-id="2516d-117">**HatchStyleDiagonalCross**</span></span>

 

 



