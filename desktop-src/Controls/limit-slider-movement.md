---
title: Como limitar o movimento do controle deslizante
description: Conforme descrito em sobre controles TrackBar, é possível definir parte do intervalo TrackBar como um intervalo de seleção. Uma finalidade de um intervalo de seleção pode ser limitar a movimentação do controle deslizante, tornando algumas partes dos limites completos do intervalo.
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822413"
---
# <a name="how-to-limit-slider-movement"></a>Como limitar o movimento do controle deslizante

Conforme descrito em [sobre controles TrackBar](trackbar-controls.md), é possível definir parte do intervalo TrackBar como um intervalo de seleção. Uma finalidade de um intervalo de seleção pode ser limitar a movimentação do controle deslizante, tornando algumas partes dos limites completos do intervalo.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="limit-slider-movement"></a>Limitar movimento do controle deslizante

O código de exemplo a seguir limita a movimentação do controle deslizante redefinindo a posição do controle deslizante sempre que ele é movido para fora do intervalo de seleção.


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a>Comentários

Esse trecho de código seria parte de um procedimento de janela da caixa de diálogo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles TrackBar](using-trackbar-controls.md)
</dt> </dl>

 

 




