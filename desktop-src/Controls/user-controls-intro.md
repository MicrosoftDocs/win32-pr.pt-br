---
title: Controles personalizados
description: Esta seção contém informações sobre controles personalizados ou definidos pelo aplicativo.
ms.assetid: 220f7058-db04-46d0-acee-ed5e676790b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d1a31a44f1f71d99088f7729c2de6d5fdb597e14507f5f994dfaca1b96613d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059706"
---
# <a name="custom-controls"></a>Controles personalizados

Esta seção contém informações sobre controles personalizados ou definidos pelo aplicativo.

Os tópicos a seguir são discutidos.

-   [Criando controles Owner-Drawn dados](#creating-owner-drawn-controls)
-   [Subclasse da classe window de um controle existente](#subclassing-the-window-class-of-an-existing-control)
-   [Implementando uma classe Application-Defined janela](#implementing-an-application-defined-window-class)
-   [Enviando notificações de um controle](#sending-notifications-from-a-control)
-   [Acessibilidade](#accessibility)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-owner-drawn-controls"></a>Criando controles Owner-Drawn dados

Botões, menus, controles de texto estático, caixas de listagem e caixas de combinação podem ser criados com um sinalizador de estilo desenhado pelo proprietário. Quando um controle tem o estilo desenhado pelo proprietário, o sistema lida com a interação do usuário com o controle como de costume, executando tarefas como detectar quando um usuário escolheu um botão e notificar o proprietário do evento do botão. No entanto, como o controle é desenhado pelo proprietário, a janela pai do controle é responsável pela aparência visual do controle. A janela pai recebe uma mensagem sempre que o controle deve ser desenhado.

Para botões e controles de texto estático, o estilo desenhado pelo proprietário afeta como o sistema desenha todo o controle. Para caixas de listagem e caixas de combinação, a janela pai desenha os itens dentro do controle e o controle desenha seu próprio contorno. Por exemplo, um aplicativo pode personalizar uma caixa de listagem para exibir um bitmap pequeno ao lado de cada item na lista.

O código de exemplo a seguir mostra como criar um controle de texto estático desenhado pelo proprietário. Suponha que Unicode está definido.


```
// g_myStatic is a global HWND variable.
g_myStatic = CreateWindowEx(0, L"STATIC", L"Some static text", 
            WS_CHILD | WS_VISIBLE | SS_OWNERDRAW, 
            25, 125, 150, 20, hDlg, 0, 0, 0);
```



No exemplo a seguir, no procedimento de janela da caixa de diálogo que contém o controle criado no exemplo anterior, a mensagem [**WM \_ DRAWITEM**](wm-drawitem.md) é tratada exibindo o texto em uma cor personalizada, usando a fonte padrão. Observe que você não precisa chamar [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) ao manipular **WM \_ DRAWITEM.**


```
case WM_DRAWITEM:
{
    LPDRAWITEMSTRUCT pDIS = (LPDRAWITEMSTRUCT)lParam;
    if (pDIS->hwndItem == g_myStatic)
    {
        SetTextColor(pDIS->hDC, RGB(100, 0, 100));
        WCHAR staticText[99];
        int len = SendMessage(myStatic, WM_GETTEXT, 
            ARRAYSIZE(staticText), (LPARAM)staticText);
        TextOut(pDIS->hDC, pDIS->rcItem.left, pDIS->rcItem.top, staticText, len);
    }
    return TRUE;
}
```



Para obter mais informações sobre controles desenhados pelo proprietário, consulte Criando uma caixa de [listagem](using-list-boxes.md) desenhada pelo proprietário e [Caixas de combinação desenhadas pelo proprietário](about-combo-boxes.md).

## <a name="subclassing-the-window-class-of-an-existing-control"></a>Subclasse da classe window de um controle existente

A subclasse de um controle existente é outra maneira de criar um controle personalizado. O procedimento de subclasse pode alterar os comportamentos selecionados do controle processando as mensagens que afetam os comportamentos selecionados. Todas as outras mensagens passam para o procedimento de janela original para o controle . Por exemplo, um aplicativo pode exibir um bitmap pequeno ao lado do texto em um controle de edição de linha única somente leitura, subclassando o controle e processando a mensagem [**WM \_ PAINT.**](/windows/desktop/gdi/wm-paint) Para obter mais informações, consulte [Sobre procedimentos de janela](/windows/desktop/winmsg/about-window-procedures) e [controles de subclasse](subclassing-overview.md).

## <a name="implementing-an-application-defined-window-class"></a>Implementando uma classe Application-Defined janela

Para criar um controle que não é explicitamente baseado em um controle existente, o aplicativo deve criar e registrar uma classe de janela. O processo para registrar uma classe de janela definida pelo aplicativo para um controle personalizado é o mesmo que registrar uma classe para uma janela comum. Para criar um controle personalizado, especifique o nome da classe de janela na [**função CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou em um modelo de caixa de diálogo. Cada classe deve ter um nome exclusivo, um procedimento de janela correspondente e outras informações.

No mínimo, o procedimento de janela desenha o controle . Se um aplicativo usar o controle para permitir que o usuário digite informações, o procedimento de janela também processa mensagens de entrada do teclado e do mouse e envia mensagens de notificação para a janela pai. Além disso, se o controle dá suporte a mensagens de controle, o procedimento de janela processa as mensagens enviadas a ele pela janela pai ou outras janelas. Por exemplo, os controles geralmente processam a mensagem [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode) enviada pelas caixas de diálogo para direcionar uma caixa de diálogo para processar a entrada do teclado de uma determinada maneira.

O procedimento de janela para um controle definido pelo aplicativo deve processar qualquer mensagem de controle predefinida na tabela a seguir se a mensagem afetar a operação do controle.



| Mensagem                                          | Recomendação                                                                                                                                                                                                                                  |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)       | Processe se o controle usar as teclas ENTER, ESC, TAB ou seta. A [**função IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) envia essa mensagem aos controles em uma caixa de diálogo para determinar se as chaves devem ser processadas ou passadas para o controle . |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)             | Processar se a [**mensagem WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) também for processada.                                                                                                                                                                  |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)             | Processe se o texto do controle não for o mesmo que o título especificado pela [**função CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)                                                                                                                 |
| [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) | Processe se o texto do controle não for o mesmo que o título especificado pela [**função CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)                                                                                                                 |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)       | Processe se o controle exibir um sinal de foco, um retângulo de foco ou outro item para indicar que ele tem o foco de entrada.                                                                                                                            |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)         | Processe se o controle exibir um sinal de foco, um retângulo de foco ou outro item para indicar que ele tem o foco de entrada.                                                                                                                            |
| [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)             | Processe se o texto do controle não for o mesmo que o título especificado pela [**função CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)                                                                                                                 |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)             | Processe se o controle exibir texto. O sistema envia essa mensagem ao criar uma caixa de diálogo que tem o estilo \_ SETFONT do DS.                                                                                                                  |



 

