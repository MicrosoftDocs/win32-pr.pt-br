---
description: Antes de pintar, o sistema deve preparar o dispositivo de vídeo para operações de desenho.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Dispositivos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967677"
---
# <a name="display-devices"></a>Dispositivos de vídeo

Antes de pintar, o sistema deve preparar o dispositivo de vídeo para operações de desenho. Um contexto de dispositivo de vídeo define um conjunto de objetos gráficos e seus atributos associados e os modos gráficos que afetam a saída. O sistema prepara cada contexto de dispositivo de vídeo para saída para uma janela, definindo os objetos de desenho, as cores e os modos para a janela em vez do dispositivo de vídeo. Quando o aplicativo fornece o contexto do dispositivo de exibição por meio de chamadas para funções GDI, a GDI usa as informações no contexto para gerar a saída na janela especificada sem intrusão em outras janelas ou outras partes da tela.

O sistema fornece cinco tipos de contextos de dispositivo de exibição.



| Type                                           | Significado                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Common](common-display-device-contexts.md)   | Permite desenhar na área do cliente de uma janela especificada.                                                                                                        |
| [class](class-display-device-contexts.md)     | Permite desenhar na área do cliente de uma janela especificada.                                                                                                        |
| [parent](parent-display-device-contexts.md)   | Permite desenhar em qualquer lugar na janela. Embora o contexto do dispositivo pai também permita o desenho na janela pai, ele não se destina a ser usado dessa maneira. |
| [pessoal](private-display-device-contexts.md) | Permite desenhar na área do cliente de uma janela especificada.                                                                                                        |
| [Window](window-display-device-contexts.md)   | Permite desenhar em qualquer lugar na janela.                                                                                                                          |



 

O sistema fornece um contexto de dispositivo comum, classe, pai ou privado para uma janela com base no tipo de contexto de dispositivo de exibição especificado no estilo de classe dessa janela. O sistema fornece um contexto de dispositivo de janela somente quando o aplicativo solicita explicitamente um, por exemplo, chamando a função [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) . Em todos os casos, um aplicativo pode usar a função [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) para determinar qual janela um DC de exibição atualmente representa.

Esta seção fornece informações sobre os tópicos a seguir.

-   [Exibir cache de contexto do dispositivo](display-device-context-cache.md)
-   [Exibir padrões de contexto do dispositivo](display-device-context-defaults.md)
-   [Contextos de dispositivo de exibição comuns](common-display-device-contexts.md)
-   [Contextos de dispositivo de exibição particular](private-display-device-contexts.md)
-   [Os contextos do dispositivo de exibição pai](parent-display-device-contexts.md)
-   [A classe exibe contextos de dispositivo](class-display-device-contexts.md)
-   [Janela exibir contextos de dispositivo](window-display-device-contexts.md)
-   [Os contextos do dispositivo de exibição pai](parent-display-device-contexts.md)

 

 



