---
description: Os recursos de cores de dispositivos, como telas e impressoras, podem variar de monocromático a milhares de cores.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Noções básicas de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165088"
---
# <a name="color-basics"></a><span data-ttu-id="dcc71-103">Noções básicas de cor</span><span class="sxs-lookup"><span data-stu-id="dcc71-103">Color Basics</span></span>

<span data-ttu-id="dcc71-104">Os recursos de cores de dispositivos, como telas e impressoras, podem variar de monocromático a milhares de cores.</span><span class="sxs-lookup"><span data-stu-id="dcc71-104">The color capabilities of devices, such as displays and printers, can range from monochrome to thousands of colors.</span></span> <span data-ttu-id="dcc71-105">Como um aplicativo pode precisar gerar saída para dispositivos durante esse intervalo, ele deve estar preparado para lidar com recursos de cores variáveis.</span><span class="sxs-lookup"><span data-stu-id="dcc71-105">Because an application may need to generate output for devices throughout this range, it should be prepared to handle varying color capabilities.</span></span>

<span data-ttu-id="dcc71-106">Um aplicativo pode descobrir o número de cores disponíveis para um determinado dispositivo usando a função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar o valor de NUMCOLORS.</span><span class="sxs-lookup"><span data-stu-id="dcc71-106">An application can discover the number of colors available for a given device by using the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve the NUMCOLORS value.</span></span> <span data-ttu-id="dcc71-107">Esse valor especifica a contagem de cores disponíveis para uso pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dcc71-107">This value specifies the count of colors available for use by the application.</span></span> <span data-ttu-id="dcc71-108">Normalmente, essa contagem corresponde a uma propriedade física do dispositivo de saída, como o número de tintas na impressora ou o número de sinais de cor distintos que o adaptador de vídeo pode transmitir para o monitor.</span><span class="sxs-lookup"><span data-stu-id="dcc71-108">Usually, this count corresponds to a physical property of the output device, such as the number of inks in the printer or the number of distinct color signals the display adapter can transmit to the monitor.</span></span>

<span data-ttu-id="dcc71-109">Embora o valor de NUMCOLORS especifique a contagem de cores, ele não identifica quais são as cores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dcc71-109">Although the NUMCOLORS value specifies the count of colors, it does not identify what the available colors are.</span></span> <span data-ttu-id="dcc71-110">Um aplicativo pode descobrir quais cores estão disponíveis enumerando todas as canetas com o \_ tipo sólido PS.</span><span class="sxs-lookup"><span data-stu-id="dcc71-110">An application can discover what colors are available by enumerating all pens having the PS\_SOLID type.</span></span> <span data-ttu-id="dcc71-111">Como o driver de dispositivo que dá suporte a um determinado dispositivo geralmente tem uma gama completa de canetas sólidas e como o sistema requer que as canetas sólidas tenham apenas cores que o dispositivo pode gerar, a enumeração dessas canetas geralmente é equivalente à enumeração das cores.</span><span class="sxs-lookup"><span data-stu-id="dcc71-111">Because the device driver that supports a given device usually has a full range of solid pens and because the system requires that solid pens have only colors that the device can generate, enumerating these pens is often equivalent to enumerating the colors.</span></span> <span data-ttu-id="dcc71-112">Um aplicativo pode enumerar as canetas usando a função [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) .</span><span class="sxs-lookup"><span data-stu-id="dcc71-112">An application can enumerate the pens by using the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function.</span></span> <span data-ttu-id="dcc71-113">Para obter um exemplo de código, consulte [enumerando cores](enumerating-colors.md).</span><span class="sxs-lookup"><span data-stu-id="dcc71-113">For a code example, see [Enumerating Colors](enumerating-colors.md).</span></span>

<span data-ttu-id="dcc71-114">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="dcc71-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="dcc71-115">Valores de cor</span><span class="sxs-lookup"><span data-stu-id="dcc71-115">Color Values</span></span>](color-values.md)
-   [<span data-ttu-id="dcc71-116">Aproximações de cores e pontilhamento</span><span class="sxs-lookup"><span data-stu-id="dcc71-116">Color Approximations and Dithering</span></span>](color-approximations-and-dithering.md)
-   [<span data-ttu-id="dcc71-117">Cor em bitmaps</span><span class="sxs-lookup"><span data-stu-id="dcc71-117">Color in Bitmaps</span></span>](color-in-bitmaps.md)
-   [<span data-ttu-id="dcc71-118">Mistura de cores</span><span class="sxs-lookup"><span data-stu-id="dcc71-118">Color Mixing</span></span>](color-mixing.md)

 

 



