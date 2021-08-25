---
title: entrada de teclado (Introdução com Win32 e C++)
description: Entrada de teclado
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3ed8ac1e8d7cd8e6ea35c9e9f58c10fd516cca010b5e5dce667817b32028c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822346"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a>entrada de teclado (Introdução com Win32 e C++)

O teclado é usado para vários tipos distintos de entrada, incluindo:

-   Entrada de caracteres. Texto que o usuário digita em um documento ou caixa de edição.
-   Atalhos de teclado. Traços de chave que invocam funções de aplicativo; por exemplo, CTRL + O para abrir um arquivo.
-   Comandos do sistema. Traços de chave que invocam funções do sistema; por exemplo, ALT + TAB para alternar janelas.

Ao pensar sobre a entrada do teclado, é importante lembrar que um traço de chave não é o mesmo que um caractere. Por exemplo, pressionar a tecla a pode resultar em qualquer um dos caracteres a seguir.

-   um
-   Um
-   á (se o teclado der suporte à combinação de diacríticos)

Além disso, se a tecla ALT for mantida pressionada, pressionar a tecla a produz ALT + A, que o sistema não trata como um caractere, mas sim como um comando do sistema.

## <a name="key-codes"></a>Códigos-chave

Quando você pressiona uma tecla, o hardware gera um *código de verificação*. Os códigos de verificação variam de um teclado para o outro e há códigos de verificação separados para eventos de tecla para cima e para baixo. Você quase nunca se preocupa com códigos de verificação. O driver de teclado traduz códigos de verificação em *códigos de chave virtual*. Os códigos de chave virtual são independentes de dispositivo. Pressionar a tecla a em qualquer teclado gera o mesmo código de chave virtual.

Em geral, os códigos de chave virtual não correspondem a códigos ASCII ou a qualquer outro padrão de codificação de caracteres. Isso é óbvio se você pensar nisso, porque a mesma chave pode gerar caracteres diferentes (a, A, á) e algumas chaves, como teclas de função, não correspondem a nenhum caractere.

Dito isso, os seguintes códigos de chave virtual mapeiam para equivalentes ASCII:

-   0 a 9 chaves = ASCII ' 0 ' – ' 9 ' (0x30 – 0x39)
-   A a Z Keys = ASCII ' A ' – ' Z ' (0x41 – 0x5A)

Em alguns aspectos, esse mapeamento é incerto, pois você nunca deve considerar os códigos de chave virtual como caracteres, pelos motivos discutidos.

O arquivo de cabeçalho WinUser. h define constantes para a maioria dos códigos de chave virtual. Por exemplo, o código de chave virtual para a tecla de seta para a esquerda é **VK \_ esquerdo** (0x25). Para obter a lista completa de códigos de chave virtual, consulte [**códigos de chave virtual**](/windows/desktop/inputdev/virtual-key-codes). Nenhuma constante é definida para os códigos de chave virtual que correspondem a valores ASCII. Por exemplo, o código de chave virtual para a chave é 0x41, mas não há nenhuma constante chamada **VK \_ A**. Em vez disso, basta usar o valor numérico.

## <a name="key-down-and-key-up-messages"></a>Mensagens de Key-Down e Key-Up

Quando você pressiona uma tecla, a janela que tem o foco do teclado recebe uma das mensagens a seguir.

-   [**SYSKEYDOWN do WM \_**](/windows/desktop/inputdev/wm-syskeydown)
-   [**o WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)

A mensagem do [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) indica uma *chave do sistema*, que é um traço de chave que invoca um comando do sistema. Há dois tipos de chave do sistema:

-   ALT + qualquer tecla
-   F10

A tecla F10 ativa a barra de menus de uma janela. Várias combinações de teclas ALT invocam comandos do sistema. Por exemplo, ALT + TAB alterna para uma nova janela. Além disso, se uma janela tiver um menu, a tecla ALT poderá ser usada para ativar itens de menu. Algumas combinações de teclas ALT não fazem nada.

Todos os outros traços de chave são considerados chaves não do sistema e produzem a mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) . Isso inclui as teclas de função diferentes de F10.

