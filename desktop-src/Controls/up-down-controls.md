---
title: Sobre controles de Up-Down
description: Um controle de cima para baixo é um par de botões de seta que o usuário pode clicar para incrementar ou decrementar um valor, como uma posição de rolagem ou um número exibido em um controle complementar (chamado de janela Buddy).
ms.assetid: ae2c0283-9cad-40d1-b8a6-a90484a95f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc8dad15a8254b138cae4175cc16b1ef3111745
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641920"
---
# <a name="about-up-down-controls"></a>Sobre controles de Up-Down

Um controle de cima para baixo é um par de botões de seta que o usuário pode clicar para incrementar ou decrementar um valor, como uma posição de rolagem ou um número exibido em um controle complementar (chamado de janela Buddy).

Para o usuário, um controle up e sua janela Buddy geralmente se parecem com um único controle. Você pode especificar que um controle de cima para baixo se Posicione automaticamente ao lado de sua janela Buddy e que ele defina automaticamente a legenda da janela Buddy para sua posição atual. Por exemplo, você pode usar um controle de cima para baixo com um controle de edição para solicitar ao usuário uma entrada numérica. A ilustração a seguir mostra um controle de cima para baixo com um controle de edição como sua janela Buddy, uma combinação que às vezes é referenciada como um controle Spinner.

![captura de tela mostrando um controle retangular curto e largo com setas para cima e para baixo na borda direita](images/updown.jpg)

Os tópicos a seguir são discutidos nesta seção.

