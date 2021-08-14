---
title: Caixas de combinação de listas suspensas
description: Com uma lista suspensa ou uma caixa de combinação, os usuários fazem uma escolha entre uma lista de valores mutuamente exclusivos.
ms.assetid: dbe88cf1-7946-4343-bc16-ce12be7ce205
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e74589da084a9f4c9f950336b3093452988052b57aba42e6a7a8f449f24a254f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966201"
---
# <a name="drop-down-lists--combo-boxes"></a>Listas suspensas & caixas de combinação

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com uma lista suspensa ou uma caixa de combinação, os usuários fazem uma escolha entre uma lista de valores mutuamente exclusivos. Os usuários podem escolher uma e apenas uma opção. Com uma lista suspensa padrão, os usuários estão limitados a escolhas na lista, mas com uma caixa de combinação, eles podem inserir uma opção que não está na lista.

![captura de tela da caixa de combinação de tempo de lembrete ](images/ctrl-drop-image1.png)

Uma caixa de combinação típica.

Os termos a seguir são importantes para entender conforme você lê este artigo:

-   Uma caixa de listagem padrão é uma caixa que contém uma lista de vários itens, com vários itens visíveis.
-   Uma lista suspensa é uma lista na qual o item selecionado está sempre visível e os outros são visíveis sob demanda clicando em um botão suspenso.
-   Uma caixa de combinação é uma combinação de uma caixa de listagem padrão ou uma lista suspensa e uma [caixa de texto](ctrl-text-boxes.md)editável, permitindo, assim, que os usuários insiram um valor que não esteja na lista.
    -   Uma lista suspensa editável é uma combinação de uma lista suspensa e uma caixa de texto editável.
    -   Uma caixa de listagem editável é uma combinação de uma caixa de listagem padrão e uma caixa de texto editável.

