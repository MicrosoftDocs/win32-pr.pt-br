---
title: Personalizando caixas de diálogo comuns
description: Este tópico discute como usar caixas de diálogo comuns.
ms.assetid: 31ba9deb-32e6-455c-be0e-ff8bcc691c80
keywords:
- Biblioteca de caixa de diálogo comum, personalizando
- caixas de diálogo comuns, personalizando
- Personalizando caixas de diálogo comuns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6272cbff88b7544ea945851f4f347cb43031b93ae08852bc139c7fb7ca6dd91d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786116"
---
# <a name="customizing-common-dialog-boxes"></a>Personalizando caixas de diálogo comuns

Você pode usar as caixas de diálogo comuns em seu formulário padrão ou pode personalizá-las. Da perspectiva do usuário, o principal benefício da caixa de diálogo comum é sua aparência e funcionalidade consistentes do aplicativo para o aplicativo. Portanto, é importante que você personalize uma caixa de diálogo comum somente quando for absolutamente necessário para um aplicativo. Caso contrário, a aparência consistente e a interface de codificação simples são perdidas. As personalizações apropriadas deixam intactas o máximo possível dos controles originais. Aumentar o tamanho da caixa de diálogo ou adicionar novos controles no espaço já disponível na caixa de diálogo é uma personalização apropriada. Ocultar controles originais ou alterar a funcionalidade pretendida dos controles originais é uma personalização menos adequada.

Esta seção aborda os seguintes métodos para personalizar uma caixa de diálogo comum:

