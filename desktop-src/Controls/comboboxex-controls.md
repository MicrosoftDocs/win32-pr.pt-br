---
title: Sobre controles ComboBoxEx
description: Os controles ComboBoxEx são controles de caixa de combinação que fornecem suporte nativo para imagens de itens.
ms.assetid: a4b1aa79-40c4-4eff-801c-4f308d86fb35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427abef015474047d1842d13e5fb40640d0406c5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824022"
---
# <a name="about-comboboxex-controls"></a>Sobre controles ComboBoxEx

Os controles ComboBoxEx são controles de caixa de combinação que fornecem suporte nativo para imagens de itens. Para tornar as imagens de item facilmente acessíveis, o controle fornece suporte à lista de imagens. Ao usar esse controle, você pode fornecer a funcionalidade de uma caixa de combinação sem ter que desenhar manualmente os gráficos de itens.

Este tópico inclui as seções a seguir.

-   [Criando controles ComboBoxEx](#creating-comboboxex-controls)
-   [Estilos de controle ComboBoxEx](#comboboxex-control-styles)
-   [Itens de controle ComboBoxEx](#comboboxex-control-items)
-   [Itens de retorno de chamada](#callback-items)
-   [Listas de imagens de controle ComboBoxEx](#comboboxex-control-image-lists)
-   [Sobre as mensagens de notificação de controle ComboBoxEx](#about-comboboxex-control-notification-messages)
-   [Encaminhamento de mensagens de controle ComboBoxEx](#comboboxex-control-message-forwarding)

## <a name="creating-comboboxex-controls"></a>Criando controles ComboBoxEx

Efetivamente, um controle ComboBoxEx cria uma caixa de combinação filho e executa tarefas de desenho de proprietário com base em uma lista de imagens atribuídas. Portanto, o estilo [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) é implícito e não é necessário usá-lo ao criar o controle. Como as listas de imagens são usadas para fornecer gráficos de itens, o estilo [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) não pode ser usado.

Um controle ComboBoxEx deve ser inicializado chamando-se a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , ESPECIFICANDO \_ classes ICC USEREX \_ na estrutura de [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) que o acompanha.

Você pode criar um controle ComboBoxEx usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especificando [**WC \_ ComboBoxEx**](common-control-window-classes.md) como a classe de janela. A classe é registrada quando a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) é chamada conforme explicado acima.

Os controles ComboBoxEx são criados sem uma lista de imagens padrão. Para usar imagens de item, você deve criar uma lista de imagens para o controle ComboBoxEx e atribuí-la ao controle usando a mensagem [**CBEM \_ SetImageList**](cbem-setimagelist.md) . Se você não atribuir uma lista de imagens ao controle ComboBoxEx, o controle exibirá somente o texto do item.

## <a name="comboboxex-control-styles"></a>Estilos de controle ComboBoxEx

Os controles ComboBoxEx dão suporte apenas aos seguintes estilos de ComboBox:

-   CBS \_ simples
-   \_lista suspensa CBS
-   DROPDOWNLIST do CBS \_
-   WS- \_ filho

Há também vários [estilos estendidos de controle ComboBoxEx](comboboxex-control-extended-styles.md) que são usados somente por ComboBoxEx.

> [!Note]  
> O [**estilo \_ simples do CBS**](combo-box-styles.md) pode não funcionar corretamente em alguns casos.

 

Como o controle ComboBoxEx executa tarefas de desenho de proprietário para você com base em uma lista de imagens atribuída, o estilo [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) é implícito; você não precisa usá-lo ao criar o controle. Como as listas de imagens são usadas para fornecer gráficos de itens, o estilo [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) não pode ser usado. O controle ComboBoxEx também dá suporte a [estilos estendidos de controle ComboBoxEx](comboboxex-control-extended-styles.md) que fornecem recursos adicionais.

## <a name="comboboxex-control-items"></a>Itens de controle ComboBoxEx

Os controles ComboBoxEx mantêm informações de item usando uma estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) . Essa estrutura inclui membros para índices de item, índices de imagem (normal, estado de seleção e sobreposição), valores de recuo, cadeias de caracteres de texto e valores específicos de item.

O controle ComboBoxEx fornece acesso fácil e manipulação de itens por meio de mensagens. Para adicionar ou excluir um item, envie a mensagem [**CBEM \_ INSERTITEM**](cbem-insertitem.md) ou [**CBEM \_ DELETEITEM**](cbem-deleteitem.md) . Você pode modificar os itens atualmente no controle usando a mensagem [**CBEM \_ SETITEM**](cbem-setitem.md) .

## <a name="callback-items"></a>Itens de retorno de chamada

Os controles ComboBoxEx dão suporte a atributos de item de retorno de chamada. Você pode especificar um item como um item de retorno de chamada ao adicioná-lo ao controle usando [**CBEM \_ INSERTITEM**](cbem-insertitem.md). Ao atribuir valores à estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) de um item, você deve especificar os valores de sinalizador de retorno de chamada apropriados. Veja a seguir os membros da estrutura **COMBOBOXEXITEM** e seus valores de sinalizador de retorno de chamada correspondentes.



| Membro             | Valor de retorno de chamada      |
|--------------------|---------------------|
| **pszText**        | textcallback de LPSTR \_ |
| **iImage**         | Eu \_ IMAGECALLBACK    |
| **iSelectedImage** | Eu \_ IMAGECALLBACK    |
| **iOverlay**       | Eu \_ IMAGECALLBACK    |
| **iIndent**        | Eu \_ INDENTCALLBACK   |



 

O controle solicitará informações sobre itens de retorno de chamada enviando códigos de notificação [CBEN \_ GETDISPINFO](cben-getdispinfo.md) . Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) . Quando seu aplicativo processa essa mensagem, ele deve fornecer as informações solicitadas para o controle. Se você definir o membro **Mask** da estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que acompanha o CBEIF \_ di \_ SETITEM, o controle armazenará os dados do item e não os solicitará novamente.

## <a name="comboboxex-control-image-lists"></a>Listas de imagens de controle ComboBoxEx

Se desejar que um controle ComboBoxEx exiba ícones com itens, você deverá fornecer uma lista de imagens. Os controles ComboBoxEx dão suporte a até três imagens para um item — uma para o estado selecionado, uma para seu estado não selecionado e outra para uma imagem de sobreposição. Atribua uma lista de imagens existente a um controle ComboBoxEx usando a mensagem [**CBEM \_ SetImageList**](cbem-setimagelist.md) .

A estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) contém membros que representam os índices de imagem para cada lista de imagens (selecionada, desmarcada e sobreposição). Para cada item, defina esses membros para exibir as imagens desejadas. Não é necessário especificar índices de imagem para cada tipo de imagem. Você pode misturar e combinar os tipos de imagem como desejar, mas sempre defina o membro **Mask** da estrutura **COMBOBOXEXITEM** para indicar quais membros estão sendo usados. O controle ignora os membros que não foram sinalizados como válidos.

> [!Note]  
> Se você usar o [**estilo \_ simples do CBS**](combo-box-styles.md) , os ícones não serão exibidos.

 

## <a name="about-comboboxex-control-notification-messages"></a>Sobre as mensagens de notificação de controle ComboBoxEx

Um controle ComboBoxEx envia mensagens de notificação para relatar alterações em si mesmo ou para solicitar informações do item de retorno de chamada. O pai do controle recebe todas as mensagens de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) da caixa de combinação contida no controle ComboBoxEx. O controle ComboBoxEx envia suas próprias notificações usando mensagens de [**\_ notificação do WM**](wm-notify.md) . Como resultado, o proprietário do controle deve estar preparado para processar as duas formas de mensagens de notificação.

A seguir estão os códigos de notificação específicos do ComboBoxEx que são enviados por meio de mensagens de [**\_ notificação do WM**](wm-notify.md) .



| Notificação                              | **Descrição**                                                                                                            |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)     | Sinaliza que o usuário ativou a lista suspensa ou clicou na caixa de edição do controle.                               |
| [CBEN \_ ENDEDIT](cben-endedit.md)         | Sinaliza que o usuário selecionou um item na lista suspensa ou concluiu uma operação de edição na caixa de edição. |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)   | Relata que um item foi excluído.                                                                                          |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md) | Solicita informações sobre os atributos de um item.                                                                           |
| [CBEN \_ INSERTITEM](cben-insertitem.md)   | Sinaliza que um item foi inserido no controle.                                                                          |



 

