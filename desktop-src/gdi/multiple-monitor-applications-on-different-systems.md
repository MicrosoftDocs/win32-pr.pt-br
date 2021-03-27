---
description: Para que seu aplicativo de vários monitoraware funcione em sistemas com e sem suporte de monitor múltiplo, vincule seu aplicativo com Multimon. h.
ms.assetid: 8667305e-ca76-49cb-878e-07814431e6db
title: Vários aplicativos de monitor em sistemas diferentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5d470861136ac9362d986b8647c86abee7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967644"
---
# <a name="multiple-monitor-applications-on-different-systems"></a>Vários aplicativos de monitor em sistemas diferentes

Para que seu aplicativo de vários monitoraware funcione em sistemas com e sem suporte de monitor múltiplo, vincule seu aplicativo com Multimon. h. Você também deve definir os \_ \_ stubs de MULTIMON de compilação em exatamente um arquivo C. Se o sistema não oferecer suporte a vários monitores, isso retornará valores padrão de [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) e as várias funções de monitor agirão como se houver apenas uma exibição. Em vários sistemas de monitor, seu aplicativo funcionará normalmente.

Como as coordenadas negativas podem ocorrer facilmente em um sistema de multimonitoring, você deve recuperar as coordenadas que estão incluídas no lParam usando as macros **Get \_ X \_ lParam** e **Get \_ Y \_ lParam** .

Não use coordenadas negativas ou coordenadas maiores que SM \_ CXSCREEN e SM \_ CYSCREEN para ocultar uma janela. As janelas que usam esses limites para ocultar podem aparecer em outro monitor. Da mesma forma, não use esses limites para manter uma janela visível, pois isso pode fazer com que uma janela se ajuste ao monitor primário. É melhor reexaminar os aplicativos existentes para esses problemas. No entanto, você pode minimizar problemas em aplicativos existentes executando o aplicativo no monitor primário ou mantendo o monitor primário no canto superior esquerdo da tela virtual.

Observe que SM \_ CXMAXTRACK e SM \_ CYMAXTRACK são definidos para a área de trabalho, não apenas um monitor. Talvez seja necessário redefinir o Windows usando esses limites.

Uma janela pai ou relacionada pode não estar no mesmo monitor que uma janela filho. Para localizar o monitor de uma janela, os aplicativos devem usar a função [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) .

Para que uma proteção de tela seja exibida em todos os monitores, vincule com a versão mais recente de SCRNSAVE. lib. Caso contrário, a proteção de tela só poderá aparecer no monitor primário e deixar os outros monitores inalterados. As proteções de tela vinculadas com o SCRNSAVE. lib mais recente funcionarão em sistemas de monitor únicos e múltiplos. Para ter uma proteção de tela diferente em cada monitor, use as várias funções de monitor para lidar com cada monitor separadamente.

Os dispositivos de entrada que fornecem coordenadas para o sistema em coordenadas absolutas, como tablets, têm a entrada do cursor restrita ao monitor primário. Para alternar a entrada de Tablet entre monitores, consulte as instruções do OEM.

Para mapear a entrada do mouse que é enviada em coordenadas absolutas para toda a tela virtual, use a estrutura de [**entrada**](/windows/win32/api/winuser/ns-winuser-input) com MOUSEEVENTF \_ Absolute e MOUSEEVENTF \_ VIRTUALDESKTOP.

A função [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) funciona bem para vários sistemas de monitor. No entanto, as funções [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt), [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt), [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)e [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) falharão se os contextos do dispositivo de origem e de destino forem diferentes.

 

 
