---
title: Sobre controles de header
description: Um controle de header é uma janela que geralmente é posicionada acima de colunas de texto ou números. Ele contém um título para cada coluna e pode ser dividido em partes.
ms.assetid: b464fb9a-e342-4209-ba6f-15b5388f3914
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6308def8c760ffab492d7aeea086970740be07ebd559d94791baf3512c178b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412254"
---
# <a name="about-header-controls"></a>Sobre controles de header

Um controle de header é uma janela que geralmente é posicionada acima de colunas de texto ou números. Ele contém um título para cada coluna e pode ser dividido em partes. O usuário pode arrastar os divisores que separam as partes para definir a largura de cada coluna. A ilustração a seguir mostra um controle de título que tem colunas rotuladas que dão informações detalhadas sobre arquivos em um diretório.

![captura de tela de uma caixa de diálogo com um controle de header de três colunas](images/header.png)

Você pode criar um controle de título usando a função [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especificando a classe de janela [**\_ HEADER**](common-control-window-classes.md) do WC e os Estilos de Controle [de Título apropriados.](header-control-styles.md) Essa classe de janela é registrada quando a DLL de controle comum é carregada. Para garantir que essa DLL seja carregada, use a [**função InitCommonControlsEx.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) Depois de criar um controle de header, você pode dividi-lo em partes, definir o texto em cada parte e controlar a aparência da janela usando mensagens de janela de header.

Um controle de header pode ser criado como uma janela filho de outro controle, como uma caixa de listagem. No entanto, o controle pai não está ciente do controle de header e não permite o espaço gasto pelo header, com o resultado que os itens de lista aparecerão atrás do header. Se você quiser usar um controle de header em uma caixa de listagem ou outro controle, o controle pai deverá ser desenhado pelo proprietário para que todos os itens sejam exibidos na posição correta.

Os controles de exibição de lista já têm controles de header. Em vez de criar um controle de header para um controle de exibição de lista, use [**LVM \_ GETHEADER**](lvm-getheader.md) ou [**ListView \_ GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) para recuperar o controle existente.

-   [Tamanho e posição do controle de cabeça](#header-control-size-and-position)
-   [Itens](#items)
-   [Controles de header desenhados pelo proprietário](#owner-drawn-header-controls)
-   [Filtros de controle de cabeça](#header-control-filters)
-   [Processamento de mensagem de controle de header padrão](#default-header-control-message-processing)

## <a name="header-control-size-and-position"></a>Tamanho e posição do controle de cabeça

Normalmente, você deve definir o tamanho e a posição de um controle de cabeça para se ajustar dentro dos limites de um retângulo específico, como a área do cliente de uma janela. Usando a mensagem [**\_ LAYOUT do HDM,**](hdm-layout.md) você pode recuperar os valores de posição e tamanho apropriados do controle de header.

Ao enviar [**\_ o LAYOUT do HDM,**](hdm-layout.md)especifique o endereço de uma estrutura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) que contém as coordenadas do retângulo que o controle de cabeça deve ocupar e fornece um ponteiro para uma estrutura [**WINDOWPOS.**](/windows/win32/api/winuser/ns-winuser-windowpos) O controle preenche a estrutura **WINDOWPOS** com valores de tamanho e posição apropriados para posicionar o controle ao longo da parte superior do retângulo especificado. O valor de altura é a soma das alturas das bordas horizontais do controle e a altura média dos caracteres na fonte atualmente selecionada no contexto do dispositivo do controle.

Se você quiser usar [**\_ o LAYOUT do HDM**](hdm-layout.md) para definir o tamanho inicial e a posição de um controle de cabeça, de definir o estado de visibilidade inicial do controle para que ele seja ocultado. Depois de **enviar o LAYOUT \_ do HDM** para recuperar os valores de tamanho e posição, você pode usar a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para definir o novo tamanho, posição e estado de visibilidade.

## <a name="items"></a>Itens

Um controle de header normalmente tem vários itens de cabeça que definem as colunas do controle. Você adiciona um item a um controle de header enviando a mensagem [**\_ INSERTITEM do HDM**](hdm-insertitem.md) para o controle. A mensagem inclui o endereço de uma [**estrutura HDITEM.**](/windows/win32/api/commctrl/ns-commctrl-hditema) Essa estrutura define as propriedades do item de header, que podem incluir uma cadeia de caracteres, uma imagem mapeada, um tamanho inicial e um valor **LPARAM** definido pelo aplicativo.

O **membro fmt** da estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) de um item pode incluir o sinalizador **HDF \_ STRING** ou **\_ HDF BITMAP** para indicar se o controle exibe a cadeia de caracteres ou bitmap do item. Se você quiser exibir uma cadeia de caracteres e um bitmap, crie um item desenhado pelo proprietário definindo o membro **fmt** para incluir o sinalizador **HDF \_ OWNERDRAW.** A **estrutura HDITEM** também especifica sinalizadores de formatação que determinam se o controle deve ser central, alinhado à esquerda ou alinhado à direita da cadeia de caracteres ou bitmap no retângulo do item.

[**HDM \_ INSERTITEM**](hdm-insertitem.md) retorna o índice do item recém-adicionado. Você pode usar o índice em outras mensagens para definir propriedades ou recuperar informações sobre o item. Você pode excluir um item usando a mensagem [**\_ DELETEITEM do HDM,**](hdm-deleteitem.md) especificando o índice do item a ser excluído.

Você pode usar a mensagem [**\_ SETITEM**](hdm-setitem.md) do HDM para definir as propriedades de um item de header existente e a mensagem [**\_ GETITEM do HDM**](hdm-getitem.md) para recuperar as propriedades atuais de um item. Para recuperar uma contagem dos itens em um controle de header, use a mensagem [**\_ HDM GETITEMCOUNT.**](hdm-getitemcount.md)

## <a name="owner-drawn-header-controls"></a>Owner-Drawn controles de header

Você pode definir itens individuais de um controle de header para serem itens desenhados pelo proprietário. O uso dessa técnica oferece mais controle do que você teria sobre a aparência de um item de header.

Você pode usar a mensagem [**\_ INSERTITEM**](hdm-insertitem.md) do HDM para inserir um novo item desenhado pelo proprietário em um controle de header ou a mensagem [**\_ SETITEM**](hdm-setitem.md) do HDM para alterar um item existente para um item desenhado pelo proprietário. Ambas as mensagens incluem o endereço de uma estrutura [**HDITEM,**](/windows/win32/api/commctrl/ns-commctrl-hditema) que deve ter o membro **fmt** definido como o **valor \_ OWNERDRAW do HDF.**

Quando um controle de cabeça deve desenhar um item desenhado pelo proprietário, ele envia a mensagem [**WM \_ DRAWITEM**](wm-drawitem.md) para a janela pai. O *parâmetro wParam* da mensagem é o identificador de janela filho do controle de título e o parâmetro *lParam* é um endereço de uma [**estrutura DRAWITEMSTRUCT.**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) A janela pai usa as informações na estrutura para desenhar o item. Para um item desenhado pelo proprietário em um controle de header, a estrutura **DRAWITEMSTRUCT** contém as informações a seguir.



| Membro         | DESCRIÇÃO                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | [**ODT \_ Tipo de controle desenhado**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) pelo proprietário do HEADER.                                                                                        |
| **CtlID**      | Identificador de janela filho do controle de header.                                                                                                         |
| **Itemid**     | Índice do item a ser desenhado.                                                                                                                         |
| **Itemaction** | [**ODA \_ Sinalizador de ação**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) de desenho DRAWENTIRE.                                                                                         |
| **Itemstate**  | [**ODS \_ Sinalizador**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) de ação de desenho SELECIONADO se o cursor estiver no item e o botão do mouse estiver ino mouse. Caso contrário, esse membro será zero. |
| **hwndItem**   | Lidar com o controle de header.                                                                                                                          |
| **Hdc**        | Lidar com o contexto do dispositivo do controle de header.                                                                                                    |
| **rcItem**     | Coordenadas do item de cabeça a ser desenhado. As coordenadas são relativas ao canto superior esquerdo do controle de cabeça.                               |
| **Itemdata**   | Valor de 32 bits definido pelo aplicativo associado ao item.                                                                                             |



 

## <a name="header-control-filters"></a>Filtros de controle de cabeça

Ao especificar o estilo de janela [**\_ FILTERBAR**](header-control-styles.md) do HDS para um controle de título, você pode habilitar o posicionamento das caixas de edição de filtro sob os títulos de coluna. Um botão de filtro é exibido ao lado da caixa de edição. Você pode implementar a filtragem respondendo aos códigos de notificação [HDN \_ BEGINFILTEREDIT](hdn-beginfilteredit.md), [HDN \_ ENDFILTEREDIT,](hdn-endfilteredit.md) [HDN \_ FILTERBTNCLICK](hdn-filterbtnclick.md)ou [HDN \_ FILTERCHANGE.](hdn-filterchange.md)

Por padrão, a caixa de edição contém um prompt para o usuário inserir texto. Você pode restaurar a caixa de edição para esse estado padrão usando [**Header \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) ou [**\_ Header ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters).

O exemplo de código a seguir mostra como recuperar o controle de header de um controle de exibição de lista e adicionar uma barra de filtros.


```
// hList is the HWND of the list-view control.
HWND hHeader = ListView_GetHeader(hList);
LONG_PTR styles = GetWindowLongPtr(hHeader, GWL_STYLE);
SetWindowLongPtr(g_hHeader, GWL_STYLE, styles | HDS_FILTERBAR);
```



## <a name="default-header-control-message-processing"></a>Processamento de mensagem de controle de header padrão

Esta seção descreve as mensagens de janela manipuladas pelo procedimento de janela para a [**classe de janela \_ HEADER do WC.**](common-control-window-classes.md)



| Mensagem                                            | Processamento executado                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                 | Inicializa o controle de header.                                                                                                                                                                                                                                                                               |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)               | Não reinicializa o controle de header.                                                                                                                                                                                                                                                                             |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)         | Preenche a tela de fundo do controle de header usando a cor da tela de fundo atual do controle.                                                                                                                                                                                                                      |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)         | Retorna uma combinação dos valores [**\_ WANTTAB e**](/windows/desktop/dlgbox/wm-getdlgcode) [**DLGC \_ WANTARROWS do DLGC.**](/windows/desktop/dlgbox/wm-getdlgcode)                                                                                                                     |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Retorna o alça para a fonte atual, que é usada pelo controle de header para desenhar seu texto.                                                                                                                                                                                                                 |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) | Captura a entrada do mouse. Se o cursor do mouse estiver em um divisor, o controle enviará o código de notificação [ \_ BEGINTRACK](hdn-begintrack.md) do HDN e começará a arrastar o divisor. Se o cursor estiver em um item, o item será exibido no estado pressionado.                                                            |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | O mesmo que [**a mensagem WM \_ LBUTTONDBLCLK.**](/windows/desktop/inputdev/wm-lbuttondblclk)                                                                                                                                                                                                                                       |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)         | Libera a captura do mouse. Se o controle estava acompanhando a movimentação do mouse, ele envia o código de notificação [ \_ DO HDN ENDTRACK](hdn-endtrack.md) e redesenha o controle de header. Caso contrário, o controle envia o código de notificação [ \_ ITEMCLICK](hdn-itemclick.md) do HDN e redesenha o item de header que foi clicado. |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)         | Se um divisor estiver sendo arrastado, o controle enviará o código de notificação [ \_ HDN TRACK](hdn-track.md) e exibirá o item na nova posição. Se o botão esquerdo do mouse estiver ino mouse e o cursor estiver em um item, o item será exibido no estado pressionado.                                                      |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)             | Aloca e inicializa uma estrutura de dados interna.                                                                                                                                                                                                                                                         |
| [**WM \_ NCDESTROY**](/windows/desktop/winmsg/wm-ncdestroy)           | Libera os recursos alocados pelo controle de header depois que o controle de header não é reinicializado.                                                                                                                                                                                                                |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                      | Pinta a região inválida do controle de header. Se o *parâmetro wParam* for não NULL, o controle assumirá que o valor é um HDC e pintará usando esse contexto de dispositivo.                                                                                                                                    |
| [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor)           | Define a forma do cursor, dependendo se o cursor está em um divisor ou em um item de header.                                                                                                                                                                                                                   |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)               | Seleciona um novo alça de fonte no contexto do dispositivo para o controle de header.                                                                                                                                                                                                                                     |



 

 

 