---
title: Estados do botão
description: Esta seção discute como selecionar um botão altera seu estado e como o aplicativo deve responder.
ms.assetid: 7302f0f3-f29d-43d7-8e25-4f36d5ef6a86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96865191ac64b14dd35ff1d22631c6bf11763aff
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454397"
---
# <a name="button-states"></a>Estados do botão

Esta seção discute como selecionar um botão altera seu estado e como o aplicativo deve responder.

A seção consiste nos seguintes tópicos:

-   [Seleção de botão](#button-selection)
-   [Elementos de um estado de botão](#elements-of-a-button-state)
    -   [Estado de foco](#focus-state)
    -   [Estado de push](#push-state)
    -   [Estado de verificação](#check-state)
-   [Alterações em um estado de botão](#changes-to-a-button-state)

## <a name="button-selection"></a>Seleção de botão

O usuário pode selecionar um botão de três maneiras: clicando nele com o mouse, alternando para ele e, em seguida, pressionando a tecla ENTER ou (se o botão fizer parte de um grupo definido pelo estilo [**de \_ grupo WS**](/windows/desktop/winmsg/window-styles) ), alternando para o botão selecionado no grupo e usando as teclas de direção para mover dentro desse grupo. Os dois métodos de tabulação fazem parte da interface de teclado predefinida fornecida pelo sistema. Para obter uma descrição completa desta interface, consulte [caixas de diálogo](/windows/desktop/dlgbox/dialog-boxes).

A seleção de um botão geralmente causa os seguintes eventos:

-   O sistema dá ao botão o foco do teclado.
-   O botão envia à janela pai uma mensagem para notificá-la da seleção.
-   A janela pai (ou o sistema) envia ao botão uma mensagem para alterar seu estado.
-   A janela pai (ou o sistema) redesenha o botão para refletir seu novo estado.

## <a name="elements-of-a-button-state"></a>Elementos de um estado de botão

O estado de um botão pode ser caracterizado por seu estado de foco, estado de push e estado de verificação.

-   [Estado de foco](#focus-state)
-   [Estado de push](#push-state)
-   [Estado de verificação](#check-state)

### <a name="focus-state"></a>Estado de foco

O estado de foco se aplica a uma caixa de seleção, botão de opção, botão de ação ou botão desenhado pelo proprietário. Um botão recebe o foco do teclado quando o usuário o seleciona e perde o foco quando o usuário seleciona outro controle. Somente um controle pode ter o foco do teclado por vez.

Quando um botão tem o foco do teclado, o sistema normalmente realça o texto, o ícone ou o bitmap de um botão ao redor dele com uma linha pontilhada. Além disso, um botão de ação tem uma borda espessa escura quando tem o foco. O sistema altera automaticamente o realce de um botão automático, mas o aplicativo deve alterar o realce de um botão não automático enviando mensagens.

### <a name="push-state"></a>Estado de push

O estado de push aplica-se a um botão de ação, caixa de seleção, botão de opção ou caixa de seleção de três Estados, mas não se aplica a outros botões. O estado de push de um botão pode ser enviado por Push ou não ser enviado por push. Quando um botão de ação (ou qualquer botão com o estilo [**BS \_ PUSHLIKE**](button-styles.md) ) é enviado por push, o botão é desenhado como um botão de baixo e baixo. Quando não é enviado por push, ele é desenhado como um botão gerado. Quando uma caixa de seleção, um botão de opção ou uma caixa de seleção de três Estados é clicado, o plano de fundo do botão fica acinzentado. Quando não for enviado por push, o plano de fundo do botão não ficará acinzentado.

### <a name="check-state"></a>Estado de verificação

O estado de verificação se aplica a uma caixa de seleção, a um botão de opção ou a uma caixa de seleção de três Estados, mas não se aplica a outros botões. O estado pode ser marcado, limpo ou (para caixas de seleção de três Estados) indeterminado. Uma caixa de seleção é marcada quando contém uma marca de seleção e é apagada quando não. Um botão de opção é verificado quando contém um ponto preto; Ele é limpo quando não faz isso. Uma caixa de seleção de três Estados é marcada quando ela contém uma marca de seleção, é apagada quando não é, e é indeterminada quando contém uma caixa cinza. O sistema altera automaticamente o estado de verificação de um botão automático, mas o aplicativo deve alterar o estado de verificação de um botão não automático.

## <a name="changes-to-a-button-state"></a>Alterações em um estado de botão

Quando o usuário seleciona um botão, geralmente é necessário alterar um ou mais dos elementos de estado do botão. O sistema altera automaticamente o estado de foco para todos os tipos de botão, o estado de push para botões de Push ou botões com o estilo [**BS \_ PUSHLIKE**](button-styles.md) e o estado de verificação para todos os botões automáticos. O aplicativo deve fazer todas as outras alterações de estado, levando em conta o tipo, o estilo e o estado atual do botão. A lista a seguir mostra os elementos de estado que devem ser alterados para cada tipo de botão:

-   Uma caixa de seleção deve alterar o estado de verificação.
-   Um botão de opção deve alterar o estado de verificação. Também pode ser necessário alterar o estado de verificação de outros botões de opção no mesmo grupo para garantir a natureza mutuamente exclusiva dos botões de opção.
-   Como o estado de um botão desenhado pelo proprietário é dependente do aplicativo, o que o aplicativo deve alterar no botão pode variar. Nenhum elemento de uma caixa de grupo deve ser alterado, pois os usuários não podem selecionar caixas de grupo.

Um aplicativo pode determinar o estado de um botão enviando a ele uma mensagem [**BM \_ getcheck**](bm-getcheck.md) ou [**BM \_ GetState**](bm-getstate.md) ; o aplicativo pode definir o estado de um botão enviando-o a uma mensagem [**BM \_ SetCheck**](bm-setcheck.md) ou [**BM \_ SetState**](bm-setstate.md) .

 

 