---
title: Editar operações de texto de controle
description: O sistema processa automaticamente todas as operações de texto iniciadas pelo usuário e notifica o aplicativo quando as operações são concluídas.
ms.assetid: 9af3a1bc-4c87-4cc9-966d-50742be7c811
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9640616cf70b9a2933ef9d4c3fdb2accbfdcabf0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008427"
---
# <a name="edit-control-text-operations"></a>Editar operações de texto de controle

O sistema processa automaticamente todas as operações de texto iniciadas pelo usuário e notifica o aplicativo quando as operações são concluídas.

Os tópicos a seguir abordam as operações de texto iniciadas pelo usuário e a resposta do aplicativo:

-   [Selecionando um controle de edição](#selecting-an-edit-control)
-   [Configurando e recuperando texto](#setting-and-retrieving-text)
-   [Selecionando texto](#selecting-text)
-   [Substituindo texto](#replacing-text)
-   [Alterando a fonte usada por um controle de edição](#changing-the-font-used-by-an-edit-control)
-   [Operações de recortar cópia colar e limpar](#cut-copy-paste-and-clear-operations)
-   [Modificando texto](#modifying-text)
-   [Limitando texto digitado pelo usuário](#limiting-user-entered-text)
-   [Operações de caractere e linha](#character-and-line-operations)
-   [Rolando o texto em um controle de edição](#scrolling-text-in-an-edit-control)
-   [Configurando tabulações e margens](#setting-tab-stops-and-margins)
-   [Ocultando a entrada do usuário](#concealing-user-input)
-   [Usando números inteiros](#using-integers)
-   [Desfazendo operações de texto](#undoing-text-operations)
-   [Manipulação de linhas e quebras de linha](#handling-wordwrap-and-line-breaks)
-   [Recuperando pontos e caracteres](#retrieving-points-and-characters)
-   [Preenchimento automático de cadeias de caracteres](#autocompletion-of-strings)
-   [Script complexo em controles de edição](#complex-script-in-edit-controls)

## <a name="selecting-an-edit-control"></a>Selecionando um controle de edição

O usuário pode selecionar um controle de edição clicando nele com o mouse ou pressionando a tecla TAB para movê-lo. O método de tabulação faz parte de uma interface de teclado predefinida que o sistema fornece. Para obter uma descrição completa desta interface, consulte [caixas de diálogo](/windows/desktop/dlgbox/dialog-boxes). Quando o usuário seleciona um controle de edição, o sistema dá ao controle o foco do teclado (consulte "foco e ativação do teclado" em [sobre a entrada do teclado](/windows/desktop/inputdev/about-keyboard-input)) e realça seu texto usando o vídeo inverso.

## <a name="setting-and-retrieving-text"></a>Configurando e recuperando texto

Um aplicativo pode definir o texto de um controle de edição usando a função [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) , a função [**SetDlgItemText**](/windows/desktop/DevNotes/-setdlgitemtext) ou enviando o controle de uma mensagem do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) .

Para recuperar todo o texto de um controle de edição, primeiro use a função [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) ou a mensagem [**\_ GETTEXTLENGTH do WM**](/windows/desktop/winmsg/wm-gettextlength) para determinar o tamanho do buffer necessário para conter o texto. Em seguida, recupere o texto usando a função [**GetWindowText**](/windows/desktop/DevNotes/-getwindowtext) , a função [**GetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta) ou a mensagem de [**\_ gettext do WM**](/windows/desktop/winmsg/wm-gettext) .

## <a name="selecting-text"></a>Selecionando texto

Depois de selecionar um controle de edição, o usuário pode selecionar o texto no controle usando o mouse ou o teclado. Um aplicativo pode recuperar as posições de caractere inicial e final da seleção atual em um controle de edição enviando o controle uma mensagem em [**\_ GETSEL**](em-getsel.md) . O valor de retorno para a posição final é um maior que o último caractere na seleção (ou seja, a posição do primeiro caractere após o último caractere selecionado).

Um aplicativo também pode selecionar texto em um controle de edição enviando ao controle uma mensagem em [**\_ SETSEL**](em-setsel.md) com os índices de caracteres inicial e final para a seleção. Por exemplo, o aplicativo pode usar **em \_ SETSEL** com [**em \_ REPLACESEL**](em-replacesel.md) para excluir texto de um controle de edição.

Essas três mensagens se aplicam a controles de linha única e de edição de várias linhas.

## <a name="replacing-text"></a>Substituindo texto

Um aplicativo pode substituir o texto selecionado em um controle de edição enviando ao controle uma mensagem em [**\_ REPLACESEL**](em-replacesel.md) com um ponteiro para o texto de substituição. Se não houver seleção atual, em **\_ REPLACESEL** inserirá o texto de substituição no ponto de inserção. O aplicativo poderá receber um código de notificação [en \_ ERRSPACE](en-errspace.md) se o texto de substituição exceder a memória disponível. Essa mensagem se aplica a controles de linha única e de edição de várias linhas.

Um aplicativo pode usar [**em \_ REPLACESEL**](em-replacesel.md) para substituir parte do texto de um controle de edição ou da função [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) para substituir tudo.

## <a name="changing-the-font-used-by-an-edit-control"></a>Alterando a fonte usada por um controle de edição

Um aplicativo pode alterar a fonte que um controle de edição usa enviando a mensagem de aplicativo do [**WM \_**](/windows/desktop/winmsg/wm-setfont) . A maioria dos aplicativos faz isso ao processar a mensagem [**\_ INITDIALOG do WM**](/windows/desktop/dlgbox/wm-initdialog) . Alterar a fonte não altera o tamanho do controle de edição; os aplicativos que enviam a mensagem de **\_ fonte** de aplicativo do WM podem precisar recuperar as métricas de fonte para o texto e recalcular o tamanho do controle de edição. Para obter mais informações sobre fontes e métricas de fontes, consulte [fontes e texto](/windows/desktop/gdi/fonts-and-text).

## <a name="cut-copy-paste-and-clear-operations"></a>Operações de recortar cópia colar e limpar

Há quatro mensagens para mover o texto entre um controle de edição e a área de transferência. A mensagem de [**\_ cópia do WM**](/windows/desktop/dataxchg/wm-copy) copia a seleção atual (se houver) de um controle de edição para a área de transferência sem excluí-la do controle de edição. A mensagem de [**\_ recorte do WM**](/windows/desktop/dataxchg/wm-cut) exclui a seleção atual (se houver) no controle de edição e copia o texto excluído para a área de transferência. A mensagem de [**\_ limpeza do WM**](/windows/desktop/dataxchg/wm-clear) exclui a seleção atual (se houver) de um controle de edição, mas não a copia para a área de transferência (a menos que o usuário tenha pressionado a tecla Shift). A mensagem de [**\_ colagem do WM**](/windows/desktop/dataxchg/wm-paste) copia o texto da área de transferência em um controle de edição no ponto de inserção. Essas quatro mensagens se aplicam a controles de linha única e de edição de várias linhas.

Microsoft Windows NT 4,0 e posterior: um controle de edição inclui um menu de contexto interno que torna mais fácil para o usuário mover o texto entre o controle de edição e a área de transferência. O menu de contexto é exibido quando o usuário clica com o botão direito do mouse no controle. Os comandos no menu de contexto incluem **desfazer**, **recortar**, **copiar**, **colar**, **excluir** e **selecionar tudo**.

## <a name="modifying-text"></a>Modificando texto

O usuário pode selecionar, excluir ou mover o texto em um controle de edição. O sistema mantém um sinalizador interno para cada controle de edição que indica se o conteúdo do controle foi modificado. O sistema limpa esse sinalizador quando cria o controle e define o sinalizador sempre que o texto no controle é modificado. Um aplicativo pode recuperar o sinalizador de modificação enviando o controle uma mensagem em [**\_ GetModify**](em-getmodify.md) . O aplicativo pode, então, definir ou limpar o sinalizador de modificação enviando o controle uma mensagem em [**\_ SetModify**](em-setmodify.md) . Essas mensagens se aplicam a controles de linha única e de edição de várias linhas.

## <a name="limiting-user-entered-text"></a>Limitando texto digitado pelo usuário

O limite padrão para a quantidade de texto que um usuário pode inserir em um controle de edição é 32 KB. Um aplicativo pode alterar o limite padrão enviando o controle uma mensagem [**em \_ SETLIMITTEXT**](em-setlimittext.md) . Essa mensagem define um limite rígido para o número de bytes que o usuário pode inserir em um controle de edição, mas que não afeta o texto que já está no controle quando a mensagem foi enviada nem texto copiado para o controle pela função [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) ou pela mensagem [**\_ SetText do WM**](/windows/desktop/winmsg/wm-settext) . Por exemplo, suponha que o aplicativo use a função **SetDlgItemText** para inserir 500 bytes em um controle de edição e o usuário também insira 500 bytes (total de 1.000 bytes). Se o aplicativo enviar uma mensagem em em **\_ SETLIMITTEXT** limitando o texto digitado pelo usuário a 300 bytes, os 1.000 bytes já no controle de edição permanecerão lá e o usuário não poderá adicionar mais nenhum texto. Por outro lado, se o aplicativo enviar uma mensagem **em \_ SETLIMITTEXT** limitando o texto digitado pelo usuário a 1.300 bytes, os 1.000 bytes permanecerão, mas o usuário poderá adicionar 300 mais bytes.

Quando o usuário atinge o limite de caracteres de um controle de edição, o sistema envia ao aplicativo uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) que contém um código de notificação [en \_ MAXTEXT](en-maxtext.md) . Este código de notificação não significa que a memória foi esgotada, mas que o limite de texto inserido pelo usuário foi atingido; o usuário não pode inserir mais texto. Para alterar esse limite, um aplicativo deve enviar ao controle uma nova mensagem em [**\_ SETLIMITTEXT**](em-setlimittext.md) com um limite superior.

Como exemplo do uso de em [**\_ SETLIMITTEXT**](em-setlimittext.md) e [en \_ MAXTEXT](en-maxtext.md), suponha que o aplicativo deve limitar o usuário a não mais do que quatro caracteres em um controle de edição. O aplicativo usaria em **\_ SETLIMITTEXT** para especificar um limite de quatro caracteres. Se o usuário tentou inserir um quinto caractere, o sistema enviaria um código de \_ notificação en MAXTEXT para o aplicativo.

## <a name="character-and-line-operations"></a>Operações de caractere e linha

Há várias mensagens que retornam informações sobre os caracteres e as linhas em um controle de edição. A maioria das mensagens retorna um índice, geralmente um número de base zero, para se referir a um caractere ou linha. Por exemplo, em um controle de edição de linha única que contém n caracteres, o índice de linha é zero e os caracteres são indexados de zero a n-1. Em um controle de edição de várias linhas que contém linhas m e n caracteres, as linhas são indexadas de zero para m-1 e os caracteres são indexados de zero a n-1. Observe que a indexação de caracteres ignora as quebras de linha.

Um aplicativo pode determinar o número de caracteres em um controle de edição enviando a mensagem do [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) para o controle de edição. Essa mensagem retorna o comprimento, em caracteres (sem incluir o caractere nulo de terminação), do texto em um controle de linha única ou de edição de várias linhas. A mensagem em [**\_ LINELENGTH**](em-linelength.md) retorna o comprimento, em caracteres, de uma linha especificada pelo índice de caracteres de um caractere na linha. O comprimento retornado não inclui nenhum caractere selecionado. Um aplicativo pode usar essas mensagens em um controle de linha única ou de edição de várias linhas.

A mensagem em [**\_ GETFIRSTVISIBLELINE**](em-getfirstvisibleline.md) retorna o índice de base zero da linha visível superior em um controle de edição de várias linhas ou o índice de base zero do primeiro caractere visível em um controle de edição de linha única. Um aplicativo pode copiar uma linha de um controle de edição para um buffer enviando a mensagem em [**\_ getline**](em-getline.md) para o controle de edição. A linha é especificada por seu índice de linha e a primeira palavra do buffer de recebimento contém o número máximo de bytes a serem copiados para o buffer. O valor de retorno é o número de bytes copiados. Essa mensagem também pode ser usada em um controle de linha única ou de edição de várias linhas.

Há mensagens exclusivas disponíveis para retornar as informações sobre uma linha em um controle de edição de várias linhas. A mensagem em [**\_ GETLINECOUNT**](em-getlinecount.md) retorna o número de linhas em um controle de edição. A mensagem em [**\_ LINEFROMCHAR**](em-linefromchar.md) retorna o índice da linha que contém um índice de caracteres especificado. A mensagem em [**\_ LINEINDEX**](em-lineindex.md) retorna o índice do primeiro caractere em uma linha especificada.

## <a name="scrolling-text-in-an-edit-control"></a>Rolando o texto em um controle de edição

Para implementar a rolagem em um controle de edição, você pode usar os estilos de rolagem automática abordados em [Editar tipos de controle e estilos](about-edit-controls.md), ou você pode adicionar explicitamente barras de rolagem ao controle de edição. Para adicionar uma barra de rolagem horizontal, use o estilo WS \_ HSCROLL; para adicionar uma barra de rolagem vertical, use o estilo [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles). Um controle de edição com barras de rolagem processa suas próprias mensagens da barra de rolagem. Para obter informações detalhadas sobre como adicionar barras de rolagem a controles de edição, consulte [barras de rolagem](scroll-bars.md).

O sistema fornece três mensagens que um aplicativo pode enviar para um controle de edição com barras de rolagem. A mensagem em [**\_ LINESCROLL**](em-linescroll.md) pode rolar um controle de edição de várias linhas vertical e horizontalmente. O parâmetro *lParam* especifica o número de linhas a serem roladas verticalmente a partir da linha atual e o parâmetro *wParam* especifica o número de caracteres a rolar horizontalmente, começando do caractere atual. O controle de edição não reconhece mensagens de rolagem horizontais se tiver o estilo [**es \_ Center**](edit-control-styles.md) ou [**es \_ Right**](edit-control-styles.md) . A mensagem em **\_ LINESCROLL** aplica-se somente a controles de edição de várias linhas.

A mensagem de [**\_ rolagem**](em-scroll.md) em em rola um controle de edição de várias linhas verticalmente. O parâmetro *wParam* especifica a ação de rolagem. A mensagem de **\_ rolagem** em em aplica-se somente a controles de edição de várias linhas. **Em \_ SCROLL** tem o mesmo efeito que a [**mensagem \_ VSCROLL do WM**](wm-vscroll.md) .

A mensagem em [**\_ SCROLLCARET**](em-scrollcaret.md) rola o cursor para a exibição em um controle de edição.

## <a name="setting-tab-stops-and-margins"></a>Configurando tabulações e margens

Um aplicativo pode definir paradas de tabulação em um controle de edição de várias linhas usando a mensagem em [**\_ SetTabStops**](em-settabstops.md) . (O padrão para uma parada de tabulação é de oito caracteres.) Quando um aplicativo adiciona texto ao controle de edição, os caracteres de tabulação no texto geram automaticamente espaço até a próxima parada de tabulação. A mensagem em **\_ SetTabStops** não faz com que o sistema Redesenhe o texto automaticamente. Para fazer isso, um aplicativo pode chamar a função [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) . A mensagem em **\_ SetTabStops** aplica-se somente a controles de edição de várias linhas.

Um aplicativo pode definir a largura das margens esquerda e direita para um controle de edição usando a mensagem em [**\_ SetMargins**](em-setmargins.md) . Depois de enviar essa mensagem, o sistema redesenha o controle de edição para refletir as novas configurações de margem. Um aplicativo pode recuperar a largura da margem esquerda ou direita enviando a mensagem em [**\_ GetMargins**](em-getmargins.md) . Por padrão, as margens de controle de edição são definidas de forma muito grande para acomodar o maior número de caracteres horizontais (larguras negativas negativos) para a fonte atual que está sendo usada no controle de edição.

## <a name="concealing-user-input"></a>Ocultando a entrada do usuário

Um aplicativo pode usar um caractere de senha em um controle de edição para ocultar a entrada do usuário. Quando um caractere de senha é definido, ele é exibido no lugar de cada caractere que o usuário digita. Quando um caractere de senha é removido, o controle exibe os caracteres que o usuário digita. Se o aplicativo criar um controle de edição de linha única usando a [**\_ senha**](edit-control-styles.md)do estilo es, o caractere de senha padrão será um asterisco ( \* ). Um aplicativo pode usar a mensagem em [**\_ SetPasswordChar**](em-setpasswordchar.md) para remover ou definir um caractere de senha diferente e a mensagem em [**\_ getpasswordchar**](em-getpasswordchar.md) para recuperar o caractere de senha atual. Essas mensagens se aplicam somente a controles de edição de linha única.

## <a name="using-integers"></a>Usando números inteiros

Há duas funções de conversão de inteiros para controles de edição projetados para conter somente números. A função [**SetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-setdlgitemint) cria a representação de cadeia de caracteres de um inteiro especificado (assinado ou não assinado) e envia a cadeia de caracteres para um controle de edição. **SetDlgItemInt** não retorna nenhum valor. A função [**GetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-getdlgitemint) cria um inteiro (assinado ou não assinado) de sua representação de cadeia de caracteres em um controle de edição. **GetDlgItemInt** retorna o número inteiro (ou um valor de erro).

## <a name="undoing-text-operations"></a>Desfazendo operações de texto

Cada controle de edição mantém um sinalizador de desfazer que indica se um aplicativo pode reverter ou desfazer a operação mais recente no controle de edição (desfazendo uma exclusão de texto, por exemplo). O controle de edição define o sinalizador de desfazer para indicar que a operação pode ser desfeita e a redefine para indicar que a operação não pode ser desfeita. Um aplicativo pode determinar a configuração do sinalizador de desfazer enviando o controle uma mensagem [**em \_ CanUndo**](em-canundo.md) .

Um aplicativo pode desfazer a operação mais recente enviando o controle uma mensagem [**em \_ desfazer**](em-undo.md) . Uma operação pode ser desfeita fornecida. nenhuma outra operação de controle de edição ocorre primeiro. Por exemplo, o usuário pode excluir texto, substituir o texto (desfazer a exclusão) e, em seguida, excluir o texto novamente (desfazer a substituição). A mensagem em **\_ desfazer** aplica-se a controles de linha única e de edição de várias linhas e sempre funciona para controles de edição de linha única.

Um aplicativo pode redefinir um sinalizador de desfazer do controle de edição enviando o controle uma mensagem em [**\_ EMPTYUNDOBUFFER**](em-emptyundobuffer.md) . O sistema redefine automaticamente o sinalizador de desfazer sempre que um controle de edição recebe uma mensagem em [**\_ SetHandle**](em-sethandle.md) ou [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) . A função [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) envia uma mensagem de **\_ SetText do WM** .

## <a name="handling-wordwrap-and-line-breaks"></a>Manipulação de linhas e quebras de linha

Um aplicativo pode usar funções de WordWrap com controles de edição de várias linhas para localizar a palavra ou o fragmento de palavra que deve ser encapsulado na próxima linha. Usando a função WordWrap padrão fornecida pelo sistema, as linhas sempre terminam nos espaços entre as palavras. Um aplicativo pode especificar sua própria função WordWrap fornecendo uma função [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) WordWrap e enviando o controle de edição uma mensagem [**em \_ SETWORDBREAKPROC**](em-setwordbreakproc.md) . Um aplicativo pode recuperar o endereço da função WordWrap atual enviando o controle uma mensagem em [**\_ GETWORDBREAKPROC**](em-getwordbreakproc.md) .

Um aplicativo pode direcionar um controle de edição de várias linhas para adicionar ou remover um caractere de quebra de linha flexível (dois retornos de carro e um feed de linha) automaticamente no final das linhas de texto encapsulado. Um aplicativo pode ativar ou desativar esse recurso enviando o controle de edição uma mensagem [**em \_ FMTLINES**](em-fmtlines.md) . Essa mensagem se aplica somente a controles de edição de várias linhas e não afeta uma linha que termina com uma quebra de linha rígida (um retorno de carro e um feed de linha inserido pelo usuário). Também em controles de edição de várias linhas, um aplicativo pode especificar o estilo [**es \_ WANTRETURN**](edit-control-styles.md) para solicitar que o sistema Insira um retorno de carro quando o usuário pressiona a tecla Enter no controle de edição.

## <a name="retrieving-points-and-characters"></a>Recuperando pontos e caracteres

Para determinar o caractere mais próximo de um ponto especificado na área do cliente de um controle de edição, envie a mensagem em [**\_ CHARFROMPOS**](em-charfrompos.md) para o controle. A mensagem retorna o índice de caracteres e o índice de linha do caractere mais próximo ao ponto. Da mesma forma, você pode recuperar as coordenadas da área do cliente de um caractere especificado enviando a mensagem em [**\_ POSFROMCHAR**](em-posfromchar.md) . A mensagem retorna as coordenadas x e y do canto superior esquerdo do caractere especificado.

## <a name="autocompletion-of-strings"></a>Preenchimento automático de cadeias de caracteres

O preenchimento automático expande as cadeias de caracteres que foram inseridas parcialmente em um controle de edição em cadeias de caracteres completas. Por exemplo, quando um usuário começa a inserir uma URL no controle de edição de endereço inserido na barra de ferramentas do Windows Internet Explorer, o preenchimento automático expande a cadeia de caracteres em uma ou mais URLs completas que são consistentes com a cadeia de caracteres parcial existente. Uma cadeia de caracteres de URL parcial, como "MIC", pode ser expandida para " https://www.microsoft.com " ou " https://www.microsoft.com/windows ". O preenchimento automático normalmente é usado com controles de edição ou com controles que têm um controle de edição inserido.

Para obter mais informações, consulte a documentação da interface [**IAutoComplete**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete) e [**IAutoComplete2**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2) .

## <a name="complex-script-in-edit-controls"></a>Script complexo em controles de edição

Um *script complexo* é um idioma cuja forma impressa não é disposta de forma simples. Por exemplo, um script complexo pode permitir renderização bidirecional, formatação contextual de glifos ou caracteres de combinação. Os controles de edição padrão foram estendidos para dar suporte a texto multilíngüe e scripts complexos. Isso inclui não apenas a entrada e a exibição, mas também o movimento correto do cursor sobre clusters de caracteres (em tailandês e o script devanágari, por exemplo).

Um aplicativo bem escrito recebe esse suporte automaticamente, sem modificação. Novamente, você deve considerar a adição de suporte à ordem de leitura da direita para a esquerda e ao alinhamento à direita. Nesse caso, alterne os sinalizadores de estilo estendido da janela de controle de edição para controlar esses atributos, conforme mostrado no exemplo a seguir.


```
// ID_EDITCONTROL is the control ID in the resource file.
HANDLE hWndEdit = GetDlgItem(hDlg, ID_EDITCONTROL);
LONG lAlign = GetWindowLong(hWndEdit, GWL_EXSTYLE) ;

// To toggle alignment
lAlign ^= WS_EX_RIGHT ;

// To toggle reading order
lAlign ^= WS_EX_RTLREADING ;
```



Depois de definir o valor de **LALIGN** , habilite a nova exibição definindo o estilo estendido da janela de controle de edição da seguinte maneira.


```
// This assumes your edit control is in a dialog box. If not, 
// get the edit control handle from another source.

SetWindowLong(hWndEdit, GWL_EXSTYLE, lAlign);
InvalidateRect(hWndEdit, NULL, FALSE);
```



O Uniscribe é outro conjunto de funções que fornecem um controle fino para o processamento de scripts complexos. Para obter mais informações, consulte [Uniscribe](/windows/desktop/Intl/uniscribe).

 

 