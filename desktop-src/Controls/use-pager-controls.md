---
title: Como usar controles de pager
description: Esta seção descreve como implementar o controle de pager em seu aplicativo.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b917943f5f86498bb3cbea2c58842049c4618caf64a66a6b8db1cb2ab86a315b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828631"
---
# <a name="how-to-use-pager-controls"></a>Como usar controles de pager

Esta seção descreve como implementar o controle de pager em seu aplicativo.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="initialize-a-pager-control"></a>Inicializar um controle pager

Para usar o controle pager, você deve chamar a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) com o sinalizador ICC PAGESCROLLER CLASS definido no \_ membro \_ **dwICC** da estrutura [**INITCOMMONCONTROLSEX.**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)

### <a name="create-a-pager-control"></a>Criar um controle pager

Use [**CreateWindow ou**](/windows/desktop/api/winuser/nf-winuser-createwindowa) a API [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar um controle de pager. O nome da classe para o controle [**é WC \_ PAGESCROLLER,**](common-control-window-classes.md)que é definido em Commctrl.h. O [**estilo \_ PGS HORZ**](pager-control-styles.md) é usado para criar um pager horizontal e o estilo [**\_ PGS VERT**](pager-control-styles.md) é usado para criar um pager vertical. Como esse é um controle filho, o estilo FILHO do [**WS \_**](/windows/desktop/winmsg/window-styles) também deve ser usado.

Depois que o controle de pager for criado, você provavelmente deseja atribuir uma janela independente a ele. Se a janela contida for uma janela filho, você deverá tornar a janela filho um filho do controle pager para que o tamanho e a posição sejam calculados corretamente. Em seguida, atribua a janela ao controle de pager com a [**mensagem \_ SETCHILD do PGM.**](pgm-setchild.md) Esteja ciente de que essa mensagem não altera realmente a janela pai da janela contida; ele simplesmente atribui a janela contida. Se a janela contida for um dos controles comuns, ela deverá ter o estilo [**CCS \_ NORESIZE**](common-control-styles.md) para impedir que o controle tentar se reorganizar de acordo com o tamanho do controle de pager.

### <a name="process-pager-control-notifications"></a>Processar notificações de controle de pager

No mínimo, é necessário processar a notificação [ \_ CALCSIZE do PGN.](pgn-calcsize.md) Se você não processar essa notificação e inserir um valor para a largura ou altura, as setas de rolagem no controle de pager não serão exibidas. Isso porque o controle de pager usa a largura ou a altura fornecida na notificação CALCSIZE pgn para determinar o \_ tamanho "ideal" da janela contida.

O exemplo a seguir demonstra como processar o caso de notificação [ \_ CALCSIZE do PGN.](pgn-calcsize.md) Neste exemplo, a janela contida é um controle de barra de ferramentas que contém um número desconhecido de botões em um tamanho desconhecido. O exemplo mostra como usar a [**mensagem \_ GETMAXSIZE de TB**](tb-getmaxsize.md) para determinar o tamanho de todos os itens na barra de ferramentas. Em seguida, o exemplo coloca a largura de todos os itens no membro **iWidth** da estrutura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) que é passada para a notificação.


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

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 