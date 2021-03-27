---
description: As funções a seguir são usadas com pintura e desenho.
ms.assetid: ec18323e-c13b-4328-83bf-9e4ed4a712b8
title: Funções de pintura e desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162ce40c88766a81320f72ea7c2e4a84dd92c478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967633"
---
# <a name="painting-and-drawing-functions"></a>Funções de pintura e desenho

As funções a seguir são usadas com pintura e desenho.



| Função                                       | Descrição                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)               | Prepara uma janela para pintura.                                                                             |
| [**DrawAnimatedRects**](/windows/desktop/api/Winuser/nf-winuser-drawanimatedrects) | Desenha um retângulo e o anima para indicar a atividade do ícone ou da janela.                                      |
| [**DrawCaption**](/windows/desktop/api/Winuser/nf-winuser-drawcaption)             | Desenha uma legenda de janela.                                                                                     |
| [**DrawEdge**](/windows/desktop/api/Winuser/nf-winuser-drawedge)                   | Desenha uma ou mais bordas do retângulo.                                                                       |
| [**DrawFocusRect**](/windows/desktop/api/Winuser/nf-winuser-drawfocusrect)         | Desenha um retângulo no estilo que indica que o retângulo tem o foco.                                  |
| [**DrawFrameControl**](/windows/desktop/api/Winuser/nf-winuser-drawframecontrol)   | Desenha um controle Frame.                                                                                      |
| [**Empatestate**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)                 | Exibe uma imagem e aplica um efeito visual para indicar um estado.                                          |
| [**DrawStateProc**](/windows/desktop/api/Winuser/nc-winuser-drawstateproc)         | Uma função de retorno de chamada que renderiza uma imagem complexa para [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea).                        |
| [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)                   | Marca o fim da pintura em uma janela.                                                                      |
| [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn)   | Impede o desenho em áreas inválidas de uma janela.                                                          |
| [**GdiFlush**](/windows/desktop/api/Wingdi/nf-wingdi-gdiflush)                   | Libera o lote atual do thread de chamada.                                                                 |
| [**GdiGetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdigetbatchlimit)   | Retorna o número máximo de chamadas de função que podem ser acumuladas no lote atual do thread de chamada. |
| [**GdiSetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdisetbatchlimit)   | Define o número máximo de chamadas de função que podem ser acumuladas no lote atual do thread de chamada.    |
| [**GetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor)               | Retorna a cor do plano de fundo de um contexto de dispositivo.                                                          |
| [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 | Retorna o modo de combinação em segundo plano para um contexto de dispositivo.                                                       |
| [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect)         | Obtém o retângulo delimitador acumulado para um contexto de dispositivo.                                               |
| [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     | Obtém o modo de combinação de primeiro plano de um contexto de dispositivo.                                                           |
| [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)         | Obtém as coordenadas do menor retângulo que inclui a região de atualização de uma janela.                 |
| [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)           | Obtém a região de atualização de uma janela.                                                                         |
| [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)             | Obtém o contexto do dispositivo para uma janela, incluindo barra de título, menus e barras de rolagem.                          |
| [**GetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgn)           | Obtém uma cópia da região da janela de uma janela.                                                               |
| [**GetWindowRgnBox**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgnbox)     | Obtém as dimensões do retângulo delimitador mais rígido da região da janela de uma janela.                   |
| [**Cinzastring**](/windows/desktop/api/Winuser/nf-winuser-graystringa)               | Desenha texto cinza em um local.                                                                              |
| [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)       | Adiciona um retângulo à região de atualização de uma janela.                                                               |
| [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn)         | Invalida a área do cliente dentro de uma região.                                                                |
| [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate)   | Desabilita ou habilita o desenho em uma janela.                                                                    |
| [**OutputProc**](/windows/desktop/api/Winuser/nc-winuser-graystringproc)               | Uma função de retorno de chamada usada com a função [**cinzentastring**](/windows/desktop/api/Winuser/nf-winuser-graystringa) . Ele é usado para desenhar uma cadeia de caracteres.   |
| [**PaintDesktop**](/windows/desktop/api/Winuser/nf-winuser-paintdesktop)           | Preenche a região de recorte em um contexto de dispositivo com um padrão.                                               |
| [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)           | Atualiza uma região na área do cliente da janela.                                                                 |
| [**SetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor)               | Define o plano de fundo como um valor de cor.                                                                       |
| [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 | Define o modo de combinação em segundo plano de um contexto de dispositivo.                                                           |
| [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect)         | Controla a acumulação de informações de retângulo delimitador para um contexto de dispositivo.                           |
| [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     | Define o modo de combinação de primeiro plano.                                                                               |
| [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)           | Define a região da janela de uma janela.                                                                         |
| [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)           | Atualiza a área do cliente de uma janela.                                                                        |
| [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect)           | Valida a área do cliente dentro de um retângulo.                                                               |
| [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn)             | Valida a área do cliente dentro de uma região.                                                                  |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)           | Retorna um identificador para a janela associada a um contexto de dispositivo.                                            |



 

 

 



