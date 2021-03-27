---
description: O plano de fundo da janela é a cor ou o padrão usado para preencher a área do cliente antes que uma janela comece a desenhar.
ms.assetid: d0613f9b-e65b-4de2-887d-2b642d36b22d
title: Plano de fundo da janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d567b0bdc38866cd9332ff8ed399bfb23f53c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827990"
---
# <a name="window-background"></a>Plano de fundo da janela

O plano de fundo da janela é a cor ou o padrão usado para preencher a área do cliente antes que uma janela comece a desenhar. O plano de fundo da janela aborda qualquer coisa na tela antes que a janela fosse movida, apagando as imagens existentes e impedindo que a nova saída do aplicativo seja misturada com informações não relacionadas.

O sistema pinta o plano de fundo de uma janela ou dá à janela a oportunidade de fazer isso enviando uma mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) quando o aplicativo chama [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint). Se um aplicativo não processar a mensagem, mas a passar para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), o sistema apagará o plano de fundo preenchendo-o com o padrão no pincel de plano de fundo especificado pela classe da janela. Se o pincel não for válido ou se a classe não tiver um pincel de plano de fundo, o sistema definirá o membro **fErase** na estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) que **BeginPaint** retornará, mas não executará nenhuma outra ação. Em seguida, o aplicativo tem uma segunda chance de desenhar o plano de fundo da janela, se necessário.

Se ele processar o [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md), o aplicativo deverá usar o parâmetro *wParam* da mensagem para desenhar o plano de fundo. Esse parâmetro contém um identificador para o contexto do dispositivo de exibição para a janela. Depois de desenhar o plano de fundo, o aplicativo deve retornar um valor diferente de zero. Isso garante que o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) não defina erroneamente o membro **FErase** da estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) com um valor diferente de zero (indicando que o plano de fundo deve ser apagado) quando o aplicativo processar a mensagem de [**\_ pintura do WM**](wm-paint.md) subsequente.

Um aplicativo pode definir um pincel de plano de fundo de classe atribuindo uma alça de pincel ou um valor de cor do sistema ao membro **hbrBackground** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ao registrar a classe com a função [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . A função [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) ou [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) pode ser usada para criar uma alça de pincel. Um valor de cor do sistema pode ser um daqueles definidos para a função [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) . (O valor deve ser aumentado em um antes de ser atribuído ao membro).

Um aplicativo pode processar a mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) , embora um pincel de plano de fundo de classe seja definido. Isso é típico em aplicativos que permitem que o usuário altere a cor ou o padrão do plano de fundo da janela para uma janela especificada sem afetar outras janelas na classe. Nesses casos, o aplicativo não deve passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Não é necessário que um aplicativo alinhe pincéis, pois o sistema desenha o pincel usando a origem da janela como o ponto de referência. Considerando isso, o usuário pode mover a janela sem afetar o alinhamento dos pincéis de padrão.

 

 
