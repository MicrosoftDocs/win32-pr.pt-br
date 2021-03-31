---
title: Sobre controles de cabeçalho
description: Um controle de cabeçalho é uma janela que geralmente é posicionada acima das colunas de texto ou números. Ele contém um título para cada coluna e pode ser dividido em partes.
ms.assetid: b464fb9a-e342-4209-ba6f-15b5388f3914
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d9beaa9dc3bd8eb94d749ec271902a480b853e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641875"
---
# <a name="about-header-controls"></a>Sobre controles de cabeçalho

Um controle de cabeçalho é uma janela que geralmente é posicionada acima das colunas de texto ou números. Ele contém um título para cada coluna e pode ser dividido em partes. O usuário pode arrastar os divisores que separam as partes para definir a largura de cada coluna. A ilustração a seguir mostra um controle de cabeçalho com colunas rotuladas que fornecem informações detalhadas sobre os arquivos em um diretório.

![captura de tela de uma caixa de diálogo com um controle de cabeçalho de três colunas](images/header.png)

Você pode criar um controle de cabeçalho usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe da janela de [**\_ cabeçalho WC**](common-control-window-classes.md) e os [estilos de controle de cabeçalho](header-control-styles.md)apropriados. Essa classe de janela é registrada quando a DLL de controle comum é carregada. Para garantir que essa DLL seja carregada, use a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) . Depois de criar um controle de cabeçalho, você pode dividi-lo em partes, definir o texto em cada parte e controlar a aparência da janela usando mensagens de janela de cabeçalho.

Um controle de cabeçalho pode ser criado como uma janela filho de outro controle, como uma caixa de listagem. No entanto, o controle pai não está ciente do controle de cabeçalho e não permite o espaço ocupado pelo cabeçalho, com o resultado que os itens de lista aparecerão atrás do cabeçalho. Se você quiser usar um controle de cabeçalho em uma caixa de listagem ou outro controle, o controle pai deverá ser desenhado pelo proprietário para que todos os itens sejam exibidos na posição correta.

Controles de exibição de lista já têm controles de cabeçalho. Em vez de criar um controle de cabeçalho para um controle de exibição de lista, você usa o [**LVM \_ GetHeader**](lvm-getheader.md) ou [**ListView \_ GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) para recuperar o controle existente.

