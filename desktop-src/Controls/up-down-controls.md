---
title: Sobre Up-Down controles
description: Um controle para cima para baixo é um par de botões de seta que o usuário pode clicar para incrementar ou decrementar um valor, como uma posição de rolagem ou um número exibido em um controle de acompanhamento (chamado de janela de amigos).
ms.assetid: ae2c0283-9cad-40d1-b8a6-a90484a95f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749014a4b9959b8afd6e769919a0dc9df19e99ce4edeabca774e535f26f4cf8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132147"
---
# <a name="about-up-down-controls"></a>Sobre Up-Down controles

Um controle para cima para baixo é um par de botões de seta que o usuário pode clicar para incrementar ou decrementar um valor, como uma posição de rolagem ou um número exibido em um controle de acompanhamento (chamado de janela de amigos).

Para o usuário, um controle up-down e sua janela de parceiro geralmente se parecem com um único controle. Você pode especificar que um controle para cima e para baixo se posiciona automaticamente ao lado de sua janela mais nova e que ele de definiu automaticamente a legenda da janela do parceiro para sua posição atual. Por exemplo, você pode usar um controle up-down com um controle de edição para solicitar ao usuário uma entrada numérica. A ilustração a seguir mostra um controle de cima para baixo com um controle de edição como sua janela de amigos, uma combinação que às vezes é chamada de controle girador.

![captura de tela mostrando um controle retangular curto e largo com setas para cima e para baixo na borda direita](images/updown.jpg)

Os tópicos a seguir são discutidos nesta seção.

