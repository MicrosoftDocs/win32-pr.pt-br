---
title: Botões de opção
description: Com um botão de opção, os usuários fazem uma escolha entre um conjunto de opções relacionadas mutuamente exclusivas.
ms.assetid: f9af0a8a-d4a1-464c-a967-bab88ae0726b
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 00495695753506702015431c889e74d5a7effe9a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172434"
---
# <a name="radio-buttons"></a>Botões de opção

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com um botão de opção, os usuários fazem uma escolha entre um conjunto de opções relacionadas mutuamente exclusivas. Os usuários podem escolher uma e apenas uma opção. Os botões de opção são tão chamados porque funcionam como as predefinições de canal em rádios.

![captura de tela de três botões de opção ](images/radio-buttons-image1.png)

Um grupo típico de botões de opção.

Um grupo de botões de opção se comporta como um único controle. Somente a opção selecionada pode ser acessada usando a tecla Tab, mas os usuários podem percorrer o grupo usando as teclas de direção.

> [!Note]  
> As diretrizes relacionadas ao [layout](vis-layout.md) e à [navegação por teclado](inter-keyboard.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **O controle é usado para escolher uma opção de um conjunto de opções mutuamente exclusivas?** Se não, use outro controle. Para escolher várias opções, use as [caixas de seleção](ctrl-check-boxes.md), uma lista de [seleção múltipla](ctrl-list-boxes.md) ou uma lista de caixas de seleção.
-   **É o número de opções entre dois e sete?** Como o espaço da tela usado é proporcional ao número de opções, mantenha o número de opções em um grupo entre dois e sete. Para oito ou mais opções, use uma [lista suspensa](/windows/desktop/uxguide/ctrl-drop) ou [lista de seleção única](ctrl-list-boxes.md).
-   **Uma caixa de seleção seria uma opção melhor?** Se houver apenas duas opções, você poderá usar uma única [caixa de seleção](ctrl-check-boxes.md) em vez disso. No entanto, as caixas de seleção são adequadas apenas para ativar ou desativar uma única opção, enquanto botões de opção podem ser usados para alternativas completamente diferentes. Se ambas as soluções forem possíveis:
    -   Use botões de opção se o significado da caixa de seleção desmarcada não for completamente óbvio.

        **Incorreto:**

        ![captura de tela da caixa de seleção paisagem ](images/radio-buttons-image2.png)

        **Correto:**

        ![captura de tela de botões de opção paisagem/retrato ](images/radio-buttons-image3.png)

        No exemplo correto, as opções não são opostas, portanto, os botões de opção são a melhor opção.

    -   Use botões de opção em páginas de assistente para tornar as alternativas desclaradas, mesmo que uma caixa de seleção seja aceitável de outra forma.
    -   Use botões de opção se você tiver espaço de tela suficiente e as opções forem importantes o suficiente para ser um bom uso desse espaço de tela. Caso contrário, use uma caixa de seleção ou lista suspensa.

        **Incorreto:**

        ![captura de tela de mostrar/não mostrar botões de opção ](images/radio-buttons-image4.png)

        Neste exemplo, as opções não são importantes o suficiente para usar botões de opção.

        **Correto:**

        ![captura de tela da caixa de seleção não mostrar esta mensagem ](images/radio-buttons-image5.png)

        Neste exemplo, uma caixa de seleção é um uso eficiente do espaço da tela para essa opção de periférico.

    -   Use uma caixa de seleção se houver outras caixas de seleção na página.

-   **Uma lista suspensa seria uma opção melhor?** Se a opção padrão for recomendada para a maioria dos usuários na maioria das situações, os botões de opção poderão chamar mais atenção às opções do que o necessário.
    -   Considere o uso de uma lista suspensa se você não quiser chamar a atenção para as opções ou se não quiser encorajar os usuários a fazer alterações. Uma lista suspensa se concentra na seleção atual, enquanto botões de opção enfatizam todas as opções igualmente.

        ![captura de tela da qualidade mais alta como botão padrão ](images/radio-buttons-image6.png)

        Neste exemplo, uma lista suspensa se concentra na seleção atual e desencoraja os usuários de fazerem alterações.

    -   Considere uma lista suspensa se houver outras listas suspensas na página.

-   **Um conjunto de botões de comando, links de comando ou um botão de divisão é uma opção melhor?** Se os botões de opção forem usados apenas para afetar como um comando é executado, geralmente é melhor apresentar as variações de comando em vez disso. Isso permite que os usuários escolham o comando correto com uma única interação.
-   **As opções apresentam opções de programa, em vez de dados?** Os valores das opções não devem ser baseados em contexto ou outros dados. Para dados, use uma lista suspensa ou lista de seleção única.
-   Se o controle for usado em uma página de assistente ou em um painel de controle, **o controlará uma resposta à instrução principal e os usuários poderão alterar a opção mais tarde?** Nesse caso, considere o uso de links de comando em vez de botões de opção para tornar a interação mais eficiente.
-   **Os valores são não numéricos?** Para dados numéricos, use [caixas de texto](ctrl-text-boxes.md), [listas suspensas](/windows/desktop/uxguide/ctrl-drop)ou [controles deslizantes](ctrl-sliders.md).

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Liste as opções em uma ordem lógica,** como a maior probabilidade de ser selecionada para a operação menos simples, mais complexa ou menos arriscada para a maioria. A ordenação alfabética não é recomendada porque ela é dependente de idioma e, portanto, não é localizável.
-   **Se nenhuma das opções for uma opção válida, adicione outra opção para refletir essa opção,** como nenhuma ou não se aplica.
-   **Prefira alinhar os botões de opção verticalmente em vez de horizontalmente.** O alinhamento horizontal é mais difícil de ler e localizar.

    **Correto:**

    ![captura de tela de alinhamento vertical do botão de opção ](images/radio-buttons-image7.png)

    Neste exemplo, os botões de opção estão alinhados verticalmente.

    **Incorreto:**

    ![captura de tela do alinhamento do botão de opção horizontal ](images/radio-buttons-image8.png)

    Neste exemplo, o alinhamento horizontal é mais difícil de ler.

-   **Reconsidere o uso de caixas de grupo para organizar grupos de botões de opção**— isso geralmente resulta em uma desordem de tela desnecessária.
-   **Não use rótulos de botão de opção como rótulos de caixa de grupo.**
-   **Não use a seleção de um botão de opção para:**
    -   Executar comandos.
    -   Exiba outras janelas, como uma caixa de diálogo para coletar mais entradas.
    -   Mostrar ou ocultar dinamicamente outros controles relacionados ao controle selecionado (leitores de tela não podem detectar esses eventos). No entanto, você pode alterar o texto dinamicamente com base na seleção.

### <a name="subordinate-controls"></a>Controles subordinados

-   Coloque controles subordinados à direita ou abaixo (recuado, libere com o rótulo do botão de opção) o botão de opção e seu rótulo. Termine o rótulo do botão de opção com dois-pontos.

    ![captura de tela de controle à direita de seu rótulo ](images/radio-buttons-image9.png)

    Neste exemplo, o botão de opção e seu controle subordinado compartilham o rótulo do botão de opção e sua chave de acesso. Nesse caso, as teclas de seta movem o foco do botão de opção para sua caixa de texto subordinada.

-   **Deixe caixas de texto editáveis e listas suspensas dependentes habilitadas se compartilharem o rótulo do botão de opção.** Quando os usuários digitam ou colam qualquer coisa na caixa, selecione a opção correspondente automaticamente. Fazer isso simplifica a interação.

    ![captura de tela da caixa de diálogo intervalo de páginas com caixa de texto ](images/radio-buttons-image10.png)

    Neste exemplo, a inserção de um número de página seleciona páginas automaticamente.

-   **Evite aninhar botões de opção com outros botões de opção ou caixas de seleção.** Se possível, mantenha todas as opções no mesmo nível.

    **Correto:**

    ![captura de tela de botões de opção alinhados à esquerda ](images/radio-buttons-image11.png)

    Neste exemplo, as opções estão no mesmo nível.

    **Incorreto:**

    ![captura de tela de botões de opção aninhados ](images/radio-buttons-image12.png)

    Neste exemplo, o uso de opções aninhadas adiciona complexidade desnecessária.

-   Se você aninhar botões de opção com outros botões de opção ou caixas de seleção, **Desabilite esses controles subordinados até que a opção de alto nível seja selecionada.** Isso evita a confusão sobre o significado dos controles subordinados.

### <a name="default-values"></a>Valores padrão

-   Como um grupo de botões de opção representa um conjunto de opções mutuamente exclusivas, **sempre tenha um botão de opção selecionado por padrão. Selecione o mais seguro (para evitar perda de dados ou acesso ao sistema) e a opção mais segura e privada.** Se não houver fatores de segurança e segurança, selecione a opção mais provável ou conveniente.
-   **Exceções:** Não terá uma seleção padrão se:
    -   **Não há nenhuma opção padrão aceitável para segurança, segurança ou motivos legais e, portanto, o usuário deve fazer uma escolha explícita.** Se o usuário não fizer uma seleção, exiba uma mensagem de erro para forçar uma.
    -   **A interface do usuário (UI) deve refletir o estado atual e a opção ainda não foi definida.** Um valor padrão significaria incorretamente que o usuário não precisa fazer uma seleção.
    -   **O objetivo é coletar dados não polarizados.** Os valores padrão diferenciariam a coleta de dados.
    -   **O grupo de botões de opção representa uma propriedade em um estado misto**, que ocorre ao exibir uma propriedade para vários objetos que não têm a mesma configuração. Não exibir uma mensagem de erro nesse caso, pois cada objeto tem um estado válido.
-   **Torne a primeira opção a opção padrão**, já que os usuários costumam esperar isso — a menos que a ordem não seja lógica. Para fazer isso, talvez seja necessário alterar os rótulos de opção.

    **Incorreto:**

    ![captura de tela do último botão de opção como opção padrão ](images/radio-buttons-image13.png)

    Neste exemplo, a opção padrão não é a primeira opção.

    **Correto:**

    ![captura de tela do primeiro botão de opção como padrão ](images/radio-buttons-image14.png)

    Neste exemplo, os rótulos de opção são redefinidos para tornar a primeira opção a opção padrão.

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![captura de tela de dimensionamento e espaçamento do botão de opção ](images/radio-buttons-image15.png)

Dimensionamento e espaçamento recomendados para botões de opção.

## <a name="labels"></a>Rótulos

### <a name="radio-button-labels"></a>Rótulos de botão de opção

-   Rotular cada botão de opção.

<!-- -->

-   Atribua uma [chave de acesso](glossary.md) exclusiva para cada rótulo. Para obter diretrizes, consulte [teclado](inter-keyboard.md).
-   Use [a capitalização no estilo de frase](glossary.md).
-   Escreva o rótulo como uma frase, não como uma frase, e não use pontuação final.
    -   **Exceção:** Se um rótulo de botão de opção também rotular um controle subordinado que o segue, termine o rótulo com dois-pontos.
-   Use frases paralelas e tente manter o comprimento sobre o mesmo para todos os rótulos.
-   Focalize o texto do rótulo nas diferenças entre as opções. Se todas as opções tiverem o mesmo texto introdutório, mova esse texto para o rótulo do grupo.
-   Use frases positivas. Por exemplo, use do em vez de não e imprima em vez de não imprimir.
-   Descreva apenas a opção com o rótulo. Mantenha os rótulos breves para que seja fácil consultá-los em mensagens e documentação. Se a opção exigir mais explicações, forneça a explicação em um controle de [texto estático](glossary.md) usando frases completas e pontuação final.

    ![captura de tela de botões de opção com texto explicativo](images/radio-buttons-image16.png)

    Neste exemplo, as opções são explicadas usando controles de texto estáticos separados.

    > [!Note]  
    > Adicionar uma explicação a um botão de opção não significa que você precisa fornecer explicações para todos os botões de opção. Forneça as informações relevantes no rótulo, se possível, e use explicações somente quando necessário. Não apenas redeclare o rótulo para fins de consistência.

     

-   **Se uma opção for altamente recomendável, adicione "(recomendado)" ao rótulo.** Certifique-se de adicionar ao rótulo de controle, não às anotações complementares.
-   **Se uma opção for destinada apenas a usuários avançados, adicione "(avançado)" ao rótulo.** Certifique-se de adicionar ao rótulo de controle, não às anotações complementares.
-   Se você precisar usar rótulos de várias linhas, alinhe a parte superior do rótulo com o botão de opção.
-   Não use um controle subordinado, os valores que ele contém ou seu rótulo de unidades para criar uma frase ou frase. Esse tipo de design não é localizável porque a estrutura da frase varia de acordo com a linguagem.

### <a name="radio-button-group-labels"></a>Rótulos do grupo de botões de opção

-   Use o rótulo de grupo para explicar a finalidade do grupo, não como fazer a seleção. Suponha que os usuários saibam como usar botões de opção. Por exemplo, não diga "Selecione uma das opções a seguir".
-   Todos os grupos de botões de opção precisam de rótulos. Grave o rótulo como uma palavra ou frase, não como uma frase, terminando com dois-pontos usando texto estático ou uma caixa de grupo.

    **Exceção:** Omita o rótulo se for meramente uma recondição de uma [instrução principal](glossary.md)da caixa de diálogo. Nesse caso, a instrução principal leva os dois-pontos (a menos que seja uma pergunta) e a chave de acesso (se houver).

    **Aceitável:**

    ![captura de tela do rótulo do grupo de botões de opção redundante ](images/radio-buttons-image17.png)

    Neste exemplo, o rótulo do grupo de botões de opção é apenas uma recondição da instrução principal.

    **Melhor:**

    ![captura de tela da instrução Main do botão de opção ](images/radio-buttons-image18.png)

    Neste exemplo, o rótulo redundante é removido, portanto, a instrução principal leva os dois-pontos.

-   Não atribua uma chave de acesso ao rótulo. Fazer isso não é necessário e torna mais difícil atribuir as outras chaves de acesso.
    -   **Exceção:** Se nem todos os controles puderem ter chaves de acesso exclusivas, você poderá atribuir uma chave de acesso ao rótulo em vez dos controles individuais. Para obter mais informações, consulte [teclado](inter-keyboard.md).

## <a name="documentation"></a>Documentação

Ao fazer referência a botões de opção:

-   Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua a tecla de acesso sublinhado ou dois-pontos.
-   Em programação e outras documentações técnicas, consulte botões de opção como botões de opção. Em qualquer outro lugar, use os botões de opção, especialmente na documentação do usuário.
-   Para descrever a interação do usuário, use clique.
-   Quando possível, formate o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

Exemplo: clique em **página atual** e em **OK**.

 

 