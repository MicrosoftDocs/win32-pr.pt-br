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
# <a name="adding-palette-message-handlers"></a><span data-ttu-id="2acb4-106">Adicionando manipuladores de mensagens de paleta</span><span class="sxs-lookup"><span data-stu-id="2acb4-106">Adding Palette Message Handlers</span></span>

<span data-ttu-id="2acb4-107">O exemplo a seguir ilustra manipuladores de mensagens simples para as mensagens do [**WM \_ paletachanged**](/windows/desktop/gdi/wm-palettechanged) e do [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) .</span><span class="sxs-lookup"><span data-stu-id="2acb4-107">The following example illustrates simple message handlers for the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages.</span></span> <span data-ttu-id="2acb4-108">O exemplo usa a função [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para processar a mensagem do **WM \_ QUERYNEWPALETTE** .</span><span class="sxs-lookup"><span data-stu-id="2acb4-108">The example uses the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to process the **WM\_QUERYNEWPALETTE** message.</span></span>

<span data-ttu-id="2acb4-109">Seu aplicativo deve responder à mensagem do [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) ao invalidar a janela de destino para permitir que a função [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) redesenhe uma imagem.</span><span class="sxs-lookup"><span data-stu-id="2acb4-109">Your application should respond to the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message by invalidating the destination window to let the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function redraw an image.</span></span> <span data-ttu-id="2acb4-110">Você deve responder à mensagem [**da \_ paletachanged do WM**](/windows/desktop/gdi/wm-palettechanged) usando a função [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para obter a paleta.</span><span class="sxs-lookup"><span data-stu-id="2acb4-110">You should respond to the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) message by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function to realize the palette.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2acb4-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2acb4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2acb4-112">Usando DrawDib</span><span class="sxs-lookup"><span data-stu-id="2acb4-112">Using DrawDib</span></span>](using-drawdib.md)
</dt> </dl>

 

 