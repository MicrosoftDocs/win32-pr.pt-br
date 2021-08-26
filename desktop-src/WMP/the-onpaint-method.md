---
title: O método OnPaint
description: O método OnPaint
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- plug-ins Windows Media Player, método onpaint
- plug-ins, método OnPaint
- plug-ins de interface do usuário, método OnPaint
- Plug-ins de interface do usuário, método OnPaint
- Método OnPaint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5e121cdaeac1c7589e58b1613a8d25bdff4f44f6db2375bcbdc34da20929e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001946"
---
# <a name="the-onpaint-method"></a>O método OnPaint

O método OnPaint é chamado sempre que a janela de plug-in deve ser pintada. Isso ocorre quando a janela de plug-in recebe uma \_ mensagem do WM Paint, que é mapeada para o método OnPaint no mapa de mensagens descrito anteriormente. O assistente fornece uma implementação desse método que pinta o preto de fundo e coloca o nome do plug-in na janela de plug-in. A única modificação necessária para o plug-in da interface do usuário de pesquisa é a remoção do código que exibe o texto.

O código a seguir é usado para implementar esse método:


```C++
LRESULT OnPaint(UINT nMsg, WPARAM wParam, 
                         LPARAM lParam, BOOL& bHandled)
{
    PAINTSTRUCT ps;

    HDC hDC = BeginPaint(&ps);

    RECT rc;
    GetClientRect(&rc);

    HBRUSH hNewBrush = ::CreateSolidBrush( RGB(0, 0, 0) );

    if (hNewBrush)
    {
        ::FillRect(hDC, &rc, hNewBrush );
        ::DeleteObject( hNewBrush );
    }

    EndPaint(&ps);
    return 0;
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




