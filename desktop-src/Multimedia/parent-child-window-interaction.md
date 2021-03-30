---
title: Parent-Child interação da janela
description: Parent-Child interação da janela
ms.assetid: de10bf12-4ba4-4c6b-be56-489e4e2b26b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da43ab5ebe1aa24d8d67b8c901cd3302d8db48ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640740"
---
# <a name="parent-child-window-interaction"></a>Parent-Child interação da janela

Algumas mensagens no nível do sistema, como o [**WM \_ PaletteChanged**](/windows/desktop/gdi/wm-palettechanged) e o [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette), são enviadas somente para janelas de nível superior e sobrepostas. Se uma janela de captura for uma janela filho, seu pai deverá encaminhar essas mensagens.

Da mesma forma, se a janela pai alterar o tamanho, talvez seja necessário enviar mensagens de notificação para a janela de captura. Por outro lado, se as dimensões do vídeo capturado forem alteradas, a janela de captura poderá precisar enviar mensagens de notificação para a janela pai. A maneira mais simples de gerenciar isso é sempre manter as dimensões da janela de captura iguais ao tamanho do fluxo de vídeo capturado, notificando o pai sempre que essas dimensões forem alteradas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturar janelas](capture-windows.md)
</dt> </dl>

 

 