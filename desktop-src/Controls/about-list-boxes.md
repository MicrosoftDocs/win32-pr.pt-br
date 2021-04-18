---
title: Sobre as caixas de listagem
description: Esta seção descreve os recursos da caixa de listagem.
ms.assetid: 359bb363-5b97-4e0c-bdc4-bfa6a6504a76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674712226a79960e44ab99ed8e59c88b27984efb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454367"
---
# <a name="about-list-boxes"></a>Sobre as caixas de listagem

Um controle de caixa de listagem contém uma lista simples da qual o usuário geralmente pode selecionar um ou mais itens. As caixas de listagem fornecem flexibilidade limitada em comparação com os controles de [exibição de lista](list-view-control-reference.md) .

Os itens da caixa de listagem podem ser representados por cadeias de caracteres de texto, bitmaps ou ambos. Se a caixa de listagem não for grande o suficiente para exibir todos os itens da caixa de listagem de uma só vez, a caixa de listagem fornecerá uma barra de rolagem. O usuário rola pelos itens da caixa de listagem e aplica ou remove o status da seleção, conforme necessário. A seleção de um item da caixa de listagem altera sua aparência visual, geralmente alterando o texto e as cores do plano de fundo para aqueles especificados pelas métricas relevantes do sistema operacional. Quando o usuário seleciona ou anula a seleção de um item, o sistema envia uma mensagem de notificação para a janela pai da caixa de listagem.

Para um aplicativo ANSI, o sistema converte o texto em uma caixa de listagem para Unicode usando a página de código do **CP \_ ACP** . Isso pode causar problemas. Por exemplo, caracteres romanos acentuados em uma caixa de listagem não-Unicode no Windows, a versão japonesa será distorcido. Para corrigir isso, compile o aplicativo como Unicode ou use uma caixa de listagem desenhada pelo proprietário.

Esta seção aborda os seguintes tópicos:

