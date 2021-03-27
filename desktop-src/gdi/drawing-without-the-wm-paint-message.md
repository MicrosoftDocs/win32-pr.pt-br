---
description: Embora os aplicativos realizem a maioria das operações de desenho enquanto a mensagem do WM \_ Paint está processando, às vezes é mais eficiente para um aplicativo desenhar diretamente em uma janela sem depender da mensagem do WM \_ Paint.
ms.assetid: 2d015879-58d2-4cbe-b1cc-445f2e8fd316
title: Desenho sem a mensagem de WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66695e85b700de6f62366dedb6fe082f410d4385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827653"
---
# <a name="drawing-without-the-wm_paint-message"></a>Desenho sem a mensagem de pintura do WM \_

Embora os aplicativos realizem a maioria das operações de desenho enquanto a mensagem do [**WM \_ Paint**](wm-paint.md) está processando, às vezes é mais eficiente para um aplicativo desenhar diretamente em uma janela sem depender da mensagem do **WM \_ Paint** . Isso pode ser útil quando o usuário precisa de comentários imediatos, como ao selecionar texto e arrastar ou dimensionar um objeto. Nesses casos, o aplicativo geralmente é desenhado durante o processamento de mensagens de teclado ou mouse.

Para desenhar em uma janela sem usar uma mensagem do [**WM \_ Paint**](wm-paint.md) , o aplicativo usa a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para recuperar um contexto de dispositivo de exibição para a janela. Com o contexto do dispositivo de vídeo, o aplicativo pode desenhar na janela e evitar o intrusão em outras janelas. Quando o desenho do aplicativo termina, ele chama a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) para liberar o contexto do dispositivo de vídeo para uso por outros aplicativos.

Ao desenhar sem usar uma mensagem do [**WM \_ Paint**](wm-paint.md) , o aplicativo geralmente não invalida a janela. Em vez disso, ele se baseia em tal maneira de poder restaurar facilmente a janela e remover o desenho. Por exemplo, quando o usuário seleciona texto ou um objeto, o aplicativo normalmente desenha a seleção invertendo o que já está na janela. O aplicativo pode remover a seleção e restaurar o conteúdo original da janela simplesmente invertendo.

O aplicativo é responsável por gerenciar cuidadosamente as alterações feitas na janela. Em particular, se um aplicativo desenhar uma seleção e uma mensagem de [**\_ pintura do WM**](wm-paint.md) intermediário ocorrer, o aplicativo deverá garantir que qualquer desenho feito durante a mensagem não corromperá a seleção. Para evitar isso, muitos aplicativos removem a seleção, executam operações de desenho usuais e, em seguida, restauram a seleção quando o desenho é concluído.

 

 



