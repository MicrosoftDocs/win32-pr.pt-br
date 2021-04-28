---
title: Escrevendo o procedimento de janela
description: Escrevendo o procedimento de janela
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832aba88211a7decf20c233f5d9ab4fbeb1b1c27
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105714"
---
# <a name="writing-the-window-procedure"></a>Escrevendo o procedimento de janela

A função [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) chama o procedimento de janela da janela que é o destino da mensagem. O procedimento de janela tem a assinatura a seguir.

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

Há quatro parâmetros:

- *HWND* é um identificador para a janela.
- *uMsg* é o código da mensagem; por exemplo, a mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) indica que a janela foi redimensionada.
- *wParam* e *lParam* contêm dados adicionais que pertencem à mensagem. O significado exato depende do código da mensagem.

**LRESULT** é um valor inteiro que seu programa retorna ao Windows. Ele contém a resposta do programa a uma mensagem específica. O significado desse valor depende do código da mensagem. O **retorno** de chamada é a Convenção de chamada para a função.

Um procedimento de janela típico é simplesmente uma grande instrução switch que alterna o código da mensagem. Adicione casos para cada mensagem que você deseja manipular.

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

Dados adicionais para a mensagem estão contidos nos parâmetros *lParam* e *wParam* . Ambos os parâmetros são valores inteiros do tamanho de uma largura de ponteiro (32 bits ou 64 bits). O significado de cada um depende do código da mensagem (*uMsg*). Para cada mensagem, você precisará pesquisar o código de mensagem no MSDN e converter os parâmetros para o tipo de dados correto. Normalmente, os dados são um valor numérico ou um ponteiro para uma estrutura. Algumas mensagens não têm nenhum dado.

Por exemplo, a documentação para a mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) informa que:

- *wParam* é um sinalizador que indica se a janela foi minimizada, maximizada ou redimensionada.
- *lParam* contém a nova largura e a altura da janela como valores de 16 bits empacotados no número 1 32-ou 64-bit. Você precisará executar uma mudança de bits para obter esses valores. Felizmente, o arquivo de cabeçalho WinDef. h inclui macros auxiliares que fazem isso.

Um procedimento de janela típico lida com dezenas de mensagens, para que possa aumentar muito tempo. Uma maneira de tornar seu código mais modular é colocar a lógica para manipular cada mensagem em uma função separada. No procedimento de janela, converta os parâmetros *wParam* e *lParam* no tipo de dados correto e passe esses valores para a função. Por exemplo, para manipular a mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) , o procedimento da janela ficaria assim:

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

As macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) obtêm os valores de largura e altura de 16 bits do *lParam*. (Você pode procurar esses tipos de detalhes na documentação do MSDN para cada código de mensagem.) O procedimento de janela extrai a largura e a altura e, em seguida, passa esses valores para a `OnSize` função.

## <a name="default-message-handling"></a>Manipulação de mensagens padrão

Se você não tratar uma mensagem específica em seu procedimento de janela, passe os parâmetros da mensagem diretamente para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Essa função executa a ação padrão para a mensagem, que varia por tipo de mensagem.

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a>Evitando afunilamentos em seu procedimento de janela

Enquanto o procedimento de janela é executado, ele bloqueia todas as outras mensagens do Windows criadas no mesmo thread. Portanto, evite processamento longo dentro de seu procedimento de janela. Por exemplo, suponha que seu programa abra uma conexão TCP e espere indefinidamente que o servidor responda. Se você fizer isso dentro do procedimento de janela, sua interface do usuário não responderá até que a solicitação seja concluída. Durante esse tempo, a janela não pode processar a entrada do mouse ou do teclado, redesenhar a si mesma ou até mesmo fechar.

Em vez disso, você deve mover o trabalho para outro thread, usando um dos recursos de multitarefa que são criados no Windows:

- Crie um novo thread.
- Use um pool de thread.
- Usar chamadas de e/s assíncronas.
- Usar chamadas de procedimento assíncronos.

## <a name="next"></a>Avançar

[Pintando a janela](painting-the-window.md)
