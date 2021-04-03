---
title: Sobre controles de guia
description: Um controle guia é análogo aos divisores em um bloco de anotações ou aos rótulos em um arquivo de gabinete. Usando um controle guia, um aplicativo pode definir várias páginas para a mesma área de uma janela ou caixa de diálogo.
ms.assetid: 55ed2863-7f8d-43ce-a0f9-6f6d41e3f947
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c45ac7caa05c73e1dcf22a8e6f0eb4d031ca079
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084934"
---
# <a name="about-tab-controls"></a>Sobre controles de guia

Um controle guia é análogo aos divisores em um bloco de anotações ou aos rótulos em um arquivo de gabinete. Usando um controle guia, um aplicativo pode definir várias páginas para a mesma área de uma janela ou caixa de diálogo. Cada página consiste em um determinado tipo de informação ou um grupo de controles que o aplicativo exibe quando o usuário seleciona a guia correspondente.

A captura de tela a seguir mostra um controle de guia simples que contém guias para dias da semana. A guia terça-feira foi selecionada.

![captura de tela de uma folha de propriedades com cinco guias, uma para cada dia da semana](images/tab-simple.png)

Este tópico inclui as seções a seguir.

-   [Criando controles de guia](#creating-tab-controls)
-   [Estilos de controle de guia](#tab-control-styles)
-   [Guias e atributos de tabulação](#tabs-and-tab-attributes)
-   [Área de exibição](#display-area)
-   [Seleção de guia](#tab-selection)
-   [Listas de imagens de controle de guia](#tab-control-image-lists)
-   [Tamanho e posição da Tabulação](#tab-size-and-position)
-   [Guias desenhadas pelo proprietário](#owner-drawn-tabs)
-   [Dicas de ferramenta de controle de guia](#tab-control-tooltips)
-   [Processamento de mensagem de controle de guia padrão](#default-tab-control-message-processing)

## <a name="creating-tab-controls"></a>Criando controles de guia

Você pode criar um controle guia chamando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe da janela do [**\_ TABCONTROL WC**](common-control-window-classes.md) . Essa classe de janela é registrada quando a DLL de controles comuns é carregada. Para garantir que a DLL seja carregada, use a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .

No Microsoft Visual Studio, você pode criar um controle guia usando a caixa de ferramentas.

Você envia mensagens a um controle guia para adicionar guias e, caso contrário, afeta a aparência e o comportamento do controle. Cada mensagem tem uma macro correspondente que você pode usar em vez de enviar a mensagem explicitamente. Não é possível desabilitar uma guia individual em um controle guia. No entanto, você pode desabilitar um controle guia em uma folha de propriedades desabilitando a página correspondente.

## <a name="tab-control-styles"></a>Estilos de controle de guia

Você pode aplicar determinadas características a controles guia especificando os estilos de controle de guia quando o controle é criado. Por exemplo, você pode especificar o alinhamento e a aparência geral das guias em um controle guia.

Você pode fazer com que as guias se pareçam com botões especificando o estilo de [**\_ botões de TCS**](tab-control-styles.md) . As guias nesse tipo de controle de guia devem servir para a mesma função que os controles de botão; ou seja, clicar em uma guia deve executar um comando em vez de exibir uma página. Como a área de exibição em um controle de guia de botão normalmente não é usada, nenhuma borda é desenhada em torno dela.

Você pode fazer com que uma guia receba o foco de entrada quando clicado especificando o estilo de [**TCS \_ FOCUSONBUTTONDOWN**](tab-control-styles.md) . Normalmente, esse estilo é usado apenas com o estilo de [**\_ botões de TCS**](tab-control-styles.md) . Você pode especificar que uma guia não receba o foco de entrada quando clicado usando o estilo [**TCS \_ FOCUSNEVER**](tab-control-styles.md) .

Por padrão, um controle guia exibe apenas uma linha de guias. Se nem todas as guias puderem ser mostradas de uma vez, o controle guia exibirá um controle acima para baixo para que o usuário possa rolar guias adicionais para exibição. Você pode fazer com que um controle guia exiba várias linhas de guias, se necessário, especificando o estilo de [**\_ multilinha de TCS**](tab-control-styles.md) . Com esse estilo, todas as guias podem ser exibidas ao mesmo tempo. As guias são alinhadas à esquerda em cada linha, a menos que você especifique o estilo de [**TCS \_ RIGHTJUSTIFY**](tab-control-styles.md) . Nesse caso, a largura de cada guia é aumentada para que cada linha de guias preencha toda a largura do controle guia.

Um controle guia dimensiona automaticamente cada guia para caber seu ícone, se houver, e seu rótulo. Para dar à mesma largura todas as guias, você pode especificar o estilo de [**\_ FIXEDWIDTH de TCS**](tab-control-styles.md) . O controle dimensiona todas as guias para se ajustarem ao rótulo mais largo, ou você pode atribuir uma largura e uma altura específicas usando a mensagem do [**TCM \_ setitems**](tcm-setitemsize.md) . Dentro de cada guia, o controle centraliza o ícone e o rótulo, colocando o ícone à esquerda do rótulo. Você pode forçar o ícone à esquerda, deixando o rótulo centralizado, especificando o estilo de [**TCS \_ FORCEICONLEFT**](tab-control-styles.md) . Você pode alinhar à esquerda o ícone e o rótulo usando o estilo de [**TCS \_ FORCELABELLEFT**](tab-control-styles.md) . Não é possível usar o estilo de **\_ FIXEDWIDTH de TCS** com o estilo de [**TCS \_ RIGHTJUSTIFY**](tab-control-styles.md) .

Você pode especificar que a janela pai desenhe as guias no controle usando o estilo [**TCS \_ OwnerDrawFixed**](tab-control-styles.md) . Para obter mais informações, consulte [guias desenhadas pelo proprietário](#owner-drawn-tabs).

Você pode especificar que um controle de guia criará um controle ToolTip usando o estilo de [**\_ Tooltips de TCS**](tab-control-styles.md) . Para obter mais informações sobre isso, consulte [dicas de ferramentas de controle de tabulação](#tab-control-tooltips).

## <a name="tabs-and-tab-attributes"></a>Guias e atributos de tabulação

Cada guia em um controle guia consiste em um ícone, um rótulo e dados definidos pelo aplicativo. Essas informações são especificadas por uma estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Você pode adicionar guias a um controle guia, recuperar o número de guias, recuperar e definir o conteúdo de uma guia e excluir guias. As guias são identificadas por seu índice de base zero.

Para adicionar guias a um controle guia, use a [**mensagem \_ INSERTITEM do TCM**](tcm-insertitem.md) , especificando a posição do item e o endereço de uma estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Você pode recuperar e definir o conteúdo de uma guia existente usando as mensagens [**TCM \_ GETITEM**](tcm-getitem.md) e [**TCM \_ SETITEM**](tcm-setitem.md) . Para cada guia, você pode especificar um ícone, um rótulo ou ambos. Você também pode especificar dados definidos pelo aplicativo para associar à guia.

Você pode recuperar o número atual de guias usando a mensagem [**TCM \_ GetItemCount**](tcm-getitemcount.md) , excluir uma guia usando a mensagem [**\_ DELETEITEM do TCM**](tcm-deleteitem.md) e excluir todas as guias em um controle guia usando a mensagem [**\_ DELETEALLITEMS do TCM**](tcm-deleteallitems.md) .

Você pode associar dados definidos pelo aplicativo a cada guia. Por exemplo, você pode salvar informações sobre cada página com sua guia correspondente. Por padrão, um controle guia aloca quatro bytes extras por guia para dados definidos pelo aplicativo. Você pode alterar o número de bytes extras por guia usando a mensagem [**\_ SETITEMEXTRA do TCM**](tcm-setitemextra.md) . Você só pode usar esta mensagem quando o controle guia está vazio.

Os dados definidos pelo aplicativo são especificados pelo membro **lParam** da estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . Se você usar mais de 4 bytes de dados definidos pelo aplicativo, precisará definir sua própria estrutura e usá-la em vez de **TCITEM**. Você pode recuperar e definir dados definidos pelo aplicativo da mesma maneira que recupera e define outras informações sobre uma guia — usando as mensagens [**TCM \_ GETITEM**](tcm-getitem.md) e [**TCM \_ SETITEM**](tcm-setitem.md) .

O primeiro membro de sua estrutura deve ser uma estrutura [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) e os membros restantes devem especificar dados definidos pelo aplicativo. **TCITEMHEADER** é idêntico a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema), exceto que não tem o membro **lParam** . A diferença entre o tamanho da sua estrutura e o tamanho de **TCITEMHEADER** deve ser igual ao número de bytes extras por guia.

## <a name="display-area"></a>Área de exibição

A área de exibição de um controle guia é a área na qual um aplicativo exibe a página atual. Normalmente, um aplicativo cria uma janela ou caixa de diálogo filho, definindo o tamanho e a posição da janela de acordo com a área de exibição. Dado o retângulo da janela para um controle guia, você pode calcular o retângulo delimitador da área de exibição usando a mensagem [**\_ ADJUSTRECT do TCM**](tcm-adjustrect.md) .

Às vezes, a área de exibição deve ser um tamanho específico — por exemplo, o tamanho de uma caixa de diálogo filho sem janela restrita. Dado o retângulo delimitador para a área de exibição, você pode usar [**\_ ADJUSTRECT de TCM**](tcm-adjustrect.md) para calcular o retângulo de janela correspondente para o controle guia.

## <a name="tab-selection"></a>Seleção de guia

Quando o usuário seleciona uma guia, um controle guia envia seus códigos de notificação de janela pai na forma de mensagens de [**\_ notificação do WM**](wm-notify.md) . O código de notificação do [TCN \_ SELCHANGING](tcn-selchanging.md) é enviado antes de a seleção ser alterada e o código de notificação do [TCN \_ SELCHANGE](tcn-selchange.md) é enviado depois que a seleção é alterada.

Você pode processar [o \_ SELCHANGING de TCN](tcn-selchanging.md) para salvar o estado da página de saída. Você pode retornar **true** para impedir que a seleção seja alterada. Por exemplo, talvez você não queira sair de uma caixa de diálogo filho na qual um controle tem uma configuração inválida.

Você deve processar [o \_ SELCHANGE de TCN](tcn-selchange.md) para exibir a página de entrada na área de exibição. Isso pode simplesmente envolver a alteração das informações exibidas em uma janela filho. Com mais frequência, cada página consiste em uma janela ou caixa de diálogo filho. Nesse caso, um aplicativo pode processar essa notificação destruindo ou ocultando a janela ou caixa de diálogo filho de saída e criando ou mostrando a janela ou caixa de diálogo filho de entrada.

Você pode recuperar e definir a seleção atual usando as mensagens do [**TCM \_ getcurseal**](tcm-getcursel.md) e [**TCM \_ setcurse**](tcm-setcursel.md) .

## <a name="tab-control-image-lists"></a>Listas de imagens de controle de guia

Cada guia pode ter um ícone associado a ele, que é especificado por um índice na lista de imagens para o controle guia. Quando um controle guia é criado, ele não tem nenhuma lista de imagens associada a ele. Um aplicativo pode criar uma lista de imagens usando a função [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) e, em seguida, atribuí-la a um controle guia usando a mensagem de [**TCM \_ SetImageList**](tcm-setimagelist.md) .

Você pode adicionar imagens à lista de imagens de um controle guia da mesma forma como faria com qualquer outra lista de imagens. No entanto, um aplicativo deve remover imagens usando a mensagem [**\_ REMOVEIMAGE do TCM**](tcm-removeimage.md) em vez da função [**ImageList \_ Remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) . Essa mensagem garante que cada guia permaneça associada à mesma imagem que antes.

A destruição de um controle de guia não destrói uma lista de imagens associada a ele. Você deve destruir a lista de imagens separadamente. Isso será útil se você quiser atribuir a mesma lista de imagens a vários controles guia.

Para recuperar o identificador para a lista de imagens atualmente associada a um controle guia, você pode usar a mensagem [**TCM \_ GetImageList**](tcm-getimagelist.md) .

## <a name="tab-size-and-position"></a>Tamanho e posição da Tabulação

Cada guia em um controle guia tem um tamanho e uma posição. Você pode definir o tamanho das guias, recuperar o retângulo delimitador de uma guia ou determinar qual guia está em uma posição especificada.

Para controles de tabulação de largura fixa e de proprietário, você pode definir a largura e a altura exatas das guias usando a mensagem do [**TCM \_ setitems**](tcm-setitemsize.md) . Em outros controles guia, o tamanho de cada guia é calculado com base no ícone e no rótulo da guia. O controle guia inclui espaço para uma borda e uma margem adicional. Você pode definir a espessura da margem usando a mensagem de [**\_ AutoPreenchimento do TCM**](tcm-setpadding.md) .

Você pode determinar o retângulo delimitador atual para uma guia usando a [**mensagem \_ GETITEMRECT do TCM**](tcm-getitemrect.md) . Você pode determinar qual guia, se houver, está em um local especificado usando a mensagem [**\_ HITTEST de TCM**](tcm-hittest.md) .

Em um controle guia com o estilo de [**\_ multilinha de TCS**](tab-control-styles.md) , você pode determinar o número atual de linhas de guias usando a mensagem do [**TCM \_ GetRowCount**](tcm-getrowcount.md) .

## <a name="owner-drawn-tabs"></a>Owner-Drawn guias

Se um controle guia tiver o estilo de [**TCS \_ OwnerDrawFixed**](tab-control-styles.md) , a janela pai deverá pintar guias processando a mensagem [**\_ DRAWITEM do WM**](wm-drawitem.md) . O controle guia envia essa mensagem sempre que uma guia precisa ser pintada. O parâmetro *lParam* especifica o endereço de uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) , que contém o índice da guia, seu retângulo delimitador e o DC (contexto do dispositivo) no qual desenhar.

Por padrão, o membro de **dados** de [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contém o valor do membro **lParam** da estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) . No entanto, se você alterar a quantidade de dados definidos pelo aplicativo por guia, **os dados** conterá o endereço dos dados. Você pode alterar a quantidade de dados definidos pelo aplicativo por guia usando a mensagem [**\_ SETITEMEXTRA do TCM**](tcm-setitemextra.md) .

Para especificar o tamanho dos itens em um controle guia, a janela pai deve processar a [**mensagem \_ MEASUREITEM do WM**](wm-measureitem.md) . Como todas as guias em um controle de guia desenhado pelo proprietário têm o mesmo tamanho, essa mensagem é enviada apenas uma vez. Não há nenhum estilo de controle de guia para guias de tamanho variável desenhadas pelo proprietário. Você também pode definir a largura e a altura das guias usando a mensagem do [**TCM \_ setitems**](tcm-setitemsize.md) .

## <a name="tab-control-tooltips"></a>Dicas de ferramenta de controle de guia

Você pode usar um controle ToolTip para fornecer uma breve descrição de cada guia em um controle guia. Um controle guia que tem o estilo de [**\_ Tooltips de TCS**](tab-control-styles.md) cria um controle ToolTip quando ele é criado e destrói o controle ToolTip quando ele é destruído. Você também pode criar um controle ToolTip e atribuí-lo a um controle guia.

Se você usar um controle ToolTip com um controle guia, a janela pai deverá processar o código de notificação [TTN \_ GETDISPINFO](ttn-getdispinfo.md) para fornecer uma descrição de cada guia na solicitação.

Para usar o mesmo controle ToolTip com mais de um controle guia, crie o controle ToolTip por conta própria e atribua-o ao controle guia usando a mensagem [**TCM \_ SetToolTips**](tcm-settooltips.md) . Você pode recuperar o identificador para um controle de dica de ferramenta atual do controle guia usando a mensagem [**TCM \_ GetToolTips**](tcm-gettooltips.md) . Se você criar seu próprio controle ToolTip, não deverá usar o estilo [**de \_ Tooltips de TCS**](tab-control-styles.md) .

## <a name="default-tab-control-message-processing"></a>Processamento de mensagem de controle de guia padrão

Esta seção descreve o processamento de mensagens executado por um controle guia. Mensagens específicas para controles de guia são discutidas em outras seções desta documentação.



| Mensagem                                                  | Processamento realizado                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ capturachanged**](/windows/desktop/inputdev/wm-capturechanged) | Não fará nada se o controle de guia lançar a captura do mouse em si. Se outra janela tiver capturado o mouse e um botão for mantido pressionado, o comando liberará o botão.                                                                                                                                                                                                                                                                                                                |
| [**criação do WM \_**](/windows/desktop/winmsg/wm-create)                 | Aloca e Inicializa uma estrutura de dados interna. O controle criará um controle ToolTip se o estilo de [**\_ Tooltips de TCS**](tab-control-styles.md) for especificado.                                                                                                                                                                                                                                                                                                    |
| [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)               | Libera recursos alocados durante o processamento de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) .                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**GETDLGCODE do WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)         | Retorna uma combinação dos valores DLGC \_ WANTARROWS e DLGC \_ WANTCHARS.                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**WM \_ GETfont**](/windows/desktop/winmsg/wm-getfont)               | Retorna o identificador para a fonte usada para rótulos.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**o WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)               | Processa as chaves de direção e altera a seleção, se apropriado.                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**KILLFOCUS do WM \_**](/windows/desktop/inputdev/wm-killfocus)           | Invalida a guia que tem o foco para que ela seja repintada para refletir um estado não focalizado.                                                                                                                                                                                                                                                                                                                                                                                      |
| [**LBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-lbuttondown)       | Encaminha a mensagem para o controle ToolTip, se houver, e altera a seleção se o usuário estiver clicando em uma guia. Se o usuário estiver clicando em um botão, o controle redesenhará o botão para dar uma aparência de baixo relevo e capturará o mouse. Se o usuário estiver clicando em uma guia ou botão e o estilo de [**\_ FOCUSONBUTTONDOWN de TCS**](tab-control-styles.md) for especificado, o controle definirá o foco para ele mesmo.                                                     |
| [**LBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-lbuttonup)           | Libera o mouse se um botão foi pressionado. Se o cursor estiver sobre o botão e estiver sendo mantido inativo, o controle alterará a seleção de acordo e redesenhará o botão.                                                                                                                                                                                                                                                                                                         |
| [**admousemove do WM \_**](/windows/desktop/inputdev/wm-mousemove)           | Encaminha a mensagem para o controle ToolTip, se houver. Se o estilo de [**\_ botões de TCS**](tab-control-styles.md) for especificado e o botão do mouse estiver sendo pressionado depois de clicar, o controle também poderá redesenhar o botão afetado para dar a ele uma aparência de alto ou baixo relevo.                                                                                                                                                                                            |
| [**notificação do WM \_**](wm-notify.md)                          | Encaminha os códigos de notificação enviados pelo controle ToolTip.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**pintura do WM \_**](/windows/desktop/gdi/wm-paint)                            | Desenha uma borda em torno da área de exibição (a menos que o estilo de [**\_ botões de TCS**](tab-control-styles.md) seja especificado) e pinta todas as guias que interseccionam o retângulo inválido. Para cada guia, ele desenha o corpo da guia (ou envia uma mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) para a janela pai) e, em seguida, desenha uma borda ao seu torno na guia. Se o parâmetro *wParam* for não nulo, o controle assumirá que o valor é um hDC e pinta usando esse contexto de dispositivo. |
| [**RBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-rbuttondown)       | Envia um código de notificação [nm \_ RCLICK](nm-rclick-tab.md) para a janela pai.                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)             | Invalida a guia que tem o foco para que ela seja repintada para refletir um estado focalizado.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ SETfont**](/windows/desktop/winmsg/wm-setfont)               | Define a fonte usada para rótulos.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ reemissão**](/windows/desktop/gdi/wm-setredraw)                    | Define o estado de um sinalizador interno que determina se o controle é repintado quando os itens são inseridos e excluídos, quando a fonte é alterada e assim por diante.                                                                                                                                                                                                                                                                                                                      |
| [**tamanho do WM \_**](/windows/desktop/winmsg/wm-size)                     | Recalcula as posições das guias e pode invalidar parte do controle guia para forçar a repintura de algumas ou de todas as guias.                                                                                                                                                                                                                                                                                                                                                             |



 

 

 