-   [Estilos de controle para cima para baixo](#up-down-control-styles)
-   [Posição e aceleração](#position-and-acceleration)
-   [Processamento de mensagens Up-Down controles padrão](#default-up-down-controls-message-processing)

## <a name="up-down-control-styles"></a>Up-Down de controle

Usando estilos de janela, você pode manipular características de um controle para cima para baixo, como como ele se posiciona em relação à janela mais nova, se ele define o texto de sua janela de amigos e se ele processa as teclas SETA PARA CIMA e SETA PARA BAIXO.

Um controle de cima para baixo com o estilo [**\_ ALIGNLEFT**](up-down-control-styles.md) ou [**UDS \_ ALIGNRIGHT do UDS**](up-down-control-styles.md) se alinha com a borda esquerda ou direita da janela do seu parceiro. A largura da janela do parceiro é reduzida para acomodar a largura do controle de cima para baixo.

Um controle para cima para baixo com o [**estilo \_ SETBUDDYINT do UDS**](up-down-control-styles.md) define a legenda de sua janela de parceiro sempre que a posição atual é muda. O controle insere um separador de milhares entre cada três dígitos de uma cadeia de caracteres decimal, a menos que o estilo [**\_ UDS NOTHOUSANDS**](up-down-control-styles.md) seja especificado. Se a janela do parceiro for uma caixa de listagem, um controle para cima e para baixo define sua seleção atual em vez de sua legenda.

Você pode especificar o [**estilo UDS \_ ARROWKEYS**](up-down-control-styles.md) para fornecer uma interface de teclado para um controle de cima para baixo. Se esse estilo for especificado, o controle processa as teclas de seta para cima e para baixo. O controle também subclasse a janela do parceiro para que ele possa processar essas chaves quando a janela do parceiro tiver o foco.

Se você usar um controle up-down para rolagem horizontal, poderá especificar o estilo [**\_ UDS HORZ.**](up-down-control-styles.md) Esse estilo faz com que as setas do controle para cima para baixo apontem para a esquerda e para a direita em vez de para cima e para baixo.

Por padrão, a posição atual não mudará se o usuário tentar incrementá-la ou decrementá-la além do valor máximo ou mínimo. Você pode alterar esse comportamento usando o estilo [**\_ WRAP do UDS,**](up-down-control-styles.md) de modo que a posição "wraps" para o extremo oposto. Por exemplo, incrementar após o limite superior quebra a posição de volta para o limite inferior.

## <a name="position-and-acceleration"></a>Posição e aceleração

Depois que um controle para cima para baixo for criado, você poderá alterar a posição atual, a posição mínima e a posição máxima do controle enviando mensagens. Você também pode alterar a base de rádio usada para exibir a posição atual na janela do colega e a taxa na qual a posição atual muda quando a seta para cima ou para baixo é clicada.

Para recuperar a posição atual de um controle up-down, use a [**mensagem \_ GETPOS do UDM.**](udm-getpos.md) Para um controle de cima para baixo com uma janela de parceiro, a posição atual é o número na legenda da janela do parceiro. Como a legenda pode ter sido alterada (por exemplo, o usuário pode ter editado o texto de um controle de edição), o controle para cima para baixo recupera a legenda atual e atualiza sua posição atual de acordo.

A legenda da janela do colega pode ser uma cadeia de caracteres decimal ou hexadecimal, dependendo da base de rádio (ou seja, base 10 ou 16) do controle de cima para baixo. Você pode definir a base de rádio usando a mensagem [**\_ SETBASE do UDM**](udm-setbase.md) e recuperar a base de rádio usando a [**mensagem \_ GETBASE do UDM.**](udm-getbase.md)

A [**mensagem \_ SETPOS do UDM**](udm-setpos.md) define a posição atual de uma janela do parceiro. Observe que, ao contrário de uma barra de rolagem, um controle para cima e para baixo altera automaticamente sua posição atual quando as setas para cima e para baixo são clicadas. Um aplicativo, portanto, não precisa definir a posição atual ao processar a mensagem [**WM \_ VSCROLL**](wm-vscroll.md) ou [**WM \_ HSCROLL.**](wm-hscroll.md)

Você pode alterar as posições mínima e máxima de um controle up-down usando a [**mensagem \_ SETRANGE do UDM.**](udm-setrange.md) A posição máxima pode ser menor que a mínima e, nesse caso, clicar no botão de seta para cima diminui a posição atual. Para colocá-lo de outra maneira, para cima significa mover para a posição máxima. Para recuperar as posições mínima e máxima para um controle de cima para baixo, use a [**mensagem \_ GETRANGE do UDM.**](udm-getrange.md)

Você pode controlar a taxa na qual a posição muda quando o usuário mantém um botão de seta para baixo definindo a aceleração do controle para cima para baixo. A aceleração é definida por uma matriz de [**estruturas UDACCEL.**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) Cada estrutura especifica um intervalo de tempo e o número de unidades pelas quais incrementar ou decrementar no final desse intervalo. Para definir a aceleração, use a [**mensagem \_ UDM SETACCEL.**](udm-setaccel.md) Para recuperar informações de aceleração, use a [**mensagem \_ GETACCEL do UDM.**](udm-getaccel.md)

## <a name="default-up-down-controls-message-processing"></a>Processamento de mensagens Up-Down controles padrão

Esta seção descreve as mensagens Windows padrão processadas por um controle up-down.



| Mensagem                                        | Processamento executado                                                                                                                                                                                         |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)             | Aloca e inicializa uma estrutura de dados privada e salva seu endereço como dados de janela.                                                                                                                     |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)           | Libera os dados alocados durante o [**processamento de WM \_ CREATE.**](/windows/desktop/winmsg/wm-create)                                                                                                                                   |
| [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)             | Invalida a janela.                                                                                                                                                                                      |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)         | Altera a posição atual no caso de uma tecla SETA PARA CIMA ou SETA PARA BAIXO.                                                                                                                                   |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)             | Conclui a alteração de posição.                                                                                                                                                                               |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) | Captura o mouse. Se a janela do parceiro for um controle de edição ou uma caixa de listagem, ela define o foco para a janela do parceiro. Se o mouse estiver sobre o botão para cima ou para baixo, ele começará a alterar a posição e define um temporizador. |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)     | Conclui a alteração de posição e libera a captura do mouse se o controle para cima para baixo tiver capturado o mouse. Se a janela do parceiro for um controle de edição, ela selecionará todo o texto no controle de edição.             |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                  | Pinta o controle de cima para baixo. Se o *parâmetro wParam* for não NULL, o controle assumirá que o valor é um **HDC** e pintará usando esse contexto de dispositivo.                                                    |
| [**TEMPORIZADOR \_ DE WM**](/windows/desktop/winmsg/wm-timer)               | Altera a posição atual se o mouse estiver sendo pressionado sobre um botão e um intervalo suficiente tiver decorrido.                                                                                            |



 

 

 