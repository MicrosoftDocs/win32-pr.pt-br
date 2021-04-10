---
title: Sobre os controles de dica de ferramenta
description: As dicas de ferramentas são exibidas automaticamente ou aparecem quando o usuário pausa o ponteiro do mouse sobre uma ferramenta ou algum outro elemento da interface do usuário.
ms.assetid: 1020cec7-57b4-4463-9419-f80fd14fa12c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9c1042523c86e794865da5d38fb023ee37d60b4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008445"
---
# <a name="about-tooltip-controls"></a>Sobre os controles de dica de ferramenta

As dicas de ferramentas são exibidas automaticamente ou aparecem quando o usuário pausa o ponteiro do mouse sobre uma ferramenta ou algum outro elemento da interface do usuário. A dica de ferramenta aparece perto do ponteiro e desaparece quando o usuário clica em um botão do mouse, move o ponteiro para longe da ferramenta ou simplesmente aguarda alguns segundos.

O controle ToolTip na ilustração a seguir exibe informações sobre um arquivo na área de trabalho do Windows. À medida que move o mouse sobre a ilustração, você também deve ver uma dica de ferramenta em tempo real que contém texto descritivo.

![captura de tela mostrando texto em uma dica de ferramenta que aparece em um arquivo na área de trabalho](images/tt-desktop.png)

Esta seção descreve como a dica de ferramenta controla o trabalho e como criá-los.

