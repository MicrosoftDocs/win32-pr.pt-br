---
title: Como implementar dicas de ferramentas de balão
description: As dicas de ferramentas de balão são semelhantes às dicas de ferramenta padrão, mas são exibidas em um balão \ 0034; de estilo animado \ 0034; com uma haste apontando para a ferramenta.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635291"
---
# <a name="how-to-implement-balloon-tooltips"></a>Como implementar dicas de ferramentas de balão

As dicas de ferramentas de balão são semelhantes às dicas de ferramenta padrão, mas são exibidas em um "balão" estilo animado com uma haste apontando para a ferramenta. As dicas de ferramentas de balão podem ser de linha única ou de várias linhas. Eles são criados e manipulados quase da mesma forma que as dicas de ferramentas padrão.

A posição padrão da haste e do retângulo é mostrada na ilustração a seguir. Se a ferramenta estiver muito próxima da parte superior da tela, a dica de ferramenta aparecerá abaixo e à direita do retângulo da ferramentas. Se a ferramenta estiver muito perto do lado direito da tela, os princípios semelhantes se aplicarão, mas a dica de ferramenta aparecerá à esquerda do retângulo de ferramentas.

![captura de tela de uma caixa de diálogo; uma dica de ferramenta de balão com uma linha de texto é exibida acima e à direita do destino](images/tt-balloon.png)

Você pode alterar o posicionamento padrão definindo o sinalizador **\_ CENTERTIP de TTF** no membro **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de dica de ferramenta. Nesse caso, a haste normalmente aponta para o centro da borda inferior do retângulo da ferramenta e o retângulo do texto é exibido diretamente abaixo da ferramenta. A haste é anexada ao retângulo de texto no centro da borda superior. Se a ferramenta estiver muito perto da parte inferior da tela, o retângulo de texto será centralizado acima da ferramenta e o tronco se conectará ao centro da borda inferior.

A ilustração a seguir mostra uma dica de ferramenta que é centralizada na Tool.

![captura de tela de uma caixa de diálogo; uma dica de ferramenta de balão com uma linha de texto é exibida centralizada abaixo do destino](images/tt-ballooncenter.png)

Se você quiser especificar onde os pontos de haste, defina o sinalizador de **\_ faixa de TTF** no membro **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) da dica de ferramenta. Em seguida, você especifica a coordenada enviando uma mensagem [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) , com as coordenadas x e y no valor de *lParam* . Se **ttf \_ CENTERTIP** também for definido, a haste ainda apontará para a posição especificada pela mensagem **TTM \_ TRACKPOSITION** .

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="implement-balloon-tooltips"></a>Implementar dicas de ferramentas de balão

O código de exemplo a seguir mostra como implementar uma dica de ferramenta de balão centralizado usando o estilo de controle ToolTip de **\_ balão de TTS** .


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de dica de ferramenta](using-tooltip-contro.md)
</dt> <dt>

[**Estilos de dica de ferramenta**](tooltip-styles.md)
</dt> </dl>

 

 




