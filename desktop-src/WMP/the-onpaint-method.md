---
title: O método OnPaint
description: O método OnPaint
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Plug-ins do Windows Media Player, método OnPaint
- plug-ins, método OnPaint
- plug-ins de interface do usuário, método OnPaint
- Plug-ins de interface do usuário, método OnPaint
- Método OnPaint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22641c34bb2edab30c1bf97011e893bc1d9d44a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453692"
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

 

 




