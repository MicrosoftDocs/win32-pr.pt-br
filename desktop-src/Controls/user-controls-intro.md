---
title: Controles personalizados
description: Esta seção contém informações sobre controles personalizados ou definidos pelo aplicativo.
ms.assetid: 220f7058-db04-46d0-acee-ed5e676790b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82ed9394ec06257e524153b86ef487f4507f35b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084910"
---
# <a name="custom-controls"></a>Controles personalizados

Esta seção contém informações sobre controles personalizados ou definidos pelo aplicativo.

Os tópicos a seguir são discutidos.

-   [Criando Owner-Drawn controles](#creating-owner-drawn-controls)
-   [Subclasse da classe Window de um controle existente](#subclassing-the-window-class-of-an-existing-control)
-   [Implementando uma classe de janela de Application-Defined](#implementing-an-application-defined-window-class)
-   [Enviando notificações de um controle](#sending-notifications-from-a-control)
-   [Acessibilidade](#accessibility)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-owner-drawn-controls"></a>Criando Owner-Drawn controles

Botões, menus, controles de texto estáticos, caixas de listagem e caixas de combinação podem ser criados com um sinalizador de estilo desenhado pelo proprietário. Quando um controle tem o estilo desenhado pelo proprietário, o sistema manipula a interação do usuário com o controle como de costume, realizando tarefas como detectar quando um usuário escolheu um botão e notificando o proprietário do evento. No entanto, como o controle é desenhado pelo proprietário, a janela pai do controle é responsável pela aparência visual do controle. A janela pai recebe uma mensagem sempre que o controle deve ser desenhado.

Para botões e controles de texto estáticos, o estilo desenhado pelo proprietário afeta como o sistema desenha todo o controle. Para caixas de listagem e caixas de combinação, a janela pai desenha os itens dentro do controle e o controle desenha sua própria estrutura de tópicos. Por exemplo, um aplicativo pode personalizar uma caixa de listagem para que ela exiba um bitmap pequeno ao lado de cada item na lista.

O código de exemplo a seguir mostra como criar um controle de texto estático desenhado pelo proprietário. Suponha que o Unicode esteja definido.


```
// g_myStatic is a global HWND variable.
g_myStatic = CreateWindowEx(0, L"STATIC", L"Some static text", 
            WS_CHILD | WS_VISIBLE | SS_OWNERDRAW, 
            25, 125, 150, 20, hDlg, 0, 0, 0);
```



No exemplo a seguir, do procedimento de janela da caixa de diálogo que contém o controle criado no exemplo anterior, a mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) é manipulada exibindo o texto em uma cor personalizada, usando a fonte padrão. Observe que você não precisa chamar [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) ao manipular o **WM \_ DRAWITEM**.


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



Para obter mais informações sobre os controles desenhados pelo proprietário, consulte [criando uma caixa de listagem desenhada pelo](using-list-boxes.md) proprietário e [caixas de combinação desenhadas pelo proprietário](about-combo-boxes.md).

## <a name="subclassing-the-window-class-of-an-existing-control"></a>Subclasse da classe Window de um controle existente

A criação de uma subclasse de um controle existente é outra maneira de criar um controle personalizado. O procedimento de subclasse pode alterar os comportamentos selecionados do controle processando as mensagens que afetam os comportamentos selecionados. Todas as outras mensagens passam para o procedimento de janela original do controle. Por exemplo, um aplicativo pode exibir um bitmap pequeno ao lado do texto em um controle de edição somente leitura, de linha única, subclassendo o controle e processando a mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) . Para obter mais informações, consulte [sobre procedimentos de janela](/windows/desktop/winmsg/about-window-procedures) e [controles de subclasses](subclassing-overview.md).

## <a name="implementing-an-application-defined-window-class"></a>Implementando uma classe de janela de Application-Defined

Para criar um controle que não seja explicitamente baseado em um controle existente, o aplicativo deve criar e registrar uma classe de janela. O processo para registrar uma classe de janela definida pelo aplicativo para um controle personalizado é o mesmo que registrar uma classe para uma janela comum. Para criar um controle personalizado, especifique o nome da classe de janela na função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou em um modelo de caixa de diálogo. Cada classe deve ter um nome exclusivo, um procedimento de janela correspondente e outras informações.

No mínimo, o procedimento de janela desenha o controle. Se um aplicativo usar o controle para permitir que as informações de tipo de usuário, o procedimento de janela também processará mensagens de entrada do teclado e do mouse e enviará mensagens de notificação para a janela pai. Além disso, se o controle oferecer suporte a mensagens de controle, o procedimento de janela processará as mensagens enviadas a ele pela janela pai ou outras janelas. Por exemplo, os controles geralmente processam a mensagem do [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode) enviada por caixas de diálogo para direcionar uma caixa de diálogo para processar a entrada do teclado de uma maneira determinada.

O procedimento de janela para um controle definido pelo aplicativo deve processar qualquer mensagem de controle predefinida na tabela a seguir se a mensagem afetar a operação do controle.



| Mensagem                                          | Recomendação                                                                                                                                                                                                                                  |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETDLGCODE do WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)       | Processar se o controle usar as teclas ENTER, ESC, TAB ou arrow. A função [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) envia essa mensagem aos controles em uma caixa de diálogo para determinar se as chaves devem ser processadas ou passadas para o controle. |
| [**WM \_ GETfont**](/windows/desktop/winmsg/wm-getfont)             | Processar se a mensagem de [**\_ fonte do WM**](/windows/desktop/winmsg/wm-setfont) também for processada.                                                                                                                                                                  |
| [**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)             | Processar se o texto de controle não for o mesmo que o título especificado pela função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**GETTEXTLENGTH do WM \_**](/windows/desktop/winmsg/wm-gettextlength) | Processar se o texto de controle não for o mesmo que o título especificado pela função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**KILLFOCUS do WM \_**](/windows/desktop/inputdev/wm-killfocus)       | Processar se o controle exibir um cursor, um retângulo de foco ou outro item para indicar que ele tem o foco de entrada.                                                                                                                            |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)         | Processar se o controle exibir um cursor, um retângulo de foco ou outro item para indicar que ele tem o foco de entrada.                                                                                                                            |
| [**SetText do WM \_**](/windows/desktop/winmsg/wm-settext)             | Processar se o texto de controle não for o mesmo que o título especificado pela função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .                                                                                                                 |
| [**WM \_ SETfont**](/windows/desktop/winmsg/wm-setfont)             | Processar se o controle exibir texto. O sistema envia essa mensagem ao criar uma caixa de diálogo com o estilo de fonte de domínio \_ .                                                                                                                  |



 

