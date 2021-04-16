---
description: Esta seção aborda a interface de vários documentos, que é uma especificação que define uma interface do usuário para aplicativos que permitem ao usuário trabalhar com mais de um documento ao mesmo tempo.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface.htm
title: Interface de vários documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1898202aad6ec8d26f859bec2457124328c3a27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782524"
---
# <a name="multiple-document-interface"></a>Interface de vários documentos

\[Muitos usuários novos e intermediários acham difícil aprender a usar aplicativos MDI. Portanto, você deve considerar outros modelos para a interface do usuário. No entanto, você pode usar o MDI para aplicativos que não se ajustam facilmente a um modelo existente.\]

A interface de vários documentos (MDI) é uma especificação que define uma interface do usuário para aplicativos que permitem ao usuário trabalhar com mais de um documento ao mesmo tempo.

### <a name="in-this-section"></a>Nesta seção



| Tópico                                                                              | Descrição                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Sobre a interface de vários documentos](about-the-multiple-document-interface.md) | Descreve a interface de vários documentos.<br/>                                     |
| [Usando a interface de vários documentos](using-the-multiple-document-interface.md) | Explica como executar tarefas associadas à interface de vários documentos.<br/> |
| [Referência de MDI](multiple-document-interface-reference.md)                         | Contém a referência de API.<br/>                                                    |



 

### <a name="mdi-functions"></a>Funções MDI



| Nome                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)           | Cria uma janela filho MDI. <br/>                                                                                                                                                                                                                                                                                                                                    |
| [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca)                 | Fornece o processamento padrão para qualquer mensagem de janela que o procedimento de janela de uma janela de quadro MDI não processe. Todas as mensagens de janela que não são explicitamente processadas pelo procedimento de janela devem ser passadas para a função [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) , não para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . <br/>                              |
| [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca)           | Fornece o processamento padrão para qualquer mensagem de janela que o procedimento de janela de uma janela filho MDI não processe. Uma mensagem de janela não processada pelo procedimento de janela deve ser passada para a função [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) , não para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . <br/>                                             |
| [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) | Processa teclas do acelerador de tecla para comandos de menu da janela das janelas filho MDI associadas à janela do cliente MDI especificado. A função traduz as mensagens do [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) e do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) para as mensagens do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) e as envia para as janelas filho MDI apropriadas. <br/> |



 

### <a name="mdi-messages"></a>Mensagens MDI



| Nome                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MDIACTIVATE do WM \_**](wm-mdiactivate.md)       | Enviado a uma janela do cliente MDI para instruir a janela do cliente a ativar uma janela filho MDI diferente. <br/>                                                                                                                                                                                                                                                                                                                               |
| [**MDICASCADE do WM \_**](wm-mdicascade.md)         | Enviado a uma janela do cliente MDI para organizar todas as janelas filhas em um formato em cascata. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**MDICREATE do WM \_**](wm-mdicreate.md)           | Enviado a uma janela do cliente MDI para criar uma janela filho MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**MDIDESTROY do WM \_**](wm-mdidestroy.md)         | Enviado a uma janela do cliente MDI para fechar uma janela filho MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**MDIGETACTIVE do WM \_**](wm-mdigetactive.md)     | Enviado a uma janela do cliente MDI para recuperar o identificador para a janela filho MDI ativa. <br/>                                                                                                                                                                                                                                                                                                                                                |
| [**MDIICONARRANGE do WM \_**](wm-mdiiconarrange.md) | Enviado a uma janela do cliente MDI para organizar todas as janelas filho MDI minimizadas. Ele não afeta as janelas filhas que não são minimizadas. <br/>                                                                                                                                                                                                                                                                                                  |
| [**MDIMAXIMIZE do WM \_**](wm-mdimaximize.md)       | Enviado a uma janela do cliente MDI para maximizar uma janela filho MDI. O sistema redimensiona a janela filho para que sua área cliente preencha a janela do cliente. O sistema coloca o ícone do menu de janela da janela filho na posição mais à direita da barra de menus da janela do quadro e coloca o ícone de restauração da janela filho na posição mais à esquerda. O sistema também acrescenta o texto da barra de título da janela filho ao da janela do quadro. <br/> |
| [**MDINEXT do WM \_**](wm-mdinext.md)               | Enviado a uma janela do cliente MDI para ativar a janela filho seguinte ou anterior. <br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**MDIREFRESHMENU do WM \_**](wm-mdirefreshmenu.md) | Enviado para uma janela do cliente MDI para atualizar o menu janela da janela do quadro MDI. <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**MDIRESTORE do WM \_**](wm-mdirestore.md)         | Enviado a uma janela do cliente MDI para restaurar uma janela filho MDI do tamanho maximizado ou minimizado. <br/>                                                                                                                                                                                                                                                                                                                                      |
| [**MDISETMENU do WM \_**](wm-mdisetmenu.md)         | Enviado a uma janela do cliente MDI para substituir o menu inteiro de uma janela de quadro MDI, para substituir o menu janela da janela do quadro ou ambos. <br/>                                                                                                                                                                                                                                                                                           |
| [**MDITILE do WM \_**](wm-mditile.md)               | Enviado a uma janela do cliente MDI para organizar todas as janelas filho MDI em um formato de bloco. <br/>                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="mdi-structures"></a>Estruturas MDI



| Nome                                       | Descrição                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) | Contém informações sobre a classe, o título, o proprietário, o local e o tamanho de uma janela filho MDI. <br/> |



 

 