> [!Note]  
> As diretrizes relacionadas ao [layout](vis-layout.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **O controle é usado para escolher uma opção de uma lista de valores mutuamente exclusivos?** Se não, use outro controle. Para escolher várias opções, use uma lista de [seleção múltipla padrão](ctrl-list-boxes.md), lista de caixas de seleção, Construtor de listas ou adicionar/remover lista em vez disso.
-   **São os comandos de opções?** Nesse caso, use um [botão de menu](ctrl-command-buttons.md) ou um botão de divisão em vez disso. Use listas suspensas e caixas de combinação para objetos (substantivos) ou atributos (adjetivos), mas não com comandos (verbos).
-   **A lista apresenta dados, em vez de opções de programa?** De qualquer forma, uma lista suspensa ou caixa de combinação é uma opção adequada. Por outro lado, os [botões de opção](ctrl-radio-buttons.md) são adequados apenas para um pequeno número de opções de programa.

**Listas suspensas**

-   **Há uma opção padrão que é recomendada para a maioria dos usuários na maioria das situações?** Está vendo a opção selecionada muito mais importante do que ver as alternativas? Considere usar uma lista suspensa se você não quiser encorajar os usuários a fazer alterações ocultando as alternativas. Caso contrário, considere os botões de opção, uma lista de seleção única ou uma caixa de listagem editável, que fornece mais ênfase às opções alternativas.

    ![captura de tela da qualidade mais alta como botão padrão ](images/ctrl-drop-image2.png)

    Neste exemplo, a qualidade de cor mais alta é a melhor opção para a maioria dos usuários; portanto, uma lista suspensa é uma boa opção para minimizar as alternativas.

-   **Deseja chamar a atenção para a opção?** Nesse caso, considere os botões de opção, uma lista de seleção única ou uma caixa de listagem editável, que tende a chamar mais atenção ao usar mais espaço na tela. Como as listas suspensas são compactos, são boas opções para as opções que você deseja enfatizar.
-   **O espaço na tela é Premium?** Nesse caso, use uma lista suspensa porque o espaço da tela usado é fixo e independente do número de opções.
-   **Há outras listas suspensas na janela?** Nesse caso, considere usar uma lista suspensa para fins de consistência.

**Listas suspensas editáveis**

Além dos princípios que acabou de ser fornecido para listas suspensas, o seguinte também se aplica:

-   **As opções possíveis são restritas?** Em caso afirmativo, use uma lista suspensa normal. As caixas de combinação são para entrada irrestrita, na qual os usuários podem precisar inserir um valor que não esteja na lista no momento. Como a entrada não é restringida, se os usuários inserirem texto que não seja válido, você deverá tratar o erro com uma mensagem de erro.
-   **Você pode enumerar as opções mais prováveis com antecedência**? Caso contrário, use uma caixa de texto.
-   **A lista suspensa está sendo usada para listar a entrada do usuário anterior?** A menos que os usuários precisem examinar a lista completa de entradas anteriores, use uma caixa de texto com a opção preenchimento automático em vez disso.

    ![captura de tela da caixa de diálogo Executar com lista suspensa ](images/ctrl-drop-image3.png)

    Neste exemplo, os usuários podem precisar revisar sua entrada anterior, portanto, uma lista suspensa editável é uma boa opção.

    ![captura de tela do Outlook para linha e preenchimento automático ](images/ctrl-drop-image4.png)

    Neste exemplo, uma caixa de texto com preenchimento automático é uma boa opção.

-   **Os usuários precisarão de ajuda para selecionar valores válidos?** Em caso afirmativo, use uma caixa de texto com um [botão procurar](ctrl-command-buttons.md) .

    ![captura de tela do Outlook para o botão de linha e de procura ](images/ctrl-drop-image5.png)

    Neste exemplo, os usuários podem clicar em "para" para ajudá-los a selecionar valores válidos.

-   **É importante encorajar os usuários a revisarem as opções alternativas ou a alteração de convite?** Em caso afirmativo, considere usar uma caixa de listagem editável. Com uma lista suspensa editável, os usuários não vão estar cientes das alternativas até que a lista seja descartada.
-   **Os usuários precisam localizar um item rapidamente em uma lista grande?** (Somente Win32) Nesse caso, use uma caixa de combinação porque os usuários podem selecionar um item digitando seu nome completo. Por outro lado, a lista suspensa do Win32 seleciona itens com base apenas no último caractere digitado (portanto, digitar "Jun" em uma lista de meses corresponde a novembro, e não a junho). Nesse caso, use uma caixa de combinação mesmo que as opções possíveis sejam restritas.

**Caixas de listagem editáveis**

-   **As opções possíveis são restritas?** Nesse caso, use uma lista de seleção única ou uma lista suspensa normal em vez disso. As caixas de combinação são para entrada irrestrita, em que os usuários talvez precisem inserir um valor que não esteja na lista no momento. Como a entrada não é restringida, se os usuários digitarem texto que não é válido, você deverá tratar o erro com uma mensagem de erro.
-   **Você pode enumerar as opções mais prováveis com antecedência?** Caso contrário, use uma caixa de texto.
-   **É importante encorajar os usuários a revisarem as opções alternativas ou a alteração de convite?** Caso contrário, considere uma lista suspensa editável em vez disso.
-   **Deseja chamar a atenção para a opção?** Caso contrário, considere uma lista suspensa editável em vez disso. Como as listas suspensas são compactos, são boas opções para as opções que você deseja enfatizar.
-   **O espaço na tela é Premium?** Nesse caso, use uma lista suspensa editável porque o espaço de tela usado é fixo e independente do número de opções.

Para listas suspensas, **o número de itens na lista não é um fator na escolha do controle** porque eles são dimensionados de milhares de itens até um todo. As listas suspensas editáveis redimensionam de milhares de itens para nenhum, porque os usuários podem inserir um valor que não está na lista. Como as listas suspensas podem ser usadas para dados, o número de itens pode não ser conhecido com antecedência e talvez não seja garantido. **Inclua sempre pelo menos três itens em caixas de listagem editáveis para justificar o espaço de tela adicional.**

## <a name="usage-patterns"></a>Padrões de uso

Listas suspensas e caixas de combinação têm vários padrões de uso:



|   Uso     |    Exemplo   |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lista** suspensa uma lista suspensa padrão, com um conjunto fixo de valores predeterminados. <br/>                                 | quando fechado, somente o item selecionado fica visível. Quando os usuários clicarem no botão suspenso, todas as opções se tornarão visíveis. para alterar o valor, os usuários abrem a lista e clicam em outro valor.<br/> ![captura de tela da lista suspensa, opções ocultas ](images/ctrl-drop-image6.png)<br/> Neste exemplo, a lista está em seu estado normal.<br/> ![captura de tela da lista suspensa, opções exibidas ](images/ctrl-drop-image7.png)<br/> Neste exemplo, a lista foi descartada.<br/> |
| **Visualização lista** suspensa uma lista suspensa que visualiza os resultados da seleção para ajudar os usuários a escolherem.<br/>             | ![captura de tela das opções de cor e texto ](images/ctrl-drop-image8.png)<br/> Nesses exemplos, as listas suspensas visualizam os resultados da seleção.<br/>                                                                                                                                                                                                                                                                                                                                           |
| **Lista suspensa editável** uma caixa de combinação suspensa, que permite aos usuários inserir um valor que não esteja na lista suspensa.<br/> | ![aa511458. dropdownlists27 (en-US, msdn. 10) .png](images/ctrl-drop-image9.png)![captura de tela da caixa de combinação de tamanho de fonte editável ](images/ctrl-drop-image10.png)<br/> Exemplos de uma lista suspensa editável nos modos editar e descartar.<br/> Use esse controle quando desejar dar a flexibilidade de uma caixa de texto, mas quiser ajudar os usuários fornecendo uma lista conveniente de opções prováveis.<br/>                                                                                                   |
| **Caixas de listagem editáveis** uma caixa de combinação regular, que permite aos usuários inserir um valor que não esteja na lista sempre visível. <br/> | ![captura de tela da lista suspensa de opções de fonte ](images/ctrl-drop-image11.png)<br/> Nesses exemplos, as caixas de listagem editáveis são sempre exibidas.<br/> Esse controle é uma opção melhor do que a lista suspensa editável quando é importante encorajar os usuários a revisarem as opções alternativas ou a alteração de convite.<br/>                                                                                                                                                                      |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Não use a alteração de uma lista suspensa ou caixa de combinação para**:
    -   Executar comandos.
    -   Exiba outras janelas, como uma caixa de diálogo para coletar mais entradas.
    -   Exibir dinamicamente outros controles relacionados ao controle selecionado ([leitores de tela](inter-accessibility.md) não podem detectar esses eventos).

### <a name="presentation"></a>Apresentação

-   **Classifique itens de lista em uma ordem lógica**, como agrupar opções altamente relacionadas juntas, colocando as opções mais comuns primeiro ou usando a ordem alfabética. Classifique os nomes em ordem alfabética, números em ordem numérica e datas em ordem cronológica. Listas com 12 ou mais itens devem ser classificadas alfabeticamente para facilitar a localização dos itens.

    **Correto:** ![ captura de tela da lista suspensa lógica ](images/ctrl-drop-image12.png)

    Neste exemplo, os itens de lista são classificados por sua relação espacial.

    **Incorreto:** ![ captura de tela da lista suspensa desorganizada ](images/ctrl-drop-image13.png)

    Neste exemplo, há muitos itens de lista que precisam ser classificados em ordem alfabética.

    **Correto:** ![ captura de tela da lista suspensa em ordem alfabética ](images/ctrl-drop-image14.png)

    Neste exemplo, os itens de lista são classificados em ordem alfabética, exceto para a opção que representa todos os itens.

-   **Coloque opções que representem todas ou nenhuma no início da lista, independentemente da ordem de classificação dos itens restantes.**
-   **Coloque meta-Options entre parênteses.**

    ![Captura de tela que mostra uma lista suspensa com ' (nenhum) ' selecionado.](images/ctrl-drop-image15.png)

    Neste exemplo, "(None)" é uma meta-opção porque não é um valor válido para a escolha, em vez disso, ela descreve que a própria opção não está sendo usada.

-   **Ao desabilitar uma lista suspensa ou caixa de combinação, desabilite também todos os rótulos e botões de comando associados.**

### <a name="drop-down-lists"></a>Listas suspensas

-   Quando uma única lista suspensa é usada para alterar a exibição de um controle associado, **altere a exibição imediatamente na seleção, em vez de exigir um botão de comando separado.** Use um botão de comando separado somente se a lista levar um tempo significativo para ser renderizado. No entanto, os cabeçalhos de lista e os [botões de menu](ctrl-command-buttons.md) são os controles preferidos para essa finalidade.
-   **Não faça com que itens de lista em branco** **usem meta-Options em vez disso**. Os usuários não sabem como interpretar itens em branco, enquanto o significado das meta-opções é explícito.

    **Correto:** ![ captura de tela da lista suspensa com nenhum selecionado ](images/ctrl-drop-image16.png)

    **Incorreto:** ![ captura de tela da lista suspensa com o branco selecionado ](images/ctrl-drop-image17.png)

    No exemplo incorreto, o significado da opção em branco não é claro.

### <a name="preview-drop-down-lists"></a>Listas suspensas de visualização

-   **Use visualizações na lista de itens quando for melhor mostrar com imagens do que descrever usando apenas texto.**

    ![captura de tela da lista suspensa de fontes visualizadas ](images/ctrl-drop-image18.png)

    Neste exemplo, a visualização explica as opções muito melhores do que apenas texto.

-   **Não use ícones desnecessários e não auxiliares em visualizações**.

    **Incorreto:** ![ captura de tela da lista suspensa de rótulos com ícones ](images/ctrl-drop-image19.png)

    Neste exemplo, os ícones de visualização são desnecessários porque não comunicam nenhuma informação.

### <a name="combo-boxes"></a>Caixas de combinação

-   **Limite o tamanho do texto de entrada quando possível.** Por exemplo, se a entrada válida for um número entre 0 e 999, use uma caixa de combinação limitada a três caracteres.
-   **Se houver muitas opções possíveis, concentre o conteúdo da lista nas opções mais prováveis**. Como os usuários podem inserir valores que não estão na lista, as caixas de combinação não precisam listar todas as opções, apenas as opções prováveis ou um exemplo representativo.

    ![captura de tela da lista suspensa de tamanhos de fonte ](images/ctrl-drop-image10.png)

    Neste exemplo, muitas opções válidas não são listadas, como 15, ou fontes de meio tamanho, como 9,5.

### <a name="default-values"></a>Valores padrão

-   **Selecione a opção mais segura (para evitar perda de dados ou acesso ao sistema) e a mais segura por padrão.** Se não houver fatores de segurança e segurança, selecione a opção mais provável ou conveniente.
    -   **Exceção:** Exibir um valor padrão em branco se o controle representar uma propriedade em um [estado misto](glossary.md), o que acontece ao exibir uma propriedade para vários objetos que não têm a mesma configuração.

## <a name="prompts"></a>Solicitações

Um prompt é um rótulo ou uma instrução curta colocada dentro de uma lista suspensa editável como seu valor padrão. Ao contrário do texto estático, os prompts desaparecerão da tela quando os usuários digitarem algo na caixa de combinação ou se chegarem ao foco de entrada.

![captura de tela de uma caixa de pesquisa ](images/ctrl-drop-image20.png)

Um prompt típico.

Use um prompt quando:

-   O espaço na tela é um tanto que usar um rótulo ou instrução é indesejável, como em uma barra de ferramentas.
-   O prompt destina-se principalmente a identificar a finalidade da lista de forma compactada. Elas não devem ser informações cruciais que os usuários precisam ver ao usar a caixa de combinação.

Não use prompts apenas para direcionar os usuários a selecionar algo na lista ou clicar em botões. Por exemplo, prompts como selecionar uma opção ou inserir um nome de arquivo e, em seguida, clique em enviar são desnecessários.

Ao usar prompts:

-   Desenhe o texto do prompt em itálico e texto em branco em preto normal. O texto do prompt não deve ser confundido com texto real.
-   Mantenha o texto do prompt conciso. Você pode usar fragmentos em vez de frases completas.
-   Use [a capitalização no estilo de frase](glossary.md).
-   Não use pontuação final ou reticências.
-   O texto do prompt não deve ser editável e deve desaparecer quando os usuários clicarem na caixa de texto ou na guia.
    -   **Exceção:** O prompt será exibido se a caixa de texto tiver o foco de entrada padrão e apenas desaparecer quando o usuário começar a digitar.
-   O texto do prompt será restaurado se a caixa de texto ainda estiver vazia quando perder o foco de entrada.

**Incorreto:** ![ captura de tela de seis listas suspensas editáveis](images/ctrl-drop-image21.png)

Neste exemplo, o espaço da tela não está em um Premium; Depois que uma lista suspensa editável é preenchida, é difícil para os usuários se lembrarem do que se trata; e o texto do prompt é editável e desenhado da mesma maneira que o texto real.

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![captura de tela de especificações e lista suspensa ](images/ctrl-drop-image22.png)

Dimensionamento e espaçamento recomendados para listas suspensas e caixas de combinação.

-   **Escolha uma largura apropriada para os dados válidos mais longos.** As listas suspensas não podem ser roladas horizontalmente, para que os usuários possam ver apenas o que está visível no controle. (No entanto, observe que as caixas de combinação podem ter a funcionalidade de rolagem habilitada.)
-   **Inclua mais 30%** (até 200 por cento para texto mais curto) para qualquer texto (mas não números) que serão localizados.
-   **Escolha um comprimento de lista que elimine a rolagem vertical desnecessária.** Como as listas suspensas são exibidas sob demanda, suas listas devem mostrar até 30 itens. As caixas de listagem editáveis (aquelas que não têm um botão suspenso) devem mostrar entre 3 e 12 itens.

## <a name="labels"></a>Rótulos

**Rótulos de controle**

-   Grave o rótulo como uma palavra ou frase, não como uma frase, e termine-o com dois-pontos. **Exceções:**
    -   Listas suspensas editáveis com prompts localizados onde o espaço está em um nível Premium.
    -   Se uma lista suspensa ou caixa de combinação for subordinada a um botão de opção ou caixa de seleção e for introduzida por seu rótulo que termina com dois-pontos, não coloque um rótulo adicional no controle.
-   Atribua uma [chave de acesso](glossary.md) exclusiva para cada rótulo. Para obter diretrizes, consulte [teclado](inter-keyboard.md).
-   Use [a capitalização no estilo de frase](glossary.md).
-   Posicione o rótulo à esquerda ou acima do controle e alinhe o rótulo com a borda esquerda do controle. Se o rótulo estiver à esquerda, alinhe verticalmente o texto do rótulo com o texto de controle.

    **Correto:** ![ captura de tela do alinhamento do rótulo da lista suspensa ](images/ctrl-drop-image23.png)

    Neste exemplo, o rótulo está alinhado corretamente com o texto de controle.

    **Incorreto:** ![ captura de tela da lista suspensa alinhada incorretamente ](images/ctrl-drop-image24.png)

    Neste exemplo, o rótulo está alinhado incorretamente com o texto de controle.

-   Você pode especificar unidades (segundos, conexões e assim por diante) entre parênteses após o rótulo.
-   Não faça do conteúdo da lista suspensa ou da caixa de combinação (ou seu rótulo de unidades) parte de uma frase, pois isso não é localizável.

**Texto da opção**

-   Atribua um nome exclusivo a cada opção.
-   Use [maiúsculas e minúsculas no estilo de frase](glossary.md), a menos que um item seja um substantivo adequado.
-   Grave o rótulo como uma palavra ou frase, não como uma frase e não use pontuação final.
-   Use frases paralelas e tente manter o comprimento sobre o mesmo para todas as opções.

**Texto de instrução**

-   Se você precisar adicionar texto de instrução sobre uma lista suspensa ou caixa de combinação, adicione-a acima do rótulo. Use frases completas com pontuação final.
-   Use [a capitalização no estilo de frase](glossary.md).
-   Informações adicionais que são úteis, mas não necessárias, devem ser mantidas curtas. Coloque essas informações entre parênteses entre o rótulo e os dois-pontos ou sem parênteses abaixo do controle.

    ![captura de tela da lista suspensa com dados adicionados ](images/ctrl-drop-image25.png)

    Este exemplo mostra informações adicionais colocadas abaixo do controle.

## <a name="documentation"></a>Documentação

Ao fazer referência a listas suspensas:

-   Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua a tecla de acesso sublinhado ou dois-pontos; inclua lista ou caixa, o que for mais claro.
-   Para opções de lista, use o texto de opção exato, incluindo sua capitalização.
-   Em programação e outras documentações técnicas, consulte listas suspensas como listas suspensas. Em qualquer outro lugar, use List ou Box, o que for mais claro.
-   Para descrever a interação do usuário, use clique.
-   Quando possível, formate as opções de rótulo e lista usando texto em negrito. Caso contrário, coloque o rótulo e as opções entre aspas somente se necessário para evitar confusão.

Exemplo: na lista **tamanho da fonte** , clique em **fontes grandes**.

Ao fazer referência a caixas de combinação:

-   Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua a tecla de acesso sublinhado ou dois-pontos; inclua a caixa palavra.
-   Para obter opções de lista, use o texto de opção exato, incluindo sua capitalização.
-   Em programação e outras documentações técnicas, consulte caixas de combinação como caixas de combinação. Em qualquer outro lugar, use box.
-   Para descrever a interação do usuário, use Enter.
-   Quando possível, formate as opções de rótulo e lista usando texto em negrito. Caso contrário, coloque o rótulo e as opções entre aspas somente se necessário para evitar confusão.

Exemplo: na caixa **fonte** , insira a fonte que você deseja usar.

 

