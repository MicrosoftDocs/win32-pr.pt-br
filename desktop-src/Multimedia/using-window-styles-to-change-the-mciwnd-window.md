---
title: Usando estilos de janela para alterar a janela MCIWnd
description: Usando estilos de janela para alterar a janela MCIWnd
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- Função MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758948"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a>Usando estilos de janela para alterar a janela MCIWnd

Assim como em qualquer janela, você pode alterar a aparência e o comportamento de uma janela MCIWnd escolhendo os estilos de janela padrão especificados com a função [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Além disso, você pode escolher entre vários outros estilos de janela que são específicos para o Windows MCIWnd. Com esses estilos, seu aplicativo pode alterar essas janelas MCIWnd das seguintes maneiras:

-   Alterar o tamanho da janela.
-   Ocultar ou exibir controles.
-   Emitir mensagens de notificação.
-   Exibir informações na barra de título.

Você pode definir estilos de janela especificando-os na função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) ou pode usar a macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) para alterar o estilo de uma janela existente do MCIWnd. Você também pode consultar uma janela MCIWnd para seus estilos atuais usando a macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .

Para obter uma lista dos estilos de janela específicos do MCIWnd, consulte [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).

 

 