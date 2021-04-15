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
# <a name="how-to-control-the-avi-clip"></a>Como controlar o clipe AVI

Este tópico demonstra como usar as macros de controle de animação para reproduzir, parar e fechar um clipe Audio-Video AVI (intercalado) associado.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows
-   Arquivos AVI

## <a name="instructions"></a>Instruções


Crie uma função que usa como parâmetros um identificador para o controle de animação e um sinalizador que indica a ação a ser executada no clipe AVI associado.

A função no exemplo C++ a seguir chama uma das três macros de controle de animação ([**Animate \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**anima \_ Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**Animate \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) com base no valor do parâmetro *nação* . O identificador para o controle de animação que está associado ao clipe AVI é passado por meio do parâmetro *hwndAnim* .


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre os controles de animação](animation-control-overview.md)
</dt> <dt>

[Referência de controle de animação](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Usando controles de animação](using-animation-control.md)
</dt> <dt>

[Controle de animação](animation-control-reference.md)
</dt> </dl>

 

 




