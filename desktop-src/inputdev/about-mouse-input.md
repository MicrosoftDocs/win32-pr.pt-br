---
title: Sobre a entrada do mouse
description: Este tópico discute a entrada do mouse.
ms.assetid: 1f945a31-76d5-4e23-a55a-769ca114dbe9
keywords:
- entrada do usuário, entrada do mouse
- capturando entrada do usuário, entrada do mouse
- entrada do mouse
- cursor do mouse
- cursores, entrada de mouse
- captura do mouse
- Trava do mouse
- XBUTTONs
- configuração do mouse
- mensagens do mouse
- WM_NCHITTEST mensagem
- Recurso de acessibilidade do mouse desaparecer
- Recurso de acessibilidade do sonar do mouse
- roda do mouse
- WM_MOUSEWHEEL mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2294027cb4ca2c97371a7a06c90a7e46188e3b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641020"
---
# <a name="about-mouse-input"></a>Sobre a entrada do mouse

O mouse é um dispositivo de entrada de usuário importante, mas opcional para aplicativos. Um aplicativo bem escrito deve incluir uma interface do mouse, mas não deve depender apenas do mouse para adquirir a entrada do usuário. O aplicativo também deve fornecer suporte completo ao teclado.

Um aplicativo recebe entrada do mouse na forma de mensagens que são enviadas ou postadas em suas janelas.

Esta seção contém os seguintes tópicos:

