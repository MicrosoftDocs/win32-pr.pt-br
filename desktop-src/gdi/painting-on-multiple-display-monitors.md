---
description: O sistema manipula automaticamente a pintura em um DC (contexto de dispositivo) que abrange mais de um monitor, mesmo quando os monitores têm profundidades de cores diferentes.
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: Pintando em vários monitores de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b6a3e3699000399c61e641137a951ed321fd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661592"
---
# <a name="painting-on-multiple-display-monitors"></a><span data-ttu-id="70677-103">Pintando em vários monitores de vídeo</span><span class="sxs-lookup"><span data-stu-id="70677-103">Painting on Multiple Display Monitors</span></span>

<span data-ttu-id="70677-104">O sistema manipula automaticamente a pintura em um DC (contexto de dispositivo) que abrange mais de um monitor, mesmo quando os monitores têm profundidades de cores diferentes.</span><span class="sxs-lookup"><span data-stu-id="70677-104">The system automatically handles painting into a device context (DC) that spans more than one monitor, even when the monitors have different color depths.</span></span> <span data-ttu-id="70677-105">Geralmente, isso produz bons resultados, mas pode não ser o ideal.</span><span class="sxs-lookup"><span data-stu-id="70677-105">Usually this produces good results, but it may not be optimal.</span></span> <span data-ttu-id="70677-106">Por exemplo, uma janela em dois monitores de profundidades de cores muito diferentes poderia ter uma representação de cor ruim.</span><span class="sxs-lookup"><span data-stu-id="70677-106">For example, a window on two monitors of vastly different color depths could have poor color rendition.</span></span> <span data-ttu-id="70677-107">Além disso, monitores com a mesma intensidade de cor podem ter um exemplo de formatsfor de cor diferente, as cores podem ser codificadas com diferentes números de bits ou estar localizadas em locais diferentes no valor de cor de um pixel.</span><span class="sxs-lookup"><span data-stu-id="70677-107">Also, monitors with the same color depth may have different color formatsfor example, colors could be encoded with different numbers of bits, or be located in different places in a pixel's color value.</span></span>

<span data-ttu-id="70677-108">Para obter os melhores resultados para cada um dos monitores em um DC que abrange mais de uma exibição, chame [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) para enumerar os monitores que interseccionam seu controlador de domínio e pinte a área de interseção em cada um deles separadamente de acordo com os atributos de exibição desse monitor.</span><span class="sxs-lookup"><span data-stu-id="70677-108">To get the best results for each of the monitors in a DC that spans more than one display, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) to enumerate the monitors that intersect your DC and paint the intersecting area in each of them separately according to the display attributes for that monitor.</span></span> <span data-ttu-id="70677-109">Consulte o exemplo em [pintura em um DC que abrange vários monitores](painting-on-a-dc-that-spans-multiple-displays.md).</span><span class="sxs-lookup"><span data-stu-id="70677-109">See the example in [Painting on a DC That Spans Multiple Displays](painting-on-a-dc-that-spans-multiple-displays.md).</span></span>

<span data-ttu-id="70677-110">Se você fizer todo o desenho em seu código **de \_ pintura do WM** e se o código de **\_ pintura do WM** tratar de todos os vários modos de vídeo, você deverá ser capaz de posicionar o código de **\_ pintura do WM** no **MonitorEnumProc** de [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) com apenas algumas modificações.</span><span class="sxs-lookup"><span data-stu-id="70677-110">If you do all of your drawing in your **WM\_PAINT** code and if your **WM\_PAINT** code handles all of the various video modes, then you should be able to place your **WM\_PAINT** code in the **MonitorEnumProc** of [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) with only a few modifications.</span></span>

 

 



