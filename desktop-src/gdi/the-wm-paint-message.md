---
description: Normalmente, um aplicativo desenha em uma janela em resposta a uma mensagem do WM \_ Paint.
ms.assetid: b2317ce9-e775-450e-91f5-00f735f256a3
title: A mensagem de WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138913771621699abb27d4f5648e732b21a607ff5466ec4766726ab278d46fed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965176"
---
# <a name="the-wm_paint-message"></a>A mensagem do WM \_ Paint

Normalmente, um aplicativo desenha em uma janela em resposta a uma mensagem do [**WM \_ Paint**](wm-paint.md) . O sistema envia essa mensagem a um procedimento de janela quando as alterações na janela alteram o conteúdo da área do cliente. O sistema enviará a mensagem somente se não houver nenhuma outra mensagem na fila de mensagens do aplicativo.

Ao receber uma mensagem de [**\_ pintura do WM**](wm-paint.md) , um aplicativo pode chamar [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) para recuperar o contexto do dispositivo de vídeo para a área do cliente e usá-lo em chamadas para funções GDI para realizar todas as operações de desenho necessárias para atualizar a área do cliente. Depois de concluir as operações de desenho, o aplicativo chama a função [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para liberar o contexto do dispositivo de vídeo.

Antes de [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) retornar o contexto do dispositivo de vídeo, o sistema prepara o contexto do dispositivo para a janela especificada. Ele primeiro define a região de recorte para que o contexto do dispositivo seja igual à interseção da parte da janela que precisa de atualização e da parte visível para o usuário. Somente as partes da janela que foram alteradas são redesenhadas. As tentativas de desenhar fora desta região são recortadas e não aparecem na tela.

O sistema também pode enviar mensagens do [**WM \_ NCPAINT**](wm-ncpaint.md) e do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) para o procedimento de janela antes de [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) retornar. Essas mensagens direcionam o aplicativo para desenhar a área não cliente e o plano de fundo da janela. A *área não cliente* é a parte de uma janela que está fora da área do cliente. A área inclui recursos como a barra de título, o menu janela (também conhecido como menu do **sistema** ) e as barras de rolagem. A maioria dos aplicativos depende da função de janela padrão, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), para desenhar essa área e, portanto, passar a mensagem do **WM \_ NCPAINT** para essa função. O *plano de fundo da janela* é a cor ou o padrão em que uma janela é preenchida antes de outras operações de desenho começarem. O plano de fundo aborda todas as imagens anteriormente na janela ou na tela na janela. Se uma janela pertencer a uma classe de janela que tem um pincel de plano de fundo de classe, a função **DefWindowProc** desenhará o plano de fundo da janela automaticamente.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) preenche uma estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) com informações como as dimensões da parte da janela a ser atualizada e um sinalizador que indica se o plano de fundo da janela foi desenhado. O aplicativo pode usar essas informações para otimizar o desenho. Por exemplo, ele pode usar as dimensões da região de atualização, especificada pelo membro **rcPaint** , para limitar o desenho apenas às partes da janela que precisam de atualização. Se um aplicativo tiver uma saída muito simples, ele poderá ignorar a região de atualização e desenhar em toda a janela, contando com o sistema para descartar (cortar) qualquer saída desnecessária. Como o sistema corta o desenho que se estende fora da região de recorte, apenas o desenho que está na região de atualização fica visível.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) define a região de atualização de uma janela como **nula**. Isso limpa a região, impedindo que ela gere mensagens subsequentes do [**WM \_ Paint**](wm-paint.md) . Se um aplicativo processa uma mensagem do **WM \_ Paint** , mas não chama **BeginPaint** ou, caso contrário, limpa a região de atualização, o aplicativo continua a receber mensagens do **WM \_ Paint** , desde que a região não esteja vazia. Em todos os casos, um aplicativo deve limpar a região de atualização antes de retornar da mensagem do **WM \_ Paint** .

Depois que o aplicativo termina de desenhar, ele deve chamar [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint). Para a maioria das janelas, o **Endpainte** libera o contexto do dispositivo de vídeo, disponibilizando-o para outras janelas. **EndPaint** também mostra o cursor, se ele foi anteriormente ocultado por [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint). **BeginPaint** oculta o cursor para impedir que as operações de desenho corrompam.

-   [A região de atualização](the-update-region.md)
-   [Invalidando e validando a região de atualização](invalidating-and-validating-the-update-region.md)
-   [Recuperando a região de atualização](retrieving-the-update-region.md)
-   [Excluindo a região de atualização](excluding-the-update-region.md)
-   [Desenho síncrono e assíncrono](synchronous-and-asynchronous-drawing.md)

 

 
