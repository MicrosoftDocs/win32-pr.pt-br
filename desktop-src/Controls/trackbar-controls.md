---
title: Sobre controles trackbar
description: Uma barra de faixa é uma janela que contém um controle deslizante (às vezes chamado de thumb) em um canal e marcas de escala opcionais. Quando o usuário move o controle deslizante, usando o mouse ou as teclas de direção, a barra de faixa envia mensagens de notificação para indicar a alteração.
ms.assetid: 9fc7bef8-da1d-493b-9a9a-3770873713f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450fba1c9b41cf5789bcda08263ff7a0b8b2d2d17db3746cf5d47bdc5d0b6a4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967928"
---
# <a name="about-trackbar-controls"></a>Sobre controles trackbar

Uma barra de faixa é uma janela que contém um controle deslizante (às vezes chamado de thumb) em um canal e marcas de escala opcionais. Quando o usuário move o controle deslizante, usando o mouse ou as teclas de direção, a barra de faixa envia mensagens de notificação para indicar a alteração.

-   [Intervalo de seleção](#selection-range)
-   [Mensagens da barra de faixa](#trackbar-messages)
-   [Mensagens de notificação da barra de faixas](#trackbar-notification-messages)
-   [Processamento de mensagens da barra de faixa padrão](#default-trackbar-message-processing)
-   [Dicas de ferramenta da barra de faixas](#trackbar-tooltips)

As barras de faixa são úteis quando você deseja que o usuário selecione um valor inteiro sem sinal discreto ou um conjunto de valores inteiros sem sinal consecutivos em um intervalo. Por exemplo, você pode usar uma barra de faixa para permitir que o usuário de definir a taxa de repetição do teclado movendo o controle deslizante para uma determinada marca de escala. A ilustração a seguir mostra uma barra de faixa típica.

![captura de tela de uma barra de faixa com rótulos nas extremidades para lentidão e rapidez](images/tkb-simple.png)

O controle deslizante em uma barra de faixa se move em incrementos que você especifica ao criar. Os valores nesse intervalo são chamados de unidades lógicas. Por exemplo, se você especificar que a barra de faixa deve ter unidades lógicas que variam de 0 a 5, o controle deslizante poderá ocupar apenas seis posições: uma posição no lado esquerdo da barra de faixa e uma posição para cada incremento no intervalo. Normalmente, cada uma dessas posições é identificada por uma marca de escala; no entanto, o número de marcas de escala é arbitrário e pode ser menor que o número de posições lógicas.

Você cria uma barra de faixa usando a [**função CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especificando a [**classe de janela TRACKBAR \_ CLASS.**](common-control-window-classes.md) Depois de criar uma barra de faixa, você pode usar mensagens da barra de faixa para definir e recuperar muitas de suas propriedades. As alterações que você pode fazer incluem definir as posições mínima e máxima para o controle deslizante, desenhar marcas de escala, definir um intervalo de seleção e reposicionar o controle deslizante.

## <a name="selection-range"></a>Intervalo de seleção

Se você criar uma barra de faixa com o [**estilo TBS \_ ENABLESELRANGE,**](trackbar-control-styles.md) poderá especificar um intervalo de seleção. A barra de faixa realça o intervalo de seleção e exibe marcas de escala triangulares no início e no final, conforme mostrado na ilustração a seguir.

![captura de tela de uma barra de faixa com um intervalo realçada](images/tkb-selrange.png)

O intervalo de seleção da barra de faixas não afeta sua funcionalidade de forma alguma. O aplicativo deve implementar o intervalo. Você pode fazer isso de uma das seguintes maneiras:

-   Use um intervalo de seleção para habilitar o usuário a definir valores mínimos e máximos para algum parâmetro. Por exemplo, o usuário pode mover o controle deslizante para uma posição e clicar em um botão rotulado como "Max". Em seguida, o aplicativo define o intervalo de seleção para mostrar os valores escolhidos pelo usuário.
-   Limite o movimento do controle deslizante a um subinterrange predeterminado dentro do controle, manipulando a notificação [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) e não permite qualquer movimentação fora do intervalo de seleção. Você pode fazer isso, por exemplo, se o intervalo de valores disponíveis para o usuário puder mudar devido a outras escolhas que o usuário fez ou de acordo com os recursos disponíveis.

## <a name="trackbar-messages"></a>Mensagens da barra de faixa

As unidades lógicas de uma barra de faixa são o conjunto de valores contíguos que a barra de faixa pode representar. Normalmente, eles são definidos especificando o intervalo de valores possíveis com uma mensagem [**\_ SETRANGE de TBM**](tbm-setrange.md) assim que a barra de faixas tiver sido criada. Os aplicativos podem alterar dinamicamente o intervalo usando **TBM \_ SETRANGE**, [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)ou [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md).

Para recuperar a posição do controle deslizante (ou seja, o valor escolhido pelo usuário), use a [**mensagem \_ GETPOS do TBM.**](tbm-getpos.md) Para definir a posição do controle deslizante, use a [**mensagem \_ SETPOS do TBM.**](tbm-setpos.md)

Uma barra de faixa exibe automaticamente as marcas de escala no início e no fim, a menos que você especifique o [**estilo \_ NOTICKS do TBS.**](trackbar-control-styles.md) (No editor Microsoft Visual Studio de recursos, isso significa definir a propriedade Marcas de Escala como False.) Você pode usar o estilo [**TBS \_ AUTOTICKS**](trackbar-control-styles.md) para exibir automaticamente marcas de escala adicionais em intervalos regulares ao longo da barra de faixa. Por padrão, uma **barra de faixa \_ TBS AUTOTICKS** exibe uma marca de escala em cada incremento do intervalo da barra de faixas. Para especificar um intervalo diferente para as marcas de escala automáticas, envie a [**mensagem \_ TBM SETTICFREQ**](tbm-setticfreq.md) para a barra de faixas. Por exemplo, você pode usar essa mensagem para exibir apenas 10 marcas de escala em um intervalo de 1 a 100.

Para definir a posição de uma única marca de escala, envie a [**mensagem \_ SETTIC tbm.**](tbm-settic.md) Uma barra de faixa mantém uma matriz de valores DWORD que armazena a posição de cada marca de escala. A matriz não inclui as primeiras e as últimas marcas de escala, que a barra de faixa cria automaticamente. Você pode especificar um índice nessa matriz ao enviar a mensagem [**\_ GETTIC TBM**](tbm-gettic.md) para recuperar a posição da marca de escala correspondente. Como alternativa, você pode enviar a [**mensagem \_ GETPTICS do TBM**](tbm-getptics.md) para recuperar um ponteiro para a matriz. O número de elementos na matriz é igual a dois a menos que a contagem de tiques retornada pela [**mensagem \_ GETNUMTICS de TBM.**](tbm-getnumtics.md) Isso porque a contagem retornada por **TBM \_ GETNUMTICS** inclui as primeiras e as últimas marcas de escala, que não estão incluídas na matriz. Para recuperar a posição física de uma marca de escala, nas coordenadas do cliente da janela da barra de faixas, envie a [**mensagem \_ TBM GETTICPOS.**](tbm-getticpos.md) A [**mensagem \_ TBM CLEARTICS**](tbm-cleartics.md) remove todas, menos a primeira e a última das marcas de escala de uma barra de faixa.

O tamanho da linha de uma barra de faixa determina até que ponto o controle deslizante se move em resposta à entrada do teclado das teclas de direção, como a seta para a direita ou a tecla SETA PARA BAIXO. Para recuperar ou definir o tamanho da linha, envie as [**mensagens \_ GETLINESIZE**](tbm-getlinesize.md) [**e TBM \_ SETLINESIZE.**](tbm-setlinesize.md) A barra de faixa também envia os códigos de notificação TBTB e TB LINEDOWN para sua janela pai quando o usuário \_ \_ pressiona as teclas de seta.

O tamanho da página de uma barra de faixa determina até que ponto o controle deslizante se move em resposta à entrada do teclado, como a tecla PAGE UP ou PAGE DOWN ou a entrada do mouse, como cliques no canal da barra de faixa. Para recuperar ou definir o tamanho da página, envie as [**mensagens \_ TBM GETPAGESIZE**](tbm-getpagesize.md) e [**TBM \_ SETPAGESIZE.**](tbm-setpagesize.md) A barra de faixa também envia os códigos de notificação PAGEUP e PAGEDOWN de TB para sua janela pai quando recebe a entrada do teclado ou mouse que \_ \_ rola a página. Para obter mais informações, consulte [Mensagens de notificação da barra de controle](#trackbar-notification-messages).

Um aplicativo pode enviar mensagens para recuperar as dimensões de uma barra de faixa. A [**mensagem \_ TBM GETTHUMBRECT**](tbm-getthumbrect.md) recupera o retângulo delimitador do controle deslizante. A [**mensagem \_ TBM GETTHUMBLENGTH**](tbm-getthumblength.md) recupera o comprimento do controle deslizante. A [**mensagem TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md) recupera o retângulo delimitador para o canal da barra de faixas, que é a área sobre a qual o controle deslizante se move. Ele contém o realçando quando um intervalo é selecionado. Se uma barra de faixa tiver o estilo [**\_ FIXEDLENGTH TBS,**](trackbar-control-styles.md) você poderá enviar a mensagem [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md) para alterar o comprimento do controle deslizante.

Você recupera ou configura o intervalo de seleção enviando mensagens para a barra de faixas. Use a [**mensagem TBM \_ SETSEL**](tbm-setsel.md) para definir as posições inicial e final de uma seleção. Para definir apenas a posição inicial ou apenas a posição final de uma seleção, envie uma mensagem [**TBM \_ SETSELSTART**](tbm-setselstart.md) ou [**TBM \_ SETSELEND.**](tbm-setselend.md) Para recuperar as posições inicial ou final de um intervalo de seleção, envie uma [**mensagem TBM \_ GETSELSTART**](tbm-getselstart.md) ou [**TBM \_ GETSELEND.**](tbm-getselend.md) Para limpar um intervalo de seleção e restaurar a barra de faixas para seu intervalo original, envie a [**mensagem \_ TBM CLEARSEL.**](tbm-clearsel.md)

> [!Note]  
> É responsabilidade do aplicativo garantir que o usuário não possa selecionar valores fora do intervalo de seleção. O controle em si não impede que o usuário move o controle deslizante para fora do intervalo.

 

## <a name="trackbar-notification-messages"></a>Mensagens de notificação da barra de faixas

Uma barra de faixa notifica sua janela pai de ações do usuário enviando ao pai uma mensagem [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL.**](wm-vscroll.md) Uma barra de faixa com o [**estilo \_ TBS HORZ**](trackbar-control-styles.md) envia **mensagens WM \_ HSCROLL.** Uma barra de faixa com o [**estilo \_ TBS VERT**](trackbar-control-styles.md) envia **mensagens WM \_ VSCROLL.** A palavra de ordem baixa do *parâmetro wParam* de **WM \_ HSCROLL** ou **WM \_ VSCROLL** contém o código de notificação. Para os códigos de notificação THUMBPOSITION e TB THUMBTRACK, a palavra de ordem alta do parâmetro \_ \_ *wParam* especifica a posição do controle deslizante. Para todos os outros códigos de notificação, a palavra de ordem alta é zero; envie a [**mensagem \_ GETPOS do TBM**](tbm-getpos.md) para determinar a posição do controle deslizante. O *parâmetro lParam* é o alça para a barra de faixas.

O sistema envia os códigos de notificação TB \_ BOTTOM, TB \_ LINEDOWN, TBTB e TB TOP somente quando o usuário interage com uma barra de faixa usando \_ \_ o teclado. Os códigos \_ de notificação THUMBPOSITION e TB THUMBTRACK de TB só são enviados quando o usuário está usando o \_ mouse. Os códigos de \_ notificação PAGEUP TB ENDTRACK, TB PAGEDOWN e \_ TB são enviados em ambos os \_ casos. A tabela a seguir lista os códigos de notificação da barra de faixa e os eventos (códigos de chave virtual ou eventos do mouse) que causam o enviado das notificações de Códigos de Chave [**Virtual.**](/windows/desktop/inputdev/virtual-key-codes)



| Código de notificação | Motivo enviado                                                                                                                     |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| TB \_ BOTTOM        | [**FIM \_ da VK**](/windows/desktop/inputdev/virtual-key-codes)                                                                         |
| TB \_ ENDTRACK      | [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) (o usuário lançou uma chave que enviou um código de chave virtual relevante)                              |
| LINEDOWN DE TB \_      | [**VK \_ RIGHT**](/windows/desktop/inputdev/virtual-key-codes) ou [ **VK \_ DOWN**](/windows/desktop/inputdev/virtual-key-codes)     |
| TB \_ LINEUP        | [**VK \_ LEFT**](/windows/desktop/inputdev/virtual-key-codes) ou [ **VK \_ UP**](/windows/desktop/inputdev/virtual-key-codes)              |
| PAGEDOWN DE TB \_      | [**VK \_ NEXT**](/windows/desktop/inputdev/virtual-key-codes) (o usuário clicou no canal abaixo ou à direita do controle deslizante)   |
| PAGEUP DE TB \_        | [**VK \_ PRIOR**](/windows/desktop/inputdev/virtual-key-codes) (o usuário clicou no canal acima ou à esquerda do controle deslizante) |
| POSIÇÃO DIGITAL DE TB \_ | [**WM \_ LBUTTONUP seguindo um**](/windows/desktop/inputdev/wm-lbuttonup) código de notificação \_ DE TB THUMBTRACK                                         |
| TB \_ THUMBTRACK    | Movimento do controle deslizante (o usuário arrastou o controle deslizante)                                                                                   |
| TB \_ TOP           | [**VK \_ HOME**](/windows/desktop/inputdev/virtual-key-codes)                                                                      |



 

## <a name="default-trackbar-message-processing"></a>Processamento de mensagens da barra de faixa padrão

Esta seção descreve o processamento de mensagem de janela executado por uma barra de faixas.



| Mensagem                                              | Processamento executado                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAPTURECHANGED**](/windows/desktop/inputdev/wm-capturechanged) | Elimina o temporizador se um tiver sido definido durante o processamento de [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) e envia o código de notificação THUMBPOSITION do \_ TB, se necessário. Ele sempre envia o código de \_ notificação TB ENDTRACK.                                     |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                   | Executa a inicialização adicional, como definir o tamanho da linha, o tamanho da página e a frequência de marca de escala para valores padrão.                                                                                                                                 |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)                 | Libera recursos.                                                                                                                                                                                                                                         |
| [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)                   | Reintsimos a janela da barra de faixas.                                                                                                                                                                                                                            |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)           | Apaga a tela de fundo da janela usando a cor da tela de fundo atual para a barra de faixas.                                                                                                                                                                       |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)           | Retorna o valor \_ WANTARROWS do DLGC.                                                                                                                                                                                                                      |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)               | Processa as teclas de direção e envia os códigos de notificação TB \_ TOP, TB \_ BOTTOM, TB \_ PAGEUP, TB \_ PAGEDOWN, \_ TBTB e TB \_ LINEDOWN, conforme apropriado.                                                                                               |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)                   | Envia o código \_ de notificação TB ENDTRACK se a chave era uma das teclas de direção.                                                                                                                                                                       |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)           | Reintsimos a janela da barra de faixas.                                                                                                                                                                                                                            |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)       | Define o foco e a captura do mouse para a barra de faixas. Quando necessário, ele define um temporizador que determina a rapidez com que o controle deslizante se move para o cursor do mouse quando o usuário mantém o botão do mouse pressionado na janela.                                      |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)           | Libera a captura do mouse e encerra o temporizador se um tiver sido definido durante o processamento [**de WM \_ LBUTTONDOWN.**](/windows/desktop/inputdev/wm-lbuttondown) Ele envia o código de \_ notificação THUMBPOSITION de TB, se necessário. Ele sempre envia o código de \_ notificação TB ENDTRACK. |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)           | Move o controle deslizante e envia o código de notificação TB THUMBTRACK ao acompanhar \_ o mouse (consulte [**WM \_ TIMER**](/windows/desktop/winmsg/wm-timer)).                                                                                                                          |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                        | Pinta a barra de faixa. Se o parâmetro wParam for não NULL, o controle assumirá que o valor é um HDC e pintará usando esse contexto de dispositivo.                                                                                                             |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)             | Reintsimos a janela da barra de faixas.                                                                                                                                                                                                                            |
| [**TAMANHO \_ DO WM**](/windows/desktop/winmsg/wm-size)                       | Define as dimensões da barra de faixa, removendo o controle deslizante se não houver espaço suficiente para exibi-lo.                                                                                                                                                      |
| [**TEMPORIZADOR \_ DE WM**](/windows/desktop/winmsg/wm-timer)                     | Recupera a posição do mouse e atualiza a posição do controle deslizante. (Ele é recebido somente quando o usuário está arrastando o controle deslizante.)                                                                                                                         |
| [**WM \_ WININICHANGE**](/windows/desktop/winmsg/wm-wininichange)       | Inicializa dimensões do controle deslizante.                                                                                                                                                                                                                           |



 

## <a name="trackbar-tooltips"></a>Dicas de ferramenta da barra de faixas

Uma barra de faixa criada com o estilo [**TBS \_ TOOLTIPS**](trackbar-control-styles.md) tem um controle de dica de ferramenta padrão. A dica de ferramenta permanece visível e exibe o valor atual conforme o usuário arrasta o controle deslizante usando o mouse.

Você pode atribuir um novo controle de dica de ferramenta a uma barra de faixa enviando a [**mensagem TBM \_ SETTOOLTIPS.**](tbm-settooltips.md) Para recuperar o alça para um controle de dica de ferramenta atribuído, use a [**mensagem \_ GETTOOLTIPS do TBM.**](tbm-gettooltips.md)

 

 