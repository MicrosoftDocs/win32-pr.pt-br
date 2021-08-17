---
title: Controles de rotação
description: Com um controle de rotação, os usuários podem clicar em botões de seta para alterar incrementalmente o valor dentro de sua caixa de texto numérica associada.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b97f5acc8a3f904df3a868274356e5337f5cc9280a5eed81693d92ce9bf9a37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118217337"
---
# <a name="spin-controls"></a>Controles de rotação

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com um controle de rotação, os usuários podem clicar em botões de seta para alterar incrementalmente o valor dentro de sua caixa de [texto numérica associada.](ctrl-text-boxes.md) O termo caixa de rotação refere-se à combinação de uma caixa de texto e seu controle de rotação associado.

![captura de tela do controle de rotação e da caixa de texto ](images/ctrl-spin-controls-image1.png)

Uma caixa de rotação típica.

Os usuários geralmente preferem controles de rotação porque podem fazer alterações sem mover as mãos do mouse. Quando o controle de rotação é emparelhado com uma caixa de texto, os usuários podem digitar ou colar entrada diretamente na caixa de texto, portanto, o uso do controle de rotação é opcional.

Embora os controles de rotação sejam usados para entrada numérica, a entrada não precisa ser um número inteiro puro. A entrada pode ser números decimais e pode ter sinais negativos, delimitadores (como dois-pontos ou hifens) e modificadores de unidade.