-   [Comportamento e aparência da dica de ferramenta](#tooltip-behavior-and-appearance)
-   [Criando controles de dica de ferramenta](#creating-tooltip-controls)
-   [Ativando controles de dica de ferramenta](#activating-tooltip-controls)
-   [Ferramentas de suporte](#supporting-tools)
-   [Exibindo texto](#displaying-text)
-   [Mensagens e notificação](#messaging-and-notification)
-   [Testes de clique](#hit-testing)
-   [Processamento de mensagens padrão](#default-message-processing)

## <a name="tooltip-behavior-and-appearance"></a>Comportamento e aparência da dica de ferramenta

Os controles ToolTip podem exibir uma única linha de texto ou várias linhas. Seus cantos podem ser arredondados ou quadrados. Eles podem ou não ter uma haste que aponte para as ferramentas como um balão de fala. O texto da dica de ferramenta pode ser fixo ou pode ser movido com o ponteiro do mouse, chamado acompanhamento. O texto fixo pode ser exibido ao lado de uma ferramenta ou pode ser exibido em uma ferramenta, que é conhecida como in-loco. As dicas de ferramenta padrão são listadas, exibem uma única linha de texto, têm cantos quadrados e não têm nenhuma haste apontando para a ferramenta.

Rastrear dicas de ferramenta, que têm suporte da [versão 4,70](common-control-versions.md) dos controles comuns, alteram a posição na tela dinamicamente. Ao atualizar rapidamente a posição, esses controles de dica de ferramenta parecem se mover suavemente ou "rastrear". Eles são úteis quando você deseja que o texto da dica de ferramenta siga a posição do ponteiro do mouse à medida que ele se move. Para obter mais informações sobre como controlar dicas de ferramentas e um exemplo com código que mostra como criá-las, consulte [rastrear dicas de ferramenta](using-tooltip-contro.md).

As dicas de ferramentas de várias linhas, que também são suportadas pela versão 4,70 dos controles comuns, exibem texto em mais de uma linha. Eles são úteis para exibir mensagens longas. Para obter mais informações e um exemplo que mostra como criar dicas de ferramentas de várias linhas, consulte [Tooltips de várias linhas](using-tooltip-contro.md).

As dicas de ferramentas de balão são exibidas em uma caixa com cantos arredondados e uma haste apontando para a ferramenta. Eles podem ser de linha única ou multilinha. A ilustração a seguir mostra uma dica de ferramenta de balão com a haste e o retângulo em suas posições padrão. Para obter mais informações sobre dicas de ferramentas de balão e um exemplo que mostra como criá-las, consulte [usando controles de dica de ferramenta](using-tooltip-contro.md).

![captura de tela mostrando uma dica de ferramenta contendo uma linha de texto, posicionada acima de um botão em uma caixa de diálogo](images/tt-balloon.png)

Uma dica de ferramenta também pode ter texto de título e um ícone, conforme mostrado na ilustração a seguir. Observe que a dica de ferramenta deve ter texto; Se ele tiver apenas o texto do título, a dica de ferramenta não será exibida. Além disso, o ícone não aparece, a menos que haja um título.

![captura de tela mostrando uma dica de ferramenta com um ícone, título e texto, posicionado abaixo de um botão em uma caixa de diálogo](images/tt-titled.png)

Às vezes, as cadeias de caracteres de texto são recortadas porque são muito longas para serem exibidas completamente em uma pequena janela. As dicas de ferramenta in-loco são usadas para exibir cadeias de caracteres de texto para objetos que foram recortados, como o nome do arquivo na ilustração a seguir. Para obter um exemplo que mostra como criar dicas de ferramenta in-loco, consulte [tooltips](using-tooltip-contro.md)in-loco.

![captura de tela mostrando uma dica de ferramenta que contém um nome de arquivo posicionado ao lado de um ícone de arquivo em um controle de árvore](images/tt-inplace.png)

O cursor deve focalizar uma ferramenta por um período de tempo antes que a dica de ferramentas seja exibida. A duração padrão desse tempo limite é controlada pelo tempo de clique duplo do usuário e geralmente é cerca de um meio segundo. Para especificar um valor de tempo limite não padrão, envie a dica de ferramenta controle uma mensagem [**TTM \_ SetDelayTime**](ttm-setdelaytime.md) .

## <a name="creating-tooltip-controls"></a>Criando controles de dica de ferramenta

Para criar um controle ToolTip, chame [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especifique a classe da janela [**tooltips da \_ classe**](common-control-window-classes.md) . Essa classe é registrada quando a DLL de controle comum é carregada. Para garantir que essa DLL seja carregada, inclua a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) em seu aplicativo. Você deve definir explicitamente um controle ToolTip como o primeiro. Caso contrário, ele pode ser coberto pela janela pai. O fragmento de código a seguir mostra como criar um controle ToolTip.


```
HWND hwndTip = CreateWindowEx(NULL, TOOLTIPS_CLASS, NULL,
                            WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            hwndParent, NULL, hinstMyDll,
                            NULL);

SetWindowPos(hwndTip, HWND_TOPMOST,0, 0, 0, 0,
             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);
```



O procedimento de janela do controle ToolTip define automaticamente o tamanho, a posição e a visibilidade do controle. A altura da janela de dica de ferramenta é baseada na altura da fonte selecionada atualmente no contexto do dispositivo para o controle ToolTip. A largura varia com base no comprimento da cadeia de caracteres que está atualmente na janela de dica de ferramenta.

## <a name="activating-tooltip-controls"></a>Ativando controles de dica de ferramenta

Um controle ToolTip pode ser ativo ou inativo. Quando ele estiver ativo, o texto da dica de ferramenta aparecerá quando o ponteiro do mouse estiver em um Tool. Quando ele estiver inativo, o texto da dica de ferramenta não será exibido, mesmo se o ponteiro estiver em um Tool. A mensagem de [**\_ ativação TTM**](ttm-activate.md) ativa e desativa um controle ToolTip.

## <a name="supporting-tools"></a>Ferramentas de suporte

Um controle ToolTip pode dar suporte A qualquer número de ferramentas. Para dar suporte a uma ferramenta específica, você deve registrar a ferramenta com o controle ToolTip enviando o controle da mensagem [**TTM \_ AddTool**](ttm-addtool.md) . A mensagem inclui o endereço de uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , que fornece informações de que o controle ToolTip precisa para exibir o texto da ferramenta. O membro **UID** da estrutura **TOOLINFO** é definido pelo aplicativo. Cada vez que você adiciona uma ferramenta, seu aplicativo fornece um identificador exclusivo. O membro **cbSize** da estrutura **TOOLINFO** é necessário e deve especificar o tamanho da estrutura.

Um controle ToolTip oferece suporte a ferramentas implementadas como Windows (como janelas filhas ou janelas de controle) e como áreas retangulares dentro da área do cliente da janela. Quando você adiciona uma ferramenta implementada como uma área retangular, o membro **HWND** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) deve especificar o identificador para a janela que contém a área e o membro **Rect** deve especificar as coordenadas do cliente do retângulo delimitador da área. Além disso, o membro **UID** deve especificar o identificador definido pelo aplicativo para a ferramenta.

Quando você adiciona uma ferramenta implementada como uma janela, o membro **UID** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) deve conter o identificador de janela para a ferramenta. Além disso, o membro **uFlags** deve especificar o valor de **\_ IDISHWND de TTF** , que diz ao controle ToolTip para interpretar o membro **UID** como um identificador de janela.

## <a name="displaying-text"></a>Exibindo texto

Quando você adiciona uma ferramenta a um controle ToolTip, o membro **lpszText** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) deve especificar o endereço da cadeia de caracteres a ser exibida para a ferramenta. Depois de adicionar uma ferramenta, você pode alterar o texto usando a mensagem [**TTM \_ UPDATETIPTEXT**](ttm-updatetiptext.md) .

Se a palavra de ordem superior de **lpszText** for zero, a palavra de ordem inferior deverá ser o identificador de um recurso de cadeia de caracteres. Quando o controle ToolTip precisar do texto, o sistema carregará o recurso de cadeia de caracteres especificado da instância do aplicativo identificada pelo membro **hinst** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .

Se você especificar o \_ valor de MONOcallback de LPSTR no membro **lpszText** , o controle ToolTip notificará a janela especificada no membro **hWnd** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)sempre que o controle ToolTip precisar exibir o texto para a ferramenta. O controle ToolTip envia o código de notificação [TTN \_ GETDISPINFO](ttn-getdispinfo.md) para a janela. A mensagem inclui o endereço de uma estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) , que contém o identificador de janela, bem como o identificador definido pelo aplicativo para a ferramenta. A janela examina a estrutura para determinar a ferramenta para a qual o texto é necessário e preenche os membros da estrutura apropriados com informações que o controle ToolTip precisa para exibir a cadeia de caracteres.

> [!Note]  
> O comprimento máximo do texto da dica de ferramenta padrão é de 80 caracteres. Para obter mais informações, consulte a estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) . O texto da dica de ferramenta de várias linhas pode ser maior.

 

Muitos aplicativos criam barras de ferramentas contendo ferramentas que correspondem aos comandos de menu. Para essas ferramentas, é conveniente que o controle ToolTip Exiba o mesmo texto que o item de menu correspondente. O sistema remove automaticamente os caracteres de acelerador de e comercial (&) de todas as cadeias passadas para um controle de dica de ferramenta e encerra a cadeia de caracteres no primeiro caractere de tabulação ( \\ t), a menos que o controle tenha o estilo [**\_ noprefixo TTS**](tooltip-styles.md) .

Para recuperar o texto de uma ferramenta, use a mensagem [**TTM \_ gettext**](ttm-gettext.md) .

## <a name="messaging-and-notification"></a>Mensagens e notificação

O texto da dica de ferramenta normalmente é exibido quando o ponteiro do mouse passa sobre uma área, normalmente o retângulo definido por uma ferramenta como um controle de botão. No entanto, o Microsoft Windows só envia mensagens relacionadas ao mouse para a janela que contém o ponteiro, não o controle ToolTip em si. As informações relacionadas ao mouse devem ser retransmitidas para o controle ToolTip para que ele exiba o texto da dica de ferramenta na hora e no local apropriados.

Você poderá fazer com que as mensagens sejam retransmitidas automaticamente se:

-   A ferramenta é um controle ou é definida como um retângulo na estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) da ferramenta.
-   A janela associada à ferramenta está no mesmo thread que o controle ToolTip.

Se essas duas condições forem atendidas, defina o sinalizador de **\_ subclasse ttf** no membro **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) da ferramenta ao adicionar a ferramenta ao controle ToolTip com [**TTM \_ addferramenta**](ttm-addtool.md). As mensagens de mouse necessárias serão retransmitidas automaticamente para o controle ToolTip.

