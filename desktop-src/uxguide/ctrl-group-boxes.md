---
title: Caixas de grupo
description: Uma caixa de grupo é um quadro retangular rotulado que circunda um conjunto de controles relacionados. Uma caixa de grupo é uma maneira de mostrar as relações visualmente; Além de, possivelmente, fornecer uma chave de acesso para um grupo de controles, ele não fornece nenhuma funcionalidade.
ms.assetid: 5b5ffb36-3ed1-44cd-af87-5cddf46c56a6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 67f930383f2d4412d30027971c6cab2bd3edcccd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104564128"
---
# <a name="group-boxes"></a>Caixas de grupo

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Uma caixa de grupo é um quadro retangular rotulado que circunda um conjunto de controles relacionados. Uma caixa de grupo é uma maneira de mostrar as relações visualmente; Além de, possivelmente, fornecer uma chave de acesso para um grupo de controles, ele não fornece nenhuma funcionalidade.

![captura de tela da caixa de grupo contendo caixas de seleção ](images/ctrl-group-boxes-image1.png)

Uma caixa de grupo típica.

> [!Note]  
> As diretrizes relacionadas ao [layout](vis-layout.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Embora as caixas de grupo sejam um forte meio de indicar relações, a utilização delas adiciona resíduos visuais e reduz consideravelmente o espaço disponível em uma superfície. Elas são visualmente pesadas e devem ser usadas com moderação – apenas quando não há uma solução melhor.

Uma tendência de design no Windows é uma aparência mais simples e mais limpa, eliminando linhas desnecessárias.

Para decidir se uma caixa de grupo é necessária, considere estas perguntas:

-   **Há mais de um controle no grupo?** Caso contrário, use um rótulo de texto sem formatação em vez disso. Uma exceção rara é usar uma caixa de grupo com um único controle para manter a consistência com outras caixas de grupo na mesma superfície.

**Incorreto:** ![ captura de tela da caixa de grupo que contém uma caixa de texto ](images/ctrl-group-boxes-image2.png)

Neste exemplo, a caixa de grupo tem apenas um único controle.

-   **Os controles estão relacionados? Mostrar a relação adiciona clareza?** Caso contrário, apresente os controles separadamente fora de uma caixa de grupo.
-   **Todos os controles estão dentro do grupo?** Nesse caso, indique a relação na superfície maior, como a caixa de diálogo pai ou a página.

**Incorreto:** ![ captura de tela da caixa de grupo que contém todos os controles ](images/ctrl-group-boxes-image3.png)

Neste exemplo, todos os controles (além dos botões de confirmação) na caixa de diálogo estão dentro da caixa de grupo.

-   **Você pode efetivamente comunicar as relações usando apenas o layout?** Nesse caso, use o [layout](vis-layout.md) em vez disso. Você pode colocar controles relacionados ao lado um do outro e colocar o espaçamento adicional entre controles não relacionados. Você também pode usar títulos e recuo para mostrar relações hierárquicas.

![Figura de quatro ícones mostrando quatro grupos de tarefas ](images/ctrl-group-boxes-image4.png)

Neste exemplo, layout sozinho é usado para mostrar relações de controle.

-   **Você pode realmente comunicar as relações usando um separador?** Nesse caso, use um separador. Um separador é uma linha horizontal que unifica os controles abaixo dele. Os separadores fornecem uma aparência mais simples e limpa. No entanto, ao contrário das caixas de grupo, elas funcionam melhor quando abrangem a largura total da superfície.
    -   **Desenvolvedores:** Você pode implementar um separador com um retângulo esboçado com uma altura de um.

![Captura de tela que mostra os controles de email separados por separadores de retângulo gravados.](images/ctrl-group-boxes-image5.png)

Neste exemplo, os separadores rotulados são usados para mostrar relações de controle.

![captura de tela de controles separados por separadores ](images/ctrl-group-boxes-image6.png)

Neste exemplo, separadores sem rótulo são usados para mostrar relações de controle.

-   **Você pode realmente comunicar as relações sem texto?** Nesse caso, considere o uso de elementos gráficos, como [planos de fundo](vis-graphic.md) ou agregadores.

## <a name="guidelines"></a>Diretrizes

-   **Não aninhe caixas de grupo.** Use layout para mostrar relações dentro de uma caixa de grupo.

**Incorreto:** ![ captura de tela de uma caixa de grupo dentro de uma caixa de grupo ](images/ctrl-group-boxes-image7.png)

Neste exemplo, as caixas de grupo aninhadas resultam em uma desordem Visual desnecessária.

**Correto:** ![ captura de tela dos mesmos controles dentro de uma caixa de grupo ](images/ctrl-group-boxes-image8.png)

Neste exemplo, a mesma relação de controle é mostrada usando o layout em vez disso.

-   Não coloque controles em rótulos de caixa de grupo.
    -   **Exceção:** Você pode usar uma caixa de seleção como um rótulo de caixa de grupo se todos os controles dentro da caixa estiverem habilitados e desabilitados pela caixa de seleção.

**Incorreto:** ![ captura de tela da lista suspensa em um rótulo de caixa de grupo ](images/ctrl-group-boxes-image9.png)

Neste exemplo, uma lista suspensa é colocada incorretamente em uma caixa de grupo. Este exemplo deve usar [guias](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) em vez disso.

-   **Não desabilite caixas de grupo.** Para indicar que um grupo de controles não é aplicado no momento, desabilite todos os controles dentro da caixa de grupo, mas não a própria caixa de grupo. Essa abordagem é mais acessível e pode ser suportada consistentemente por todas as estruturas de interface do usuário.

## <a name="labels"></a>Rótulos

-   Rotular todas as caixas de grupo.
-   Não atribua uma chave de acesso ao rótulo. Fazer isso é desnecessário e torna mais difícil atribuir as outras chaves de acesso. Em vez disso, atribua chaves de acesso aos controles dentro da caixa de grupo.
    -   **Exceção:** Se uma superfície tiver muitos controles, talvez não haja chaves de acesso suficientes disponíveis. Nesse caso, reduza o número de chaves de acesso atribuindo-as a caixas de grupo em vez dos controles dentro das caixas de grupo.
-   Use [a capitalização no estilo de frase](glossary.md).
-   Escreva o rótulo usando um substantivo ou uma frase de substantivo, não como uma frase, e não use pontuação final, incluindo dois-pontos.
-   Use frases paralelas para rótulos de caixa de grupo na mesma superfície.
-   Mantenha os rótulos da caixa de grupo concisos. Não use o texto de instruções como rótulo. No entanto, você pode ter texto de instrução dentro da caixa de grupo.
-   Não repita o rótulo da caixa de grupo nos rótulos de controle dentro da caixa. Por exemplo, se a caixa de grupo for rotulada como alinhamento, Rotule os botões de opção esquerda, direita e assim por diante, não alinhamento à esquerda ou alinhamento à direita.
-   Não faça referência a caixas de grupo no texto da interface do usuário.

## <a name="documentation"></a>Documentação

Ao fazer referência a caixas de Grupo:

-   Consulte as caixas de grupo somente no programador e outras documentações técnicas. Para caixa de grupo, use duas palavras em minúsculas.
-   Em qualquer outro lugar, é desnecessário incluir o nome da caixa de grupo em um procedimento, a menos que uma caixa de diálogo contenha mais de uma opção com o mesmo nome. Nesses casos, use sob com o nome da caixa de grupo.
-   Quando possível, formate o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

Exemplo: em **efeitos**, selecione **oculto**.

 

 