As mensagens de controle definidas pelo aplicativo são específicas para o controle fornecido e devem ser enviadas explicitamente ao controle usando uma função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ou [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) . O valor numérico de cada mensagem deve ser exclusivo e não deve entrar em conflito com os valores de outras mensagens da janela. Para garantir que os valores de mensagem definidos pelo aplicativo não entrem em conflito, um aplicativo deve criar cada valor adicionando um número exclusivo ao valor de [**\_ usuário do WM**](/windows/desktop/winmsg/wm-user) .

## <a name="sending-notifications-from-a-control"></a>Enviando notificações de um controle

Controles personalizados podem ser necessários para enviar notificações de eventos para a janela pai para que o aplicativo host possa responder a esses eventos. Por exemplo, um modo de exibição de lista personalizado pode enviar uma notificação quando o usuário seleciona um item e outra notificação quando um item é clicado duas vezes.

As notificações são enviadas [**como \_ comando do WM**](/windows/desktop/menurc/wm-command) ou mensagens de [**\_ notificação do WM**](wm-notify.md) . **WM \_ NOTIFICAr** mensagens que contêm mais informações do que as mensagens de **\_ comando do WM** .

O identificador de controle é um número exclusivo que o aplicativo usa para identificar o controle que envia a mensagem. O aplicativo define o identificador para um controle quando ele cria o controle. O aplicativo especifica o identificador no parâmetro *HMENU* da função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou no membro **ID** da estrutura [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) .

Como o próprio controle não define o identificador de controle, o controle deve recuperar o identificador antes de poder enviar mensagens de notificação. Um controle deve usar a função [**GetDlgCtrlID**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) para recuperar seu próprio identificador de controle. Embora o identificador de controle seja especificado como o identificador de menu quando o controle é criado, a função [**GetMenu**](/windows/desktop/api/winuser/nf-winuser-getmenu) não pode ser usada para recuperar o identificador. Como alternativa, um controle pode recuperar o identificador do membro **HMENU** na estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) durante o processamento da mensagem [**de \_ criação do WM**](/windows/desktop/winmsg/wm-create) .

Os exemplos a seguir, em que *hwndControl* é o identificador da janela de controle e CN \_ VALUECHANGED é uma definição de notificação personalizada, mostram as duas maneiras de enviar uma notificação específica do controle.


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



Observe que a estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) pode fazer parte de uma estrutura maior definida pelo controle que contém informações adicionais. No exemplo, os valores antigos e novos do controle podem estar contidos nessa estrutura. (Essas estruturas estendidas são usadas com muitas notificações padrão; por exemplo, consulte [LVN \_ INSERTITEM](lvn-insertitem.md), que usa a estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .)

## <a name="accessibility"></a>Acessibilidade

Todos os controles comuns dão suporte ao Microsoft Acessibilidade Ativa (MSAA), que permite o acesso programático por aplicativos de tecnologia acessível, como leitores de tela. A MSAA também habilita a automação da interface do usuário, uma tecnologia mais nova, para interagir com controles.

Os controles personalizados devem implementar a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (para oferecer suporte a MSAA) ou as interfaces de automação da interface do usuário, ou ambas. Caso contrário, os produtos de tecnologia acessível poderão obter apenas informações muito limitadas sobre a janela de controle, não terão acesso às propriedades do controle e não poderão disparar eventos no controle.

Para obter mais informações sobre como tornar seu controle acessível, consulte [API de automação do Windows](/windows/desktop/WinAuto/windows-automation-api-portal).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Referência de controle geral](common-control-reference.md)
</dt> <dt>

[Personalizando a aparência de um controle usando o desenho personalizado](custom-draw.md)
</dt> <dt>

[Mensagens de controle](control-messages.md)
</dt> <dt>

[Usando estilos visuais com controles Owner-Drawn](using-visual-styles.md)
</dt> </dl>

 

 