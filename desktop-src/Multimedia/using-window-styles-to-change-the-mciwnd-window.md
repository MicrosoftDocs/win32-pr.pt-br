---
title: Usando estilos de janela para alterar a janela MCIWnd
description: Usando estilos de janela para alterar a janela MCIWnd
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- Função MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90212b43d6d51c82eb9b6e1a26bb06c7215c2568594e04980294b0d87bd53e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135604"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a>Usando estilos de janela para alterar a janela MCIWnd

Assim como em qualquer janela, você pode alterar a aparência e o comportamento de uma janela MCIWnd escolhendo entre os estilos de janela padrão especificados com a [função CreateWindow.](/windows/win32/api/winuser/nf-winuser-createwindowa) Além disso, você pode escolher entre vários outros estilos de janela específicos para janelas MCIWnd. Com esses estilos, seu aplicativo pode alterar essas janelas MCIWnd das seguintes maneiras:

-   Alterar o tamanho da janela.
-   Ocultar ou exibir controles.
-   Emitir mensagens de notificação.
-   Exibir informações na barra de título.

Você pode definir estilos de janela especificando-os na função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) ou pode usar a macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) para alterar o estilo de uma janela MCIWnd existente. Você também pode consultar uma janela MCIWnd para seus estilos atuais usando a macro [**MCIWndGetStyles.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)

Para ver uma lista dos estilos de janela específicos de MCIWnd, consulte [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).

 

 