A configuração da **\_ subclasse ttf** para que as mensagens do mouse sejam retransmitidas para o controle é suficiente para a maioria das finalidades. No entanto, ele não funcionará em casos em que não haja nenhuma conexão direta entre o controle ToolTip e a janela da ferramenta. Por exemplo, se uma ferramenta for implementada como uma área retangular em uma janela definida pelo aplicativo, o procedimento de janela receberá as mensagens do mouse. A configuração da **\_ subclasse ttf** é suficiente para garantir que elas sejam passadas para o controle. No entanto, se uma ferramenta for implementada como uma janela definida pelo sistema, as mensagens do mouse serão enviadas para essa janela e não estarão diretamente disponíveis para o aplicativo. Nesse caso, você deve fazer uma subclasse da janela ou usar um gancho de mensagem para acessar as mensagens do mouse. Você deve retransmitir explicitamente as mensagens do mouse para o controle ToolTip com [**TTM \_ RELAYEVENT**](ttm-relayevent.md). Para obter um exemplo de como usar **TTM \_ RELAYEVENT**, consulte [rastrear dicas de ferramenta](using-tooltip-contro.md).

Quando um controle ToolTip recebe uma [**mensagem \_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) , ele determina se o ponteiro do mouse está no retângulo delimitador de uma ferramenta. Se for, o controle ToolTip definirá um timer. No final do intervalo de tempo limite, o controle ToolTip verifica a posição do ponteiro para ver se ele foi movido. Se não tiver, o controle ToolTip recuperará o texto para a ferramenta e exibirá a ToolTip. O controle ToolTip continua mostrando a janela até receber uma mensagem retransmitida ou de botão para baixo ou até que uma mensagem do **WM \_ MOUSEMOVE** indique que o ponteiro foi movido para fora do retângulo delimitador da ferramenta.

