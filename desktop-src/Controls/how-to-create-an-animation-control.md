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
# <a name="how-to-create-an-animation-control"></a><span data-ttu-id="853c3-103">Como criar um controle de animação</span><span class="sxs-lookup"><span data-stu-id="853c3-103">How to Create an Animation Control</span></span>

<span data-ttu-id="853c3-104">Este tópico demonstra como criar um controle de animação.</span><span class="sxs-lookup"><span data-stu-id="853c3-104">This topic demonstrates how to create an animation control.</span></span> <span data-ttu-id="853c3-105">O exemplo de código do C++ que o acompanha cria um controle de animação em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="853c3-105">The accompanying C++ code example creates an animation control in a dialog box.</span></span> <span data-ttu-id="853c3-106">Ele posiciona o controle de animação abaixo de um controle especificado e define as dimensões do controle de animação com base nas dimensões de um quadro no clipe de Audio-Video intercalado (AVI).</span><span class="sxs-lookup"><span data-stu-id="853c3-106">It positions the animation control below a specified control, and sets the dimensions of the animation control based on the dimensions of a frame in the Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="853c3-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="853c3-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="853c3-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="853c3-108">Technologies</span></span>

-   [<span data-ttu-id="853c3-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="853c3-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="853c3-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="853c3-110">Prerequisites</span></span>

-   <span data-ttu-id="853c3-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="853c3-111">C/C++</span></span>
-   <span data-ttu-id="853c3-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="853c3-112">Windows User Interface Programming</span></span>
-   <span data-ttu-id="853c3-113">Arquivos AVI</span><span class="sxs-lookup"><span data-stu-id="853c3-113">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="853c3-114">Instruções</span><span class="sxs-lookup"><span data-stu-id="853c3-114">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-animation-control"></a><span data-ttu-id="853c3-115">Etapa 1: criar uma instância do controle de animação.</span><span class="sxs-lookup"><span data-stu-id="853c3-115">Step 1: Create an instance of the animation control.</span></span>

<span data-ttu-id="853c3-116">Use a macro [**animar \_ criar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) para criar uma instância do controle animação.</span><span class="sxs-lookup"><span data-stu-id="853c3-116">Use the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro to create an instance of the animation control.</span></span>


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a><span data-ttu-id="853c3-117">Etapa 2: posicionar o controle de animação.</span><span class="sxs-lookup"><span data-stu-id="853c3-117">Step 2: Position the animation control.</span></span>

<span data-ttu-id="853c3-118">Obter as coordenadas de tela do botão de controle especificado.</span><span class="sxs-lookup"><span data-stu-id="853c3-118">Get the screen coordinates of the specified control button.</span></span>


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



<span data-ttu-id="853c3-119">Converta as coordenadas do canto inferior esquerdo em coordenadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="853c3-119">Convert the coordinates of the lower-left corner to client coordinates.</span></span>


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



<span data-ttu-id="853c3-120">Posicione o controle de animação abaixo do botão de controle especificado.</span><span class="sxs-lookup"><span data-stu-id="853c3-120">Position the animation control below the specified control button.</span></span>


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a><span data-ttu-id="853c3-121">Etapa 3: abrir o clipe AVI.</span><span class="sxs-lookup"><span data-stu-id="853c3-121">Step 3: Open the AVI clip.</span></span>

<span data-ttu-id="853c3-122">Chame a macro de [**animação \_ aberta**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) para abrir o clipe AVI e exibir o primeiro quadro no controle de animação.</span><span class="sxs-lookup"><span data-stu-id="853c3-122">Call the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) macro to open the AVI clip and display the first frame in the animation control.</span></span> <span data-ttu-id="853c3-123">Chame a função de **janela** para tornar o controle de animação visível.</span><span class="sxs-lookup"><span data-stu-id="853c3-123">Call the **ShowWindow** function to make the animation control visible.</span></span>


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a><span data-ttu-id="853c3-124">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="853c3-124">Complete example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="853c3-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="853c3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="853c3-126">Sobre os controles de animação</span><span class="sxs-lookup"><span data-stu-id="853c3-126">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="853c3-127">Referência de controle de animação</span><span class="sxs-lookup"><span data-stu-id="853c3-127">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="853c3-128">Usando controles de animação</span><span class="sxs-lookup"><span data-stu-id="853c3-128">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="853c3-129">Animação</span><span class="sxs-lookup"><span data-stu-id="853c3-129">Animation</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




