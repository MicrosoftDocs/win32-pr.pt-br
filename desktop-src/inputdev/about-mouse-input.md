---
title: Sobre a entrada do mouse
description: Este tópico discute a entrada do mouse.
ms.assetid: 1f945a31-76d5-4e23-a55a-769ca114dbe9
keywords:
- entrada do usuário, entrada do mouse
- capturando entrada do usuário, entrada do mouse
- entrada do mouse
- cursor do mouse
- cursores, entrada do mouse
- captura de mouse
- mouse ClickLock
- XBUTTONs
- configuração do mouse
- mensagens do mouse
- WM_NCHITTEST mensagem
- Recurso de acessibilidade do Mouse Accessibilit
- Recurso de acessibilidade do Sonar do Mouse
- roda do mouse
- WM_MOUSEWHEEL mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c4978babd6322102908699dbf88b68e2d3b92f57fa9bfa79b9b8c3eae88931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105785"
---
# <a name="about-mouse-input"></a>Sobre a entrada do mouse

O mouse é um dispositivo importante, mas opcional, de entrada do usuário para aplicativos. Um aplicativo bem escrito deve incluir uma interface do mouse, mas não deve depender exclusivamente do mouse para adquirir a entrada do usuário. O aplicativo também deve fornecer suporte completo ao teclado.

Um aplicativo recebe a entrada do mouse na forma de mensagens enviadas ou postadas em suas janelas.

Esta seção contém os seguintes tópicos:

-   [Mouse Cursor](#mouse-cursor)
-   [Captura do mouse](#mouse-capture)
-   [Mouse ClickLock](#mouse-clicklock)
-   [Configuração do mouse](#mouse-configuration)
-   [XBUTTONs](#xbuttons)
-   [Mensagens do mouse](#mouse-messages)
    -   [Mensagens do mouse da área do cliente](#client-area-mouse-messages)
    -   [Mensagens do mouse de área não delimitada](#nonclient-area-mouse-messages)
    -   [A mensagem WM \_ NCHITTEST](/windows)
-   [Mouse Sonar](#mouse-sonar)
-   [Ressusução do mouse](#mouse-vanish)
-   [A roda do mouse](#the-mouse-wheel)
-   [Ativação de janela](#window-activation)

## <a name="mouse-cursor"></a>Mouse Cursor

Quando o usuário move o mouse, o sistema move um bitmap na tela chamado *cursor do mouse.* O cursor do mouse contém um ponto de pixel único chamado ponto de calor *,* um ponto que o sistema rastreia e reconhece como a posição do cursor. Quando ocorre um evento do mouse, a janela que contém o ponto quente normalmente recebe a mensagem do mouse resultante do evento. A janela não precisa estar ativa ou ter o foco do teclado para receber uma mensagem do mouse.

O sistema mantém uma variável que controla a velocidade do mouse, ou seja, a distância que o cursor se move quando o usuário move o mouse. Você pode usar a [**função SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) com o **sinalizador SPI \_ GETMOUSE** ou **SPI \_ SETMOUSE** para recuperar ou definir a velocidade do mouse. Para obter mais informações sobre cursores do mouse, consulte [Cursores](/windows/desktop/menurc/cursors).

## <a name="mouse-capture"></a>Captura do mouse

O sistema normalmente posta uma mensagem do mouse na janela que contém o ponto quente do cursor quando ocorre um evento do mouse. Um aplicativo pode alterar esse comportamento usando a [**função SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture) para rotear mensagens do mouse para uma janela específica. A janela recebe todas as mensagens do mouse até que o aplicativo chama a função [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) ou especifica outra janela de captura ou até que o usuário clique em uma janela criada por outro thread.

Quando a captura do mouse muda, o sistema envia uma [**mensagem WM \_ CAPTURECHANGED**](wm-capturechanged.md) para a janela que está perdendo a captura do mouse. O *parâmetro lParam* da mensagem especifica um ponteiro para a janela que está ganhando a captura do mouse.

Somente a janela de primeiro plano pode capturar a entrada do mouse. Quando uma janela em segundo plano tenta capturar a entrada do mouse, ela recebe mensagens somente para eventos do mouse que ocorrem quando o ponto quente do cursor está dentro da parte visível da janela.

Capturar a entrada do mouse será útil se uma janela deve receber toda a entrada do mouse, mesmo quando o cursor se move para fora da janela. Por exemplo, um aplicativo normalmente rastreia a posição do cursor após um evento de botão do mouse para baixo, seguindo o cursor até que ocorra um evento de aumento do botão do mouse. Se um aplicativo não tiver capturado a entrada do mouse e o usuário liberar o botão do mouse fora da janela, a janela não receberá a mensagem de aplicação do botão.

Um thread pode usar a [**função GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture) para determinar se uma de suas janelas capturou o mouse. Se uma das janelas do thread tiver capturado o mouse, **GetCapture** recuperará uma alça para a janela.

## <a name="mouse-clicklock"></a>Mouse ClickLock

O recurso de acessibilidade ClickLock do mouse permite que um usuário bloqueie o botão principal do mouse após um único clique. Para um aplicativo, o botão ainda parece estar pressionado. Para desbloquear o botão, um aplicativo pode enviar qualquer mensagem do mouse ou o usuário pode clicar em qualquer botão do mouse. Esse recurso permite que um usuário faça combinações complexas de mouse de forma mais simples. Por exemplo, aqueles com determinadas limitações físicas podem realçar texto, arrastar objetos ou abrir menus com mais facilidade. Para obter mais informações, consulte os seguintes sinalizadores e os Comentários em [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

-   **SPI \_ GETMOUSECLICKLOCK**
-   **SPI \_ SETMOUSECLICKLOCK**
-   **SPI \_ GETMOUSECLICKLOCKTIME**
-   **SPI \_ SETMOUSECLICKLOCKTIME**

## <a name="mouse-configuration"></a>Configuração do mouse

Embora o mouse seja um dispositivo de entrada importante para aplicativos, nem todos os usuários necessariamente têm um mouse. Um aplicativo pode determinar se o sistema inclui um mouse passando o valor **\_ MOUSEPRESENT do SM** para a [**função GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)

Windows dá suporte a um mouse com até três botões. Em um mouse de três botões, os botões são designados como os botões esquerdo, médio e direito. Mensagens e constantes nomeadas relacionadas aos botões do mouse usam as letras L, M e R para identificar os botões. O botão em um mouse de botão único é considerado o botão esquerdo. Embora Windows suporte a um mouse com vários botões, a maioria dos aplicativos usa o botão esquerdo principalmente e os outros minimamente, se for o caso.

Os aplicativos também podem dar suporte a uma roda do mouse. A roda do mouse pode ser pressionada ou girada. Quando a roda do mouse é pressionada, ela atua como o botão central (terceiro), enviando mensagens normais de botão central para seu aplicativo. Quando ela é girada, uma mensagem de roda é enviada para seu aplicativo. Para obter mais informações, consulte [a seção Roda do](#the-mouse-wheel) Mouse.

Os aplicativos podem dar suporte a botões application-command. Esses botões, chamados botões X, foram projetados para permitir o acesso mais fácil a um navegador da Internet, email eletrônico e serviços de mídia. Quando um botão X é pressionado, uma [**mensagem \_ WM APPCOMMAND**](wm-appcommand.md) é enviada ao seu aplicativo. Para obter mais informações, consulte a descrição na mensagem **\_ WM APPCOMMAND.**

Um aplicativo pode determinar o número de botões no mouse passando o valor **\_ de SM CMOUSEBUTTONS** para a [**função GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Para configurar o mouse para um usuário à esquerda, o aplicativo pode usar a função [**SwapMouseButton**](/windows/win32/api/winuser/nf-winuser-swapmousebutton) para inverter o significado dos botões esquerdo e direito do mouse. Passar o **valor \_ SPI SETMOUSEBUTTONSWAP** para a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) é outra maneira de reverter o significado dos botões. Observe, no entanto, que o mouse é um recurso compartilhado, portanto, reverter o significado dos botões afeta todos os aplicativos.

## <a name="xbuttons"></a>XBUTTONs

Windows dá suporte a um mouse com cinco botões. Além dos botões esquerdo, médio e direito, há XBUTTON1 e XBUTTON2, que fornecem navegação para trás e para frente ao usar o navegador.

O gerenciador de janelas dá suporte a XBUTTON1 e XBUTTON2 por meio das mensagens **WM \_ XBUTTON \* *_ e _* WM \_ NCXBUTTON \* *_ . A HIWORD do _* WPARAM** nessas mensagens contém um sinalizador que indica qual botão X foi pressionado. Como essas mensagens do mouse também se ajustam entre as constantes **WM \_ MOUSEFIRST** e **WM \_ MOUSELAST,** um aplicativo pode filtrar todas as mensagens do mouse com [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).

Os seguintes suportes são XBUTTON1 e XBUTTON2:

-   [**WM \_ APPCOMMAND**](wm-appcommand.md)
-   [**WM \_ NCXBUTTONDBLCLK**](wm-ncxbuttondblclk.md)
-   [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)
-   [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
-   [**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md)
-   [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)
-   [**WM \_ XBUTTONUP**](wm-xbuttonup.md)
-   [**MOUSEHOOKSTRUCTEX**](/windows/win32/api/winuser/ns-winuser-mousehookstructex)

As SEGUINTES APIs foram modificadas para dar suporte a estes botões:

-   [**evento \_ mouse**](/windows/win32/api/winuser/nf-winuser-mouse_event)
-   [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
-   [**MSLLHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-msllhookstruct)
-   [**MOUSEINPUT**](/windows/win32/api/winuser/ns-winuser-mouseinput)
-   [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)

É improvável que uma janela filho em um aplicativo de componente seja capaz de implementar comandos diretamente para XBUTTON1 e XBUTTON2. Portanto, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia uma [**mensagem WM \_ APPCOMMAND**](wm-appcommand.md) para uma janela quando um botão X é clicado. **DefWindowProc** também envia a mensagem **WM \_ APPCOMMAND** para sua janela pai. Isso é semelhante à maneira como os menus de contexto são invocados com um clique com o botão direito do mouse–**DefWindowProc** envia uma mensagem [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) para o menu e também a envia para seu pai. Além disso, se **DefWindowProc** receber uma mensagem **WM \_ APPCOMMAND** para uma janela de nível superior, ele chamará um gancho de shell com o código HSHELL \_ APPCOMMAND.

Há suporte para os teclados que têm chaves extras para funções de navegador, funções de mídia, lançamento de aplicativos e gerenciamento de energia. Para obter mais informações, consulte [Teclas de teclado para navegação e outras funções](about-keyboard-input.md).

## <a name="mouse-messages"></a>Mensagens do mouse

O mouse gera um evento de entrada quando o usuário move o mouse ou pressiona ou libera um botão do mouse. O sistema converte eventos de entrada do mouse em mensagens e os posta na fila de mensagens do thread apropriado. Quando as mensagens do mouse são postadas mais rapidamente do que um thread pode processá-las, o sistema descarta tudo, menos a mensagem mais recente do mouse.

Uma janela recebe uma mensagem do mouse quando ocorre um evento do mouse enquanto o cursor está dentro das bordas da janela ou quando a janela captura o mouse. As mensagens do mouse são divididas em dois grupos: mensagens de área do cliente e mensagens de área não cliente. Normalmente, um aplicativo processa mensagens de área do cliente e ignora mensagens de área não cliente.

Esta seção contém os seguintes tópicos:

-   [Mensagens do mouse da área do cliente](#client-area-mouse-messages)
-   [Mensagens do mouse de área não delimitada](#nonclient-area-mouse-messages)
-   [A mensagem WM \_ NCHITTEST](/windows)

### <a name="client-area-mouse-messages"></a>Mensagens do mouse da área do cliente

Uma janela recebe uma mensagem do mouse da área do cliente quando ocorre um evento do mouse na área do cliente da janela. O sistema posta a [**mensagem WM \_ MOUSEMOVE**](wm-mousemove.md) na janela quando o usuário move o cursor dentro da área do cliente. Ele posta uma das mensagens a seguir quando o usuário pressiona ou libera um botão do mouse enquanto o cursor está dentro da área do cliente.



| Mensagem                                       | Significado                                     |
|-----------------------------------------------|---------------------------------------------|
| [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md) | O botão esquerdo do mouse foi clicado duas vezes.   |
| [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md)     | O botão esquerdo do mouse foi pressionado.          |
| [**WM \_ LBUTTONUP**](wm-lbuttonup.md)         | O botão esquerdo do mouse foi liberado.         |
| [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md) | O botão do meio do mouse foi clicado duas vezes. |
| [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md)     | O botão do meio do mouse foi pressionado.        |
| [**WM \_ MBUTTONUP**](wm-mbuttonup.md)         | O botão do meio do mouse foi liberado.       |
| [**WM \_ RBUTTONDBLCLK**](wm-rbuttondblclk.md) | O botão direito do mouse foi clicado duas vezes.  |
| [**WM \_ RBUTTONDOWN**](wm-rbuttondown.md)     | O botão direito do mouse foi pressionado.         |
| [**WM \_ RBUTTONUP**](wm-rbuttonup.md)         | O botão direito do mouse foi liberado.        |
| [**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md) | Um botão X do mouse foi clicado duas vezes.       |
| [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)     | Um botão X do mouse foi pressionado.              |
| [**WM \_ XBUTTONUP**](wm-xbuttonup.md)         | Um botão X do mouse foi liberado.             |



 

Além disso, um aplicativo pode chamar a [**função TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) para que o sistema envie duas outras mensagens. Ele posta a [**mensagem WM \_ MOUSEHOVER**](wm-mousehover.md) quando o cursor passar o mouse sobre a área do cliente por um determinado período de tempo. Ele posta a [**mensagem WM \_ MOUSELEAVE**](wm-mouseleave.md) quando o cursor sai da área do cliente.

### <a name="message-parameters"></a>Parâmetros de mensagem

O *parâmetro lParam* de uma mensagem do mouse da área do cliente indica a posição do ponto de acionamento do cursor. A palavra de ordem baixa indica a coordenada X do ponto de calor e a palavra de ordem alta indica a coordenada y. As coordenadas são especificadas nas coordenadas do cliente. No sistema de coordenadas do cliente, todos os pontos na tela são especificados em relação às coordenadas (0,0) do canto superior esquerdo da área do cliente.

O *parâmetro wParam* contém sinalizadores que indicam o status dos outros botões do mouse e as teclas CTRL e SHIFT no momento do evento do mouse. Você pode verificar esses sinalizadores quando o processamento da mensagem do mouse depende do estado de outro botão do mouse ou da tecla CTRL ou SHIFT. O *parâmetro wParam* pode ser uma combinação dos valores a seguir.



| Valor            | Descrição                      |
|------------------|----------------------------------|
| **CONTROLE \_ MK**  | A tecla CTRL está inocizada.            |
| **MK \_ LBUTTON**  | O botão esquerdo do mouse está ino mouse.   |
| **MK \_ MBUTTON**  | O botão do meio do mouse está ino mouse. |
| **MK \_ RBUTTON**  | O botão direito do mouse está ino mouse.  |
| **SHIFT \_ da MK**    | A tecla SHIFT está inobada.           |
| **MK \_ XBUTTON1** | O primeiro botão X está ino mouse.      |
| **MK \_ XBUTTON2** | O segundo botão X está ino mouse.     |



 

### <a name="double-click-messages"></a>Double-Click mensagens

O sistema gera uma mensagem de clique duplo quando o usuário clica no botão do mouse duas vezes em sucessão rápida. Quando o usuário clica em um botão, o sistema estabelece um retângulo centralizado em torno do ponto de contato do cursor. Ele também marca a hora em que o clique ocorreu. Quando o usuário clica no mesmo botão uma segunda vez, o sistema determina se o ponto de calor ainda está dentro do retângulo e calcula o tempo decorrido desde o primeiro clique. Se o ponto de calor ainda estiver dentro do retângulo e o tempo decorrido não exceder o valor de tempo limite de clique duplo, o sistema gerará uma mensagem de clique duplo.

Um aplicativo pode obter e definir valores de tempo-out de clique duplo usando as funções [**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime) e [**SetDoubleClickTime,**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime) respectivamente. Como alternativa, o aplicativo pode definir o valor de tempo-de-tempo-de-clique duplo usando o **sinalizador SPI \_ SETDOUBLECLICKTIME** com a [**função SystemParametersInfo.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) Ele também pode definir o tamanho do retângulo que o sistema usa para detectar cliques duplos passando os sinalizadores **SPI \_ SETDOUBLECLKWIDTH** e **SPI \_ SETDOUBLECLKHEIGHT** para **SystemParametersInfo**. Observe, no entanto, que definir o valor de tempo-de-tempo-de-clique duplo e o retângulo afeta todos os aplicativos.

Uma janela definida pelo aplicativo não recebe, por padrão, mensagens de clique duplo. Devido à sobrecarga do sistema envolvida na geração de mensagens de clique duplo, essas mensagens são geradas somente para janelas que pertencem a classes que têm o estilo de classe **\_ DBLCLKS CS.** Seu aplicativo deve definir esse estilo ao registrar a classe de janela. Para obter mais informações, consulte [Classes de janela](/windows/desktop/winmsg/window-classes).

Uma mensagem de clique duplo é sempre a terceira mensagem em uma série de quatro mensagens. As duas primeiras mensagens são as mensagens de botão para baixo e de botão para cima geradas pelo primeiro clique. O segundo clique gera a mensagem de clique duplo seguida por outra mensagem de botão para cima. Por exemplo, clicar duas vezes no botão esquerdo do mouse gera a seguinte sequência de mensagens:

1.  [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md)
2.  [**WM \_ LBUTTONUP**](wm-lbuttonup.md)
3.  [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md)
4.  [**WM \_ LBUTTONUP**](wm-lbuttonup.md)

Como uma janela sempre recebe uma mensagem de botão para baixo antes de receber uma mensagem de clique duplo, um aplicativo normalmente usa uma mensagem de clique duplo para estender uma tarefa iniciada durante uma mensagem de botão para baixo. Por exemplo, quando o usuário clica em uma cor na paleta de cores Microsoft Paint, Paint exibe a cor selecionada ao lado da paleta. Quando o usuário clica duas vezes em uma cor, Paint exibe a cor e abre a **caixa de** diálogo Editar Cores.

### <a name="nonclient-area-mouse-messages"></a>Mensagens do mouse de área não delimitada

Uma janela recebe uma mensagem do mouse de área não delimitada quando um evento do mouse ocorre em qualquer parte de uma janela, exceto na área do cliente. A área nãoncliente de uma janela consiste em sua borda, barra de menus, barra de título, barra de rolagem, menu de janela, botão minimizar e maximizar o botão.

O sistema gera mensagens de área não dependentes principalmente para seu próprio uso. Por exemplo, o sistema usa mensagens de área não delimitadoras para alterar o cursor para uma seta de duas pontas quando o ponto quente do cursor se move para a borda de uma janela. Uma janela deve passar mensagens do mouse de área não dependente para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para aproveitar a interface interna do mouse.

Há uma mensagem de mouse de área não delimitada correspondente para cada mensagem do mouse da área do cliente. Os nomes dessas mensagens são semelhantes, exceto que as constantes nomeadas para as mensagens de área não delimitadas incluem as letras NC. Por exemplo, mover o cursor na área não dependente gera uma mensagem [**WM \_ NCMOUSEMOVE**](wm-ncmousemove.md) e pressionar o botão esquerdo do mouse enquanto o cursor está na área não dependente gera uma mensagem [**WM \_ NCLBUTTONDOWN.**](wm-nclbuttondown.md)

O *parâmetro lParam* de uma mensagem de mouse de área não dependente é uma estrutura que contém as coordenadas x e y do ponto de a quente do cursor. Ao contrário das coordenadas das mensagens do mouse da área do cliente, as coordenadas são especificadas em coordenadas de tela em vez de coordenadas de cliente. No sistema de coordenadas da tela, todos os pontos na tela são relativos às coordenadas (0,0) do canto superior esquerdo da tela.

O *parâmetro wParam* contém um valor de teste de clique, um valor que indica onde na área não dependente o evento do mouse ocorreu. A seção a seguir explica a finalidade dos valores de teste de acerto.

### <a name="the-wm_nchittest-message"></a>A mensagem WM \_ NCHITTEST

Sempre que ocorre um evento do mouse, o sistema envia uma mensagem [**WM \_ NCHITTEST**](wm-nchittest.md) para a janela que contém o ponto quente do cursor ou a janela que capturou o mouse. O sistema usa essa mensagem para determinar se uma área do cliente ou uma mensagem do mouse de área não cliente deve ser enviada. Um aplicativo que deve receber mensagens de botão do mouse e movimento do mouse deve passar a mensagem **WM \_ NCHITTEST** para a [**função DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

O *parâmetro lParam* da [**mensagem WM \_ NCHITTEST**](wm-nchittest.md) contém as coordenadas de tela do ponto de calor do cursor. A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examina as coordenadas e retorna um valor de teste de acerto que indica o local do ponto de destino. O valor de teste de acerto pode ser um dos valores a seguir.



| Valor             | Local do ponto de a quente                                                                                                                                                                                |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HTBORDER**      | Na borda de uma janela que não tem uma borda deizing.                                                                                                                                       |
| **HTBOTTOM**      | Na borda inferior horizontal de uma janela.                                                                                                                                                         |
| **HTBOTTOMLEFT**  | No canto inferior esquerdo de uma borda da janela.                                                                                                                                                        |
| **HTBOTTOMRIGHT** | No canto inferior direito de uma borda da janela.                                                                                                                                                       |
| **Htcaption**     | Em uma barra de título.                                                                                                                                                                                     |
| **HTCLIENT**      | Em uma área de cliente.                                                                                                                                                                                   |
| **HTCLOSE**       | Em um **botão** Fechar.                                                                                                                                                                              |
| **HTERROR**       | Na tela de fundo ou em uma linha de divisão entre janelas (o mesmo que HTNOWHERE, exceto que a [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) produz um aviso de aviso do sistema para indicar um erro). |
| **Htgrowbox**     | Em uma caixa de tamanho (o mesmo que **HTSIZE**).                                                                                                                                                                 |
| **HTHELP**        | Em um **botão ajuda.**                                                                                                                                                                               |
| **HTHSCROLL**     | Em uma barra de rolagem horizontal.                                                                                                                                                                         |
| **HTLEFT**        | Na borda esquerda de uma janela.                                                                                                                                                                     |
| **HTMENU**        | Em um menu.                                                                                                                                                                                          |
| **HTMAXBUTTON**   | Em um **botão Maximizar.**                                                                                                                                                                           |
| **HTMINBUTTON**   | Em um **botão** Minimizar.                                                                                                                                                                           |
| **Htnowhere**     | Na tela de fundo ou em uma linha de divisão entre janelas.                                                                                                                                     |
| **HTREDUCE**      | Em um **botão** Minimizar.                                                                                                                                                                           |
| **HTRIGHT**       | Na borda direita de uma janela.                                                                                                                                                                    |
| **HTSIZE**        | Em uma caixa de tamanho (igual a **HTGROWBOX**).                                                                                                                                                              |
| **HTSYSMENU**     | Em um menu **Sistema** ou em um **botão** Fechar em uma janela filho.                                                                                                                                    |
| **HTTOP**         | Na borda superior horizontal de uma janela.                                                                                                                                                         |
| **HTTOPLEFT**     | No canto superior esquerdo de uma borda da janela.                                                                                                                                                        |
| **HTTOPRIGHT**    | No canto superior direito de uma borda da janela.                                                                                                                                                       |
| **HTTRANSPARENT** | Em uma janela atualmente coberta por outra janela no mesmo thread.                                                                                                                                 |
| **HTVSCROLL**     | Na barra de rolagem vertical.                                                                                                                                                                         |
| **HTZOOM**        | Em um **botão Maximizar.**                                                                                                                                                                           |



 

Se o cursor estiver na área do cliente de uma janela, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retornará o valor de teste de acerto **HTCLIENT** para o procedimento de janela. Quando o procedimento de janela retorna esse código para o sistema, o sistema converte as coordenadas de tela do ponto de acesso do cursor em coordenadas do cliente e, em seguida, posta a mensagem do mouse da área do cliente apropriada.

A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna um dos outros valores de teste de acerto quando o ponto quente do cursor está na área não dependente de uma janela. Quando o procedimento de janela retorna um desses valores de teste de clique, o sistema posta uma mensagem do mouse de área não dependente, colocando o valor de teste de clique no parâmetro *wParam* da mensagem e nas coordenadas do cursor no parâmetro *lParam.*

## <a name="mouse-sonar"></a>Mouse Sonar

O recurso de acessibilidade do Sonar do Mouse mostra brevemente vários círculos concêntricos ao redor do ponteiro quando o usuário pressiona e libera a tecla CTRL. Esse recurso ajuda um usuário a localizar o ponteiro do mouse em uma tela desorganização ou com resolução definida como alta, em um monitor de baixa qualidade ou para usuários com deficiência visual. Para obter mais informações, consulte os seguintes sinalizadores [**em SystemParametersInfo:**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)

**SPI \_ GETMOUSESONAR**

**SPI \_ SETMOUSESONAR**

## <a name="mouse-vanish"></a>Ressusução do mouse

O recurso de acessibilidade Do Mouse Accessibility oculta o ponteiro quando o usuário está digitando. O ponteiro do mouse reaparece quando o usuário move o mouse. Esse recurso impede que o ponteiro oculta o texto que está sendo digitado, por exemplo, em um email ou outro documento. Para obter mais informações, consulte os seguintes sinalizadores [**em SystemParametersInfo:**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)

**SPI \_ GETMOUSEVACORE**

**SPI \_ SETMOUSEVANISH**

## <a name="the-mouse-wheel"></a>A roda do mouse

A roda do mouse combina os recursos de uma roda e um botão do mouse. A roda tem entalhes discretos e espaçados uniformemente. Quando você gira a roda, uma mensagem de roda é enviada ao seu aplicativo à medida que cada entalhe é encontrado. o botão de roda também pode operar como um botão normal Windows meio (terceiro). Pressionar e liberar a roda do mouse envia mensagens padrão do [**WM \_ MBUTTONUP**](wm-mbuttonup.md) e do [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md) . Clicar duas vezes no terceiro botão envia a mensagem padrão do [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md) .

A roda do mouse tem suporte por meio da mensagem do [**WM \_ MOUSEWHEEL**](wm-mousewheel.md) .

Girar o mouse envia a mensagem do [**WM \_ MOUSEWHEEL**](wm-mousewheel.md) para a janela de foco. A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga a mensagem para o pai da janela. Não deve haver nenhum encaminhamento interno da mensagem, pois **DefWindowProc** propaga a cadeia pai até que uma janela que o processa seja encontrada.

### <a name="determining-the-number-of-scroll-lines"></a>Determinando o número de linhas de rolagem

Os aplicativos devem usar a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para recuperar o número de linhas que um documento rola para cada operação de rolagem (entalhe de roda). Para recuperar o número de linhas, um aplicativo faz a seguinte chamada:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



A variável "pulScrollLines" aponta para um valor inteiro sem sinal que recebe o número sugerido de linhas para rolar quando a roda do mouse é girada sem Chaves modificadoras:

-   Se esse número for 0, não deverá ocorrer nenhuma rolagem.
-   Se esse número for o **Wheel \_ PAGESCROLL**, um volante deverá ser interpretado como um clique uma vez nas regiões Page Down ou Page up da barra de rolagem.
-   Se o número de linhas a rolar for maior que o número de linhas visíveis, a operação de rolagem também deverá ser interpretada como uma operação Page Down ou Page up.

O valor padrão para o número de linhas de rolagem será 3. Se um usuário alterar o número de linhas de rolagem usando a folha de propriedades do mouse no painel de controle, o sistema operacional transmitirá uma mensagem do [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) para todas as janelas de nível superior com **SPI \_ SETWHEELSCROLLLINES** especificado. Quando um aplicativo recebe a **mensagem \_ SETTINGCHANGE do WM** , ele pode obter o novo número de linhas de rolagem chamando:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



### <a name="controls-that-scroll"></a>Controles que rolam

A tabela a seguir lista os controles com a funcionalidade de rolagem (incluindo linhas de rolagem definidas pelo usuário). 

| Control                 | Rolagem                                                                                                                                                               |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Controle de edição            | Vertical e horizontal.                                                                                                                                                |
| Controle de caixa de listagem        | Vertical e horizontal.                                                                                                                                                |
| Caixa de combinação               | Quando não é descartada, cada rolagem recupera o próximo item ou o anterior. Quando desativadas, cada rolagem encaminha a mensagem para a caixa de listagem, que rola de forma adequada. |
| CMD (linha de comando)      | Vertical.                                                                                                                                                               |
| Modo de exibição de árvore               | Vertical e horizontal.                                                                                                                                                |
| Exibição de Lista               | Vertical e horizontal.                                                                                                                                                |
| Rolagens para cima/para baixo         | Um item por vez.                                                                                                                                                     |
| Rolagens do TrackBar        | Um item por vez.                                                                                                                                                     |
| Edição avançada da Microsoft 1,0 | Vertical. observe que o cliente Exchange tem suas próprias versões dos controles de exibição de lista e de exibição de árvore que não têm suporte à roda.                                        |
| Edição avançada da Microsoft 2,0 | Vertical.                                                                                                                                                               |



 

### <a name="detecting-a-mouse-with-a-wheel"></a>Detectando um mouse com uma roda

Para determinar se um mouse com uma roda está conectado, chame [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) com **SM \_ MOUSEWHEELPRESENT**. Um valor de retorno **true** indica que o mouse está conectado.

O exemplo a seguir é do procedimento de janela para um controle de edição de várias linhas:


```
BOOL ScrollLines(
     PWNDDATA pwndData,   //scrolls the window indicated
     int cLinesToScroll); //number of times

short gcWheelDelta; //wheel delta from roll
PWNDDATA pWndData; //pointer to structure containing info about the window
UINT gucWheelScrollLines=0;//number of lines to scroll on a wheel rotation

gucWheelScrollLines = SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 
                             0, 
                             pulScrollLines, 
                             0);

case WM_MOUSEWHEEL:
    /*
     * Do not handle zoom and datazoom.
     */
    if (wParam & (MK_SHIFT | MK_CONTROL)) {
        goto PassToDefaultWindowProc;
    }

    gcWheelDelta -= (short) HIWORD(wParam);
    if (abs(gcWheelDelta) >= WHEEL_DELTA && gucWheelScrollLines > 0) 
    {
        int cLineScroll;

        /*
         * Limit a roll of one (1) WHEEL_DELTA to
         * scroll one (1) page.
         */
        cLineScroll = (int) min(
                (UINT) pWndData->ichLinesOnScreen - 1,
                gucWheelScrollLines);

        if (cLineScroll == 0) {
            cLineScroll++;
        }

        cLineScroll *= (gcWheelDelta / WHEEL_DELTA);
        assert(cLineScroll != 0);

        gcWheelDelta = gcWheelDelta % WHEEL_DELTA;
        return ScrollLines(pWndData, cLineScroll);
    }

    break;
```



## <a name="window-activation"></a>Ativação de janela

Quando o usuário clica em uma janela de nível superior inativa ou na janela filho de uma janela de nível superior inativa, o sistema envia a mensagem do [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md) (entre outras) para a janela de nível superior ou filho. O sistema envia essa mensagem depois de postar a mensagem [**\_ NCHITTEST do WM**](wm-nchittest.md) na janela, mas antes de postar a mensagem de botão para baixo. Quando o **WM \_ MOUSEACTIVATE** é passado para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , o sistema ativa a janela de nível superior e, em seguida, posta a mensagem de botão para baixo na janela de nível superior ou filho.

Ao processar o [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md), uma janela pode controlar se a janela de nível superior se torna a janela ativa como resultado de um clique do mouse e se a janela que foi clicada recebe a mensagem de botão inferior. Ele faz isso retornando um dos seguintes valores após o processamento do **WM \_ MOUSEACTIVATE**.



| Valor                    | Significado                                                              |
|--------------------------|----------------------------------------------------------------------|
| **ativação do MA \_**         | Ativa a janela e não descarta a mensagem do mouse.         |
| **MA \_ NOativar**       | Não ativa a janela e não descarta a mensagem do mouse. |
| **\_ACTIVATEANDEAT ma**   | Ativa a janela e descarta a mensagem do mouse.                 |
| **\_NOACTIVATEANDEAT ma** | Não ativa a janela, mas descarta a mensagem do mouse.         |

## <a name="see-also"></a>Confira também

[Aproveitando o movimento do High-Definition mouse](../dxtecharts/taking-advantage-of-high-dpi-mouse-movement.md)