-   [Tamanho e posição do controle de cabeçalho](#header-control-size-and-position)
-   [Itens](#items)
-   [Controles de cabeçalho de desenho proprietário](#owner-drawn-header-controls)
-   [Filtros de controle de cabeçalho](#header-control-filters)
-   [Processamento de mensagens de controle de cabeçalho padrão](#default-header-control-message-processing)

## <a name="header-control-size-and-position"></a>Tamanho e posição do controle de cabeçalho

Normalmente, você deve definir o tamanho e a posição de um controle de cabeçalho para se ajustar nos limites de um retângulo específico, como a área de cliente de uma janela. Usando a mensagem [**de \_ layout HDM**](hdm-layout.md) , você pode recuperar os valores de tamanho e posição apropriados do controle de cabeçalho.

Ao enviar [**o \_ layout HDM**](hdm-layout.md), você especifica o endereço de uma estrutura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) que contém as coordenadas do retângulo que o controle de cabeçalho deve ocupar e fornece um ponteiro para uma estrutura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) . O controle preenche a estrutura **WINDOWPOS** com valores de tamanho e posição apropriados para posicionar o controle ao longo da parte superior do retângulo especificado. O valor de altura é a soma das alturas das bordas horizontais do controle e a altura média de caracteres na fonte selecionada atualmente no contexto do dispositivo do controle.

Se você quiser usar o [**\_ layout HDM**](hdm-layout.md) para definir o tamanho inicial e a posição de um controle de cabeçalho, defina o estado de visibilidade inicial do controle para que ele fique oculto. Depois de enviar o **\_ layout HDM** para recuperar os valores de tamanho e posição, você pode usar a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para definir o novo tamanho, a posição e o estado de visibilidade.

## <a name="items"></a>Itens

Um controle de cabeçalho normalmente tem vários itens de cabeçalho que definem as colunas do controle. Você adiciona um item a um controle de cabeçalho enviando a mensagem [**HDM \_ INSERTITEM**](hdm-insertitem.md) para o controle. A mensagem inclui o endereço de uma estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Essa estrutura define as propriedades do item de cabeçalho, que pode incluir uma cadeia de caracteres, uma imagem de bitmap, um tamanho inicial e um valor de **lParam** definido pelo aplicativo.

O membro **fmt** da estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) de um item pode incluir a **cadeia de \_ caracteres HDF** ou o sinalizador **\_ bitmap HDF** para indicar se o controle exibe a cadeia de caracteres ou o bitmap do item. Se você quiser exibir uma cadeia de caracteres e um bitmap, crie um item desenhado pelo proprietário definindo o membro **fmt** para incluir o sinalizador **HDF \_ OWNERDRAW** . A estrutura **HDITEM** também especifica sinalizadores de formatação que dizem ao controle se deve ser centralizado, alinhado à esquerda ou alinhado à cadeia de caracteres ou ao bitmap no retângulo do item.

[**HDM \_ INSERTITEM**](hdm-insertitem.md) retorna o índice do item recém-adicionado. Você pode usar o índice em outras mensagens para definir propriedades ou recuperar informações sobre o item. Você pode excluir um item usando a mensagem [**HDM \_ DELETEITEM**](hdm-deleteitem.md) , especificando o índice do item a ser excluído.

Você pode usar a mensagem [**HDM \_ SETITEM**](hdm-setitem.md) para definir as propriedades de um item de cabeçalho existente e a mensagem [**HDM \_ GETITEM**](hdm-getitem.md) para recuperar as propriedades atuais de um item. Para recuperar uma contagem dos itens em um controle de cabeçalho, use a mensagem [**HDM \_ GetItemCount**](hdm-getitemcount.md) .

## <a name="owner-drawn-header-controls"></a>Controles de cabeçalho Owner-Drawn

Você pode definir itens individuais de um controle de cabeçalho para serem itens desenhados pelo proprietário. O uso dessa técnica lhe dá mais controle do que você teria sobre a aparência de um item de cabeçalho.

Você pode usar a mensagem [**HDM \_ INSERTITEM**](hdm-insertitem.md) para inserir um novo item desenhado pelo proprietário em um controle de cabeçalho ou na mensagem [**HDM \_ SETITEM**](hdm-setitem.md) para alterar um item existente para um item de desenho proprietário. Ambas as mensagens incluem o endereço de uma estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , que deve ter o membro **fmt** definido como o valor **\_ OWNERDRAW HDF** .

Quando um controle de cabeçalho deve desenhar um item desenhado pelo proprietário, ele envia a mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) para a janela pai. O parâmetro *wParam* da mensagem é o identificador da janela filho do controle de cabeçalho e o parâmetro *lParam* é um endereço de uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . A janela pai usa as informações na estrutura para desenhar o item. Para um item desenhado pelo proprietário em um controle de cabeçalho, a estrutura **DRAWITEMSTRUCT** contém as informações a seguir.



| Membro         | DESCRIÇÃO                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | [**Odt \_**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Proprietário do cabeçalho-tipo de controle desenhado.                                                                                        |
| **CtlID**      | Identificador da janela filho do controle de cabeçalho.                                                                                                         |
| **itemID**     | Índice do item a ser desenhado.                                                                                                                         |
| **Ação** | [**Oda \_**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Sinalizador de ação de desenho DRAWENTIRE.                                                                                         |
| **itemState**  | [**ODS \_**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) Sinalizador de ação de desenho selecionado se o cursor estiver no item e o botão do mouse estiver inativo. Caso contrário, esse membro será zero. |
| **hwndItem**   | Identificador para o controle de cabeçalho.                                                                                                                          |
| **hDC**        | Identificador para o contexto do dispositivo do controle de cabeçalho.                                                                                                    |
| **rcItem**     | Coordenadas do item de cabeçalho a ser desenhado. As coordenadas são relativas ao canto superior esquerdo do controle de cabeçalho.                               |
| **Dados do**   | Valor de 32 bits definido pelo aplicativo associado ao item.                                                                                             |



 

## <a name="header-control-filters"></a>Filtros de controle de cabeçalho

Ao especificar o estilo de janela do [**HDS \_ FILTERBAR**](header-control-styles.md) para um controle de cabeçalho, você pode habilitar o posicionamento das caixas de edição de filtro abaixo dos títulos de coluna. Um botão de filtro é exibido ao lado da caixa de edição. Você pode implementar a filtragem respondendo a códigos de notificação [HDN \_ BEGINFILTEREDIT](hdn-beginfilteredit.md), [HDN \_ ENDFILTEREDIT](hdn-endfilteredit.md), [HDN \_ FILTERBTNCLICK](hdn-filterbtnclick.md)ou [HDN \_ FILTERCHANGE](hdn-filterchange.md) .

Por padrão, a caixa de edição contém um prompt para que o usuário insira texto. Você pode restaurar a caixa de edição para esse estado padrão usando o [**cabeçalho \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) ou o [**cabeçalho \_ ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters).

O exemplo de código a seguir mostra como recuperar o controle de cabeçalho de um controle de exibição de lista e adicionar uma barra de filtro.


```
// hList is the HWND of the list-view control.
HWND hHeader = ListView_GetHeader(hList);
LONG_PTR styles = GetWindowLongPtr(hHeader, GWL_STYLE);
SetWindowLongPtr(g_hHeader, GWL_STYLE, styles | HDS_FILTERBAR);
```



## <a name="default-header-control-message-processing"></a>Processamento de mensagens de controle de cabeçalho padrão

Esta seção descreve as mensagens de janela tratadas pelo procedimento de janela para a classe de janela de [**\_ cabeçalho WC**](common-control-window-classes.md) .



| Mensagem                                            | Processamento realizado                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**criação do WM \_**](/windows/desktop/winmsg/wm-create)                 | Inicializa o controle de cabeçalho.                                                                                                                                                                                                                                                                               |
| [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)               | Desinicializa o controle de cabeçalho.                                                                                                                                                                                                                                                                             |
| [**ERASEBKGND do WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)         | Preenche o plano de fundo do controle de cabeçalho usando a cor do plano de fundo atual do controle.                                                                                                                                                                                                                      |
| [**GETDLGCODE do WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)         | Retorna uma combinação dos valores [**DLGC \_ WANTTAB**](/windows/desktop/dlgbox/wm-getdlgcode) e [**DLGC \_ WANTARROWS**](/windows/desktop/dlgbox/wm-getdlgcode) .                                                                                                                     |
| [**WM \_ GETfont**](/windows/desktop/winmsg/wm-getfont)               | Retorna o identificador para a fonte atual, que é usada pelo controle de cabeçalho para desenhar seu texto.                                                                                                                                                                                                                 |
| [**LBUTTONDBLCLK do WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk) | Captura a entrada do mouse. Se o cursor do mouse estiver em um divisor, o controle enviará o código de notificação [HDN \_ BEGINTRACK](hdn-begintrack.md) e começará a arrastar o divisor. Se o cursor estiver em um item, o item será exibido no estado pressionado.                                                            |
| [**LBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-lbuttondown)     | O mesmo que a mensagem [**\_ LBUTTONDBLCLK do WM**](/windows/desktop/inputdev/wm-lbuttondblclk) .                                                                                                                                                                                                                                       |
| [**LBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-lbuttonup)         | Libera a captura do mouse. Se o controle estava rastreando o movimento do mouse, ele envia o código de notificação do [ \_ endtrack HDN](hdn-endtrack.md) e redesenha o controle de cabeçalho. Caso contrário, o controle enviará o código de notificação [HDN \_ DoClick](hdn-itemclick.md) e redesenhará o item de cabeçalho que foi clicado. |
| [**admousemove do WM \_**](/windows/desktop/inputdev/wm-mousemove)         | Se um divisor estiver sendo arrastado, o controle enviará o código de notificação [HDN \_ Track](hdn-track.md) e exibirá o item na nova posição. Se o botão esquerdo do mouse estiver pressionado e o cursor estiver em um item, o item será exibido no estado pressionado.                                                      |
| [**NCCREATE do WM \_**](/windows/desktop/winmsg/wm-nccreate)             | Aloca e Inicializa uma estrutura de dados interna.                                                                                                                                                                                                                                                         |
| [**NCDESTROY do WM \_**](/windows/desktop/winmsg/wm-ncdestroy)           | Libera os recursos alocados pelo controle de cabeçalho depois que o controle de cabeçalho não é inicializado.                                                                                                                                                                                                                |
| [**pintura do WM \_**](/windows/desktop/gdi/wm-paint)                      | Pinta a região inválida do controle de cabeçalho. Se o parâmetro *wParam* for não nulo, o controle assumirá que o valor é um hDC e pinta usando esse contexto de dispositivo.                                                                                                                                    |
| [**WM \_ SETcursor**](/windows/desktop/menurc/wm-setcursor)           | Define a forma do cursor, dependendo se o cursor está em um divisor ou em um item de cabeçalho.                                                                                                                                                                                                                   |
| [**WM \_ SETfont**](/windows/desktop/winmsg/wm-setfont)               | Seleciona um novo identificador de fonte no contexto do dispositivo para o controle de cabeçalho.                                                                                                                                                                                                                                     |



 

 

 