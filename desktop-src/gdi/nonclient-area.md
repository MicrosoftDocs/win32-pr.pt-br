---
description: O sistema envia uma mensagem WM NCPAINT para a janela sempre que uma parte da área não dependente da janela, como a barra de título, a barra de menus ou o quadro da janela, deve \_ ser atualizada.
ms.assetid: e4dc61f3-6a9f-4ed4-8685-62eb4ceb85f1
title: Área nonclient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a20593063af4382e79697b249324ba0fd6fe2782d903b645a2b80c25c63c436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698735"
---
# <a name="nonclient-area"></a>Área nonclient

O sistema envia uma mensagem [**\_ WM NCPAINT**](wm-ncpaint.md) para a janela sempre que uma parte da área não dependente da janela, como a barra de título, a barra de menus ou o quadro da janela, deve ser atualizada. O sistema também pode enviar outras mensagens para direcionar uma janela para atualizar uma parte de sua área de cliente; por exemplo, quando uma janela se torna ativa ou inativa, ela envia a mensagem [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) para atualizar sua barra de título. Em geral, o processamento dessas mensagens para janelas padrão não é recomendado, porque o aplicativo deve ser capaz de desenhar todas as partes necessárias da área não dependente para a janela. Por esse motivo, a maioria dos aplicativos passa essas mensagens para [**DefWindowProc para**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processamento padrão.

Um aplicativo que cria áreas não dependentes personalizadas para suas janelas deve processar essas mensagens. Ao fazer isso, o aplicativo deve usar um contexto de dispositivo de janela para executar o desenho na janela. O *contexto do dispositivo de* janela permite que o aplicativo desenhe em todas as partes da janela, incluindo a área não dependente. Um aplicativo recupera um contexto de dispositivo de janela usando a função [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e, quando o desenho é concluído, deve liberar o contexto do dispositivo de janela usando a [**função ReleaseDC.**](/windows/desktop/api/Winuser/nf-winuser-releasedc)

O sistema mantém uma região de atualização para a área não dependente. Quando um aplicativo recebe uma mensagem [**WM \_ NCPAINT,**](wm-ncpaint.md) o parâmetro *wParam* contém um handle para uma região que define as dimensões da região de atualização. O aplicativo pode usar o handle para combinar a região de atualização com a região de recorte para o contexto do dispositivo de janela. O sistema não combina automaticamente a região de atualização ao recuperar o contexto do dispositivo de janela, a menos que o aplicativo use [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e especifique o handle de região e o sinalizador \_ INTERSECTRGN DCX. Se o aplicativo não combinar a região de atualização, somente as operações de desenho que se estenderiam para fora da janela serão recortados. O aplicativo não é responsável por limpar a região de atualização, independentemente de usar a região.

Se um aplicativo processar a [**mensagem WM \_ NCACTIVATE,**](../winmsg/wm-ncactivate.md) após o processamento, ele deverá retornar **TRUE** para direcionar o sistema para concluir a alteração da janela ativa. Se a janela for minimizada quando o aplicativo receber a mensagem **WM \_ NCACTIVATE,** ela deverá passar a mensagem para [**DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Nesses casos, a função padrão redesenha o rótulo para o ícone.

 

 
