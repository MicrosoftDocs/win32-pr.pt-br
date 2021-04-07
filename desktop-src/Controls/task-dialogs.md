---
title: Caixa de diálogo tarefa
description: Esta seção contém informações sobre os elementos de programação usados com uma caixa de diálogo de tarefa. Uma caixa de diálogo de tarefa é semelhante ao, enquanto é muito mais flexível do que a de um quadro de mensagem básico.
ms.assetid: vs|controls|~\controls\taskdialogs\taskdialogs.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f115531b9f872c824e9d1822be07777b2bc439
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/24/2020
ms.locfileid: "103824061"
---
# <a name="task-dialog"></a>Caixa de diálogo tarefa

Esta seção contém informações sobre os elementos de programação usados com uma caixa de diálogo de tarefa. Uma caixa de *diálogo de tarefa* é semelhante ao, enquanto é muito mais flexível do que a de um quadro de mensagem básico.

### <a name="overviews"></a>Visões gerais



| Tópico                                           | Sumário                                            |
|-------------------------------------------------|-----------------------------------------------------|
| [Sobre caixas de diálogo de tarefas](task-dialogs-overview.md) | Descreve os elementos de uma caixa de diálogo de tarefa.<br/> |



 

### <a name="functions"></a>Funções



| Tópico                                                  | Sumário                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog)                       | Cria, exibe e opera uma caixa de diálogo de tarefa. A caixa de diálogo tarefa contém texto e título de mensagem definidos pelo aplicativo, ícones e qualquer combinação de botões de push predefinidos. Essa função não oferece suporte ao registro de uma função de retorno de chamada para receber notificações.<br/>                                                                                                                |
| [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) | Uma função definida pelo aplicativo usada com a função [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Ele recebe mensagens da caixa de diálogo de tarefas quando ocorrem vários eventos.<br/> O tipo **PFTASKDIALOGCALLBACK** define um ponteiro para essa função de retorno de chamada. [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) é um espaço reservado para o nome da função definida pelo aplicativo.<br/> |
| [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)       | Cria, exibe e opera uma caixa de diálogo de tarefa. A caixa de diálogo tarefa contém ícones definidos pelo aplicativo, mensagens, títulos, caixas de seleção de verificação, links de comando, botões de push e botões de opção. Essa função pode registrar uma função de retorno de chamada para receber mensagens de notificação.<br/>                                                                                                               |



 

### <a name="messages"></a>Mensagens



| Tópico                                                                                           | Sumário                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_botão de clique do TDM \_**](tdm-click-button.md)                                                  | Simula a ação de um clique de botão em uma caixa de diálogo de tarefa.<br/>                                                                                                                                  |
| [**\_botão de \_ opção de clique do TDM \_**](tdm-click-radio-button.md)                                     | Simula a ação de um botão de opção clique em uma caixa de diálogo de tarefa.<br/>                                                                                                                            |
| [**\_verificação de clique TDM \_**](tdm-click-verification.md)                                      | Simula a ação de uma caixa de seleção de verificação clique em uma caixa de diálogo de tarefa.<br/>                                                                                                                   |
| [**\_botão habilitar \_ TDM**](tdm-enable-button.md)                                                | Habilita ou desabilita um botão de ação em uma caixa de diálogo de tarefa.<br/>                                                                                                                                       |
| [**\_botão de \_ opção \_ habilitar TDM**](tdm-enable-radio-button.md)                                   | Habilita ou desabilita um botão de opção em uma caixa de diálogo de tarefa.<br/>                                                                                                                                      |
| [**\_página de navegação TDM \_**](tdm-navigate-page.md)                                                | Recria uma caixa de diálogo de tarefa com novo conteúdo, simulando a funcionalidade de um assistente de várias páginas.<br/>                                                                                           |
| [**\_ \_ \_ estado necessário da elevação do botão \_ de TDM Set \_**](tdm-set-button-elevation-required-state.md) | Especifica se um determinado botão de diálogo de tarefa ou link de comando deve ter um ícone de escudo de UAC (controle de conta de usuário); ou seja, se a ação invocada pelo botão requer elevação. <br/> |
| [**\_texto do \_ elemento do conjunto de TDM \_**](tdm-set-element-text.md)                                         | Atualiza um elemento de texto em uma caixa de diálogo de tarefa.<br/>                                                                                                                                                  |
| [**\_barra de \_ progresso do letreiro de conjunto de TDM \_ \_**](tdm-set-marquee-progress-bar.md)                        | Indica se a barra de progresso hospedada deve ser exibida no modo de letreiro.<br/>                                                                                                            |
| [**\_letreiro da \_ barra de progresso do conjunto de TDM \_ \_**](tdm-set-progress-bar-marquee.md)                        | Inicia e interrompe a exibição do letreiro da barra de progresso e define a velocidade do letreiro.<br/>                                                                                              |
| [**\_PDV de \_ barra de progresso do conjunto de TDM \_ \_**](tdm-set-progress-bar-pos.md)                                | Define a posição atual de uma barra de progresso.<br/>                                                                                                                                             |
| [**\_intervalo da \_ barra de progresso do conjunto de TDM \_ \_**](tdm-set-progress-bar-range.md)                            | Define os valores mínimo e máximo para a barra de progresso hospedado.<br/>                                                                                                                          |
| [**\_estado da \_ barra de progresso do conjunto TDM \_ \_**](tdm-set-progress-bar-state.md)                            | Define o estado atual da barra de progresso.<br/>                                                                                                                                               |
| [**\_texto do \_ elemento de atualização TDM \_**](tdm-update-element-text.md)                                   | Atualiza um elemento de texto em uma caixa de diálogo de tarefa. <br/>                                                                                                                                                 |
| [**\_ícone de atualização TDM \_**](tdm-update-icon.md)                                                    | Atualiza o ícone de uma caixa de diálogo de tarefa. <br/>                                                                                                                                                     |



 

