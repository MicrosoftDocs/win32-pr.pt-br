---
title: Sobre carets
description: Este tópico aborda os pontos de cuidado.
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- recursos, pontos de cuidado
- carets, removendo
- linhas piscando
- blocos piscando
- bitmaps piscando
- carets, visibilidade
- carets, tempos de piscar
- tempos de piscar
- carets,positions
- removendo os pontos de cuidado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ed2cbe50771b893c7a2ccc0874a882aabb23a1d0b4ba27822d7ce0ec47a18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461316"
---
# <a name="about-carets"></a>Sobre carets

O sistema fornece um a caret por fila de mensagens. Uma janela deve criar um achamado somente quando ele tiver o foco do teclado ou estiver ativo. A janela deve destruir o a tecla caret antes de perder o foco do teclado ou ficar inativa. Para obter mais informações sobre a entrada do teclado, consulte [Entrada do teclado.](/windows/desktop/inputdev/keyboard-input)

Use a [**função CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) para especificar os parâmetros de um acento. O sistema forma um a careta invertendo a cor do pixel dentro do retângulo especificado pela posição, largura e altura do caret. A largura e a altura são especificadas em unidades lógicas; portanto, a aparência de um cursor está sujeita ao modo de mapeamento da janela.

Os tópicos a seguir são discutidos nesta seção.

-   [Visibilidade do caret](#caret-visibility)
-   [Horário de piscar do a caret](#caret-blink-time)
-   [Posição do caret](#caret-position)
-   [Removendo um caret](#removing-a-caret)

## <a name="caret-visibility"></a>Visibilidade do caret

Depois que o cursor for definido, use a [**função ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) para tornar o cursor visível. Quando o cursor é exibido, ele começa automaticamente a piscar. Para exibir um a careta sólido, o sistema inverte cada pixel no retângulo; para exibir um acinzenta, o sistema inverte todos os outros pixels; para exibir um bitmap caret, o sistema inverte apenas os bits em branco do bitmap.

## <a name="caret-blink-time"></a>Horário de piscar do a caret

O tempo decorrido, em milissegundos, necessário para inverter o aro é chamado de hora *de piscar.* O afileiramento piscará, desde que o thread que possui a fila de mensagens tenha uma bomba de mensagens que processa as mensagens.

O usuário pode definir a hora de piscar do cursor usando o Painel de Controle e os aplicativos devem respeitar as configurações escolhidas pelo usuário. Um aplicativo pode determinar o tempo de piscar do aro usando a [**função GetCaretBlinkTime.**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) Se você estiver escrevendo um aplicativo que permite que o usuário ajuste a hora de piscar, como um applet Painel de Controle, use a função [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) para definir a taxa do tempo de piscar para um número especificado de milissegundos.

O *tempo de flash* é o tempo decorrido, em milissegundos, necessário para exibir, inverter e restaurar a exibição do aro. O tempo de flash de um a careta é duas vezes maior que a hora de piscar.

## <a name="caret-position"></a>Posição do caret

Você pode determinar a posição do aro usando a [**função GetCaretPos.**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) A posição, em coordenadas do cliente, é copiada para uma estrutura especificada por um parâmetro em **GetCaretPos.** Um aplicativo pode mover um aro em uma janela usando a [**função SetCaretPos.**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) Uma janela só poderá mover um a caret se ele já tiver o achamado. **SetCaretPos** pode mover o aro se ele está visível ou não.

## <a name="removing-a-caret"></a>Removendo um caret

Você pode remover temporariamente um a carete ocultando-o ou pode remover permanentemente o a caret, destrói-o. Para ocultar o aro, use a [**função HideCaret.**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) Isso é útil quando seu aplicativo deve redesenhar a tela durante o processamento de uma mensagem, mas deve manter o sinal de adoção fora do caminho. Quando o aplicativo terminar de desenhar, ele poderá exibir o aro novamente usando a [**função ShowCaret.**](/windows/desktop/api/Winuser/nf-winuser-showcaret) Ocultar o a careta não destrói sua forma nem invalida o ponto de inserção. Ocultar o a careta é cumulativo; ou seja, se o aplicativo chamar **HideCaret** cinco vezes, ele também deverá chamar **ShowCaret** cinco vezes antes que o aro reaparecer.

Para remover o aro da tela e destruir sua forma, use a [**função DestroyCaret.**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) **DestroyCaret** destruirá o aro somente se a janela envolvida na tarefa atual possuir o aro.

 

 