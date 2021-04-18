---
title: Sobre os Cursors
description: Este tópico discute os Cursors.
ms.assetid: 4487c93c-9a0f-467c-86b1-969f664d5526
keywords:
- recursos, Cursors
- Cursors, removendo
- linhas piscando
- blocos piscando
- bitmaps piscando
- interpolações, visibilidade
- interpolações, tempos de intermitência
- horários de intermitência
- Cursors, posições
- removendo os Cursors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a19eb3895ada13297f090a09529b2bcb7c75dee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105811607"
---
# <a name="about-carets"></a>Sobre os Cursors

O sistema fornece um acento circunflexo por fila de mensagens. Uma janela deve criar um cursor somente quando ele tem o foco do teclado ou está ativo. A janela deve destruir o cursor antes de perder o foco do teclado ou se tornar inativo. Para obter mais informações sobre a entrada do teclado, consulte [entrada do teclado](/windows/desktop/inputdev/keyboard-input).

Use a função [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret) para especificar os parâmetros de um cursor. O sistema forma um cursor invertendo a cor do pixel dentro do retângulo especificado pela posição, largura e altura do cursor. A largura e a altura são especificadas em unidades lógicas; Portanto, a aparência de um cursor está sujeita ao modo de mapeamento da janela.

Os tópicos a seguir são discutidos nesta seção.

-   [Visibilidade do cursor](#caret-visibility)
-   [Tempo de intermitência do cursor](#caret-blink-time)
-   [Posição do cursor](#caret-position)
-   [Removendo um cursor](#removing-a-caret)

## <a name="caret-visibility"></a>Visibilidade do cursor

Depois que o cursor for definido, use a função de [**Iscaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) para tornar o cursor visível. Quando o cursor é exibido, ele começa a piscar automaticamente. Para exibir um cursor sólido, o sistema inverte todos os pixels no retângulo; para exibir um cursor cinza, o sistema inverte todos os outros pixels; para exibir um cursor de bitmap, o sistema inverte apenas os bits brancos do bitmap.

## <a name="caret-blink-time"></a>Tempo de intermitência do cursor

O tempo decorrido, em milissegundos, necessário para inverter o cursor é chamado de *tempo de intermitência*. O cursor piscará contanto que o thread proprietário da fila de mensagens tenha um bombeamento de mensagens processando as mensagens.

O usuário pode definir o tempo de intermitência do cursor usando o painel de controle e os aplicativos devem respeitar as configurações que o usuário escolheu. Um aplicativo pode determinar o tempo de intermitência do cursor usando a função [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) . Se você estiver escrevendo um aplicativo que permite ao usuário ajustar o tempo de intermitência, como um miniaplicativo do painel de controle, use a função [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) para definir a taxa do tempo de intermitência para um número especificado de milissegundos.

O *tempo de flash* é o tempo decorrido, em milissegundos, necessário para exibir, inverter e restaurar a exibição do cursor. A hora de flash de um cursor é duas vezes maior do que o tempo de intermitência.

## <a name="caret-position"></a>Posição do cursor

Você pode determinar a posição do cursor usando a função [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos) . A posição, em coordenadas do cliente, é copiada para uma estrutura especificada por um parâmetro em **GetCaretPos**. Um aplicativo pode mover um cursor em uma janela usando a função [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos) . Uma janela pode mover um cursor somente se ele já possuir o cursor. **SetCaretPos** pode mover o cursor se ele estiver visível ou não.

## <a name="removing-a-caret"></a>Removendo um cursor

Você pode remover temporariamente um cursor ocultando-o ou pode remover permanentemente o cursor destruindo-o. Para ocultar o cursor, use a função [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret) . Isso é útil quando seu aplicativo precisa redesenhar a tela durante o processamento de uma mensagem, mas deve manter o cursor fora do caminho. Quando o aplicativo termina o desenho, ele pode exibir o cursor novamente usando a função de [**Iscaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret) . Ocultar o cursor não destrói sua forma ou invalidar o ponto de inserção. Ocultar o cursor é cumulativo; ou seja, se o aplicativo chamar **HideCaret** cinco vezes, ele também deverá chamar o **cuidado** cinco vezes antes que o cursor reapareça.

Para remover o cursor da tela e destruir sua forma, use usando a função [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret) . **DestroyCaret** destrói o cursor somente se a janela envolvida na tarefa atual possuir o cursor.

 

 