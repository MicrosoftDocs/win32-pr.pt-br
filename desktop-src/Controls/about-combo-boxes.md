---
title: Sobre caixas de combinação
description: Esta seção aborda os diferentes tipos de caixas de combinação.
ms.assetid: 76410a87-aa0e-4da9-9e78-c80ac485e3cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344596a3c0aa772568956344aaddcc053b534993
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104570266"
---
# <a name="about-combo-boxes"></a>Sobre caixas de combinação

Uma caixa de combinação combina uma caixa de edição ou texto estático e uma lista.

Este tópico inclui as seções a seguir.

-   [Tipos e estilos de caixa de combinação](#combo-box-types-and-styles)
-   [Lista de caixas de combinação](#combo-box-list)
    -   [Seleção atual](#current-selection)
    -   [Listas suspensas](#drop-down-lists)
    -   [Listar Conteúdo](#list-contents)
-   [Editar campos de seleção de controle](#edit-control-selection-fields)
-   [Caixas de combinação desenhadas pelo proprietário](#owner-drawn-combo-boxes)
-   [Caixas de combinação de subclasse](#subclassed-combo-boxes)

## <a name="combo-box-types-and-styles"></a>Tipos e estilos de caixa de combinação

Uma caixa de combinação consiste em uma lista e um campo de seleção. A lista apresenta as opções que um usuário pode selecionar e o campo seleção exibe a seleção atual. Se o campo de seleção for um controle de edição, o usuário poderá inserir informações não disponíveis na lista; caso contrário, o usuário só poderá selecionar itens na lista.

A biblioteca de controles comuns inclui três estilos principais de caixa de combinação, conforme mostrado na tabela a seguir.



| Tipo de caixa de combinação             | Constante de estilo                                                 | Descrição                                                                                  |
|----------------------------|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Simples                     | [**CBS \_ simples**](combo-box-styles.md)             | Exibe a lista em todos os momentos e mostra o item selecionado em um controle de edição.              |
| Lista suspensa                  | [**\_lista suspensa CBS**](combo-box-styles.md)         | Exibe a lista quando o ícone é clicado e mostra o item selecionado em um controle de edição.  |
| Lista suspensa (lista suspensa) | [**DROPDOWNLIST do CBS \_**](combo-box-styles.md) | Exibe a lista quando o ícone é clicado e mostra o item selecionado em um controle estático. |



 

As capturas de tela a seguir mostram os três tipos de caixa de combinação que podem aparecer no Windows Vista. Na primeira captura de tela, o usuário selecionou um item na caixa de combinação simples. O usuário também pode digitar um novo valor na caixa de edição deste controle. A lista foi dimensionada no editor de recursos Microsoft Visual Studio e só é grande o suficiente para acomodar dois itens.

![captura de tela mostrando um item selecionado em uma caixa de combinação simples](images/simplecombo.png)

Na segunda captura de tela, o usuário digitou um novo texto no controle de edição da caixa de combinação suspensa. O usuário também pode ter selecionado um item existente. A caixa de listagem se expande para acomodar o máximo de itens possível.

![captura de tela mostrando texto digitado em uma caixa de combinação suspensa](images/dropdown.png)

Na terceira captura de tela, o usuário abriu a caixa de combinação lista suspensa. A caixa de listagem se expande para acomodar o máximo de itens possível. O usuário não pode inserir um novo texto.

![captura de tela mostrando um item selecionado em uma caixa de combinação da lista suspensa](images/droplist.png)

Também há vários estilos de caixa de combinação que definem propriedades específicas. Os estilos de caixa de combinação definem propriedades específicas de uma caixa de combinação. Você pode combinar estilos; no entanto, alguns estilos se aplicam apenas a determinados tipos de caixa de combinação. Para uma tabela de estilos de caixa de combinação, consulte [estilos de caixa de combinação](combo-box-styles.md).

> [!Note]  
> Para usar estilos visuais com caixas de combinação, um aplicativo deve incluir um manifesto e deve chamar [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) no início do programa. Para obter informações sobre estilos visuais, consulte [estilos visuais](themes-overview.md). Para obter informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="combo-box-list"></a>Lista de caixas de combinação

A lista é a parte de uma caixa de combinação que exibe os itens que um usuário pode selecionar. Normalmente, um aplicativo Inicializa o conteúdo da lista quando ele cria uma caixa de combinação. Qualquer item de lista selecionado pelo usuário é a *seleção atual*. Não é possível selecionar vários itens. Nas caixas de combinação simples e suspensas, o usuário pode digitar o campo de seleção em vez de selecionar um item de lista. Nesses casos, não há nenhuma seleção atual, e é responsabilidade do aplicativo Adicionar o item à lista e torná-lo a seleção atual, se for apropriado para isso.

Esta seção aborda os seguintes tópicos:

-   [Seleção atual](#current-selection)
-   [Listas suspensas](#drop-down-lists)
-   [Listar Conteúdo](#list-contents)

### <a name="current-selection"></a>Seleção atual

A seleção atual é um item de lista que o usuário selecionou; o texto selecionado é exibido no campo seleção da caixa de combinação. No entanto, no caso de uma caixa de combinação simples ou de uma caixa de combinação suspensa, a seleção atual é apenas uma forma de entrada de usuário possível em uma caixa de combinação. O usuário também pode digitar texto no campo de seleção.

A seleção atual é identificada pelo índice de base zero do item de lista selecionado. Um aplicativo pode definir e recuperá-lo a qualquer momento. O procedimento da janela pai ou da caixa de diálogo recebe uma notificação quando o usuário altera a seleção atual para uma caixa de combinação. A janela pai ou a caixa de diálogo não é notificada quando o aplicativo altera a seleção.

Quando uma caixa de combinação é criada, não há nenhuma seleção atual. Isso também é verdadeiro para uma caixa de combinação simples ou suspensa, se o usuário tiver editado o conteúdo do campo de seleção. Para definir a seleção atual, um aplicativo envia a mensagem do [**CB \_ setcurse**](cb-setcursel.md) para a caixa de combinação. Um aplicativo também pode usar a [**mensagem \_ SelectString de CB**](cb-selectstring.md) para definir a seleção atual como um item de lista cuja cadeia de caracteres começa com uma cadeia de caracteres especificada. Para determinar a seleção atual, um aplicativo envia a mensagem de [**\_ iscursão CB**](cb-getcursel.md) para a caixa de combinação. Se não houver nenhuma seleção atual, essa mensagem retornará um \_ erro CB.

Quando o usuário altera a seleção atual em uma caixa de combinação, a janela pai ou o procedimento de caixa de diálogo recebe uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) com o código de notificação [CBN \_ SELCHANGE](cbn-selchange.md) na palavra de ordem superior do parâmetro *wParam* . Esse código de notificação não é enviado quando a seleção atual é definida usando a mensagem [**\_ setcurseaction**](cb-setcursel.md) .

Uma caixa de combinação suspensa ou uma caixa de listagem suspensa envia o código de notificação [CBN \_ closeup](cbn-closeup.md) para a janela pai ou o procedimento da caixa de diálogo quando a lista suspensa é fechada. Se o usuário alterou a seleção atual, a caixa de combinação também envia o código de notificação [CBN \_ SELCHANGE](cbn-selchange.md) quando a lista suspensa é fechada. Para executar um processo específico cada vez que o usuário seleciona um item de lista, você pode manipular o \_ código de notificação CBN SELCHANGE ou CBN \_ closeup. Normalmente, você esperaria pelo código de \_ notificação CBN closeup antes de processar uma alteração na seleção atual. Isso pode ser particularmente importante se uma quantidade significativa de processamento for necessária.

Um aplicativo também pode processar os códigos de notificação [CBN \_ SELENDOK](cbn-selendok.md) e [CBN \_ SELENDCANCEL](cbn-selendcancel.md) . O sistema envia CBN \_ SELENDOK quando o usuário seleciona um item de lista ou seleciona um item e fecha a lista. Isso indica que o usuário foi concluído e que a seleção deve ser processada. CBN \_ SELENDCANCEL é enviado quando o usuário seleciona um item, mas seleciona outro controle, pressiona ESC enquanto a lista suspensa está aberta ou fecha a caixa de diálogo. Isso indica que a seleção do usuário deve ser ignorada. CBN \_ SELENDOK é enviado antes de cada mensagem [CBN \_ SELCHANGE](cbn-selchange.md) .

Em uma caixa de combinação simples, o sistema envia o código de notificação [CBN \_ DBLCLK](cbn-dblclk.md) quando o usuário clica duas vezes em um item de lista. Em uma caixa de combinação suspensa ou lista suspensa, um único clique oculta a lista, portanto, não é possível clicar duas vezes em um item.

### <a name="drop-down-lists"></a>Listas suspensas

Determinadas notificações e mensagens se aplicam somente a caixas de combinação que contêm listas suspensas. Quando uma lista suspensa é aberta ou fechada, a janela pai de uma caixa de combinação recebe uma notificação na forma de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) . Se a lista estiver sendo aberta, a palavra de ordem superior de *wParam* será [CBN \_ DROPDOWN](cbn-dropdown.md). Se a lista estiver sendo fechada, ela será [CBN \_ closeup](cbn-closeup.md).

Um aplicativo pode abrir a lista de uma caixa de combinação suspensa ou caixa de listagem suspensa usando a mensagem de lista [**suspensa \_ CB**](cb-showdropdown.md) . Ele pode determinar se a lista está aberta usando a mensagem [**CB \_ getremovestate**](cb-getdroppedstate.md) e pode determinar as coordenadas de uma lista suspensa usando a mensagem [**CB \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md) . Um aplicativo também pode aumentar a largura de uma lista suspensa usando a mensagem [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md) .

### <a name="list-contents"></a>Listar Conteúdo

Quando um aplicativo cria uma caixa de combinação, ele normalmente Inicializa a caixa de combinação adicionando um ou mais itens à lista. Posteriormente, um aplicativo pode adicionar ou excluir itens de lista, reinicializar a lista ou recuperar informações de item dela.

Um aplicativo adiciona itens de lista a uma caixa de combinação enviando a mensagem de [**\_ AddString CB**](cb-addstring.md) para ele. O item especificado é adicionado ao final da lista ou, em uma caixa de combinação classificada, em sua posição classificada correta com base na cadeia de caracteres do item. Em uma caixa de combinação não classificada, um aplicativo pode usar a mensagem de [**\_ inserção de CB**](cb-insertstring.md) para inserir um item em uma posição específica. Depois de adicionado, um item de lista é identificado pela sua posição.

Usando a mensagem de [**\_ FINDSTRINGEXACT**](cb-findstringexact.md) [**\_ FindString**](cb-findstring.md) ou CB, um aplicativo pode determinar a posição de um item de lista. **CB \_ FINDstring** localiza um item cuja cadeia de caracteres começa com a cadeia de caracteres especificada. **CB \_ FINDSTRINGEXACT** localiza um item cuja cadeia de caracteres corresponde exatamente à cadeia de caracteres. Nenhuma mensagem diferencia maiúsculas de minúsculas.

Um aplicativo pode remover um item de lista usando a [**mensagem \_ excluída CB**](cb-deletestring.md) . Se um aplicativo precisar reinicializar a lista da caixa de combinação, ele poderá primeiro limpar seu conteúdo inteiro usando a mensagem [**CB \_ RESETCONTENT**](cb-resetcontent.md) . Ao adicionar vários itens à lista depois que uma caixa de combinação já tiver sido mostrada, um aplicativo poderá limpar o sinalizador de redesenho para impedir que a caixa de combinação seja repintada após a adição de cada item. Para obter mais informações sobre como redesenhar, consulte a descrição da mensagem de [**\_ reemissão do WM**](/windows/desktop/gdi/wm-setredraw) .

Para recuperar a cadeia de caracteres associada a um item de lista, um aplicativo pode usar a mensagem [**CB \_ GETLBTEXT**](cb-getlbtext.md) . A cadeia de caracteres do item é copiada para o buffer especificado pelo aplicativo. Para garantir que o buffer seja grande o suficiente para receber a cadeia de caracteres, o aplicativo pode primeiro usar a mensagem [**\_ GETLBTEXTLEN CB**](cb-getlbtextlen.md) para determinar o comprimento da cadeia de caracteres. Para obter o número de itens de lista em uma caixa de combinação, um aplicativo pode usar a mensagem de [**\_ iscount CB**](cb-getcount.md) .

## <a name="edit-control-selection-fields"></a>Editar campos de seleção de controle

Um aplicativo pode recuperar ou definir o conteúdo do campo de seleção e pode determinar ou definir a seleção de edição. O aplicativo também pode limitar a quantidade de texto que um usuário pode digitar no campo de seleção. Quando o conteúdo do campo de seleção é alterado, o sistema envia mensagens de notificação para o procedimento de janela ou caixa de diálogo pai.

Para recuperar o conteúdo do campo de seleção, um aplicativo pode enviar a mensagem de [**\_ gettext do WM**](/windows/desktop/winmsg/wm-gettext) para a caixa de combinação. Para definir o conteúdo do campo de seleção de uma caixa de combinação simples ou suspensa, um aplicativo pode enviar a mensagem do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) para a caixa de combinação.

A seleção de editar é o intervalo do texto selecionado, se houver, no campo de seleção de uma caixa de combinação simples ou suspensa. Um aplicativo pode determinar as posições de caractere inicial e final da seleção atual usando a mensagem [**CB \_ GETEDITSEL**](cb-geteditsel.md) . Ele também pode selecionar os caracteres na seleção de edição usando a mensagem [**CB \_ SETEDITSEL**](cb-seteditsel.md) .

Inicialmente, a quantidade de texto que o usuário pode digitar no campo de seleção é limitada pelo tamanho do campo de seleção. No entanto, se a caixa de combinação tiver o estilo [**\_ AUTOHSCROLL do CBS**](combo-box-styles.md) , o texto poderá continuar além do tamanho do campo de seleção. Um aplicativo pode usar a [**mensagem \_ LIMITTEXT CB**](cb-limittext.md) para limitar a quantidade de texto que um usuário pode digitar no campo de seleção, independentemente de o controle ter o **estilo \_ AUTOHSCROLL CBS** .

Quando o usuário edita o conteúdo do campo de seleção, a janela pai ou o procedimento de caixa de diálogo recebe mensagens de notificação. O código de notificação [CBN \_ EDITUPDATE](cbn-editupdate.md) é enviado primeiro, indicando que o texto no campo de seleção foi editado. Depois que o texto alterado é exibido, o sistema envia [CBN \_ EDITCHANGE](cbn-editchange.md). Quando o conteúdo do campo de seleção é alterado como resultado de um item de lista que está sendo selecionado, essas mensagens não são enviadas.

## <a name="owner-drawn-combo-boxes"></a>Owner-Drawn caixas de combinação

Um aplicativo pode criar uma caixa de combinação desenhada pelo proprietário para assumir a responsabilidade por itens de lista de pintura. A janela pai de uma caixa de combinação desenhada pelo proprietário (seu proprietário) recebe mensagens do [**WM \_ DRAWITEM**](wm-drawitem.md) quando uma parte da caixa de combinação precisa ser pintada. Uma caixa de combinação desenhada pelo proprietário pode listar informações diferentes de, ou além de, cadeias de caracteres de texto. As caixas de combinação desenhadas pelo proprietário podem ser de qualquer tipo. No entanto, o controle de edição em uma caixa de combinação simples ou suspensa só pode exibir texto, enquanto o proprietário pinta o campo de seleção em uma caixa de listagem suspensa.

O proprietário de uma caixa de combinação desenhada pelo proprietário deve processar a mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) . Essa mensagem é enviada sempre que uma parte da caixa de combinação deve ser redesenhada. O proprietário pode precisar processar outras mensagens, dependendo dos estilos especificados para a caixa de combinação.

Um aplicativo pode criar uma caixa de combinação desenhada pelo proprietário especificando o estilo [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) ou [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) . Se todos os itens da lista na caixa de combinação tiverem a mesma altura, como cadeias de caracteres ou ícones, um aplicativo poderá usar o estilo **\_ OwnerDrawFixed do CBS** . Se os itens de lista forem de altura variável, como bitmaps de tamanho diferente, um aplicativo poderá usar o estilo **\_ OwnerDrawVariable do CBS** .

O proprietário de uma caixa de combinação desenhada pelo proprietário pode processar uma mensagem do [**WM \_ MEASUREITEM**](wm-measureitem.md) para especificar as dimensões de itens de lista na caixa de combinação. Se o aplicativo criar a caixa de combinação usando o [**estilo \_ OwnerDrawFixed do CBS**](combo-box-styles.md) , o sistema enviará a mensagem do **WM \_ MEASUREITEM** apenas uma vez. As dimensões especificadas pelo proprietário são usadas para todos os itens de lista. Se o estilo [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) for usado, o sistema enviará uma mensagem do **WM \_ MEASUREITEM** para cada item de lista adicionado à caixa de combinação. O proprietário pode determinar ou definir a altura de um item de lista a qualquer momento usando as mensagens [**CB \_ GETITEMHEIGHT**](cb-getitemheight.md) e [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md) , respectivamente.

Se as informações exibidas em uma caixa de combinação desenhada pelo proprietário incluírem texto, um aplicativo poderá controlar o texto de cada item de lista especificando o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) . As caixas de combinação com o estilo de [**\_ classificação CBS**](combo-box-styles.md) são classificadas com base neste texto. Se uma caixa de combinação for classificada e não do estilo **\_ HASSTRINGS do CBS** , o proprietário deverá processar a mensagem do [**WM \_ COMPAREITEM**](wm-compareitem.md) .

Em uma caixa de combinação desenhada pelo proprietário, o proprietário deve manter o controle dos itens de lista contendo informações que não sejam ou além do texto. Uma maneira conveniente de fazer isso é salvar o identificador nas informações como dados do item. Para liberar objetos de dados associados a itens em uma caixa de combinação, o proprietário pode processar a mensagem [**\_ DELETEITEM do WM**](wm-deleteitem.md) .

## <a name="subclassed-combo-boxes"></a>Caixas de combinação de subclasse

A subclasse é um procedimento que permite que um aplicativo intercepte e processe mensagens enviadas ou postadas em uma janela. Usando a subclasse, um aplicativo pode substituir seu próprio processamento para determinadas mensagens, deixando a maioria do processamento de mensagens para o procedimento de janela definido pela classe.

Quando o sistema operacional cria uma janela, ele salva informações sobre ela em uma estrutura de dados interna que inclui um ponteiro para o procedimento de janela. Para subclasse de uma janela, um aplicativo chama a função [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) para substituir o ponteiro para esse procedimento por um ponteiro para um procedimento de subclasse definido pelo aplicativo. Depois disso, todas as mensagens para a janela são enviadas para o procedimento de subclasse. Esse procedimento usa a função [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) para passar mensagens não processadas para o procedimento de janela original. Para obter uma descrição do processamento de mensagens executado pelo procedimento da janela da classe COMBOBOX, consulte [comportamento padrão da caixa de combinação](combo-box-features.md).

Quando a caixa de combinação está fora de uma caixa de diálogo, um aplicativo não pode processar a guia, inserir e teclas ESC, a menos que use um procedimento de subclasse. Quando uma caixa de combinação simples ou suspensa recebe o foco de entrada, ela imediatamente define o foco para seu controle de edição filho. Portanto, um aplicativo deve subclasse do controle de edição para interceptar a entrada do teclado para uma caixa de combinação simples ou suspensa. Para obter um exemplo disso, consulte [subclasse de uma caixa de combinação](using-combo-boxes.md).

Se um procedimento de subclasse processar a mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , ele deverá usar a função [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) para se preparar para a pintura. Antes de chamar a função [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) , ela passa o identificador do controlador de domínio (DC) como o parâmetro *wParam* para o procedimento de janela. Se **EndPaint** for chamado primeiro, o procedimento da janela de classe não pintará porque **endpaintt** valida a janela inteira.

Uma técnica relacionada à subclasse é a superclasse. Uma superclasse é semelhante a qualquer outra classe, exceto que seu procedimento de janela não chama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para lidar com mensagens não processadas. Em vez disso, ele passa mensagens não processadas para o procedimento de janela para a classe de janela pai. Siga as diretrizes em [procedimentos de janela](/windows/desktop/winmsg/window-procedures) para evitar problemas que podem ocorrer com a subclasse e a superclasse.

 

 