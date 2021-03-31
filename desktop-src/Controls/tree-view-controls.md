---
title: Sobre controles de Tree-View
description: Um controle de exibição de árvore é uma janela que exibe uma lista hierárquica de itens, como os cabeçalhos de um documento, as entradas em um índice ou os arquivos e diretórios em um disco.
ms.assetid: 10cc7949-dd77-412d-bad1-db8d8a049582
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df70a2d3c2f841b022930a07ee2f140ee5bfc8e3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917736"
---
# <a name="about-tree-view-controls"></a>Sobre controles de Tree-View

Um controle de exibição de árvore é uma janela que exibe uma lista hierárquica de itens, como os cabeçalhos de um documento, as entradas em um índice ou os arquivos e diretórios em um disco. Cada item consiste em um rótulo e uma imagem de bitmap opcional, e cada item pode ter uma lista de subitens associados a ele. Ao clicar em um item, o usuário pode expandir ou recolher a lista de subitens associada.

A ilustração a seguir mostra um controle de exibição em árvore simples com um nó raiz, um nó expandido e um nó recolhido. O controle usa um bitmap para o item selecionado e outro bitmap para outros itens.

![captura de tela mostrando cinco nós em uma hierarquia; o texto de um nó é selecionado, mas os nós não são vinculados entre si por linhas](images/tv-simple.png)

Depois de criar um controle de exibição de árvore, você adiciona, remove, organiza ou manipula itens, enviando mensagens para o controle. Cada mensagem tem uma ou mais macros correspondentes que você pode usar em vez de enviar a mensagem explicitamente.

Os tópicos a seguir são discutidos nesta seção.

