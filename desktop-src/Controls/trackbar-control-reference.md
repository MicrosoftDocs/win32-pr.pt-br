---
title: TrackBar
description: Esta seção contém informações sobre os elementos de programação usados com controles TrackBar.
ms.assetid: vs|controls|~\controls\trackbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe8e58cd8db9c2811f31cac92ee3d1d31c2c02d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753566"
---
# <a name="trackbar"></a>TrackBar

Esta seção contém informações sobre os elementos de programação usados com controles TrackBar.

### <a name="overviews"></a>Visões gerais



| Tópico                                                  | Sumário                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre controles TrackBar](trackbar-controls.md)       | Um TrackBar é uma janela que contém um controle deslizante (às vezes chamado de Thumb) em um canal e marcas de escala opcionais. Quando o usuário move o controle deslizante, usando o mouse ou as teclas de direção, o TrackBar envia mensagens de notificação para indicar a alteração.<br/> |
| [Usando controles TrackBar](using-trackbar-controls.md) | Esta seção fornece detalhes de implementação e exemplos para controles TrackBar.<br/>                                                                                                                                                                               |



 

### <a name="messages"></a>Mensagens



| Tópico                                                 | Sumário                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TBM \_ CLEARSEL**](tbm-clearsel.md)                 | Limpa o intervalo de seleção atual em um TrackBar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ CLEARTICS**](tbm-cleartics.md)               | Remove as marcas de escala atuais de um TrackBar. Essa mensagem não remove a primeira e a última marca de escala, que são criadas automaticamente pelo TrackBar. <br/>                                                                                                                                           |
| [**TBM \_ GETbuddy**](tbm-getbuddy.md)                 | Recupera o identificador para uma janela de amigo do controle TrackBar em um determinado local. O local especificado é relativo à orientação do controle (horizontal ou vertical). <br/>                                                                                                                                 |
| [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md)     | Recupera o tamanho e a posição do retângulo delimitador para o canal de um TrackBar. (O canal é a área sobre a qual o controle deslizante se move. Ele contém o realce quando um intervalo é selecionado.) <br/>                                                                                                         |
| [**TBM \_ GETlines**](tbm-getlinesize.md)           | Recupera o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado das teclas de direção, como as chaves ou. As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante. <br/>                                         |
| [**TBM \_ GETNUMTICS**](tbm-getnumtics.md)             | Recupera o número de marcas de escala em um TrackBar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETpagesize**](tbm-getpagesize.md)           | Recupera o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado, como as chaves ou, ou entrada do mouse, como cliques no canal do TrackBar. As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante. <br/>   |
| [**TBM \_ GETPOS**](tbm-getpos.md)                     | Recupera a posição lógica atual do controle deslizante em um TrackBar. As posições lógicas são os valores inteiros no intervalo de TrackBar de mínimo para as posições do controle deslizante máximo. <br/>                                                                                                                       |
| [**TBM \_ GETPTICS**](tbm-getptics.md)                 | Recupera o endereço de uma matriz que contém as posições das marcas de escala para um TrackBar. <br/>                                                                                                                                                                                                        |
| [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md)           | Recupera a posição máxima do controle deslizante em um TrackBar. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md)           | Recupera a posição mínima do controle deslizante em um TrackBar. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETSELEND**](tbm-getselend.md)               | Recupera a posição final do intervalo de seleção atual em um TrackBar. <br/>                                                                                                                                                                                                                            |
| [**TBM \_ GETSELSTART**](tbm-getselstart.md)           | Recupera a posição inicial do intervalo de seleção atual em um TrackBar. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)     | Recupera o comprimento do controle deslizante em um TrackBar. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md)         | Recupera o tamanho e a posição do retângulo delimitador para o controle deslizante em um TrackBar. <br/>                                                                                                                                                                                                                |
| [**TBM \_ GETTIC**](tbm-gettic.md)                     | Recupera a posição lógica de uma marca de escala em um TrackBar. A posição lógica pode ser qualquer um dos valores inteiros na faixa de TrackBar de mínimo para máximo de posições do controle deslizante. <br/>                                                                                                                     |
| [**TBM \_ GETTICPOS**](tbm-getticpos.md)               | Recupera a posição física atual de uma marca de escala em um TrackBar.<br/>                                                                                                                                                                                                                                   |
| [**\_GETtooltips tbm**](tbm-gettooltips.md)           | Recupera o identificador para o controle de dica de ferramenta atribuído ao TrackBar, se houver. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md) | Recupera o sinalizador de formato de caractere Unicode para o controle. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ SETbuddy**](tbm-setbuddy.md)                 | Atribui uma janela como a janela Buddy para um controle TrackBar. As janelas TrackBar Buddy são exibidas automaticamente em um local em relação à orientação do controle (horizontal ou vertical). <br/>                                                                                                          |
| [**TBM \_ SETlinhasize**](tbm-setlinesize.md)           | Define o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado das teclas de direção, como as chaves ou. As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante. <br/>                                              |
| [**TBM de \_ páginas**](tbm-setpagesize.md)           | Define o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado, como as chaves ou, ou entrada do mouse, como cliques no canal do TrackBar. As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante. <br/>        |
| [**TBM \_ SETPOS**](tbm-setpos.md)                     | Define a posição lógica atual do controle deslizante em um TrackBar. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETPOSNOTIFY**](tbm-setposnotify.md)         | Define a posição lógica atual do controle deslizante em um TrackBar. <br/>                                                                                                                                                                                                                                         |
| [**\_SETRANGE tbm**](tbm-setrange.md)                 | Define o intervalo de posições lógicas mínimas e máximas para o controle deslizante em um TrackBar. <br/>                                                                                                                                                                                                                  |
| [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)           | Define a posição lógica máxima para o controle deslizante em um TrackBar. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)           | Define a posição lógica mínima para o controle deslizante em um TrackBar. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETSEL**](tbm-setsel.md)                     | Define as posições inicial e final para o intervalo de seleção disponível em um TrackBar. <br/>                                                                                                                                                                                                                |
| [**TBM \_ SETSELEND**](tbm-setselend.md)               | Define a posição lógica final do intervalo de seleção atual em um TrackBar. Essa mensagem será ignorada se o TrackBar não tiver o [**estilo \_ ENABLESELRANGE TBS**](trackbar-control-styles.md) . <br/>                                                                              |
| [**TBM \_ SETSELSTART**](tbm-setselstart.md)           | Define a posição lógica inicial do intervalo de seleção atual em um TrackBar. Essa mensagem será ignorada se o TrackBar não tiver o [**estilo \_ ENABLESELRANGE TBS**](trackbar-control-styles.md) . <br/>                                                                            |
| [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md)     | Define o comprimento do controle deslizante em um TrackBar. Essa mensagem será ignorada se o TrackBar não tiver o [**estilo \_ Cadeia TBS**](trackbar-control-styles.md) . <br/>                                                                                                                      |
| [**TBM \_**](tbm-settic.md)                     | Define uma marca de escala em um TrackBar na posição lógica especificada. <br/>                                                                                                                                                                                                                                      |
| [**TBM \_ SETTICFREQ**](tbm-setticfreq.md)             | Define a frequência de intervalo para marcas de escala em um TrackBar. Por exemplo, se a frequência for definida como dois, uma marca de escala será exibida para todos os outros incrementos no intervalo do TrackBar. A configuração padrão para a frequência é uma; ou seja, cada incremento no intervalo é associado a uma marca de escala. <br/> |
| [**TBM \_ SETTIPSIDE**](tbm-settipside.md)             | Posiciona um controle ToolTip usado por um controle TrackBar. Os controles TrackBar que usam o estilo de [**\_ dicas de ferramenta TBS**](trackbar-control-styles.md) exibem dicas de ferramenta. <br/>                                                                                                                           |
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



 

 

 





