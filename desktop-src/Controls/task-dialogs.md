---
title: Caixa de diálogo Tarefa
description: Esta seção contém informações sobre os elementos de programação usados com uma caixa de diálogo de tarefa. Uma caixa de diálogo de tarefa é semelhante a, embora muito mais flexível do que, uma caixa de mensagem básica.
ms.assetid: vs|controls|~\controls\taskdialogs\taskdialogs.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6797314b75fff46ddf8a4f64638fefb5ea0181d2353bd1a1d3caa57325d28e7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168546"
---
# <a name="task-dialog"></a>Caixa de diálogo Tarefa

Esta seção contém informações sobre os elementos de programação usados com uma caixa de diálogo de tarefa. Uma *caixa de diálogo* de tarefa é semelhante a, embora muito mais flexível do que, uma caixa de mensagem básica.

### <a name="overviews"></a>Visões gerais



| Tópico                                           | Sumário                                            |
|-------------------------------------------------|-----------------------------------------------------|
| [Sobre caixas de diálogo de tarefa](task-dialogs-overview.md) | Descreve os elementos de uma caixa de diálogo de tarefa.<br/> |



 

### <a name="functions"></a>Funções



| Tópico                                                  | Sumário                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog)                       | Cria, exibe e opera uma caixa de diálogo de tarefa. A caixa de diálogo de tarefa contém texto e título de mensagem definidos pelo aplicativo, ícones e qualquer combinação de botões de push predefinidos. Essa função não dá suporte ao registro de uma função de retorno de chamada para receber notificações.<br/>                                                                                                                |
| [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) | Uma função definida pelo aplicativo usada com a [**função TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) Ele recebe mensagens da caixa de diálogo de tarefa quando vários eventos ocorrem.<br/> O **tipo PFTASKDIALOGCALLBACK** define um ponteiro para essa função de retorno de chamada. [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) é um espaço reservado para o nome da função definida pelo aplicativo.<br/> |
| [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)       | Cria, exibe e opera uma caixa de diálogo de tarefa. A caixa de diálogo de tarefa contém ícones definidos pelo aplicativo, mensagens, título, caixa de seleção de verificação, links de comando, botões de push e botões de rádio. Essa função pode registrar uma função de retorno de chamada para receber mensagens de notificação.<br/>                                                                                                               |



 

### <a name="messages"></a>Mensagens



| Tópico                                                                                           | Sumário                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BOTÃO DE CLIQUE DO \_ TDM \_**](tdm-click-button.md)                                                  | Simula a ação de um clique de botão em uma caixa de diálogo de tarefa.<br/>                                                                                                                                  |
| [**BOTÃO DE RÁDIO CLIQUE EM TDM \_ \_ \_**](tdm-click-radio-button.md)                                     | Simula a ação de um clique de botão de rádio em uma caixa de diálogo de tarefa.<br/>                                                                                                                            |
| [**VERIFICAÇÃO DE CLIQUE DO TDM \_ \_**](tdm-click-verification.md)                                      | Simula a ação de uma caixa de seleção de verificação clicando em uma caixa de diálogo de tarefa.<br/>                                                                                                                   |
| [**BOTÃO HABILITAR TDM \_ \_**](tdm-enable-button.md)                                                | Habilita ou desabilita um botão de push em uma caixa de diálogo de tarefa.<br/>                                                                                                                                       |
| [**BOTÃO DE RÁDIO HABILITAR TDM \_ \_ \_**](tdm-enable-radio-button.md)                                   | Habilita ou desabilita um botão de rádio em uma caixa de diálogo de tarefa.<br/>                                                                                                                                      |
| [**PÁGINA NAVEGAÇÃO DO \_ TDM \_**](tdm-navigate-page.md)                                                | Recria uma caixa de diálogo de tarefa com novos conteúdos, simulando a funcionalidade de um assistente de várias páginas.<br/>                                                                                           |
| [**ESTADO NECESSÁRIO \_ DA \_ \_ ELEVAÇÃO DO BOTÃO \_ \_ DE CONJUNTO DE TDM**](tdm-set-button-elevation-required-state.md) | Especifica se um determinado botão de diálogo de tarefa ou link de comando deve ter um ícone de blindagem UAC (Controle de Conta de Usuário). ou seja, se a ação invocada pelo botão requer elevação. <br/> |
| [**TEXTO DO ELEMENTO SET \_ \_ TDM \_**](tdm-set-element-text.md)                                         | Atualiza um elemento de texto em uma caixa de diálogo de tarefa.<br/>                                                                                                                                                  |
| [**BARRA DE PROGRESSO DO TDM \_ SET \_ \_ MARQUEE \_**](tdm-set-marquee-progress-bar.md)                        | Indica se a barra de progresso hospedada deve ser exibida no modo de letreiro.<br/>                                                                                                            |
| [**MARCA DE BARRA DE PROGRESSO DO CONJUNTO DE \_ \_ \_ \_ TDM**](tdm-set-progress-bar-marquee.md)                        | Inicia e interrompe a exibição do letreiro da barra de progresso e define a velocidade do letreiro.<br/>                                                                                              |
| [**POS DA BARRA DE PROGRESSO DO CONJUNTO DE TDM \_ \_ \_ \_**](tdm-set-progress-bar-pos.md)                                | Define a posição atual para uma barra de progresso.<br/>                                                                                                                                             |
| [**INTERVALO DE BARRAS DE PROGRESSO DO CONJUNTO DE TDM \_ \_ \_ \_**](tdm-set-progress-bar-range.md)                            | Define os valores mínimo e máximo para a barra de progresso hospedada.<br/>                                                                                                                          |
| [**ESTADO DA BARRA DE PROGRESSO DO CONJUNTO DE TDM \_ \_ \_ \_**](tdm-set-progress-bar-state.md)                            | Define o estado atual da barra de progresso.<br/>                                                                                                                                               |
| [**TEXTO DO ELEMENTO UPDATE DO TDM \_ \_ \_**](tdm-update-element-text.md)                                   | Atualiza um elemento de texto em uma caixa de diálogo de tarefa. <br/>                                                                                                                                                 |
| [**ÍCONE DE ATUALIZAÇÃO DO TDM \_ \_**](tdm-update-icon.md)                                                    | Atualiza o ícone de uma caixa de diálogo de tarefa. <br/>                                                                                                                                                     |



 