As mensagens de controle definidas pelo aplicativo são específicas para o controle determinado e devem ser explicitamente enviadas ao controle usando uma [**função SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ou [**SendDlgItemMessage.**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) O valor numérico de cada mensagem deve ser exclusivo e não deve estar em conflito com os valores de outras mensagens da janela. Para garantir que os valores de mensagem definidos pelo aplicativo não conflitam, um aplicativo deve criar cada valor adicionando um número exclusivo ao [**valor do WM \_ USER.**](/windows/desktop/winmsg/wm-user)

## <a name="sending-notifications-from-a-control"></a>Enviando notificações de um controle

Controles personalizados podem ser necessários para enviar notificações de eventos para a janela pai para que o aplicativo host possa responder a esses eventos. Por exemplo, uma exibição de lista personalizada pode enviar uma notificação quando o usuário seleciona um item e outra notificação quando um item é clicado duas vezes.

As notificações são enviadas como [**mensagens WM \_ COMMAND**](/windows/desktop/menurc/wm-command) ou [**WM \_ NOTIFY.**](wm-notify.md) **WM \_ As mensagens NOTIFY** carregam mais informações do que **as mensagens COMMAND \_ do WM.**

O identificador de controle é um número exclusivo que o aplicativo usa para identificar o controle que envia a mensagem. O aplicativo define o identificador de um controle quando ele cria o controle . O aplicativo especifica o identificador no parâmetro *hMenu* da função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou no membro **id** da estrutura [**DLGITEMTEMPLATEEX.**](/windows/desktop/dlgbox/dlgitemtemplateex)

Como o controle em si não configura o identificador de controle, o controle deve recuperar o identificador antes de poder enviar mensagens de notificação. Um controle deve usar a [**função GetDlgCtrlID**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) para recuperar seu próprio identificador de controle. Embora o identificador de controle seja especificado como o identificador de menu quando o controle é criado, a [**função GetMenu**](/windows/desktop/api/winuser/nf-winuser-getmenu) não pode ser usada para recuperar o identificador. Como alternativa, um controle pode recuperar o identificador do membro **hMenu** na estrutura [**CREATETRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) durante o processamento da [**mensagem WM \_ CREATE.**](/windows/desktop/winmsg/wm-create)

Os exemplos a seguir, em que *hwndControl* é o handle da janela de controle e CN VALUECHANGED é uma definição de notificação personalizada, mostram as duas maneiras de enviar uma notificação específica \_ do controle.


```
 // Send as WM_COMMAND.
SendMessage(GetParent(hwndControl), 
    WM_COMMAND,
    MAKEWPARAM(GetDlgCtrlID(hwndControl), CN_VALUECHANGED),
    (LPARAM)hwndControl);

// Send as WM_NOTIFY.           
NMHDR nmh;
nmh.code = CN_VALUECHANGED;
nmh.idFrom = GetDlgCtrlID(hwndControl);
nmh.hwndFrom = hwndControl;
SendMessage(GetParent(hwndControl), 
    WM_NOTIFY, 
    (WPARAM)hwndControl, 
    (LPARAM)&nmh);
```



Observe que a [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) pode fazer parte de uma estrutura maior definida pelo controle que contém informações adicionais. No exemplo, os valores antigo e novo do controle podem estar contidos nessa estrutura. (Essas estruturas estendidas são usadas com muitas notificações padrão; por exemplo, consulte [LVN \_ INSERTITEM](lvn-insertitem.md), que usa a [**estrutura NMLISTVIEW.)**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)

## <a name="accessibility"></a>Acessibilidade

Todos os controles comuns são Microsoft Active Accessibility (MSAA), que permite o acesso programático por aplicativos de tecnologia acessível, como leitores de tela. A MSAA também permite Automação da Interface do Usuário, uma tecnologia mais nova, interagir com controles.

Os controles personalizados devem implementar a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (para dar suporte à MSAA) ou as interfaces Automação da Interface do Usuário ou ambas. Caso contrário, os produtos de tecnologia acessível poderão obter apenas informações muito limitadas sobre a janela de controle, não terão acesso às propriedades do controle e não poderão disparar eventos no controle.

Para obter mais informações sobre como tornar seu controle acessível, [consulte Windows API de Automação.](/windows/desktop/WinAuto/windows-automation-api-portal)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Referência de controle geral](common-control-reference.md)
</dt> <dt>

[Personalização da aparência de um controle usando desenho personalizado](custom-draw.md)
</dt> <dt>

[Controlar mensagens](control-messages.md)
</dt> <dt>

[Usando estilos visuais com Owner-Drawn controles](using-visual-styles.md)
</dt> </dl>

 

 