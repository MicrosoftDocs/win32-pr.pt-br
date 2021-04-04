---
title: Caixa de listagem
description: Esta seção contém informações sobre os elementos de programação usados com caixas de listagem. Uma caixa de listagem é uma janela de controle que contém uma lista simples de itens dos quais o usuário pode escolher.
ms.assetid: vs|controls|~\controls\listboxes\listboxes.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fda5e6bb2d1d4c3c4f23e506900257c1b2ce64b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084920"
---
# <a name="list-box"></a>Caixa de listagem

Esta seção contém informações sobre os elementos de programação usados com caixas de listagem. Uma caixa de listagem é uma janela de controle que contém uma lista simples de itens dos quais o usuário pode escolher. Para obter listas mais complexas, use a [exibição de lista](list-view-control-reference.md) em vez disso.

### <a name="overviews"></a>Visões gerais



| Tópico                                    | Sumário                                                              |
|------------------------------------------|-----------------------------------------------------------------------|
| [Sobre as caixas de listagem](about-list-boxes.md) | Descreve os recursos da caixa de listagem.<br/>                               |
| [Usando caixas de listagem](using-list-boxes.md) | Explica como executar tarefas associadas a caixas de listagem. <br/> |



 

### <a name="functions"></a>Funções



| Tópico                                    | Sumário                                                                                                                |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)         | Substitui o conteúdo de uma caixa de listagem pelos nomes dos subdiretórios e arquivos em um diretório especificado.<br/> |
| [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) | Recupera a seleção atual de uma caixa de listagem de seleção única.<br/>                                            |
| [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert)         | Desenha o ícone inserir na janela pai da caixa de listagem de arrastar especificada. <br/>                                  |
| [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) | Recupera informações sobre a caixa de listagem especificada.<br/>                                                          |
| [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt)     | Recupera o índice do item no ponto especificado em uma caixa de listagem. <br/>                                       |
| [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist)     | Altera a caixa de listagem de seleção única especificada para uma caixa de listagem de arrastar. <br/>                                         |



 

### <a name="messages"></a>Mensagens



