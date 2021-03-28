---
description: O sistema envia uma \_ mensagem NCPAINT do WM para a janela sempre que uma parte da área não cliente da janela, como a barra de título, barra de menus ou quadro de janela, deve ser atualizada.
ms.assetid: e4dc61f3-6a9f-4ed4-8685-62eb4ceb85f1
title: Área não cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51da31709f5bd9326cc0d05a9e37e2df78bfbb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165063"
---
# <a name="nonclient-area"></a>Área não cliente

O sistema envia uma [**mensagem \_ NCPAINT do WM**](wm-ncpaint.md) para a janela sempre que uma parte da área não cliente da janela, como a barra de título, barra de menus ou quadro de janela, deve ser atualizada. O sistema também pode enviar outras mensagens para direcionar uma janela para atualizar uma parte de sua área de cliente; por exemplo, quando uma janela se torna ativa ou inativa, ela envia a mensagem do [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) para atualizar sua barra de título. Em geral, o processamento dessas mensagens para o Windows padrão não é recomendado, pois o aplicativo deve ser capaz de desenhar todas as partes necessárias da área não cliente para a janela. Por esse motivo, a maioria dos aplicativos passa essas mensagens para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para o processamento padrão.

Um aplicativo que cria áreas não cliente personalizadas para suas janelas deve processar essas mensagens. Ao fazer isso, o aplicativo deve usar um contexto de dispositivo de janela para executar o desenho na janela. O *contexto do dispositivo de janela* permite que o aplicativo desenhe em todas as partes da janela, incluindo a área não cliente. Um aplicativo recupera um contexto de dispositivo de janela usando a função [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e, quando o desenho é concluído, deve liberar o contexto do dispositivo de janela usando a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) .

O sistema mantém uma região de atualização para a área que não é cliente. Quando um aplicativo recebe uma mensagem do [**WM \_ NCPAINT**](wm-ncpaint.md) , o parâmetro *wParam* contém um identificador para uma região que define as dimensões da região de atualização. O aplicativo pode usar o identificador para combinar a região de atualização com a região de recorte para o contexto do dispositivo de janela. O sistema não combina automaticamente a região de atualização ao recuperar o contexto do dispositivo de janela, a menos que o aplicativo use [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e especifique o identificador de região e o sinalizador de INTERSECTRGN do DCX \_ . Se o aplicativo não combinar a região de atualização, apenas as operações de desenho que, de outra forma, se estenderão fora da janela serão recortadas. O aplicativo não é responsável por limpar a região de atualização, independentemente de usar a região.

Se um aplicativo processar a [**mensagem \_ NCACTIVATE do WM**](../winmsg/wm-ncactivate.md) , depois de processá-la deverá retornar **true** para instruir o sistema a concluir a alteração da janela ativa. Se a janela for minimizada quando o aplicativo receber a **mensagem \_ NCACTIVATE do WM** , ela deverá passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Nesses casos, a função padrão redesenha o rótulo para o ícone.

 

 
