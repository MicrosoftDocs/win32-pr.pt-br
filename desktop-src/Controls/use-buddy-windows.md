---
title: Como usar o Buddy Windows
description: Ao definir outros controles como Buddy Windows para um TrackBar, você pode posicionar automaticamente esses controles nas extremidades do TrackBar como rótulos.
ms.assetid: 5797AA55-BD8D-407A-8896-08EE0DDC7E30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eca9a4e3b3049f8d4cf7515879d91a096f5a9e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005352"
---
# <a name="how-to-use-buddy-windows"></a><span data-ttu-id="a7f69-103">Como usar o Buddy Windows</span><span class="sxs-lookup"><span data-stu-id="a7f69-103">How to Use Buddy Windows</span></span>

<span data-ttu-id="a7f69-104">Ao definir outros controles como Buddy Windows para um TrackBar, você pode posicionar automaticamente esses controles nas extremidades do TrackBar como rótulos.</span><span class="sxs-lookup"><span data-stu-id="a7f69-104">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span>

<span data-ttu-id="a7f69-105">A ilustração a seguir mostra um TrackBar horizontal e vertical, ambos com controles estáticos como Buddy Windows.</span><span class="sxs-lookup"><span data-stu-id="a7f69-105">The following illustration shows a horizontal and a vertical trackbar, both with static controls as buddy windows.</span></span>

![captura de tela mostrando uma caixa de diálogo com um TrackBar horizontal e um TrackBar vertical](images/tkb-buddy.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="a7f69-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="a7f69-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a7f69-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="a7f69-108">Technologies</span></span>

-   [<span data-ttu-id="a7f69-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="a7f69-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a7f69-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a7f69-110">Prerequisites</span></span>

-   <span data-ttu-id="a7f69-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="a7f69-111">C/C++</span></span>
-   <span data-ttu-id="a7f69-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="a7f69-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a7f69-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="a7f69-113">Instructions</span></span>

### <a name="use-buddy-windows"></a><span data-ttu-id="a7f69-114">Usar as janelas de amigo</span><span class="sxs-lookup"><span data-stu-id="a7f69-114">Use Buddy Windows</span></span>

<span data-ttu-id="a7f69-115">O exemplo de código a seguir cria as janelas Buddy mostradas na ilustração.</span><span class="sxs-lookup"><span data-stu-id="a7f69-115">The following code example creates the buddy windows shown in the illustration.</span></span>


```
void LabelTrackbarsWithBuddies(HWND hDlg)
{
    HWND hwndTrackbar;
    HWND hwndBuddy;
    
    const int staticWidth   = 50;
    const int staticHeight  = 20;

//======================================================
// For horizontal Trackbar.

    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Left", SS_RIGHT | WS_CHILD | WS_VISIBLE, 
                                    0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                    
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);
    
    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Right", SS_LEFT | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
    
//======================================================    
// For vertical Trackbar.
    
    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER2);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Top", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);

    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Bottom", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
}
```



## <a name="remarks"></a><span data-ttu-id="a7f69-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7f69-116">Remarks</span></span>

<span data-ttu-id="a7f69-117">**IDC \_ SLIDER1** e **IDC \_ controledeslizante2** são trackbars criados no editor de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7f69-117">**IDC\_SLIDER1** and **IDC\_SLIDER2** are trackbars created in the resource editor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7f69-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7f69-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7f69-119">Usando controles TrackBar</span><span class="sxs-lookup"><span data-stu-id="a7f69-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




