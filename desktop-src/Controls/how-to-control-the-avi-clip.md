---
title: Como controlar o clipe AVI
description: Este tópico demonstra como usar as macros de controle de animação para reproduzir, parar e fechar um clipe Audio-Video AVI (intercalado) associado.
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c11f7d8f519f98f3293d5be29fac0e0a40dd704
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104454475"
---
# <a name="how-to-control-the-avi-clip"></a><span data-ttu-id="15b26-103">Como controlar o clipe AVI</span><span class="sxs-lookup"><span data-stu-id="15b26-103">How to Control the AVI Clip</span></span>

<span data-ttu-id="15b26-104">Este tópico demonstra como usar as macros de controle de animação para reproduzir, parar e fechar um clipe Audio-Video AVI (intercalado) associado.</span><span class="sxs-lookup"><span data-stu-id="15b26-104">This topic demonstrates how to use the animation control macros to play, stop, and close an associated Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="15b26-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="15b26-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="15b26-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="15b26-106">Technologies</span></span>

-   [<span data-ttu-id="15b26-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="15b26-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="15b26-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="15b26-108">Prerequisites</span></span>

-   <span data-ttu-id="15b26-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="15b26-109">C/C++</span></span>
-   <span data-ttu-id="15b26-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="15b26-110">Windows User Interface Programming</span></span>
-   <span data-ttu-id="15b26-111">Arquivos AVI</span><span class="sxs-lookup"><span data-stu-id="15b26-111">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="15b26-112">Instruções</span><span class="sxs-lookup"><span data-stu-id="15b26-112">Instructions</span></span>


<span data-ttu-id="15b26-113">Crie uma função que usa como parâmetros um identificador para o controle de animação e um sinalizador que indica a ação a ser executada no clipe AVI associado.</span><span class="sxs-lookup"><span data-stu-id="15b26-113">Create a function that takes as parameters a handle to the animation control and a flag that indicates the action to be performed on the associated AVI clip.</span></span>

<span data-ttu-id="15b26-114">A função no exemplo C++ a seguir chama uma das três macros de controle de animação ([**Animate \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**anima \_ Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**Animate \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) com base no valor do parâmetro *nação* .</span><span class="sxs-lookup"><span data-stu-id="15b26-114">The function in the following C++ example calls one of three animation control macros ([**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) based on the value of the *nAction* parameter.</span></span> <span data-ttu-id="15b26-115">O identificador para o controle de animação que está associado ao clipe AVI é passado por meio do parâmetro *hwndAnim* .</span><span class="sxs-lookup"><span data-stu-id="15b26-115">The handle to the animation control that is associated with the AVI clip is passed via the *hwndAnim* parameter.</span></span>


```C++
// DoAnimation - plays, stops, or closes an animation control's 
//               AVI clip, depending on the value of an action flag. 
// hwndAnim    - handle to an animation control. 
// nAction     - flag that determines whether to play, stop, or close 
//               the AVI clip. 

void DoAnimation(HWND hwndAnim, int nAction) 
{ 
    int const PLAYIT = 1, STOPIT = 2, CLOSEIT = 3; 
    switch (nAction) { 
        case PLAYIT: 
         // Play the clip continuously starting with the 
         // first frame. 
            Animate_Play(hwndAnim, 0, -1, -1); 
            break; 

        case STOPIT: 
            Animate_Stop(hwndAnim); 
            break; 

        case CLOSEIT: 
            Animate_Close(hwndAnim); 
            break; 

        default: 
            break; 
    }
    
    return; 
```



## <a name="related-topics"></a><span data-ttu-id="15b26-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15b26-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15b26-117">Sobre os controles de animação</span><span class="sxs-lookup"><span data-stu-id="15b26-117">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="15b26-118">Referência de controle de animação</span><span class="sxs-lookup"><span data-stu-id="15b26-118">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="15b26-119">Usando controles de animação</span><span class="sxs-lookup"><span data-stu-id="15b26-119">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="15b26-120">Controle de animação</span><span class="sxs-lookup"><span data-stu-id="15b26-120">Animation Control</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




