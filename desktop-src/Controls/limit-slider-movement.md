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
# <a name="how-to-limit-slider-movement"></a><span data-ttu-id="0d1b8-104">Como limitar o movimento do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="0d1b8-104">How to Limit Slider Movement</span></span>

<span data-ttu-id="0d1b8-105">Conforme descrito em [sobre controles TrackBar](trackbar-controls.md), é possível definir parte do intervalo TrackBar como um intervalo de seleção.</span><span class="sxs-lookup"><span data-stu-id="0d1b8-105">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="0d1b8-106">Uma finalidade de um intervalo de seleção pode ser limitar a movimentação do controle deslizante, tornando algumas partes dos limites completos do intervalo.</span><span class="sxs-lookup"><span data-stu-id="0d1b8-106">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0d1b8-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="0d1b8-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0d1b8-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="0d1b8-108">Technologies</span></span>

-   [<span data-ttu-id="0d1b8-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="0d1b8-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0d1b8-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="0d1b8-110">Prerequisites</span></span>

-   <span data-ttu-id="0d1b8-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="0d1b8-111">C/C++</span></span>
-   <span data-ttu-id="0d1b8-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="0d1b8-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0d1b8-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="0d1b8-113">Instructions</span></span>

### <a name="limit-slider-movement"></a><span data-ttu-id="0d1b8-114">Limitar movimento do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="0d1b8-114">Limit Slider Movement</span></span>

<span data-ttu-id="0d1b8-115">O código de exemplo a seguir limita a movimentação do controle deslizante redefinindo a posição do controle deslizante sempre que ele é movido para fora do intervalo de seleção.</span><span class="sxs-lookup"><span data-stu-id="0d1b8-115">The following example code limits movement of the slider by resetting the slider's position whenever it is moved outside the selection range.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="0d1b8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d1b8-116">Remarks</span></span>

<span data-ttu-id="0d1b8-117">Esse trecho de código seria parte de um procedimento de janela da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0d1b8-117">This code snippet would be part of a dialog box's Window Procedure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d1b8-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d1b8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d1b8-119">Usando controles TrackBar</span><span class="sxs-lookup"><span data-stu-id="0d1b8-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




