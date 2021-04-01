---
title: Como usar controles de pager
description: Esta seção descreve como implementar o controle de pager em seu aplicativo.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bfff0c8d8097c4b0e861506bb73f55467b711
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008448"
---
# <a name="how-to-use-pager-controls"></a>Como usar controles de pager

Esta seção descreve como implementar o controle de pager em seu aplicativo.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="initialize-a-pager-control"></a>Inicializar um controle de pager

Para usar o controle de pager, você deve chamar a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) com o \_ sinalizador de classe ICC PAGESCROLLER \_ definido no membro **dwICC** da estrutura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .

### <a name="create-a-pager-control"></a>Criar um controle de pager

Use o [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou a API [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar um controle de pager. O nome da classe para o controle é [**WC \_ PAGESCROLLER**](common-control-window-classes.md), que é definido em commctrl. h. O estilo [**PGS \_ na horizontal**](pager-control-styles.md) é usado para criar um pager horizontal e o estilo [**\_ Vert PGS**](pager-control-styles.md) é usado para criar um pager vertical. Como esse é um controle filho, o [**estilo \_ filho WS**](/windows/desktop/winmsg/window-styles) também deve ser usado.

Depois que o controle de pager for criado, você provavelmente desejará atribuir uma janela contida a ele. Se a janela contida for uma janela filho, você deverá tornar a janela filho um filho do controle de pager para que o tamanho e a posição sejam calculados corretamente. Em seguida, atribua a janela ao controle de pager com [**a \_ mensagem do PGM**](pgm-setchild.md) . Lembre-se de que essa mensagem não altera realmente a janela pai da janela contida; Ele simplesmente atribui a janela contida. Se a janela contida for um dos controles comuns, ela deverá ter o estilo [**\_ myresize da CCS**](common-control-styles.md) para impedir que o controle tente se redimensionar para o tamanho do controle de pager.

### <a name="process-pager-control-notifications"></a>Notificações de controle do pager de processo

No mínimo, é necessário processar a notificação [PGN \_ CALCSIZE](pgn-calcsize.md) . Se você não processar essa notificação e inserir um valor para a largura ou a altura, as setas de rolagem no controle de pager não serão exibidas. Isso ocorre porque o controle de pager usa a largura ou a altura fornecida na \_ notificação PGN CALCSIZE para determinar o tamanho "ideal" da janela contida.

O exemplo a seguir demonstra como processar o caso de notificação [PGN \_ CALCSIZE](pgn-calcsize.md) . Neste exemplo, a janela contida é um controle ToolBar que contém um número desconhecido de botões em um tamanho desconhecido. O exemplo mostra como usar a mensagem de [**TB \_ getmaxsize**](tb-getmaxsize.md) para determinar o tamanho de todos os itens na barra de ferramentas. Em seguida, o exemplo coloca a largura de todos os itens no membro **iWidth** da estrutura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) que é passada para a notificação.


```C++
case PGN_SCROLL:{

    LPNMPGSCROLL pScroll = (LPNMPGSCROLL)lParam;
 
    switch(pScroll->iDir){
     
        case PGF_SCROLLLEFT:
        case PGF_SCROLLRIGHT:
        case PGF_SCROLLUP:
        case PGF_SCROLLDOWN:
     
            pScroll->iScroll = 20;
        
            break;
        }
    }
  
return 0;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de pager](using-pager-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 