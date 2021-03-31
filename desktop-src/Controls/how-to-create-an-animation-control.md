---
title: Como criar um controle de animação
description: Este tópico demonstra como criar um controle de animação.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ff190617996e42e6580b82311fb51f4248000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005140"
---
# <a name="how-to-create-an-animation-control"></a>Como criar um controle de animação

Este tópico demonstra como criar um controle de animação. O exemplo de código do C++ que o acompanha cria um controle de animação em uma caixa de diálogo. Ele posiciona o controle de animação abaixo de um controle especificado e define as dimensões do controle de animação com base nas dimensões de um quadro no clipe de Audio-Video intercalado (AVI).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows
-   Arquivos AVI

## <a name="instructions"></a>Instruções

### <a name="step-1-create-an-instance-of-the-animation-control"></a>Etapa 1: criar uma instância do controle de animação.

Use a macro [**animar \_ criar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) para criar uma instância do controle animação.


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a>Etapa 2: posicionar o controle de animação.

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



Posicione o controle de animação abaixo do botão de controle especificado.


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a>Etapa 3: abrir o clipe AVI.

Chame a macro de [**animação \_ aberta**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) para abrir o clipe AVI e exibir o primeiro quadro no controle de animação. Chame a função de **janela** para tornar o controle de animação visível.


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

[Sobre os controles de animação](animation-control-overview.md)
</dt> <dt>

[Referência de controle de animação](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Usando controles de animação](using-animation-control.md)
</dt> <dt>

[Animação](animation-control-reference.md)
</dt> </dl>

 

 




