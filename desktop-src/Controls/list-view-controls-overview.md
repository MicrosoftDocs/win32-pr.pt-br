---
title: Sobre controles de List-View
description: Um controle de exibição de lista é uma janela que exibe uma coleção de itens.
ms.assetid: 163f7778-690c-4166-b0c5-c7be1a03ae98
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 592684378b4264319d790b1e2e05eb9e0ae37f28
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424326"
---
# <a name="about-list-view-controls"></a>Sobre controles de List-View

Consulte o [exemplo de controle ListView virtual](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw).

Um controle de exibição de lista é uma janela que exibe uma coleção de itens. Os controles de exibição de lista fornecem várias maneiras de organizar e exibir itens e são muito mais flexíveis do que [caixas de listagem](list-boxes.md)simples. Por exemplo, informações adicionais sobre cada item podem ser exibidas em colunas à direita do ícone e rótulo.

-   [Exibições e estilos de exibição de lista](#list-view-styles-and-views)
    -   [Estilos de List-View estendidos](#extended-list-view-styles)
-   [Estilo de List-View virtual](#virtual-list-view-style)
    -   [Criando um controle de List-View virtual](#creating-a-virtual-list-view-control)
    -   [Problemas de compatibilidade](#compatibility-issues)
    -   [Manipulando códigos de notificação de controle de List-View virtual](#handling-virtual-list-view-control-notification-codes)
    -   [Gerenciamento de cache](#cache-management)
-   [Áreas de trabalho da exibição de lista](#list-view-working-areas)
-   [Listar listas de imagens de exibição](#list-view-image-lists)
-   [Listar itens e subitens de exibição](#list-view-items-and-subitems)
    -   [Listar Estados de item de exibição](#list-view-item-states)
    -   [Itens de retorno de chamada e a máscara de retorno de chamada](#callback-items-and-the-callback-mask)
    -   [Posição do item de exibição de lista](#list-view-item-position)
    -   [Organizando, classificação e localizar itens](#arranging-sorting-and-finding-items)
-   [Colunas de exibição de lista](#list-view-columns)
-   [Posição de rolagem da exibição de lista](#list-view-scroll-position)
-   [Edição de rótulo de exibição de lista](#list-view-label-editing)
-   [Cores de exibição de lista](#list-view-colors)
-   [Organizando itens de lista por grupo](#arranging-list-items-by-group)
-   [Marcas de inserção](#insertion-marks)

## <a name="list-view-styles-and-views"></a>List-View estilos e exibições

Controles de exibição de lista podem exibir itens em cinco exibições diferentes. O estilo de janela do controle especifica a exibição padrão. Estilos de janela adicionais especificam o alinhamento de itens e recursos específicos do controle. A tabela a seguir descreve as exibições.



| Nome da exibição             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exibição de ícone             | Especificado pelo estilo de janela [**ÍCONE LVS \_**](list-view-window-styles.md) ou passando o ÍCONE DE EXIBIÇÃO **LV \_ \_** com a [**mensagem LVM \_ SETVIEW.**](lvm-setview.md) Cada item é exibido como um ícone em tamanho normal com um rótulo abaixo dele. O usuário pode arrastar os itens para qualquer local na janela de exibição de lista.                                                                                                                                                                                                                                         |
| Exibição de ícone pequeno       | Especificado pelo estilo de [**janela \_ SMALLICON LVS**](list-view-window-styles.md) ou passando **LV \_ VIEW \_ SMALLICON** com [**LVM \_ SETVIEW**](lvm-setview.md). Cada item aparece como um ícone pequeno com o rótulo à direita dele. O usuário pode arrastar os itens para qualquer local.                                                                                                                                                                                                                                                       |
| Modo de exibição de lista             | Especificado pelo estilo da janela [**LVS \_ LIST**](list-view-window-styles.md) ou passando **LV \_ VIEW \_ LIST** com [**LVM \_ SETVIEW**](lvm-setview.md). Cada item aparece como um ícone pequeno com um rótulo à direita dele. Os itens são organizados em colunas e o usuário não pode arrastá-los para um local arbitrário.                                                                                                                                                                                                                               |
| Exibição de relatório (detalhes) | Especificado pelo estilo de janela do [**\_ relatório LVS**](list-view-window-styles.md) ou passando **\_ \_ detalhes da exibição LV** com o [**LVM \_ SetView**](lvm-setview.md). Cada item aparece em sua própria linha, com informações organizadas em colunas. A coluna mais à esquerda sempre é justificada e contém o ícone pequeno e o rótulo. Colunas subsequentes contêm subitens, conforme especificado pelo aplicativo. Cada coluna tem um cabeçalho, a menos que você também especifique o estilo de janela [**LVS \_ nocolumnheader**](list-view-window-styles.md) . |
| Exibição Lado a Lado             | **Versão 6 e posterior.** Especificado passando o **\_ \_ bloco de exibição LV** com o [**LVM \_ SetView**](lvm-setview.md). Cada item aparece como um ícone de tamanho máximo com um rótulo de uma ou mais linhas ao lado dele.                                                                                                                                                                                                                                                                                                                                                        |



 

As capturas de tela a seguir usam exibições para mostrar diferentes quantidades de informações sobre cada um dos sete animais de estimação. As exibições demonstram como as informações podem ser exibidas no Windows Vista. Os estilos visuais para o controle foram definidos para o tema "Explorer" usando [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).

A captura de tela a seguir mostra a exibição de detalhes.

![captura de tela que mostra informações em cinco colunas e sete linhas](images/lv-detailsview.png)

A captura de tela a seguir mostra a exibição de ícone.

![captura de tela que mostra apenas o nome de cada animal de estimação e um ícone que indica a espécie](images/lv-iconview.png)

A captura de tela a seguir mostra o modo de exibição de lista.

![captura de tela que mostra, para cada animal de estimação, um ícone grande próximo ao texto do nome, da categoria e do preço do animal de estimação](images/lv-listview.png)

A captura de tela a seguir mostra a exibição de azul.

![exibição deile.](images/lv-tileview.png)

Você pode alterar o tipo de exibição depois de criar um controle de exibição de lista. Para recuperar e alterar o estilo da janela, use as [**funções GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) Para determinar os estilos de janela da exibição atual, use o [**valor \_ TYPEMASK LVS.**](list-view-window-styles.md)

Você pode controlar a maneira como os itens são organizados no ícone ou na exibição de ícone pequeno especificando o estilo de janela [**LVS \_ ALIGNTOP**](list-view-window-styles.md) (padrão) ou [**LVS \_ ALIGNLEFT.**](list-view-window-styles.md)

Você pode alterar o alinhamento depois de criar um controle de exibição de lista. Para determinar o alinhamento atual, use o valor [**LVS \_ ALIGNMASK.**](list-view-window-styles.md)

Estilos de janela adicionais fornecem outras opções, como se um usuário pode editar rótulos ou selecionar mais de um item por vez. Para ver uma lista completa, consulte [Estilos de janela de exibição de lista.](list-view-window-styles.md)

### <a name="extended-list-view-styles"></a>Estilos List-View estendidos

Os estilos de controle de exibição de lista estendida fornecem opções como caixas de seleção, barras de rolagem simples, linhas de grade e acompanhamento a quente. Para ver uma lista completa, consulte [Estilos List-View estendidos.](extended-list-view-styles.md) Você não acessa estilos estendidos de exibição de lista da mesma maneira que os estilos de janela padrão. Você não usa as [**funções GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para fazer alterações de estilo estendidas.

Há duas mensagens que configuram e recuperam informações de estilo estendidas, [**LVM \_ SETEXTENDEDLISTVIEWSTYLE**](lvm-setextendedlistviewstyle.md) e [**LVM \_ GETEXTENDEDLISTVIEWSTYLE**](lvm-getextendedlistviewstyle.md). Em vez de enviar as mensagens explicitamente, você pode usar as seguintes macros correspondentes: [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle), [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)e [**ListView \_ GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle).

## <a name="virtual-list-view-style"></a>Estilo List-View virtual

Uma exibição de lista virtual é um controle de exibição de lista que tem o [**estilo LVS \_ OWNERDATA.**](list-view-window-styles.md) Esse estilo permite que o controle gere milhões de itens porque o proprietário recebe a carga de gerenciamento de dados de item. Isso permite que você use o controle de exibição de lista virtual com grandes bancos de dados de informações, em que os métodos específicos de acesso ao dado já estão em vigor.

Um controle de exibição de lista virtual mantém muito pouco informações sobre o item. Exceto para a seleção de item e as informações de foco, o proprietário do controle deve gerenciar todas as informações de item. Outros processos solicitam informações do item do proprietário usando códigos de notificação do [LVN \_ GETDISPINFO](lvn-getdispinfo.md) .

Como esse tipo de controle de lista destina-se a grandes conjuntos de dados, é recomendável que você armazene em cache os dados de item solicitados para melhorar o desempenho de recuperação. A exibição de lista fornece um mecanismo de dicas de cache para ajudar na otimização do cache. A dica é implementada na forma de um código de notificação [LVN \_ ODCACHEHINT](lvn-odcachehint.md) .

### <a name="creating-a-virtual-list-view-control"></a>Criando um controle de List-View virtual

Você cria controles de exibição de lista virtual usando a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando o estilo de janela [**LVS \_ OWNERDATA**](list-view-window-styles.md) como parte do parâmetro de função *dwStyle* . Não há suporte para a alternância dinâmica de e para o estilo **LVS \_ OWNERDATA** .

Você pode usar o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) em combinação com a maioria dos outros estilos de janela, exceto o estilo [**LVS \_ SORTASCENDING**](list-view-window-styles.md) ou [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) . Todos os controles de exibição de lista virtual são padronizados para o estilo de [**\_ AutoOrganizar LVS**](list-view-window-styles.md) .

Para habilitar itens a serem exibidos na lista, você deve primeiro enviar a mensagem [**LVM \_ setitemcount**](lvm-setitemcount.md) , seja explicitamente ou usando a macro [**\_ SetItemCountEx do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) .

As seguintes mensagens não têm suporte no estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) : [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md), [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md), [**LVM \_ SETTILEINFO**](lvm-settileinfo.md)e [**LVM \_ MAPIDTOINDEX**](lvm-mapidtoindex.md).

### <a name="compatibility-issues"></a>Problemas de compatibilidade

Todos os quatro estilos de exibição de lista – ícone, ícone pequeno, lista e exibição de relatório – são suportados no [**estilo LVS \_ OWNERDATA.**](list-view-window-styles.md) Controles de exibição de lista que têm o **estilo LVS \_ OWNERDATA** não armazenam nenhuma informação específica do item. Portanto, os únicos sinalizadores de estado de item válidos que você pode aplicar a um item são [**LVIS \_ SELECTED**](list-view-item-states.md) e [**LVIS \_ FOCUSED.**](list-view-item-states.md) Nenhuma outra informação de estado é armazenada. Em particular, o controle de exibição de lista não mantém imagens de estado ou sobreposição para cada item. No entanto, você pode fazer com que o controle de exibição de lista consulte seu aplicativo para essas imagens enviando uma mensagem [**LVM \_ SETCALLBACKMASK.**](lvm-setcallbackmask.md)

A maioria das mensagens de controle de exibição de lista e as macros associadas tem suporte total. No entanto, algumas mensagens têm limitações ou não têm suporte quando você usa o estilo [**LVS \_ OWNERDATA.**](list-view-window-styles.md) A tabela a seguir resume as mensagens afetadas.



| Mensagem                                             | Limitação                                                                                                                                                                                                                                                      |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LVM \_ ARRANGE**](lvm-arrange.md)                 | Não dá suporte ao **estilo \_ SNAPTOGRID da LVA.**                                                                                                                                                                                                                 |
| [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md)   | Define a contagem de itens como zero e limpa todas as variáveis de seleção internas, mas na verdade não exclui nenhum item. Ele faz um retorno de chamada de notificação.                                                                                                           |
| [**LVM \_ DELETEITEM**](lvm-deleteitem.md)           | Tem suporte apenas para integridade de seleção e não exclui um item.                                                                                                                                                                                 |
| [**LVM \_ GETITEMSTATE**](lvm-getitemstate.md)       | Retorna apenas os estados de foco e seleção (ou seja, os estados armazenados pelo controle de exibição de lista).                                                                                                                                                                |
| [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md)         | Não dá suporte aos critérios de pesquisa de exibição de lista **LVNI \_ CUT,** **LVNI \_ HIDDEN** ou **LVNI \_ DROPHILITED.** Todos os outros critérios têm suporte.                                                                                                                     |
| [**\_GETWORKAREAS LVM**](lvm-getworkareas.md)       | Não tem suporte.                                                                                                                                                                                                                                               |
| [**\_INSERTITEM LVM**](lvm-insertitem.md)           | Tem suporte apenas para integridade de seleção.                                                                                                                                                                                                                      |
| [**\_SETITEM LVM**](lvm-setitem.md)                 | Não tem suporte. Para definir o estado do item, use a mensagem [**ListView \_ SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .                                                                                                                                               |
| [**LVM \_ SETitemcount**](lvm-setitemcount.md)       | Define o número de itens atualmente na lista. Se o controle de exibição de lista enviar uma notificação que solicita dados de qualquer item até o conjunto máximo, o proprietário deverá estar preparado para fornecer esses dados. Os parâmetros de mensagem dão suporte a controles de exibição de lista virtual. |
| [**\_SETITEMPOSITION LVM**](lvm-setitemposition.md) | Não tem suporte.                                                                                                                                                                                                                                               |
| [**GetItemState do LVM \_**](lvm-setitemstate.md)       | Permite que apenas os Estados de seleção e foco sejam alterados para o item.                                                                                                                                                                                          |
| [**\_SETITEMTEXT LVM**](lvm-setitemtext.md)         | Não tem suporte. É responsabilidade do aplicativo manter os textos do item.                                                                                                                                                                            |
| [**\_SETWORKAREAS LVM**](lvm-setworkareas.md)       | Não tem suporte.                                                                                                                                                                                                                                               |
| [**\_SORTITEMS LVM**](lvm-sortitems.md)             | Não tem suporte. É responsabilidade do aplicativo apresentar os itens na ordem desejada.                                                                                                                                                             |



 

### <a name="handling-virtual-list-view-control-notification-codes"></a>Manipulando códigos de notificação de controle de List-View virtual

Os controles de exibição de lista com o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) enviam os mesmos códigos de notificação que outros controles de exibição de lista e dois outros: [LVN \_ ODCACHEHINT](lvn-odcachehint.md) e [LVN \_ ODFINDITEM](lvn-odfinditem.md). A seguir estão as notificações mais comuns que o controle de exibição de lista com o **estilo LVS \_ OWNERDATA** envia.



|      Notificação                    |     Descrição                         |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LVN \_ GETDISPINFO](lvn-getdispinfo.md) | Um controle de exibição de lista virtual mantém muito poucas informações de item por conta própria. Como resultado, ele geralmente envia o código de notificação [ \_ GETDISPINFO LVN](lvn-getdispinfo.md) para solicitar informações de item. Essa mensagem é tratada da mesma maneira que os itens de retorno de chamada em um controle de lista padrão. Como o número de itens com suporte pelo controle pode ser muito grande, o armazenamento em cache de dados de item melhora o desempenho. Ao lidar com LVN GETDISPINFO, o proprietário do controle tenta primeiro fornecer informações de item solicitadas do cache (para obter mais informações, consulte \_ Gerenciamento de [Cache](#cache-management)). Se o item solicitado não for armazenado em cache, o proprietário deverá estar preparado para fornecer as informações por outros meios. |
| [LVN \_ ODCACHEHINT](lvn-odcachehint.md) | Uma exibição de lista virtual envia o código de notificação [ \_ ODCACHEHINT LVN](lvn-odcachehint.md) para ajudar na otimização do cache. O código de notificação fornece valores de índice inclusivos para um intervalo de itens que ele recomenda que sejam armazenados em cache. Ao receber o código de notificação, o proprietário deve estar preparado para carregar o cache com informações de item para o intervalo solicitado para que as informações sejam prontamente disponíveis quando uma mensagem [ \_ GETDISPINFO LVN](lvn-getdispinfo.md) for enviada.                                                                                                                                                                                                                                   |
| [LVN \_ ODFINDITEM](lvn-odfinditem.md)   | O [código de notificação \_ ODFINDITEM LVN](lvn-odfinditem.md) é enviado por um controle de exibição de lista virtual quando o controle precisa que o proprietário localmente um item de retorno de chamada específico. O código de notificação é enviado quando o controle de exibição de lista recebe acesso rápido à chave ou quando recebe uma [**mensagem \_ FINDITEM LVM.**](lvm-finditem.md) As informações de pesquisa são enviadas na forma de uma estrutura [**LVFINDINFO,**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) que é membro da [**estrutura NMLVFINDITEM.**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) O proprietário deve estar preparado para pesquisar um item que corresponde às informações fornecidas pelo controle de exibição de lista. O proprietário retornará o índice do item se for bem-sucedido ou -1 se nenhum item correspondente for encontrado.               |



 

### <a name="cache-management"></a>Gerenciamento de cache

Um controle de exibição de lista com o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) produz um grande número de códigos de notificação [ \_ GETDISPINFO LVN](lvn-getdispinfo.md) e, para auxiliar na otimização do cache, [uma \_ mensagem LVN ODCACHEHINT.](lvn-odcachehint.md) \_Mensagens do LVN ODCACHEHINT fornecem informações sobre os itens recomendados a serem incluídos no cache. Essas mensagens são enviadas como mensagens de [**\_ notificação do WM**](wm-notify.md) , com o valor de *lParam* atuando como o endereço de uma estrutura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) .

A estrutura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) inclui dois membros inteiros, **iFrom** e **iTo**, que representam os pontos de extremidade inclusivos de um intervalo de itens que provavelmente serão necessários. O proprietário deve estar preparado para carregar o cache com as informações do item para cada um dos itens dentro do intervalo recomendado.

O controle de lista geralmente precisa de informações de item para o primeiro item (deslocamento 0). O código de notificação [LVN \_ ODCACHEHINT](lvn-odcachehint.md) talvez nem sempre inclua o item 0, mas ele sempre deve ser incluído no cache.

Os últimos itens da lista são acessados com frequência. Portanto, o proprietário talvez queira manter um segundo cache que inclui os itens no final da lista. O intervalo solicitado de [LVN \_ ODCACHEHINT](lvn-odcachehint.md) pode ser verificado no cache final para torná-lo disponível automaticamente em vez de recarregar o mesmo intervalo de término a cada vez.

## <a name="list-view-working-areas"></a>List-View áreas de trabalho

Os controles de exibição de lista dão suporte a áreas de trabalho, que são áreas virtuais retangulares que o controle de exibição de lista usa para organizar seus itens. Uma área de trabalho não é uma janela e não pode ter uma borda visível. Por padrão, o controle de exibição de lista não tem áreas de trabalho. Ao criar uma área de trabalho, você pode criar uma borda vazia à esquerda, à parte superior ou à direita dos itens ou fazer com que uma barra de rolagem horizontal seja exibida quando normalmente não haveria uma.

Quando uma área de trabalho é criada, os itens que residem na área de trabalho se tornam membros da área de trabalho. Da mesma forma, se um item for movido para uma área de trabalho, o item se tornará um membro dessa área de trabalho. Se um item não estiver em nenhuma área de trabalho, ele se tornará automaticamente um membro da primeira área de trabalho (índice 0). Para colocar o novo item em uma área de trabalho específica, primeiro você deve criar o item e, em seguida, usar a mensagem [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) ou [**LVM \_ SETITEMPOSITION32**](lvm-setitemposition32.md) para movê-lo para a área de trabalho desejada.

A ilustração a seguir é um exemplo de um controle de exibição de lista que contém quatro áreas de trabalho, cada uma em um quadrante diferente da área do cliente.

![captura de tela de um controle de exibição de lista com uma área de trabalho em cada quadrante da área do cliente](images/working.jpg)

Várias áreas de trabalho podem ser usadas para criar áreas diferentes em uma exibição. Você pode criar áreas em uma única exibição que têm significados diferentes. Por exemplo, uma exibição de um sistema de arquivos pode ter uma área para arquivos de leitura/gravação e outra área para arquivos somente leitura. O usuário pode categorizar itens colocando-os em diferentes áreas de trabalho. Se um arquivo for movido para a área somente leitura, ele se tornará automaticamente somente leitura.

Várias áreas de trabalho podem intersecção, mas todos os itens que estão dentro da interseção tornam-se membros da área com o índice inferior; portanto, é melhor evitar essa situação. Ao classificar várias áreas de trabalho, os itens são classificação em comparação com os outros itens na mesma área de trabalho.

O número de áreas de trabalho pode ser recuperado com a mensagem [**\_ GETNUMBEROFWORKAREAS LVM.**](lvm-getnumberofworkareas.md) As áreas de trabalho são alteradas com a mensagem [**LVM \_ SETWORKAREAS**](lvm-setworkareas.md) e podem ser recuperadas com a mensagem [**\_ GETWORKAREAS LVM.**](lvm-getworkareas.md) Ambas as mensagens levam o endereço de uma matriz de estruturas [**RECT**](/previous-versions//dd162897(v=vs.85)) como *o lParam* e o número de estruturas **RECT** como *o wParam*. Os membros **esquerdo** e **superior** dessas estruturas especificam as coordenadas do canto superior esquerdo (a origem) da área de trabalho e os membros **direito** e **inferior** especificam o canto inferior direito da área de trabalho. Todas as coordenadas estão nas coordenadas do cliente da exibição de lista. O número máximo de áreas de trabalho permitidas é definido pelo valor de **\_ \_ WORKAREAS Max LV** .

A alteração da área de trabalho não tem efeito nos controles de exibição de lista que têm a [**\_ lista de LVS**](list-view-window-styles.md) ou a exibição de [**\_ relatório LVS**](list-view-window-styles.md) , mas as áreas de trabalho serão mantidas quando o tipo de exibição for alterado. Com as exibições [**\_ ícone LVS**](list-view-window-styles.md) e [**LVS \_ SMALLICON**](list-view-window-styles.md) , a área de trabalho pode ser modificada para alterar a forma como os itens são exibidos. Tornar a largura da área de trabalho (direita esquerda) maior que a largura do cliente do controle faz com que os itens sejam encapsulados nessa largura e a barra de rolagem horizontal seja exibida. Tornar a largura da área de trabalho mais estreita do que a largura da área do cliente do controle faz com que os itens sejam encapsulados na área de trabalho e não na área do cliente. Definir o membro **esquerdo** ou **superior** como um valor positivo faz com que os itens sejam exibidos começando na área de trabalho, criando um espaço vazio entre a borda do controle e os itens. Um espaço vazio também pode ser criado entre a borda direita do controle e os itens, tornando a largura da área de trabalho menor que a largura do cliente do controle.

## <a name="list-view-image-lists"></a>List-View listas de imagens

Por padrão, um controle de exibição de lista não exibe imagens de item. Para exibir imagens de itens, você deve criar listas de imagens e associá-las ao controle. Um controle de exibição de lista pode ter três listas de imagens:

-   Uma lista de imagens que contém ícones de tamanho completo exibidos quando o controle está no modo de exibição de ícones.
-   Uma lista de imagens que contém ícones pequenos exibidos quando o controle está na exibição de ícones pequenos, na exibição de lista ou no modo de exibição de relatório.
-   Uma lista de imagens que contém imagens de estado, que são exibidas à esquerda do ícone de tamanho completo ou pequeno. Você pode usar imagens de estado, como caixas de seleção marcadas e des limpas, para indicar estados de item definidos pelo aplicativo. As imagens de estado são exibidas na exibição de ícone, exibição de ícone pequeno, exibição de lista e exibição de relatório.

As listas de imagens de ícone de tamanho completo e pequeno também podem conter imagens de sobreposição, que são projetadas para serem desenhadas de forma transparente sobre os ícones de item.

Para usar imagens de sobreposição em um controle de exibição de lista:

1.  Chame a [**função ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) para atribuir um índice de imagem de sobreposição a uma imagem nas listas de imagens de ícone pequeno e de tamanho completo. Uma imagem de sobreposição é identificada por um índice baseado em um.
2.  Você pode associar um índice de imagem de sobreposição a um item ao chamar a macro [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) ou [**ListView \_ SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) Use a [**macro INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) para especificar um  índice de imagem de sobreposição no membro de estado da estrutura [**LVITEM do**](/windows/win32/api/commctrl/ns-commctrl-lvitema) item. Você também deve definir os bits [**\_ OVERLAYMASK LVIS**](list-view-item-states.md) no **membro stateMask.**

Se uma lista de imagens de estado for especificada, um controle de exibição de lista reserva espaço à esquerda do ícone de cada item para uma imagem de estado.

Para associar uma imagem de estado a um item, use a macro [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) para especificar um índice de imagem de estado no membro de estado da [**estrutura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)  O índice identifica uma imagem na lista de imagens de estado do controle. Embora os índices de lista de imagens sejam baseados em zero, o controle usa índices baseados em um para identificar imagens de estado. Um índice de imagem de estado de zero indica que um item não tem nenhuma imagem de estado.

Por padrão, quando um controle de exibição de lista é destruído, ele destrói as listas de imagens atribuídas a ele. No entanto, se um controle de exibição de lista tiver o estilo de janela [**LVS \_ SHAREIMAGELISTS,**](list-view-window-styles.md) o aplicativo será responsável por destruir as listas de imagens quando elas não estão mais em uso. Você deve especificar esse estilo se atribuir as mesmas listas de imagens a vários controles de exibição de lista; caso contrário, mais de um controle poderá tentar destruir a mesma lista de imagens.

## <a name="list-view-items-and-subitems"></a>Itens de List-View e subitens

Cada item em um controle de exibição de lista tem um ícone, um rótulo, um estado atual e um valor definido pelo aplicativo. Usando mensagens de exibição de lista, você pode adicionar, modificar e excluir itens, bem como recuperar informações sobre itens.

Cada item pode ter um ou mais *subitens*. Um subitem é uma cadeia de caracteres que, na exibição de relatório, é exibida em uma coluna separada do ícone e do rótulo do item. Para especificar o texto de um subitem, use a mensagem [**LVM \_ SETITEMTEXT**](lvm-setitemtext.md) ou [**LVM \_ SETITEM**](lvm-setitem.md) . Todos os itens em um controle de exibição de lista têm o mesmo número de subitens. O número de subitens é determinado pelo número de colunas no controle de exibição de lista. Quando você adiciona uma coluna a um controle de exibição de lista, especifica seu índice de subitem associado.

A estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) define um item de exibição de lista ou subitem. O membro **iItem** é o índice de base zero do item. O membro **iSubItem** é o índice baseado em um de subitem ou zero se a estrutura contiver informações sobre um item. Membros adicionais especificam os dados de texto, ícone, estado e item do item. *Os dados do item* são um valor definido pelo aplicativo associado a um item de exibição de lista.

Para adicionar um item a um controle de exibição de lista, use a mensagem [**\_ INSERTITEM LVM**](lvm-insertitem.md) , especificando o endereço de uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Antes de adicionar vários itens, você pode enviar ao controle uma mensagem do [**LVM \_ setitemcount**](lvm-setitemcount.md) , especificando o número de itens que o controle terá, em última análise. Essa mensagem permite que o controle de exibição de lista realoque suas estruturas de dados internas apenas uma vez, em vez de cada vez que você adiciona um item. Você pode determinar o número de itens em um controle de exibição de lista usando a mensagem [**LVM \_ GetItemCount**](lvm-getitemcount.md) . Se você estiver adicionando um grande número de itens a um controle de exibição de lista, poderá acelerar o processo desabilitando o redesenho antes de adicionar os itens e, em seguida, habilitar o redesenho depois que os itens são adicionados. Use a [**mensagem WM \_ SETREDRAW**](/windows/desktop/gdi/wm-setredraw) para habilitar e desabilitar o redesenhar.

Para alterar os atributos de um item de exibição de lista, use a mensagem [**LVM \_ SETITEM,**](lvm-setitem.md) especificando o endereço de uma [**estrutura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) O **membro** de máscara dessa estrutura especifica os atributos de item que você deseja alterar. Por exemplo, para alterar apenas o texto de um item ou subitem, use a [**mensagem LVM \_ SETITEMTEXT.**](lvm-setitemtext.md)

Para recuperar informações sobre um item de exibição de lista, use a mensagem [**\_ GETITEM LVM,**](lvm-getitem.md) especificando o endereço da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) a ser preenchida. O **membro** de máscara dessa estrutura especifica os atributos de item a serem recuperados. Para recuperar apenas um item ou o texto do subitem, use a [**mensagem LVM \_ GETITEMTEXT.**](lvm-getitemtext.md)

Para excluir um item de exibição de lista, use a [**mensagem LVM \_ DELETEITEM.**](lvm-deleteitem.md) Você pode excluir todos os itens em um controle de exibição de lista usando a [**mensagem LVM \_ DELETEALLITEMS.**](lvm-deleteallitems.md)

### <a name="list-view-item-states"></a>List-View de item

O estado de um item é um valor que especifica a disponibilidade do item, indica ações do usuário ou, de outra forma, reflete o status do item. Um controle de exibição de lista altera alguns bits de estado, como quando o usuário seleciona um item. Um aplicativo pode alterar outros bits de estado para desabilitar ou ocultar o item ou especificar uma imagem de sobreposição ou imagem de estado. Para obter mais informações sobre imagens de sobreposição e imagens de estado, consulte [List-View Image Lists](#list-view-image-lists).

O estado de um item é especificado pelo membro **de** estado da [**estrutura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Quando você especifica ou altera o estado de um item, o membro **stateMask** especifica quais bits de estado você precisa alterar. Você pode alterar o estado de um item usando a [**mensagem LVM \_ SETITEMSTATE.**](lvm-setitemstate.md) Você pode especificar o estado de um item ao criá-lo ou ao alterar seus atributos usando a mensagem [**LVM \_ SETITEM**](lvm-setitem.md) . Para determinar o estado atual de um item, use a mensagem [**LVM \_ GetItemState**](lvm-getitemstate.md) ou [**LVM \_ GETITEM**](lvm-getitem.md) .

Para definir a imagem de sobreposição de um item, o membro **stateMask** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve incluir o valor [**LVIS \_ OVERLAYMASK**](list-view-item-states.md) e o membro de **estado** deve incluir o índice baseado em um da imagem de sobreposição deslocada 8 bits à esquerda usando a macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) . O índice pode ser zero para não especificar nenhuma imagem de sobreposição.

Para definir a imagem de estado de um item, o membro **stateMask** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve incluir o valor [**LVIS \_ STATEIMAGEMASK**](list-view-item-states.md) e o membro de **estado** deve incluir o índice baseado em um da imagem de estado deslocada 12 bits para a esquerda usando a macro [**INDEXTOSTATEIMAGEMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextostateimagemask) . O índice pode ser zero para não especificar nenhuma imagem de estado.

### <a name="callback-items-and-the-callback-mask"></a>Itens e máscara de retorno de chamada

Para cada um de seus itens, um controle de exibição de lista normalmente armazena o texto do rótulo, o índice da lista de imagens dos ícones do item e um conjunto de sinalizadores de bits para o estado do item. Você pode definir itens de retorno de chamada ou alterar a máscara de retorno de chamada do controle para indicar que o aplicativo, em vez do controle, armazena algumas ou todas essas informações. Talvez você queira usar retornos de chamada se o aplicativo armazenar algumas dessas informações.

Um *item de retorno de chamada* em um controle de exibição de lista é um item para o qual o aplicativo armazena o índice de texto ou ícone, ou ambos. Você pode definir itens de retorno de chamada ao enviar a mensagem [**\_ INSERTITEM LVM**](lvm-insertitem.md) para adicionar um item ao controle de exibição de lista. Se o aplicativo armazenar o texto para o item ou subitem, defina o membro **pszText** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) do item como **LPSTR \_ textcallback**. Se o aplicativo armazenar o índice de ícone de um item, de definir o membro **iImage** da estrutura **LVITEM** do item como **I \_ IMAGECALLBACK.**

A *máscara de retorno de* chamada de um controle de exibição de lista é um conjunto de sinalizadores de bits que especificam os estados de item para os quais o aplicativo, em vez do controle, armazena os dados atuais. A máscara de retorno de chamada se aplica a todos os itens do controle, ao contrário da designação de item de retorno de chamada, que se aplica a um item específico. A máscara de retorno de chamada é zero por padrão, o que significa que o controle de exibição de lista armazena todas as informações de estado do item. Depois de criar um controle de exibição de lista e inicializar seus itens, você pode enviar a mensagem [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) para alterar a máscara de retorno de chamada. Para recuperar a máscara de retorno de chamada atual, envie a [**mensagem \_ GETCALLBACKMASK LVM.**](lvm-getcallbackmask.md)

Quando um controle de exibição de lista deve exibir ou classificar um item de exibição de lista para o qual o aplicativo armazena informações de retorno de chamada, o controle envia o código de notificação [ \_ GETDISPINFO LVN](lvn-getdispinfo.md) para a janela pai do controle. Essa mensagem especifica uma estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) que contém o tipo de informação necessária e identifica o item ou subitem a ser recuperado. A janela pai deve processar LVN \_ GETDISPINFO para fornecer os dados solicitados.

Se o controle de exibição de lista detectar uma alteração nas informações de retorno de chamada de um item, como uma alteração nas informações de texto, ícone ou estado, o controle enviará um código de notificação [LVN \_ SETDISPINFO](lvn-setdispinfo.md) para notificá-lo sobre a alteração.

Se você alterar os atributos ou os bits de estado de um item de retorno de chamada, use a mensagem [**UPDATE do \_ LVM**](lvm-update.md) para forçar o controle a repintar o item. Essa mensagem também faz com que o controle organize seus itens se ele tiver o [**estilo LVS \_ AUTOARRANGE.**](list-view-window-styles.md) Você pode usar a mensagem [**LVM \_ REDRA LISTEMS**](lvm-redrawitems.md) para redesenhar um intervalo de itens invalidando as partes correspondentes da área de cliente do controle de exibição de lista.

Usando efetivamente os itens de retorno de chamada e a máscara de retorno de chamada, você pode garantir que cada atributo de item seja mantido em apenas um local. Fazer isso pode simplificar seu aplicativo, mas o único espaço salvo é a memória que, de outra forma, seria necessária para armazenar rótulos de item e texto de subitem.

### <a name="list-view-item-position"></a>Posição do item de List-View

Cada item de exibição de lista tem uma posição e um tamanho, que você pode recuperar e definir usando mensagens. Você também pode determinar qual item, se houver, está em uma posição especificada. A posição dos itens de exibição de lista é especificada em *coordenadas de exibição*, que são deslocamento de coordenadas de cliente pela posição de rolagem.

Para recuperar e definir a posição de um item, use as mensagens [**LVM \_ GETITEMPOSITION**](lvm-getitemposition.md) e [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) . **LVM \_ O GETITEMPOSITION** funciona para todas as exibições, mas o **LVM \_ SETITEMPOSITION** funciona apenas para exibições de ícone e ícone pequeno.

Você pode determinar qual item, se houver, está em um local específico usando a mensagem do [**LVM \_ HITTEST**](lvm-hittest.md) .

Para recuperar o retângulo delimitador para um item de lista ou apenas para seu ícone ou rótulo, use a mensagem [**LVM \_ GETITEMRECT**](lvm-getitemrect.md) .

### <a name="arranging-sorting-and-finding-items"></a>Organizando, classificando e localizando itens

Você pode usar as mensagens de exibição de lista para organizar e classificar itens e para localizar itens com base em seus atributos ou posições. Organizar os itens de reposicionamento para alinhar em uma grade, mas os índices dos itens não são alterados. A classificação altera a sequência de itens (e seus índices correspondentes) e os reposiciona adequadamente. Você pode organizar itens somente em exibições de ícone e ícone pequeno, mas pode classificar itens em qualquer modo de exibição. Para localizar itens, você envia mensagens de exibição de lista que especificam um local ou uma propriedade do item.

Para organizar itens, use a mensagem de [**\_ organização do LVM**](lvm-arrange.md) . Você pode garantir que os itens sejam organizados em todos os momentos, especificando o estilo de janela de [**\_ AutoOrganizar LVS**](list-view-window-styles.md) .

Para classificar itens, use a mensagem [**LVM \_ SORTITEMS**](lvm-sortitems.md) . Ao classificar usando essa mensagem, você especifica uma função de retorno de chamada definida pelo aplicativo que o controle de exibição de lista chama para comparar a ordem relativa de qualquer dois itens. O controle passa para a função de comparação os dados de item associados a cada um dos dois itens. Os dados do item são o valor especificado no membro **lParam** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) do item quando eles foram inseridos na lista. Especificando os dados de item apropriados e fornecendo uma função de comparação apropriada, você pode classificar itens por seu rótulo, por qualquer subitem ou por qualquer outra propriedade. Observe que a classificação de itens não reordena os subitens correspondentes. Quando os itens são reordenados, seus subitens correspondentes são carregados com eles; ou seja, linhas inteiras são mantidas juntas. Para ordenar as colunas separadamente umas das outras, desconectando os subitens de seus itens, você deve regenerar as colunas após a classificação usando [**LVM \_ SETITEM**](lvm-setitem.md).

Você pode garantir que um controle de exibição de lista sempre seja classificação especificando o estilo de janela [**LVS \_ SORTASCENDING**](list-view-window-styles.md) ou [**LVS \_ SORTDESCENDING.**](list-view-window-styles.md) Os controles com esses estilos usam o texto de rótulo dos itens para classiá-los em ordem crescente ou decrescente. Não é possível fornecer uma função de comparação ao usar esses estilos de janela. Se um controle de exibição de lista tiver qualquer um desses estilos, uma mensagem [**LVM \_ INSERTITEM**](lvm-insertitem.md) falhará se você tentar inserir um item que tenha **LPSTR \_ TEXTCALLBACK** como o membro **pszText** de sua estrutura [**LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

Você pode encontrar um item de exibição de lista com propriedades específicas usando a [**mensagem LVM \_ FINDITEM.**](lvm-finditem.md) Você pode encontrar um item de exibição de lista que está em um estado especificado e tem uma relação especificada com um determinado item usando a mensagem [**\_ GETNEXTITEM LVM.**](lvm-getnextitem.md) Por exemplo, você pode recuperar o próximo item selecionado à direita de um item especificado.

## <a name="list-view-columns"></a>List-View colunas

As colunas controlam a maneira como os itens e seus subitens são exibidos no modo de exibição de relatório. Cada coluna tem um título e uma largura e está associada a um subitem específico; o subitem zero é o ícone e o rótulo do item. Os atributos de uma coluna são definidos por uma estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) .

Para adicionar uma coluna a um controle de exibição de lista, use a mensagem [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) . Para excluir uma coluna, use a mensagem [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) .

> [!Note]  
> A exclusão de coluna zero de um controle de exibição de lista tem suporte apenas no ComCtl32.dll versão 6 e posterior. A versão 5 também dá suporte à exclusão de coluna zero, mas somente depois de usar [**CCM \_ SetVersion**](ccm-setversion.md) para definir a versão como 5 ou posterior. As versões anteriores à versão 5 não dão suporte à exclusão de coluna zero.

 

Você pode recuperar e alterar as propriedades de uma coluna existente usando as mensagens [**LVM \_ GetColumn**](lvm-getcolumn.md) e [**LVM \_ SetColumn**](lvm-setcolumn.md) . Para recuperar ou alterar a largura de uma coluna, use as mensagens [**LVM \_ GETCOLUMNWIDTH**](lvm-getcolumnwidth.md) e [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) .

A menos que o estilo de janela [**LVS \_ nocolumnheader**](list-view-window-styles.md) seja especificado, os cabeçalhos de coluna aparecerão na exibição de relatório. O usuário pode clicar em um cabeçalho de coluna, fazendo com que um código de notificação [**LVN \_ COLUMNCLICK**](lvn-columnclick.md) seja enviado para a janela pai. Normalmente, a janela pai classifica o controle de exibição de lista pela coluna especificada quando esse clique ocorre. O usuário também pode arrastar os guias de coluna entre os cabeçalhos para dimensionar as colunas.

Os controles de exibição de lista podem exibir imagens ao lado de títulos de coluna. Para implementar esse recurso, especifique o valor da **\_ imagem LVCF** e atribua o índice da imagem ao membro **iImage** na estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) .

Os controles de exibição de lista podem definir a ordem na qual as colunas são exibidas. Para implementar esse recurso, especifique o valor do **\_ pedido LVCF** e atribua a ordem da coluna ao membro **iOrder** na estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) . A ordem da coluna é baseada em zero e está na ordem da esquerda para a direita. Por exemplo, zero indica a coluna mais à esquerda.

## <a name="list-view-scroll-position"></a>List-View posição de rolagem

A menos que o estilo da janela [**\_ LVS NOSCROLL**](list-view-window-styles.md) seja especificado, um controle de exibição de lista pode ser rolado para mostrar mais itens do que pode caber na área de cliente do controle. Você pode recuperar a posição de rolagem e as informações relacionadas de um controle de exibição de lista, rolar um controle de exibição de lista por uma quantidade especificada ou rolar um controle de exibição de lista para que um item de lista especificado seja visível.

Na exibição de ícone ou exibição de ícone pequeno, a posição de rolagem atual é definida pela *origem da exibição*. A origem da exibição é o conjunto de coordenadas, em relação à área visível do controle de exibição de lista, que correspondem às coordenadas de exibição (0, 0). Para recuperar a origem da exibição atual, use a [**mensagem \_ GETORIGIN LVM.**](lvm-getorigin.md) Essa mensagem deve ser usada somente no ícone ou na exibição de ícone pequeno; ele retorna um erro na exibição de lista ou relatório.

Na exibição de lista ou relatório, a posição de rolagem atual é definida pelo *índice superior.* O índice superior é o índice do primeiro item visível no controle de exibição de lista. Para recuperar o índice superior atual, use a [**mensagem \_ GETTOPINDEX LVM.**](lvm-gettopindex.md) Essa mensagem retorna um resultado válido somente na exibição de lista ou relatório; ele retorna zero no ícone ou exibição de ícone pequeno.

Você pode usar a mensagem [**\_ GETVIEWRECT LVM**](lvm-getviewrect.md) para recuperar o retângulo delimitador de todos os itens em um controle de exibição de lista, em relação à área visível do controle.

A [**mensagem \_ GETCOUNTPERPAGE do LVM**](lvm-getcountperpage.md) retorna o número de itens que cabem em uma página do controle de exibição de lista. Essa mensagem retorna um resultado válido somente nas exibições de lista e relatório; em exibições de ícone e ícone pequeno, ele retorna o número total de itens.

Para rolar um controle de exibição de lista por um valor específico, use a [**mensagem SCROLL \_ LVM.**](lvm-scroll.md) Usando a mensagem [**LVM \_ ENSUREVISIBLE**](lvm-ensurevisible.md) , você pode rolar o controle de exibição de lista, se necessário, para garantir que um item especificado esteja visível.

## <a name="list-view-label-editing"></a>Edição de rótulo de List-View

Um controle de exibição de lista que tem o estilo de janela [**LVS \_ EDITLABELS**](list-view-window-styles.md) permite que um usuário edite rótulos de item no local. O usuário começa a editar clicando no rótulo de um item que tem o foco. Como alternativa, um aplicativo pode começar a ser editado automaticamente usando a mensagem [**LVM \_ EDITLABEL**](lvm-editlabel.md) . O controle List-View notifica a janela pai quando a edição começa e quando é cancelada ou concluída. Quando a edição for concluída, a janela pai será responsável por atualizar o rótulo do item, se apropriado.

Quando o rótulo é iniciado, um [controle de edição](edit-controls.md) é criado, posicionado e inicializado. Antes de ser exibida, o controle List-View envia à janela pai um código de notificação [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) . Se você precisar modificar o processo de edição de rótulo, poderá implementar um manipulador para essa notificação.

Um uso para um manipulador de notificação [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) é controlar quais rótulos o usuário pode editar. Para impedir a edição do rótulo, retorne um valor diferente de zero. Para personalizar a edição de rótulo, faça com que o manipulador de notificação recupere um identificador para o controle de edição enviando uma mensagem [**LVM \_ GETEDITCONTROL**](lvm-geteditcontrol.md) para o controle de exibição de lista. Quando você tiver esse identificador, poderá personalizar o controle de edição enviando as mensagens usuais em \_ xxx. Por exemplo, para limitar a quantidade de texto que um usuário pode inserir, envie o controle de edição uma mensagem em [**\_ LIMITTEXT**](em-limittext.md) . Você pode alterar o texto padrão do controle de edição com [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta). Você pode até mesmo subclasse do controle de edição para interceptar e descartar caracteres inválidos.

Quando a edição de rótulo é cancelada ou concluída, um controle de exibição de lista envia sua janela pai um código de notificação [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) . O *parâmetro lParam* é o endereço de uma [**estrutura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) O **membro** do item dessa estrutura é uma [**estrutura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cujo membro **iItem** identifica o item. Se a edição for cancelada, o **membro pszText** da estrutura **LVITEM** será **NULL**; caso contrário, **pszText** é o endereço do texto editado. A janela pai será responsável por atualizar o rótulo do item se quiser manter o novo rótulo.

## <a name="list-view-colors"></a>List-View cores

Um aplicativo pode recuperar e definir três cores para um controle de exibição de lista.



| Color                   | Mensagens usadas para recuperar e definir cores                                                             |
|-------------------------|------------------------------------------------------------------------------------------------------|
| Cor do texto              | [**LVM \_ GETTEXTCOLOR**](lvm-gettextcolor.md), [ **LVM \_ SETTEXTCOLOR**](lvm-settextcolor.md)         |
| Cor da tela de fundo do texto   | [**LVM \_ GETTEXTBKCOLOR,**](lvm-gettextbkcolor.md) [ **LVM \_ SETTEXTBKCOLOR**](lvm-settextbkcolor.md) |
| Cor da tela de fundo da janela | [**LVM \_ GETBKCOLOR,**](lvm-getbkcolor.md) [ **LVM \_ SETBKCOLOR**](lvm-setbkcolor.md)                 |



 

Para personalizar a aparência de um controle de exibição de lista mais significativamente, use [NM \_ CUSTOMDRAW (exibição](nm-customdraw-list-view.md) de lista) ou use estilos visuais (consulte [Estilos](themes-overview.md) visuais e Habilitando [estilos visuais).](cookbook-overview.md)

## <a name="arranging-list-items-by-group"></a>Organizando itens de lista por grupo

Os recursos de agrupamento do controle de exibição de lista permitem agrupar visualmente conjuntos de itens relacionados logicamente. Os grupos podem ser criados com base em propriedades de item, atributos ou outras características. Esses grupos normalmente são separados na tela por um header horizontal que contém o nome do grupo. A captura de tela a seguir mostra itens agrupados.

![captura de tela de um controle de exibição de lista, com cachorros em um grupo e gatos em outro grupo](images/lv-groups.png)

Você usa a [**estrutura LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) para armazenar informações sobre um grupo, como o texto de rodapé e de rodapé, o estado atual do grupo e assim por diante. A API de agrupamento inclui mensagens que permitem que você gerencie grupos e elementos de grupo adicionando itens a grupos, adicionando grupos a exibições, classificando itens de grupo e consultando grupos de tamanho de item e outras informações. Por exemplo, você pode definir e recuperar parâmetros de exibição para cada grupo usando as macros [**ListView \_ SetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupmetrics) e [**ListView \_ GetGroupMetrics**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupmetrics) .

O agrupamento está disponível em todas as exibições, exceto na exibição de lista. Ele não está disponível em controles que têm o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .

Para obter mais informações, consulte [usando controles de List-View](using-list-view-controls.md).

## <a name="insertion-marks"></a>Marcas de inserção

Marcas de inserção mostram os usuários em que os itens arrastados serão colocados. As marcas de inserção são exibidas no momento quando o usuário arrasta um item para o menu **Iniciar** ou para a barra de início rápido. A marca de inserção também funciona para listas que são definidas como AutoOrganizar. Quando um usuário arrasta um item para um ponto entre dois outros itens, a marca de inserção mostra o novo local esperado do item. A captura de tela a seguir mostra uma marca de inserção.

![captura de tela que mostra uma marca de inserção ao arrastar um arquivo entre dois outros em um controle de exibição de lista](images/insertmark.png)

Os elementos da API de marca de inserção habilitam o posicionamento de marcas de inserção, fornecendo mensagens e sinalizadores que executam a detecção de ocorrências, que especificam o local e a aparência da marca de inserção por item, e essa consulta para obter informações sobre o tamanho atual e a aparência da marca de inserção.

## <a name="see-also"></a>Confira também

* [Exemplo de controle ListView virtual](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)
