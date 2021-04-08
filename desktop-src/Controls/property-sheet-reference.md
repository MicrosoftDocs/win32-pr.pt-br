---
title: 'Folha de propriedades de '
description: Esta seção contém informações sobre elementos de programação usados com folhas de propriedades.
ms.assetid: f4fa9815-eab8-4b0b-ae5f-0bce4374223a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c42b7b4c1be7d0dc11613da36f78abbad847d6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917700"
---
# <a name="property-sheet"></a>Folha de propriedades de 

Esta seção contém informações sobre elementos de programação usados com folhas de propriedades.

### <a name="overviews"></a>Visões gerais



| Tópico                                              | Sumário                                                                                                                    |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Sobre folhas de propriedades](property-sheets.md)       | Uma *folha de propriedades* é uma janela que permite ao usuário exibir e editar as propriedades de um item.<br/>                  |
| [Criando assistentes](wizards.md)                    | Um assistente é um tipo de folha de propriedades que fornece uma maneira simples e poderosa de orientar os usuários por meio de um procedimento.<br/> |
| [Usando folhas de propriedades](using-property-sheets.md) | Esta seção fornece detalhes de implementação e código de exemplo para trabalhar com folhas de propriedades.<br/>                     |



 

### <a name="functions"></a>Funções



| Tópico                                                        | Sumário                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*AddPropSheetPageProc*](/windows/desktop/api/Prsht/nc-prsht-lpfnaddpropsheetpage)           | Especifica uma função de retorno de chamada definida pelo aplicativo que uma extensão de folha de propriedades usa para adicionar uma página a uma folha de propriedades.<br/>                                                                                                                      |
| [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)   | Cria uma nova página para uma folha de propriedades.<br/>                                                                                                                                                                                                        |
| [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) | Destrói uma página de folha de propriedades. Um aplicativo deve chamar essa função para páginas que não foram passadas para a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .<br/>                                                                              |
| [**Folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)                       | Cria uma folha de propriedades e adiciona as páginas definidas na estrutura de cabeçalho da folha de propriedades especificada.<br/>                                                                                                                                           |
| [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)                 | Especifica uma função de retorno de chamada definida pelo aplicativo que uma folha de propriedades chama quando uma página é criada e quando está prestes a ser destruída. Um aplicativo pode usar essa função para executar operações de inicialização e limpeza para a página.<br/> |
| [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback)                         | Uma função de retorno de chamada definida pelo aplicativo que o sistema chama quando a folha de propriedades está sendo criada e inicializada.<br/>                                                                                                                        |



 

### <a name="messages"></a>Mensagens



