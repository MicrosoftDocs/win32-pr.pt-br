---
title: Escrevendo o procedimento de janela
description: Escrevendo o procedimento de janela
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853f5effe693e10ad0c5515e9d2ea87d200a1e7dd9b0c79da46228909e53deef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520456"
---
# <a name="writing-the-window-procedure"></a>Escrevendo o procedimento de janela

A [**função DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) chama o procedimento de janela da janela que é o destino da mensagem. O procedimento de janela tem a assinatura a seguir.

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

Há quatro parâmetros:

- *hwnd* é um handle para a janela.
- *uMsg é* o código da mensagem; por exemplo, a [**mensagem WM \_ SIZE**](/windows/desktop/winmsg/wm-size) indica que a janela foi relizada.
- *wParam* e *lParam contêm* dados adicionais que pertencem à mensagem. O significado exato depende do código da mensagem.

**LRESULT** é um valor inteiro que o programa retorna para Windows. Ele contém a resposta do programa a uma mensagem específica. O significado desse valor depende do código da mensagem. **CALLBACK** é a convenção de chamada para a função.

Um procedimento de janela típico é simplesmente uma instrução switch grande que alterna o código da mensagem. Adicione casos para cada mensagem que você deseja manipular.

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

Dados adicionais para a mensagem estão contidos nos parâmetros *lParam* e *wParam.* Ambos os parâmetros são valores inteiros do tamanho de uma largura de ponteiro (32 bits ou 64 bits). O significado de cada depende do código da mensagem (*uMsg*). Para cada mensagem, você precisará procurar o código da mensagem no MSDN e castiá-los para o tipo de dados correto. Normalmente, os dados são um valor numérico ou um ponteiro para uma estrutura. Algumas mensagens não têm dados.

Por exemplo, a documentação da mensagem [**WM \_ SIZE**](/windows/desktop/winmsg/wm-size) informa que:

- *wParam* é um sinalizador que indica se a janela foi minimizada, maximizada ou ressalvada.
- *lParam* contém a nova largura e altura da janela como valores de 16 bits empacotados em um número de 32 ou 64 bits. Você precisará executar algumas mudanças de bits para obter esses valores. Felizmente, o arquivo de título WinDef.h inclui macros auxiliares que fazem isso.

Um procedimento de janela típico lida com dezenas de mensagens, para que ele possa crescer muito. Uma maneira de tornar seu código mais modular é colocar a lógica para lidar com cada mensagem em uma função separada. No procedimento de janela, caste os parâmetros *wParam* e *lParam* para o tipo de dados correto e passe esses valores para a função . Por exemplo, para lidar com [**a mensagem WM \_ SIZE,**](/windows/desktop/winmsg/wm-size) o procedimento de janela teria esta aparência:

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

As [**macros LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) [**e HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) obterão os valores de largura e altura de 16 bits de *lParam*. (Você pode procurar esses tipos de detalhes na documentação do MSDN para cada código de mensagem.) O procedimento de janela extrai a largura e a altura e, em seguida, passa esses valores para a `OnSize` função.

## <a name="default-message-handling"></a>Tratamento de mensagens padrão

Se você não tratar uma mensagem específica em seu procedimento de janela, passe os parâmetros de mensagem diretamente para a [**função DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Essa função executa a ação padrão para a mensagem, que varia de acordo com o tipo de mensagem.

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a>Evitando gargalos em seu procedimento de janela

Enquanto o procedimento de janela é executado, ele bloqueia todas as outras mensagens para janelas criadas no mesmo thread. Portanto, evite o processamento demorado dentro do procedimento de janela. Por exemplo, suponha que seu programa abra uma conexão TCP e aguarde indefinidamente para que o servidor responda. Se você fizer isso dentro do procedimento de janela, sua interface do usuário não responderá até que a solicitação seja concluída. Durante esse tempo, a janela não pode processar a entrada do mouse ou do teclado, reint si mesma ou até mesmo fechar.

Em vez disso, você deve mover o trabalho para outro thread, usando um dos recursos de multitarefa que são integrados Windows:

- Crie um novo thread.
- Use um pool de thread.
- Use chamadas de E/S assíncronas.
- Use chamadas de procedimento assíncrono.

## <a name="next"></a>Avançar

[Pintar a janela](painting-the-window.md)
