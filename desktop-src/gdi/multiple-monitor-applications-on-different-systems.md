---
description: Para que seu aplicativo monitoraware múltiplo funcione em sistemas com e sem suporte a vários monitores, vincule seu aplicativo com Multimon.h.
ms.assetid: 8667305e-ca76-49cb-878e-07814431e6db
title: Vários aplicativos monitor em sistemas diferentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c597261063f49b6e6856576e3528698291348afb2b8478d854a824b92d2cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037714"
---
# <a name="multiple-monitor-applications-on-different-systems"></a>Vários aplicativos monitor em sistemas diferentes

Para que seu aplicativo monitoraware múltiplo funcione em sistemas com e sem suporte a vários monitores, vincule seu aplicativo com Multimon.h. Você também deve definir COMPILE \_ MULTIMON \_ STUBS em exatamente um arquivo C. Se o sistema não dá suporte a vários monitores, isso retorna valores padrão de [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) e as várias funções de monitor atuam como se houvesse apenas uma exibição. Em vários sistemas de monitor, seu aplicativo funcionará normalmente.

Como as coordenadas negativas podem ocorrer facilmente em um sistema multimonitor, você deve recuperar coordenadas que são empacotadas no lParam usando as macros **GET \_ X \_ LPARAM** e **GET Y \_ \_ LPARAM.**

Não use coordenadas negativas ou coordenadas maiores que SM \_ CXSCREEN e SM \_ CYSCREEN para ocultar uma janela. Windows que usam esses limites para ocultar podem aparecer em outro monitor. Da mesma forma, não use esses limites para manter uma janela visível porque isso pode fazer com que uma janela se encaixe no monitor primário. É melhor reexaminar aplicativos existentes para esses problemas. No entanto, você pode minimizar problemas em aplicativos existentes executando o aplicativo no monitor primário ou mantendo o monitor primário no canto superior esquerdo da tela virtual.

Observe que SM \_ CXMAXTRACK e SM CYMAXTRACK são definidos para a \_ área de trabalho, não apenas um monitor. Windows usar esses limites pode precisar ser redefinido.

Uma janela pai ou relacionada pode não estar no mesmo monitor que uma janela filho. Para localizar o monitor de uma janela, os aplicativos devem usar a [**função MonitorFromWindow.**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)

Para que uma economia de tela seja exibida em todos os monitores, vincule com a versão mais recente do Scrnsave.lib. Caso contrário, a economia de tela só poderá aparecer no monitor primário e deixar os outros monitores inalterados. As economias de tela vinculadas ao Scrnsave.lib mais recente funcionarão em sistemas de monitor único e múltiplo. Para ter uma economia de tela diferente em cada monitor, use as várias funções de monitor para lidar com cada monitor separadamente.

Dispositivos de entrada que entregam coordenadas para o sistema em coordenadas absolutas, como tablets, têm sua entrada de cursor restrita ao monitor primário. Para alternar a entrada do tablet entre monitores, consulte as instruções do OEM.

Para mapear a entrada do mouse enviada em coordenadas absolutas para toda a tela virtual, use a estrutura [**INPUT**](/windows/win32/api/winuser/ns-winuser-input) com MOUSEEVENTF ABSOLUTE e \_ MOUSEEVENTF \_ VIRTUALDESKTOP.

A [**função BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) funciona bem para vários sistemas de monitor. No entanto, as funções [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt), [**PlgBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)e [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) falharão se os contextos do dispositivo de origem e de destino são diferentes.

 

 