| Tópico                                                               | Sumário                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PSM \_ ADDPAGE**](psm-addpage.md)                                 | Adiciona uma nova página ao final de uma folha de propriedades existente. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet do \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .<br/>                                                                                                |
| [**aplicação de PSM \_**](psm-apply.md)                                     | Simula a seleção do botão **aplicar** , indicando que uma ou mais páginas foram alteradas e que as alterações precisam ser validadas e registradas.<br/>                                                                                                                   |
| [**CANCELTOCLOSE de PSM \_**](psm-canceltoclose.md)                     | Enviado por um aplicativo quando ele realizou alterações desde a notificação de [ \_ aplicação de PSN](psn-apply.md) mais recente que não pode ser cancelada. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .<br/> |
| [**PSM \_ alterado**](psm-changed.md)                                 | Informa uma folha de propriedades de que as informações em uma página foram alteradas. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) .<br/>                                                                                         |
| [**ENABLEWIZBUTTONS de PSM \_**](psm-enablewizbuttons.md)               | Habilita ou desabilita qualquer um dos botões padrão em um assistente Aero. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .<br/>                                                                          |
| [**GETCURRENTPAGEHWND de PSM \_**](psm-getcurrentpagehwnd.md)           | Recupera um identificador para a janela da página atual de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .<br/>                                                          |
| [**PSM \_ GETresult**](psm-getresult.md)                             | Usado por folhas de propriedades sem janela restrita para recuperar as informações retornadas às folhas de propriedades modais por [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta). Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetResult PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .<br/>                 |
| [**PSM \_ GETtabcontrol**](psm-gettabcontrol.md)                     | Recupera o identificador para o controle guia de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetTabControl PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) .<br/>                                                                                 |
| [**HWNDTOINDEX de PSM \_**](psm-hwndtoindex.md)                         | Usa o identificador de janela da página da folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) .<br/>                                                                  |
| [**IDTOINDEX de PSM \_**](psm-idtoindex.md)                             | Usa a ID de recurso de uma página de folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) .<br/>                                                                          |
| [**INDEXTOHWND de PSM \_**](psm-indextohwnd.md)                         | Usa o índice de uma página de folha de propriedades e retorna seu identificador de janela. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) .<br/>                                                                               |
| [**INDEXTOID de PSM \_**](psm-indextoid.md)                             | Obtém o índice de uma página de folha de propriedades e retorna sua ID de recurso. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .<br/>                                                                                     |
| [**INDEXTOPAGE de PSM \_**](psm-indextopage.md)                         | Obtém o índice de uma página de folha de propriedades e retorna seu identificador HPROPSHEETPAGE. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .<br/>                                                                       |
| [**INSERTPAGE de PSM \_**](psm-insertpage.md)                           | Insere uma nova página em uma folha de propriedades existente. A página pode ser inserida em um índice especificado ou após uma página especificada. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .<br/>                |
| [**ISDIALOGMESSAGE de PSM \_**](psm-isdialogmessage.md)                 | Passa uma mensagem para uma caixa de diálogo de folha de propriedades e indica se a caixa de diálogo processou a mensagem. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .<br/>                              |
| [**PAGETOINDEX de PSM \_**](psm-pagetoindex.md)                         | Usa o identificador HPROPSHEETPAGE da página da folha de propriedades e retorna seu índice de base zero. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .<br/>                                                          |
| [**PRESSBUTTON de PSM \_**](psm-pressbutton.md)                         | Simula a seleção de um botão de folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) .<br/>                                                                                              |
| [**QUERYSIBLINGS de PSM \_**](psm-querysiblings.md)                     | Enviado a uma folha de propriedades, que, em seguida, encaminha a mensagem para cada uma de suas páginas. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .<br/>                                                              |
| [**REBOOTSYSTEM de PSM \_**](psm-rebootsystem.md)                       | Indica que o sistema precisa ser reiniciado para que as alterações entrem em vigor. Você pode enviar a mensagem de [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) explicitamente ou usando a macro [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .<br/>                        |
| [**RECALCPAGESIZES de PSM \_**](psm-recalcpagesizes.md)                 | Recalcula o tamanho da página de uma folha de propriedades padrão ou do assistente depois que as páginas são adicionadas ou removidas. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .<br/>                                     |
| [**REMOVEPAGE de PSM \_**](psm-removepage.md)                           | Remove uma página de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .<br/>                                                                                                              |
| [**RESTARTWINDOWS de PSM \_**](psm-restartwindows.md)                   | Indica que o Windows precisa ser reiniciado para que as alterações entrem em vigor.<br/>                                                                                                                                                                                         |
| [**SETBUTTONTEXT de PSM \_**](psm-setbuttontext.md)                     | Define o texto em um botão em um assistente de Aero. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .<br/>                                                                                                 |
| [**PSM \_ SETcurseal**](psm-setcursel.md)                             | Ativa a página especificada em uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setcurseal PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .<br/>                                                                                                    |
| [**SETCURSELID de PSM \_**](psm-setcurselid.md)                         | Ativa a página determinada em uma folha de propriedades com base no identificador de recurso da página. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .<br/>                                                   |
| [**SETFINISHTEXT de PSM \_**](psm-setfinishtext.md)                     | Define o texto do botão **concluir** em um assistente, mostra e habilita o botão e oculta os botões **Avançar** e **voltar** . Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .<br/>               |
| [**SETHEADERBITMAP de PSM \_**](psm-setheaderbitmap.md)                 | Esta mensagem não está implementada.<br/>                                                                                                                                                                                                                                     |
| [**SETHEADERBITMAPRESOURCE de PSM \_**](psm-setheaderbitmapresource.md) | Esta mensagem não está implementada.<br/>                                                                                                                                                                                                                                     |
| [**SETHEADERSUBTITLE de PSM \_**](psm-setheadersubtitle.md)             | Define o texto do subtítulo para o cabeçalho da página interior de um assistente. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .<br/>                                                                        |
| [**SETHEADERTITLE de PSM \_**](psm-setheadertitle.md)                   | Define o texto do título do cabeçalho da página interior de um assistente. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .<br/>                                                                                 |
| [**SETNEXTTEXT de PSM \_**](psm-setnexttext.md)                         | Define o texto do botão **Avançar** em um assistente. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) .<br/>                                                                                                |
| [**PSM \_ SETtitle**](psm-settitle.md)                               | Define o título de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetTitle PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .<br/>                                                                                                                    |
| [**SETWIZBUTTONS de PSM \_**](psm-setwizbuttons.md)                     | Habilita ou desabilita os botões **voltar**, **Avançar** e **concluir** em um assistente. Você também pode usar a macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para postar a mensagem.<br/>                                                                          |
| [**SHOWWIZBUTTONS de PSM \_**](psm-showwizbuttons.md)                   | Mostra ou oculta botões em um assistente. Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .<br/>                                                                                                        |
| [**PSM \_ INalterado**](psm-unchanged.md)                             | Informa uma folha de propriedades que as informações em uma página foram revertidas para o estado salvo anteriormente. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ inalterada PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) .<br/>                                                      |



 

