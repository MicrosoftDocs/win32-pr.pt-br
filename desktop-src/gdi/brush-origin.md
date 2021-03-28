---
description: Quando um aplicativo chama uma função de desenho para pintar uma forma, o sistema posiciona um pincel no início da operação de pintura e mapeia um pixel no bitmap do pincel para a área do cliente na origem da janela, que é o canto superior esquerdo da janela.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Origem do pincel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 016237b97a52da6fd7fa14a3b6ba2dc25b03b96e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560827"
---
# <a name="brush-origin"></a><span data-ttu-id="b05dd-103">Origem do pincel</span><span class="sxs-lookup"><span data-stu-id="b05dd-103">Brush Origin</span></span>

<span data-ttu-id="b05dd-104">Quando um aplicativo chama uma função de desenho para pintar uma forma, o sistema posiciona um pincel no início da operação de pintura e mapeia um pixel no bitmap do pincel para a área do cliente na *origem da janela*, que é o canto superior esquerdo da janela.</span><span class="sxs-lookup"><span data-stu-id="b05dd-104">When an application calls a drawing function to paint a shape, the system positions a brush at the start of the paint operation and maps a pixel in the brush bitmap to the client area at the *window origin*, which is the upper-left corner of the window.</span></span> <span data-ttu-id="b05dd-105">As coordenadas do pixel que o sistema mapeia são chamadas de *origem do pincel*.</span><span class="sxs-lookup"><span data-stu-id="b05dd-105">The coordinates of the pixel that the system maps are called the *brush origin*.</span></span> <span data-ttu-id="b05dd-106">A origem do pincel padrão está localizada no canto superior esquerdo do bitmap do pincel, nas coordenadas (0, 0).</span><span class="sxs-lookup"><span data-stu-id="b05dd-106">The default brush origin is located in the upper-left corner of the brush bitmap, at the coordinates (0,0).</span></span> <span data-ttu-id="b05dd-107">Em seguida, o sistema copia o pincel pela área do cliente, formando um padrão que é tão alto quanto o bitmap.</span><span class="sxs-lookup"><span data-stu-id="b05dd-107">The system then copies the brush across the client area, forming a pattern that is as tall as the bitmap.</span></span> <span data-ttu-id="b05dd-108">A operação de cópia continua, linha por linha, até que toda a área do cliente seja preenchida.</span><span class="sxs-lookup"><span data-stu-id="b05dd-108">The copy operation continues, row by row, until the entire client area is filled.</span></span> <span data-ttu-id="b05dd-109">No entanto, o padrão de pincel é visível somente dentro dos limites da forma especificada.</span><span class="sxs-lookup"><span data-stu-id="b05dd-109">However, the brush pattern is visible only within the boundaries of the specified shape.</span></span>

<span data-ttu-id="b05dd-110">Há instâncias em que a origem do pincel padrão não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="b05dd-110">There are instances when the default brush origin should not be used.</span></span> <span data-ttu-id="b05dd-111">Por exemplo, pode ser necessário que um aplicativo use o mesmo pincel para pintar os planos de fundo de suas janelas pai e filho e misturar o plano de fundo de uma janela filho com aquela da janela pai.</span><span class="sxs-lookup"><span data-stu-id="b05dd-111">For example, it may be necessary for an application to use the same brush to paint the backgrounds of its parent and child windows and blend a child window's background with that of the parent window.</span></span> <span data-ttu-id="b05dd-112">Para fazer isso, o aplicativo deve redefinir a origem do pincel chamando a função [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) e deslocando a origem do número de pixels necessário.</span><span class="sxs-lookup"><span data-stu-id="b05dd-112">To do this, the application should reset the brush origin by calling the [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) function and shifting the origin the required number of pixels.</span></span> <span data-ttu-id="b05dd-113">(Um aplicativo pode recuperar a origem do pincel atual chamando a função [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) .)</span><span class="sxs-lookup"><span data-stu-id="b05dd-113">(An application can retrieve the current brush origin by calling the [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) function.)</span></span>

<span data-ttu-id="b05dd-114">A ilustração a seguir mostra uma estrela de cinco pontas preenchida usando um pincel definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b05dd-114">The following illustration shows a five-pointed star filled by using an application-defined brush.</span></span> <span data-ttu-id="b05dd-115">A ilustração mostra uma imagem com zoom do pincel, bem como o local no qual ele foi mapeado no início da operação de pintura.</span><span class="sxs-lookup"><span data-stu-id="b05dd-115">The illustration shows a zoomed image of the brush, as well as the location to which it was mapped at the beginning of the paint operation.</span></span>

![ilustração mostrando que a origem do pincel está mapeada para a origem da janela](images/csbru-01.png)

 

 



