---
title: Controles de rotação
description: Com um controle de rotação, os usuários podem clicar nos botões de seta para alterar incrementalmente o valor dentro de sua caixa de texto numérica associada.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 54ce622983e52d65fa58ef05aca783ff67ebce66
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104297869"
---
# <a name="spin-controls"></a>Controles de rotação

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com um controle de rotação, os usuários podem clicar nos botões de seta para alterar incrementalmente o valor dentro de sua [caixa de texto numérica](ctrl-text-boxes.md)associada. O termo caixa de rotação refere-se à combinação de uma caixa de texto e seu controle de rotação associado.

![captura de tela do controle de rotação e caixa de texto ](images/ctrl-spin-controls-image1.png)

Uma caixa de rotação típica.

Os usuários geralmente preferem controles de rotação porque podem fazer alterações sem mover suas mãos do mouse. Quando o controle de rotação é emparelhado com uma caixa de texto, os usuários podem digitar ou colar a entrada diretamente na caixa de texto, portanto, o uso do controle de rotação é opcional.

Enquanto os controles de rotação são usados para entrada numérica, a entrada não precisa ser um número inteiro puro. A entrada pode ser de números decimais e pode ter sinais negativos, delimitadores (como dois-pontos ou hifens) e modificadores de unidade.

> [!Note]  
> As diretrizes relacionadas às [caixas de texto](ctrl-text-boxes.md) e ao [layout](vis-layout.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **O controle é usado para entrada numérica?** Caso contrário, use outro controle, como uma [lista suspensa](/windows/desktop/uxguide/ctrl-drop) ou [controle deslizante](ctrl-sliders.md), para selecionar um conjunto fixo de valores. Use barras de rolagem para rolar.
-   **Os usuários acham o valor como uma quantidade relativa, não um valor numérico?** Nesse caso, use um controle deslizante em vez disso. Use caixas de rotação somente para valores numéricos exatos e conhecidos. Por exemplo, os usuários pensam em definir o volume de áudio como baixo ou médio, e não em definir o valor como 2 ou 5.
-   **O controle está emparelhado com uma caixa de texto?** Caso contrário, não use. Controles de rotação não devem ser usados sozinhos ou com outros tipos de controles além de uma caixa de texto.

    **Incorreto:**

    ![captura de tela do controle de rotação, gráfico, nenhuma caixa de texto ](images/ctrl-spin-controls-image2.png)

    Neste exemplo, um controle de rotação é usado para controlar um gráfico dinâmico.

-   **Os intervalos de valores contíguos são válidos?** Caso contrário, use uma lista suspensa de valores válidos em vez disso.

    ![captura de tela da lista suspensa ](images/ctrl-spin-controls-image3.png)

    Neste exemplo, nem todos os números de unidade de disco são válidos, portanto, uma lista suspensa é uma opção melhor.

-   **O uso do controle de rotação é prático?** O uso de um controle de rotação é prático para:

    -   Inserindo um pequeno número, normalmente abaixo de 100.
    -   Fazer alterações pequenas em um valor padrão ou existente.

    Embora os controles de rotação possam ser usados para qualquer entrada numérica, eles são ineficientes em situações diferentes desses.

-   **O controle de rotação é útil?** O controle é usado em um contexto em que os usuários provavelmente estão usando o mouse? Caso contrário, considere um controle de rotação opcional.
-   **As listas suspensas de controles irmãos são:** Se houver outras listas suspensas, considere usar uma lista suspensa para fins de consistência.

    ![captura de tela da caixa de diálogo com listas suspensas ](images/ctrl-spin-controls-image4.png)

    Neste exemplo, uma caixa de rotação pode ser usada, mas uma lista suspensa é usada para fins de consistência.

-   **Os usuários de toque ou caneta são um destino principal?** Nesse caso, considere usar uma lista suspensa em vez disso. Os botões de seta em um controle de rotação são muito pequenos para serem usados com eficiência com toque ou caneta.

Se um controle deslizante ou uma caixa de rotação for possível, use uma caixa de rotação se:

-   O espaço na tela for restrito.
-   É provável que um usuário prefira usar o teclado.

Use um controle deslizante se:

-   Os usuários forem se beneficiar com um feedback instantâneo.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Use controles de rotação sempre que eles forem práticos e úteis.** Confira [esse é o controle certo?](#is-this-the-right-control)

    -   **Exceção:** Para ser consistente com outras caixas de texto na mesma interface do usuário, use controles de rotação mesmo que nem sempre sejam práticos.

    **Correto:**

    ![captura de tela dos controles de rotação mês, dia e ano ](images/ctrl-spin-controls-image5.png)

    Neste exemplo, um controle de rotação é usado com o controle Year para consistência, embora nem sempre seja prático.

    **Incorreto:**

    ![captura de tela do controle de rotação de endereço IP ](images/ctrl-spin-controls-image6.png)

    Neste exemplo, o controle de rotação é inutilizável.

-   **Sempre faça um controle de rotação do "colega" da caixa de texto.** Isso coloca o controle de rotação dentro da caixa de texto.

    **Correto:**

    ![captura de tela do controle de rotação colocado dentro da caixa de texto ](images/ctrl-spin-controls-image7.png)

    **Incorreto:**

    ![captura de tela do controle de rotação colocado fora da caixa de texto ](images/ctrl-spin-controls-image8.png)

    No exemplo correto, o controle de rotação é colocado dentro de sua caixa de texto associada.

-   **Desabilitar um controle de rotação quando sua caixa de texto associada estiver desabilitada.** O controle de rotação é um método de entrada suplementar — nunca o único método de entrada.

### <a name="values"></a>Valores

-   **Defina o botão superior para aumentar o valor em uma unidade e o botão inferior para diminuir em uma unidade.** Normalmente, a unidade é uma, mas deve ser a menor alteração comum no valor. Idealmente, o controle de rotação deve abranger todos os valores válidos e deve ser mais conveniente do que digitar o texto.

    ![captura de tela do controle de rotação ' margens ' ](images/ctrl-spin-controls-image9.png)

    Neste exemplo, clicar em um controle de rotação altera os valores por 0,1, que é a menor alteração comum no valor. O uso de uma unidade menor abordaria o intervalo de valores válidos, mas tornaria os controles de rotação inutilizáveis.

-   **Use o controle de rotação para limitar a entrada a valores válidos.** O uso de um controle de rotação nunca deve resultar em um valor incorreto.
-   **No final de um intervalo de valores válidos, reinicie o intervalo.** A metáfora do controle de rotação é que o usuário está girando uma roda de valores, portanto, esse comportamento semelhante a roda.
    -   **Exceção:** Não reinicie o intervalo se o valor resultante estiver certo de estar incorreto.

        ![captura de tela do controle de rotação ' número de cópias ' ](images/ctrl-spin-controls-image10.png)

        Neste exemplo, clicar no botão de seta para baixo não reinicia o intervalo (acessando o valor máximo) porque esse valor está certo para estar incorreto.

-   **Use texto em vez de valores numéricos especiais.** Permitir que os usuários girem para esses valores especiais em vez de precisarem conhecê-los e digitá-los.

    ![captura de tela do controle de rotação ' suspender após (nunca) ' ](images/ctrl-spin-controls-image11.png)

    Neste exemplo, nunca é um valor especial, mas os usuários podem girar para ele.

-   **Se o valor tiver delimitadores, a caixa de texto associada deverá ter vários pontos de foco de entrada.** Isso permite que os segmentos numéricos sejam manipulados individualmente.

    ![captura de tela do controle de rotação de tempo, minutos selecionados ](images/ctrl-spin-controls-image12.png)

    Neste exemplo, o controle de rotação afeta os valores de horas, minutos, segundos e A.M./P.M. – o que tiver o foco.

-   **Se o valor tiver unidades, use o controle de rotação para alterar essas unidades também.**

    ![captura de tela do controle de rotação de tempo, ' a.m. ' selecionado ](images/ctrl-spin-controls-image13.png)

    Neste exemplo, o controle de rotação pode ser usado para alterar as unidades.

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

 

 