| Tópico                                                     | Sumário                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**o \_ ADDfile do lb**](lb-addfile.md)                         | Adiciona o nome de arquivo especificado a uma caixa de listagem que contém uma listagem de diretório. <br/>                                                                                                                                                                                     |
| [**seqüência de caracteres de LB \_**](lb-addstring.md)                     | Adiciona uma cadeia de caracteres a uma caixa de listagem. <br/>                                                                                                                                                                                                                                      |
| [**LB \_ DeleteString**](lb-deletestring.md)               | Exclui uma cadeia de caracteres em uma caixa de listagem. <br/>                                                                                                                                                                                                                                   |
| [**Dir. de LB \_**](lb-dir.md)                                 | Adiciona nomes à lista exibida por uma caixa de listagem. <br/>                                                                                                                                                                                                                   |
| [**Localizar LBstring \_**](lb-findstring.md)                   | Localiza a primeira cadeia de caracteres em uma caixa de listagem que começa com a cadeia de caracteres especificada. <br/>                                                                                                                                                                                       |
| [**\_FINDSTRINGEXACT lb**](lb-findstringexact.md)         | Localiza a primeira cadeia de caracteres da caixa de listagem que corresponde exatamente à cadeia de caracteres especificada, exceto que a pesquisa não diferencia maiúsculas de minúsculas. <br/>                                                                                                                                          |
| [**\_GETANCHORINDEX lb**](lb-getanchorindex.md)           | Obtém o índice do item de âncora que é o item do qual uma seleção múltipla é iniciada. <br/>                                                                                                                                                                       |
| [**\_GETCARETINDEX lb**](lb-getcaretindex.md)             | Recupera o índice do item que tem o retângulo de foco em uma caixa de listagem de seleção múltipla. O item pode ou não ser selecionado. <br/>                                                                                                                               |
| [**GetCount de LB \_**](lb-getcount.md)                       | Obtém o número de itens em uma caixa de listagem. <br/>                                                                                                                                                                                                                           |
| [**KG \_ de lb**](lb-getcursel.md)                     | Obtém o índice do item selecionado no momento, se houver, em uma caixa de listagem de seleção única. <br/>                                                                                                                                                                            |
| [**\_GETHORIZONTALEXTENT lb**](lb-gethorizontalextent.md) | Obtém a largura, em pixels, que uma caixa de listagem pode ser rolada horizontalmente (a largura rolável) se a caixa de listagem tiver uma barra de rolagem horizontal. <br/>                                                                                                                       |
| [**\_GETITEMDATA lb**](lb-getitemdata.md)                 | Obtém o valor definido pelo aplicativo associado ao item da caixa de listagem especificado. <br/>                                                                                                                                                                                   |
| [**\_GETITEMHEIGHT lb**](lb-getitemheight.md)             | Obtém a altura dos itens em uma caixa de listagem. <br/>                                                                                                                                                                                                                           |
| [**\_GETITEMRECT lb**](lb-getitemrect.md)                 | Obtém as dimensões do retângulo que vincula um item da caixa de listagem, como é exibido atualmente na caixa de listagem. <br/>                                                                                                                                                    |
| [**\_GETLISTBOXINFO lb**](lb-getlistboxinfo.md)           | Obtém o número de itens por coluna em uma caixa de listagem especificada. <br/>                                                                                                                                                                                                      |
| [**\_local lb**](lb-getlocale.md)                     | Obtém a localidade atual da caixa de listagem. <br/>                                                                                                                                                                                                                          |
| [**\_GETSEL lb**](lb-getsel.md)                           | Obtém o estado de seleção de um item. <br/>                                                                                                                                                                                                                              |
| [**\_GETSELCOUNT lb**](lb-getselcount.md)                 | Obtém o número total de itens selecionados em uma caixa de listagem de seleção múltipla. <br/>                                                                                                                                                                                         |
| [**\_GETSELITEMS lb**](lb-getselitems.md)                 | Preenche um buffer com uma matriz de inteiros que especificam os números de item dos itens selecionados em uma caixa de listagem de seleção múltipla. <br/>                                                                                                                                        |
| [**LB \_ GETtext**](lb-gettext.md)                         | Obtém uma cadeia de caracteres de uma caixa de listagem. <br/>                                                                                                                                                                                                                                    |
| [**\_GETTEXTLEN lb**](lb-gettextlen.md)                   | Obtém o comprimento de uma cadeia de caracteres em uma caixa de listagem. <br/>                                                                                                                                                                                                                        |
| [**\_GETTOPINDEX lb**](lb-gettopindex.md)                 | Obtém o índice do primeiro item visível em uma caixa de listagem. <br/>                                                                                                                                                                                                           |
| [**\_INITSTORAGE lb**](lb-initstorage.md)                 | Aloca memória para armazenar itens da caixa de listagem. Essa mensagem é usada antes que um aplicativo adicione um grande número de itens a uma caixa de listagem.<br/>                                                                                                                                |
| [**KG \_ InsertString**](lb-insertstring.md)               | Insere uma cadeia de caracteres ou dados de item em uma caixa de listagem. Ao contrário da mensagem de [**\_ AddString do lb**](lb-addstring.md) , a mensagem de [**\_ inserção de lb**](lb-insertstring.md) não faz com que uma lista com o estilo de [**\_ classificação lbs**](list-box-styles.md) seja classificada. <br/> |
| [**\_ITEMFROMPOINT lb**](lb-itemfrompoint.md)             | Obtém o índice de base zero do item mais próximo ao ponto especificado em uma caixa de listagem.<br/>                                                                                                                                                                                   |
| [**\_RESETCONTENT lb**](lb-resetcontent.md)               | Remove todos os itens de uma caixa de listagem. <br/>                                                                                                                                                                                                                                |
| [**seleção de LBstring \_**](lb-selectstring.md)               | Pesquisa uma caixa de listagem para um item que começa com os caracteres em uma cadeia de caracteres especificada. <br/>                                                                                                                                                                            |
| [**\_SELITEMRANGE lb**](lb-selitemrange.md)               | Seleciona ou anula a seleção de um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla. <br/>                                                                                                                                                                              |
| [**\_SELITEMRANGEEX lb**](lb-selitemrangeex.md)           | Seleciona um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla. <br/>                                                                                                                                                                                           |
| [**\_SETANCHORINDEX lb**](lb-setanchorindex.md)           | Define o item de âncora que é o item do qual uma seleção múltipla é iniciada. Uma seleção múltipla abrange todos os itens do item de âncora para o item de cursor.<br/>                                                                                                        |
| [**\_SETCARETINDEX lb**](lb-setcaretindex.md)             | Define o retângulo de foco para o item no índice especificado em uma caixa de listagem de seleção múltipla. Se o item não estiver visível, ele será rolado para a exibição. <br/>                                                                                                               |
| [**\_SETCOLUMNWIDTH lb**](lb-setcolumnwidth.md)           | Define a largura, em pixels, de todas as colunas em uma caixa de listagem de várias colunas. <br/>                                                                                                                                                                                          |
| [**NÚMERO de LB \_**](lb-setcount.md)                       | Define a contagem de itens em uma caixa de listagem criada com o estilo [**\_ NODATA de lbs**](list-box-styles.md) e não é criada com o estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) . <br/>                                                          |
| [**LB- \_ REcursel**](lb-setcursel.md)                     | Seleciona uma cadeia de caracteres e a rola para a exibição, se necessário. <br/>                                                                                                                                                                                                          |
| [**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md) | Define a largura, em pixels, pela qual uma caixa de listagem pode ser rolada horizontalmente (a largura rolável). <br/>                                                                                                                                                               |
| [**\_SETITEMDATA lb**](lb-setitemdata.md)                 | Define um valor que está associado ao item especificado em uma caixa de listagem. <br/>                                                                                                                                                                                            |
| [**\_SETITEMHEIGHT lb**](lb-setitemheight.md)             | Define a altura, em pixels, de itens em uma caixa de listagem. <br/>                                                                                                                                                                                                               |
| [**LB \_ SETlocale**](lb-setlocale.md)                     | Define a localidade atual da caixa de listagem. <br/>                                                                                                                                                                                                                          |
| [**\_SETSEL lb**](lb-setsel.md)                           | Seleciona uma cadeia de caracteres em uma caixa de listagem de seleção múltipla. <br/>                                                                                                                                                                                                                |
| [**LB \_ SETtabstops**](lb-settabstops.md)                 | Define as posições de parada de tabulação em uma caixa de listagem. <br/>                                                                                                                                                                                                                        |
| [**\_SETTOPINDEX lb**](lb-settopindex.md)                 | Garante que o item especificado em uma caixa de listagem esteja visível. <br/>                                                                                                                                                                                                         |



 

