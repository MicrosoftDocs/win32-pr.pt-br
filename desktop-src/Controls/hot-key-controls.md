---
title: Sobre controles de teclas de acesso
description: Um controle de tecla ativa é uma janela que permite que o usuário insira uma combinação de teclas a serem usadas como uma tecla de acesso.
ms.assetid: 5f011459-4c30-45d4-9668-19f575b041ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5e0c0f9a0ddec515c1732863333b7c1a878db5
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423876"
---
# <a name="about-hot-key-controls"></a>Sobre controles de teclas de acesso

Um controle de tecla ativa é uma janela que permite que o usuário insira uma combinação de teclas a serem usadas como uma tecla de acesso. Uma tecla de tecla quente é uma combinação de teclas que o usuário pode pressionar para executar uma ação rapidamente. Por exemplo, um usuário pode criar uma tecla quente que ativa uma determinada janela e a leva para a parte superior da ordem z. O controle de teclas de acesso exibe as escolhas do usuário e garante que o usuário selecione uma combinação de chaves válida. A captura de tela a seguir mostra como um controle de tecla quente aparece em uma caixa de diálogo depois que o usuário pressiona a tecla Alt.

![captura de tela de uma caixa de diálogo que contém um controle de tecla quente](images/hotkey.png)

## <a name="using-hot-key-controls"></a>Usando controles de teclas de acesso

Quando o usuário ins ins muita chave a ser usada como uma tecla de acesso, os nomes das chaves aparecem no controle de teclas ativas. Uma combinação de teclas pode consistir em uma tecla modificadora (como CTRL, ALT ou SHIFT) e uma tecla que o acompanha (como uma tecla de caractere, uma tecla de seta, uma tecla de função e assim por diante).

Depois que o usuário escolher uma combinação de chaves, o aplicativo recuperará a combinação de chaves do controle de teclas de acesso e a usará para configurar uma chave quente no sistema. As informações recuperadas do controle de teclas ativas incluem um sinalizador que indica a chave modificadora e o código da chave virtual da chave que o acompanha.

O aplicativo pode usar as informações fornecidas por um controle de tecla quente para configurar uma tecla de acesso global ou uma tecla de acesso específica do thread. Uma tecla de hot global está associada a uma janela específica; ele permite que o usuário ative a janela de qualquer parte do sistema. Um aplicativo define uma chave de acesso global usando a [**mensagem WM \_ SETHOTKEY.**](/windows/desktop/inputdev/wm-sethotkey) Sempre que o usuário pressiona uma tecla de acesso global, a janela especificada em **WM \_ SETHOTKEY** recebe uma mensagem [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) que especifica o [**valor SC \_ HOTKEY.**](/windows/desktop/inputdev/wm-sethotkey) Essa mensagem ativa a janela que a recebe. A tecla de acesso permanece válida até que o aplicativo que chamou o **WM \_ setteclaize** saia.

Uma tecla de acesso específica a um thread gera uma mensagem de [**\_ tecla de atalho do WM**](/windows/desktop/inputdev/wm-hotkey) que é postada no início de um thread específico para que ele seja removido pela próxima iteração do loop de mensagem. Um aplicativo define uma chave de acesso específica ao thread usando a função [**RegisterHotKey**](/windows/desktop/api/winuser/nf-winuser-registerhotkey) .

### <a name="hot-key-control-messages"></a>Mensagens de controle de tecla quente

Depois de criar um controle de tecla de atalho, um aplicativo interage com ele usando três mensagens: [**hkm \_ SetRules**](hkm-setrules.md), hkm set e [**hkm \_ gettecla**](hkm-gethotkey.md). [**\_**](hkm-sethotkey.md)

