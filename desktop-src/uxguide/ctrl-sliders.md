---
title: Controles deslizantes (conceitos básicos de Design)
description: Com um controle deslizante, os usuários podem escolher um intervalo contínuo de valores.
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
# <a name="sliders-design-basics"></a>Controles deslizantes (conceitos básicos de Design)

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com um controle deslizante, os usuários podem escolher um intervalo contínuo de valores. Um controle deslizante tem uma barra que mostra o intervalo e um indicador que mostra o valor atual. As marcas de escala opcionais mostram valores.

![Figura mostrando barras, controle deslizante e marcas de escala ](images/ctrl-sliders-image1.png)

Um controle deslizante típico.

> [!Note]  
> As diretrizes relacionadas ao [layout](vis-layout.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Use um controle deslizante quando desejar que os usuários possam **definir valores contíguos definidos (como volume ou brilho) ou um intervalo de valores discretos (como configurações de resolução de tela).**

Um controle deslizante é uma boa opção quando você sabe que os usuários imaginam o valor como uma quantidade relativa, e não como um valor numérico. Por exemplo, os usuários pensam em definir o volume de áudio como baixo ou médio, e não em definir o valor como 2 ou 5.

Para decidir, considere estas perguntas:

-   **A configuração parece uma quantidade relativa?** Caso contrário, use [botões de opção](ctrl-radio-buttons.md)ou uma lista [suspensa](/windows/desktop/uxguide/ctrl-drop) ou de [seleção única](ctrl-list-boxes.md).
-   **A configuração é um valor numérico exato conhecido?** Nesse caso, use uma [caixa de texto numérica](ctrl-text-boxes.md).
-   **O usuário se beneficiaria com um feedback instantâneo sobre o efeito das alterações de configuração?** Se sim, use um controle deslizante. Por exemplo, os usuários podem escolher uma cor com mais facilidade vendo imediatamente o efeito das alterações nos valores de matiz, saturação ou luminosidade.
-   **A configuração tem um intervalo de quatro ou mais valores?** Se não parecer, use os botões de opção.
-   **O usuário pode alterar o valor?** Controles deslizantes são destinados para interação do usuário. Se um usuário não puder alterar o valor, use uma [caixa de texto](ctrl-text-boxes.md) somente leitura em vez disso.

Se um controle deslizante ou uma caixa de texto numérica for possível, use uma caixa de texto numérica se:

-   O espaço na tela for restrito.
-   É provável que um usuário prefira usar o teclado.

Use um controle deslizante se:

-   Os usuários forem se beneficiar com um feedback instantâneo.

## <a name="guidelines"></a>Diretrizes

-   **Use uma orientação natural.** Por exemplo, se o controle deslizante representar um valor real que normalmente é mostrado na vertical (como temperatura), use uma orientação vertical.
-   **Oriente o controle deslizante para refletir a cultura dos usuários.** Por exemplo, as culturas ocidentais são lidas da esquerda para a direita, portanto, para controles deslizantes horizontais, coloque a extremidade inferior do intervalo à esquerda e a extremidade superior à direita. Para culturas que lêem da direita para a esquerda, faça o oposto.
-   **Dimensione o controle para que um usuário possa definir facilmente o valor desejado.** Para configurações com valores distintos, certifique-se de que o usuário pode facilmente selecionar qualquer valor utilizando o mouse.
-   **Considere usar uma escala não linear se o intervalo de valores for grande e os usuários provavelmente selecionarem valores em uma extremidade do intervalo.** Por exemplo, o valor de tempo pode ser de 1 minuto, 1 hora, 1 dia ou 1 mês.
-   **Sempre que for prático, dê comentários imediatos enquanto ou depois que um usuário fizer uma seleção.** por exemplo, o Microsoft Windows volume control emite bipes para indicar o volume de áudio resultante.
-   **Use rótulos para mostrar o intervalo de valores.**

    **Exceção:** Se o controle deslizante for verticalmente orientado e o rótulo superior for máximo, alto, mais ou equivalente, você poderá omitir os outros rótulos, pois o significado é claro.

    ![Figura de um controle deslizante vertical ](images/ctrl-sliders-image2.png)

    Neste exemplo, a orientação vertical do controle deslizante torna os rótulos de intervalo desnecessários.

-   **Use marcas de escala quando os usuários precisarem saber o valor aproximado da configuração.**
-   **Use marcas de escala e um rótulo de valor quando os usuários precisarem saber o valor exato da configuração que escolherem.** Sempre use um rótulo de valor se um usuário precisar saber as unidades para fazer sentido da configuração.

    ![figura do controle deslizante mostrando o número de pixels selecionados ](images/ctrl-sliders-image3.png)

    Neste exemplo, um rótulo é usado para indicar claramente o valor selecionado.

-   **Para controles deslizantes orientados horizontalmente, coloque as marcas de escala sob o controle deslizante.** Para controles deslizantes orientados verticalmente, coloque as marcas de escala à direita para culturas ocidentais; para culturas que lêem da direita para a esquerda, faça o oposto.
-   **Coloque o rótulo de valor completamente abaixo do controle deslizante para que a relação seja clara.**

    **Incorreto:**

    ![Figura de um rótulo que é maior que seu controle deslizante ](images/ctrl-sliders-image4.png)

    Neste exemplo, o rótulo de valor não está alinhado sob o controle deslizante.

-   **Ao desabilitar um controle deslizante, desabilite também todos os rótulos associados.**
-   **Não use um controle deslizante e uma caixa de texto numérico para a mesma configuração.** Use apenas o controle mais apropriado.

    **Exceção:** Use ambos os controles quando o usuário precisar de comentários imediatos e a capacidade de definir um valor numérico exato.

-   **Não use um controle deslizante como indicador de progresso.**
-   **Não altere o tamanho do indicador do controle deslizante do tamanho padrão.**

    **Incorreto:**

    ![figura do controle deslizante menor que o padrão ](images/ctrl-sliders-image5.png)

    Neste exemplo, um tamanho menor do que o padrão é usado.

    **Correto:**

    ![Figura mostrando o controle deslizante padrão ](images/ctrl-sliders-image6.png)

    Neste exemplo, o tamanho padrão é usado.

-   **Não rotular todas as marcas de escala.**

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![figura do espaçamento e dimensionamento do controle deslizante recomendado ](images/ctrl-sliders-image7.png)

Dimensionamento e espaçamento recomendados para controles deslizantes.

## <a name="labels"></a>Rótulos

### <a name="slider-labels"></a>Rótulos de controle deslizante

-   Use um rótulo de texto estático que termine com dois-pontos ou um rótulo de caixa de grupo sem pontuação final.
-   Atribua uma chave de acesso exclusiva para cada rótulo. Para obter diretrizes de atribuição, consulte [teclado](inter-keyboard.md).
-   Use a capitalização com estilo de frase.
-   Posicione o rótulo do controle deslizante à esquerda do controle deslizante ou acima e alinhado com a borda esquerda do controle deslizante (ou seu identificador de intervalo esquerdo, se presente).

### <a name="range-labels"></a>Rótulos de intervalo

-   Rotule as duas extremidades do intervalo do controle deslizante, a menos que uma orientação vertical torne isso desnecessário.
-   Use somente o Word, se possível, para cada rótulo.
-   Não use pontuação final.
-   Certifique-se de que esses rótulos sejam descritivos e paralelos. Exemplos: Máximo/Mínimo, Mais/Menos, Baixo/Alto (altura), Baixo/Alto (som).
-   Use a capitalização com estilo de frase.
-   Não atribua chaves de acesso.

### <a name="value-labels"></a>Rótulos de valor

-   Se você precisar de um rótulo de valor, mostre-o abaixo do controle deslizante.
-   Centralize o texto em relação ao controle e inclua as unidades (como pixels).

    ![figura do rótulo centralizado sob o controle deslizante ](images/ctrl-sliders-image8.png)

    Neste exemplo, o rótulo do valor é centralizado sob o controle deslizante e inclui as unidades.

## <a name="documentation"></a>Documentação

Ao fazer referência a controles deslizantes:

-   Use o texto exato do rótulo, incluindo sua capitalização e inclua o controle deslizante de palavra. Não inclua a tecla de acesso sublinhado ou dois-pontos.
-   Para descrever a interação do usuário, use mover.
-   Quando possível, formate o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

Exemplo: para aumentar a resolução da tela, mova o controle deslizante de **resolução da tela** para a direita.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Glossário](glossary.md)
</dt> </dl>

 

 