---
description: 'Um aplicativo desenha uma janela em uma variedade de vezes: ao criar uma janela pela primeira vez, ao alterar o tamanho da janela, ao mover a janela por trás de outra janela, ao minimizar ou maximizar a janela, ao exibir dados de um arquivo aberto e ao rolar, alterar ou selecionar uma parte dos dados exibidos.'
ms.assetid: 4b5d6842-5707-4884-a55a-e09e342cea46
title: Quando desenhar em uma janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42c8c157de5a591be5ad1a6ad3e319cf83220e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296676"
---
# <a name="when-to-draw-in-a-window"></a>Quando desenhar em uma janela

Um aplicativo desenha uma janela em uma variedade de vezes: ao criar uma janela pela primeira vez, ao alterar o tamanho da janela, ao mover a janela por trás de outra janela, ao minimizar ou maximizar a janela, ao exibir dados de um arquivo aberto e ao rolar, alterar ou selecionar uma parte dos dados exibidos.

O sistema gerencia ações como mover e dimensionar uma janela. Se uma ação afetar o conteúdo da janela, o sistema marcará a parte afetada da janela como pronta para atualização e, na próxima oportunidade, enviará uma mensagem de [**\_ pintura do WM**](wm-paint.md) para o procedimento de janela da janela. A mensagem é um sinal para o aplicativo determinar o que deve ser atualizado e para realizar o desenho necessário.

Algumas ações são gerenciadas pelo aplicativo, como exibir arquivos abertos e selecionar dados exibidos. Para essas ações, um aplicativo pode marcar para atualizar a parte da janela afetada pela ação, fazendo com que uma mensagem de [**\_ pintura do WM**](wm-paint.md) seja enviada na próxima oportunidade. Se uma ação exigir comentários imediatos, o aplicativo poderá ser desenhado enquanto a ação ocorrer, sem esperar pelo **WM \_ Paint**. Por exemplo, um aplicativo típico realça a área que o usuário seleciona em vez de aguardar a próxima mensagem de **\_ pintura do WM** para atualizar a área.

Em todos os casos, um aplicativo pode desenhar em uma janela assim que é criado. Para desenhar na janela, o aplicativo deve primeiro recuperar um identificador para um contexto de dispositivo de exibição para a janela. O ideal é que um aplicativo execute a maioria de suas operações de desenho durante o processamento de mensagens de [**\_ pintura do WM**](wm-paint.md) . Nesse caso, o aplicativo recupera um contexto de dispositivo de exibição chamando a função [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) . Se um aplicativo desenhar em qualquer outro momento, como de dentro de [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) ou durante o processamento de mensagens de teclado ou mouse, ele chamará a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para recuperar o DC de vídeo.

 

 