### <a name="notifications"></a>Notificações



| Tópico                                             | Sumário                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LBN \_ DBLCLK](lbn-dblclk.md)                     | Notifica o aplicativo de que o usuário clicou duas vezes em um item em uma caixa de listagem. <br/>                                                                                                                                                                                                                                         |
| [LBN \_ ERRSPACE](lbn-errspace.md)                 | Notifica o aplicativo que a caixa de listagem não pode alocar memória suficiente para atender a uma solicitação específica. <br/>                                                                                                                                                                                                                     |
| [LBN \_ KILLFOCUS](lbn-killfocus.md)               | Notifica o aplicativo que a caixa de listagem perdeu o foco do teclado. <br/>                                                                                                                                                                                                                                                  |
| [LBN \_ SELCANCEL](lbn-selcancel.md)               | Notifica o aplicativo que o usuário cancelou a seleção em uma caixa de listagem. <br/>                                                                                                                                                                                                                                         |
| [LBN \_ SELCHANGE](lbn-selchange.md)               | Notifica o aplicativo que a seleção em uma caixa de listagem foi alterada. <br/>                                                                                                                                                                                                                                                   |
| [LBN \_ SETFOCUS](lbn-setfocus.md)                 | Notifica o aplicativo que a caixa de listagem recebeu o foco do teclado. <br/>                                                                                                                                                                                                                                              |
| [**CHARTOITEM do WM \_**](wm-chartoitem.md)           | Enviado por uma caixa de listagem com o estilo de [**lbs \_ WANTKEYBOARDINPUT**](list-box-styles.md) para seu proprietário em resposta a uma mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) . <br/>                                                                                                                                        |
| [**CTLCOLORLISTBOX do WM \_**](wm-ctlcolorlistbox.md) | Enviado para a janela pai de uma caixa de listagem antes de o sistema desenhar a caixa de listagem. Ao responder a essa mensagem, a janela pai pode definir o texto e as cores de plano de fundo da caixa de listagem usando o identificador de contexto do dispositivo de exibição especificado. <br/>                                                                              |
| [**DELETEITEM do WM \_**](wm-deleteitem.md)           | Enviado ao proprietário de uma caixa de listagem ou caixa de combinação quando a caixa de listagem ou a caixa de combinação é destruída ou quando os itens são removidos pela mensagem [**lb \_ DeleteString**](lb-deletestring.md), [**lb \_ RESETCONTENT**](lb-resetcontent.md), [**CB \_ excluirstring**](cb-deletestring.md)ou [**CB \_ RESETCONTENT**](cb-resetcontent.md) . <br/> |
| [**VKEYTOITEM do WM \_**](wm-vkeytoitem.md)           | Enviado por uma caixa de listagem com o estilo de [**lbs \_ WANTKEYBOARDINPUT**](list-box-styles.md) para seu proprietário em resposta a uma mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) . <br/>                                                                                                                                  |
| [\_BEGINDRAG DL](dl-begindrag.md)                 | Notifica a janela pai da caixa de listagem de arrastar que o usuário clicou com o botão esquerdo do mouse em um item. <br/>                                                                                                                                                                                                                   |
| [\_CANCELDRAG DL](dl-canceldrag.md)               | Sinaliza que o usuário cancelou uma operação de arrastar clicando com o botão direito do mouse ou pressionando a tecla ESC. <br/>                                                                                                                                                                                                          |
| [arrastar para DL \_](dl-dragging.md)                   | Sinaliza que o usuário moveu o mouse ao arrastar um item. <br/>                                                                                                                                                                                                                                                        |
| [DL \_ removido](dl-dropped.md)                     | Sinaliza que o usuário concluiu uma operação de arrastar liberando o botão esquerdo do mouse. <br/>                                                                                                                                                                                                                                 |



 

### <a name="structures"></a>Estruturas



| Tópico                                        | Sumário                                                                                                                                                               |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) | Contém informações sobre um item de lista ou caixa de combinação excluído.<br/>                                                                                            |
| [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)         | Contém informações sobre um evento de arrastar. O ponteiro para [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) é passado como o parâmetro *lParam* da mensagem de arrastar lista. <br/> |



 

### <a name="constants"></a>Constantes



| Tópico                                  | Sumário                                                                |
|----------------------------------------|-------------------------------------------------------------------------|
| [Estilos de caixa de listagem](list-box-styles.md) | Descreve os estilos de janela que definem um controle de caixa de listagem. <br/> |



 

 