Um aplicativo pode enviar a mensagem [**hkm \_ SetRules**](hkm-setrules.md) para especificar um conjunto de combinações de teclas CTRL, ALT e Shift que são consideradas chaves de acesso inválidas. Se o aplicativo especificar uma combinação de chave inválida, ele também deverá especificar uma combinação de modificador padrão a ser usada quando o usuário selecionar a combinação inválida. Quando o usuário insere a combinação inválida, o sistema executa uma operação OR lógica na combinação inválida e a combinação padrão. O resultado é considerado uma combinação válida; Ele é convertido em uma cadeia de caracteres e exibido no controle.

A [**mensagem \_ settecla hkm**](hkm-sethotkey.md) permite que um aplicativo defina a combinação de teclas de acesso para um controle de tecla de atalho. Essa mensagem também é usada normalmente quando o controle de teclas de acesso é criado.

Os aplicativos usam a mensagem [**hkm \_ getteclaize**](hkm-gethotkey.md) para recuperar o código de chave virtual e os sinalizadores de modificador da tecla de atalho escolhida pelo usuário.

### <a name="hot-key-control-notifications"></a>Notificações de controle de tecla quente

O controle de teclas de acesso não envia nenhum código de notificação por meio da mensagem de [**\_ notificação do WM**](wm-notify.md) . No entanto, será enviada a notificação de [ \_ alteração en](en-change.md) por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) quando o usuário alterar o conteúdo do controle.

### <a name="default-hot-key-message-processing"></a>Processamento de mensagem de tecla de atalho padrão

Esta seção descreve as mensagens de janela manipuladas pelo procedimento de janela para a classe de janela [**HOTKEY \_ CLASS**](common-control-window-classes.md) pré-definida usada com controles de teclas de acesso.

|    Mensagem                                            |    Processamento executado                               |
|------------------------------------------------|--------------------------------------------------------------|
| [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)               | Recupera o código da chave virtual.             |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)             | Inicializa o controle de teclas de acesso, limpa as regras de teclas de acesso e usa a fonte do sistema.   |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)     | Oculta o aro, chama a [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e mostra o aro novamente.   |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)     | Retorna uma combinação dos valores [**\_ WANTCHARS e DLGC**](/windows/desktop/dlgbox/wm-getdlgcode) [**\_ WANTARROWS do DLGC.**](/windows/desktop/dlgbox/wm-getdlgcode)   |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)           | Recupera a fonte.                         |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)         | Chamará [**a função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) se a chave for ENTER, TAB, BARRA DE ESPAÇOS, DEL, ESC ou BACKSPACE. Se a chave for SHIFT, CTRL ou ALT, ela verificará se a combinação é válida e, se for, definirá a tecla quente usando a combinação. Todas as outras chaves são definidas como teclas de acesso sem que sua validade seja verificada primeiro. |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)             | Recupera o código da chave virtual.             |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)     | Destrói o a careta.                         |
| [**LBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-lbuttondown) | Define o foco para a janela.               |
| [**NCCREATE do WM \_**](/windows/desktop/winmsg/wm-nccreate)         | Define o estilo de janela [**WS \_ ex \_ CLIENTEDGE**](/windows/desktop/winmsg/extended-window-styles) .        |
| [**pintura do WM \_**](/windows/desktop/gdi/wm-paint)                  | Pinta o controle de tecla de atalho.                 |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)       | Cria e mostra o cursor.                |
| [**WM \_ SETfont**](/windows/desktop/winmsg/wm-setfont)           | Define a fonte.                              |
| [**SYSCHAR do WM \_**](/windows/desktop/menurc/wm-syschar)           | Recupera o código de chave virtual.             |
| [**SYSKEYDOWN do WM \_**](/windows/desktop/inputdev/wm-syskeydown)   | Chama a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) se a chave estiver inserida, Tab, barra de espaço, del, ESC ou Backspace. Se a chave for SHIFT, CTRL ou ALT, ela verificará se a combinação é válida e, se for, define a tecla de acesso usando a combinação. Todas as outras chaves são definidas como teclas de acesso sem que a validade seja verificada primeiro. |
| [**SYSKEYUP do WM \_**](/windows/desktop/inputdev/wm-syskeyup)       | Recupera o código de chave virtual.             |
