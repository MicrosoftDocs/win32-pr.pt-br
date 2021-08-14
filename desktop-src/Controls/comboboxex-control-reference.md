---
title: Controle ComboBoxEx
description: Esta seção contém informações sobre os elementos de programação usados com controles ComboBoxEx.
ms.assetid: vs|controls|~\controls\comboex\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded6ff945424f63baaf0063ce5d8897f84883d5063989aa6c7a9fb1a4f76a704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413459"
---
# <a name="comboboxex-control"></a>Controle ComboBoxEx

Esta seção contém informações sobre os elementos de programação usados com controles ComboBoxEx.

### <a name="overviews"></a>Visões gerais



| Tópico                                                | Sumário                                                                                           |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Sobre controles ComboBoxEx](comboboxex-controls.md) | Os controles ComboBoxEx são controles de caixa de combinação que fornecem suporte nativo para imagens de itens.<br/> |
| [Usando controles ComboBoxEx](using-comboboxex.md)    | Esta seção contém código de exemplo e informações sobre como usar controles ComboBoxEx.<br/> |



 

### <a name="messages"></a>Mensagens



| Tópico                                                   | Sumário                                                                                                                                                                                                   |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CBEM \_ DELETEITEM**](cbem-deleteitem.md)             | Remove um item de um controle ComboBoxEx. <br/>                                                                                                                                                     |
| [**CBEM \_ GETCOMBOCONTROL**](cbem-getcombocontrol.md)   | Obtém o identificador para o controle da caixa de combinação filho. <br/>                                                                                                                                                |
| [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md)     | Obtém o identificador para a parte de controle de edição de um controle ComboBoxEx. Um controle ComboBoxEx usa uma caixa de edição quando ela é definida como o estilo [**\_ DROPDOWN do CBS**](combo-box-styles.md) . <br/> |
| [**CBEM \_ Extended**](cbem-getextendedstyle.md) | Obtém os estilos estendidos que estão em uso para um controle ComboBoxEx. <br/>                                                                                                                             |
| [**CBEM \_ GETimagelist**](cbem-getimagelist.md)         | Obtém o identificador para uma lista de imagens atribuída a um controle ComboBoxEx. <br/>                                                                                                                             |
| [**CBEM \_ GETITEM**](cbem-getitem.md)                   | Obtém informações de item para um determinado item ComboBoxEx.<br/>                                                                                                                                              |
| [**CBEM \_ GETUNICODEFORMAT**](cbem-getunicodeformat.md) | Obtém o sinalizador de formato de caractere UNICODE para o controle. <br/>                                                                                                                                        |
| [**CBEM \_ HASEDITCHANGED**](cbem-haseditchanged.md)     | Determina se o usuário alterou o texto de um controle de edição ComboBoxEx.<br/>                                                                                                                  |
| [**CBEM \_ INSERTITEM**](cbem-insertitem.md)             | Insere um novo item em um controle ComboBoxEx. <br/>                                                                                                                                                    |
| [**CBEM \_ KILLCOMBOFOCUS**](cbem-killcombofocus.md)     | Esta mensagem não está implementada. <br/>                                                                                                                                                               |
| [**CBEM \_ SETCOMBOFOCUS**](cbem-setcombofocus.md)       | Esta mensagem não está implementada. <br/>                                                                                                                                                               |
| [**CBEM \_ SETextendedattribute**](cbem-setextendedstyle.md) | Define os estilos estendidos dentro de um controle ComboBoxEx. <br/>                                                                                                                                              |
| [**CBEM \_ SETimagelist**](cbem-setimagelist.md)         | Define uma lista de imagens para um controle ComboBoxEx. <br/>                                                                                                                                                   |
| [**CBEM \_ SETITEM**](cbem-setitem.md)                   | Define os atributos de um item em um controle ComboBoxEx. <br/>                                                                                                                                       |
| [**CBEM \_ SETUNICODEFORMAT**](cbem-setunicodeformat.md) | Define o sinalizador de formato de caractere UNICODE para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle. <br/>      |
| [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md)     | Define o estilo visual de um controle ComboBoxEx.<br/>                                                                                                                                                  |



 

### <a name="notifications"></a>Notificações



| Tópico                                                      | Sumário                                                                                                                                                                                                                                                     |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CBEN \_ BEGINEDIT](cben-beginedit.md)                      | Enviado quando o usuário ativa a lista suspensa ou clica na caixa de edição do controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                    |
| [CBEN \_ DELETEITEM](cben-deleteitem.md)                    | Enviado quando um item foi excluído. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                     |
| [CBEN \_ DRAGBEGIN](cben-dragbegin.md)                      | Enviado quando o usuário começa a arrastar a imagem do item exibido na parte de edição do controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                  |
| [CBEN \_ ENDEDIT](cben-endedit.md)                          | Enviado quando o usuário concluiu uma operação na caixa de edição ou selecionou um item na lista suspensa do controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                             |
| [CBEN \_ GETDISPINFO](cben-getdispinfo.md)                  | Enviado para recuperar informações de exibição sobre um item de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                             |
| [CBEN \_ INSERTITEM](cben-insertitem.md)                    | Enviado quando um novo item é inserido no controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                  |
| [NM \_ SetCursor (ComboBoxEx)](nm-setcursor-comboboxex-.md) | Notifica uma janela pai do controle ComboBoxEx que o controle está definindo o cursor em resposta a uma mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Estruturas



| Tópico                                    | Sumário                                                                                                                                                                                     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) | Contém informações sobre um item em um controle ComboBoxEx.<br/>                                                                                                                       |
| [**NMCBEDRAGBEGIN**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbedragbegina) | Contém informações usadas com o código de notificação [CBEN \_ DRAGBEGIN](cben-dragbegin.md) . <br/>                                                                                      |
| [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita)     | Contém informações sobre a conclusão de uma operação de edição em um controle ComboBoxEx. Essa estrutura é usada com o código de notificação [CBEN \_ ENDEDIT](cben-endedit.md) . <br/> |
| [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)     | Contém informações específicas para itens de ComboBoxEx para uso com códigos de notificação. <br/>                                                                                               |



 

### <a name="constants"></a>Constantes



| Tópico                                                                        | Sumário                                                                                                                  |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Estilos estendidos do controle ComboBoxEx](comboboxex-control-extended-styles.md) | Dê suporte aos estilos estendidos listados nesta seção, bem como a maioria dos estilos de controle de caixa de combinação padrão.<br/> |



 

 

