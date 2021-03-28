---
description: A função GetSystemMetrics retorna valores para o monitor primário, exceto para SM \_ CXMAXTRACK e SM \_ CYMAXTRACK, que se referem a toda a área de trabalho.
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: Várias métricas do sistema de monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f4da5c687df28817105e1ec3876ffd1ab5649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091174"
---
# <a name="multiple-monitor-system-metrics"></a><span data-ttu-id="9df1a-103">Várias métricas do sistema de monitor</span><span class="sxs-lookup"><span data-stu-id="9df1a-103">Multiple Monitor System Metrics</span></span>

<span data-ttu-id="9df1a-104">A função [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) retorna valores para o monitor primário, exceto para SM \_ CXMAXTRACK e SM \_ CYMAXTRACK, que se referem a toda a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9df1a-104">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function returns values for the primary monitor, except for SM\_CXMAXTRACK and SM\_CYMAXTRACK, which refer to the entire desktop.</span></span> <span data-ttu-id="9df1a-105">As métricas a seguir são as mesmas para todos os drivers de dispositivo: SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON.</span><span class="sxs-lookup"><span data-stu-id="9df1a-105">The following metrics are the same for all device drivers: SM\_CXCURSOR, SM\_CYCURSOR, SM\_CXICON, SMCYICON.</span></span> <span data-ttu-id="9df1a-106">Os seguintes recursos de exibição são os mesmos para todos os monitores: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.</span><span class="sxs-lookup"><span data-stu-id="9df1a-106">The following display capabilities are the same for all monitors: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.</span></span>

<span data-ttu-id="9df1a-107">O [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) também tem constantes que se referem apenas a um sistema de vários monitores.</span><span class="sxs-lookup"><span data-stu-id="9df1a-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) also has constants that refer only to a Multiple Monitor system.</span></span> <span data-ttu-id="9df1a-108">SM \_ XVIRTUALSCREEN e SM \_ YVIRTUALSCREEN identificam o canto superior esquerdo da tela virtual, SM \_ CXVIRTUALSCREEN e SM \_ CYVIRTUALSCREEN são as medidas vertical e horizontal da tela virtual, SM \_ CMONITORS é o número de monitores anexados à área de trabalho e SM \_ SAMEDISPLAYFORMAT indica se todos os monitores na área de trabalho têm o mesmo formato de cor.</span><span class="sxs-lookup"><span data-stu-id="9df1a-108">SM\_XVIRTUALSCREEN and SM\_YVIRTUALSCREEN identify the upper-left corner of the virtual screen, SM\_CXVIRTUALSCREEN and SM\_CYVIRTUALSCREEN are the vertical and horizontal measurements of the virtual screen, SM\_CMONITORS is the number of monitors attached to the desktop, and SM\_SAMEDISPLAYFORMAT indicates whether all the monitors on the desktop have the same color format.</span></span>

<span data-ttu-id="9df1a-109">Para obter informações sobre um único monitor de exibição ou todos os monitores de exibição em uma área de trabalho, use EnumDisplayMonitors.</span><span class="sxs-lookup"><span data-stu-id="9df1a-109">To get information about a single display monitor or all of the display monitors in a desktop, use EnumDisplayMonitors.</span></span> <span data-ttu-id="9df1a-110">O retângulo da janela da área de trabalho retornado por [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) ou [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) é sempre igual ao retângulo do monitor primário, para compatibilidade com os aplicativos existentes.</span><span class="sxs-lookup"><span data-stu-id="9df1a-110">The rectangle of the desktop window returned by [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) or [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) is always equal to the rectangle of the primary monitor, for compatibility with existing applications.</span></span> <span data-ttu-id="9df1a-111">Assim, o resultado de</span><span class="sxs-lookup"><span data-stu-id="9df1a-111">Thus, the result of</span></span>


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



<span data-ttu-id="9df1a-112">será:</span><span class="sxs-lookup"><span data-stu-id="9df1a-112">will be:</span></span>


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



<span data-ttu-id="9df1a-113">Para alterar a área de trabalho de um monitor, chame [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com SPI \_ SETWORKAREA e *pvParam* apontando para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que esteja no monitor desejado.</span><span class="sxs-lookup"><span data-stu-id="9df1a-113">To change the work area of a monitor, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETWORKAREA and *pvParam* pointing to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that is on the desired monitor.</span></span> <span data-ttu-id="9df1a-114">Se *pvParam* for **NULL**, a área de trabalho do monitor primário será modificada.</span><span class="sxs-lookup"><span data-stu-id="9df1a-114">If *pvParam* is **NULL**, the work area of the primary monitor is modified.</span></span> <span data-ttu-id="9df1a-115">Usar SPI \_ GETWORKAREA sempre retorna a área de trabalho do monitor primário.</span><span class="sxs-lookup"><span data-stu-id="9df1a-115">Using SPI\_GETWORKAREA always returns the work area of the primary monitor.</span></span> <span data-ttu-id="9df1a-116">Para obter a área de trabalho de um monitor diferente do monitor primário, chame [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span><span class="sxs-lookup"><span data-stu-id="9df1a-116">To get the work area of a monitor other than the primary monitor, call [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span>

 

 
