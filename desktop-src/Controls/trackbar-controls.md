---
title: Sobre controles TrackBar
description: Um TrackBar é uma janela que contém um controle deslizante (às vezes chamado de Thumb) em um canal e marcas de escala opcionais. Quando o usuário move o controle deslizante, usando o mouse ou as teclas de direção, o TrackBar envia mensagens de notificação para indicar a alteração.
ms.assetid: 9fc7bef8-da1d-493b-9a9a-3770873713f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e364f57a094ed5a29369a00a112150d0282f24
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641897"
---
# <a name="about-trackbar-controls"></a>Sobre controles TrackBar

Um TrackBar é uma janela que contém um controle deslizante (às vezes chamado de Thumb) em um canal e marcas de escala opcionais. Quando o usuário move o controle deslizante, usando o mouse ou as teclas de direção, o TrackBar envia mensagens de notificação para indicar a alteração.

-   [Intervalo de seleção](#selection-range)
-   [Mensagens TrackBar](#trackbar-messages)
-   [Mensagens de notificação do TrackBar](#trackbar-notification-messages)
-   [Processamento de mensagem TrackBar padrão](#default-trackbar-message-processing)
-   [Dicas de ferramenta TrackBar](#trackbar-tooltips)

Trackbars são úteis quando você deseja que o usuário selecione um valor inteiro não assinado discreto ou um conjunto de valores inteiros consecutivos sem sinal em um intervalo. Por exemplo, você pode usar um TrackBar para permitir que o usuário defina a taxa de repetição do teclado movendo o controle deslizante para uma determinada marca de escala. A ilustração a seguir mostra um TrackBar típico.

![captura de tela de um TrackBar com rótulos nas extremidades para lento e rápido](images/tkb-simple.png)

O controle deslizante em um TrackBar se move em incrementos que você especifica ao criá-lo. Os valores neste intervalo são chamados de unidades lógicas. Por exemplo, se você especificar que o TrackBar deve ter unidades lógicas que variam de 0 a 5, o controle deslizante poderá ocupar apenas seis posições: uma posição no lado esquerdo do TrackBar e uma posição para cada incremento no intervalo. Normalmente, cada uma dessas posições é identificada por uma marca de escala; no entanto, o número de marcas de escala é arbitrário e pode ser menor que o número de posições lógicas.

Você cria um TrackBar usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe de janela de [**\_ classe TrackBar**](common-control-window-classes.md) . Depois de criar um TrackBar, você pode usar mensagens TrackBar para definir e recuperar muitas de suas propriedades. As alterações que você pode fazer incluem definir as posições mínima e máxima para o controle deslizante, marcas de escala de desenho, definir um intervalo de seleção e reposicionar o controle deslizante.

## <a name="selection-range"></a>Intervalo de seleção

Se você criar um TrackBar com o [**estilo \_ ENABLESELRANGE TBS**](trackbar-control-styles.md) , poderá especificar um intervalo de seleção. O TrackBar realça o intervalo de seleção e exibe marcas de escala triangulares no início e no final, conforme mostrado na ilustração a seguir.

![captura de tela de um TrackBar com um intervalo realçado](images/tkb-selrange.png)

O intervalo de seleção do TrackBar não afeta sua funcionalidade de nenhuma forma. Cabe ao aplicativo implementar o intervalo. Você pode fazer isso de uma das seguintes maneiras:

-   Use um intervalo de seleção para permitir que o usuário defina valores máximos e mínimos para algum parâmetro. Por exemplo, o usuário pode mover o controle deslizante para uma posição e, em seguida, clicar em um botão rotulado como "Max". Em seguida, o aplicativo define o intervalo de seleção para mostrar os valores escolhidos pelo usuário.
-   Limite a movimentação do controle deslizante para um subintervalo predeterminado dentro do controle, manipulando a notificação do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) e desautorizando qualquer movimento fora do intervalo de seleção. Você pode fazer isso, por exemplo, se o intervalo de valores disponíveis para o usuário puder ser alterado devido a outras opções que o usuário fez ou de acordo com os recursos disponíveis.

## <a name="trackbar-messages"></a>Mensagens TrackBar

As unidades lógicas de um TrackBar são o conjunto de valores contíguos que o TrackBar pode representar. Normalmente, eles são definidos especificando o intervalo de valores possíveis com uma [**mensagem \_ SETRANGE tbm**](tbm-setrange.md) assim que o TrackBar tiver sido criado. Os aplicativos podem alterar dinamicamente o intervalo usando **tbm \_ SETRANGE**, [**tbm \_ SETRANGEMAX**](tbm-setrangemax.md)ou [**tbm \_ SETRANGEMIN**](tbm-setrangemin.md).

Para recuperar a posição do controle deslizante (ou seja, o valor que o usuário escolheu), use a mensagem [**tbm \_ GETPOS**](tbm-getpos.md) . Para definir a posição do controle deslizante, use a mensagem [**tbm \_ SETPOS**](tbm-setpos.md) .

Um TrackBar exibe automaticamente as marcas de escala no início e no final, a menos que você especifique o estilo de [**\_ notiques de TBS**](trackbar-control-styles.md) . (No Microsoft Visual Studio editor de recursos, isso significa definir a propriedade de marcas de escala como false.) Você pode usar o estilo de [**\_ escala automática TBS**](trackbar-control-styles.md) para exibir automaticamente marcas de escala adicionais em intervalos regulares ao longo do TrackBar. Por padrão, um TrackBar de **\_ tiques** automáticos de TBS exibe uma marca de escala em cada incremento do intervalo de TrackBar. Para especificar um intervalo diferente para as marcas de escala automáticas, envie a mensagem [**tbm \_ SETTICFREQ**](tbm-setticfreq.md) para o TrackBar. Por exemplo, você pode usar essa mensagem para exibir apenas 10 marcas de escala em um intervalo de 1 a 100.

Para definir a posição de uma marca de escala única, envie [**a \_ mensagem de tbm**](tbm-settic.md) de seleção. Um TrackBar mantém uma matriz de valores DWORD que armazena a posição de cada marca de escala. A matriz não inclui a primeira e a última marca de escala, que o TrackBar cria automaticamente. Você pode especificar um índice nessa matriz ao enviar a mensagem [**tbm \_ GETTIC**](tbm-gettic.md) para recuperar a posição da marca de escala correspondente. Como alternativa, você pode enviar a mensagem [**tbm \_ GETPTICS**](tbm-getptics.md) para recuperar um ponteiro para a matriz. O número de elementos na matriz é igual a dois menores que a contagem de tiques retornada pela mensagem [**tbm \_ GETNUMTICS**](tbm-getnumtics.md) . Isso ocorre porque a contagem retornada por **tbm \_ GETNUMTICS** inclui as primeiras e as últimas marcas de escala, que não estão incluídas na matriz. Para recuperar a posição física de uma marca de escala, em coordenadas do cliente da janela do TrackBar, envie a mensagem [**tbm \_ GETTICPOS**](tbm-getticpos.md) . A mensagem [**tbm \_ CLEARTICS**](tbm-cleartics.md) remove todas as primeiras e as últimas das marcas de escala de uma TrackBar.

O tamanho da linha de um TrackBar determina a distância com que o controle deslizante se move em resposta à entrada do teclado das teclas de direção, como a seta para a direita ou a tecla de seta para baixo. Para recuperar ou definir o tamanho da linha, envie as mensagens [**tbm \_**](tbm-getlinesize.md) getlineize e [**tbm \_**](tbm-setlinesize.md) setlinese. O TrackBar também envia os códigos de notificação da lista de TB \_ e TB \_ LINEDOWN para sua janela pai quando o usuário pressiona as teclas de direção.

O tamanho de página de um TrackBar determina o quanto o controle deslizante se move em resposta à entrada do teclado, como a tecla PAGE UP ou PAGE DOWN, ou a entrada do mouse, como cliques no canal TrackBar. Para recuperar ou definir o tamanho da página, envie as mensagens [**tbm \_**](tbm-getpagesize.md) GetPages e [**tbm \_ SetPageSize**](tbm-setpagesize.md) . O TrackBar também envia os códigos de notificação de TB \_ PageUp e TB \_ PageDown para sua janela pai quando recebe entrada de teclado ou mouse que rola a página. Para obter mais informações, consulte [mensagens de notificação do TrackBar](#trackbar-notification-messages).

Um aplicativo pode enviar mensagens para recuperar as dimensões de um TrackBar. A mensagem [**tbm \_ GETTHUMBRECT**](tbm-getthumbrect.md) recupera o retângulo delimitador do controle deslizante. A mensagem [**tbm \_ GETTHUMBLENGTH**](tbm-getthumblength.md) recupera o comprimento do controle deslizante. A mensagem [**tbm \_ GETCHANNELRECT**](tbm-getchannelrect.md) recupera o retângulo delimitador para o canal do TrackBar, que é a área sobre a qual o controle deslizante se move. Ele contém o realce quando um intervalo é selecionado. Se um TrackBar tiver o [**estilo \_ Cadeia TBS**](trackbar-control-styles.md) , você poderá enviar a [**mensagem \_ tbm SETTHUMBLENGTH**](tbm-setthumblength.md) para alterar o comprimento do controle deslizante.

Você recupera ou define o intervalo de seleção enviando mensagens para o TrackBar. Use a mensagem [**tbm \_ SETSEL**](tbm-setsel.md) para definir as posições inicial e final de uma seleção. Para definir apenas a posição inicial ou apenas a posição final de uma seleção, envie uma mensagem [**tbm \_ SETSELSTART**](tbm-setselstart.md) ou [**tbm \_ SETSELEND**](tbm-setselend.md) . Para recuperar as posições inicial ou final de um intervalo de seleção, envie uma mensagem [**tbm \_ GETSELSTART**](tbm-getselstart.md) ou [**tbm \_ GETSELEND**](tbm-getselend.md) . Para limpar um intervalo de seleção e restaurar o TrackBar para seu intervalo original, envie a mensagem [**tbm \_ CLEARSEL**](tbm-clearsel.md) .

> [!Note]  
> É responsabilidade do aplicativo garantir que o usuário não possa selecionar valores fora do intervalo de seleção. O próprio controle não impede que o usuário mova o controle deslizante para fora do intervalo.

 

## <a name="trackbar-notification-messages"></a>Mensagens de notificação do TrackBar

Um TrackBar notifica sua janela pai sobre ações do usuário enviando o pai uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) . Um TrackBar com o [**estilo \_ na horizontal TBS**](trackbar-control-styles.md) envia mensagens do **WM \_ HSCROLL** . Um TrackBar com o [**estilo \_ vertical do TBS**](trackbar-control-styles.md) envia mensagens do **WM \_ VSCROLL** . A palavra de ordem inferior do parâmetro *wParam* do **WM \_ HSCROLL** ou do **WM \_ VSCROLL** contém o código de notificação. Para os \_ códigos de notificação TB THUMBPOSITION e TB \_ THUMBTRACK, a palavra de ordem superior do parâmetro *wParam* especifica a posição do controle deslizante. Para todos os outros códigos de notificação, a palavra de ordem superior é zero; Envie a mensagem [**tbm \_ GETPOS**](tbm-getpos.md) para determinar a posição do controle deslizante. O parâmetro *lParam* é o identificador para o TrackBar.

O sistema envia a parte de TB \_ inferior, TB \_ LINEDOWN, TB \_ e \_ códigos de notificação principais somente quando o usuário interage com um TrackBar usando o teclado. Os \_ códigos de notificação de THUMBTRACK TB THUMBPOSITION e TB \_ são enviados somente quando o usuário está usando o mouse. Os códigos de notificação de PageUp de TB de \_ faixa, TB \_ PageDown e TB \_ são enviados em ambos os casos. A tabela a seguir lista os códigos de notificação do TrackBar e os eventos (códigos de chave virtual ou eventos de mouse) que fazem com que as notificações de [**códigos de chaves virtuais**](/windows/desktop/inputdev/virtual-key-codes)sejam enviadas.



| Código de notificação | Motivo de envio                                                                                                                     |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| TB \_ inferior        | [**VK \_ fim**](/windows/desktop/inputdev/virtual-key-codes)                                                                         |
| endtrack de TB \_      | [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) (o usuário lançou uma chave que enviou um código de chave virtual relevante)                              |
| TB de \_ LINEDOWN      | [**VK \_ DIREITA**](/windows/desktop/inputdev/virtual-key-codes) ou [ **VK \_ para baixo**](/windows/desktop/inputdev/virtual-key-codes)     |
| linha de TB \_        | [**VK \_ ESQUERDA**](/windows/desktop/inputdev/virtual-key-codes) ou [ **VK \_ cima**](/windows/desktop/inputdev/virtual-key-codes)              |
| TB \_ PageDown      | [**VK \_ Em seguida**](/windows/desktop/inputdev/virtual-key-codes) (o usuário clicou no canal abaixo ou à direita do controle deslizante)   |
| TB de \_ PageUp        | [**VK \_ ANTES**](/windows/desktop/inputdev/virtual-key-codes) (o usuário clicou no canal acima ou à esquerda do controle deslizante) |
| TB de \_ THUMBPOSITION | [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) seguindo um \_ código de notificação de THUMBTRACK TB                                         |
| TB de \_ THUMBTRACK    | Movimentação do controle deslizante (o usuário arrastou o controle deslizante)                                                                                   |
| TB \_ superior           | [**\_página inicial do VK**](/windows/desktop/inputdev/virtual-key-codes)                                                                      |



 

## <a name="default-trackbar-message-processing"></a>Processamento de mensagem TrackBar padrão

Esta seção descreve o processamento de mensagem de janela executado por um TrackBar.



| Mensagem                                              | Processamento realizado                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ capturachanged**](/windows/desktop/inputdev/wm-capturechanged) | Interrompe o temporizador se um tiver sido definido durante o processamento de [**\_ LBUTTONDOWN do WM**](/windows/desktop/inputdev/wm-lbuttondown) e enviará o \_ código de notificação TB THUMBPOSITION, se necessário. Ele sempre envia o \_ código de notificação de faixa TB.                                     |
| [**criação do WM \_**](/windows/desktop/winmsg/wm-create)                   | Executa uma inicialização adicional, como definir o tamanho da linha, o tamanho da página e a frequência da marca de escala com os valores padrão.                                                                                                                                 |
| [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)                 | Libera recursos.                                                                                                                                                                                                                                         |
| [**habilitar o WM \_**](/windows/desktop/winmsg/wm-enable)                   | Redesenha a janela TrackBar.                                                                                                                                                                                                                            |
| [**ERASEBKGND do WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)           | Apaga o plano de fundo da janela, usando a cor de plano de fundo atual para o TrackBar.                                                                                                                                                                       |
| [**GETDLGCODE do WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)           | Retorna o valor de WANTARROWS de DLGC \_ .                                                                                                                                                                                                                      |
| [**o WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)               | Processa as teclas de direção e envia as TB, na parte superior, nos TB inferior, nos \_ \_ TB \_ PageUp, TB PageDown, na lista de \_ TB \_ e nos códigos de notificação de \_ LINEDOWN TB, conforme apropriado.                                                                                               |
| [**o WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)                   | Envia o \_ código de notificação de ENDTRACK TB se a chave tiver sido uma das chaves de direção.                                                                                                                                                                       |
| [**KILLFOCUS do WM \_**](/windows/desktop/inputdev/wm-killfocus)           | Redesenha a janela TrackBar.                                                                                                                                                                                                                            |
| [**LBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-lbuttondown)       | Define o foco e a captura do mouse para o TrackBar. Quando necessário, ele define um temporizador que determina com que rapidez o controle deslizante se move para o cursor do mouse quando o usuário mantém o botão do mouse na janela.                                      |
| [**LBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-lbuttonup)           | Libera a captura do mouse e encerra o temporizador se um tiver sido definido durante o processamento de [**\_ LBUTTONDOWN do WM**](/windows/desktop/inputdev/wm-lbuttondown) . Ele envia o \_ código de notificação THUMBPOSITION TB, se necessário. Ele sempre envia o \_ código de notificação de faixa TB. |
| [**admousemove do WM \_**](/windows/desktop/inputdev/wm-mousemove)           | Move o controle deslizante e envia o código de notificação de TB \_ THUMBTRACK ao rastrear o mouse (consulte o [**\_ temporizador do WM**](/windows/desktop/winmsg/wm-timer)).                                                                                                                          |
| [**pintura do WM \_**](/windows/desktop/gdi/wm-paint)                        | Pinta o TrackBar. Se o parâmetro wParam for não nulo, o controle assumirá que o valor é um HDC e pinta usando esse contexto de dispositivo.                                                                                                             |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)             | Redesenha a janela TrackBar.                                                                                                                                                                                                                            |
| [**tamanho do WM \_**](/windows/desktop/winmsg/wm-size)                       | Define as dimensões do TrackBar, removendo o controle deslizante se não houver espaço suficiente para exibi-lo.                                                                                                                                                      |
| [**\_temporizador do WM**](/windows/desktop/winmsg/wm-timer)                     | Recupera a posição do mouse e atualiza a posição do controle deslizante. (Ele é recebido somente quando o usuário está arrastando o controle deslizante.)                                                                                                                         |
| [**WININICHANGE do WM \_**](/windows/desktop/winmsg/wm-wininichange)       | Inicializa dimensões do controle deslizante.                                                                                                                                                                                                                           |



 

## <a name="trackbar-tooltips"></a>Dicas de ferramenta TrackBar

Um TrackBar que é criado com o estilo de [**\_ dicas de ferramenta TBS**](trackbar-control-styles.md) tem um controle ToolTip padrão. A dica de ferramenta permanece visível e exibe o valor atual, pois o usuário arrasta o controle deslizante usando o mouse.

Você pode atribuir um novo controle ToolTip a um TrackBar enviando a mensagem [**tbm \_ SetToolTips**](tbm-settooltips.md) . Para recuperar o identificador para um controle ToolTip atribuído, use a mensagem [**tbm \_ GetToolTips**](tbm-gettooltips.md) .

 

 