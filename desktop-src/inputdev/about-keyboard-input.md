---
title: Sobre a entrada do teclado
description: Este tópico discute a entrada do teclado.
ms.assetid: de34727e-e8c7-481d-982d-0e42a02704db
keywords:
- entrada do usuário, entrada de teclado
- capturando entrada do usuário, entrada de teclado
- entrada do teclado
- foco do teclado
- mensagens de pressionamento de tecla
- mensagens de caracteres
- pressionamentos de tecla do sistema
- pressionamentos de tecla não do sistema
- mensagens de caracteres não do sistema
- chaves inativas
- mensagens de caracteres inativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de85794901be3fef37156bde29520039f85702b
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373199"
---
# <a name="about-keyboard-input"></a>Sobre a entrada do teclado

Os aplicativos devem aceitar a entrada do usuário do teclado, bem como do mouse. Um aplicativo recebe entrada de teclado na forma de mensagens postadas em suas janelas.

Esta seção contém os seguintes tópicos:

-   [Modelo de entrada do teclado](#keyboard-input-model)
-   [Foco e ativação do teclado](#keyboard-focus-and-activation)
-   [Mensagens de pressionamento de tecla](#keystroke-messages)
    -   [Pressionamentos de tecla do sistema e não do sistema](#system-and-nonsystem-keystrokes)
    -   [Códigos de chave virtual descritos](#virtual-key-codes-described)
    -   [Sinalizadores de mensagem de pressionamento de tecla](#keystroke-message-flags)
-   [Mensagens de caracteres](#character-messages)
    -   [Mensagens de caracteres não do sistema](#nonsystem-character-messages)
    -   [Mensagens de caracteres inativos](#dead-character-messages)
-   [Status da chave](#key-status)
-   [Conversões de teclas e de caracteres](#keystroke-and-character-translations)
-   [Suporte a teclas de atalho](#hot-key-support)
-   [Teclas de teclado para navegação e outras funções](#keyboard-keys-for-browsing-and-other-functions)
-   [Simulando entrada](#simulating-input)
-   [Idiomas, localidades e layouts de teclado](#languages-locales-and-keyboard-layouts)

## <a name="keyboard-input-model"></a>Modelo de entrada do teclado

O sistema fornece suporte de teclado independente de dispositivo para aplicativos instalando um driver de dispositivo de teclado apropriado para o teclado atual. O sistema fornece suporte de teclado independente de idioma usando o layout de teclado específico do idioma selecionado no momento pelo usuário ou pelo aplicativo. O driver de dispositivo de teclado recebe códigos de verificação do teclado, que são enviados para o layout de teclado onde eles são convertidos em mensagens e postados para as janelas apropriadas em seu aplicativo.

Atribuído a cada chave em um teclado é um valor exclusivo chamado de *código de verificação*, um identificador dependente de dispositivo para a chave no teclado. Um teclado gera dois códigos de verificação quando o usuário digita uma chave — uma quando o usuário pressiona a tecla e outra quando o usuário libera a chave.

O driver de dispositivo de teclado interpreta um código de verificação e traduz (mapeia)-o para um *código de chave virtual*, um valor independente de dispositivo definido pelo sistema que identifica a finalidade de uma chave. Depois de converter um código de verificação, o layout do teclado cria uma mensagem que inclui o código de verificação, o código de chave virtual e outras informações sobre a tecla e, em seguida, coloca a mensagem na fila de mensagens do sistema. O sistema remove a mensagem da fila de mensagens do sistema e a posta na fila de mensagens do thread apropriado. Eventualmente, o loop de mensagem do thread remove a mensagem e a passa para o procedimento de janela apropriado para processamento. A figura a seguir ilustra o modelo de entrada do teclado.

![modelo de processamento de entrada de teclado](images/csinp-01.png)

## <a name="keyboard-focus-and-activation"></a>Foco e ativação do teclado

O sistema posta mensagens de teclado na fila de mensagens do thread em primeiro plano que criou a janela com o foco do teclado. O *foco do teclado* é uma propriedade temporária de uma janela. O sistema compartilha o teclado entre todas as janelas na exibição alternando o foco do teclado, na direção do usuário, de uma janela para outra. A janela que tem o foco do teclado recebe (da fila de mensagens do thread que a criou) todas as mensagens de teclado até que o foco seja alterado para uma janela diferente.

Um thread pode chamar a função [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) para determinar qual das suas janelas (se houver) atualmente tem o foco do teclado. Um thread pode dar o foco do teclado a uma de suas janelas chamando a função [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) . Quando o foco do teclado muda de uma janela para outra, o sistema envia uma mensagem do [**WM \_ KILLFOCUS**](wm-killfocus.md) para a janela que perdeu o foco e, em seguida, envia uma mensagem do [**WM \_ SETFOCUS**](wm-setfocus.md) para a janela que ganhou o foco.

O conceito de foco do teclado está relacionado ao da janela ativa. A *janela ativa* é a janela de nível superior com a qual o usuário está trabalhando no momento. A janela com o foco do teclado é a janela ativa ou uma janela filho da janela ativa. Para ajudar o usuário a identificar a janela ativa, o sistema a coloca na parte superior da ordem Z e realça sua barra de título (se tiver uma) e uma borda.

O usuário pode ativar uma janela de nível superior clicando nela, selecionando-a usando a combinação de teclas ALT + TAB ou ALT + ESC ou selecionando-a na Lista de Tarefas. Um thread pode ativar uma janela de nível superior usando a função [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) . Ele pode determinar se uma janela de nível superior criada por ele está ativa usando a função [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) .

Quando uma janela é desativada e outra ativada, o sistema envia a mensagem de [**\_ ativação do WM**](wm-activate.md) . A palavra de ordem inferior do parâmetro *wParam* será zero se a janela estiver sendo desativada e diferente de zero se estiver sendo ativada. Quando o procedimento de janela padrão recebe a mensagem de **\_ ativação do WM** , ele define o foco do teclado para a janela ativa.

Para bloquear a entrada de eventos de teclado e de mouse para aplicativos, use [**BlockInput**](/windows/win32/api/winuser/nf-winuser-blockinput). Observe que a função **BlockInput** não interferirá na tabela de estado de entrada do teclado assíncrono. Isso significa que chamar a função [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) enquanto a entrada está bloqueada alterará a tabela de estado de entrada do teclado assíncrono.

## <a name="keystroke-messages"></a>Mensagens de pressionamento de tecla

Pressionar uma chave faz com que uma mensagem do [**WM \_ KEYDOWN**](wm-keydown.md) ou [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) seja colocada na fila de mensagens do thread anexada à janela que tem o foco do teclado. A liberação de uma chave faz com que uma mensagem do [**WM \_ KEYUP**](wm-keyup.md) ou do [**WM \_ SYSKEYUP**](wm-syskeyup.md) seja colocada na fila.

As mensagens de chave e de baixo normalmente ocorrem em pares, mas se o usuário mantiver uma chave longa o suficiente para iniciar o recurso de repetição automático do teclado, o sistema gerará várias mensagens do [**WM \_ KEYDOWN**](wm-keydown.md) ou do [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) em uma linha. Em seguida, ele gera uma única mensagem do [**WM \_ KEYUP**](wm-keyup.md) ou do [**WM \_ SYSKEYUP**](wm-syskeyup.md) quando o usuário libera a chave.

Esta seção contém os seguintes tópicos:

-   [Pressionamentos de tecla do sistema e não do sistema](#system-and-nonsystem-keystrokes)
-   [Códigos de chave virtual descritos](#virtual-key-codes-described)
-   [Sinalizadores de mensagem de pressionamento de tecla](#keystroke-message-flags)

### <a name="system-and-nonsystem-keystrokes"></a>Pressionamentos de tecla do sistema e não do sistema

O sistema faz uma distinção entre pressionamentos de tecla do sistema e pressionamentos de tecla não do sistema. As teclas do sistema produzem mensagens de pressionamento de tecla do sistema, o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) e o [**WM \_ SYSKEYUP**](wm-syskeyup.md). As teclas não do sistema produzem mensagens de pressionamento de tecla que não são do sistema, o [**WM \_ KEYDOWN**](wm-keydown.md) e o [**WM \_ KEYUP**](wm-keyup.md).

Se o procedimento de janela precisar processar uma mensagem de pressionamento de tecla do sistema, verifique se depois de processar a mensagem o procedimento a transmite para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Caso contrário, todas as operações do sistema que envolvem a tecla ALT serão desabilitadas sempre que a janela tiver o foco do teclado. Ou seja, o usuário não poderá acessar os menus ou o menu do sistema da janela ou usar a combinação de teclas ALT + ESC ou ALT + TAB para ativar uma janela diferente.

As mensagens de pressionamento de tecla do sistema são usadas principalmente pelo sistema em vez de por um aplicativo. O sistema as usa para fornecer sua interface de teclado interna para menus e permitir que o usuário controle qual janela está ativa. As mensagens de pressionamento de tecla do sistema são geradas quando o usuário digita uma chave em combinação com a tecla ALT, ou quando o usuário digita e nenhuma janela tem o foco do teclado (por exemplo, quando o aplicativo ativo é minimizado). Nesse caso, as mensagens são postadas na fila de mensagens anexada à janela ativa.

As mensagens de pressionamento de tecla não do sistema são para uso pelas janelas do aplicativo; a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) não faz nada com eles. Um procedimento de janela pode descartar qualquer mensagem de pressionamento de tecla não do sistema que não seja necessária.

### <a name="virtual-key-codes-described"></a>Códigos de Virtual-Key descritos

O parâmetro **wParam** de uma mensagem de pressionamento de tecla contém o código de chave virtual da chave que foi pressionada ou liberada. Um procedimento de janela processa ou ignora uma mensagem de pressionamento de tecla, dependendo do valor do código de chave virtual.

Um procedimento de janela típico processa apenas um pequeno subconjunto das mensagens de pressionamento de tecla que recebe e ignora o restante. Por exemplo, um procedimento de janela pode processar apenas mensagens de pressionamentos de tecla [**\_ KEYDOWN do WM**](wm-keydown.md) e apenas aquelas que contêm códigos de chave virtual para as chaves de movimento do cursor, teclas Shift (também chamadas de chaves de controle) e teclas de função. Um procedimento de janela típico não processa mensagens de pressionamento de teclas de chaves de caractere. Em vez disso, ele usa a função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) para converter a mensagem em mensagens de caracteres. Para obter mais informações sobre **TranslateMessage** e mensagens de caracteres, consulte [mensagens de caracteres](#character-messages).

### <a name="keystroke-message-flags"></a>Sinalizadores de mensagem de pressionamento de tecla

O parâmetro **lParam** de uma mensagem de pressionamento de tecla contém informações adicionais sobre a tecla que gerou a mensagem. Essas informações incluem a contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição. A ilustração a seguir mostra os locais desses sinalizadores e valores no parâmetro **lParam** .

![os locais dos sinalizadores e valores no parâmetro lParam de uma mensagem de pressionamento de tecla](images/csinp-02.png)

Um aplicativo pode usar os valores a seguir para manipular os sinalizadores de teclas.



| Valor            | Descrição                                                                       |
|------------------|-----------------------------------------------------------------------------------|
| **ALTDOWN de KF \_**  | Manipula o sinalizador de tecla ALT, que indica se a tecla ALT é pressionada.     |
| **KF \_ DLGMODE**  | Manipula o sinalizador de modo de diálogo, que indica se uma caixa de diálogo está ativa. |
| **KF \_ ESTENDIDO** | Manipula o sinalizador de chave estendida.                                                |
| **KF \_ MENUMODE** | Manipula o sinalizador de modo de menu, que indica se um menu está ativo.         |
| **KF \_ REPEAT**   | Manipula o sinalizador de estado de chave anterior.                                          |
| **KF \_ UP**       | Manipula o sinalizador de estado de transição.                                            |

Código de exemplo:

```cpp
case WM_KEYDOWN:
case WM_KEYUP:
case WM_SYSKEYDOWN:
case WM_SYSKEYUP:
{
    WORD vkCode = LOWORD(wParam);                                       // virtual-key code

    BYTE scanCode = LOBYTE(HIWORD(lParam));                             // scan code
    BOOL scanCodeE0 = (HIWORD(lParam) & KF_EXTENDED) == KF_EXTENDED;    // extended-key flag, 1 if scancode has 0xE0 prefix

    BOOL upFlag = (HIWORD(lParam) & KF_UP) == KF_UP;                    // transition-state flag, 1 on keyup
    BOOL repeatFlag = (HIWORD(lParam) & KF_REPEAT) == KF_REPEAT;        // previous key-state flag, 1 on autorepeat
    WORD repeatCount = LOWORD(lParam);                                  // repeat count, > 0 if several keydown messages was combined into one message

    BOOL altDownFlag = (HIWORD(lParam) & KF_ALTDOWN) == KF_ALTDOWN;     // ALT key was pressed

    BOOL dlgModeFlag = (HIWORD(lParam) & KF_DLGMODE) == KF_DLGMODE;     // dialog box is active
    BOOL menuModeFlag = (HIWORD(lParam) & KF_MENUMODE) == KF_MENUMODE;  // menu is active
    
    // ...
}
break;
```

### <a name="repeat-count"></a>Contagem repetida

Você pode verificar a contagem de repetição para determinar se uma mensagem de tecla representa mais de um teclas. O sistema incrementa a contagem quando o teclado gera [**mensagens WM \_ KEYDOWN**](wm-keydown.md) ou [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) mais rapidamente do que um aplicativo pode processá-las. Isso geralmente ocorre quando o usuário mantém uma tecla para baixo o suficiente para iniciar o recurso de repetição automática do teclado. Em vez de preencher a fila de mensagens do sistema com as mensagens de chave para baixo resultantes, o sistema combina as mensagens em uma única mensagem de tecla para baixo e incrementa a contagem de repetição. A liberação de uma chave não pode iniciar o recurso de repetição automática, portanto, a contagem de repetição para mensagens [**WM \_ KEYUP**](wm-keyup.md) e [**WM \_ SYSKEYUP**](wm-syskeyup.md) é sempre definida como 1.

### <a name="scan-code"></a>Digitalizar código

O código de verificação é o valor gerado pelo hardware do teclado quando o usuário pressiona uma tecla. É um valor dependente do dispositivo que identifica a chave pressionada, em vez do caractere representado pela chave. Um aplicativo normalmente ignora códigos de verificação. Em vez disso, ele usa os códigos de chave virtual independentes de dispositivo para interpretar mensagens de teclas.

### <a name="extended-key-flag"></a>sinalizador Extended-Key de Extended-Key

O sinalizador de chave estendida indica se a mensagem de teclas foi originada de uma das chaves adicionais no teclado aprimorado. As teclas estendidas consistem nas teclas ALT e CTRL no lado direito do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e seta nos clusters à esquerda do teclado numérico; a tecla NUM LOCK; a tecla BREAK (CTRL+PAUSE); a tecla PRINT SCRN; e as chaves de divisão (/) e ENTER no teclado numérico. O sinalizador de chave estendida será definido se a chave for uma chave estendida.

Se especificado, o código de verificação foi precedido por um byte de prefixo com o valor 0xE0 (224).

### <a name="context-code"></a>Código de contexto

O código de contexto indica se a tecla ALT estava inoca quando a mensagem de teclas foi gerada. O código será 1 se a tecla ALT estiver inobada e 0 se ela estiver para cima.

### <a name="previous-key-state-flag"></a>Sinalizador Key-State anterior

O sinalizador de estado de chave anterior indica se a chave que gerou a mensagem de teclas estava anteriormente para cima ou para baixo. Será 1 se a chave estava anteriormente inobada e 0 se a chave estava acima anteriormente. Você pode usar esse sinalizador para identificar mensagens de teclas geradas pelo recurso de repetição automática do teclado. Esse sinalizador é definido como 1 para mensagens de tecla [**WM \_ KEYDOWN**](wm-keydown.md) e [**WM \_ SYSKEYDOWN geradas**](wm-syskeydown.md) pelo recurso de repetição automática. Ele sempre é definido como 1 para [**mensagens WM \_ KEYUP**](wm-keyup.md) e [**WM \_ SYSKEYUP.**](wm-syskeyup.md)

### <a name="transition-state-flag"></a>sinalizador Transition-State de Transition-State

O sinalizador de estado de transição indica se pressionar uma tecla ou liberar uma chave gerou a mensagem de pressionamento de tecla. Esse sinalizador sempre é definido como 0 para mensagens [**WM \_ KEYDOWN**](wm-keydown.md) e [**WM \_ SYSKEYDOWN;**](wm-syskeydown.md) ele sempre é definido como 1 para mensagens [**WM \_ KEYUP**](wm-keyup.md) e [**WM \_ SYSKEYUP.**](wm-syskeyup.md)

## <a name="character-messages"></a>Mensagens de caractere

As mensagens de teclas fornecem muitas informações sobre teclas, mas não fornecem códigos de caractere para teclas de caractere. Para recuperar códigos de caractere, um aplicativo deve incluir a [**função TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) em seu loop de mensagem de thread. **TranslateMessage** passa uma [**mensagem WM \_ KEYDOWN**](wm-keydown.md) [**ou WM \_ SYSKEYDOWN**](wm-syskeydown.md) para o layout do teclado. O layout examina o código de chave virtual da mensagem e, se ele corresponde a uma chave de caractere, fornece o código de caractere equivalente (levando em conta o estado das teclas SHIFT e CAPS LOCK). Em seguida, ele gera uma mensagem de caractere que inclui o código de caractere e coloca a mensagem na parte superior da fila de mensagens. A próxima iteração do loop de mensagem remove a mensagem de caractere da fila e envia a mensagem para o procedimento de janela apropriado.

Esta seção contém os seguintes tópicos:

-   [Mensagens de caractere não sistema](#nonsystem-character-messages)
-   [Mensagens de caractere morta](#dead-character-messages)

### <a name="nonsystem-character-messages"></a>Mensagens de caractere não sistema

Um procedimento de janela pode receber as seguintes mensagens de caractere: [**WM \_ CHAR,**](wm-char.md) [**WM \_ DEADCHAR,**](wm-deadchar.md) [**WM \_ SYSCHAR,**](/windows/desktop/menurc/wm-syschar) [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)e [**WM \_ UNICHAR.**](wm-unichar.md) A [**função TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) gera uma mensagem **WM \_ CHAR** ou **WM \_ DEADCHAR** quando processa uma mensagem [**WM \_ KEYDOWN.**](wm-keydown.md) Da mesma forma, ele gera uma **mensagem WM \_ SYSCHAR** ou **WM \_ SYSDEADCHAR** quando processa uma mensagem [**WM \_ SYSKEYDOWN.**](wm-syskeydown.md)

Um aplicativo que processa a entrada do teclado normalmente ignora todas as mensagens [**WM \_ CHAR**](wm-char.md) e [**WM \_ UNICHAR,**](wm-unichar.md) passando outras mensagens para a [**função DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Observe que **o WM \_ CHAR** usa o UTF (Formato de Transformação Unicode) de 16 bits, enquanto **o WM \_ UNICHAR** usa UTF-32. O sistema usa as [**mensagens WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) e [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md) para implementar mnemônicos de menu.

O **parâmetro wParam** de todas as mensagens de caractere contém o código de caractere da chave de caractere que foi pressionada. O valor do código de caractere depende da classe de janela da janela que recebe a mensagem. Se a versão Unicode da [**função RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) tiver sido usada para registrar a classe de janela, o sistema fornece caracteres Unicode para todas as janelas dessa classe. Caso contrário, o sistema fornece códigos de caractere ASCII. Para obter mais informações, consulte [Unicode e Conjuntos de caracteres](/windows/desktop/Intl/unicode-and-character-sets).

O conteúdo do parâmetro **lParam** de uma mensagem de caractere é idêntico ao conteúdo do parâmetro **lParam** da mensagem de chave para baixo que foi convertida para produzir a mensagem de caractere. Para obter informações, consulte [Sinalizadores de mensagem de teclas](#keystroke-message-flags).

### <a name="dead-character-messages"></a>Dead-Character mensagens

Alguns teclados que não são do inglês contêm chaves de caractere que não devem produzir caracteres por conta própria. Em vez disso, eles são usados para adicionar um diacrético ao caractere produzido pelo teclatro subsequente. Essas chaves são chamadas *de chaves mortas.* A tecla circunflexa em um teclado alemão é um exemplo de uma tecla morta. Para inserir o caractere que consiste em um "o" com um circunflexo, um usuário alemão digitaria a chave circunflexa seguida pela tecla "o". A janela com o foco do teclado receberia a seguinte sequência de mensagens:

1.  [**WM \_ KEYDOWN**](wm-keydown.md)
2.  [**WM \_ DEADCHAR**](wm-deadchar.md)
3.  [**WM \_ KEYUP**](wm-keyup.md)
4.  [**WM \_ KEYDOWN**](wm-keydown.md)
5.  [**WM \_ CHAR**](wm-char.md)
6.  [**WM \_ KEYUP**](wm-keyup.md)

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) gera a mensagem [**WM \_ DEADCHAR**](wm-deadchar.md) quando processa a mensagem [**WM \_ KEYDOWN**](wm-keydown.md) de uma chave morta. Embora o *parâmetro wParam* da mensagem **WM \_ DEADCHAR** contenha o código de caractere do diacrático para a chave morta, um aplicativo normalmente ignora a mensagem. Em vez disso, ele [**processa a mensagem WM \_ CHAR**](wm-char.md) gerada pelo teclatro subsequente. O *parâmetro wParam* da **mensagem WM \_ CHAR** contém o código de caractere da letra com o diacrático. Se o conjunto de teclas subsequente gerar um caractere que não pode ser combinado com um diacrático, o sistema gerará duas **mensagens WM \_ CHAR.** O *parâmetro wParam* do primeiro contém o código de caractere do diacrático; O *parâmetro wParam* do segundo contém o código de caractere da chave de caractere subsequente.

A [**função TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) gera a mensagem [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md) quando processa a mensagem [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) de uma chave morta do sistema (uma tecla morta pressionada em combinação com a tecla ALT). Um aplicativo normalmente ignora a **mensagem WM \_ SYSDEADCHAR.**

## <a name="key-status"></a>Status da chave

Durante o processamento de uma mensagem de teclado, um aplicativo pode precisar determinar o status de outra chave além da que gerou a mensagem atual. Por exemplo, um aplicativo de processamento de palavras que permite que o usuário pressione SHIFT+END para selecionar um bloco de texto deve verificar o status da tecla SHIFT sempre que receber uma mensagem de pressionamento de tecla da tecla END. O aplicativo pode usar a [**função GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) para determinar o status de uma chave virtual no momento em que a mensagem atual foi gerada; ele pode usar a [**função GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) para recuperar o status atual de uma chave virtual.

O layout do teclado mantém uma lista de nomes. O nome de uma chave que produz um único caractere é o mesmo que o caractere produzido pela chave. O nome de uma chave não caractere, como TAB e ENTER, é armazenado como uma cadeia de caracteres. Um aplicativo pode recuperar o nome de qualquer chave do driver de dispositivo chamando a [**função GetKeyNameText.**](/windows/win32/api/winuser/nf-winuser-getkeynametexta)

## <a name="keystroke-and-character-translations"></a>Conversões de teclas e de caracteres

O sistema inclui várias funções de finalidade especial que convertem códigos de verificação, códigos de caractere e códigos de chave virtual fornecidos por várias mensagens de teclas. Essas funções incluem [**MapVirtualKey,**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya) [**ToAscii,**](/windows/win32/api/winuser/nf-winuser-toascii) [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)e [**VkKeyScan.**](/windows/win32/api/winuser/nf-winuser-vkkeyscana)

Além disso, o Microsoft Rich Edit 3,0 dá suporte ao [IME HexToUnicode](/windows/desktop/Intl/hextounicode-ime), que permite que um usuário converta entre caracteres hexadecimais e Unicode usando teclas de acesso. Isso significa que, quando o Microsoft Rich Edit 3,0 é incorporado a um aplicativo, o aplicativo herdará os recursos do IME HexToUnicode.

## <a name="hot-key-support"></a>Suporte a Hot-Key

Uma *tecla de atalho* é uma combinação de teclas que gera uma mensagem de [**\_ tecla**](wm-hotkey.md) de acesso do WM, uma mensagem que o sistema coloca na parte superior da fila de mensagens de um thread, ignorando todas as mensagens existentes na fila. Os aplicativos usam teclas de acesso para obter a entrada de teclado de alta prioridade do usuário. Por exemplo, ao definir uma tecla de atalho que consiste na combinação de teclas CTRL + C, um aplicativo pode permitir que o usuário cancele uma operação demorada.

Para definir uma tecla de acesso, um aplicativo chama a função [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) , especificando a combinação de chaves que gera a mensagem de [**tecla de \_ atalho do WM**](wm-hotkey.md) , o identificador para a janela a fim de receber a mensagem e o identificador da tecla de acesso. Quando o usuário pressiona a tecla de atalho, uma mensagem de **\_ tecla** de acesso do WM é colocada na fila de mensagens do thread que criou a janela. O parâmetro *wParam* da mensagem contém o identificador da tecla de acesso. O aplicativo pode definir várias teclas de acesso para um thread, mas cada tecla de acesso no thread deve ter um identificador exclusivo. Antes de o aplicativo ser encerrado, ele deve usar a função [**UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) para destruir a tecla de acesso.

Os aplicativos podem usar um controle de tecla de atalho para facilitar o usuário a escolher uma tecla de atalho. Os controles de teclas de acesso normalmente são usados para definir uma tecla de atalho que ativa uma janela; Eles não usam as funções [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) e [**UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) . Em vez disso, um aplicativo que usa um controle de tecla de atalho normalmente envia a mensagem de [**\_ settecla do WM**](wm-sethotkey.md) para definir a tecla de atalho. Sempre que o usuário pressionar a tecla de atalho, o sistema enviará uma mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) especificando a tecla de acesso SC \_ . Para obter mais informações sobre os controles de tecla de atalho, consulte "usando controles de tecla quente" em [controles de tecla de atalho](../controls/hot-key-controls.md).

## <a name="keyboard-keys-for-browsing-and-other-functions"></a>Teclas de teclado para navegação e outras funções

o Windows fornece suporte para teclados com chaves especiais para funções de navegador, funções de mídia, inicialização de aplicativos e gerenciamento de energia. O [**\_ APPCOMMAND do WM**](wm-appcommand.md) dá suporte às teclas de teclado adicionais. Além disso, a função [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) é modificada para dar suporte às teclas de teclado adicionais.

É improvável que uma janela filho em um aplicativo de componente seja capaz de implementar diretamente os comandos para essas teclas de teclado adicionais. Assim, quando uma dessas chaves for pressionada, o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) enviará uma mensagem do [**WM \_ APPCOMMAND**](wm-appcommand.md) para uma janela. **DefWindowProc** também produzirá a mensagem do **WM \_ APPCOMMAND** em sua janela pai. Isso é semelhante à maneira como os menus de contexto são invocados com o botão direito do mouse, que é o **DefWindowProc** envia uma mensagem de [**\_ CONTEXTMENU do WM**](/windows/desktop/menurc/wm-contextmenu) em um clique com o botão direito e o Bubble para seu pai. Além disso, se o **DefWindowProc** receber uma mensagem do **WM \_ APPCOMMAND** para uma janela de nível superior, ele chamará um gancho de shell com o código **HSHELL \_ APPCOMMAND**.

o Windows também dá suporte ao Microsoft IntelliMouse Explorer, que é um mouse com cinco botões. Os dois botões extras dão suporte à navegação do navegador para frente e para trás. Para obter mais informações, consulte [XBUTTONs](about-mouse-input.md).

## <a name="simulating-input"></a>Simulando entrada

Para simular uma série ininterrupta de eventos de entrada do usuário, use a função [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) . A função aceita três parâmetros. O primeiro parâmetro, *cInputs*, indica o número de eventos de entrada que serão simulados. O segundo parâmetro, *rgInputs*, é uma matriz de estruturas de [**entrada**](/windows/win32/api/winuser/ns-winuser-input) , cada uma descrevendo um tipo de evento de entrada e informações adicionais sobre esse evento. O último parâmetro, *cbSize*, aceita o tamanho da estrutura de **entrada** , em bytes.

A função [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) funciona injetando uma série de eventos de entrada simulados no fluxo de entrada de um dispositivo. O efeito é semelhante a chamar o [**\_ evento KEYBD**](/windows/win32/api/winuser/nf-winuser-keybd_event) ou a função de [**\_ evento mouse**](/windows/win32/api/winuser/nf-winuser-mouse_event) repetidamente, exceto que o sistema garante que nenhum outro evento de entrada seja intermisturado com os eventos simulados. Quando a chamada é concluída, o valor de retorno indica o número de eventos de entrada que foram reproduzidos com êxito. Se esse valor for zero, a entrada foi bloqueada.

A função [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) não redefine o estado atual do teclado. Portanto, se o usuário tiver alguma tecla pressionada quando você chamar essa função, poderá interferir nos eventos que essa função gera. Se você estiver preocupado com a possibilidade de interferência, verifique o estado do teclado com a função [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) e corrija conforme necessário.

## <a name="languages-locales-and-keyboard-layouts"></a>Idiomas, localidades e layouts de teclado

Uma *linguagem* é uma linguagem natural, como Inglês, francês e japonês. Um *subidioma* é uma variante de um idioma natural que é falado em uma região geográfica específica, como os subidiomas em inglês falados no Reino Unido e o Estados Unidos. Os aplicativos usam valores, chamados de [identificadores de idioma](/windows/desktop/Intl/language-identifiers), para identificar exclusivamente idiomas e subidiomas.

Normalmente, os aplicativos usam *localidades* para definir o idioma no qual a entrada e a saída são processadas. Definir a localidade para o teclado, por exemplo, afeta os valores de caracteres gerados pelo teclado. Definir a localidade para a exibição ou impressora afeta os glifos exibidos ou impressos. Os aplicativos definem a localidade de um teclado carregando e usando layouts de teclado. Eles definem a localidade para uma exibição ou impressora selecionando uma fonte que ofereça suporte à localidade especificada.

Um layout de teclado não apenas especifica a posição física das chaves no teclado, mas também determina os valores de caracteres gerados pressionando essas chaves. Cada layout identifica a linguagem de entrada atual e determina quais valores de caracteres são gerados por quais chaves e combinações de teclas.

Cada layout de teclado tem um identificador correspondente que identifica o layout e o idioma. A palavra inferior do identificador é um identificador de idioma. A palavra alta é um identificador de dispositivo, especificando o layout físico ou é zero, indicando um layout físico padrão. O usuário pode associar qualquer idioma de entrada a um layout físico. Por exemplo, um usuário de fala em inglês que ocasionalmente trabalha em francês pode definir o idioma de entrada do teclado para francês sem alterar o layout físico do teclado. Isso significa que o usuário pode inserir texto em francês usando o layout familiar em inglês.

Os aplicativos geralmente não são esperados para manipular idiomas de entrada diretamente. Em vez disso, o usuário configura combinações de idioma e layout e, em seguida, alterna entre elas. Quando o usuário clica no texto marcado com um idioma diferente, o aplicativo chama a função [**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) para ativar o layout padrão do usuário para esse idioma. Se o usuário editar o texto em um idioma que não está na lista ativa, o aplicativo poderá chamar a função [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) com o idioma para obter um layout baseado nesse idioma.

A função [**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) define o idioma de entrada para a tarefa atual. O parâmetro *HKL* pode ser o identificador para o layout do teclado ou um identificador de idioma com extensão zero. As alças de layout do teclado podem ser obtidas na função [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) ou [**GetKeyboardLayoutList**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist) . Os valores de **HKL \_ Next** e **HKL \_** Previous também podem ser usados para selecionar o teclado seguinte ou anterior.

A função [**GetKeyboardLayoutName**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea) recupera o nome do layout de teclado ativo para o thread de chamada. Se um aplicativo criar o layout ativo usando a função [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) , **GetKeyboardLayoutName** recuperará a mesma cadeia de caracteres usada para criar o layout. Caso contrário, a cadeia de caracteres é o identificador de idioma primário correspondente à localidade do layout ativo. Isso significa que a função pode não necessariamente diferenciar entre layouts diferentes com o mesmo idioma principal, portanto, não é possível retornar informações específicas sobre o idioma de entrada. No entanto, a função [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) pode ser usada para determinar o idioma de entrada.

A função [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) carrega um layout de teclado e torna o layout disponível para o usuário. Os aplicativos podem tornar o layout imediatamente ativo para o thread atual usando o valor de **\_ ativação KLF** . Um aplicativo pode usar o valor de **\_ reordenação KLF** para reordenar os layouts sem especificar também o valor de **\_ ativação KLF** . Os aplicativos sempre devem usar o valor **\_ \_ OK KLF substituto** ao carregar layouts de teclado para garantir que a preferência do usuário, se houver, esteja selecionada.

Para suporte multilíngue, a função [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) fornece os sinalizadores **KLF \_ REPLACELANG** e **KLF \_ NOTELLSHELL** . O sinalizador **KLF \_ REPLACELANG** direciona a função para substituir um layout de teclado existente sem alterar o idioma. A tentativa de substituir um layout existente usando o mesmo identificador de idioma, mas sem especificar **KLF \_ REPLACELANG** , é um erro. O sinalizador **KLF \_ NOTELLSHELL** impede que a função notifique o shell quando um layout de teclado é adicionado ou substituído. Isso é útil para aplicativos que adicionam vários layouts em uma série de chamadas consecutivas. Esse sinalizador deve ser usado em todos, exceto na última chamada.

A função [**UnloadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout) é restrita, pois não pode descarregar o idioma de entrada padrão do sistema. Isso garante que o usuário sempre tenha um layout disponível para inserir texto usando o mesmo conjunto de caracteres usado pelo shell e pelo sistema de arquivos.

 

 