Quando você libera uma chave, o sistema envia uma mensagem de chave correspondente:

-   [**o WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)
-   [**SYSKEYUP do WM \_**](/windows/desktop/inputdev/wm-syskeyup)

Se você mantiver uma chave longa o suficiente para iniciar o recurso de repetição do teclado, o sistema enviará várias mensagens de chave para baixo, seguidos por uma única mensagem de chave.

Em todas as quatro mensagens de teclado discutidas até agora, o parâmetro *wParam* contém o código de chave virtual da chave. O parâmetro *lParam* contém algumas informações diversas incluídas em 32 bits. Normalmente, você não precisa das informações no *lParam*. Um sinalizador que pode ser útil é o bit 30, o sinalizador "estado de chave anterior", que é definido como 1 para mensagens de chave suspensa repetidas.

Como o nome indica, os traços de chave do sistema são destinados principalmente para uso pelo sistema operacional. Se você interceptar a mensagem do [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) , chame [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) posteriormente. Caso contrário, você impedirá que o sistema operacional trate o comando.

## <a name="character-messages"></a>Mensagens de caracteres

Os traços de chave são convertidos em caracteres pela função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) , que vimos primeiro no [módulo 1](your-first-windows-program.md). Essa função examina as mensagens de chave e as converte em caracteres. Para cada caractere produzido, a função **TranslateMessage** coloca uma mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) ou do [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) na fila de mensagens da janela. O parâmetro *wParam* da mensagem contém o caractere UTF-16.

Como você pode imaginar, as mensagens do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) são geradas de mensagens do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) , enquanto as mensagens do WM [**\_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) são geradas de mensagens do [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) . Por exemplo, suponha que o usuário pressione a tecla SHIFT seguida da tecla a. Supondo um layout de teclado padrão, você obteria a seguinte sequência de mensagens:

**WM \_ KEYDOWN**: Shift  
**WM \_ KEYDOWN**: A  
**WM \_ CHAR**: ' A '  


Por outro lado, a combinação ALT + P geraria:

 **WM \_ SYSKEYDOWN**: \_ menu VK  
**WM \_ SYSKEYDOWN**: 0x50  
**WM \_ SYSCHAR**: ' p '  
**WM \_ SYSKEYUP**: 0x50  
**WM \_ MENU KEYUP**: VK \_  


(O código de chave virtual para a tecla ALT é chamado de VK \_ MENU por motivos históricos.)

A mensagem do [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) indica um caractere do sistema. Assim como com o [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), você geralmente deve passar essa mensagem diretamente para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Caso contrário, você pode interferir com os comandos padrão do sistema. Em particular, não trate o **WM \_ SYSCHAR** como texto digitado pelo usuário.

A mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) é o que você normalmente considera como entrada de caracteres. O tipo de dados do caractere é **WCHAR \_ t**, representando um caractere Unicode UTF-16. A entrada de caracteres pode incluir caracteres fora do intervalo ASCII, especialmente com layouts de teclado que são comumente usados fora do Estados Unidos. Você pode experimentar diferentes layouts de teclado instalando um teclado regional e, em seguida, usando o recurso de teclado na tela.

Os usuários também podem instalar um IME (editor de método de entrada) para inserir scripts complexos, como caracteres japoneses, com um teclado padrão. Por exemplo, usando um IME em Japonês para inserir o caractere katakana カ (ka), você pode receber as seguintes mensagens:

**WM \_ KEYDOWN**: VK \_ PROCESSKEY (a chave de processo do IME)  
**WM \_ KEYUP**: 0x4b  
**WM \_ KEYDOWN**: VK \_ PROCESSKEY  
**WM \_ KEYUP**: 0x41  
**WM \_ KEYDOWN**: VK \_ PROCESSKEY  
**WM \_ CHAR**: カ  
**WM \_ KEYUP**: VK \_ Return  


