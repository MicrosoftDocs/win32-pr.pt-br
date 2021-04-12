---
title: Implementando uma interface do usuário
description: Esta seção descreve algumas das tarefas associadas à implementação de uma interface do usuário para um aplicativo do Windows.
ms.assetid: 889791a7-d12c-4ec6-9b04-8fed14ecdb2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941458e046a85dc6e27a684d8aa3a7ea609e889
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294259"
---
# <a name="implementing-a-user-interface"></a>Implementando uma interface do usuário

Esta seção descreve algumas das tarefas associadas à implementação de uma interface do usuário para um aplicativo do Windows.

-   [Protótipo](#prototype)
-   [Constructo](#construct)
-   [Simplifique](#simplify)
    -   [Reduzir, reutilizar, desobstruir](#reduce-reuse-declutter)
    -   [A melhor interface do usuário não é uma interface do usuário](#the-best-ui-is-no-ui)
    -   [A interface do usuário Less é uma interface de usuário melhor](#less-ui-is-better-ui)
    -   [Interface do usuário consistente é boa interface do usuário](#consistent-ui-is-good-ui)

## <a name="prototype"></a>Protótipo

As interfaces do usuário devem ser criadas na lista de cenários e requisitos do usuário que foram identificados na etapa de análise do usuário.

Os protótipos podem ser tão simples quanto esboços de lápis ou tão complexos quanto a telas de tela interativa. Mantenha todo o trabalho anterior, pois ele pode ser útil ao mostrar os participantes das alternativas que foram consideradas e explicar por que eles foram descartados.

Tente limitar essa etapa a dois ou três protótipos no máximo. Os protótipos não precisam ser exaustivos; Eles simplesmente precisam simular efetivamente a experiência de usar o aplicativo real.

Demonstre os protótipos e acompanhe os comentários dos usuários para ajudar a identificar as tendências gerais de usabilidade. Se for possível, descarte os protótipos menos bem-sucedidos e incorpore o máximo possível de comentários úteis em um ou mais dos protótipos restantes. Repita esse processo como tempo e recursos permitidos.

Há várias ferramentas de protótipo disponíveis, incluindo [SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)) no Microsoft Expression Studio 3, o editor de layout na Microsoft Visual Studio e até mesmo o Microsoft Paint.

## <a name="construct"></a>Constructo

Ao implementar a interface do usuário para um aplicativo, considere o seguinte:

-   Estrutura de comando

    Determine se uma estrutura de comando tradicional deve ser implementada com base em menus e barras de ferramentas, ou uma estrutura de comando alternativa baseada na estrutura da faixa de opção do Windows. Para obter mais informações, consulte [menus](../menurc/menus.md), [barras de ferramentas](../controls/toolbar-control-reference.md)e [Windows Ribbon Framework](../windowsribbon/-uiplat-windowsribbon-entry.md).

-   Janelas e caixas de diálogo

    Com base no design da interface do usuário e no trabalho de criação de protótipos, implemente as janelas do aplicativo, incluindo a janela principal, janelas filhas, caixas de diálogo e caixas de mensagem. Siga as diretrizes de UX para determinar quais estilos e controles usar nas janelas e caixas de diálogo. Para obter mais informações, consulte [janelas](../winmsg/windows.md), [caixas de diálogo](../dlgbox/dialog-boxes.md)e controles do [Windows](../controls/window-controls.md).

-   Controles personalizados

    Crie novos controles personalizados somente se você não puder obter a funcionalidade desejada de um dos controles padrão do Windows. Novos controles personalizados são muito dispendiosos para desenvolver e exigir trabalho adicional para torná-los acessíveis. Se seu aplicativo exigir controles personalizados, certifique-se de que eles sejam expostos adequadamente para tecnologias assistenciais. Para obter mais informações, consulte [controles personalizados](../controls/user-controls-intro.md) e [API de automação do Windows](../winauto/windows-automation-api-portal.md).

-   Suporte para dispositivos de entrada de usuário padrão

    A maioria dos aplicativos do Windows precisa dar suporte à entrada do usuário por meio do teclado e do mouse. A capacidade de navegar e acessar toda a funcionalidade do aplicativo por meio do teclado sozinho é especialmente importante para os usuários que estão com deficiência visual ou que têm problemas de mobilidade. Para obter mais informações, consulte [entrada do usuário](../inputdev/user-input.md) e o [software de engenharia para o ebook de acessibilidade](https://www.microsoft.com/download/details.aspx?id=19262).

-   Estilos visuais, animações e efeitos visuais

    O Windows inclui várias tecnologias que você pode usar para adicionar interesse visual e definir a interface do usuário além da de outros aplicativos. Isso inclui a especificação dos estilos visuais de controles, a adição de animações a elementos de interface do usuário e a implementação de vários efeitos visuais na interface do usuário. Para obter mais informações, consulte [estilos visuais](../controls/themes-overview.md), [Gerenciador de animação do Windows](../uianimation/-main-portal.md)e [Gerenciador de janelas da área de trabalho](../dwm/dwm-overview.md).

## <a name="simplify"></a>Simplificar o 

Uma experiência de usuário bem-sucedida depende da abordagem, da perspectiva e das suposições do desenvolvedor durante o processo de design. Obter uma compreensão básica de como um aplicativo pode ser usado pelo público-alvo exige a capacidade de pensar de forma ampla, além das restrições do que atende às necessidades do desenvolvedor. Investir nesse tempo, esforço e pesquisa no início de um projeto pagará dividendos no final.

### <a name="reduce-reuse-declutter"></a>Reduzir, reutilizar, desobstruir

Os recursos só aprimoram um produto se forem realmente usados. Em muitos casos, a proliferação de recursos pode introduzir complexidade com a adição de mais ícones, itens de menu, barras de ferramentas e caixas de diálogo que interferem na eficiência e na produtividade, em vez de adicionar valor.

### <a name="the-best-ui-is-no-ui"></a>A melhor interface do usuário não é uma interface do usuário

A interface de usuário implica que o usuário precisa interagir com o aplicativo para fazer algo acontecer. No caso ideal, nenhuma interação é necessária. Da perspectiva do usuário, ele simplesmente funciona. Se um recurso puder ser adicionado que remove com segurança uma interação do usuário, ele tornará a experiência do usuário significativamente melhor.

### <a name="less-ui-is-better-ui"></a>A interface do usuário Less é uma interface de usuário melhor

Em muitos casos, não é possível remover completamente a interação da interface de usuário da experiência do usuário. No entanto, a menor interação do usuário exigia um aplicativo o melhor.

Identifique as atividades mais comuns e essenciais que os usuários executarão com o aplicativo e torne essas funções mais proeminentes na interface do usuário. Retenha outras funções e atividades para menor status, seja visualmente, hierarquicamente ou por meio de configurações opcionais do aplicativo e preferências do usuário.

-   Substituir em vez de adicionar

    A conservação da regra de interface do usuário declara que você adiciona algo somente quando você pode tirar algo fora. Essa regra força um desenvolvedor a pensar criticamente sobre um novo recurso considerando o impacto que o recurso tem sobre toda a experiência do usuário.

    Novos recursos não devem ser promovidos porque são novos: não confunda o marketing com usabilidade. Para ajudar os usuários a localizar novos recursos em seu produto, adicione um item ao menu **ajuda** que descreve as alterações ocorridas desde a última versão do aplicativo.

-   O usuário é um recurso limitado

    Quanto mais funcionalidades forem expostas a qualquer momento, mais difícil será para um usuário encontrar a funcionalidade de que precisam.

-   É rude interromper

    Quando um aplicativo exibe uma caixa de diálogo, ele força o usuário a parar qualquer coisa que esteja fazendo e prestar atenção a algo mais. Se for possível, remova completamente a necessidade de uma caixa de diálogo, evitando casos de erro e outras experiências de usuário com interrupções. Para obter mais informações sobre as diretrizes de mensagem, consulte [mensagens](https://msdn.microsoft.com/library/dd535525.aspx).

-   Simples pode ser poderoso

    Uma interface do usuário simples não implica uma falta de funcionalidade. Normalmente, o resultado de uma interface do usuário mais simples é uma curva de aprendizado reduzida, maior eficiência e produtividade aprimorada. Isso permite que um usuário aumente sua proficiência com o aplicativo.

### <a name="consistent-ui-is-good-ui"></a>Interface do usuário consistente é boa interface do usuário

Em geral, é recomendável buscar consistência em toda a interface do usuário do aplicativo. Fornecer uma interface de usuário consistente permite que um usuário se torne mais proficiente com um aplicativo em um tempo muito menor. Eles são capazes de aplicar seu conhecimento existente do aplicativo a diferentes situações e usar funcionalidades desconhecidas com confiança.

Em casos raros, a consistência não fornece nenhum benefício ao usuário e pode até mesmo prejudicar a experiência do usuário. Não torne a interface do usuário consistente se essa consistência prejudica a capacidade de realizar uma tarefa. A consistência em si não garante a usabilidade. É um erro imaginar que a consistência na interface resultará em um bom design.

Por exemplo, a interface do usuário do jogo de vídeo normalmente é muito específica para o tipo de jogo. A tentativa de criar uma interface de usuário genérica que funciona bem para dois jogos especializados, um que exija uma roda de direcionamento e outro que funcione melhor com um joystick e botões, provavelmente não será bem-sucedido para qualquer jogo. Na melhor das hipóteses, é provável que o primeiro seja o que não é bom para ambos.

Ter bons dados sobre como as coisas são usadas é a chave para tomar essa decisão. Fique claro sobre os prós e contras de cada compensação (velocidade versus confiabilidade, facilidade de aprendizado versus proficiência especializada, consistência global versus otimização local) e tome as melhores decisões para o recurso em relação ao produto inteiro.

O design está escolhendo como falhar: a otimização para uma coisa significa falha em outro. A chave para o bom design da interface do usuário é a possibilidade de decidir quais características do aplicativo são as mais importantes e quais podem ser recortadas.

 

 