### <a name="notifications"></a>Notificações



| Tópico                                                           | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BOTÃO TDN \_ \_ CLICADO](tdn-button-clicked.md)                  | Enviado por uma caixa de diálogo de tarefa quando o usuário seleciona um botão ou um link de comando na caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                   |
| [TDN \_ CRIADO](tdn-created.md)                                 | Enviado por uma caixa de diálogo de tarefa após a criação da caixa de diálogo de tarefa e antes de ser exibida. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                  |
| [TDN \_ DESTRUÍDO](tdn-destroyed.md)                             | Enviado por uma caixa de diálogo de tarefa quando ela é destruída e seu alça de janela não é mais válido. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                       |
| [CAIXA DE DIÁLOGO \_ TDN \_ CONSTRUÍDA](tdn-dialog-constructed.md)          | Enviado por uma caixa de diálogo de tarefa após a criação da caixa de diálogo de tarefa e antes de ser exibida. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                  |
| [BOTÃO EXPANDIR \_ TDN \_ \_ CLICADO](tdn-expando-button-clicked.md) | Enviado por uma caixa de diálogo de tarefa quando o usuário clica no botão de expansão da caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                            |
| [AJUDA DO \_ TDN](tdn-help.md)                                       | Enviado por uma caixa de diálogo de tarefa quando o usuário pressiona F1 no teclado enquanto a caixa de diálogo de tarefa tem foco. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                            |
| [HIPERLINK TDN \_ \_ CLICADO](tdn-hyperlink-clicked.md)            | Enviado por uma caixa de diálogo de tarefa quando o usuário clica em um hiperlink no conteúdo da caixa de diálogo da tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                        |
| [TDN \_ NAVEGADO](tdn-navigated.md)                             | Enviado por uma caixa de diálogo de tarefa quando ocorreu uma navegação. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                                                     |
| [BOTÃO DE RÁDIO TDN \_ \_ \_ CLICADO](tdn-radio-button-clicked.md)     | Enviado por uma caixa de diálogo de tarefa quando o usuário seleciona um botão ou um link de comando na caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                  |
| [TEMPORIZADOR DE \_ TDN](tdn-timer.md)                                     | Enviado por uma caixa de diálogo de tarefa aproximadamente a cada 200 milissegundos. Esse código de notificação é enviado quando o sinalizador TIMER DE RETORNO DE CHAMADA do TDF foi definido no membro \_ \_ **dwFlags** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que foi passada para a [**função TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o **método TaskDialogIndirect.**<br/> |
| [VERIFICAÇÃO DE TDN \_ \_ CLICADA](tdn-verification-clicked.md)      | Enviado pela caixa de diálogo de tarefa quando o usuário clica na caixa de seleção de verificação da caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                       |



 

### <a name="structures"></a>Estruturas



| Tópico                                           | Sumário                                                                                                                                                   |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_botão TASKDIALOG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialog_button) | Contém informações usadas para exibir um botão em uma caixa de diálogo de tarefa. A estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usa essa estrutura.<br/> |
| [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)    | Contém informações usadas para exibir uma caixa de diálogo de tarefa. A função [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) usa essa estrutura.<br/>          |



 

 