> [!Note]  
> Diretrizes relacionadas a [caixas de texto](ctrl-text-boxes.md) e [layout](vis-layout.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **O controle é usado para entrada numérica?** Caso não, use outro controle, como uma lista de lista ou controle deslizante, para selecionar um conjunto fixo de valores. [](/windows/desktop/uxguide/ctrl-drop) [](ctrl-sliders.md) Use barras de rolagem para rolagem.
-   **Os usuários pensam no valor como uma quantidade relativa, não como um valor numérico?** Em caso afirmado, use um controle deslizante. Use caixas de rotação somente para valores numéricos exatos e conhecidos. Por exemplo, os usuários pensam em definir o volume de áudio como baixo ou médio, e não em definir o valor como 2 ou 5.
-   **O controle está emparelhado com uma caixa de texto?** Caso não, não use. Controles de rotação não devem ser usados sozinhos ou com outros tipos de controles além de uma caixa de texto.

    **Incorreto:**

    ![captura de tela do controle de rotação, gráfico, sem caixa de texto ](images/ctrl-spin-controls-image2.png)

    Neste exemplo, um controle de rotação é usado para controlar um gráfico dinâmico.

-   **Os intervalos de valores contíguos são válidos?** Caso contrário, use uma lista lista de valores válidos.

    ![captura de tela da lista lista listada ](images/ctrl-spin-controls-image3.png)

    Neste exemplo, nem todos os números de unidade de disco são válidos, portanto, uma listada é uma opção melhor.

-   **O uso do controle de rotação é prático?** Usar um controle de rotação é prático para:

    -   Inserindo um número pequeno, normalmente abaixo de 100.
    -   Fazendo pequenas alterações em um valor existente ou padrão.

    Embora os controles de rotação possam ser usados para qualquer entrada numérica, eles são ineficientes em situações diferentes dessas.

-   **O controle de rotação é útil?** O controle é usado em um contexto em que os usuários provavelmente usarão o mouse? Caso não, considere um controle de rotação opcional.
-   **Os controles irmãos são listas listadas?** Se houver outras listas listadas, considere o uso de uma lista de listas para consistência.

    ![captura de tela da caixa de diálogo com listas listadas ](images/ctrl-spin-controls-image4.png)

    Neste exemplo, uma caixa de rotação pode ser usada, mas uma lista de listas é usada para consistência.

-   **Os usuários de toque ou caneta são um destino primário?** Se sim, considere usar uma lista lista listada. Os botões de seta em um controle de rotação são muito pequenos para serem usados com eficiência com toque ou uma caneta.

Se um controle deslizante ou uma caixa de rotação for possível, use uma caixa de rotação se:

-   O espaço na tela for restrito.
-   É provável que um usuário prefira usar o teclado.

Use um controle deslizante se:

-   Os usuários forem se beneficiar com um feedback instantâneo.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Use controles de rotação sempre que eles são práticos e úteis.** Veja [Este é o controle certo?](#is-this-the-right-control)

    -   **Exceção:** Para ser consistente com outras caixas de texto na mesma interface do usuário, use controles de rotação mesmo que nem sempre sejam práticos.

    **Correto:**

    ![captura de tela de controles de rotação de mês, dia, ano ](images/ctrl-spin-controls-image5.png)

    Neste exemplo, um controle de rotação é usado com o controle de ano para consistência, embora nem sempre seja prático.

    **Incorreto:**

    ![captura de tela do controle de rotação de endereço IP ](images/ctrl-spin-controls-image6.png)

    Neste exemplo, o controle de rotação é inutilizável.

-   **Sempre faça um controle de rotação o "parceiro" da caixa de texto.** Isso coloca o controle de rotação dentro da caixa de texto.

    **Correto:**

    ![captura de tela do controle de rotação colocado dentro da caixa de texto ](images/ctrl-spin-controls-image7.png)

    **Incorreto:**

    ![captura de tela do controle de rotação colocado fora da caixa de texto ](images/ctrl-spin-controls-image8.png)

    No exemplo correto, o controle de rotação é colocado dentro de sua caixa de texto associada.

-   **Desabilite um controle de rotação quando a caixa de texto associada estiver desabilitada.** O controle de rotação é um método de entrada complementar – nunca o único método de entrada.

### <a name="values"></a>Valores

-   **Defina o botão superior para aumentar o valor em uma unidade e o botão inferior para diminuir em uma unidade.** Normalmente, a unidade é uma, mas deve ser a menor alteração comum no valor. Idealmente, o controle de rotação deve abranger todos os valores válidos e deve ser mais conveniente do que digitar o texto.

    ![captura de tela do controle de rotação 'margens' ](images/ctrl-spin-controls-image9.png)

    Neste exemplo, clicar em um controle de rotação altera os valores em .1, que é a menor alteração comum no valor. Usar uma unidade menor cobriria o intervalo de valores válidos, mas tornava os controles de rotação inutilizáveis.

-   **Use o controle de rotação para limitar a entrada a valores válidos.** O uso de um controle de rotação nunca deve resultar em um valor incorreto.
-   **No final de um intervalo de valores válidos, reinicie o intervalo.** A metáfora do controle de rotação é que o usuário está girando uma roda de valores, portanto, esse comportamento semelhante à roda.
    -   **Exceção:** Não reinicie o intervalo se o valor resultante estiver incorreto.

        ![captura de tela do controle de rotação 'número de cópias' ](images/ctrl-spin-controls-image10.png)

        Neste exemplo, clicar no botão de seta para baixo não reinicia o intervalo (indo para o valor máximo) porque esse valor está certo de estar incorreto.

-   **Use texto em vez de valores numéricos especiais.** Permitir que os usuários girem para esses valores especiais em vez de precisar conhece-los e digitá-los.

    ![captura de tela do controle de rotação " sleep after (never)" ](images/ctrl-spin-controls-image11.png)

    Neste exemplo, Nunca é um valor especial, mas os usuários podem girar para ele.

-   **Se o valor tiver delimitadores, a caixa de texto associada deverá ter vários pontos de foco de entrada.** Isso permite que os segmentos numéricos sejam manipulados individualmente.

    ![captura de tela do controle de rotação de tempo, minutos selecionados ](images/ctrl-spin-controls-image12.png)

    Neste exemplo, o controle de rotação afeta os valores de horas, minutos, segundos e A.M./P.M.– o que tiver o foco.

-   **Se o valor tiver unidades, use o controle de rotação para alterar essas unidades também.**

    ![captura de tela do controle de rotação de tempo, 'a.m.' selecionado ](images/ctrl-spin-controls-image13.png)

    Neste exemplo, o controle de rotação pode ser usado para alterar unidades.

## <a name="labels"></a>Rótulos

-   Aplique as diretrizes de [rotulamento da caixa de texto](ctrl-text-boxes.md) para rotular a caixa de texto associada. Os controles de rotação nunca são rotulados diretamente.

## <a name="documentation"></a>Documentação

Ao fazer referência a controles de rotação:

-   Não consulte os controles de rotação na documentação do usuário. Em vez disso, consulte o rótulo da caixa de texto associada.
-   Consulte controles de rotação e caixas de rotação somente em programação e outras documentações técnicas.

Exemplo: na caixa **Data** , digite ou selecione a parte da data que você deseja alterar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Glossário](glossary.md)
</dt> </dl>

 

 