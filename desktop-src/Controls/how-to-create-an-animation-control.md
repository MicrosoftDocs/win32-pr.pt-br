---
title: Como criar um controle de animação
description: Este tópico demonstra como criar um controle de animação.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8117d7c9393a828786532bd3d3fbfcf4f4eaaf6bb1bfdccdc5a2f97fa1c5cb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435816"
---
# <a name="how-to-create-an-animation-control"></a>Como criar um controle de animação

Este tópico demonstra como criar um controle de animação. O exemplo de código C++ que acompanha cria um controle de animação em uma caixa de diálogo. Ele posiciona o controle de animação abaixo de um controle especificado e define as dimensões do controle de animação com base nas dimensões de um quadro no clipe Audio-Video INTERcalado (AVI).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação
-   Arquivos AVI

## <a name="instructions"></a>Instruções

### <a name="step-1-create-an-instance-of-the-animation-control"></a>Etapa 1: Criar uma instância do controle de animação.

Use a [**macro Animar \_ Criar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) para criar uma instância do controle de animação.


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a>Etapa 2: Posiciona o controle de animação.

Obter as coordenadas de tela do botão de controle especificado.


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



Converta as coordenadas do canto inferior esquerdo em coordenadas do cliente.


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



Posiciona o controle de animação abaixo do botão de controle especificado.


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a>Etapa 3: Abra o clipe AVI.

Chame a [**macro Animar \_ Abrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) para abrir o clipe AVI e exibir o primeiro quadro no controle de animação. Chame a **função ShowWindow** para tornar o controle de animação visível.


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a>Exemplo completo


```C++
// CreateAnimationCtrl - creates an animation control, positions it 
//                       below the specified control in a dialog box, 
//                       and opens the AVI clip for the animation control. 
// Returns the handle to the animation control. 
// hwndDlg             - handle to the dialog box. 
// nIDCtl              - identifier of the control below which the animation control 
//                       is to be positioned. 
// 
// Constants 
//     IDC_ANIMATE - identifier of the animation control. 
//     CX_FRAME, CY_FRAME - width and height of the frames 
//     in the AVI clip. 

HWND CreateAnimationCtrl(HWND hwndDlg, int nIDCtl) 
{ 
    HWND hwndAnim = NULL;    
    
    // Create the animation control.
    // IDC_ANIMATE - identifier of the animation control. 
    // hwndDlg - handle to the dialog box.
    RECT rc;
    hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
        WS_BORDER | WS_CHILD, g_hinst); 

    // Get the screen coordinates of the specified control button.
    // nIDCtl - identifier of the control below which the animation control is to be positioned.
    GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 

    // Convert the coordinates of the lower-left corner to 
    // client coordinates.
    POINT pt;
    pt.x = rc.left; 
    pt.y = rc.bottom; 
    ScreenToClient(hwndDlg, &pt); 

    // Position the animation control below the Stop button.
    // CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
    SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
        CX_FRAME, CY_FRAME, 
        SWP_NOZORDER | SWP_DRAWFRAME);

    // Open the AVI clip, and show the animation control.
    Animate_Open(hwndAnim, "SEARCH.AVI"); 
    ShowWindow(hwndAnim, SW_SHOW); 

    return hwndAnim; 
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre controles de animação](animation-control-overview.md)
</dt> <dt>

[Referência de controle de animação](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Usando controles de animação](using-animation-control.md)
</dt> <dt>

[Animação](animation-control-reference.md)
</dt> </dl>

 

 




