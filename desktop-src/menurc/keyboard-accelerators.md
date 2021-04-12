---
title: Aceleradores de teclado
description: Esta seção aborda aceleradores de teclado. Um acelerador de teclado é um pressionamento de teclas ou uma combinação de pressionamentos de teclas que gera uma mensagem de comando para um aplicativo.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators.htm
keywords:
- entrada do usuário, aceleradores de teclado
- capturando entrada do usuário, aceleradores de teclado
- aceleradores de teclado
- aceleradores
- WM_COMMAND mensagem
- WM_SYS mensagem de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd8cecd2fc1273750c75b8e5f33106d22343a14
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365980"
---
# <a name="keyboard-accelerators"></a>Aceleradores de teclado

Um *acelerador de teclado* (ou, simplesmente, acelerador) é um pressionamento de teclas ou uma combinação de pressionamentos de teclas que gera um [**\_ comando do WM**](wm-command.md) ou uma mensagem do [**WM \_ SYSCOMMAND**](wm-syscommand.md) para um aplicativo.

### <a name="in-this-section"></a>Nesta seção



| Nome                                                                 | Descrição                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Sobre aceleradores de teclado](about-keyboard-accelerators.md)       | Discute aceleradores de teclado.<br/>                                |
| [Usando aceleradores de teclado](using-keyboard-accelerators.md)       | Discute as tarefas associadas a aceleradores de teclado.<br/> |
| [Referência do acelerador de teclado](keyboard-accelerator-reference.md) | Contém a referência de API.<br/>                                     |



 

### <a name="keyboard-accelerator-functions"></a>Funções do acelerador de teclado



| Nome                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea)       | Copia a tabela de acelerador especificada. Essa função é usada para obter os dados da tabela de aceleração que correspondem a um identificador de tabela de aceleração ou para determinar o tamanho dos dados da tabela de aceleração. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)   | Cria uma tabela de acelerador. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) | Destrói uma tabela de acelerador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa)               | Carrega a tabela de acelerador especificada. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)       | Processa chaves do acelerador para comandos de menu. A função converte uma mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) ou [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) em um [**\_ comando do WM**](wm-command.md) ou em uma mensagem do [**WM \_ SYSCOMMAND**](wm-syscommand.md) (se houver uma entrada para a chave na tabela de acelerador especificada) e, em seguida, envia o **\_ comando do WM** ou a mensagem do **WM \_ SYSCOMMAND** diretamente para o procedimento de janela especificado. [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) não retorna até que o procedimento de janela tenha processado a mensagem. <br/> |



 

### <a name="keyboard-accelerator-messages"></a>Mensagens do acelerador de teclado



| Nome                                          | Descrição                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHANGEUISTATE do WM \_**](wm-changeuistate.md) | Enviado para indicar que o estado da interface do usuário deve ser alterado.<br/>                                                                                                                                                                                                                                                  |
| [**INITMENU do WM \_**](wm-initmenu.md)           | Enviado quando um menu está prestes a ficar ativo. Ele ocorre quando o usuário clica em um item na barra de menus ou pressiona uma tecla de menu. Isso permite que o aplicativo modifique o menu antes que ele seja exibido. <br/> Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |
| [**QUERYUISTATE do WM \_**](wm-queryuistate.md)   | Enviado para recuperar o estado da interface do usuário para uma janela.<br/>                                                                                                                                                                                                                                                            |
| [**UPDATEUISTATE do WM \_**](wm-updateuistate.md) | Enviado para alterar o estado da interface do usuário para a janela especificada e todas as suas janelas filhas.<br/>                                                                                                                                                                                                                        |



 

### <a name="keyboard-accelerator-notifications"></a>Notificações do acelerador de teclado



| Nome                                          | Descrição                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INITMENUPOPUP do WM \_**](wm-initmenupopup.md) | Enviado quando um menu suspenso ou submenu está prestes a ficar ativo. Isso permite que um aplicativo modifique o menu antes que ele seja exibido, sem alterar o menu inteiro. <br/>                                                                                                                                              |
| [**MENUCHAR do WM \_**](wm-menuchar.md)           | Enviado quando um menu está ativo e o usuário pressiona uma tecla que não corresponde a nenhum mnemônico ou tecla de aceleração. Essa mensagem é enviada para a janela que possui o menu. <br/>                                                                                                                                             |
| [**MENUSELECT do WM \_**](wm-menuselect.md)       | Enviado para a janela do proprietário de um menu quando o usuário seleciona um item de menu. <br/>                                                                                                                                                                                                                                                      |
| [**SYSCHAR do WM \_**](wm-syschar.md)             | Postado na janela com o foco do teclado quando uma mensagem do [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) é convertida pela função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . Especifica o código de caractere de uma chave de caractere do sistema que é uma tecla de caractere que é pressionada enquanto a tecla ALT está inativa. <br/> |
| [**SYSCOMMAND do WM \_**](wm-syscommand.md)       | Uma janela recebe essa mensagem quando o usuário escolhe um comando no menu **janela** ou quando o usuário escolhe o botão Maximizar, o botão minimizar, o botão restaurar ou o botão fechar.<br/>                                                                                                                                |



 

### <a name="keyboard-accelerator-structures"></a>Estruturas do acelerador de teclado



| Nome                   | Descrição                                                          |
|------------------------|----------------------------------------------------------------------|
| [**DA aceleração extra**](/windows/win32/api/winuser/ns-winuser-accel) | Define uma chave de acelerador usada em uma tabela de acelerador. <br/> |



 

 