Um controle ToolTip tem, na verdade, três durações de tempo limite associadas a ela. A duração inicial é a hora em que o ponteiro do mouse deve permanecer parado dentro do retângulo delimitador de uma ferramenta antes que a janela de dica de ferramentas seja exibida. A duração da reexibição é o comprimento do atraso antes que janelas de dica de ferramenta subsequentes sejam exibidas quando o ponteiro se move de uma das ferramentas para outra. A duração do pop-up é a hora em que a janela de dica de ferramenta permanece exibida antes de ser ocultada. Ou seja, se o ponteiro permanecer parado dentro do retângulo delimitador depois que a janela de dica de ferramenta for exibida, a janela de dica de ferramenta será ocultada automaticamente no final da duração do pop-up. Você pode ajustar todas as durações de tempo limite usando a mensagem [**TTM \_ SetDelayTime**](ttm-setdelaytime.md) .

Se um aplicativo incluir uma ferramenta implementada como uma área retangular e o tamanho ou a posição do controle for alterado, o aplicativo poderá usar a mensagem [**TTM \_ NEWTOOLRECT**](ttm-newtoolrect.md) para relatar a alteração para o controle ToolTip. Um aplicativo não precisa relatar alterações de tamanho e posição para uma ferramenta implementada como uma janela porque o controle ToolTip usa o identificador de janela da ferramenta para determinar se o ponteiro do mouse está na ferramenta, não no retângulo delimitador da ferramenta.

Quando uma dica de ferramenta está prestes a ser exibida, o controle ToolTip envia à janela do proprietário um código de notificação [TTN \_ show](ttn-show.md) . A janela do proprietário recebe um código de notificação [ \_ pop TTN](ttn-pop.md) quando uma dica de ferramenta está prestes a ser ocultada. Cada código de notificação é enviado no contexto de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .

## <a name="hit-testing"></a>Testes de clique

A mensagem [**TTM \_ HITTEST**](ttm-hittest.md) permite que você recupere informações que um controle ToolTip mantém sobre a ferramenta que ocupa um determinado ponto. A mensagem inclui uma estrutura [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) que contém um identificador de janela, as coordenadas de um ponto e o endereço de uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . O controle ToolTip determina se uma ferramenta ocupa o ponto e, se tiver, preenche **TOOLINFO** com informações sobre a ferramenta.

## <a name="default-message-processing"></a>Processamento de mensagens padrão

A tabela a seguir descreve as mensagens tratadas pelo procedimento de janela para o controle ToolTip.



| Mensagem                                        | Descrição                                                                                                                                                                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**criação do WM \_**](/windows/desktop/winmsg/wm-create)             | Garante que o controle ToolTip tenha os estilos de janela [**WS \_ ex \_ TOOLWINDOW**](/windows/desktop/winmsg/window-styles) e [**WS \_ Popup**](/windows/desktop/winmsg/window-styles) . Ele também aloca memória e inicializa variáveis internas. |
| [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)           | Libera recursos alocados para o controle ToolTip.                                                                                                                                                                                                                |
| [**WM \_ GETfont**](/windows/desktop/winmsg/wm-getfont)           | Retorna o identificador da fonte que o controle ToolTip usará para desenhar texto.                                                                                                                                                                                    |
| [**admousemove do WM \_**](/windows/desktop/inputdev/wm-mousemove)     | Oculta a janela de dica de ferramenta.                                                                                                                                                                                                                                         |
| [**pintura do WM \_**](/windows/desktop/gdi/wm-paint)                  | Desenha a janela de dica de ferramenta.                                                                                                                                                                                                                                         |
| [**WM \_ SETfont**](/windows/desktop/winmsg/wm-setfont)           | Define o identificador da fonte que o controle ToolTip usará para desenhar texto.                                                                                                                                                                                       |
| [**\_temporizador do WM**](/windows/desktop/winmsg/wm-timer)               | Oculta a janela ToolTip se a ferramenta tiver mudado de posição ou se o ponteiro do mouse tiver se movido para fora da ferramenta. Caso contrário, ele mostra a janela de dica de ferramenta.                                                                                                             |
| [**WININICHANGE do WM \_**](/windows/desktop/winmsg/wm-wininichange) | Redefine as variáveis internas baseadas em métricas do sistema.                                                                                                                                                                                                       |



 

 

 