-   [Estilos de exibição de árvore](#tree-view-styles)
-   [Itens pai e filho](#parent-and-child-items)
-   [Rótulos de item](#item-labels)
-   [Edição de rótulo de exibição de árvore](#tree-view-label-editing)
-   [Posição do item de exibição de árvore](#tree-view-item-position)
-   [Visão geral dos Estados do item de exibição de árvore](#tree-view-item-states-overview)
-   [Seleção de item](#item-selection)
-   [Informações do item](#item-information)
-   [Árvore-Exibir listas de imagens](#tree-view-image-lists)
-   [Operações de arrastar e soltar](#drag-and-drop-operations)
-   [Mensagens de notificação de controle de exibição de árvore](#tree-view-control-notification-messages)
-   [Processamento de mensagens de controle de Tree-View padrão](#default-tree-view-control-message-processing)
-   [Tópicos relacionados](#related-topics)

## <a name="tree-view-styles"></a>Estilos de Tree-View

Estilos de exibição de árvore controlam aspectos de uma aparência de controle de exibição de árvore. Você define os estilos iniciais ao criar o controle de exibição de árvore. Você pode recuperar e alterar os estilos depois de criar o controle de exibição de árvore usando as funções [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

O estilo de [**\_ HASLINES de TVs**](tree-view-control-window-styles.md) aprimora a representação gráfica de uma hierarquia de controle de exibição em árvore por meio do desenho de linhas que vinculam itens filho ao item pai, conforme mostrado na ilustração a seguir.

![captura de tela mostrando a disposição anterior, mas com linhas que ingressam nos nós; a primeira linha descende do nó raiz](images/tv-haslines.png)

Por si só, esse estilo não desenha linhas na raiz da hierarquia. Para fazer isso, você precisa combinar os estilos de [**TVs \_ HASLINES**](tree-view-control-window-styles.md) e [**TVs \_ LINESATROOT**](tree-view-control-window-styles.md) . O resultado é mostrado na ilustração a seguir.

![captura de tela mostrando a disposição anterior, mas com uma linha horizontal adicional que leva ao nó raiz](images/tv-rootlines.png)

O usuário pode expandir ou recolher a lista de itens filho de um item pai clicando duas vezes no item pai. Um controle de exibição de árvore que tem o estilo [**\_ HASBUTTONS de TVs**](tree-view-control-window-styles.md) adiciona um botão à esquerda de cada item pai. O usuário pode clicar no botão uma vez, em vez de clicar duas vezes no item pai para expandir ou recolher o filho. **TVs \_ HASBUTTONS** não Adiciona botões a itens na raiz da hierarquia. Para fazer isso, você deve combinar [**TVs \_ HASLINES**](tree-view-control-window-styles.md), [**TVs \_ LINESATROOT**](tree-view-control-window-styles.md)e **TVs \_ HASBUTTONS**. Essa combinação de estilos é mostrada na ilustração a seguir.

![captura de tela mostrando a disposição anterior, mas com os botões expandir/recolher em cada vértice de duas linhas](images/tv-hasbuttons.png)

O estilo das [**\_ caixas de seleção TVs**](tree-view-control-window-styles.md) cria caixas de seleção ao lado de cada item. Se você quiser usar o estilo da caixa de seleção, deverá definir o estilo das **\_ caixas de seleção TVs** (com [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)) depois de criar o controle de exibição de árvore e antes de preencher a árvore. Caso contrário, as caixas de seleção podem parecer desmarcadas, dependendo dos problemas de tempo. A ilustração a seguir mostra o estilo da caixa de seleção.

![captura de tela mostrando a disposição anterior, mas com uma caixa de seleção ao lado de cada nó; duas caixas de seleção estão selecionadas](images/tv-haschecks.png)

O [**estilo \_ FULLROWSELECT de TVs**](tree-view-control-window-styles.md) faz com que o realce de seleção se estenda pela largura total do controle, não apenas no próprio item. A ilustração a seguir mostra esse estilo.

![captura de tela mostrando a organização original de cinco nós sem linhas, mas o realce de seleção estende a largura total do controle](images/tv-fullrow.png)

O [**estilo \_ EDITLABELS de TVs**](tree-view-control-window-styles.md) possibilita que o usuário edite os rótulos de itens de exibição em árvore. Para obter mais informações sobre como editar rótulos, consulte [edição de rótulos de exibição em árvore](#tree-view-label-editing).

Para obter mais informações sobre esses e outros estilos, consulte [estilos de janela de controle de exibição de árvore](tree-view-control-window-styles.md).

## <a name="parent-and-child-items"></a>Itens pai e filho

Qualquer item em um controle de exibição de árvore pode ter uma lista de subitens, chamados de *itens filho*, associados a ele. Um item que tem um ou mais itens filho é chamado de *item pai*. Um item filho é exibido abaixo de seu item pai e é recuado para indicar que ele é subordinado ao pai. Um item que não tem pai aparece na parte superior da hierarquia e é chamado de *Item raiz*.

Para adicionar um item a um controle de exibição de árvore, envie a mensagem [**TVM \_ INSERTITEM**](tvm-insertitem.md) para o controle. A mensagem retorna um identificador para o tipo HTREEITEM, que identifica exclusivamente o item. Ao adicionar um item, você deve especificar o identificador para o item pai do novo item. Se você especificar **NULL** ou o \_ valor raiz de TVI em vez de um identificador de item pai na estrutura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , o item será adicionado como um item raiz.

Em um determinado momento, o estado da lista de itens filho de um item pai pode ser expandido ou recolhido. Quando o estado é expandido, os itens filho são exibidos abaixo do item pai. Quando ele é recolhido, os itens filho não são exibidos. A lista alterna automaticamente entre os Estados expandidos e recolhidos quando o usuário clica duas vezes no item pai ou, se o pai tem o estilo [**\_ HASBUTTONS de TVs**](tree-view-control-window-styles.md) , quando o usuário clica no botão associado ao item pai. Um aplicativo pode expandir ou recolher os itens filho usando a mensagem [**de \_ expansão TVM**](tvm-expand.md) .

Um controle de exibição de árvore envia a janela pai uma mensagem de notificação de [TVN ao \_ expandir](tvn-itemexpanding.md) quando a lista de itens filho de um item pai está prestes a ser expandida ou recolhida. A notificação dá a um aplicativo a oportunidade de impedir a alteração ou definir qualquer atributo do item pai que dependa do estado da lista de itens filho. Depois de alterar o estado da lista, o controle de exibição de árvore envia a janela pai uma mensagem de notificação [TVN \_ ](tvn-itemexpanded.md) .

Quando uma lista de itens filhos é expandida, ela é recuada em relação ao item pai. Você pode definir a quantidade de recuo usando a mensagem [**TVM \_ SetIndent**](tvm-setindent.md) ou recuperar a quantidade atual usando a mensagem [**TVM \_ GetIndent**](tvm-getindent.md) .

Um controle de exibição de árvore usa a memória alocada do heap do processo que cria o controle de exibição de árvore. O número máximo de itens em um modo de exibição de árvore é baseado na quantidade de memória disponível no heap.

## <a name="item-labels"></a>Rótulos de item

Normalmente, você especifica o texto do rótulo de um item ao adicionar o item ao controle de exibição de árvore. A mensagem [**TVM \_ INSERTITEM**](tvm-insertitem.md) inclui uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que define as propriedades do item, incluindo uma cadeia de caracteres que contém o texto do rótulo.

Um controle de exibição de árvore aloca memória para armazenar cada item; o texto dos rótulos de item ocupa uma parte significativa dessa memória. Se o seu aplicativo mantiver uma cópia das cadeias de caracteres no controle de exibição em árvore, você poderá diminuir os requisitos de memória do controle especificando o \_ valor de USERcallback de LPSTR no membro **PszText** de [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) em vez de passar cadeias de caracteres reais para o modo de exibição de árvore. O uso de \_ TEXTcallback de LPSTR faz com que o controle de exibição em árvore recupere o texto do rótulo de um item da janela pai sempre que o item precisar ser redesenhado. Para recuperar o texto, o controle de exibição de árvore envia uma mensagem de notificação [TVN \_ GETDISPINFO](tvn-getdispinfo.md) , que inclui o endereço de uma estrutura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . A janela pai deve preencher os membros apropriados da estrutura incluída.

## <a name="tree-view-label-editing"></a>Edição de rótulo de Tree-View

O usuário pode editar diretamente os rótulos de itens em um controle de exibição de árvore que tem o estilo [**\_ EDITLABELS de TVs**](tree-view-control-window-styles.md) . O usuário começa a editar clicando no rótulo do item que tem o foco. Um aplicativo começa a ser editado usando a mensagem [**TVM \_ EDITLABEL**](tvm-editlabel.md) . O controle de exibição de árvore notifica a janela pai quando a edição começa e quando é cancelada ou concluída. Quando a edição for concluída, a janela pai será responsável por atualizar o rótulo do item, se apropriado.

Quando começa a edição do rótulo, um controle de exibição de árvore envia a janela pai uma mensagem de notificação [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) . Ao processar essa notificação, um aplicativo pode permitir a edição de alguns rótulos e impedir a edição de outros. Retornar zero permite a edição, e o retorno de zero é evitado.

Quando a edição de rótulo é cancelada ou concluída, um controle de exibição de árvore envia a janela pai uma mensagem de notificação [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) . O parâmetro *lParam* é o endereço de uma estrutura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . O parâmetro *Item* é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que identifica o item e inclui o texto editado. A janela pai é responsável por atualizar o rótulo do item se quiser manter o novo rótulo. O membro **pszText** de **TVITEM** será zero se a edição for cancelada.

Durante a edição do rótulo, normalmente em resposta à mensagem de notificação do [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) , você pode recuperar o identificador para o controle de edição usado para edição de rótulo usando a mensagem [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) . Você pode enviar o controle de edição uma mensagem em [**\_ SETLIMITTEXT**](em-setlimittext.md) para limitar a quantidade de texto que um usuário pode inserir ou subclasse do controle de edição para interceptar e descartar caracteres inválidos. Observe, no entanto, que o controle de edição é exibido somente *depois* que   TVN \_ BEGINLABELEDIT é enviado.

## <a name="tree-view-item-position"></a>Posição do item de Tree-View

A posição inicial de um item é definida quando o item é adicionado ao controle de exibição de árvore usando a mensagem [**TVM \_ INSERTITEM**](tvm-insertitem.md) . A mensagem inclui uma estrutura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) que especifica o identificador para o item pai e o identificador para o item após o qual o novo item será inserido. O segundo identificador deve identificar um item filho do pai determinado ou um destes valores: TVI \_ First, TVI \_ Last ou TVI \_ Sort.

Quando TVI \_ First ou TVI \_ Last é especificado, o controle Tree-View coloca o novo item no início ou no final da lista de itens filho de um determinado item pai. Quando \_ a classificação TVI é especificada, o controle de exibição de árvore insere o novo item na lista de itens filho em ordem alfabética com base no texto dos rótulos de item.

Você pode colocar a lista de itens filho de um item pai em ordem alfabética usando a mensagem [**TVM \_ SORTCHILDREN**](tvm-sortchildren.md) . A mensagem inclui um parâmetro que especifica se todos os níveis de itens filho decrescentes do item pai fornecido também são classificados em ordem alfabética.

A mensagem [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) permite que você classifique itens filhos com base em critérios definidos por você. Ao usar essa mensagem, você especifica uma função de retorno de chamada definida pelo aplicativo que o controle de exibição de árvore pode chamar sempre que a ordem relativa de dois itens filho precisa ser decidida. A função de retorno de chamada recebe valores definidos por aplicativo de 2 32 bits para os itens que estão sendo comparados e um terceiro valor de 32 bits que você especifica ao enviar **TVM \_ SORTCHILDRENCB**.

## <a name="tree-view-item-states-overview"></a>Visão geral dos Estados do item de Tree-View

Cada item em um controle de exibição de árvore tem um estado atual. As informações de estado de cada item incluem um conjunto de sinalizadores de bit, bem como índices de lista de imagens que indicam a imagem de estado e a imagem de sobreposição do item. Os sinalizadores de bits indicam se o item está selecionado, desabilitado, expandido e assim por diante. Na maior parte, um controle de exibição de árvore define automaticamente o estado de um item para refletir as ações do usuário, como a seleção de um item. No entanto, também é possível definir o estado de um item usando a mensagem [**TVM \_ SETITEM**](tvm-setitem.md) , e você pode recuperar o estado atual de um item usando a mensagem [**TVM \_ GETITEM**](tvm-getitem.md) . Para obter uma lista completa de Estados de item, consulte [Estados de item de controle de exibição em árvore](tree-view-control-item-states.md).

O estado atual de um item é especificado pelo membro de **estado** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) . Um controle de exibição de árvore pode alterar o estado de um item para refletir uma ação do usuário, como selecionar o item ou definir o foco para o item. Além disso, um aplicativo pode alterar o estado de um item para desabilitar ou ocultar o item ou para especificar uma imagem de sobreposição ou imagem de estado.

Quando você especifica ou altera o estado de um item, o membro **stateMask** de [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) especifica quais bits de estado definir e o membro de **estado** contém os novos valores para esses bits.

Para definir a imagem de sobreposição de um item, **stateMask** deve incluir o valor de [**\_ OVERLAYMASK TVIS**](tree-view-control-item-states.md) e o **estado** deve incluir o índice de base um da imagem de sobreposição deslocada para a esquerda 8 bits usando a macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) . O índice pode ser zero para não especificar nenhuma imagem de sobreposição.

Uma imagem de estado é exibida ao lado do ícone de um item para indicar um estado definido pelo aplicativo. As imagens de estado estão contidas em uma *lista de imagens de estado* que é especificada pelo envio de uma mensagem [**TVM \_ SetImageList**](tvm-setimagelist.md) . Para definir a imagem de estado de um item, inclua o valor [**TVIS \_ STATEIMAGEMASK**](tree-view-control-item-states.md) no membro **stateMask** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) . O bits 12 a 15 do membro de **estado** da estrutura especifica o índice na lista de imagens de estado da imagem a ser desenhada.

Para definir o índice de imagem de estado, use [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask). Essa macro usa um índice e define o bits 12 a 15 adequadamente. Para indicar que o item não tem nenhuma imagem de estado, defina o índice como zero. Essa convenção significa que a imagem zero na lista de imagens de estado não pode ser usada como uma imagem de estado. Para isolar o bits 12 a 15 do membro de **estado** , use a máscara [**TVIS \_ STATEIMAGEMASK**](tree-view-control-item-states.md) . Para obter mais informações sobre sobreposição e imagens de estado, consulte [lista de imagens de exibição em árvore](#tree-view-image-lists).

## <a name="item-selection"></a>Seleção de item

Um controle de exibição de árvore notifica a janela pai quando a seleção é alterada de um item para outro enviando as mensagens de notificação [TVN \_ SELCHANGING](tvn-selchanging.md) e [TVN \_ SELCHANGED](tvn-selchanged.md) . Ambas as notificações incluem um valor que especifica se a alteração é o resultado de um clique do mouse ou de um pressionamento de tecla. As notificações também incluem informações sobre o item que está recebendo a seleção e o item que está perdendo a seleção. Você pode usar essas informações para definir atributos de item que dependem do estado de seleção do item. Retornar **true** em resposta a TVN \_ SELCHANGING impede que a seleção seja alterada, e retornar **false** permite a alteração.

Um aplicativo pode alterar a seleção enviando a mensagem [**TVM \_ SELECTITEM**](tvm-selectitem.md) .

## <a name="item-information"></a>Informações do item

Os controles de exibição de árvore dão suporte a várias mensagens que recuperam informações sobre itens no controle.

A mensagem [**TVM \_ GETITEM**](tvm-getitem.md) pode recuperar o identificador e os atributos de um item. Os atributos de um item incluem seu estado atual, os índices na lista de imagens do controle das imagens bitmap selecionadas e não selecionadas do item, um sinalizador que indica se o item tem itens filho, o endereço da cadeia de caracteres do rótulo do item e o valor de 32 bits definido pelo aplicativo do item.

A mensagem [**TVM \_ GETNEXTITEM**](tvm-getnextitem.md) recupera o item de exibição de árvore que possui a relação especificada para o item atual. A mensagem pode recuperar o pai de um item, o próximo item visível ou o anterior, o primeiro item filho e assim por diante.

A mensagem [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) recupera o retângulo delimitador para um item de exibição de árvore. As mensagens [**TVM \_ GetCount**](tvm-getcount.md) e [**TVM \_ GETVISIBLECOUNT**](tvm-getvisiblecount.md) recuperam uma contagem dos itens em um controle de exibição de árvore e uma contagem dos itens que podem ser totalmente visíveis na janela do controle de exibição de árvore, respectivamente. Você pode garantir que um determinado item seja visível usando a mensagem [**TVM \_ ENSUREVISIBLE**](tvm-ensurevisible.md) .

## <a name="tree-view-image-lists"></a>Tree-View listas de imagens

Cada item em um controle de exibição de árvore pode ter quatro imagens de bitmap associadas a ela.

-   Uma imagem, como uma pasta aberta, exibida quando o item é selecionado.
-   Uma imagem, como uma pasta fechada, exibida quando o item não está selecionado.
-   Uma imagem de sobreposição que é desenhada de forma transparente sobre a imagem selecionada ou sem seleção.
-   Uma imagem de estado, que é uma imagem adicional exibida à esquerda da imagem selecionada ou não selecionada. Você pode usar imagens de estado, como as caixas de seleção marcada e desmarcada, para indicar os Estados de item definido pelo aplicativo.

Por padrão, um controle de exibição de árvore não exibe imagens de item. Para exibir imagens de itens, você deve criar listas de imagens e associá-las ao controle. Para obter mais informações sobre listas de imagens, consulte [listas de imagens](image-lists.md).

Um controle de exibição de árvore pode ter duas listas de imagens: uma lista de imagens normais e uma lista de imagens de estado. Uma lista de imagens normal armazena as imagens selecionadas, não selecionadas e sobreposição. Uma lista de imagens de estado armazena imagens de estado. Use a função [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) para criar uma lista de imagens e use outras funções de lista de imagens para adicionar bitmaps à lista de imagens. Em seguida, para associar a lista de imagens ao controle de exibição em árvore, use a mensagem [**TVM \_ SetImageList**](tvm-setimagelist.md) . A mensagem [**TVM \_ GetImageList**](tvm-getimagelist.md) recupera um identificador para uma das listas de imagens de um controle de exibição de árvore. Essa mensagem será útil se você precisar adicionar mais imagens à lista.

Além das imagens selecionadas e não selecionadas, uma lista de imagens normais de um controle de exibição de árvore pode conter até quatro imagens de sobreposição. As imagens de sobreposição são identificadas por um índice baseado em um e são projetadas para serem desenhadas de forma transparente nas imagens selecionadas e não selecionadas. Para atribuir um índice de máscara de sobreposição a uma imagem na lista de imagens normal, chame a função [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) .

Por padrão, todos os itens exibem a primeira imagem na lista de imagens normal para os Estados selecionados e não selecionados. Além disso, por padrão, os itens não exibem imagens de sobreposição ou imagens de estado. Você pode alterar esses comportamentos padrão para um item enviando a mensagem [**TVM \_ INSERTITEM**](tvm-insertitem.md) ou [**TVM \_ SETITEM**](tvm-setitem.md) . Essas mensagens usam a estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) para especificar índices de lista de imagens para um item.

Para especificar as imagens selecionadas e não selecionadas de um item, defina os \_ bits de imagem TVIF SELECTEDIMAGE e TVIF \_ no membro **Mask** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) e especifique índices da lista de imagens normal do controle nos membros **iSelectImage** e **iImage** . Como alternativa, você pode especificar o \_ valor I IMAGECALLBACK em **ISelectImage** e **iImage** em vez de especificar índices. Isso faz com que o controle consulte sua janela pai para obter um índice de lista de imagens cada vez que o item está prestes a ser redesenhado. O controle envia a mensagem de notificação [TVN \_ GETDISPINFO](tvn-getdispinfo.md) para recuperar o índice.

Para associar uma imagem de sobreposição a um item, use a macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) para especificar um índice de máscara de sobreposição no membro de **estado** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) do item. Você também deve definir os bits [**TVIS \_ OVERLAYMASK**](tree-view-control-item-states.md) no membro **stateMask** . Índices de máscara de sobreposição são baseados em um; um índice de zero indica que nenhuma imagem de sobreposição foi especificada.

As imagens de estado são armazenadas em uma lista de imagens de estado separada e identificadas por seu índice. Para especificar a lista de imagens de estado, envie uma mensagem [**TVM \_ SetImageList**](tvm-setimagelist.md) . Ao contrário do controle de exibição de lista, que usa um índice baseado em um para identificar imagens de estado, as imagens de estado do controle de exibição de árvore são identificadas por um índice baseado em zero. No entanto, um índice de zero indica que o item não tem uma imagem de estado. Consequentemente, a imagem zero não pode ser usada como uma imagem de estado. Para obter mais informações sobre Estados de item e imagens de estado, consulte [visão geral dos Estados de item de exibição de árvore](#tree-view-item-states-overview).

## <a name="drag-and-drop-operations"></a>Operações de arrastar e soltar

Um controle de exibição de árvore notifica a janela pai quando o usuário começa a arrastar um item. A janela pai recebe uma mensagem de notificação [TVN \_ BEGINDRAG](tvn-begindrag.md) quando o usuário começa a arrastar um item com o botão esquerdo do mouse e uma mensagem de notificação do [TVN \_ BEGINRDRAG](tvn-beginrdrag.md) quando o usuário começa a arrastar com o botão direito. Você pode impedir que um controle de exibição de árvore envie essas notificações fornecendo ao controle de exibição de árvore o estilo [**\_ DISABLEDRAGDROP de TVs**](tree-view-control-window-styles.md) .

Você Obtém uma imagem a ser exibida durante uma operação de arrastar usando a mensagem [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) . O controle de exibição de árvore cria um bitmap de arrastar com base no rótulo do item que está sendo arrastado. Em seguida, o controle de exibição de árvore cria uma lista de imagens, adiciona o bitmap a ela e retorna o identificador para a lista de imagens.

Você deve fornecer o código que realmente arrasta o item. Isso normalmente envolve o uso dos recursos de arrastar das funções da lista de imagens e processamento das mensagens do [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) e do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (ou do [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) enviadas para a janela pai após o início da operação de arrastar.

Se os itens em um controle de exibição de árvore forem os destinos das operações de arrastar e soltar, você precisará saber quando o ponteiro do mouse está em um item de destino. Você pode descobrir usando a mensagem [**TVM \_ HITTEST**](tvm-hittest.md) . Você especifica o endereço de uma estrutura [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) que contém as coordenadas atuais do ponteiro do mouse. Quando a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retorna, a estrutura contém um sinalizador que indica o local do ponteiro do mouse em relação ao controle de exibição de árvore. Se o ponteiro estiver sobre um item no controle de exibição de árvore, a estrutura também conterá o identificador para o item.

Você pode indicar que um item é o destino de uma operação de arrastar e soltar usando a mensagem [**TVM \_ SETITEM**](tvm-setitem.md) para definir o estado para o valor [**\_ DROPHILITED TVIS**](tree-view-control-item-states.md) . Um item que tem esse estado é desenhado no estilo usado para indicar um destino de arrastar e soltar.

## <a name="tree-view-control-notification-messages"></a>Tree-View mensagens de notificação de controle

Um controle de exibição de árvore envia as mensagens de notificação a seguir para sua janela pai na forma de mensagens de notificação do [**WM \_**](wm-notify.md) .



| Notificação                                    | Descrição                                                                            |
|-------------------------------------------------|----------------------------------------------------------------------------------------|
| [TVN \_ BEGINDRAG](tvn-begindrag.md)             | Sinaliza o início de uma operação de arrastar e soltar.                                        |
| [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md)   | Sinaliza o início da edição do rótulo in-loco.                                           |
| [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)           | Sinaliza que o botão direito do mouse iniciou uma operação de arrastar e soltar.             |
| [TVN \_ DELETEITEM](tvn-deleteitem.md)           | Sinaliza a exclusão de um item específico.                                               |
| [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md)       | Sinaliza o fim da edição do rótulo.                                                      |
| [TVN \_ GETDISPINFO](tvn-getdispinfo.md)         | Solicita informações que o controle de exibição de árvore requer para exibir um item.           |
| [TVN \_ DOexpanded](tvn-itemexpanded.md)       | Sinaliza que a lista de itens filho de um item pai foi expandida ou recolhida.            |
| [TVN ao \_ expandir](tvn-itemexpanding.md)     | Sinaliza que a lista de itens filho de um item pai está prestes a ser expandida ou recolhida. |
| [TVN \_ KEYDOWN](tvn-keydown.md)                 | Sinaliza um evento de teclado.                                                              |
| [TVN \_ SELCHANGED](tvn-selchanged.md)           | Sinaliza que a seleção foi alterada de um item para outro.                       |
| [TVN \_ SELCHANGING](tvn-selchanging.md)         | Sinaliza que a seleção está prestes a ser alterada de um item para outro.            |
| [TVN \_ SETDISPINFO](tvn-setdispinfo.md)         | Notifica uma janela pai de que ela deve atualizar as informações que ele mantém para um item. |



 

## <a name="default-tree-view-control-message-processing"></a>Processamento de mensagens de controle de Tree-View padrão

Esta seção descreve o processamento de mensagem de janela executado por um controle de exibição de árvore. As mensagens específicas para controles de exibição de árvore são discutidas em outras seções deste documento, portanto, elas não estão incluídas aqui.



| Mensagem                                            | Processamento realizado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**comando do WM \_**](/windows/desktop/menurc/wm-command)               | Processa as mensagens de notificação de controle de edição [en \_ Update](en-update.md) e [en \_ KILLFOCUS](en-killfocus.md) e encaminha todas as outras notificações de controle de edição para a janela pai. Nenhum valor de retorno.                                                                                                                                                                                                                                                                                                |
| [**criação do WM \_**](/windows/desktop/winmsg/wm-create)                 | Aloca memória e inicializa estruturas de dados internas. Ele retornará zero se for bem-sucedido ou-1 caso contrário.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)               | Libera todos os recursos do sistema associados ao controle. Ele retorna zero.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**habilitar o WM \_**](/windows/desktop/winmsg/wm-enable)                 | Habilita ou desabilita o controle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ERASEBKGND do WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)         | Apaga o plano de fundo da janela usando a cor da tela de fundo atual para o controle de exibição em árvore. Retorna **true**.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**GETDLGCODE do WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)         | Retorna uma combinação dos valores DLGC \_ WANTARROWS e DLGC \_ WANTCHARS.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**WM \_ GETfont**](/windows/desktop/winmsg/wm-getfont)               | Retorna o identificador para a fonte do rótulo atual.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**HSCROLL do WM \_**](wm-hscroll.md)                  | Rola o controle de exibição de árvore. Retornará **true** se a rolagem ocorrer ou **false** caso contrário.                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**o WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)             | Envia a mensagem de notificação [TVN \_ KEYDOWN](tvn-keydown.md) para a janela pai de todas as chaves. Envia a mensagem de notificação de [retorno de nm \_ (exibição de árvore)](nm-return-tree-view-.md) quando o usuário pressiona a tecla Enter. Ele move o cursor quando o usuário pressiona as teclas de direção ou a tecla PAGE UP, PAGE DOWN, HOME, END ou Backspace. Ele rola o controle de exibição de árvore quando o usuário pressiona a tecla CTRL em combinação com essas chaves. Retornará **true** se uma chave for processada ou **false** caso contrário. |
| [**KILLFOCUS do WM \_**](/windows/desktop/inputdev/wm-killfocus)         | Redesenha o item focado, se houver, e envia uma mensagem de notificação [nm \_ KILLFOCUS (exibição de árvore)](nm-killfocus-tree-view.md) para a janela pai.                                                                                                                                                                                                                                                                                                                                                                  |
| [**LBUTTONDBLCLK do WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk) | Cancela a edição do rótulo e, se um item tiver sido clicado duas vezes, o envia a mensagem de notificação [nm \_ DBLCLK (exibição de árvore)](nm-dblclk-tree-view.md) para a janela pai. Se a janela pai retornar 0, o controle de exibição de árvore alternará o estado expandido do item, enviando a janela pai as mensagens de notificação [TVN \_ ](tvn-itemexpanding.md) e [TVN \_ ](tvn-itemexpanded.md) . Nenhum valor de retorno.                                                                             |
| [**LBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-lbuttondown)     | Alterna o estado expandido se o usuário clicou no botão associado a um item pai. Se o usuário clicou em um rótulo de item, o controle de exibição de árvore seleciona e define o foco para o item. Se o usuário mover o mouse antes de soltar o botão do mouse, o controle de exibição de árvore começará uma operação de arrastar e soltar. Nenhum valor de retorno.                                                                                                                                                                          |
| [**pintura do WM \_**](/windows/desktop/gdi/wm-paint)                      | Pinta a região inválida do controle de exibição de árvore. Ele retorna zero. Se o parâmetro *wParam* for não **nulo**, o controle assumirá que o valor é um identificador para um contexto de dispositivo (HDC) e pinta usando esse contexto de dispositivo.                                                                                                                                                                                                                                                                                      |
| [**RBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-rbuttondown)     | Verifica se um item foi clicado e uma operação de arrastar foi iniciada. Se a operação tiver começado, ela enviará uma mensagem de notificação [TVN \_ BEGINRDRAG](tvn-beginrdrag.md) para a janela pai e destacará o destino de soltar. Caso contrário, ele envia uma mensagem de notificação [nm \_ RCLICK (exibição de árvore)](nm-rclick-tree-view.md) para a janela pai. Nenhum valor de retorno.                                                                                                                                           |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | Redesenha o item focado, se houver, e envia uma mensagem de notificação [nm \_ SETFOCUS](nm-setfocus.md) para a janela pai.                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ SETfont**](/windows/desktop/winmsg/wm-setfont)               | Salva a alça de fonte especificada e redesenha o controle de exibição de árvore usando a nova fonte.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**WM \_ reemissão**](/windows/desktop/gdi/wm-setredraw)              | Define ou limpa o sinalizador de redesenho. O controle de exibição de árvore é redesenhado depois que o sinalizador de redesenho é definido. Ele retorna zero.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**tamanho do WM \_**](/windows/desktop/winmsg/wm-size)                     | Recomputa variáveis internas que dependem do tamanho da área do cliente do controle de exibição de árvore. Retorna **true**.                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**estilo do WMchanged \_**](/windows/desktop/winmsg/wm-stylechanged)     | Cancela a edição do rótulo e redesenha o controle de exibição de árvore usando os novos estilos. Ele retorna zero.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**SYSCOLORCHANGE do WM \_**](/windows/desktop/gdi/wm-syscolorchange)    | Redesenha o controle de exibição de árvore usando a nova cor se o sinalizador de redesenho for definido. Nenhum valor de retorno.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_temporizador do WM**](/windows/desktop/winmsg/wm-timer)                   | Inicia a edição de um rótulo de item. Se o usuário clicar no rótulo do item focado, o controle de exibição de árvore definirá um temporizador em vez de entrar no modo de edição imediatamente. O timer possibilita que o modo de exibição de árvore Evite entrar no modo de edição se o usuário clicar duas vezes no rótulo. Ele retorna zero.                                                                                                                                                                                                                       |
| [**VSCROLL do WM \_**](wm-vscroll.md)                  | Rola o controle de exibição de árvore. Retornará **true** se a rolagem ocorrer ou **false** caso contrário.                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[EXEMPLO: CustDTv ilustra o desenho personalizado em um TreeView (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 