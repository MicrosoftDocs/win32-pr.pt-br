---
title: Adicionando manipuladores de mensagens de paleta
description: Adicionando manipuladores de mensagens de paleta
ms.assetid: bfd77f42-6a9d-4195-b1a0-1688e44358e3
keywords:
- DrawDib,paletas
- Função DrawDibRealize
- Função DrawDibDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b17512025cadf0e457b596a3bfc07399db4eb9185195f4c836ee154d5ff64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808626"
---
# <a name="adding-palette-message-handlers"></a>Adicionando manipuladores de mensagens de paleta

O exemplo a seguir ilustra manipuladores de mensagens simples para [**as mensagens WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE.**](/windows/desktop/gdi/wm-querynewpalette) O exemplo usa a [**função DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para processar a **mensagem WM \_ QUERYNEWPALETTE.**

Seu aplicativo deve responder à mensagem [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) invalidando a janela de destino para permitir que a função [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) redesenhar uma imagem. Você deve responder à [**mensagem WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) usando a [**função DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para realizar a paleta.


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

 

 