---
title: Barra de Status
description: Esta seção contém informações sobre os elementos de programação usados com controles de barra de status.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1be3ea518b63118fc80b02b382943c40ba2fd13b15713488b351b5d6cc827e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696486"
---
# <a name="status-bar"></a>Barra de Status

Esta seção contém informações sobre os elementos de programação usados com controles de barra de status.

### <a name="overviews"></a>Visões gerais



| Tópico                          | Sumário                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barras de status](status-bars.md) | Uma *barra de status* é uma janela horizontal na parte inferior de uma janela pai na qual um aplicativo pode exibir vários tipos de informações de status.<br/> |



 

### <a name="functions"></a>Funções



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Sumário</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></td>
<td>Cria uma janela de status, que normalmente é usada para exibir o status de um aplicativo. A janela geralmente aparece na parte inferior da janela pai e contém o texto especificado.
<blockquote>
[!Note]<br />
Essa função está obsoleta. Em vez disso, use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></td>
<td>A função <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> desenha o texto especificado no estilo de uma janela de status com bordas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></td>
<td>Processa <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> e <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> mensagens e exibe o texto de ajuda sobre o menu atual na janela de status especificada.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Mensagens



| Tópico                                               | Sumário                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**$ \_ Borders SB**](sb-getborders.md)             | Recupera as larguras atuais das bordas horizontais e verticais de uma janela de status. <br/>                                                                                                  |
| [**SB \_ GETicon**](sb-geticon.md)                   | Recupera o ícone de uma parte em uma barra de status. <br/>                                                                                                                                           |
| [**@ @ \_ Parts SB**](sb-getparts.md)                 | Recupera uma contagem das partes em uma janela de status. A mensagem também recupera a coordenada da borda direita do número especificado de partes. <br/>                                         |
| [**SB \_ GETrect**](sb-getrect.md)                   | Recupera o retângulo delimitador de uma parte em uma janela de status. <br/>                                                                                                                           |
| [**SB \_ GETtext**](sb-gettext.md)                   | A mensagem de [**\_ gettext do SB**](sb-gettext.md) recupera o texto da parte especificada de uma janela de status. <br/>                                                                             |
| [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md)       | A mensagem [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) recupera o comprimento, em caracteres, do texto da parte especificada de uma janela de status. <br/>                                   |
| [**SB \_ GETTIPTEXT**](sb-gettiptext.md)             | Recupera o texto da dica de ferramenta de uma parte em uma barra de status. A barra de status deve ser criada com o estilo de [**\_ dicas de ferramenta SBT**](status-bar-styles.md) para habilitar dicas de ferramenta. <br/>         |
| [**SB \_ GETUNICODEFORMAT**](sb-getunicodeformat.md) | Recupera o sinalizador de formato de caractere Unicode para o controle. <br/>                                                                                                                             |
| [**SB \_ ISsimples**](sb-issimple.md)                 | Verifica um controle de barra de status para determinar se ele está no modo simples. <br/>                                                                                                                        |
| [**SB \_ SETBKCOLOR**](sb-setbkcolor.md)             | Define a cor do plano de fundo em uma barra de status. <br/>                                                                                                                                               |
| [**ÍCONE da SB \_**](sb-seticon.md)                   | Define o ícone de uma parte em uma barra de status. <br/>                                                                                                                                                |
| [**SB \_ SETMINHEIGHT**](sb-setminheight.md)         | Define a altura mínima da área de desenho de uma janela de status. <br/>                                                                                                                               |
| [**conpartes da SB \_**](sb-setparts.md)                 | Define o número de partes em uma janela de status e a coordenada da borda direita de cada parte. <br/>                                                                                           |
| [**SB \_ SETtext**](sb-settext.md)                   | A mensagem do SB \_ SetText define o texto na parte especificada de uma janela de status.<br/>                                                                                                           |
| [**SB \_ SETTIPTEXT**](sb-settiptext.md)             | Define o texto da dica de ferramenta para uma parte em uma barra de status. A barra de status deve ter sido criada com o estilo de [**\_ dicas de ferramenta SBT**](status-bar-styles.md) para habilitar dicas de ferramenta.<br/>        |
| [**SB \_ SETUNICODEFORMAT**](sb-setunicodeformat.md) | Define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle. <br/> |
| [**SB \_ simples**](sb-simple.md)                     | Especifica se uma janela de status exibe texto simples ou exibe todas as partes da janela definidas por uma mensagem do [**SB \_ SetParts**](sb-setparts.md) anterior. <br/>                                       |



 

### <a name="notifications"></a>Notificações



| Tópico                                                 | Sumário                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Clique de nm (barra de status)](nm-click-status-bar.md)     | Notifica a janela pai de um controle de barra de status que o usuário clicou com o botão esquerdo do mouse dentro do controle. [Nm \_ CLIQUE (barra de status)](nm-click-status-bar.md) é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>              |
| [NM \_ DBLCLK (barra de status)](nm-dblclk-status-bar.md)   | Notifica a janela pai de um controle de barra de status que o usuário clicou duas vezes com o botão esquerdo do mouse dentro do controle. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .<br/>                                       |
| [NM \_ RCLICK (barra de status)](nm-rclick-status-bar.md)   | Notifica a janela pai de um controle de barra de status que o usuário clicou com o botão direito do mouse dentro do controle. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .<br/>                                             |
| [NM \_ RDBLCLK (barra de status)](nm-rdblclk-status-bar.md) | Notifica as janelas pai de um controle de barra de status que o usuário clicou duas vezes com o botão direito do mouse dentro do controle. [Nm \_ RDBLCLK (barra de status)](nm-rdblclk-status-bar.md) é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/> |
| [SBN \_ SIMPLEMODECHANGE](sbn-simplemodechange.md)     | Enviado por um controle de barra de status quando o modo simples é alterado devido a uma mensagem [**\_ simples do SB**](sb-simple.md) . Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) . <br/>                                                        |



 

### <a name="constants"></a>Constantes



| Tópico                                      | Sumário                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Estilos da barra de status](status-bar-styles.md) | Esta seção lista os estilos, além dos estilos de janela padrão, suportados pelos controles de *barra de status* . <br/> |



 

 