Algumas combinações de teclas CTRL são convertidas em caracteres de controle ASCII. Por exemplo, CTRL + A é convertido para o caractere ASCII CTRL-A (SOH) (valor ASCII 0x01). Para entrada de texto, você geralmente deve filtrar os caracteres de controle. Além disso, evite usar o [**WM \_ Char**](/windows/desktop/inputdev/wm-char) para implementar atalhos de teclado. Em vez disso, [**use mensagens WM \_ KEYDOWN;**](/windows/desktop/inputdev/wm-keydown) ou ainda melhor, use uma tabela de aceleradores. As tabelas de acelerador são descritas no próximo tópico, [Tabelas de Acelerador.](accelerator-tables.md)

O código a seguir exibe as mensagens de teclado principais no depurador. Tente jogar com combinações de teclas diferentes e ver quais mensagens são geradas.


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a>Mensagens de teclado diversas

Algumas outras mensagens de teclado podem ser ignoradas com segurança pela maioria dos aplicativos.

-   A [**mensagem \_ WM DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) é enviada para uma chave de combinação, como um diacrítico. Por exemplo, em um teclado de idioma espanhol, digitar acento (') seguido por E produz o caractere é. O **WM \_ DEADCHAR é** enviado para o caractere de destaque.
-   A [**mensagem WM \_ UNICHAR**](/windows/desktop/inputdev/wm-unichar) está obsoleta. Ele permite que programas ANSI recebam entrada de caractere Unicode.
-   O [**caractere CHAR do WM \_ IME \_**](/windows/desktop/Intl/wm-ime-char) é enviado quando um IME converte uma sequência de teclas em caracteres. Ele é enviado além da mensagem [**CHAR \_ DO WM**](/windows/desktop/inputdev/wm-char) normal.

## <a name="keyboard-state"></a>Estado do teclado

As mensagens de teclado são controladas por eventos. Ou seja, você obterá uma mensagem quando algo interessante acontecer, como uma tecla pressionada, e a mensagem informa o que acabou de acontecer. Mas você também pode testar o estado de uma chave a qualquer momento, chamando a [**função GetKeyState.**](/windows/desktop/api/winuser/nf-winuser-getkeystate)

Por exemplo, considere como você detectaria a combinação de clique do mouse esquerdo + tecla ALT. Você pode acompanhar o estado da tecla ALT escutando mensagens de traço de chave e armazenar um sinalizador, mas [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) salva o problema. Quando você receber a [**mensagem WM \_ LBUTTONDOWN,**](/windows/desktop/inputdev/wm-lbuttondown) basta chamar **GetKeyState** da seguinte forma:


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



A [**mensagem GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) aceita um código de chave virtual como entrada e retorna um conjunto de sinalizadores de bits (na verdade, apenas dois sinalizadores). O valor 0x8000 contém o sinalizador de bit que testa se a chave está pressionada no momento.

A maioria dos teclados tem duas teclas ALT, esquerda e direita. O exemplo anterior testa se um deles foi pressionado. Você também pode usar [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) para distinguir entre as instâncias esquerda e direita das teclas ALT, SHIFT ou CTRL. Por exemplo, o código a seguir testa se a tecla ALT correta é pressionada.


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



A [**função GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) é interessante porque relata um *estado de teclado virtual.* Esse estado virtual é baseado no conteúdo da fila de mensagens e é atualizado conforme você remove mensagens da fila. À medida que o programa processa mensagens de janela, **GetKeyState** fornece um instantâneo do teclado no momento em que cada mensagem foi enxuada. Por exemplo, se a última mensagem na fila for [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** relata o estado do teclado no momento em que o usuário clicou no botão do mouse.

Como [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) é baseado em sua fila de mensagens, ele também ignora a entrada do teclado que foi enviada para outro programa. Se o usuário alternar para outro programa, qualquer tecla pressionada enviada para esse programa será ignorada por **GetKeyState.** Se você realmente quiser saber o estado físico imediato do teclado, há uma função para isso: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate). No entanto, para a maioria dos códigos de interface do usuário, a função correta **é GetKeyState.**

## <a name="next"></a>Avançar

[Tabelas de acelerador](accelerator-tables.md)

 

 
