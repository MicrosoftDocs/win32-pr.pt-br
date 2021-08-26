---
title: Botões
description: Com um botão de opção, os usuários fazem uma escolha entre um conjunto de opções mutuamente exclusivas e relacionadas.
ms.assetid: f9af0a8a-d4a1-464c-a967-bab88ae0726b
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: cbe870e1c1900de29dda515fd2142b951886929af46e69b4fea3fc6644e6f8fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934449"
---
# <a name="radio-buttons"></a>Botões

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com um botão de opção, os usuários fazem uma escolha entre um conjunto de opções mutuamente exclusivas e relacionadas. Os usuários podem escolher uma e apenas uma opção. Os botões de rádio são chamados porque funcionam como as predefinições de canal em rádios.

![captura de tela de três botões de rádio ](images/radio-buttons-image1.png)

Um grupo típico de botões de rádio.

Um grupo de botões de rádio se comporta como um único controle. Somente a opção selecionada pode ser acessada usando a tecla Tab, mas os usuários podem passar pelo grupo usando as teclas de direção.

> [!Note]  
> As diretrizes relacionadas [ao layout](vis-layout.md) e à navegação [por teclado](inter-keyboard.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **O controle é usado para escolher uma opção de um conjunto de opções mutuamente exclusivas?** Se não, use outro controle. Para escolher várias opções, use caixas [de seleção](ctrl-check-boxes.md), uma lista de [seleção múltipla](ctrl-list-boxes.md) ou uma lista de caixas de seleção.
-   **O número de opções entre dois e sete?** Como o espaço de tela usado é proporcional ao número de opções, mantenha o número de opções em um grupo entre duas e sete. Para oito ou mais opções, use uma [listada ou](/windows/desktop/uxguide/ctrl-drop) [uma lista de seleção única](ctrl-list-boxes.md).
-   **Uma caixa de seleção seria uma opção melhor?** Se houver apenas duas opções, você poderá usar uma única caixa [de seleção.](ctrl-check-boxes.md) No entanto, as caixas de seleção são adequadas apenas para ligar ou desligar uma única opção, enquanto os botões de opção podem ser usados para alternativas completamente diferentes. Se ambas as soluções são possíveis:
    -   Use botões de rádio se o significado da caixa de seleção des limpa não for completamente óbvio.

        **Incorreto:**

        ![captura de tela da caixa de seleção paisagem ](images/radio-buttons-image2.png)

        **Correto:**

        ![captura de tela dos botões de rádio paisagem/retrato ](images/radio-buttons-image3.png)

        No exemplo correto, as opções não são opostas, portanto, os botões de opção são a melhor opção.

    -   Use botões de opção em páginas do assistente para limpar as alternativas, mesmo que uma caixa de seleção seja aceitável.
    -   Use botões de opção se você tiver espaço suficiente na tela e as opções são importantes o suficiente para ser um bom uso desse espaço na tela. Caso contrário, use uma caixa de seleção ou uma lista de listas.

        **Incorreto:**

        ![captura de tela de mostrar/não mostrar botões de rádio ](images/radio-buttons-image4.png)

        Neste exemplo, as opções não são importantes o suficiente para usar botões de opção.

        **Correto:**

        ![captura de tela de não mostrar esta caixa de seleção de mensagem ](images/radio-buttons-image5.png)

        Neste exemplo, uma caixa de seleção é um uso eficiente do espaço de tela para essa opção de periférico.

    -   Use uma caixa de seleção se houver outras caixas de seleção na página.

-   **Uma lista lista listada seria uma opção melhor?** Se a opção padrão for recomendada para a maioria dos usuários na maioria das situações, os botões de opção poderão chamar mais atenção para as opções do que o necessário.
    -   Considere usar uma listada se você não quiser chamar a atenção para as opções ou não quiser incentivar os usuários a fazer alterações. Uma lista lista listada se concentra na seleção atual, enquanto os botões de opção enfatizam todas as opções igualmente.

        ![captura de tela da mais alta qualidade como botão padrão ](images/radio-buttons-image6.png)

        Neste exemplo, uma listada se concentra na seleção atual e desestimula os usuários a fazer alterações.

    -   Considere uma lista lista listada se houver outras listas listadas na página.

-   **Um conjunto de botões de comando, links de comando ou um botão de divisão seria uma opção melhor?** Se os botões de rádio são usados apenas para afetar a maneira como um comando é executado, geralmente é melhor apresentar as variações de comando. Isso permite que os usuários escolham o comando certo com uma única interação.
-   **As opções apresentam opções de programa, em vez de dados?** Os valores das opções não devem ser baseados no contexto ou em outros dados. Para dados, use uma lista lista de listas ou uma lista de seleção única.
-   Se o controle for usado em uma página do assistente ou painel de controle, o controle será uma resposta à instrução principal e os usuários poderão **alterar a escolha posteriormente?** Se sim, considere usar links de comando em vez de botões de rádio para tornar a interação mais eficiente.
-   **Os valores são não numéricos?** Para dados numéricos, use [caixas de texto](ctrl-text-boxes.md), listas [listadas ou](/windows/desktop/uxguide/ctrl-drop) [controles deslizantes](ctrl-sliders.md).

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Liste as opções em uma ordem lógica,** como a mais provável de ser selecionada para a operação menos simples para a mais complexa ou menos arriscada para a maioria. A ordenação alfabética não é recomendada porque é dependente de idioma e, portanto, não é localizável.
-   **Se nenhuma das opções for uma opção válida, adicione** outra opção para refletir essa opção, como Nenhuma ou Não se aplica.
-   **Prefira alinhar os botões de rádio verticalmente em vez de horizontalmente.** O alinhamento horizontal é mais difícil de ser lido e localizado.

    **Correto:**

    ![captura de tela do alinhamento vertical do botão de rádio ](images/radio-buttons-image7.png)

    Neste exemplo, os botões de rádio são alinhados verticalmente.

    **Incorreto:**

    ![captura de tela do alinhamento horizontal do botão de rádio ](images/radio-buttons-image8.png)

    Neste exemplo, o alinhamento horizontal é mais difícil de ler.

-   **Reavaliar o uso de caixas de grupo para organizar grupos** de botões de rádio – isso geralmente resulta em confusão desnecessária na tela.
-   **Não use rótulos de botão de rádio como rótulos de caixa de grupo.**
-   **Não use a seleção de um botão de rádio para:**
    -   Executar comandos.
    -   Exibir outras janelas, como uma caixa de diálogo para coletar mais entradas.
    -   Mostrar ou ocultar dinamicamente outros controles relacionados ao controle selecionado (os leitores de tela não podem detectar esses eventos). No entanto, você pode alterar o texto dinamicamente com base na seleção.

### <a name="subordinate-controls"></a>Controles subordinados

-   Coloque os controles subordinados à direita ou abaixo (recuado, liberando com o rótulo do botão de rádio) o botão de rádio e seu rótulo. Termine o rótulo do botão de rádio com dois-pontos.

    ![captura de tela do controle à direita de seu rótulo ](images/radio-buttons-image9.png)

    Neste exemplo, o botão de rádio e seu controle subordinado compartilham o rótulo do botão de rádio e sua chave de acesso. Nesse caso, as teclas de direção movem o foco do botão de rádio para sua caixa de texto subordinada.

-   **Deixe as caixas de texto editáveis dependentes e as listas listadas habilitadas se elas compartilharem o rótulo do botão de rádio.** Quando os usuários digitarem ou colarem qualquer coisa na caixa, selecione a opção correspondente automaticamente. Isso simplifica a interação.

    ![captura de tela da caixa de diálogo intervalo de páginas com caixa de texto ](images/radio-buttons-image10.png)

    Neste exemplo, inserir um número de página seleciona automaticamente Páginas.

-   **Evite aninhar botões de rádio com outros botões de rádio ou caixas de seleção.** Se possível, mantenha todas as opções no mesmo nível.

    **Correto:**

    ![captura de tela de botões de rádio alinhados à esquerda ](images/radio-buttons-image11.png)

    Neste exemplo, as opções estão no mesmo nível.

    **Incorreto:**

    ![captura de tela de botões de rádio aninhados ](images/radio-buttons-image12.png)

    Neste exemplo, o uso de opções aninhadas adiciona complexidade desnecessária.

-   Se você aninhar botões de opção com outros botões de opção ou caixas de seleção, desabilite esses controles subordinados até que a **opção de alto nível seja selecionada.** Isso evita confusão sobre o significado dos controles subordinados.

### <a name="default-values"></a>Valores padrão

-   Como um grupo de botões de opção representa um conjunto de opções mutuamente exclusivas, sempre **tenha um botão de opção selecionado por padrão. Selecione a opção mais segura (para evitar a perda de dados** ou acesso ao sistema) e a opção mais segura e privada. Se segurança e segurança não são fatores, selecione a opção mais provável ou conveniente.
-   **Exceções:** Não terá uma seleção padrão se:
    -   **Não há nenhuma opção padrão aceitável para motivos legais, de segurança ou de segurança e, portanto, o usuário deve fazer uma escolha explícita.** Se o usuário não fizer uma seleção, exibirá uma mensagem de erro para forçar uma.
    -   **A interface do usuário deve refletir o estado atual e a opção ainda não foi definida.** Um valor padrão implicaria incorretamente que o usuário não precisa fazer uma seleção.
    -   **A meta é coletar dados sem imparcialidade.** Os valores padrão seriam desvios na coleta de dados.
    -   **O grupo de botões de opção** representa uma propriedade em um estado misto , que ocorre ao exibir uma propriedade para vários objetos que não têm a mesma configuração. Não exibir uma mensagem de erro nesse caso, pois cada objeto tem um estado válido.
-   **Faça da primeira opção a opção padrão**, já que os usuários geralmente esperam isso , a menos que esse pedido não seja lógico. Para fazer isso, talvez seja necessário alterar os rótulos de opção.

    **Incorreto:**

    ![captura de tela do último botão de opção como opção padrão ](images/radio-buttons-image13.png)

    Neste exemplo, a opção padrão não é a primeira opção.

    **Correto:**

    ![captura de tela do primeiro botão de opção como padrão ](images/radio-buttons-image14.png)

    Neste exemplo, os rótulos de opção são reformulados para tornar a primeira opção a opção padrão.

## <a name="recommended-sizing-and-spacing"></a>Espaçamento e o espaçamento recomendados

![captura de tela do espaçamento e do espaçamento do botão de rádio ](images/radio-buttons-image15.png)

O espaçamento e o espaçamento recomendados para botões de rádio.

## <a name="labels"></a>Rótulos

### <a name="radio-button-labels"></a>Rótulos de botão de rádio

-   Rotule cada botão de rádio.

<!-- -->

-   Atribua uma chave [de acesso exclusiva](glossary.md) a cada rótulo. Para diretrizes, consulte [Teclado](inter-keyboard.md).
-   Use [a capitalização de estilo de frase](glossary.md).
-   Escreva o rótulo como uma frase, não como uma frase e não use nenhuma pontuação final.
    -   **Exceção:** Se um rótulo de botão de rádio também rotular um controle subordinado que o segue, termine o rótulo com dois-pontos.
-   Use frase paralela e tente manter o comprimento aproximadamente o mesmo para todos os rótulos.
-   Concentre o texto do rótulo nas diferenças entre as opções. Se todas as opções têm o mesmo texto introdutório, mova esse texto para o rótulo do grupo.
-   Use frases positivas. Por exemplo, use do em vez de não e imprima em vez de não imprimir.
-   Descreva apenas a opção com o rótulo. Mantenha os rótulos breves para que seja fácil fazer referência a eles em mensagens e documentação. Se a opção exigir mais explicação, forneça a explicação em um controle de [texto](glossary.md) estático usando frases completas e pontuação final.

    ![captura de tela de botões de rádio com texto explicativo](images/radio-buttons-image16.png)

    Neste exemplo, as opções são explicadas usando controles de texto estático separados.

    > [!Note]  
    > Adicionar uma explicação a um botão de opção não significa que você precisa fornecer explicações para todos os botões de opção. Forneça as informações relevantes no rótulo, se possível, e use explicações somente quando necessário. Não apenas restate o rótulo para consistência.

     

-   **Se uma opção for altamente recomendada, adicione "(recomendado)" ao rótulo.** Certifique-se de adicionar ao rótulo de controle, não às notas complementares.
-   **Se uma opção for destinada somente a usuários avançados, adicione "(advanced)" ao rótulo.** Certifique-se de adicionar ao rótulo de controle, não às notas complementares.
-   Se você precisa usar rótulos de várias linhas, alinhe a parte superior do rótulo com o botão de rádio.
-   Não use um controle subordinado, os valores que ele contém ou seu rótulo de unidades para criar uma frase ou frase. Esse design não é localizável porque a estrutura de frase varia de acordo com o idioma.

### <a name="radio-button-group-labels"></a>Rótulos do grupo de botões de rádio

-   Use o rótulo do grupo para explicar a finalidade do grupo, não como fazer a seleção. Suponha que os usuários saibam como usar botões de rádio. Por exemplo, não diga "Selecione uma das opções a seguir".
-   Todos os grupos de botões de rádio precisam de rótulos. Escreva o rótulo como uma palavra ou frase, não como uma frase, terminando com dois-pontos usando texto estático ou uma caixa de grupo.

    **Exceção:** Omita o rótulo se ele for apenas uma reformulação da instrução principal de uma [caixa de diálogo.](glossary.md) Nesse caso, a instrução principal recebe os dois-pontos (a menos que seja uma pergunta) e a chave de acesso (se houver um).

    **Aceitável:**

    ![captura de tela do rótulo do grupo de botões de rádio redundante ](images/radio-buttons-image17.png)

    Neste exemplo, o rótulo do grupo de botões de rádio é apenas uma reformulação da instrução principal.

    **Melhor:**

    ![captura de tela somente da instrução principal do botão de rádio ](images/radio-buttons-image18.png)

    Neste exemplo, o rótulo redundante é removido, portanto, a instrução principal leva os dois-pontos.

-   Não atribua uma chave de acesso ao rótulo. Isso não é necessário e torna as outras chaves de acesso mais difíceis de atribuir.
    -   **Exceção:** Se nem todos os controles puderem ter chaves de acesso exclusivas, você poderá atribuir uma chave de acesso ao rótulo em vez dos controles individuais. Para obter mais informações, consulte [Teclado](inter-keyboard.md).

## <a name="documentation"></a>Documentação

Ao fazer referência a botões de rádio:

-   Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua o sublinhado ou dois-pontos da chave de acesso.
-   Na programação e em outras documentações técnicas, consulte botões de opção como botões de opção. Em qualquer outro lugar, use botões de opção, especialmente na documentação do usuário.
-   Para descrever a interação do usuário, use clique.
-   Quando possível, forja o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

Exemplo: clique **em Página atual** e clique em **OK.**

 

 