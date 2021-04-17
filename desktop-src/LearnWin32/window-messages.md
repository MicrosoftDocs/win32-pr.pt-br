---
title: Mensagens de janela (introdução ao Win32 e ao C++)
description: .
ms.assetid: 90c20456-44ed-4f0f-a6d3-b6c5660f0bc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7ea533a89cb0ccf7053945cd693cc6e1ef5c28
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "105761829"
---
# <a name="window-messages-get-started-with-win32-and-c"></a>Mensagens de janela (introdução ao Win32 e ao C++)

Um aplicativo de GUI deve responder a eventos do usuário e do sistema operacional.

- Os **eventos do usuário** incluem todas as maneiras pelas quais alguém pode interagir com seu programa: cliques do mouse, traços-chave, gestos de tela sensível ao toque e assim por diante.
- **Os eventos do sistema operacional** incluem qualquer "fora" do programa que possa afetar a forma como o programa se comporta. Por exemplo, o usuário pode conectar um novo dispositivo de hardware ou o Windows pode entrar em um estado de energia menor (suspensão ou hibernação).

Esses eventos podem ocorrer a qualquer momento enquanto o programa estiver em execução, em quase qualquer ordem. Como você estrutura um programa cujo fluxo de execução não pode ser previsto com antecedência?

Para resolver esse problema, o Windows usa um modelo de passagem de mensagens. O sistema operacional se comunica com a janela do aplicativo passando mensagens para ele. Uma mensagem é simplesmente um código numérico que designa um evento específico. Por exemplo, se o usuário pressionar o botão esquerdo do mouse, a janela receberá uma mensagem com o seguinte código de mensagem.

```C++
#define WM_LBUTTONDOWN    0x0201
```

Algumas mensagens têm dados associados a elas. Por exemplo, a mensagem do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) inclui a coordenada x e a coordenada y do cursor do mouse.

Para passar uma mensagem para uma janela, o sistema operacional chama o procedimento de janela registrado para essa janela. (E agora você sabe o que é o procedimento de janela.)

## <a name="the-message-loop"></a>O loop de mensagem

Um aplicativo receberá milhares de mensagens enquanto ele é executado. (Considere que cada pressionamento de tecla e clique no botão do mouse gera uma mensagem.) Além disso, um aplicativo pode ter várias janelas, cada uma com seu próprio procedimento de janela. Como o programa recebe todas essas mensagens e as entrega ao procedimento correto da janela? O aplicativo precisa de um loop para recuperar as mensagens e expedir para as janelas corretas.

Para cada thread que cria uma janela, o sistema operacional cria uma fila para mensagens de janela. Essa fila contém mensagens para todas as janelas criadas nesse thread. A fila em si fica oculta do seu programa. Você não pode manipular a fila diretamente. No entanto, você pode efetuar pull de uma mensagem da fila chamando a função [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) .

```C++
MSG msg;
GetMessage(&msg, NULL, 0, 0);
```

Essa função remove a primeira mensagem do início da fila. Se a fila estiver vazia, a função será bloqueada até que outra mensagem seja enfileirada. O fato de que [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) Blocks não fará com que seu programa não responda. Se não houver nenhuma mensagem, não haverá nada para o programa fazer. Se for necessário executar o processamento em segundo plano, você poderá criar threads adicionais que continuem a ser executados enquanto **GetMessage** aguardar outra mensagem. (Consulte [evitando afunilamentos em seu procedimento de janela](writing-the-window-procedure.md).)

O primeiro parâmetro de [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) é o endereço de uma estrutura de [**msg**](/windows/win32/api/winuser/ns-winuser-msg) . Se a função for realizada com sucesso, ela preencherá a estrutura de **msg** com informações sobre a mensagem. Isso inclui a janela de destino e o código da mensagem. Os outros três parâmetros permitem filtrar quais mensagens você obtém da fila. Em quase todos os casos, você definirá esses parâmetros como zero.

Embora a estrutura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) contenha informações sobre a mensagem, você quase nunca examinará essa estrutura diretamente. Em vez disso, você irá passá-lo diretamente para duas outras funções.

```C++
TranslateMessage(&msg); 
DispatchMessage(&msg);
```

