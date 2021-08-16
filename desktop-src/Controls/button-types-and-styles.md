---
title: Tipos de botão
description: Há vários tipos de botões e um ou mais estilos de botão para distinguir entre botões do mesmo tipo.
ms.assetid: bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c3614f90c36d5a81603153ec7c8612d61e73e2e98c7f668cb53a6ad2bb584b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832487"
---
# <a name="button-types"></a>Tipos de botão

Há vários tipos de botões e um ou mais estilos de botão para distinguir entre botões do mesmo tipo.

Este documento discute os tópicos a seguir.

-   [Estilos e tipos de botão](#button-types-and-styles)
-   [Caixas de seleção](#check-boxes)
-   [Caixas de grupo](#group-boxes)
-   [Botões](#push-buttons)
-   [Botões](#radio-buttons)
-   [Tópicos relacionados](#related-topics)

## <a name="button-types-and-styles"></a>Estilos e tipos de botão

Um botão pertence a um tipo e pode ter estilos adicionais que afetam sua aparência e comportamento. Para uma tabela de estilos de botão, consulte [Estilos de botão](button-styles.md).

A captura de tela a seguir mostra os diferentes tipos de botões.

![captura de tela de uma caixa de diálogo que mostra exemplos de oito tipos de botões](images/buttontypes.png)

A captura de tela mostra como os botões podem aparecer no Windows Vista. A aparência variará em diferentes versões do sistema operacional e de acordo com o tema definido pelo usuário.

Observe os seguintes pontos sobre a ilustração:

-   A caixa de seleção de três estados é mostrada no estado indeterminado. Quando marcada ou desmarcada, ela se parece com uma caixa de seleção normal.
-   O botão de push grande foi definido para o estado enviado por push programaticamente (enviando a mensagem [**\_ SETSTATE BM),**](bm-setstate.md) para que ele mantenha sua aparência mesmo quando não estiver sendo clicado.
-   No estilo visual mostrado, a tela de fundo do botão de push padrão (ou outro botão de push que tem o foco de entrada) fica entre azul e cinza.

## <a name="check-boxes"></a>Caixas de seleção

Uma *caixa de* seleção consiste em uma caixa quadrada e um rótulo, ícone ou bitmap definido pelo aplicativo que indica uma escolha que o usuário pode fazer selecionando o botão. Os aplicativos normalmente exibem caixas de seleção para permitir que o usuário escolha uma ou mais opções que não são mutuamente exclusivas.

Uma caixa de seleção pode ser um dos quatro estilos: standard, automático, três estados e três estados automáticos, conforme definido pelas constantes [**BS \_ CHECKBOX**](button-styles.md), [**BS \_ AUTOCHECKBOX,**](button-styles.md) [**BS \_ 3STATE**](button-styles.md)e [**BS \_ AUTO3STATE,**](button-styles.md)respectivamente. Cada estilo pode assumir dois estados de verificação: marcado (uma marca de seleção dentro da caixa) ou des limpo (sem marca de seleção). Além disso, uma caixa de seleção de três estados pode assumir um estado indeterminado (uma caixa sombreada dentro da caixa de seleção), o que pode significar que o usuário não fez uma escolha. Clicar repetidamente em uma caixa de seleção padrão ou automática alterna-o de marcado para limpo e novamente. Clicar repetidamente em uma caixa de seleção de três estados alterna-o de marcado para limpo para indeterminado e, em seguida, repete o ciclo.

Quando o usuário clica em uma caixa de seleção (de qualquer estilo), a caixa de seleção recebe o foco do teclado. O sistema envia à janela pai da caixa de seleção uma mensagem [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) contendo o [código de notificação BN \_ CLICKED.](bn-clicked.md) A janela pai não precisa lidar com essa mensagem se ela vem de uma caixa de seleção automática ou caixa de seleção automática de três estados, porque o sistema define automaticamente o estado de verificação para esses estilos. Mas a janela pai deverá manipular a mensagem se ela vir de uma caixa de seleção não automática ou caixa de seleção de três estados, pois a janela pai é responsável por definir o estado de verificação para esses estilos. Independentemente do estilo da caixa de seleção, o sistema reintintsa automaticamente a caixa de seleção depois que seu estado é alterado.

O aplicativo pode determinar o estado de uma caixa de seleção usando a [**função IsDlgButtonChecked.**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked)

## <a name="group-boxes"></a>Caixas de grupo

Uma *caixa de* grupo é um retângulo que envolve um conjunto de controles, como caixas de seleção ou botões de opção, com um rótulo de texto definido pelo aplicativo em seu canto superior esquerdo. A única finalidade de uma caixa de grupo é organizar controles relacionados por uma finalidade comum (geralmente indicado pelo rótulo). A caixa de grupo tem apenas um estilo, definido pela constante [**BS \_ GROUPBOX.**](button-styles.md) Como uma caixa de grupo não pode ser selecionada, ela não tem estado de verificação, estado de foco ou estado de push.

## <a name="push-buttons"></a>Botões

Um *botão de push* é um retângulo que contém um rótulo de texto definido pelo aplicativo, um ícone ou um bitmap que indica o que o botão faz quando o usuário o seleciona.

Um botão de push pode ser um dos dois estilos, padrão ou padrão, conforme definido pelas constantes [**BS \_ PUSHBUTTON**](button-styles.md) e [**BS \_ DEFPTONEBUTTON**](button-styles.md). Normalmente, um botão de push padrão é usado para iniciar uma operação. Ele recebe o foco do teclado quando o usuário clica nele. Um botão de push padrão normalmente é usado para indicar a opção mais comum ou padrão, como fechar a caixa de diálogo. É um botão que o usuário pode selecionar simplesmente pressionando ENTER quando nenhum outro botão de push na caixa de diálogo tiver o foco de entrada.

Quando o usuário clica em um botão de push, ele recebe o foco do teclado. O sistema envia à janela pai do botão uma mensagem [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) que contém o [código de notificação \_ BN CLICKED.](bn-clicked.md)

O *botão de divisão* é um tipo especial de botão de push introduzido no Windows Vista e versão [6.00.](common-control-versions.md) Um botão de divisão é dividido em duas partes. A parte principal funciona como um botão de push regular ou padrão. A segunda parte tem uma seta apontando para baixo. Normalmente, um menu é exibido quando a seta é clicada.

Um botão de divisão tem o [**estilo BS \_ SPLITBUTTON**](button-styles.md) ou o estilo [**BS \_ DEFSPLITBUTTON**](button-styles.md) se for o botão padrão em uma caixa de diálogo. Você pode modificar a aparência do botão usando a [**mensagem BCM \_ SETSPLITINFO**](bcm-setsplitinfo.md) ou a macro [**\_ SetSplitInfo do**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) botão correspondente.

Quando o usuário clica na parte principal do botão de divisão, ele envia uma notificação [BN \_ CLICKED](bn-clicked.md) como um botão de push normal. Mas quando o usuário clica na seta para baixo, ele envia uma [notificação \_ DROPDOWN de BCN.](bcn-dropdown.md) É responsabilidade do aplicativo exibir um menu em resposta a BCN \_ DROPDOWN.

Windows O Vista [e a Versão 6.00 também](common-control-versions.md) introduziram outro tipo de botão de push, o link de *comando*. Visualmente, um link de comando é muito diferente de um botão de push normal, mas tem a mesma funcionalidade. Um link de comando normalmente exibe um ícone de seta, uma linha de texto e texto adicional em uma fonte menor.

## <a name="radio-buttons"></a>Botões

Um *botão de opção* (também chamado de botão de opção) consiste em um botão arredondado e um rótulo, ícone ou bitmap definido pelo aplicativo que indica uma escolha que o usuário pode fazer selecionando o botão. Um aplicativo normalmente usa botões de opção em uma caixa de grupo para permitir que o usuário escolha um de um conjunto de opções relacionadas, mas mutuamente exclusivas.

Um botão de opção pode ser um dos dois estilos: standard ou automático, conforme definido pelas constantes de estilo [**BS \_ RADIOBUTTON**](button-styles.md) e [**BS \_ AUTORDIOBUTTON**](button-styles.md). Cada estilo pode assumir dois estados de verificação: marcado (um ponto no botão) ou des limpo (sem ponto no botão).

Quando o usuário seleciona qualquer estado, o botão de opção recebe o foco do teclado. O sistema envia à janela pai do botão uma mensagem [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) contendo o [código de notificação BN \_ CLICKED.](bn-clicked.md) A janela pai não precisará lidar com essa mensagem se ela for de um botão de opção automático, pois o sistema define automaticamente o estado de verificação para esse estilo. Mas a janela pai deverá manipular a mensagem se ela for de um botão de opção não automático, pois a janela pai é responsável por definir o estado de verificação para esse estilo. Independentemente do estilo do botão de rádio, o sistema reintrói automaticamente o botão conforme seu estado muda.

Os botões de rádio são organizados em grupos e apenas um botão no grupo pode ser verificado a qualquer momento. Se o sinalizador GRUPO do [**WS \_**](/windows/desktop/winmsg/window-styles) estiver definido para qualquer botão de rádio, esse botão será o primeiro botão em um grupo e todos os botões que o seguem imediatamente na ordem de tabulação (mas não têm o sinalizador **WS \_ GROUP)** fazem parte de seu grupo. Se nenhum botão de rádio tiver o **sinalizador GRUPO \_ do WS,** todos os botões de rádio na caixa de diálogo serão tratados como um único grupo.

O aplicativo pode determinar se um botão de rádio é verificado usando a [**função IsDlgButtonChecked.**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Estilos de botão](button-styles.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Usando botões](using-buttons.md)
</dt> </dl>

 

 