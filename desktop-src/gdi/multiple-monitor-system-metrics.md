---
description: A função GetSystemMetrics retorna valores para o monitor primário, exceto para SM \_ CXMAXTRACK e SM CYMAXTRACK, que se referem a \_ toda a área de trabalho.
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: Várias métricas do sistema de monitoramento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3143562116561bb220bc6f0b5ecfa4ad8f5103c3e4532cab639c4c2b37f59467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037704"
---
# <a name="multiple-monitor-system-metrics"></a>Várias métricas do sistema de monitoramento

A [**função GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) retorna valores para o monitor primário, exceto para SM \_ CXMAXTRACK e SM CYMAXTRACK, que se referem a \_ toda a área de trabalho. As métricas a seguir são as mesmas para todos os drivers de dispositivo: SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON. Os seguintes recursos de exibição são os mesmos para todos os monitores: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.

[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) também tem constantes que se referem apenas a um sistema de Vários Monitores. SM SEMPRERTUALSCREEN e SM YVIRTUALSCREEN identificam o canto superior esquerdo da tela \_ \_ virtual, SM CXVIRTUALSCREEN e SM CYVIRTUALSCREEN são as medidas verticais e horizontais da tela virtual, SM CMONITORS é o número de monitores anexados à área de trabalho e \_ \_ \_ SM \_ SAMEDISPLAYFORMAT indica se todos os monitores na área de trabalho têm o mesmo formato de cor.

Para obter informações sobre um único monitor de exibição ou todos os monitores de exibição em uma área de trabalho, use EnumDisplayMonitors. O retângulo da janela da área de trabalho retornado por [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) ou [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) é sempre igual ao retângulo do monitor primário, para compatibilidade com aplicativos existentes. Portanto, o resultado de


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



Para alterar a área de trabalho de um monitor, chame [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com SPI \_ SETWORKAREA e *pvParam* apontando para uma estrutura [**RECT**](/previous-versions//dd162897(v=vs.85)) que está no monitor desejado. Se *pvParam* for **NULL,** a área de trabalho do monitor primário será modificada. Usar SPI \_ GETWORKAREA sempre retorna a área de trabalho do monitor primário. Para obter a área de trabalho de um monitor diferente do monitor primário, chame [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).

 

 
