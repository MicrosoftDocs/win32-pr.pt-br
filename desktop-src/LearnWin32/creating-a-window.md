---
title: Criando uma janela
description: .
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126f040d72fec423ad5b6f3ecb31bc780a3192b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366026"
---
# <a name="creating-a-window"></a>Criando uma janela

## <a name="window-classes"></a>Classes de janela

Uma *classe de janela* define um conjunto de comportamentos que várias janelas podem ter em comum. Por exemplo, em um grupo de botões, cada botão tem um comportamento semelhante quando o usuário clica no botão. É claro que os botões não são completamente idênticos; cada botão exibe sua própria cadeia de texto e tem suas próprias coordenadas de tela. Os dados exclusivos para cada janela são chamados de *dados de instância*.

Cada janela deve ser associada a uma classe de janela, mesmo que seu programa nunca crie uma instância dessa classe. É importante entender que uma classe de janela não é uma "classe" no sentido C++. Em vez disso, é uma estrutura de dados usada internamente pelo sistema operacional. As classes de janela são registradas com o sistema em tempo de execução. Para registrar uma nova classe de janela, comece preenchendo uma estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) :

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

Você deve definir os seguintes membros da estrutura:

- **lpfnWndProc** é um ponteiro para uma função definida pelo aplicativo chamada de *procedimento de janela* ou "proc de janela". O procedimento de janela define a maior parte do comportamento da janela. Examinaremos o procedimento de janela detalhadamente mais tarde. Por enquanto, apenas trate isso como uma referência posterior.
- **HINSTANCE** é o identificador para a instância do aplicativo. Obtenha esse valor do parâmetro *HINSTANCE* de **wWinMain**.
- **lpszClassName** é uma cadeia de caracteres que identifica a classe da janela.

Os nomes de classe são locais para o processo atual, portanto, o nome só precisa ser exclusivo dentro do processo. No entanto, os controles padrão do Windows também têm classes. Se você usar qualquer um desses controles, deverá escolher nomes de classe que não estejam em conflito com os nomes de classe de controle. Por exemplo, a classe Window para o controle Button é chamada de "Button".

A estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) tem outros membros não mostrados aqui. Você pode defini-los como zero, conforme mostrado neste exemplo, ou preenchê-los em. A documentação do MSDN descreve a estrutura em detalhes.

Em seguida, passe o endereço da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) para a função [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) . Essa função registra a classe Window com o sistema operacional.

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a>Criando a janela

Para criar uma nova instância de uma janela, chame a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) :

```C++
HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}
```

Você pode ler descrições de parâmetros detalhadas no MSDN, mas aqui está um resumo rápido:

- O primeiro parâmetro permite que você especifique alguns comportamentos opcionais para a janela (por exemplo, janelas transparentes). Defina esse parâmetro como zero para os comportamentos padrão.
- `CLASS_NAME` é o nome da classe da janela. Isso define o tipo de janela que você está criando.
- O texto da janela é usado de maneiras diferentes por tipos diferentes de janelas. Se a janela tiver uma barra de título, o texto será exibido na barra de título.
- O estilo de janela é um conjunto de sinalizadores que definem algumas das aparências de uma janela. A constante **WS \_ OVERLAPPEDWINDOW** é, na verdade, vários sinalizadores combinados com **um OR-bit.** Juntos, esses sinalizadores dão à janela uma barra de título, uma borda, um menu do sistema e **minimizam** e **maximizam** os botões. Esse conjunto de sinalizadores é o estilo mais comum para uma janela de aplicativo de nível superior.
- Para posição e tamanho, a constante de **PV de \_ USEDEFAULT** significa usar valores padrão.
- O próximo parâmetro define uma janela pai ou uma janela de proprietário para a nova janela. Defina o pai se você estiver criando uma janela filho. Para uma janela de nível superior, defina como **NULL**.
- Para uma janela de aplicativo, o próximo parâmetro define o menu para a janela. Este exemplo não usa um menu, portanto, o valor é **NULL**.
- *HINSTANCE* é o identificador de instância, descrito anteriormente. (Consulte [WinMain: o ponto de entrada do aplicativo](winmain--the-application-entry-point.md).)
- O último parâmetro é um ponteiro para dados arbitrários do **tipo \* void**. Você pode usar esse valor para passar uma estrutura de dados para o procedimento de janela. Mostraremos uma maneira possível de usar esse parâmetro na seção [Gerenciando o estado do aplicativo](managing-application-state-.md).

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) retornará um identificador para a nova janela ou zero se a função falhar. Para mostrar a janela — ou seja, tornar a janela visível — passe o identificador de janela para a função de [**janela**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

```C++
ShowWindow(hwnd, nCmdShow);
```

O parâmetro *HWND* é o identificador de janela retornado por [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). O parâmetro *nCmdShow* pode ser usado para minimizar ou maximizar uma janela. O sistema operacional passa esse valor para o programa por meio da função **wWinMain** .

Este é o código completo para criar a janela. Lembre-se `WindowProc` de que ainda é apenas uma declaração de encaminhamento de uma função.

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;

RegisterClass(&wc);

// Create the window.

HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}

ShowWindow(hwnd, nCmdShow);
```

Parabéns, você criou uma janela! No momento, a janela não contém nenhum conteúdo ou interage com o usuário. Em um aplicativo de GUI real, a janela responderia a eventos do usuário e do sistema operacional. A próxima seção descreve como as mensagens de janela fornecem esse tipo de interatividade.

### <a name="next"></a>Avançar

[Mensagens de janela](window-messages.md)