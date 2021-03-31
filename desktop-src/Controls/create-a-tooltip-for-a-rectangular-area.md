---
title: Como criar uma dica de ferramenta para uma área retangular
description: O exemplo a seguir demonstra como criar um controle de dica de ferramenta padrão para a área inteira do cliente de uma janela.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635286"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a>Como criar uma dica de ferramenta para uma área retangular

O exemplo a seguir demonstra como criar um controle de dica de ferramenta padrão para a área inteira do cliente de uma janela.

A ilustração a seguir mostra a dica de ferramenta que é exibida quando o ponteiro do mouse está dentro da janela do cliente de uma caixa de diálogo. O identificador da caixa de diálogo foi passado para a função mostrada no exemplo anterior.

![captura de tela de uma caixa de diálogo; o ponteiro do mouse está dentro da janela do cliente e uma dica de ferramenta é visível](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="create-a-tooltip-for-a-rectangular-area"></a>Criar uma dica de ferramenta para uma área retangular

O exemplo a seguir demonstra como criar um controle de dica de ferramenta padrão para a área inteira do cliente de uma janela.


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de dica de ferramenta](using-tooltip-contro.md)
</dt> </dl>

 

 