## <a name="comboboxex-control-message-forwarding"></a>Encaminhamento de mensagens de controle ComboBoxEx

A seguir estão as mensagens padrão da caixa de combinação que um controle ComboBoxEx encaminha para sua caixa de combinação filho. Algumas dessas mensagens podem ser processadas pelo controle ComboBoxEx antes ou depois da mensagem ser encaminhada.

-   [**excluído de CB \_**](cb-deletestring.md)
-   [**\_FINDSTRINGEXACT CB**](cb-findstringexact.md)
-   [**iscount CB \_**](cb-getcount.md)
-   [**iscursel de CB \_**](cb-getcursel.md)
-   [**\_GETDROPPEDCONTROLRECT CB**](cb-getdroppedcontrolrect.md)
-   [**CB \_ GETremovestate**](cb-getdroppedstate.md)
-   [**\_GETITEMDATA CB**](cb-getitemdata.md)
-   [**\_GETITEMHEIGHT CB**](cb-getitemheight.md)
-   [**\_GETLBTEXT CB**](cb-getlbtext.md)
-   [**\_GETLBTEXTLEN CB**](cb-getlbtextlen.md)
-   [**\_GETEXTENDEDUI CB**](cb-getextendedui.md)
-   [**\_LIMITTEXT CB**](cb-limittext.md)
-   [**\_RESETCONTENT CB**](cb-resetcontent.md)
-   [**CB \_ SETcurseal**](cb-setcursel.md)
-   [**\_SETDROPPEDWIDTH CB**](cb-setdroppedwidth.md)
-   [**\_SETEXTENDEDUI CB**](cb-setextendedui.md)
-   [**\_SETITEMDATA CB**](cb-setitemdata.md)
-   [**\_SETITEMHEIGHT CB**](cb-setitemheight.md)
-   [**\_menu suspenso de CB**](cb-showdropdown.md)

A seguir estão as mensagens do Windows que um controle ComboBoxEx encaminha para sua janela pai:

-   [**WM \_ (Isso**](/windows/desktop/menurc/wm-command) inclui todas as notificações do CBN \_ .)
-   [**notificação do WM \_**](wm-notify.md)

 

 