A função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) está relacionada à entrada do teclado. Ele converte pressionamentos de teclas (chave para baixo, tecla para cima) em caracteres. Você não precisa realmente saber como essa função funciona; Apenas lembre-se de chamá-lo antes de [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). O link para a documentação do MSDN fornecerá mais informações, se você estiver curioso.

A função [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) informa o sistema operacional para chamar o procedimento de janela da janela que é o destino da mensagem. Em outras palavras, o sistema operacional procura o identificador de janela em sua tabela do Windows, localiza o ponteiro de função associado à janela e invoca a função.

Por exemplo, suponha que o usuário pressione o botão esquerdo do mouse. Isso causa uma cadeia de eventos:

1. O sistema operacional coloca uma [**mensagem \_ LBUTTONDOWN do WM**](/windows/desktop/inputdev/wm-lbuttondown) na fila de mensagens.
2. Seu programa chama a função [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) .
3. [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) extrai a mensagem [**\_ LBUTTONDOWN do WM**](/windows/desktop/inputdev/wm-lbuttondown) da fila e preenche a estrutura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) .
4. Seu programa chama as funções [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .
5. Dentro de [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), o sistema operacional chama o procedimento de janela.
6. O procedimento de janela pode responder à mensagem ou ignorá-la.

Quando o procedimento de janela retorna, ele retorna de volta para [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). Isso retorna ao loop de mensagem para a próxima mensagem. Desde que o programa esteja em execução, as mensagens continuarão a chegar na fila. Portanto, você deve ter um loop que recebe continuamente as mensagens da fila e as envia. Você pode considerar o loop da seguinte maneira:

```C++
// WARNING: Don't actually write your loop this way.

while (1)      
{
    GetMessage(&msg, NULL, 0,  0);
    TranslateMessage(&msg); 
    DispatchMessage(&msg);
}
```

Como escrito, é claro que esse loop nunca terminaria. É aí que entra o valor de retorno para a função [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) . Normalmente, **GetMessage** retorna um valor diferente de zero. Quando você quiser sair do aplicativo e interromper o loop de mensagem, chame a função [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) .

```C++
        PostQuitMessage(0);
```

A função [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) coloca uma mensagem do [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) na fila de mensagens. **WM \_ QUIT** é uma mensagem especial: faz que [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) retorne zero, sinalizando o final do loop de mensagem. Aqui está o loop de mensagem revisado.

```C++
// Correct.

MSG msg = { };
while (GetMessage(&msg, NULL, 0, 0) > 0)
{
    TranslateMessage(&msg);
    DispatchMessage(&msg);
}
```

Desde que [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) retorne um valor diferente de zero, a expressão no loop **while** é avaliada como true. Depois de chamar [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage), a expressão se tornará falsa e o programa interromperá o loop. (Um resultado interessante desse comportamento é que o procedimento de janela nunca recebe uma mensagem do [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) . Portanto, você não precisa ter uma instrução Case para essa mensagem em seu procedimento de janela.)

A próxima pergunta óbvia é quando chamar [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage). Retornaremos a essa pergunta no tópico [fechando a janela](closing-the-window.md), mas primeiro precisamos escrever nosso procedimento de janela.

## <a name="posted-messages-versus-sent-messages"></a>Mensagens postadas versus mensagens enviadas

A seção anterior falou sobre as mensagens que entram em uma fila. Às vezes, o sistema operacional chamará um procedimento de janela diretamente, ignorando a fila.

A terminologia para essa distinção pode ser confusa:

-   A *postagem* de uma mensagem significa que a mensagem é exibida na fila de mensagens e é expedida por meio do loop de mensagem ([**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) e [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)).
-   O *envio* de uma mensagem significa que a mensagem ignora a fila e o sistema operacional chama o procedimento de janela diretamente.

Por enquanto, a diferença não é muito importante. O procedimento de janela manipula todas as mensagens. No entanto, algumas mensagens ignoram a fila e vão diretamente para o procedimento de janela. No entanto, ele pode fazer uma diferença se seu aplicativo se comunicar entre o Windows. Você pode encontrar uma discussão mais completa sobre esse problema no tópico [sobre mensagens e filas](/windows/desktop/winmsg/about-messages-and-message-queues)de mensagens.

## <a name="next"></a>Avançar

[Escrevendo o procedimento de janela](writing-the-window-procedure.md)
