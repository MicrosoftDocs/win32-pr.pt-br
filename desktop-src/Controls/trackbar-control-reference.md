---
title: Trackbar
description: Esta seção contém informações sobre os elementos de programação usados com controles de barra de faixa.
ms.assetid: vs|controls|~\controls\trackbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f56c5a483340a8e77ef0df6503481d3cbc50e51a85bd07258cdf283dd563c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060536"
---
# <a name="trackbar"></a>Trackbar

Esta seção contém informações sobre os elementos de programação usados com controles de barra de faixa.

### <a name="overviews"></a>Visões gerais



| Tópico                                                  | Sumário                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre controles trackbar](trackbar-controls.md)       | Uma barra de faixa é uma janela que contém um controle deslizante (às vezes chamado de thumb) em um canal e marcas de escala opcionais. Quando o usuário move o controle deslizante, usando o mouse ou as teclas de direção, a barra de faixa envia mensagens de notificação para indicar a alteração.<br/> |
| [Usando controles trackbar](using-trackbar-controls.md) | Esta seção fornece detalhes de implementação e exemplos para controles de barra de faixa.<br/>                                                                                                                                                                               |



 

### <a name="messages"></a>Mensagens



| Tópico                                                 | Sumário                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TBM \_ CLEARSEL**](tbm-clearsel.md)                 | Limpa o intervalo de seleção atual em uma barra de faixas. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ CLEARTICS**](tbm-cleartics.md)               | Remove as marcas de escala atuais de uma barra de faixa. Essa mensagem não remove as primeiras e as últimas marcas de escala, que são criadas automaticamente pela barra de faixa. <br/>                                                                                                                                           |
| [**TBM \_ GETBUDDY**](tbm-getbuddy.md)                 | Recupera o alça para uma janela do parceiro de controle da barra de faixas em um determinado local. O local especificado é relativo à orientação do controle (horizontal ou vertical). <br/>                                                                                                                                 |
| [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md)     | Recupera o tamanho e a posição do retângulo delimitado para o canal de uma barra de faixa. (O canal é a área sobre a qual o controle deslizante se move. Ele contém o realçando quando um intervalo é selecionado.) <br/>                                                                                                         |
| [**TBM \_ GETLINESIZE**](tbm-getlinesize.md)           | Recupera o número de posições lógicas que o controle deslizante da barra de faixa move em resposta à entrada do teclado das teclas de direção, como as teclas ou . As posições lógicas são os incrementos inteiros no intervalo da barra de faixa de posições mínimas para máximas do controle deslizante. <br/>                                         |
| [**TBM \_ GETNUMTICS**](tbm-getnumtics.md)             | Recupera o número de marcas de escala em uma barra de faixa. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)           | Recupera o número de posições lógicas que o controle deslizante da barra de faixa move em resposta à entrada do teclado, como as teclas ou ou a entrada do mouse, como cliques no canal da barra de faixa. As posições lógicas são os incrementos inteiros no intervalo da barra de faixa de posições mínimas para máximas do controle deslizante. <br/>   |
| [**TBM \_ GETPOS**](tbm-getpos.md)                     | Recupera a posição lógica atual do controle deslizante em uma barra de faixa. As posições lógicas são os valores inteiros no intervalo da barra de faixa das posições mínimas até máximas do controle deslizante. <br/>                                                                                                                       |
| [**TBM \_ GETPTICS**](tbm-getptics.md)                 | Recupera o endereço de uma matriz que contém as posições das marcas de escala para uma barra de faixa. <br/>                                                                                                                                                                                                        |
| [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md)           | Recupera a posição máxima do controle deslizante em uma barra de faixa. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md)           | Recupera a posição mínima para o controle deslizante em uma barra de faixa. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETSELEND**](tbm-getselend.md)               | Recupera a posição final do intervalo de seleção atual em uma barra de faixa. <br/>                                                                                                                                                                                                                            |
| [**TBM \_ GETSELSTART**](tbm-getselstart.md)           | Recupera a posição inicial do intervalo de seleção atual em uma barra de faixa. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)     | Recupera o comprimento do controle deslizante em uma barra de faixa. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md)         | Recupera o tamanho e a posição do retângulo delimitador para o controle deslizante em uma barra de faixa. <br/>                                                                                                                                                                                                                |
| [**TBM \_ GETTIC**](tbm-gettic.md)                     | Recupera a posição lógica de uma marca de escala em uma barra de faixa. A posição lógica pode ser qualquer um dos valores inteiros no intervalo da barra de faixa de posições mínimas a máximas do controle deslizante. <br/>                                                                                                                     |
| [**TBM \_ GETTICPOS**](tbm-getticpos.md)               | Recupera a posição física atual de uma marca de escala em uma barra de faixa.<br/>                                                                                                                                                                                                                                   |
| [**TBM \_ GETTOOLTIPS**](tbm-gettooltips.md)           | Recupera o alça para o controle de dica de ferramenta atribuído à barra de faixas, se for o caso. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md) | Recupera o sinalizador de formato de caractere Unicode para o controle . <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ SETBUDDY**](tbm-setbuddy.md)                 | Atribui uma janela como a janela do parceiro para um controle de barra de faixa. As janelas da barra de faixa são exibidas automaticamente em um local relativo à orientação do controle (horizontal ou vertical). <br/>                                                                                                          |
| [**TBM \_ SETLINESIZE**](tbm-setlinesize.md)           | Define o número de posições lógicas que o controle deslizante da barra de faixa move em resposta à entrada do teclado das teclas de direção, como as teclas ou . As posições lógicas são os incrementos inteiros no intervalo da barra de faixa de posições mínimas para máximas do controle deslizante. <br/>                                              |
| [**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)           | Define o número de posições lógicas que o controle deslizante da barra de faixa move em resposta à entrada do teclado, como as teclas ou ou a entrada do mouse, como cliques no canal da barra de faixas. As posições lógicas são os incrementos inteiros no intervalo da barra de faixa de posições mínimas para máximas do controle deslizante. <br/>        |
| [**TBM \_ SETPOS**](tbm-setpos.md)                     | Define a posição lógica atual do controle deslizante em uma barra de faixa. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETPOSNOTIFY**](tbm-setposnotify.md)         | Define a posição lógica atual do controle deslizante em uma barra de faixa. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETRANGE**](tbm-setrange.md)                 | Define o intervalo de posições lógicas mínimas e máximas para o controle deslizante em uma barra de faixa. <br/>                                                                                                                                                                                                                  |
| [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)           | Define a posição lógica máxima para o controle deslizante em uma barra de faixa. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)           | Define a posição lógica mínima para o controle deslizante em uma barra de faixa. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETSEL**](tbm-setsel.md)                     | Define as posições inicial e final para o intervalo de seleção disponível em uma barra de faixa. <br/>                                                                                                                                                                                                                |
| [**TBM \_ SETSELEND**](tbm-setselend.md)               | Define a posição lógica final do intervalo de seleção atual em uma barra de faixa. Essa mensagem será ignorada se a barra de faixas não tiver o [**estilo TBS \_ ENABLESELRANGE.**](trackbar-control-styles.md) <br/>                                                                              |
| [**TBM \_ SETSELSTART**](tbm-setselstart.md)           | Define a posição lógica inicial do intervalo de seleção atual em uma barra de faixa. Essa mensagem será ignorada se a barra de faixas não tiver o [**estilo TBS \_ ENABLESELRANGE.**](trackbar-control-styles.md) <br/>                                                                            |
| [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md)     | Define o comprimento do controle deslizante em uma barra de faixa. Essa mensagem será ignorada se a barra de faixas não tiver o [**estilo \_ FIXEDLENGTH TBS.**](trackbar-control-styles.md) <br/>                                                                                                                      |
| [**TBM \_ SETTIC**](tbm-settic.md)                     | Define uma marca de escala em uma barra de faixa na posição lógica especificada. <br/>                                                                                                                                                                                                                                      |
| [**TBM \_ SETTICFREQ**](tbm-setticfreq.md)             | Define a frequência de intervalo para marcas de escala em uma barra de faixa. Por exemplo, se a frequência for definida como dois, uma marca de escala será exibida para todos os outros incrementos no intervalo da barra de faixas. A configuração padrão para a frequência é uma; ou seja, cada incremento no intervalo é associado a uma marca de escala. <br/> |
| [**TBM \_ SETTIPSIDE**](tbm-settipside.md)             | Posiciona um controle de dica de ferramenta usado por um controle de barra de faixa. Controles de barra de faixa que usam as dicas de ferramenta de exibição de estilo [**\_ TBS TOOLTIPS.**](trackbar-control-styles.md) <br/>                                                                                                                           |
| [**TBM \_ SETtooltip**](tbm-settooltips.md)           | Atribui um controle ToolTip a um controle TrackBar. <br/>                                                                                                                                                                                                                                                       |
| [**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md) | Define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle. <br/>                                                                                                               |



 

### <a name="notifications"></a>Notificações



| Tópico                                                              | Sumário                                                                                                                                                                                      |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (TrackBar)](nm-customdraw-trackbar.md)            | Enviado por um controle TrackBar para notificar suas janelas pai sobre as operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>        |
| [NM \_ RELEASEDCAPTURE (TrackBar)](nm-releasedcapture-trackbar-.md) | Notifica uma janela pai do controle TrackBar que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/> |
| [TRBN \_ THUMBPOSCHANGING](trbn-thumbposchanging.md)                | Notifica que a posição do Thumb em um TrackBar está sendo alterada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                               |



 

### <a name="constants"></a>Constantes



| Tópico                                                  | Sumário                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Valores de desenho personalizados](custom-draw-values.md)           | Esta seção lista os valores usados para identificar as partes de um controle TrackBar. <br/>      |
| [Estilos de controle TrackBar](trackbar-control-styles.md) | Esta seção contém informações sobre os estilos usados com controles TrackBar. <br/> |



 

 

 





