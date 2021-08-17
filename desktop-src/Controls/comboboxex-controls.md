---
title: Sobre controles ComboBoxEx
description: Os controles ComboBoxEx são controles de caixa de combinação que fornecem suporte nativo para imagens de item.
ms.assetid: a4b1aa79-40c4-4eff-801c-4f308d86fb35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993fa8db73246c62f8ceee805e767c13ffdcc15a12d0222e09f308324cc97bab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831832"
---
# <a name="about-comboboxex-controls"></a>Sobre controles ComboBoxEx

Os controles ComboBoxEx são controles de caixa de combinação que fornecem suporte nativo para imagens de item. Para tornar as imagens de item facilmente acessíveis, o controle fornece suporte à lista de imagens. Usando esse controle, você pode fornecer a funcionalidade de uma caixa de combinação sem precisar desenhar manualmente elementos gráficos de item.

Este tópico inclui as seções a seguir.

-   [Criando controles ComboBoxEx](#creating-comboboxex-controls)
-   [Estilos de controle ComboBoxEx](#comboboxex-control-styles)
-   [Itens de controle ComboBoxEx](#comboboxex-control-items)
-   [Itens de retorno de chamada](#callback-items)
-   [Listas de imagens de controle ComboBoxEx](#comboboxex-control-image-lists)
-   [Sobre mensagens de notificação de controle ComboBoxEx](#about-comboboxex-control-notification-messages)
-   [Encaminhamento de mensagem de controle ComboBoxEx](#comboboxex-control-message-forwarding)

## <a name="creating-comboboxex-controls"></a>Criando controles ComboBoxEx

Efetivamente, um controle ComboBoxEx cria uma caixa de combinação filho e executa tarefas de desenho de proprietário para você com base em uma lista de imagens atribuídas. Portanto, o [**estilo CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) está implícito e não é necessário usá-lo ao criar o controle. Como as listas de imagens são usadas para fornecer gráficos de item, o [**estilo CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) não pode ser usado.

Um controle ComboBoxEx deve ser inicializado chamando a função [**InitCommonControlsEx,**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) especificando ICC USEREX CLASSES na estrutura \_ \_ [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que acompanha.

Você pode criar um controle ComboBoxEx usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especificando [**WC \_ COMBOBOXEX**](common-control-window-classes.md) como a classe de janela. A classe é registrada quando a [**função InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) é chamada, conforme explicado acima.

Os controles ComboBoxEx são criados sem uma lista de imagens padrão. Para usar imagens de item, você deve criar uma lista de imagens para o controle ComboBoxEx e atribuí-la ao controle usando a mensagem [**CBEM \_ SETIMAGELIST.**](cbem-setimagelist.md) Se você não atribuir uma lista de imagens ao controle ComboBoxEx, o controle exibirá apenas o texto do item.

## <a name="comboboxex-control-styles"></a>Estilos de controle ComboBoxEx

Os controles ComboBoxEx suportam apenas os seguintes estilos ComboBox:

-   CBS \_ SIMPLE
-   MENU SUSPENSO DO CBS \_
-   CBS \_ DROPDOWNLIST
-   WS \_ CHILD

Também há vários Estilos [Estendidos do Controle ComboBoxEx](comboboxex-control-extended-styles.md) que são usados apenas pelo ComboBoxEx.

> [!Note]  
> O [**estilo CBS \_ SIMPLE**](combo-box-styles.md) pode não funcionar corretamente em alguns casos.

 

Como o controle ComboBoxEx executa tarefas de desenho de proprietário para você com base em uma lista de imagens atribuídas, o estilo [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) está implícito; você não precisa usá-lo ao criar o controle. Como as listas de imagens são usadas para fornecer gráficos de item, o [**estilo CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) não pode ser usado. O controle ComboBoxEx também dá suporte a Estilos Estendidos [do Controle ComboBoxEx](comboboxex-control-extended-styles.md) que fornecem recursos adicionais.

## <a name="comboboxex-control-items"></a>Itens de controle ComboBoxEx

Os controles ComboBoxEx mantêm informações de item usando [**uma estrutura COMBOBOXEXITEM.**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) Essa estrutura inclui membros para índices de item, índices de imagem (normal, estado de seleção e sobreposição), valores de recuo, cadeias de caracteres de texto e valores específicos do item.

O controle ComboBoxEx fornece acesso fácil e manipulação de itens por meio de mensagens. Para adicionar ou excluir um item, envie a [**mensagem CBEM \_ INSERTITEM**](cbem-insertitem.md) ou [**CBEM \_ DELETEITEM.**](cbem-deleteitem.md) Você pode modificar itens atualmente no controle usando a mensagem [**CBEM \_ SETITEM.**](cbem-setitem.md)

## <a name="callback-items"></a>Itens de retorno de chamada

Os controles ComboBoxEx suportam atributos de item de retorno de chamada. Você pode especificar um item como um item de retorno de chamada ao adicioná-lo ao controle usando [**CBEM \_ INSERTITEM**](cbem-insertitem.md). Ao atribuir valores à estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) de um item, você deve especificar os valores apropriados do sinalizador de retorno de chamada. A seguir estão **os membros da estrutura COMBOBOXEXITEM** e seus valores de sinalizador de retorno de chamada correspondentes.



| Membro             | Valor de retorno de chamada      |
|--------------------|---------------------|
| **Psztext**        | LPSTR \_ TEXTCALLBACK |
| **Iimage**         | I \_ IMAGECALLBACK    |
| **Iselectedimage** | I \_ IMAGECALLBACK    |
| **Ioverlay**       | I \_ IMAGECALLBACK    |
| **iIndent**        | I \_ INDENTCALLBACK   |



 

O controle solicitará informações sobre itens de retorno de chamada enviando códigos de notificação [ \_ CBEN GETDISPINFO.](cben-getdispinfo.md) Essa notificação é enviada na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) Quando seu aplicativo processa essa mensagem, ele deve fornecer as informações solicitadas para o controle. Se você  definir o membro de máscara da estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que o acompanha como CBEIF \_ DI SETITEM, o controle armazenará os dados do item e não os solicitará \_ novamente.

## <a name="comboboxex-control-image-lists"></a>Listas de imagens de controle ComboBoxEx

Se você quiser que um controle ComboBoxEx exiba ícones com itens, forneça uma lista de imagens. Os controles ComboBoxEx suportam até três imagens para um item – uma para seu estado selecionado, uma para seu estado não selecionado e outra para uma imagem de sobreposição. Atribua uma lista de imagens existente a um controle ComboBoxEx usando a [**mensagem CBEM \_ SETIMAGELIST.**](cbem-setimagelist.md)

A [**estrutura COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) contém membros que representam os índices de imagem para cada lista de imagens (selecionado, não selecionado e sobreposição). Para cada item, de definir esses membros para exibir as imagens desejadas. Não é necessário especificar índices de imagem para cada tipo de imagem. Você pode combinar e corresponder tipos de imagem  como quiser, mas sempre definir o membro de máscara da estrutura **COMBOBOXEXITEM** para indicar quais membros estão sendo usados. O controle ignora os membros que não foram sinalizados como válidos.

> [!Note]  
> Se você usar o [**estilo CBS \_ SIMPLE,**](combo-box-styles.md) os ícones não serão exibidos.

 

## <a name="about-comboboxex-control-notification-messages"></a>Sobre mensagens de notificação de controle ComboBoxEx

Um controle ComboBoxEx envia mensagens de notificação para relatar alterações dentro de si mesmo ou para solicitar informações de item de retorno de chamada. O pai do controle recebe todas as mensagens [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) da caixa de combinação contida no controle ComboBoxEx. O controle ComboBoxEx envia suas próprias notificações usando [**mensagens WM \_ NOTIFY.**](wm-notify.md) Como resultado, o proprietário do controle deve estar preparado para processar as duas formas de mensagens de notificação.

A seguir estão os códigos de notificação específicos do ComboBoxEx que são enviados por meio de [**mensagens WM \_ NOTIFY.**](wm-notify.md)



| Notificação                              | **Descrição**                                                                                                            |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)     | Sinaliza que o usuário ativou a lista de listas listadas ou clicou na caixa de edição do controle.                               |
| [CBEN \_ ENDEDIT](cben-endedit.md)         | Sinaliza que o usuário selecionou um item na lista de listas listadas ou concluiu uma operação de edição dentro da caixa de edição. |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)   | Relata que um item foi excluído.                                                                                          |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md) | Solicita informações sobre os atributos de um item.                                                                           |
| [CBEN \_ INSERTITEM](cben-insertitem.md)   | Sinaliza que um item foi inserido no controle .                                                                          |



 

## <a name="comboboxex-control-message-forwarding"></a>Encaminhamento de mensagem de controle ComboBoxEx

A seguir estão as mensagens de caixa de combinação padrão que um controle ComboBoxEx encaminha para sua caixa de combinação filho. Algumas dessas mensagens podem ser processadas pelo controle ComboBoxEx antes ou depois que a mensagem foi encaminhada.

-   [**CB \_ DELETESTRING**](cb-deletestring.md)
-   [**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
-   [**CB \_ GETCOUNT**](cb-getcount.md)
-   [**CB \_ GETCURSEL**](cb-getcursel.md)
-   [**CB \_ GETDROPPEDCONTROLRECT**](cb-getdroppedcontrolrect.md)
-   [**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
-   [**CB \_ GETITEMDATA**](cb-getitemdata.md)
-   [**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md)
-   [**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
-   [**CB \_ LIMITTEXT**](cb-limittext.md)
-   [**CB \_ RESETCONTENT**](cb-resetcontent.md)
-   [**CB \_ SETCURSEL**](cb-setcursel.md)
-   [**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md)
-   [**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
-   [**CB \_ SETITEMDATA**](cb-setitemdata.md)
-   [**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
-   [**CB \_ SHOWDROPDOWN**](cb-showdropdown.md)

A seguir estão as mensagens do Windows que um controle ComboBoxEx encaminha para sua janela pai:

-   [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) (isso inclui todas as notificações \_ cbn.)
-   [**WM \_ NOTIFY**](wm-notify.md)

 

 