### <a name="notifications"></a>Notificações



| Tópico                                                           | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_botão TDN \_ clicado](tdn-button-clicked.md)                  | Enviado por uma caixa de diálogo de tarefa quando o usuário seleciona um botão ou link de comando na caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                   |
| [TDN \_ criado](tdn-created.md)                                 | Enviado por uma caixa de diálogo de tarefa depois que a caixa de diálogo de tarefa tiver sido criada e antes de ser exibida. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [TDN \_ destruído](tdn-destroyed.md)                             | Enviado por uma caixa de diálogo de tarefa quando é destruído e seu identificador de janela não é mais válido. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                       |
| [\_diálogo TDN \_ construído](tdn-dialog-constructed.md)          | Enviado por uma caixa de diálogo de tarefa depois que a caixa de diálogo de tarefa tiver sido criada e antes de ser exibida. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [\_botão TDN expando \_ \_ clicado](tdn-expando-button-clicked.md) | Enviado por uma caixa de diálogo de tarefa quando o usuário clica no botão expando da caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                            |
| [ajuda do TDN \_](tdn-help.md)                                       | Enviado por uma caixa de diálogo de tarefa quando o usuário pressiona F1 no teclado enquanto a caixa de diálogo de tarefa tem foco. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                            |
| [\_hiperlink TDN \_ clicado](tdn-hyperlink-clicked.md)            | Enviado por uma caixa de diálogo de tarefa quando o usuário clica em um hiperlink no conteúdo da caixa de diálogo da tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                        |
| [TDN \_ navegou](tdn-navigated.md)                             | Enviado por uma caixa de diálogo de tarefa quando ocorreu uma navegação. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                                                     |
| [\_botão de opção TDN \_ \_ clicado](tdn-radio-button-clicked.md)     | Enviado por uma caixa de diálogo de tarefa quando o usuário seleciona um botão ou link de comando na caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [\_temporizador TDN](tdn-timer.md)                                     | Enviado por uma caixa de diálogo de tarefa aproximadamente a cada 200 milissegundos. Esse código de notificação é enviado quando o \_ sinalizador do temporizador de retorno de chamada TDF foi \_ definido no membro **dwFlags** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que foi passada para a função [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método **TaskDialogIndirect** .<br/> |
| [verificação de TDN \_ \_ clicada](tdn-verification-clicked.md)      | Enviado pelo diálogo de tarefa quando o usuário clica na caixa de seleção de verificação da tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                       |



 

### <a name="structures"></a>Estruturas



| Tópico                                           | Sumário                                                                                                                                                   |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_botão TASKDIALOG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialog_button) | Contém informações usadas para exibir um botão em uma caixa de diálogo de tarefa. A estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usa essa estrutura.<br/> |
| [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)    | Contém informações usadas para exibir uma caixa de diálogo de tarefa. A função [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) usa essa estrutura.<br/>          |



 

 