### <a name="notifications"></a>Notificações



| Tópico                                                     | Sumário                                                                                                                                                                                                                                                |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PSN \_ aplicar](psn-apply.md)                               | Enviado a cada página na folha de propriedades para indicar que o usuário clicou no botão OK, fechar ou aplicar e quer que todas as alterações entrem em vigor. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .<br/>      |
| [GetObject PSN \_](psn-getobject.md)                       | Enviado por uma folha de propriedades para solicitar um objeto de destino de soltar quando o cursor passa sobre um dos botões do controle de guia.<br/>                                                                                                                       |
| [ajuda do PSN \_](psn-help.md)                                 | Notifica uma página que o usuário clicou no botão ajuda. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                          |
| [PSN \_ KILLACTIVE](psn-killactive.md)                     | Notifica uma página de que ela está prestes a perder a ativação porque outra página está sendo ativada ou o usuário clicou no botão **OK** . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>       |
| [PSN \_ QUERYCANCEL](psn-querycancel.md)                   | Indica que o usuário cancelou a folha de propriedades. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                            |
| [PSN \_ QUERYINITIALFOCUS](psn-queryinitialfocus.md)       | Enviado por uma folha de propriedades para fornecer uma página de folha de propriedades a oportunidade de especificar qual controle de caixa de diálogo deve receber o foco inicial. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .<br/>           |
| [redefinição de PSN \_](psn-reset.md)                               | Notifica uma página que a folha de propriedades está prestes a ser destruída. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                   |
| [PSN \_ SETactive](psn-setactive.md)                       | Notifica uma página que está prestes a ser ativada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                   |
| [\_TRANSLATEACCELERATOR PSN](psn-translateaccelerator.md) | Notifica uma folha de propriedades de que uma mensagem do teclado foi recebida. Ele fornece à página uma oportunidade de fazer a tradução do acelerador de teclado privado. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .<br/> |
| [PSN \_ WIZBACK](psn-wizback.md)                           | Notifica uma página que o usuário clicou no botão **voltar** em um assistente. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                          |
| [PSN \_ WIZFINISH](psn-wizfinish.md)                       | Notifica uma página que o usuário clicou no botão **concluir** em um assistente. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                        |
| [PSN \_ WIZNEXT](psn-wiznext.md)                           | Notifica uma página que o usuário clicou no botão **Avançar** em um assistente. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                          |



 

### <a name="structures"></a>Estruturas



| Tópico                                      | Sumário                                                                   |
|--------------------------------------------|----------------------------------------------------------------------------|
| [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) | Define o quadro e as páginas de uma folha de propriedades.<br/>                |
| [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2)     | Define uma página em uma folha de propriedades.<br/>                             |
| [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)             | Contém informações para os códigos de notificação da folha de propriedades.<br/> |



 

 