-   [Criando uma caixa de listagem](#creating-a-list-box)
-   [Tipos e estilos de caixa de listagem](#list-box-types-and-styles)
-   [Funções da caixa de listagem](#list-box-functions)
-   [Mensagens de notificação de caixas de listagem](#notification-messages-from-list-boxes)
-   [Mensagens para caixas de listagem](#notification-messages-from-list-boxes)
-   [Processamento de mensagem de janela padrão](#default-window-message-processing)
-   [Caixas de listagem desenhadas pelo proprietário](#owner-drawn-list-boxes)
-   [Arrastar caixas de listagem](#drag-list-boxes)
    -   [Criando caixas de listagem de arrastar](#creating-drag-list-boxes)
    -   [Arrastar mensagens da caixa de listagem](#drag-list-box-messages)
    -   [Arrastar códigos de notificação da caixa de listagem](#drag-list-box-notification-codes)

## <a name="creating-a-list-box"></a>Criando uma caixa de listagem

A maneira mais fácil de criar uma caixa de listagem em uma caixa de diálogo é arrastá-la da Toolbox no Microsoft Visual Studio para o recurso da caixa de diálogo. Para criar uma caixa de listagem dinamicamente ou para criar uma caixa de listagem em uma janela diferente de uma caixa de diálogo, use a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe da janela [**\_ ListBox do WC**](common-control-window-classes.md) e os [estilos de caixa de listagem](list-box-styles.md)apropriados.

## <a name="list-box-types-and-styles"></a>Tipos e estilos de caixa de listagem

Há dois tipos de caixas de listagem: seleção única (o padrão) e seleção múltipla. Em uma caixa de listagem de seleção única, o usuário pode selecionar apenas um item por vez. Em uma caixa de listagem de seleção múltipla, o usuário pode selecionar mais de um item por vez. Para criar uma caixa de listagem de seleção múltipla, especifique o estilo [**lbs \_ MULTIPLESEL**](list-box-styles.md) ou [**lbs \_ EXTENDEDSEL**](list-box-styles.md) .

A aparência e a operação de uma caixa de listagem são controladas por estilos de [caixa de listagem](list-box-styles.md) e estilos de janela. Esses estilos indicam se a lista está classificada, organizada em várias colunas, desenhada pelo aplicativo e assim por diante. As dimensões e os estilos de uma caixa de listagem normalmente são definidos em um modelo de caixa de diálogo que é incluído nos recursos de um aplicativo.

> [!Note]  
> Para usar estilos visuais com esses controles, um aplicativo deve incluir um manifesto e deve chamar [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) no início do programa. Para obter informações sobre estilos visuais, consulte [estilos visuais](themes-overview.md). Para obter informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="list-box-functions"></a>Funções da caixa de listagem

A função [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) substitui o conteúdo de uma caixa de listagem pelos nomes de unidades, diretórios e arquivos que correspondem a um conjunto especificado de critérios. A função [**DlgDirSelectEx**](/windows/desktop/api/Winuser/nf-winuser-dlgdirselectexa) recupera a seleção atual em uma caixa de listagem que é inicializada pelo **DlgDirList**. Essas funções possibilitam que o usuário selecione uma unidade, um diretório ou um arquivo de uma caixa de listagem sem digitar o local e o nome do arquivo.

Além disso, a função [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo) retorna o número de itens por coluna em uma caixa de listagem especificada.

## <a name="notification-messages-from-list-boxes"></a>Mensagens de notificação de caixas de listagem

Quando um evento ocorre em uma caixa de listagem, a caixa de listagem envia um código de notificação, na forma de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) , para o procedimento da caixa de diálogo da janela do proprietário. Os códigos de notificação da caixa de listagem são enviados quando um usuário seleciona, clica duas vezes ou cancela um item da caixa de listagem; Quando a caixa de listagem recebe ou perde o foco do teclado; e quando o sistema não pode alocar memória suficiente para uma solicitação de caixa de listagem. Uma mensagem de **\_ comando do WM** contém o identificador da caixa de listagem na palavra de ordem inferior do parâmetro *wParam* e o código de notificação na palavra de ordem superior. O parâmetro *lParam* contém o identificador da janela de controle.

Um procedimento de caixa de diálogo não é necessário para processar essas mensagens; o procedimento de janela padrão processa-os.

Um aplicativo deve monitorar e processar os seguintes códigos de notificação da caixa de listagem.



| Código de notificação                   | Descrição                                                      |
|-------------------------------------|------------------------------------------------------------------|
| [LBN \_ DBLCLK](lbn-dblclk.md)       | O usuário clica duas vezes em um item na caixa de listagem.                  |
| [LBN \_ ERRSPACE](lbn-errspace.md)   | A caixa de listagem não pode alocar memória suficiente para atender a uma solicitação. |
| [LBN \_ KILLFOCUS](lbn-killfocus.md) | A caixa de listagem perde o foco do teclado.                           |
| [LBN \_ SELCANCEL](lbn-selcancel.md) | O usuário cancela a seleção de um item na caixa de listagem.       |
| [LBN \_ SELCHANGE](lbn-selchange.md) | A seleção em uma caixa de listagem está prestes a ser alterada.                  |
| [LBN \_ SETFOCUS](lbn-setfocus.md)   | A caixa de listagem recebe o foco do teclado.                        |



 

## <a name="messages-to-list-boxes"></a>Mensagens para caixas de listagem

Um procedimento de caixa de diálogo pode enviar mensagens para uma caixa de listagem para adicionar, excluir, examinar e alterar itens da caixa de listagem. Por exemplo, um procedimento de caixa de diálogo poderia enviar uma mensagem de [**\_ AddString de lb**](lb-addstring.md) para uma caixa de listagem para adicionar um item e uma mensagem [**\_ GETSEL de lb**](lb-getsel.md) para determinar se o item está selecionado. Outras mensagens definem e recuperam informações sobre o tamanho, a aparência e o comportamento da caixa de listagem. Por exemplo, a [**mensagem \_ SETHORIZONTALEXTENT de lb**](lb-sethorizontalextent.md) define a largura rolável de uma caixa de listagem. Um procedimento de caixa de diálogo pode enviar qualquer mensagem a uma caixa de listagem usando a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ou [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) .

Um item de caixa de listagem geralmente é referenciado por seu *índice*, um inteiro que representa a posição do item na caixa de listagem. O índice do primeiro item em uma caixa de listagem é 0, o índice do segundo item é 1 e assim por diante.

A tabela a seguir descreve como o procedimento de caixa de listagem predefinido responde às mensagens da caixa de listagem.



| Mensagem                                                   | Resposta                                                                                                                                                                                                                         |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**o \_ ADDfile do lb**](lb-addfile.md)                         | Insere um arquivo em uma caixa de listagem de diretório que é preenchida pela função [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) e recupera o índice da caixa de listagem do item inserido.                                                                  |
| [**seqüência de caracteres de LB \_**](lb-addstring.md)                     | Adiciona uma cadeia de caracteres a uma caixa de listagem e retorna seu índice.                                                                                                                                                                               |
| [**LB \_ DeleteString**](lb-deletestring.md)               | Remove uma cadeia de caracteres de uma caixa de listagem e retorna o número de cadeias de caracteres que permanecem na lista.                                                                                                                                      |
| [**Dir. de LB \_**](lb-dir.md)                                 | Adiciona uma lista de nomes de arquivo a uma caixa de listagem e retorna o índice do último nome de arquivo adicionado.                                                                                                                                       |
| [**Localizar LBstring \_**](lb-findstring.md)                   | Retorna o índice da primeira cadeia de caracteres na caixa de listagem que começa com uma cadeia de caracteres especificada.                                                                                                                                       |
| [**\_FINDSTRINGEXACT lb**](lb-findstringexact.md)         | Retorna o índice da cadeia de caracteres na caixa de listagem que é igual a uma cadeia de caracteres especificada.                                                                                                                                             |
| [**\_GETANCHORINDEX lb**](lb-getanchorindex.md)           | Retorna o índice do item que o mouse selecionou pela última vez.                                                                                                                                                                      |
| [**\_GETCARETINDEX lb**](lb-getcaretindex.md)             | Retorna o índice do item que tem o retângulo de foco.                                                                                                                                                                      |
| [**GetCount de LB \_**](lb-getcount.md)                       | Retorna o número de itens na caixa de listagem.                                                                                                                                                                                     |
| [**KG \_ de lb**](lb-getcursel.md)                     | Retorna o índice do item selecionado no momento.                                                                                                                                                                                |
| [**\_GETHORIZONTALEXTENT lb**](lb-gethorizontalextent.md) | Retorna a largura rolável, em pixels, de uma caixa de listagem.                                                                                                                                                                          |
| [**\_GETITEMDATA lb**](lb-getitemdata.md)                 | Retorna o valor associado ao item especificado.                                                                                                                                                                    |
| [**\_GETITEMHEIGHT lb**](lb-getitemheight.md)             | Retorna a altura, em pixels, de um item em uma caixa de listagem.                                                                                                                                                                         |
| [**\_GETITEMRECT lb**](lb-getitemrect.md)                 | Recupera as coordenadas do cliente do item da caixa de listagem especificado.                                                                                                                                                                 |
| [**\_local lb**](lb-getlocale.md)                     | Recupera a localidade da caixa de listagem. A palavra de ordem superior contém o código de país/região e a palavra de ordem inferior contém o identificador de idioma.                                                                              |
| [**\_GETSEL lb**](lb-getsel.md)                           | Retorna o estado de seleção de um item da caixa de listagem.                                                                                                                                                                                  |
| [**\_GETSELCOUNT lb**](lb-getselcount.md)                 | Retorna o número de itens selecionados em uma caixa de listagem de seleção múltipla.                                                                                                                                                           |
| [**\_GETSELITEMS lb**](lb-getselitems.md)                 | Cria uma matriz dos índices de todos os itens selecionados em uma caixa de listagem de seleção múltipla e retorna o número total de itens selecionados.                                                                                           |
| [**LB \_ GETtext**](lb-gettext.md)                         | Recupera a cadeia de caracteres associada a um item especificado e o comprimento da cadeia de caracteres.                                                                                                                                              |
| [**\_GETTEXTLEN lb**](lb-gettextlen.md)                   | Retorna o comprimento, em caracteres, da cadeia de caracteres associada a um item especificado.                                                                                                                                               |
| [**\_GETTOPINDEX lb**](lb-gettopindex.md)                 | Retorna o índice do primeiro item visível em uma caixa de listagem.                                                                                                                                                                       |
| [**\_INITSTORAGE lb**](lb-initstorage.md)                 | Aloca memória para o número especificado de itens e suas cadeias de caracteres associadas.                                                                                                                                                 |
| [**KG \_ InsertString**](lb-insertstring.md)               | Insere uma cadeia de caracteres em um índice especificado em uma caixa de listagem.                                                                                                                                                                             |
| [**\_ITEMFROMPOINT lb**](lb-itemfrompoint.md)             | Recupera o índice de base zero do item mais próximo ao ponto especificado em uma caixa de listagem.                                                                                                                                            |
| [**\_RESETCONTENT lb**](lb-resetcontent.md)               | Remove todos os itens de uma caixa de listagem.                                                                                                                                                                                               |
| [**seleção de LBstring \_**](lb-selectstring.md)               | Seleciona a primeira cadeia de caracteres localizada que corresponde a um prefixo especificado.                                                                                                                                                               |
| [**\_SELITEMRANGE lb**](lb-selitemrange.md)               | Seleciona um intervalo de itens especificado em uma caixa de listagem.                                                                                                                                                                                |
| [**\_SELITEMRANGEEX lb**](lb-selitemrangeex.md)           | Seleciona um intervalo de itens especificado se o índice do primeiro item no intervalo for menor que o índice do último item no intervalo. Cancela a seleção no intervalo se o índice do primeiro item for maior do que o último. |
| [**\_SETANCHORINDEX lb**](lb-setanchorindex.md)           | Define o item que o mouse selecionou pela última vez para um item especificado.                                                                                                                                                                  |
| [**\_SETCARETINDEX lb**](lb-setcaretindex.md)             | Define o retângulo de foco para um item de caixa de listagem especificado.                                                                                                                                                                           |
| [**\_SETCOLUMNWIDTH lb**](lb-setcolumnwidth.md)           | Define a largura, em pixels, de todas as colunas em uma caixa de listagem.                                                                                                                                                                         |
| [**NÚMERO de LB \_**](lb-setcount.md)                       | Define o número de itens em uma caixa de listagem.                                                                                                                                                                                          |
| [**LB- \_ REcursel**](lb-setcursel.md)                     | Seleciona um item da caixa de listagem especificado.                                                                                                                                                                                               |
| [**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md) | Define a largura rolável, em pixels, de uma caixa de listagem.                                                                                                                                                                             |
| [**\_SETITEMDATA lb**](lb-setitemdata.md)                 | Associa um valor a um item da caixa de listagem.                                                                                                                                                                                         |
| [**\_SETITEMHEIGHT lb**](lb-setitemheight.md)             | Define a altura, em pixels, de um item ou de itens em uma caixa de listagem.                                                                                                                                                                   |
| [**LB \_ SETlocale**](lb-setlocale.md)                     | Define a localidade de uma caixa de listagem e retorna o identificador de localidade anterior.                                                                                                                                                        |
| [**\_SETSEL lb**](lb-setsel.md)                           | Seleciona um item em uma caixa de listagem de seleção múltipla.                                                                                                                                                                                |
| [**LB \_ SETtabstops**](lb-settabstops.md)                 | Define as paradas de tabulação para aquelas especificadas em uma matriz especificada.                                                                                                                                                                      |
| [**\_SETTOPINDEX lb**](lb-settopindex.md)                 | Rola a caixa de listagem para que o item especificado esteja na parte superior do intervalo visível.                                                                                                                                                   |



 

## <a name="default-window-message-processing"></a>Processamento de mensagem de janela padrão

O procedimento de janela para a classe de janela da caixa de listagem predefinida executa o processamento padrão para todas as mensagens que a caixa de listagem não processa. Quando o procedimento da caixa de listagem retorna **false** para uma mensagem, o procedimento de janela predefinido verifica a mensagem e executa as ações padrão, conforme mostrado na tabela a seguir.



| Mensagem                                            | Ação padrão                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**caractere do WM \_**](/windows/desktop/inputdev/wm-char)                   | Move a seleção para o primeiro item que começa com o caractere que o usuário digitou. Se a caixa de listagem tiver o estilo L [**BS \_ OWNERDRAW**](button-styles.md) , nenhuma ação ocorrerá. Vários caracteres que são digitados em um intervalo curto são tratados como um grupo e o primeiro item que começa com essa série de caracteres é selecionado.<br/> |
| [**criação do WM \_**](/windows/desktop/winmsg/wm-create)                 | Cria uma caixa de listagem vazia.                                                                                                                                                                                                                                                                                                                                               |
| [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)               | Destrói a caixa de listagem e libera todos os recursos que ela usa.                                                                                                                                                                                                                                                                                                              |
|                                                    | Passa a mensagem para o procedimento da caixa de diálogo ou o processo da janela pai.                                                                                                                                                                                                                                                                                                 |
| [**habilitar o WM \_**](/windows/desktop/winmsg/wm-enable)                 | Se o controle estiver visível, invalida o retângulo para que as cadeias de caracteres possam ser pintadas cinza.                                                                                                                                                                                                                                                                                 |
| [**ERASEBKGND do WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)         | Apaga o plano de fundo de uma caixa de listagem. Se a caixa de listagem tiver o estilo L [**BS \_ OWNERDRAW**](button-styles.md) , o plano de fundo não será apagado.                                                                                                                                                                                                                   |
| [**GETDLGCODE do WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)         | Retorna DLGC \_ WANTARROWS \| DLGC \_ WANTCHARS, indicando que o procedimento de caixa de listagem padrão processa as teclas de direção e as mensagens do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) .                                                                                                                                                                                                      |
| [**WM \_ GETfont**](/windows/desktop/winmsg/wm-getfont)               | Retorna um identificador para a fonte atual da caixa de listagem.                                                                                                                                                                                                                                                                                                                   |
| [**HSCROLL do WM \_**](wm-hscroll.md)                  | Rola a caixa de listagem horizontalmente.                                                                                                                                                                                                                                                                                                                                       |
| [**o WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)             | Processa chaves virtuais para rolagem. A chave virtual é o índice do item para o qual mover o cursor. A seleção não é alterada.                                                                                                                                                                                                                                       |
| [**KILLFOCUS do WM \_**](/windows/desktop/inputdev/wm-killfocus)         | Desativa o cursor e destrói-o. Envia um código de notificação [lbn \_ KILLFOCUS](lbn-killfocus.md) para o proprietário da caixa de listagem.                                                                                                                                                                                                                                        |
| [**LBUTTONDBLCLK do WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk) | Controla o mouse na área do cliente da caixa de listagem. Isso permite que o usuário cancele uma seleção se o botão do mouse for liberado fora da área de lista do cliente da caixa de listagem.                                                                                                                                                                                                              |
| [**LBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-lbuttondown)     | Controla o mouse na área do cliente da caixa de listagem. Isso permite que o usuário cancele uma seleção se o botão do mouse for liberado fora da área de lista do cliente da caixa de listagem.                                                                                                                                                                                                              |
| [**LBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-lbuttonup)         | Controla o mouse na área do cliente da caixa de listagem. Isso permite que o usuário cancele uma seleção se o botão do mouse for liberado fora da área de lista do cliente da caixa de listagem.                                                                                                                                                                                                              |
| [**admousemove do WM \_**](/windows/desktop/inputdev/wm-mousemove)         | Controla o mouse na área do cliente da caixa de listagem. Isso permite que o usuário cancele uma seleção se o botão do mouse for liberado fora da área de lista do cliente da caixa de listagem.                                                                                                                                                                                                              |
| [**pintura do WM \_**](/windows/desktop/gdi/wm-paint)                      | Executa uma operação de pintura com uma subclasse usando o identificador da caixa de listagem para o contexto do dispositivo (DC).                                                                                                                                                                                                                                                                           |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | Ativa o cursor e envia um código de notificação [lbn \_ SETFOCUS](lbn-setfocus.md) para o proprietário da caixa de listagem.                                                                                                                                                                                                                                                        |
| [**WM \_ SETfont**](/windows/desktop/winmsg/wm-setfont)               | Define uma nova fonte para a caixa de listagem.                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ reemissão**](/windows/desktop/gdi/wm-setredraw)              | Define ou limpa o sinalizador de redesenho com base no valor de *wParam*.                                                                                                                                                                                                                                                                                                           |
| [**tamanho do WM \_**](/windows/desktop/winmsg/wm-size)                     | Redimensiona a caixa de listagem para um número integral de itens.                                                                                                                                                                                                                                                                                                                     |
| [**VSCROLL do WM \_**](wm-vscroll.md)                  | Rola a caixa de listagem verticalmente.                                                                                                                                                                                                                                                                                                                                         |



 

O procedimento de caixa de listagem predefinido passa todas as outras mensagens para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para o processamento padrão.

## <a name="owner-drawn-list-boxes"></a>Owner-Drawn caixas de listagem

Um aplicativo pode criar uma caixa de listagem de *desenho proprietário* para assumir a responsabilidade por itens de lista de pintura. A janela pai ou a caixa de diálogo de uma caixa de listagem desenhada pelo proprietário (seu *proprietário*) recebe mensagens do [**WM \_ DRAWITEM**](wm-drawitem.md) quando uma parte da caixa de listagem precisa ser pintada. Uma caixa de listagem desenhada pelo proprietário pode listar informações diferentes de, ou além de, cadeias de caracteres de texto.

O proprietário de uma caixa de listagem desenhada pelo proprietário deve processar a mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) . Essa mensagem é enviada sempre que uma parte da caixa de listagem deve ser redesenhada. O proprietário pode precisar processar outras mensagens, dependendo dos estilos especificados para a caixa de listagem.

Um aplicativo pode criar uma caixa de listagem desenhada pelo proprietário especificando o estilo de [**\_ OwnerDrawFixed**](list-box-styles.md) de lbs ou [**lbs \_ OwnerDrawVariable**](list-box-styles.md) . Se todos os itens da lista na caixa de listagem tiverem a mesma altura, como cadeias de caracteres ou ícones, um aplicativo poderá usar o estilo de **lb \_ OwnerDrawFixed** . Se os itens de lista forem de altura variável (por exemplo, bitmaps de tamanho diferente), um aplicativo poderá usar o estilo de **lbs \_ OwnerDrawVariable** .

O proprietário de uma caixa de listagem desenhada pelo proprietário pode processar uma mensagem do [**WM \_ MEASUREITEM**](wm-measureitem.md) para especificar as dimensões de itens de lista. Se o aplicativo criar a caixa de listagem usando o estilo [**lbs \_ OwnerDrawFixed**](list-box-styles.md) , o sistema enviará a mensagem do **WM \_ MEASUREITEM** apenas uma vez. As dimensões que são especificadas pelo proprietário são usadas para todos os itens de lista. Se o estilo de [**lbs \_ OwnerDrawVariable**](list-box-styles.md) for usado, o sistema enviará uma mensagem do **WM \_ MEASUREITEM** para cada item de lista que for adicionado à caixa de listagem. O proprietário pode determinar ou definir a altura de um item de lista a qualquer momento usando as mensagens de [**\_ SETITEMHEIGHT**](lb-setitemheight.md) lb [**\_ GETITEMHEIGHT**](lb-getitemheight.md) e lb, respectivamente.

Se as informações exibidas em uma caixa de listagem desenhada pelo proprietário incluírem texto, um aplicativo poderá controlar o texto de cada item de lista especificando o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) . As caixas de listagem com o estilo de [**\_ classificação lbs**](list-box-styles.md) são classificadas com base neste texto. Se uma caixa de listagem for classificada, mas não for do tipo **lbs \_ HASSTRINGS** , o proprietário deverá processar a mensagem do [**WM \_ COMPAREITEM**](wm-compareitem.md) .

Em uma caixa de listagem desenhada pelo proprietário, o proprietário deve manter o controle dos itens de lista que contêm informações que não sejam ou além do texto. Uma maneira conveniente de fazer isso é salvar o identificador nas informações como dados de item usando a mensagem [**\_ SETITEMDATA de lb**](lb-setitemdata.md) . Para liberar objetos de dados associados a itens em uma caixa de listagem, o proprietário pode processar a mensagem [**\_ DELETEITEM do WM**](wm-deleteitem.md) .

Para obter um exemplo de uma caixa de listagem desenhada pelo proprietário, consulte [como criar uma Owner-Drawn caixa de listagem](create-an-owner-drawn-list-box.md).

## <a name="drag-list-boxes"></a>Arrastar caixas de listagem

Uma caixa de listagem de arrastar é um tipo especial de caixa de listagem que permite ao usuário arrastar itens de uma posição para outra. Um aplicativo pode usar uma caixa de listagem de arrastar para exibir cadeias de caracteres em uma determinada sequência e permitir que o usuário altere a sequência arrastando os itens para a posição.

### <a name="creating-drag-list-boxes"></a>Criando caixas de listagem de arrastar

As caixas de listagem de arrastar têm os mesmos estilos de janela e processam as mesmas mensagens como caixas de listagem padrão. Para criar uma caixa de listagem de arrastar, primeiro crie uma caixa de listagem padrão e, em seguida, chame a função [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) . Para converter uma caixa de listagem em uma caixa de diálogo em uma caixa de listagem de arrastar, você pode chamar **MakeDragList** quando a mensagem do WM \_ INITDIALOG for processada.

### <a name="drag-list-box-messages"></a>Arrastar mensagens da caixa de listagem

Uma caixa de listagem de arrastar notifica a janela pai de eventos de arrastar enviando-o uma mensagem de arrastar lista. A janela pai deve processar a mensagem de arrastar lista.

A caixa de listagem de arrastar registra essa mensagem quando a função [**MakeDragList**](/windows/desktop/api/Commctrl/nf-commctrl-makedraglist) é chamada. Para recuperar o identificador de mensagem (valor numérico) da mensagem de arrastar lista, chame a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) e especifique o valor de DRAGLISTMSGSTRING.

O parâmetro *wParam* da mensagem de arrastar lista é o identificador de controle da caixa de listagem de arrastar. O parâmetro *lParam* é o endereço de uma estrutura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) , que contém o código de notificação para o evento de arrastar e outras informações. O valor de retorno da mensagem depende da notificação.

### <a name="drag-list-box-notification-codes"></a>Arrastar códigos de notificação da caixa de listagem

O código de notificação de lista de arrastar, que é identificado pelo membro **uNotification** da estrutura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) incluído com a mensagem de arrastar lista, pode ser [DL \_ BEGINDRAG](dl-begindrag.md), [DL \_](dl-dragging.md)drag, [DL \_ CANCELDRAG](dl-canceldrag.md)ou [DL \_ Descartado](dl-dropped.md).

O código de notificação [DL \_ BEGINDRAG](dl-begindrag.md) é enviado quando o cursor está em um item de lista e o usuário clica no botão esquerdo do mouse. A janela pai pode retornar **true** para iniciar a operação de arrastar ou **false** para não permitir a arrastar. Dessa forma, a janela pai pode habilitar o recurso de arrastar para alguns itens de lista e desabilitá-lo para outros. Você pode determinar qual item de lista está no local especificado usando a função [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) .

Se o recurso de arrastar estiver em vigor, o código de notificação de [ \_ arrastar da DL](dl-dragging.md) será enviado sempre que o mouse for movido, ou em intervalos regulares, se o mouse não estiver sendo movido. A janela pai deve primeiro determinar o item de lista sob o cursor usando [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) e, em seguida, desenhar o ícone de inserção usando a função [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) . Ao especificar **true** para o parâmetro *bAutoScroll* de **LBItemFromPt**, você pode fazer com que a caixa de listagem role por uma linha se o cursor estiver acima ou abaixo da sua área de cliente. O valor retornado para essa notificação especifica o tipo de cursor do mouse que a caixa de listagem de arrastar deve definir.

O código de notificação [DL \_ CANCELDRAG](dl-canceldrag.md) será enviado se o usuário cancelar uma operação de arrastar clicando com o botão direito do mouse ou pressionando a tecla ESC. O código de notificação [DL \_ removido](dl-dropped.md) será enviado se o usuário concluir uma operação de arrastar liberando o botão esquerdo do mouse, mesmo que o cursor não esteja sobre um item de lista. A caixa de listagem de arrastar libera a captura do mouse antes de enviar qualquer notificação. O valor de retorno dessas duas notificações é ignorado. Lista de arrastar

 

