---
description: Quase todos os aplicativos usam a tela para exibir os dados que manipulam.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: Sobre pintura e desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988778"
---
# <a name="about-painting-and-drawing"></a>Sobre pintura e desenho

Quase todos os aplicativos usam a tela para exibir os dados que manipulam. Um aplicativo pinta imagens, desenha figuras e grava o texto para que o usuário possa exibir os dados conforme eles são criados, editados e impressos. O Microsoft Windows fornece suporte avançado para pintura e desenho, mas, devido à natureza dos sistemas operacionais multitarefas, os aplicativos devem cooperar uns com os outros ao acessar a tela.

Para manter todos os aplicativos funcionando de forma tranqüila e cooperativa, o sistema gerencia toda a saída para a tela. Os aplicativos usam o Windows como seu dispositivo de saída primário, em vez da própria tela. O sistema fornece contextos de dispositivo que correspondem exclusivamente às janelas. Os aplicativos usam contextos de dispositivo de exibição para direcionar sua saída para o Windows especificado. O desenho em uma janela (direcionamento de saída para ela) impede que um aplicativo interfira na saída de outros aplicativos e permite que os aplicativos coexistam uns com os outros, ao mesmo tempo em que aproveitam ao máximo os recursos gráficos do sistema.

-   [Quando desenhar em uma janela](when-to-draw-in-a-window.md)
-   [A mensagem do WM \_ Paint](the-wm-paint-message.md)
-   [Desenho sem a mensagem de pintura do WM \_](drawing-without-the-wm-paint-message.md)
-   [Sistema de coordenadas da janela](window-coordinate-system.md)
-   [Regiões da janela](window-regions.md)
-   [Plano de fundo da janela](window-background.md)
-   [Janelas minimizadas](minimized-windows.md)
-   [Janelas redimensionadas](resized-windows.md)
-   [Área não cliente](nonclient-area.md)
-   [Região de atualização da janela filho](child-window-update-region.md)
-   [Dispositivos de vídeo](display-devices.md)
-   [Bloqueio de atualização de janela](window-update-lock.md)
-   [Retângulo delimitador acumulado](accumulated-bounding-rectangle.md)

 

 