-   [Cursor do mouse](#mouse-cursor)
-   [Captura do mouse](#mouse-capture)
-   [Trava do mouse](#mouse-clicklock)
-   [Configuração do mouse](#mouse-configuration)
-   [XBUTTONs](#xbuttons)
-   [Mensagens do mouse](#mouse-messages)
    -   [Mensagens de mouse da área do cliente](#client-area-mouse-messages)
    -   [Mensagens de mouse de área não cliente](#nonclient-area-mouse-messages)
    -   [A mensagem do WM \_ NCHITTEST](/windows)
-   [Mouse de sonar](#mouse-sonar)
-   [Desaparecer do mouse](#mouse-vanish)
-   [A roda do mouse](#the-mouse-wheel)
-   [Ativação de janela](#window-activation)

## <a name="mouse-cursor"></a>Cursor do mouse

Quando o usuário move o mouse, o sistema move um bitmap na tela chamada cursor do *mouse*. O cursor do mouse contém um ponto de pixel único chamado ponto de *acesso*, um ponto que o sistema acompanha e reconhece como a posição do cursor. Quando ocorre um evento de mouse, a janela que contém o ponto de acesso normalmente recebe a mensagem do mouse resultante do evento. A janela não precisa estar ativa ou ter o foco do teclado para receber uma mensagem do mouse.

O sistema mantém uma variável que controla a velocidade do mouse, ou seja, a distância com que o cursor se move quando o usuário move o mouse. Você pode usar a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) com o sinalizador **SPI \_ getmouse** ou **SPI \_ setmouse** para recuperar ou definir a velocidade do mouse. Para obter mais informações sobre cursores do mouse, consulte [cursores](/windows/desktop/menurc/cursors).

## <a name="mouse-capture"></a>Captura do mouse

Normalmente, o sistema posta uma mensagem do mouse na janela que contém o ponto de acesso do cursor quando ocorre um evento do mouse. Um aplicativo pode alterar esse comportamento usando a função [**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture) para rotear mensagens do mouse para uma janela específica. A janela recebe todas as mensagens do mouse até que o aplicativo chame a função [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) ou especifique outra janela de captura, ou até que o usuário clique em uma janela criada por outro thread.

Quando a captura do mouse é alterada, o sistema envia uma mensagem do [**WM \_ capturachanged**](wm-capturechanged.md) para a janela que está perdendo a captura do mouse. O parâmetro *lParam* da mensagem Especifica um identificador para a janela que está recebendo a captura do mouse.

Somente a janela em primeiro plano pode capturar a entrada do mouse. Quando uma janela de segundo plano tenta capturar a entrada do mouse, ela recebe mensagens somente para eventos de mouse que ocorrem quando o ponto de acesso do cursor está dentro da parte visível da janela.

Capturar a entrada do mouse é útil se uma janela precisar receber toda a entrada do mouse, mesmo quando o cursor se mover para fora da janela. Por exemplo, um aplicativo normalmente rastreia a posição do cursor após um evento de botão do mouse para baixo, seguindo o cursor até que ocorra um evento de botão do mouse. Se um aplicativo não tiver capturado a entrada do mouse e o usuário liberar o botão do mouse para fora da janela, a janela não receberá a mensagem de botão para cima.

Um thread pode usar a função [**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture) para determinar se uma de suas janelas capturou o mouse. Se uma das janelas do thread tiver capturado o mouse, **GetCapture** recuperará um identificador para a janela.

## <a name="mouse-clicklock"></a>Trava do mouse

O recurso de acessibilidade do mouse travado permite que um usuário bloqueie o botão do mouse primário após um único clique. Para um aplicativo, o botão ainda parece estar pressionado. Para desbloquear o botão, um aplicativo pode enviar qualquer mensagem do mouse ou o usuário pode clicar em qualquer botão do mouse. Esse recurso permite que um usuário faça combinações de mouse complexas mais simplesmente. Por exemplo, aqueles com determinadas limitações físicas podem realçar texto, arrastar objetos ou abrir menus com mais facilidade. Para obter mais informações, consulte os seguintes sinalizadores e comentários em [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

-   **SPI \_ GETMOUSECLICKLOCK**
-   **SPI \_ SETMOUSECLICKLOCK**
-   **SPI \_ GETMOUSECLICKLOCKTIME**
-   **SPI \_ SETMOUSECLICKLOCKTIME**

## <a name="mouse-configuration"></a>Configuração do mouse

Embora o mouse seja um dispositivo de entrada importante para aplicativos, nem todos os usuários têm, necessariamente, um mouse. Um aplicativo pode determinar se o sistema inclui um mouse passando o valor **de \_ MOUSEPRESENT do SM** para a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .

O Windows dá suporte a um mouse com até três botões. Em um mouse de três botões, os botões são designados como os botões esquerdo, médio e direito. As mensagens e as constantes nomeadas relacionadas aos botões do mouse usam as letras L, M e R para identificar os botões. O botão em um mouse de botão único é considerado o botão esquerdo. Embora o Windows dê suporte a um mouse com vários botões, a maioria dos aplicativos usa o botão esquerdo principalmente e os outros minimamente, se houver.

Os aplicativos também podem dar suporte a uma roda do mouse. A roda do mouse pode ser pressionada ou girada. Quando a roda do mouse é pressionada, ela atua como o botão médio (terceiro), enviando mensagens de botão médio normal para seu aplicativo. Quando ele é girado, uma mensagem de roda é enviada ao seu aplicativo. Para obter mais informações, consulte [a seção roda do mouse](#the-mouse-wheel) .

Os aplicativos podem dar suporte a botões de comando de aplicativo. Esses botões, chamados de botões X, foram projetados para permitir o acesso mais fácil a um navegador da Internet, correio eletrônico e serviços de mídia. Quando um botão X é pressionado, uma mensagem do [**WM \_ APPCOMMAND**](wm-appcommand.md) é enviada ao seu aplicativo. Para obter mais informações, consulte a descrição na mensagem do **WM \_ APPCOMMAND** .

Um aplicativo pode determinar o número de botões no mouse passando o valor de **\_ CMOUSEBUTTONS do SM** para a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Para configurar o mouse para um usuário da mão esquerda, o aplicativo pode usar a função [**SwapMouseButton**](/windows/win32/api/winuser/nf-winuser-swapmousebutton) para reverter o significado dos botões esquerdo e direito do mouse. Passar o valor **SPI \_ SETMOUSEBUTTONSWAP** para a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) é outra maneira de reverter o significado dos botões. No entanto, observe que o mouse é um recurso compartilhado, portanto, reverter o significado dos botões afeta todos os aplicativos.

## <a name="xbuttons"></a>XBUTTONs

O Windows dá suporte a um mouse com cinco botões. Além dos botões esquerdo, médio e direito, há XBUTTON1 e XBUTTON2, que fornecem navegação para trás e para frente ao usar seu navegador.

O Gerenciador de janelas dá suporte a XBUTTON1 e XBUTTON2 por meio das mensagens do **WM \_ XBUTTON \*** e do **WM \_ NCXBUTTON \*** . O HIWORD do **wParam** nessas mensagens contém um sinalizador que indica qual botão X foi pressionado. Como essas mensagens do mouse também se ajustam entre as constantes do **WM \_ MOUSEFIRST** e do **WM \_ MOUSELAST**, um aplicativo pode filtrar todas as mensagens do mouse com [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).

O seguinte suporte a XBUTTON1 e XBUTTON2:

-   [**APPCOMMAND do WM \_**](wm-appcommand.md)
-   [**NCXBUTTONDBLCLK do WM \_**](wm-ncxbuttondblclk.md)
-   [**NCXBUTTONDOWN do WM \_**](wm-ncxbuttondown.md)
-   [**NCXBUTTONUP do WM \_**](wm-ncxbuttonup.md)
-   [**XBUTTONDBLCLK do WM \_**](wm-xbuttondblclk.md)
-   [**XBUTTONDOWN do WM \_**](wm-xbuttondown.md)
-   [**XBUTTONUP do WM \_**](wm-xbuttonup.md)
-   [**MOUSEHOOKSTRUCTEX**](/windows/win32/api/winuser/ns-winuser-mousehookstructex)

As seguintes APIs foram modificadas para dar suporte a esses botões:

-   [**evento do mouse \_**](/windows/win32/api/winuser/nf-winuser-mouse_event)
-   [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
-   [**MSLLHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-msllhookstruct)
-   [**MOUSEINPUT**](/windows/win32/api/winuser/ns-winuser-mouseinput)
-   [**PARENTNOTIFY do WM \_**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)

É improvável que uma janela filho em um aplicativo de componente seja capaz de implementar diretamente os comandos para o XBUTTON1 e o XBUTTON2. Portanto, o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia uma mensagem do [**WM \_ APPCOMMAND**](wm-appcommand.md) para uma janela quando um botão X é clicado. O **DefWindowProc** também envia a mensagem do **WM \_ APPCOMMAND** para sua janela pai. Isso é semelhante à maneira como os menus de contexto são chamados com um clique com o botão direito —**DefWindowProc** envia uma mensagem de [**\_ CONTEXTMENU do WM**](/windows/desktop/menurc/wm-contextmenu) para o menu e também o envia para seu pai. Além disso, se o **DefWindowProc** receber uma mensagem do **WM \_ APPCOMMAND** para uma janela de nível superior, ele chamará um gancho de shell com o código HSHELL \_ APPCOMMAND.

Há suporte para os teclados que têm chaves extras para funções de navegador, funções de mídia, inicialização de aplicativos e gerenciamento de energia. Para obter mais informações, consulte [teclas do teclado para procurar e outras funções](about-keyboard-input.md).

## <a name="mouse-messages"></a>Mensagens do mouse

O mouse gera um evento de entrada quando o usuário move o mouse ou pressiona ou libera um botão do mouse. O sistema converte eventos de entrada do mouse em mensagens e os posta na fila de mensagens do thread apropriado. Quando as mensagens do mouse são lançadas mais rapidamente do que um thread pode processá-las, o sistema descarta tudo, exceto a mensagem de mouse mais recente.

Uma janela recebe uma mensagem do mouse quando ocorre um evento do mouse enquanto o cursor está dentro das bordas da janela ou quando a janela capturou o mouse. As mensagens do mouse são divididas em dois grupos: mensagens da área do cliente e mensagens que não são da área do cliente. Normalmente, um aplicativo processa mensagens de área do cliente e ignora mensagens que não são da área do cliente.

Esta seção contém os seguintes tópicos:

-   [Mensagens de mouse da área do cliente](#client-area-mouse-messages)
-   [Mensagens de mouse de área não cliente](#nonclient-area-mouse-messages)
-   [A mensagem do WM \_ NCHITTEST](/windows)

### <a name="client-area-mouse-messages"></a>Mensagens de mouse da área do cliente

Uma janela recebe uma mensagem de mouse da área do cliente quando um evento do mouse ocorre dentro da área do cliente da janela. O sistema posta a [**mensagem \_ MOUSEMOVE do WM**](wm-mousemove.md) na janela quando o usuário move o cursor dentro da área do cliente. Ele posta uma das mensagens a seguir quando o usuário pressiona ou libera um botão do mouse enquanto o cursor está dentro da área do cliente.



| Mensagem                                       | Significado                                     |
|-----------------------------------------------|---------------------------------------------|
| [**LBUTTONDBLCLK do WM \_**](wm-lbuttondblclk.md) | O botão esquerdo do mouse foi clicado duas vezes.   |
| [**LBUTTONDOWN do WM \_**](wm-lbuttondown.md)     | O botão esquerdo do mouse foi pressionado.          |
| [**LBUTTONUP do WM \_**](wm-lbuttonup.md)         | O botão esquerdo do mouse foi liberado.         |
| [**MBUTTONDBLCLK do WM \_**](wm-mbuttondblclk.md) | O botão do meio do mouse foi clicado duas vezes. |
| [**MBUTTONDOWN do WM \_**](wm-mbuttondown.md)     | O botão do meio do mouse foi pressionado.        |
| [**MBUTTONUP do WM \_**](wm-mbuttonup.md)         | O botão do meio do mouse foi liberado.       |
| [**RBUTTONDBLCLK do WM \_**](wm-rbuttondblclk.md) | O botão direito do mouse foi clicado duas vezes.  |
| [**RBUTTONDOWN do WM \_**](wm-rbuttondown.md)     | O botão direito do mouse foi pressionado.         |
| [**RBUTTONUP do WM \_**](wm-rbuttonup.md)         | O botão direito do mouse foi liberado.        |
| [**XBUTTONDBLCLK do WM \_**](wm-xbuttondblclk.md) | Um botão do mouse X foi clicado duas vezes.       |
| [**XBUTTONDOWN do WM \_**](wm-xbuttondown.md)     | Um botão do mouse X foi pressionado.              |
| [**XBUTTONUP do WM \_**](wm-xbuttonup.md)         | Um botão X do mouse foi liberado.             |



 

Além disso, um aplicativo pode chamar a função [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) para que o sistema envie duas outras mensagens. Ele posta a mensagem do [**WM \_ MOUSEHOVER**](wm-mousehover.md) quando o cursor passa sobre a área do cliente por um determinado período de tempo. Ele posta a mensagem do [**WM \_ MOUSELEAVE**](wm-mouseleave.md) quando o cursor sai da área do cliente.

### <a name="message-parameters"></a>Parâmetros da mensagem

O parâmetro *lParam* de uma mensagem de mouse da área do cliente indica a posição do ponto de acesso do cursor. A palavra de ordem inferior indica a coordenada x do ponto de acesso e a palavra de ordem superior indica a coordenada y. As coordenadas são especificadas nas coordenadas do cliente. No sistema de coordenadas do cliente, todos os pontos na tela são especificados em relação às coordenadas (0, 0) do canto superior esquerdo da área do cliente.

O parâmetro *wParam* contém sinalizadores que indicam o status dos outros botões do mouse e as teclas CTRL e Shift no momento do evento do mouse. Você pode verificar esses sinalizadores quando o processamento de mensagens do mouse depende do estado de outro botão do mouse ou da tecla CTRL ou SHIFT. O parâmetro *wParam* pode ser uma combinação dos valores a seguir.



| Valor            | Descrição                      |
|------------------|----------------------------------|
| **\_controle MK**  | A tecla CTRL está inoperante.            |
| **\_LBUTTON MK**  | O botão esquerdo do mouse está inativo.   |
| **\_MBUTTON MK**  | O botão do meio do mouse está inativo. |
| **\_RBUTTON MK**  | O botão direito do mouse está inativo.  |
| **\_turno MK**    | A tecla SHIFT está inoperante.           |
| **\_XButton1 MK** | O primeiro botão X está inoperante.      |
| **\_XButton2 MK** | O segundo botão X está inoperante.     |



 

### <a name="double-click-messages"></a>Double-Click mensagens

O sistema gera uma mensagem de clique duplo quando o usuário clica duas vezes em um botão do mouse em sucessão rápida. Quando o usuário clica em um botão, o sistema estabelece um retângulo centralizado em relação ao ponto de acesso do cursor. Ele também marca a hora em que o clique ocorreu. Quando o usuário clica no mesmo botão uma segunda vez, o sistema determina se o ponto de acesso ainda está dentro do retângulo e calcula o tempo decorrido desde o primeiro clique. Se o ponto de acesso ainda estiver dentro do retângulo e o tempo decorrido não exceder o valor de tempo limite de clique duplo, o sistema gerará uma mensagem de clique duplo.

Um aplicativo pode obter e definir os valores de tempo limite de clique duplo usando as funções [**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime) e [**setdoubleclicktime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime) , respectivamente. Como alternativa, o aplicativo pode definir o valor de clique duplo – tempo limite usando o sinalizador **SPI \_ setdoubleclicktime** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) . Ele também pode definir o tamanho do retângulo que o sistema usa para detectar cliques duplos passando os sinalizadores **SPI \_ SETDOUBLECLKWIDTH** e **SPI \_ SETDOUBLECLKHEIGHT** para **SystemParametersInfo**. No entanto, observe que definir o valor de clique duplo – tempo limite e Rectangle afeta todos os aplicativos.

Por padrão, uma janela definida pelo aplicativo não recebe mensagens de clique duplo. Devido à sobrecarga do sistema envolvida na geração de mensagens de clique duplo, essas mensagens são geradas somente para janelas que pertencem a classes que têm o estilo de classe **cs \_ DBLCLKS** . Seu aplicativo deve definir esse estilo ao registrar a classe de janela. Para obter mais informações, consulte [classes de janela](/windows/desktop/winmsg/window-classes).

Uma mensagem de clique duplo é sempre a terceira mensagem em uma série de quatro mensagens. As duas primeiras mensagens são as mensagens de botão para baixo e de botão para cima geradas pelo primeiro clique. O segundo clique gera a mensagem de clique duplo seguida por outra mensagem de botão. Por exemplo, clicar duas vezes com o botão esquerdo do mouse gera a seguinte sequência de mensagens:

1.  [**LBUTTONDOWN do WM \_**](wm-lbuttondown.md)
2.  [**LBUTTONUP do WM \_**](wm-lbuttonup.md)
3.  [**LBUTTONDBLCLK do WM \_**](wm-lbuttondblclk.md)
4.  [**LBUTTONUP do WM \_**](wm-lbuttonup.md)

Como uma janela sempre recebe uma mensagem de botão para baixo antes de receber uma mensagem de clique duplo, um aplicativo geralmente usa uma mensagem de clique duplo para estender uma tarefa iniciada durante uma mensagem de botão para baixo. Por exemplo, quando o usuário clica em uma cor na paleta de cores do Microsoft Paint, o Paint exibe a cor selecionada ao lado da paleta. Quando o usuário clica duas vezes em uma cor, o Paint exibe a cor e abre a caixa de diálogo **Editar cores** .

### <a name="nonclient-area-mouse-messages"></a>Mensagens de mouse de área não cliente

Uma janela recebe uma mensagem de mouse de área não cliente quando ocorre um evento do mouse em qualquer parte de uma janela, exceto a área do cliente. A área não cliente de uma janela consiste em sua borda, barra de menus, barra de título, barra de rolagem, menu janela, botão minimizar e botão Maximizar.

O sistema gera mensagens de área não cliente principalmente para seu próprio uso. Por exemplo, o sistema usa mensagens de área não cliente para alterar o cursor para uma seta de duas pontas quando o ponto de acesso do cursor se move para a borda de uma janela. Uma janela deve passar mensagens de mouse de área não cliente para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para aproveitar a interface do mouse interna.

Há uma mensagem de mouse de área não cliente correspondente para cada mensagem de mouse de área do cliente. Os nomes dessas mensagens são semelhantes, exceto pelo fato de que as constantes nomeadas para as mensagens de área não cliente incluem o NC de letras. Por exemplo, mover o cursor na área não cliente gera uma mensagem do [**WM \_ NCMOUSEMOVE**](wm-ncmousemove.md) e pressionar o botão esquerdo do mouse enquanto o cursor está na área não cliente gera uma mensagem do [**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md) .

O parâmetro *lParam* de uma mensagem de mouse de área não cliente é uma estrutura que contém as coordenadas x e y do ponto de acesso do cursor. Ao contrário das coordenadas das mensagens de mouse da área do cliente, as coordenadas são especificadas em coordenadas da tela, em vez de coordenadas do cliente. No sistema de coordenadas de tela, todos os pontos na tela são relativos às coordenadas (0, 0) do canto superior esquerdo da tela.

O parâmetro *wParam* contém um valor de teste de clique, um valor que indica em que local na área não cliente ocorreu o evento de mouse. A seção a seguir explica a finalidade dos valores de teste de clique.

### <a name="the-wm_nchittest-message"></a>A mensagem do WM \_ NCHITTEST

Sempre que um evento de mouse ocorre, o sistema envia uma mensagem do [**WM \_ NCHITTEST**](wm-nchittest.md) para a janela que contém o ponto de acesso do cursor ou a janela que capturou o mouse. O sistema usa essa mensagem para determinar se deve ser enviada uma mensagem de cliente ou de mouse de área de clientes. Um aplicativo que deve receber o movimento do mouse e as mensagens do botão do mouse devem passar a mensagem do **WM \_ NCHITTEST** para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

O parâmetro *lParam* da mensagem [**de \_ NCHITTEST do WM**](wm-nchittest.md) contém as coordenadas de tela do ponto de acesso do cursor. A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examina as coordenadas e retorna um valor de teste de clique que indica o local do ponto de acesso. O valor de teste de clique pode ser um dos valores a seguir.



| Valor             | Local do ponto de acesso                                                                                                                                                                                |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HTBORDER**      | Na borda de uma janela que não tem uma borda de dimensionamento.                                                                                                                                       |
| **HTBOTTOM**      | Na borda inferior horizontal de uma janela.                                                                                                                                                         |
| **HTBOTTOMLEFT**  | No canto inferior esquerdo de uma borda de janela.                                                                                                                                                        |
| **HTBOTTOMRIGHT** | No canto inferior direito de uma borda de janela.                                                                                                                                                       |
| **HTCAPTION**     | Em uma barra de título.                                                                                                                                                                                     |
| **HTCLIENT**      | Em uma área de cliente.                                                                                                                                                                                   |
| **HTCLOSE**       | Em um botão **fechar** .                                                                                                                                                                              |
| **HTERROR**       | Na tela de fundo ou em uma linha divisória entre janelas (o mesmo que HTNOWHERE, exceto que a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) produz um aviso sonoro do sistema para indicar um erro). |
| **HTGROWBOX**     | Em uma caixa de tamanho (igual a **HTSIZE**).                                                                                                                                                                 |
| **HTHELP**        | Em um botão de **ajuda** .                                                                                                                                                                               |
| **HTHSCROLL**     | Em uma barra de rolagem horizontal.                                                                                                                                                                         |
| **HTLEFT**        | Na borda esquerda de uma janela.                                                                                                                                                                     |
| **HTMENU**        | Em um menu.                                                                                                                                                                                          |
| **HTMAXBUTTON**   | Em um botão **maximizar** .                                                                                                                                                                           |
| **HTMINBUTTON**   | Em um botão **minimizar** .                                                                                                                                                                           |
| **HTNOWHERE**     | Na tela de fundo ou em uma linha divisória entre janelas.                                                                                                                                     |
| **HTREDUCE**      | Em um botão **minimizar** .                                                                                                                                                                           |
| **HTRIGHT**       | Na borda direita de uma janela.                                                                                                                                                                    |
| **HTSIZE**        | Em uma caixa de tamanho (igual a **HTGROWBOX**).                                                                                                                                                              |
| **HTSYSMENU**     | Em um menu do **sistema** ou em um botão **fechar** em uma janela filho.                                                                                                                                    |
| **HTTOP**         | Na borda superior horizontal de uma janela.                                                                                                                                                         |
| **HTTOPLEFT**     | No canto superior esquerdo de uma borda de janela.                                                                                                                                                        |
| **HTTOPRIGHT**    | No canto superior direito de uma borda de janela.                                                                                                                                                       |
| **HTTRANSPARENT** | Em uma janela atualmente coberta por outra janela no mesmo thread.                                                                                                                                 |
| **HTVSCROLL**     | Na barra de rolagem vertical.                                                                                                                                                                         |
| **HTZOOM**        | Em um botão **maximizar** .                                                                                                                                                                           |



 

Se o cursor estiver na área de cliente de uma janela, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retornará o valor de teste de clique **HTCLIENT** para o procedimento de janela. Quando o procedimento de janela retorna esse código para o sistema, o sistema converte as coordenadas de tela do ponto de acesso do cursor para as coordenadas do cliente e, em seguida, posta a mensagem de mouse da área do cliente apropriada.

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna um dos outros valores de teste de clique quando o ponto de acesso do cursor está em uma área não cliente da janela. Quando o procedimento de janela retorna um desses valores de teste de clique, o sistema posta uma mensagem de mouse de área não cliente, colocando o valor de teste de clique no parâmetro *wParam* da mensagem e as coordenadas do cursor no parâmetro *lParam* .

## <a name="mouse-sonar"></a>Mouse de sonar

O recurso de acessibilidade do sonar do mouse mostra brevemente vários círculos concêntricos em volta do ponteiro quando o usuário pressiona e libera a tecla CTRL. Esse recurso ajuda um usuário a localizar o ponteiro do mouse em uma tela que está obstruída ou com resolução definida como alta, em um monitor de baixa qualidade ou para usuários com visão inemparelhada. Para obter mais informações, consulte os seguintes sinalizadores em [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**SPI \_ GETMOUSESONAR**

**SPI \_ SETMOUSESONAR**

## <a name="mouse-vanish"></a>Desaparecer do mouse

O recurso de acessibilidade do mouse desaparecer oculta o ponteiro quando o usuário está digitando. O ponteiro do mouse reaparece quando o usuário move o mouse. Esse recurso mantém o ponteiro de obscurecer o texto que está sendo digitado, por exemplo, em um email ou em outro documento. Para obter mais informações, consulte os seguintes sinalizadores em [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**SPI \_ GETMOUSEVANISH**

**SPI \_ SETMOUSEVANISH**

## <a name="the-mouse-wheel"></a>A roda do mouse

A roda do mouse combina os recursos de uma roda e um botão do mouse. A roda tem entalhes discretos e espaçados uniformemente. Quando você gira a roda, uma mensagem de roda é enviada ao seu aplicativo à medida que cada entalhe é encontrado. O botão de roda também pode operar como um botão médio normal do Windows (terceiro). Pressionar e liberar a roda do mouse envia mensagens padrão do [**WM \_ MBUTTONUP**](wm-mbuttonup.md) e do [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md) . Clicar duas vezes no terceiro botão envia a mensagem padrão do [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md) .

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
| Edição avançada da Microsoft 1,0 | Vertical. Observe que o cliente do Exchange tem suas próprias versões dos controles de exibição de lista e de exibição de árvore que não têm suporte à roda.                                        |
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

## <a name="see-also"></a>Consulte também

[Aproveitando o movimento do High-Definition mouse](../dxtecharts/taking-advantage-of-high-dpi-mouse-movement.md)