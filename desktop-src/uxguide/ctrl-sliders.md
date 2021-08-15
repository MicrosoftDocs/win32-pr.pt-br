---
title: Controles deslizantes (noções básicas de design)
description: Com um controle deslizante, os usuários podem escolher entre um intervalo contínuo de valores.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 73c6ae0cc490c338ec552d0e23e829c791689f6f822d324feaa863ccbb441d73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349844"
---
# <a name="sliders-design-basics"></a>Controles deslizantes (noções básicas de design)

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com um controle deslizante, os usuários podem escolher entre um intervalo contínuo de valores. Um controle deslizante tem uma barra que mostra o intervalo e um indicador que mostra o valor atual. Marcas de escala opcionais mostram valores.

![figura mostrando barras, controle deslizante e marcas de escala ](images/ctrl-sliders-image1.png)

Um controle deslizante típico.

> [!Note]  
> As diretrizes relacionadas [ao layout](vis-layout.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Use um controle deslizante quando quiser que os usuários sejam capazes de definir valores **contíguos definidos (como volume** ou brilho) ou um intervalo de valores discretos (como configurações de resolução de tela).

Um controle deslizante é uma boa opção quando você sabe que os usuários imaginam o valor como uma quantidade relativa, e não como um valor numérico. Por exemplo, os usuários pensam em definir o volume de áudio como baixo ou médio, e não em definir o valor como 2 ou 5.

Para decidir, considere estas perguntas:

-   **A configuração parece uma quantidade relativa?** Caso não, use [botões de rádio](ctrl-radio-buttons.md)ou uma lista [de](/windows/desktop/uxguide/ctrl-drop) seleção única ou lista de [seleção única.](ctrl-list-boxes.md)
-   **A configuração é um valor numérico exato conhecido?** Em caso afirmado, use [caixas de texto numéricas](ctrl-text-boxes.md).
-   **O usuário se beneficiaria com um feedback instantâneo sobre o efeito das alterações de configuração?** Se sim, use um controle deslizante. Por exemplo, os usuários podem escolher uma cor com mais facilidade vendo imediatamente o efeito das alterações nos valores de matiz, saturação ou luminosidade.
-   **A configuração tem um intervalo de quatro ou mais valores?** Se não parecer, use os botões de opção.
-   **O usuário pode alterar o valor?** Controles deslizantes são destinados para interação do usuário. Se um usuário não puder alterar o valor, use uma caixa de texto somente [leitura.](ctrl-text-boxes.md)

Se um controle deslizante ou uma caixa de texto numérica for possível, use uma caixa de texto numérica se:

-   O espaço na tela for restrito.
-   É provável que um usuário prefira usar o teclado.

Use um controle deslizante se:

-   Os usuários forem se beneficiar com um feedback instantâneo.

## <a name="guidelines"></a>Diretrizes

-   **Use uma orientação natural.** Por exemplo, se o controle deslizante representar um valor real que normalmente é mostrado na vertical (como temperatura), use uma orientação vertical.
-   **Oriente o controle deslizante para refletir a cultura dos usuários.** Por exemplo, as culturas ocidental leem da esquerda para a direita, portanto, para controles deslizantes horizontais, coloque a extremidade baixa do intervalo à esquerda e a extremidade superior à direita. Para culturas que leem da direita para a esquerda, faça o oposto.
-   **Tamanho do controle para que um usuário possa definir facilmente o valor desejado.** Para configurações com valores distintos, certifique-se de que o usuário pode facilmente selecionar qualquer valor utilizando o mouse.
-   **Considere usar uma escala não linear se o intervalo de valores for grande e os usuários provavelmente selecionarão valores em uma extremidade do intervalo.** Por exemplo, o valor de hora pode ser 1 minuto, 1 hora, 1 dia ou 1 mês.
-   **Sempre que for prático, dê comentários imediatos enquanto ou depois que um usuário fizer uma seleção.** Por exemplo, o controle Windows volume da Microsoft dispara um aviso para indicar o volume de áudio resultante.
-   **Use rótulos para mostrar o intervalo de valores.**

    **Exceção:** Se o controle deslizante for orientado verticalmente e o rótulo superior for Máximo, Alto, Mais ou equivalente, você poderá omitir os outros rótulos, pois o significado é claro.

    ![figura de um controle deslizante vertical ](images/ctrl-sliders-image2.png)

    Neste exemplo, a orientação vertical do controle deslizante torna os rótulos de intervalo desnecessários.

-   **Use marcas de escala quando os usuários precisam saber o valor aproximado da configuração.**
-   **Use marcas de escala e um rótulo de valor quando os usuários precisam saber o valor exato da configuração escolhida.** Sempre use um rótulo de valor se um usuário precisar conhecer as unidades para entender a configuração.

    ![figura do controle deslizante mostrando o número de pixels selecionados ](images/ctrl-sliders-image3.png)

    Neste exemplo, um rótulo é usado para indicar claramente o valor selecionado.

-   **Para controles deslizantes orientados horizontalmente, coloque marcas de escala sob o controle deslizante.** Para controles deslizantes orientados verticalmente, coloque marcas de escala à direita para culturas ocidental; para culturas que leem da direita para a esquerda, faça o oposto.
-   **Coloque o rótulo de valor completamente sob o controle deslizante para que a relação seja clara.**

    **Incorreto:**

    ![figura de um rótulo que é maior que seu controle deslizante ](images/ctrl-sliders-image4.png)

    Neste exemplo, o rótulo de valor não está alinhado sob o controle deslizante.

-   **Ao desabilitar um controle deslizante, desabilite também os rótulos associados.**
-   **Não use um controle deslizante e uma caixa de texto numérica para a mesma configuração.** Use apenas o controle mais apropriado.

    **Exceção:** Use ambos os controles quando o usuário precisar de comentários imediatos e a capacidade de definir um valor numérico exato.

-   **Não use um controle deslizante como indicador de progresso.**
-   **Não altere o tamanho do indicador do controle deslizante do tamanho padrão.**

    **Incorreto:**

    ![figura do controle deslizante menor que o padrão ](images/ctrl-sliders-image5.png)

    Neste exemplo, um tamanho menor que o padrão é usado.

    **Correto:**

    ![figura mostrando o controle deslizante padrão ](images/ctrl-sliders-image6.png)

    Neste exemplo, o tamanho padrão é usado.

-   **Não rotule cada marca de escala.**

## <a name="recommended-sizing-and-spacing"></a>Espaçamento e o espaçamento recomendados

![figura do espaçamento e o espaçamento do controle deslizante recomendados ](images/ctrl-sliders-image7.png)

O espaçamento e o espaçamento recomendados para controles deslizantes.

## <a name="labels"></a>Rótulos

### <a name="slider-labels"></a>Rótulos de controle deslizante

-   Use um rótulo de texto estático terminando com dois-pontos ou um rótulo de caixa de grupo sem pontuação final.
-   Atribua uma chave de acesso exclusiva a cada rótulo. Para diretrizes de atribuição, consulte [Teclado](inter-keyboard.md).
-   Use a capitalização com estilo de frase.
-   Posiciona o rótulo do controle deslizante à esquerda do controle deslizante ou acima e alinhado com a borda esquerda do controle deslizante (ou seu identificador de intervalo à esquerda, se presente).

### <a name="range-labels"></a>Rótulos de intervalo

-   Rotule as duas extremidades do intervalo do controle deslizante, a menos que uma orientação vertical torne isso desnecessário.
-   Use apenas a palavra, se possível, para cada rótulo.
-   Não use pontuação final.
-   Certifique-se de que esses rótulos sejam descritivos e paralelos. Exemplos: Máximo/Mínimo, Mais/Menos, Baixo/Alto (altura), Baixo/Alto (som).
-   Use a capitalização com estilo de frase.
-   Não atribua chaves de acesso.

### <a name="value-labels"></a>Rótulos de valor

-   Se você precisar de um rótulo de valor, mostre-o abaixo do controle deslizante.
-   Centralize o texto em relação ao controle e inclua as unidades (como pixels).

    ![figura do rótulo centralizado sob o controle deslizante ](images/ctrl-sliders-image8.png)

    Neste exemplo, o rótulo de valor é centralizado sob o controle deslizante e inclui as unidades.

## <a name="documentation"></a>Documentação

Ao se referir a controles deslizantes:

-   Use o texto exato do rótulo, incluindo sua capitalização, e inclua o controle deslizante de palavras. Não inclua o sublinhado ou dois-pontos da chave de acesso.
-   Para descrever a interação do usuário, use mover.
-   Quando possível, forja o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

Exemplo: para aumentar a resolução da tela, mova o controle **deslizante Resolução** de tela para a direita.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Glossário](glossary.md)
</dt> </dl>

 

 