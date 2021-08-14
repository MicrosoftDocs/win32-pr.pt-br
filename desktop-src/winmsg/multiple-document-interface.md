---
description: Esta seção discute a Interface de Vários Documentos, que é uma especificação que define uma interface do usuário para aplicativos que permitem que o usuário trabalhe com mais de um documento ao mesmo tempo.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface.htm
title: Interface de vários documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d579d1075f85fae7cd2d4ca6e63e1b8196c6d2118e33102cd511a1e468a18ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705355"
---
# <a name="multiple-document-interface"></a>Interface de vários documentos

\[Muitos usuários novos e intermediários acham difícil aprender a usar aplicativos MDI. Portanto, você deve considerar outros modelos para sua interface do usuário. No entanto, você pode usar o MDI para aplicativos que não se ajustam facilmente a um modelo existente.\]

A MDI (interface de vários documentos) é uma especificação que define uma interface do usuário para aplicativos que permitem que o usuário trabalhe com mais de um documento ao mesmo tempo.

### <a name="in-this-section"></a>Nesta seção



| Tópico                                                                              | Descrição                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Sobre a interface de vários documentos](about-the-multiple-document-interface.md) | Descreve a interface de vários documentos.<br/>                                     |
| [Usando a interface de vários documentos](using-the-multiple-document-interface.md) | Explica como executar tarefas associadas à Interface de Vários Documentos.<br/> |
| [Referência de MDI](multiple-document-interface-reference.md)                         | Contém a referência de API.<br/>                                                    |



 

### <a name="mdi-functions"></a>Funções MDI



| Name                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)           | Cria uma janela filho MDI. <br/>                                                                                                                                                                                                                                                                                                                                    |
| [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca)                 | Fornece processamento padrão para todas as mensagens de janela que o procedimento de janela de uma janela de quadro MDI não processa. Todas as mensagens de janela que não são processadas explicitamente pelo procedimento de janela devem ser passadas para a função [**DefFrameProc,**](/windows/win32/api/winuser/nf-winuser-defframeproca) não para [**a função DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) <br/>                              |
| [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca)           | Fornece processamento padrão para qualquer mensagem de janela que o procedimento de janela de uma janela filho MDI não processa. Uma mensagem de janela não processada pelo procedimento de janela deve ser passada para a função [**DefMDIChildProc,**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) não para a [**função DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) <br/>                                             |
| [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) | Processa as teclas de aceleração para comandos de menu de janela das janelas filho MDI associadas à janela do cliente MDI especificada. A função converte mensagens [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) e [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) em mensagens [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) e as envia para as janelas filho MDI apropriadas. <br/> |



 

### <a name="mdi-messages"></a>Mensagens MDI



| Name                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ MDIACTIVATE**](wm-mdiactivate.md)       | Enviado para uma janela de cliente MDI para instruir a janela do cliente a ativar uma janela filho MDI diferente. <br/>                                                                                                                                                                                                                                                                                                                               |
| [**WM \_ MDICASCADE**](wm-mdicascade.md)         | Enviado para uma janela de cliente MDI para organizar todas as janelas filho em um formato em cascata. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ MDICREATE**](wm-mdicreate.md)           | Enviado para uma janela de cliente MDI para criar uma janela filho MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ MDIDESTROY**](wm-mdidestroy.md)         | Enviado para uma janela de cliente MDI para fechar uma janela filho MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)     | Enviado para uma janela de cliente MDI para recuperar o alça para a janela filho MDI ativa. <br/>                                                                                                                                                                                                                                                                                                                                                |
| [**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md) | Enviado para uma janela de cliente MDI para organizar todas as janelas filho MDI minimizadas. Ele não afeta as janelas filho que não são minimizadas. <br/>                                                                                                                                                                                                                                                                                                  |
| [**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md)       | Enviado para uma janela de cliente MDI para maximizar uma janela filho MDI. O sistema resize a janela filho para fazer com que sua área de cliente preencha a janela do cliente. O sistema coloca o ícone de menu da janela filho na posição mais à direita da barra de menus da janela do quadro e coloca o ícone de restauração da janela filho na posição mais à esquerda. O sistema também anexa o texto da barra de título da janela filho ao da janela do quadro. <br/> |
| [**WM \_ MARDXT**](wm-mdinext.md)               | Enviado para uma janela de cliente MDI para ativar a janela filho seguinte ou anterior. <br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ MDIREFRESHMENU**](wm-mdirefreshmenu.md) | Enviado para uma janela de cliente MDI para atualizar o menu de janela da janela de quadro MDI. <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ MDIRESTORE**](wm-mdirestore.md)         | Enviado para uma janela de cliente MDI para restaurar uma janela filho MDI do tamanho maximizada ou minimizada. <br/>                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ MDISETMENU**](wm-mdisetmenu.md)         | Enviado para uma janela de cliente MDI para substituir todo o menu de uma janela de quadro MDI, para substituir o menu de janela da janela de quadro ou ambos. <br/>                                                                                                                                                                                                                                                                                           |
| [**WM \_ MDITILE**](wm-mditile.md)               | Enviado para uma janela de cliente MDI para organizar todas as janelas filho MDI em um formato de parte. <br/>                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="mdi-structures"></a>Estruturas MDI



| Name                                       | Descrição                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) | Contém informações sobre a classe, o título, o proprietário, o local e o tamanho de uma janela filho MDI. <br/> |



 

 

