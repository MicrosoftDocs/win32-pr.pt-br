---
title: Tipos de botão
description: Há vários tipos de botões e um ou mais estilos de botão para distinguir entre os botões do mesmo tipo.
ms.assetid: bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682cc39ed2f88ce88f499757fbc4f902bfdceeea
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641924"
---
# <a name="button-types"></a>Tipos de botão

Há vários tipos de botões e um ou mais estilos de botão para distinguir entre os botões do mesmo tipo.

Este documento aborda os tópicos a seguir.

-   [Estilos e tipos de botão](#button-types-and-styles)
-   [Caixas de seleção](#check-boxes)
-   [Caixas de grupo](#group-boxes)
-   [Botões de push](#push-buttons)
-   [Botões de opção](#radio-buttons)
-   [Tópicos relacionados](#related-topics)

## <a name="button-types-and-styles"></a>Estilos e tipos de botão

Um botão pertence a um tipo e pode ter estilos adicionais que afetam sua aparência e comportamento. Para obter uma tabela de estilos de botão, consulte [estilos de botão](button-styles.md).

A captura de tela a seguir mostra os diferentes tipos de botões.

![captura de tela de uma caixa de diálogo que mostra exemplos de oito tipos de botões](images/buttontypes.png)

A captura de tela mostra como os botões podem aparecer no Windows Vista. A aparência varia em diferentes versões do sistema operacional e de acordo com o tema definido pelo usuário.

Observe os seguintes pontos sobre a ilustração:

-   A caixa de seleção de três Estados é mostrada no estado indeterminado. Quando marcada ou desmarcada, ela é semelhante a uma caixa de seleção normal.
-   O botão de push grande foi definido para o estado enviado por push (enviando a [**mensagem \_ SetState do BM**](bm-setstate.md) ), para que ele retenha sua aparência mesmo quando não estiver sendo clicado.
-   No estilo visual mostrado, o plano de fundo do botão de ação padrão (ou outro botão de ação que tem o foco de entrada) alterna entre azul e cinza.

## <a name="check-boxes"></a>Caixas de seleção

Uma *caixa de seleção* consiste em uma caixa quadrada e um rótulo, ícone ou bitmap definido pelo aplicativo que indica uma opção que o usuário pode fazer selecionando o botão. Os aplicativos normalmente exibem caixas de seleção para permitir que o usuário escolha uma ou mais opções que não são mutuamente exclusivas.

Uma caixa de seleção pode ser um dos quatro estilos: padrão, automático, três Estados e automáticos três Estados, conforme definido pela [**\_ caixa de seleção BS**](button-styles.md)constantes, [**BS \_ AUTOCHECKBOX**](button-styles.md), [**BS \_ 3STATE**](button-styles.md)e [**BS \_ AUTO3STATE**](button-styles.md), respectivamente. Cada estilo pode assumir dois Estados de verificação: marcada (uma marca de seleção dentro da caixa) ou desmarcada (sem marca de seleção). Além disso, uma caixa de seleção de três Estados pode assumir um estado indeterminado (uma caixa sombreada dentro da caixa de seleção), o que pode significar que o usuário não fez uma escolha. Clicar repetidamente em uma caixa de seleção padrão ou automática alternará da verificação para desmarcada e para trás novamente. Clicar repetidamente em uma caixa de seleção de três Estados faz com que ela seja marcada para desmarcada para indeterminada e, em seguida, repete o ciclo.

Quando o usuário clica em uma caixa de seleção (de qualquer estilo), a caixa de seleção recebe o foco do teclado. O sistema envia a janela pai da caixa de seleção uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) que contém o código de notificação [ \_ clicado em bilhão](bn-clicked.md) . A janela pai não precisa tratar essa mensagem se for proveniente de uma caixa de seleção automática ou uma caixa de seleção automática de três Estados, porque o sistema define automaticamente o estado de verificação para esses estilos. Mas a janela pai deve tratar a mensagem se for proveniente de uma caixa de seleção não automática ou de três Estados, porque a janela pai é responsável por definir o estado de verificação para esses estilos. Independentemente do estilo da caixa de seleção, o sistema repintará automaticamente a caixa de seleção quando seu estado for alterado.

O aplicativo pode verificar o estado de uma caixa de seleção usando a função [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

## <a name="group-boxes"></a>Caixas de grupo

Uma *caixa de grupo* é um retângulo que circunda um conjunto de controles, como caixas de seleção ou botões de opção, com um rótulo de texto definido pelo aplicativo em seu canto superior esquerdo. A única finalidade de uma caixa de grupo é organizar os controles relacionados por uma finalidade comum (geralmente indicada pelo rótulo). A caixa de grupo tem apenas um estilo, definido pelo CodeGroup da constante [**BS \_**](button-styles.md). Como uma caixa de grupo não pode ser selecionada, ela não tem estado de verificação, estado de foco ou estado de push.

## <a name="push-buttons"></a>Botões de push

Um *botão de ação* é um retângulo que contém um rótulo de texto definido pelo aplicativo, um ícone ou um bitmap que indica o que o botão faz quando o usuário o seleciona.

Um botão de ação pode ser um dos dois estilos, padrão ou padrão, conforme definido pelas constantes de botão de [**\_ pressão de BS**](button-styles.md) e [**BS \_ DEFPUSHBUTTON**](button-styles.md). Um botão de push padrão normalmente é usado para iniciar uma operação. Ele recebe o foco do teclado quando o usuário clica nele. Um botão de ação padrão normalmente é usado para indicar a opção mais comum ou padrão, como fechar a caixa de diálogo. É um botão que o usuário pode selecionar simplesmente pressionando ENTER quando nenhum outro botão de ação na caixa de diálogo tem o foco de entrada.

Quando o usuário clica em um botão de ação, ele recebe o foco do teclado. O sistema envia a janela pai do botão uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) que contém o código de notificação [ \_ clicado em bilhão](bn-clicked.md) .

O *botão divisão* é um tipo especial de botão de push introduzido no Windows Vista e na [versão 6, 0](common-control-versions.md). Um botão de divisão é dividido em duas partes. A parte principal funciona como um botão de ação normal ou padrão. A segunda parte tem uma seta apontando para baixo. Normalmente, um menu é exibido quando a seta é clicada.

Um botão de divisão tem o estilo de [**\_ SPLITBUTTON de BS**](button-styles.md) ou o estilo de [**\_ DEFSPLITBUTTON BS**](button-styles.md) se for o botão padrão em uma caixa de diálogo. Você pode modificar a aparência do botão usando a mensagem [**\_ SETSPLITINFO do BCM**](bcm-setsplitinfo.md) ou a macro [**\_ SETSPLITINFO do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) correspondente.

Quando o usuário clica na parte principal do botão de divisão, ele envia uma notificação [bilhão \_ clicada](bn-clicked.md) da mesma forma que um botão de ação normal. Mas quando o usuário clica na seta para baixo, ele envia uma notificação de [ \_ lista suspensa BCN](bcn-dropdown.md) . É responsabilidade do aplicativo exibir um menu em resposta à \_ lista suspensa BCN.

O Windows Vista e a [versão 6, 0](common-control-versions.md) também introduziram outro tipo de botão de ação, o *link do comando*. Visualmente, um link de comando é muito diferente de um botão de ação normal, mas tem a mesma funcionalidade. Um link de comando normalmente exibe um ícone de seta, uma linha de texto e texto adicional em uma fonte menor.

## <a name="radio-buttons"></a>Botões de opção

Um *botão* de opção (também chamado de botão de opção) consiste em um botão redondo e um rótulo, um ícone ou um bitmap definido pelo aplicativo que indica uma opção que o usuário pode fazer selecionando o botão. Um aplicativo geralmente usa botões de opção em uma caixa de grupo para permitir que o usuário escolha um conjunto de opções relacionadas, mas mutuamente exclusivas.

Um botão de opção pode ser um dos dois estilos: padrão ou automático, conforme definido pelas constantes de estilo [**BS \_ RadioButton**](button-styles.md) e [**BS \_ AUTORADIOBUTTON**](button-styles.md). Cada estilo pode assumir dois Estados de verificação: marcado (um ponto no botão) ou limpo (sem ponto no botão).

Quando o usuário seleciona um dos Estados, o botão de opção recebe o foco do teclado. O sistema envia a janela pai do botão uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) que contém o código de notificação [ \_ clicado em bilhão](bn-clicked.md) . A janela pai não precisa tratar essa mensagem se vier de um botão de opção automático, porque o sistema define automaticamente o estado de verificação para esse estilo. Mas a janela pai deve tratar a mensagem se ela vier de um botão de opção não automática, porque a janela pai é responsável por definir o estado de verificação para esse estilo. Independentemente do estilo do botão de opção, o sistema redesenha automaticamente o botão à medida que seu estado é alterado.

Os botões de opção são organizados em grupos e apenas um botão no grupo pode ser verificado a qualquer momento. Se o sinalizador do [**\_ grupo WS**](/windows/desktop/winmsg/window-styles) for definido para qualquer botão de opção, esse botão será o primeiro botão em um grupo e todos os botões que o seguem imediatamente na ordem de tabulação (mas que não têm o sinalizador do **\_ grupo WS** ) farão parte de seu grupo. Se nenhum botão de opção tiver o sinalizador de **\_ grupo WS** , todos os botões de opção na caixa de diálogo serão tratados como um único grupo.

O aplicativo pode verificar se um botão de opção é verificado usando a função [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Estilos de botão](button-styles.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Usando botões](using-buttons.md)
</dt> </dl>

 

 