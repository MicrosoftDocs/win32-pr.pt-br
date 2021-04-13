---
description: Ao usar vários monitores como exibições independentes, a área de trabalho contém uma exibição ou um conjunto de exibições.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Usando monitores múltiplos como exibições independentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4761e0e04ae1adaa197b06f04fa36c61ccda3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968139"
---
# <a name="using-multiple-monitors-as-independent-displays"></a><span data-ttu-id="dd825-103">Usando monitores múltiplos como exibições independentes</span><span class="sxs-lookup"><span data-stu-id="dd825-103">Using Multiple Monitors as Independent Displays</span></span>

<span data-ttu-id="dd825-104">Ao usar vários monitores como exibições independentes, a área de trabalho contém uma exibição ou um conjunto de exibições.</span><span class="sxs-lookup"><span data-stu-id="dd825-104">When using multiple monitors as independent displays, the desktop contains one display or set of displays.</span></span> <span data-ttu-id="dd825-105">Esse conjunto de exibições sempre inclui o monitor primário e se comporta conforme mencionado nas outras seções deste tópico.</span><span class="sxs-lookup"><span data-stu-id="dd825-105">This set of displays always includes the primary monitor and behaves as mentioned in the other sections of this topic.</span></span> <span data-ttu-id="dd825-106">Um aplicativo pode usar qualquer outro monitor como uma exibição independente.</span><span class="sxs-lookup"><span data-stu-id="dd825-106">An application can use any other monitor as an independent display.</span></span>

> [!Note]  
> <span data-ttu-id="dd825-107">O uso de outros monitores como exibições independentes não tem suporte em drivers que são implementados para o WDDM (Windows Display Driver Model).</span><span class="sxs-lookup"><span data-stu-id="dd825-107">Using other monitors as independent displays isn't supported on drivers that are implemented to the Windows Display Driver Model (WDDM).</span></span>

 

<span data-ttu-id="dd825-108">O Gerenciador de janelas não sabe nada sobre as exibições independentes.</span><span class="sxs-lookup"><span data-stu-id="dd825-108">The window manager knows nothing about the independent displays.</span></span> <span data-ttu-id="dd825-109">Eles são totalmente controlados pelo aplicativo e nenhuma função do Gerenciador de janelas está disponível para o aplicativo (todas as chamadas do Gerenciador de janelas vão automaticamente para a exibição primária).</span><span class="sxs-lookup"><span data-stu-id="dd825-109">They are completely controlled by the application, and no window manager functions are available to the application (all window manager calls automatically go to the primary display).</span></span> <span data-ttu-id="dd825-110">Cada exibição independente tem sua própria origem e coordenadas horizontais e verticais, e é acessada por meio das funções GDI, como [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) ou as funções do DirectX, como **DirectDrawCreate**.</span><span class="sxs-lookup"><span data-stu-id="dd825-110">Each independent display has its own origin and horizontal and vertical coordinates, and is accessed through the GDI functions such as [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) or the DirectX functions such as **DirectDrawCreate**.</span></span>

<span data-ttu-id="dd825-111">Para localizar as exibições independentes, chame [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) e procure o sinalizador exibições que não têm o \_ dispositivo de vídeo \_ anexado \_ ao \_ Desktop na estrutura do [**\_ dispositivo de vídeo**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .</span><span class="sxs-lookup"><span data-stu-id="dd825-111">To locate the independent displays, call [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and look for the displays that do not have DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span>

<span data-ttu-id="dd825-112">Um aplicativo pode abrir uma exibição chamando</span><span class="sxs-lookup"><span data-stu-id="dd825-112">An application can open a display by calling</span></span>


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



<span data-ttu-id="dd825-113">Nesta chamada, o parâmetro *lpszDisplayName* é um dos nomes de dispositivo retornados por [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) e *lpDevMode* é uma descrição do modo gráfico para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd825-113">In this call, the *lpszDisplayName* parameter is one of the device names returned by [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and *lpDevMode* is a description of the graphics mode for this device.</span></span> <span data-ttu-id="dd825-114">O HDC resultante pode ser usado para executar qualquer operação de gráficos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd825-114">The resulting hdc can be used to perform any graphics operation to the device.</span></span>

 

 



