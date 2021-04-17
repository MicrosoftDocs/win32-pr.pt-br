---
title: Adicionando manipuladores de mensagens de paleta
description: Adicionando manipuladores de mensagens de paleta
ms.assetid: bfd77f42-6a9d-4195-b1a0-1688e44358e3
keywords:
- DrawDib, paletas
- Função DrawDibRealize
- Função DrawDibDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 679990dce5977430eb2a46fc3cd06622246d357f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365976"
---
# <a name="adding-palette-message-handlers"></a>Adicionando manipuladores de mensagens de paleta

O exemplo a seguir ilustra manipuladores de mensagens simples para as mensagens do [**WM \_ paletachanged**](/windows/desktop/gdi/wm-palettechanged) e do [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) . O exemplo usa a função [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para processar a mensagem do **WM \_ QUERYNEWPALETTE** .

Seu aplicativo deve responder à mensagem do [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) ao invalidar a janela de destino para permitir que a função [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) redesenhe uma imagem. Você deve responder à mensagem [**da \_ paletachanged do WM**](/windows/desktop/gdi/wm-palettechanged) usando a função [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para obter a paleta.


```C++
case WM_PALETTECHANGED: 
    if ((HWND)wParam == hwnd) 
        break; 
case WM_QUERYNEWPALETTE: 
    hdc = GetDC(hwnd); 
    f = DrawDibRealize(hdd, hdc, FALSE) > 0; 
    ReleaseDC(hwnd, hdc); 
    if (f) 
        InvalidateRect(hwnd, NULL, TRUE); 
    break; 

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DrawDib](using-drawdib.md)
</dt> </dl>

 

 