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
# <a name="multiple-monitor-system-metrics"></a>Várias métricas do sistema de monitor

A função [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) retorna valores para o monitor primário, exceto para SM \_ CXMAXTRACK e SM \_ CYMAXTRACK, que se referem a toda a área de trabalho. As métricas a seguir são as mesmas para todos os drivers de dispositivo: SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON. Os seguintes recursos de exibição são os mesmos para todos os monitores: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.

O [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) também tem constantes que se referem apenas a um sistema de vários monitores. SM \_ XVIRTUALSCREEN e SM \_ YVIRTUALSCREEN identificam o canto superior esquerdo da tela virtual, SM \_ CXVIRTUALSCREEN e SM \_ CYVIRTUALSCREEN são as medidas vertical e horizontal da tela virtual, SM \_ CMONITORS é o número de monitores anexados à área de trabalho e SM \_ SAMEDISPLAYFORMAT indica se todos os monitores na área de trabalho têm o mesmo formato de cor.

Para obter informações sobre um único monitor de exibição ou todos os monitores de exibição em uma área de trabalho, use EnumDisplayMonitors. O retângulo da janela da área de trabalho retornado por [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) ou [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) é sempre igual ao retângulo do monitor primário, para compatibilidade com os aplicativos existentes. Assim, o resultado de


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



será:


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



Para alterar a área de trabalho de um monitor, chame [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com SPI \_ SETWORKAREA e *pvParam* apontando para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que esteja no monitor desejado. Se *pvParam* for **NULL**, a área de trabalho do monitor primário será modificada. Usar SPI \_ GETWORKAREA sempre retorna a área de trabalho do monitor primário. Para obter a área de trabalho de um monitor diferente do monitor primário, chame [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).

 

 