-   [Modelos personalizados](#custom-templates)
-   [Procedimentos de gancho para caixas de diálogo comuns](#hook-procedures-for-common-dialog-boxes)
-   [Mensagens de diálogo comuns](#common-dialog-messages)
-   [Suporte de ajuda](#help-support)
    -   [Ajuda contextual](#context-sensitive-help)
    -   [O botão ajuda](#the-help-button)

## <a name="custom-templates"></a>Modelos personalizados

As caixas de diálogo comuns têm modelos padrão que definem o número, o tipo e a posição dos controles padrão na caixa de diálogo. Você pode definir um modelo personalizado para conceder aos usuários acesso a controles adicionais que são exclusivos do seu aplicativo.

Para todas as caixas de diálogo comuns, exceto as caixas de diálogo **abrir** e **salvar como** no estilo do Explorer, você modifica o modelo padrão para criar um modelo personalizado que substitui o modelo padrão. O modelo personalizado define o tipo e a posição dos controles padrão, bem como quaisquer controles adicionais.

Quando você cria um modelo de caixa de diálogo personalizada modificando o modelo de caixa de diálogo padrão, certifique-se de que os identificadores para todos os controles adicionados sejam exclusivos e não entrem em conflito com os identificadores dos controles padrão. A tabela a seguir lista o nome do arquivo de modelo padrão e inclui o arquivo para cada um dos tipos de caixa de diálogo comuns.



| Tipo de caixa de diálogo               | Arquivo de modelo | Arquivo de inclusão |
|-------------------------------|---------------|--------------|
| **Cor**                     | Cor. Dlg     | ColorDlg. h   |
| **Localizar**                      | LocalizarTexto. Dlg  | Dlgs. h       |
| **Fonte**                      | Fonte. Dlg      | Dlgs. h       |
| **Abrir** (seleção múltipla) | FileOpen. Dlg  | Dlgs. h       |
| **Abrir** (seleção única)   | FileOpen. Dlg  | Dlgs. h       |
| **Configuração de página**                | Prnsetup. Dlg  | Dlgs. h       |
| **Imprimir**                     | Prnsetup. Dlg  | Dlgs. h       |
| **Configuração de impressão** (obsoleto)    | Prnsetup. Dlg  | Dlgs. h       |
| **Substituir**                   | LocalizarTexto. Dlg  | Dlgs. h       |



 

Para habilitar um modelo personalizado, você deve definir um sinalizador no membro **flags** da estrutura correspondente para a caixa de diálogo. Se o modelo for um recurso em um aplicativo ou em uma biblioteca de vínculo dinâmico, defina um sinalizador **PREaptotemplate** no membro **flags** e use os membros **HINSTANCE** e **lpTemplateName** da estrutura para identificar o módulo e o nome do recurso. Se o modelo já estiver na memória, defina um sinalizador **ENABLETEMPLATEHANDLE** no membro **flags** e use o membro **HINSTANCE** para identificar o objeto de memória que contém o modelo.

Na maioria dos casos, você também deve habilitar um procedimento de gancho para a caixa de diálogo dar suporte e processar a entrada para os controles adicionais em seu modelo personalizado.

Para as caixas de diálogo **abrir** e **salvar como** no estilo do Gerenciador, os modelos padrão não estão disponíveis para modificação. Em vez disso, o modelo personalizado define uma caixa de diálogo filho que inclui apenas os itens a serem adicionados à caixa de diálogo padrão. O modelo personalizado também pode definir um controle estático que especifica o local do cluster de controles padrão na caixa de diálogo filho. Para obter mais informações, consulte [modelos personalizados de estilo do Explorer](open-and-save-as-dialog-boxes.md).

## <a name="hook-procedures-for-common-dialog-boxes"></a>Procedimentos de gancho para caixas de diálogo comuns

Para cada uma das caixas de diálogo comuns, você pode habilitar um procedimento de gancho para processar mensagens do procedimento de caixa de diálogo padrão. Há dois tipos gerais de procedimentos de conexão de caixa de diálogo comuns:

-   O procedimento de gancho padrão usado com as caixas de diálogo mais comuns
-   O procedimento de gancho de estilo de Gerenciador com suporte nas caixas de diálogo **abrir** e **salvar como**

Quando você fornece um procedimento de gancho padrão para uma das caixas de diálogo comuns, o procedimento de caixa de diálogo padrão manipula suas mensagens da seguinte maneira.



| Mensagem                                 | Tratar                                                                                                                                                                                                             |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INITDIALOG do WM \_**](wm-initdialog.md) | O procedimento de caixa de diálogo padrão processa a mensagem antes de passá-la para o procedimento de gancho. O parâmetro *lParam* da mensagem é um ponteiro para a estrutura de inicialização especificada quando a caixa de diálogo foi criada. |
| Todas as outras mensagens                      | O procedimento de gancho recebe a mensagem primeiro. Em seguida, o valor de retorno do procedimento de gancho determina se o procedimento de caixa de diálogo padrão processa a mensagem ou a ignora.                                     |



 

Para as caixas de diálogo **abrir** e **salvar como** no estilo do Gerenciador, o procedimento de gancho não recebe mensagens destinadas aos controles padrão na caixa de diálogo. Em vez disso, ele recebe mensagens de notificação da caixa de diálogo e mensagens para todos os controles adicionais que você definiu em um modelo personalizado. Para obter mais informações, consulte [procedimentos de gancho de estilo de Gerenciador](open-and-save-as-dialog-boxes.md).

Para habilitar um procedimento de gancho, defina um valor **ENABLEHOOK** no membro **flags** da estrutura correspondente para a caixa de diálogo. Se um sinalizador **ENABLEHOOK** for definido, um membro **lpfnHook** da estrutura deverá especificar o endereço do procedimento de gancho.

A tabela a seguir mostra o tipo de procedimento de gancho a ser fornecido para cada uma das caixas de diálogo comuns.



| Tipo de caixa de diálogo                          | Procedimento de gancho                                      |
|------------------------------------------|-----------------------------------------------------|
| **Cor**                                | [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)                      |
| **Localizar** ou **substituir**                  | [*FRHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)                      |
| **Fonte**                                 | [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)                      |
| **Abrir** ou **salvar como** (estilo Explorer) | [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)                    |
| **Abrir** ou **salvar como** (estilo antigo)      | [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) |
| **Imprimir**                                | [*PrintHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)                |
| **Configuração de página**                           | [*PageSetupHook*](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)                |



 

Para a **caixa de diálogo Configuração** de Página, você também pode especificar um procedimento de gancho [*PagePaintHook.*](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) Esse é um procedimento de gancho especial que você pode usar para personalizar a aparência da página de exemplo exibida pela caixa **de diálogo Configuração** da Página .

> [!Note]  
> A **caixa de diálogo** Instalação de Impressão foi superada pela caixa de diálogo **Configuração** de Página . Os aplicativos devem usar a **caixa de diálogo Configuração** de Página. No entanto, para compatibilidade, a [**função PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) continua a dar suporte à exibição da caixa **de diálogo Instalação** de Impressão. Você pode fornecer um procedimento de gancho [*SetupHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc) para a caixa **de diálogo Instalação de** Impressão.

 

## <a name="common-dialog-messages"></a>Mensagens de diálogo comuns

Caixas de diálogo comuns usam mensagens para notificar o procedimento de janela ou o procedimento de gancho quando determinados eventos ocorrem. Além disso, há mensagens que você pode enviar para uma caixa de diálogo comum para recuperar informações ou para controlar o comportamento ou a aparência da caixa de diálogo. Esta seção descreve as mensagens de diálogo comuns registradas pela função  [**RegisterWindowMessage,**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) as mensagens usadas pela  caixa de diálogo Fonte e pela caixa de diálogo Configuração de Página e as mensagens usadas pelas caixas de diálogo Abrir e Salvar **como** no estilo Explorer. 

A Biblioteca de Caixas de Diálogo Comuns define um conjunto de cadeias de caracteres de mensagem. Você pode passar uma constante associada a uma dessas cadeias de caracteres de mensagem para [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter um identificador de mensagem. Em seguida, você pode usar o identificador para detectar e processar mensagens enviadas de uma caixa de diálogo comum ou para enviar mensagens para uma caixa de diálogo comum. A tabela a seguir mostra as constantes de mensagem e descreve seu uso.



| Contants                               | Usar                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLOROKSTRING**](colorokstring.md) | Uma **caixa de** diálogo Cor envia essa mensagem para o procedimento de gancho quando o usuário seleciona uma cor e clica no botão **OK.** O procedimento de gancho pode aceitar a cor ou rejeitá-la e forçar a caixa de diálogo a permanecer aberta.                                                                                                                                                                                             |
| [**FILEOKSTRING**](fileokstring.md)   | Uma **caixa** de **diálogo** Abrir ou Salvar como envia essa mensagem para o procedimento de gancho quando o usuário seleciona um nome de arquivo e clica no **botão OK.** O procedimento de gancho pode aceitar o nome do arquivo ou rejeitá-lo e forçar a caixa de diálogo a permanecer aberta. Para caixas de diálogo **Abrir** e Salvar **como** no estilo explorer, essa mensagem foi superada pela mensagem CDN notificação [**\_ FILEOK.**](cdn-fileok.md)<br/> |
| [**FINDMSGSTRING**](findmsgstring.md) | Uma **caixa** **de** diálogo Encontrar ou Substituir envia essa mensagem para o procedimento de janela de sua janela pai quando o usuário clica na caixa de diálogo Encontrar Próximo **,** Substituir ou Substituir Tudo ou fecha a caixa de diálogo. O parâmetro *lParam* da mensagem é um ponteiro para uma [**estrutura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) que contém a entrada do usuário.                                                                               |
| [**HELPMSGSTRING**](helpmsgstring.md) | Todas as caixas de diálogo comuns enviam essa mensagem para o procedimento de janela da janela pai quando o usuário clica no **botão Ajuda.** Para caixas de diálogo **Abrir** e Salvar **como** no estilo Explorer, essa mensagem foi superada pela CDN [**\_ de**](cdn-help.md) notificação da AJUDA.<br/>                                                                                                                    |
| [**LBSELCHSTRING**](lbselchstring.md) | Uma **caixa** de **diálogo** Abrir ou Salvar como envia essa mensagem para o procedimento de gancho quando o usuário altera a seleção na caixa **de listagem Nome** do Arquivo . Para caixas  de diálogo Abrir e Salvar **como** no estilo explorer, essa mensagem foi superada pela mensagem CDN notificação [**\_ SELCHANGE.**](cdn-selchange.md)<br/>                                                                                           |
| [**SETRGBSTRING**](setrgbstring.md)   | Um procedimento de gancho pode enviar essa mensagem para uma caixa **de diálogo** Cor para definir a seleção de cores atual.                                                                                                                                                                                                                                                                                                                   |
| [**SHAREVISTRING**](sharevistring.md) | Uma **caixa** de **diálogo** Abrir ou Salvar como enviará essa mensagem para o procedimento de gancho se ocorrer uma violação de compartilhamento para o arquivo selecionado quando o usuário clicar no **botão OK.** Para caixas  de diálogo Abrir e Salvar **como** no estilo explorer, essa mensagem foi superada pela mensagem CDN notificação [**\_ SHAREVIOLATION.**](cdn-shareviolation.md)<br/>                                                        |



 

Algumas caixas de diálogo comuns enviam e recebem outras mensagens de janela. O procedimento de gancho para uma **caixa de** diálogo Fonte pode enviar qualquer uma das mensagens **WM \_ CHOOSEFONT _ \_ \* *para*** a caixa de diálogo _ Fonte. Para obter mais informações, consulte [Caixa de diálogo Fonte](font-dialog-box.md). A **caixa de diálogo** Configuração de Página envia as mensagens * WM *\_ PSD \_ \** _ se você habilitar um procedimento de gancho [_PagePaintHook*.](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) Para obter mais informações, consulte [Caixa de diálogo Configuração de Página](page-setup-dialog-box.md).

As caixas de diálogo **Abrir** e **Salvar como** no estilo Explorer são suportadas por um conjunto de mensagens predefinidos. Isso inclui mensagens de notificação enviadas na forma de uma mensagem [**WM \_ NOTIFY**](../controls/wm-notify.md) para o procedimento de gancho e mensagens que o procedimento de gancho pode enviar para a caixa de diálogo. Para ver uma lista completa dessas mensagens, consulte [Procedimentos de gancho no estilo explorer.](open-and-save-as-dialog-boxes.md)

## <a name="help-support"></a>Suporte da Ajuda

Caixas de diálogo comuns fornecem ajuda contextul para os controles padrão da caixa de diálogo. Para fornecer ajuda adicional para uma caixa  de diálogo comum, você pode exibir um botão ajuda e processar mensagens geradas quando o usuário clica no botão. O **botão** Ajuda é um suplemento para a ajuda contextuletivo padrão. O **botão** Ajuda é útil para descrever a finalidade geral da caixa de diálogo como ela se aplica ao seu aplicativo.

-   [Ajuda contextitivo](#context-sensitive-help)
-   [O botão Ajuda](#the-help-button)

### <a name="context-sensitive-help"></a>Context-Sensitive ajuda

Todas as caixas de diálogo comuns fornecem ajuda contextul para os controles padrão da caixa de diálogo. O usuário pode exibir ajuda para controles individuais por qualquer um dos seguintes métodos:

-   Selecionando o controle e pressionando a tecla F1.
-   Clicando no **?** botão na barra de título e, subsequentemente, clicando em um controle .
-   Clicando no botão direito do mouse sobre um controle.

Se você personalizar uma caixa de diálogo adicionando novos controles, também deverá estender o suporte de ajuda para esses controles processando solicitações de ajuda no procedimento de gancho. O procedimento de gancho recebe as seguintes mensagens quando o usuário solicita ajuda.



| Ação do usuário                                                           | Mensagem                                      |
|-----------------------------------------------------------------------|----------------------------------------------|
| Clique no botão direito do mouse sobre um controle.                          | [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) |
| Pressione a tecla F1.                                                   | [**AJUDA DO WM \_**](../shell/wm-help.md)               |
| Clicou no **?** botão na barra de título e, em seguida, clique em um controle . | [**AJUDA DO WM \_**](../shell/wm-help.md)               |



 

Você deve processar essas mensagens para os controles que adicionou, mas permitir que o procedimento de caixa de diálogo padrão processe as mensagens para os controles padrão. Para obter mais informações sobre como processar essas mensagens, consulte [Ajuda](/previous-versions/windows/desktop/legacy/bb776786(v=vs.85)).

### <a name="the-help-button"></a>O botão Ajuda

Você pode exibir um **botão Ajuda** em qualquer uma das caixas de diálogo comuns definindo um **valor SHOWHELP** no membro **Sinalizadores** da estrutura de inicialização da caixa de diálogo. Se você exibir o **botão Ajuda,** deverá processar a solicitação de ajuda do usuário. O processamento pode ser feito em um dos procedimentos de janela do aplicativo ou em um procedimento de gancho para a caixa de diálogo. Normalmente, você processaria a solicitação de ajuda chamando a [**função WinHelp.**](/windows/win32/api/winuser/nf-winuser-winhelpa)

Para processar mensagens de ajuda em um de seus procedimentos de janela, você deve obter um identificador de mensagem para a cadeia de caracteres definida pelo valor [**HELPMSGSTRING**](helpmsgstring.md) e identificar a janela para receber mensagens. Para obter o identificador da mensagem, **especifique HELPMSGSTRING** como o parâmetro em uma chamada para a [**função RegisterWindowMessage.**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) Ao criar a caixa de diálogo, use o membro **hwndOwner** da estrutura de inicialização da caixa de diálogo para identificar a janela que deve receber as mensagens. O procedimento da caixa de diálogo envia a mensagem para o procedimento de janela sempre que o usuário clica no **botão Ajuda.**

Para processar mensagens de ajuda em um procedimento de gancho, você deve processar a [**mensagem WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) O procedimento de gancho fornece ajuda se *o parâmetro wParam* dessa mensagem indica que o usuário clicou no **botão Ajuda.** O identificador do botão **Ajuda** é a constante **pshHelp** definida no arquivo Dlgs.h.

Os procedimentos de gancho para as caixas de diálogo **Abrir** e Salvar **como** no estilo Explorer não recebem mensagens [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) para o **botão Ajuda.** Em vez disso, a caixa de diálogo envia uma CDN de notificação [**\_ da AJUDA**](cdn-help.md) para o procedimento de gancho quando o botão **Ajuda** é clicado.

 