-   [Estilos de controle de cima para baixo](#up-down-control-styles)
-   [Posição e aceleração](#position-and-acceleration)
-   [Up-Down padrão controla o processamento de mensagens](#default-up-down-controls-message-processing)

## <a name="up-down-control-styles"></a>Up-Down estilos de controle

Usando estilos de janela, você pode manipular características de um controle de cima para baixo, como como ele se posiciona em relação à sua janela Buddy, se ele define o texto de sua janela Buddy e se ele processa as teclas de seta para cima e para baixo.

Um controle de cima para baixo com o estilo [**UDS \_ ALIGNLEFT**](up-down-control-styles.md) ou [**UDS \_ ALIGNRIGHT**](up-down-control-styles.md) se alinha com a borda esquerda ou direita de sua janela Buddy. A largura da janela Buddy é diminuída para acomodar a largura do controle acima-abaixo.

Um controle de cima para baixo com o estilo [**UDS \_ SETBUDDYINT**](up-down-control-styles.md) define a legenda de sua janela Buddy sempre que a posição atual é alterada. O controle insere um separador de milhar entre cada três dígitos de uma cadeia de caracteres decimal, a menos que o estilo [**UDS \_ nomilhares**](up-down-control-styles.md) seja especificado. Se a janela Buddy for uma caixa de listagem, um controle up definirá sua seleção atual em vez de sua legenda.

Você pode especificar o estilo [**UDS \_ ARROWKEYS**](up-down-control-styles.md) para fornecer uma interface de teclado para um controle de cima para baixo. Se esse estilo for especificado, o controle processará as teclas de seta para cima e para baixo. O controle também subclasses da janela Buddy para que possa processar essas chaves quando a janela Buddy tiver o foco.

Se você usar um controle de cima para baixo para a rolagem horizontal, poderá especificar o estilo [**UDS \_ na horizontal**](up-down-control-styles.md) . Esse estilo faz com que as setas do controle para cima para baixo apontem para a esquerda e para a direita, em vez de para cima e para baixo.

Por padrão, a posição atual não será alterada se o usuário tentar incrementar ou diminuí-lo além do valor máximo ou mínimo. Você pode alterar esse comportamento usando o estilo [**de \_ encapsulamento UDS**](up-down-control-styles.md) , portanto, a posição "encapsula" para o oposto extremo. Por exemplo, incrementar além do limite superior delimita a posição de volta para o limite inferior.

## <a name="position-and-acceleration"></a>Posição e aceleração

Depois que um controle de cima para baixo é criado, você pode alterar a posição atual do controle, a posição mínima e a posição máxima enviando mensagens. Você também pode alterar a base da Radix usada para exibir a posição atual na janela Buddy e a taxa na qual a posição atual é alterada quando a seta para cima ou para baixo é clicada.

Para recuperar a posição atual de um controle de cima para baixo, use a mensagem de [**\_ GETPOS do UDM**](udm-getpos.md) . Para um controle de cima para baixo com uma janela Buddy, a posição atual é o número na legenda da janela Buddy. Como a legenda pode ter sido alterada (por exemplo, o usuário pode ter editado o texto de um controle de edição), o controle de cima para baixo recupera a legenda atual e atualiza sua posição atual de acordo.

A legenda da janela do amigo pode ser uma cadeia de caracteres decimal ou hexadecimal, dependendo da base da Radix (ou seja, base 10 ou 16) do controle acima-abaixo. Você pode definir a base do Radix usando a mensagem do [**UDM \_ SetBase**](udm-setbase.md) e recuperar a base do Radix usando a mensagem do [**UDM \_ GetBase**](udm-getbase.md) .

A mensagem do [**UDM \_ SETPOS**](udm-setpos.md) define a posição atual de uma janela Buddy. Observe que, diferentemente de uma barra de rolagem, um controle de cima para baixo altera automaticamente sua posição atual quando as setas para cima e para baixo são clicadas. Um aplicativo, portanto, não precisa definir a posição atual ao processar a mensagem do [**WM \_ VSCROLL**](wm-vscroll.md) ou do [**WM \_ HSCROLL**](wm-hscroll.md) .

Você pode alterar as posições mínima e máxima de um controle de cima para baixo usando a mensagem do [**UDM \_ SETRANGE**](udm-setrange.md) . A posição máxima pode ser menor que o mínimo e, nesse caso, clicar no botão de seta para cima diminui a posição atual. Para colocá-lo de outra maneira, isso significa mudar para a posição máxima. Para recuperar as posições mínima e máxima para um controle de cima para baixo, use a mensagem do [**UDM \_ GetRange**](udm-getrange.md) .

Você pode controlar a taxa na qual a posição é alterada quando o usuário mantém um botão de seta ao definir a aceleração do controle de cima para baixo. A aceleração é definida por uma matriz de estruturas [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) . Cada estrutura especifica um intervalo de tempo e o número de unidades pelas quais incrementar ou decrementar no final desse intervalo. Para definir a aceleração, use a mensagem de [**\_ SETACCEL do UDM**](udm-setaccel.md) . Para recuperar informações de aceleração, use a mensagem de [**\_ GETACCEL do UDM**](udm-getaccel.md) .

## <a name="default-up-down-controls-message-processing"></a>Up-Down padrão controla o processamento de mensagens

Esta seção descreve as mensagens padrão do Windows processadas por um controle acima-abaixo.



| Mensagem                                        | Processamento realizado                                                                                                                                                                                         |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**criação do WM \_**](/windows/desktop/winmsg/wm-create)             | Aloca e Inicializa uma estrutura de dados privada e salva seu endereço como dados de janela.                                                                                                                     |
| [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)           | Libera os dados alocados durante o processamento de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) .                                                                                                                                   |
| [**habilitar o WM \_**](/windows/desktop/winmsg/wm-enable)             | Invalida a janela.                                                                                                                                                                                      |
| [**o WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)         | Altera a posição atual no caso de uma tecla de seta para cima ou seta para baixo.                                                                                                                                   |
| [**o WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)             | Conclui a alteração da posição.                                                                                                                                                                               |
| [**LBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-lbuttondown) | Captura o mouse. Se a janela Buddy for uma caixa de listagem ou controle de edição, ela definirá o foco para a janela Buddy. Se o mouse estiver sobre o botão para cima ou para baixo, ele começará a alterar a posição e definirá um temporizador. |
| [**LBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-lbuttonup)     | Concluirá a alteração da posição e liberará a captura do mouse se o controle acima-abaixo tiver capturado o mouse. Se a janela Buddy for um controle de edição, ela selecionará todo o texto no controle de edição.             |
| [**pintura do WM \_**](/windows/desktop/gdi/wm-paint)                  | Pinta o controle para cima para baixo. Se o parâmetro *wParam* for não nulo, o controle assumirá que o valor é um **HDC** e pinta usando esse contexto de dispositivo.                                                    |
| [**\_temporizador do WM**](/windows/desktop/winmsg/wm-timer)               | Altera a posição atual se o mouse estiver sendo mantido sobre um botão e um intervalo suficiente tiver decorrido.                                                                                            |



 

 

 