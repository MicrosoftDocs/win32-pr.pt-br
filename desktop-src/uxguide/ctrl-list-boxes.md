---
title: Caixas de listagem
description: Com uma caixa de listagem, os usuários podem selecionar um conjunto de valores apresentados em uma lista que está sempre visível.
ms.assetid: 620e9ff9-b367-446b-9e97-9c9d6d14f4bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8d4f30394e9704ba01832c60e7b41e3453a5c7abe1715678ca84405e73724c7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218022"
---
# <a name="list-boxes"></a>Caixas de listagem

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com uma caixa de listagem, os usuários podem selecionar um conjunto de valores apresentados em uma lista que está sempre visível. Com uma caixa de listagem de seleção única, os usuários selecionam um item em uma lista de valores mutuamente exclusivos. Com uma caixa de listagem de seleção múltipla, os usuários selecionam zero ou mais itens em uma lista de valores.

![captura de tela da caixa de listagem de seleção única ](images/ctrl-list-boxes-image1.png)

Uma caixa de listagem de seleção única típica.

> [!Note]  
> Diretrizes relacionadas [a exibições de layout](vis-layout.md) e [lista](ctrl-list-views.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **A lista apresenta dados, em vez de opções de programa?** De qualquer forma, uma caixa de listagem é uma opção adequada, independentemente do número de itens. Por outro lado, [botões de opção](ctrl-radio-buttons.md) ou caixas [de](ctrl-check-boxes.md) seleção são adequados apenas para um pequeno número de opções de programa.
-   **Os usuários precisam alterar exibições, agrupar, classificar por colunas ou alterar a ordem e a largura da coluna?** Em caso afirmado, use uma [exibição de lista.](ctrl-list-views.md)
-   **O controle precisa ser uma origem de arrastar ou um destino de soltar?** Em caso afirmado, use uma exibição de lista.
-   **Os itens de lista precisam ser copiados ou copiados da área de transferência?** Em caso afirmado, use uma exibição de lista.

**Listas de seleção única**

-   **O controle é usado para escolher uma opção em uma lista de valores mutuamente exclusivos?** Se não, use outro controle. Para escolher várias opções, use uma lista padrão de seleção múltipla, uma lista de caixas de seleção, um construtor de lista ou uma lista de adicionar/remover.
-   **Há uma opção padrão recomendada para a maioria dos usuários na maioria das situações?** É muito mais importante ver a opção selecionada do que ver as alternativas? Em caso afirmativos, considere [usar](/windows/desktop/uxguide/ctrl-drop) uma lista de listas se você não quiser incentivar os usuários a fazer alterações ocultando as alternativas.

![captura de tela da mais alta qualidade como botão padrão ](images/ctrl-list-boxes-image2.png)

Neste exemplo, a qualidade de cor mais alta é a melhor opção para a maioria dos usuários, portanto, uma listada é uma boa opção para fazer downplay das alternativas.

-   **A lista exige interação constante?** Se sim, use uma lista de seleção única para simplificar a interação.

![captura de tela da lista de opções, como texto sem-texto ](images/ctrl-list-boxes-image3.png)

Neste exemplo, os usuários estão alterando constantemente o item selecionado na lista Exibir itens para definir as cores do primeiro plano e da tela de fundo. O uso de uma lista de listas, nesse caso, seria muito entediante.

-   **A configuração parece uma quantidade relativa? Os usuários se beneficiariam de comentários instantâneos** sobre o efeito da configuração de alterações? Se sim, considere usar um [controle deslizante.](ctrl-sliders.md)
-   **Há uma relação hierárquica significativa entre os itens de lista?** Em caso afirmado, use um [controle de exibição de](ctrl-tree-views.md) árvore.
-   **O espaço na tela está em um premium?** Em caso afirmativos, use uma listada porque o espaço de tela usado é fixo e independente do número de itens da lista.

**Listas de seleção múltipla padrão e listas de caixas de seleção**

-   **A seleção múltipla é essencial para a tarefa ou normalmente usada?** Em caso afirmativos, use uma lista de caixas de seleção para tornar a seleção múltipla óbvia, especialmente se os usuários de destino não são avançados. Muitos usuários não perceberão que uma lista de seleção múltipla padrão dá suporte a várias seleções. Use uma lista de seleção múltipla padrão se as caixas de seleção chamarem muita atenção para várias seleções ou resultarem em muita confusão na tela.
-   **A estabilidade da seleção múltipla é importante?** Nesse caso, use uma lista de caixas de seleção, um construtor de lista ou uma lista adicionar/remover, pois clicar em altera apenas um único item por vez. Com uma lista de seleção múltipla padrão, é muito fácil limpar todas as seleções, mesmo por acidente.
-   **O controle é usado para escolher zero ou mais itens de uma lista de valores?** Se não, use outro controle. Para escolher um item, use uma lista de seleção única.

**Listas de visualização**

-   **As opções são mais fáceis de selecionar com imagens do que apenas com texto?** Em caso afirmado, use uma lista de visualização.

**Listar construtores e adicionar/remover listas**

-   **O controle é usado para escolher zero ou mais itens de uma lista de valores?** Se não, use outro controle. Para escolher um item, use uma lista de seleção única.
-   **A ordem dos itens selecionados importa?** Em caso afirmativos, o construtor de lista e adicionar/remover padrões de lista suportam a ordem, enquanto os outros padrões de seleção múltipla não.
-   **É importante que os usuários vejam um resumo de todos os itens selecionados?** Em caso afirmativos, os padrões de lista de construtor de lista e adicionar/remover exibem apenas os itens selecionados, enquanto os outros padrões de seleção múltipla não exibem.
-   **As opções possíveis não estão restritas?** Nesse caso, use uma lista adicionar/remover para que os usuários possam escolher valores que não estão atualmente na lista.
-   **Adicionar um valor à lista requer uma caixa de diálogo especializada para escolher objetos?** Em caso afirmativos, use uma lista adicionar/remover e exibir a caixa de diálogo quando os usuários clicarem em Adicionar.
-   **O espaço na tela está em um premium?** Em caso afirmado, use uma lista adicionar/remover porque ela usa menos espaço na tela nem sempre mostrando o conjunto de opções.

Para caixas de **listagem,** o número de itens na lista não é um fator na escolha do controle porque eles são dimensionadas de milhares de itens até um para listas de seleção única (e nenhum para listas de seleção múltipla). Como as caixas de listagem podem ser usadas para dados, o número de itens pode não ser conhecido com antecedência.

**Observação:** Às vezes, um controle que se parece com uma caixa de listagem é implementado usando uma exibição de lista e vice-versa. Nesses casos, aplique as diretrizes com base no uso, não na implementação.

## <a name="usage-patterns"></a>Padrões de uso

As caixas de listagem têm vários padrões de uso:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Listas de seleção única</strong> Permitir que os usuários selecionem um item por vez. <br/></td>
<td><img src="images/ctrl-list-boxes-image4.png" alt="Screen shot of list box with one item selected " /><br/> Neste exemplo, os usuários podem selecionar apenas um item de exibição.<br/></td>
</tr>
<tr class="even">
<td><strong>Listas padrão de seleção múltipla</strong> Permitir que os usuários selecionem qualquer número de itens, incluindo nenhum.<br/></td>
<td>As listas padrão de seleção múltipla têm exatamente a mesma aparência das listas de seleção única, portanto, não há nenhuma dica visual de que uma caixa de listagem dá suporte a várias seleções. Como os usuários têm que descobrir essa capacidade, esse padrão de lista é melhor usado para tarefas em que várias seleções não são essenciais e raramente são usadas. <br/> Há dois modos de seleção múltipla diferentes: <a href="glossary.md">múltiplo e</a> <a href="glossary.md">estendido.</a> <strong>O modo</strong> de seleção estendida é, de longe, o mais comum, em que a seleção pode ser estendida arrastando ou com Shift+ clique e Ctrl+clique para selecionar grupos de valores contíguos e não adjacentes, respectivamente. No modo <strong>de seleção múltipla</strong>, clicar em qualquer item alterna seu estado de seleção, independentemente das teclas Shift e Ctrl. Devido a esse comportamento incomum, o modo de seleção múltipla foi preterido e você deve usar listas de caixas de seleção.<br/> <img src="images/ctrl-list-boxes-image5.png" alt="Screen shot of list box with several items selected " /><br/> Neste exemplo, os usuários podem selecionar qualquer número de itens usando o modo de seleção múltipla.<br/></td>
</tr>
<tr class="odd">
<td><strong>Listas de caixas de seleção</strong> Como as caixas de listagem padrão de seleção múltipla, as listas de caixas de seleção permitem que os usuários selecionem qualquer número de itens, incluindo nenhum.<br/></td>
<td>Ao contrário das listas padrão de seleção múltipla, as caixas de seleção indicam claramente que várias seleções são possíveis. Use esse padrão de lista para tarefas em que várias seleções são essenciais ou comumente usadas. <br/> <img src="images/ctrl-list-boxes-image6.png" alt="Screen shot of Toolbars check-box list " /><br/> Neste exemplo, os usuários normalmente selecionam mais de um item para que uma lista de caixas de seleção seja usada.<br/> Dada essa indicação clara de várias seleções, você pode supor que as listas de caixas de seleção são preferíveis às listas padrão de seleção múltipla. Na prática, algumas tarefas exigem várias seleções ou a usam intensamente; usar uma lista de caixas de seleção nesses casos chama muita atenção para a seleção. Consequentemente, <strong>listas padrão de seleção múltipla são muito mais comuns.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>Listas de visualização</strong> Pode ser uma ou várias seleções, mas mostram uma visualização do efeito da seleção em vez de apenas texto.<br/></td>
<td><img src="images/ctrl-list-boxes-image7.png" alt="Screen shot of Window Color options preview " /><br/> Neste exemplo, uma visualização de cada opção mostra claramente o efeito da escolha, que é mais eficaz do que usar texto sozinho.<br/></td>
</tr>
<tr class="odd">
<td><strong>Construtores de lista</strong> Permitir que os usuários criem uma lista de opções adicionando um item por vez e, opcionalmente, definindo a ordem da lista.<br/></td>
<td>Um construtor de lista consiste em duas listas de seleção única: a lista à esquerda é um conjunto fixo de opções e a lista à direita é a lista que está sendo criada. Há dois botões de comando entre as listas: <br/>
<ul>
<li>Um <strong>botão</strong> Adicionar que move a opção selecionada no momento para a lista que está sendo criada, inserida antes do item selecionado. (Clicar duas vezes em um item de opção tem o mesmo efeito.)</li>
<li>Um botão <strong>remover</strong> que remove o item selecionado da lista interna e o retorna à lista de opções. (Clicar duas vezes em um item na lista interna tem o mesmo efeito.) A lista interna pode opcionalmente ter os comandos <strong>mover para cima</strong> e <strong>mover para baixo</strong> para ordenar os itens da lista.</li>
</ul>
<img src="images/ctrl-list-boxes-image8.png" alt="Screen shot of Toolbar buttons list builder " /><br/> Neste exemplo, um construtor de listas é usado para criar uma barra de ferramentas selecionando itens de um conjunto de opções disponíveis e definindo sua ordem.<br/></td>
</tr>
<tr class="even">
<td><strong>Adicionar/remover listas</strong> Permita que os usuários criem uma lista de opções adicionando um ou mais itens por vez e, opcionalmente, definindo a ordem da lista (como construtores de lista).<br/></td>
<td>Ao contrário de um construtor de listas, clicar em <strong>Adicionar</strong> exibe uma caixa de diálogo para selecionar os itens a serem adicionados à lista. Usar uma caixa de diálogo separada permite uma flexibilidade significativa na escolha de itens, você pode usar um seletor de objetos especializado ou até mesmo uma caixa de diálogo comum. Em comparação com o construtor de listas, essa variação é mais compacta, mas requer um pouco mais de esforço para adicionar itens. <br/> <img src="images/ctrl-list-boxes-image9.png" alt="Screen shot of Menu contents list " /><br/> Neste exemplo, os usuários podem adicionar ou remover ferramentas de um menu, bem como definir a ordem.<br/> Embora os padrões de lista do construtor de lista e de adição/remoção sejam significativamente mais pesados do que as outras listas de seleção múltipla, eles oferecem duas vantagens exclusivas:<br/>
<ul>
<li>Os usuários têm controle sobre a ordem da lista, enquanto criam a lista e depois.</li>
<li>Os usuários podem examinar um resumo dos itens selecionados, o que pode ser um benefício significativo se o número de opções for grande.</li>
</ul>
Suas desvantagens são que eles exigem muito mais espaço na tela e podem ser difíceis de usar ao criar uma grande lista de itens do zero. Consequentemente, eles são mais bem usados para criar listas curtas ou modificar listas que já existem.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Diretrizes

### <a name="presentation"></a>Apresentação

-   **Classifique os itens de lista em uma ordem lógica,** como agrupar opções relacionadas, colocando os itens usados com mais frequência primeiro ou usando a ordem alfabética. Classifique os nomes em ordem alfabética, números em ordem numérica e datas em ordem cronológica. Listas com 12 ou mais itens devem ser classificadas alfabeticamente para facilitar a localização dos itens.

**Correto:** ![ captura de tela de alinhamento (esquerda, centro, direita) ](images/ctrl-list-boxes-image10.png)

Neste exemplo, os itens da caixa de listagem são classificados por sua relação espacial.

**Incorreto:** ![ captura de tela da lista desorganizada ](images/ctrl-list-boxes-image11.png)

Neste exemplo, há muitos itens de lista que devem ser classificados em ordem alfabética.

**Correto:** ![ captura de tela da lista em ordem alfabética ](images/ctrl-list-boxes-image12.png)

Neste exemplo, os itens de lista são mais fáceis de localizar porque são classificados em ordem alfabética. no entanto, o item "todos os Windows produtos" está no início da lista, independentemente de sua ordem de classificação.

-   **Coloque opções que representem todas ou nenhuma no início da lista**, independentemente da ordem de classificação dos itens restantes.
-   **Coloque meta-Options entre parênteses.**

![captura de tela da lista suspensa com nenhum selecionado ](images/ctrl-list-boxes-image13.png)

Neste exemplo, "(None)" é uma meta-opção porque não é um valor válido para a escolha, em vez disso, ele indica que a própria opção não está sendo usada.

-   **Não faça com que itens de lista em branco usem meta-Options em vez disso.** Os usuários não sabem como interpretar itens em branco, enquanto o significado das meta-opções é explícito.

**Incorreto:** ![ captura de tela da lista suspensa com o branco selecionado ](images/ctrl-list-boxes-image14.png)

Neste exemplo, o significado do item em branco não é claro.

**Correto:** ![ captura de tela da lista suspensa com nenhum selecionado ](images/ctrl-list-boxes-image13.png)

Neste exemplo, a meta-opção "(None)" é usada em seu lugar.

### <a name="interaction"></a>Interação

-   **Considere fornecer um comportamento de clique duplo.** Clicar duas vezes deve ter o mesmo efeito que selecionar um item e executar o comando padrão.
-   **Faça com que o comportamento de clique duplo seja redundante.** Sempre deve haver um botão de comando ou comando de menu de contexto que tenha o mesmo efeito.
-   **Se os usuários não puderem fazer nada com os itens selecionados, não permita a seleção.**

**Correto:** ![ captura de tela da lista de alterações do assistente concluída ](images/ctrl-list-boxes-image15.png)

Esta caixa de listagem exibe uma lista somente leitura de alterações; Não é necessário selecionar.

-   **Ao desabilitar uma caixa de listagem, desabilite também todos os rótulos e botões de comando associados.**
-   **Não use a alteração do item selecionado em uma caixa de listagem para:**
    -   Executar comandos.
    -   Exiba outras janelas, como uma caixa de diálogo para coletar mais entradas.
    -   Exibir dinamicamente outros controles relacionados ao controle selecionado (leitores de tela não podem detectar esses eventos). **Exceção:** Você pode alterar dinamicamente o texto estático usado para descrever o item selecionado.

**Aceitável:** ![ captura de tela de detalhes do item de lista selecionado ](images/ctrl-list-boxes-image16.png)

Neste exemplo, alterar o item selecionado altera a descrição.

-   **Evite a rolagem horizontal.** As listas de várias colunas dependem da rolagem horizontal, que geralmente é mais difícil de usar do que a rolagem vertical. Listas de várias colunas que exigem rolagem horizontal podem ser usadas quando você tem muitos itens classificados alfabeticamente e espaço de tela suficiente para um controle amplo.

**Aceitável:** ![ captura de tela da lista de pastas no Windows Explorer ](images/ctrl-list-boxes-image17.png)

Neste exemplo, várias colunas que exigem rolagem horizontal são usadas porque há muitos itens e muito espaço de tela disponível para um controle amplo.

### <a name="multiple-selection-lists"></a>Listas de seleção múltipla

-   **Considere a exibição do número de itens selecionados abaixo da lista,** especialmente se for provável que os usuários selecionem vários itens. Essas informações não apenas fornecem comentários úteis, mas também indica claramente que a caixa de listagem dá suporte a seleção múltipla.

![captura de tela da caixa de listagem com quatro itens selecionados ](images/ctrl-list-boxes-image5.png)

Neste exemplo, o número de itens selecionados é exibido abaixo da lista.

-   Você pode fornecer outras métricas de seleção que podem ser mais significativas, como os recursos necessários para as seleções.

![captura de tela da lista de caixas de seleção dos recursos do Windows ](images/ctrl-list-boxes-image18.png)

Neste exemplo, o espaço em disco necessário para instalar os componentes é mais significativo do que o número de itens selecionados.

-   Se houver potencialmente muitos itens de lista e a seleção ou limpeza de todos eles for provável, adicione selecionar tudo e desmarcar todos os botões de comando.
-   Para listas de seleção múltipla padrão, não use o modo de seleção múltipla porque esse modo de seleção foi preterido. Para o comportamento equivalente, use uma lista de caixas de seleção em vez disso.

### <a name="default-values"></a>Valores padrão

-   **Selecione a opção mais segura (para evitar perda de dados ou acesso ao sistema) e a mais segura por padrão.** Se não houver fatores de segurança e segurança, selecione a opção mais provável ou conveniente.

**Exceção:** Não selecione nenhum item se o controle representar uma propriedade em um [estado misto](glossary.md), o que acontece ao exibir uma propriedade para vários objetos que não têm a mesma configuração.

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![captura de tela de dimensionamento e espaçamento da caixa de listagem ](images/ctrl-list-boxes-image19.png)

Dimensionamento e espaçamento recomendados para caixas de listagem.

-   **Escolha a largura da caixa de listagem apropriada para os dados válidos mais longos.** As caixas de listagem padrão não podem ser roladas horizontalmente, para que os usuários possam ver apenas o que está visível no controle.
-   **Inclua mais 30%** (até 200 por cento para texto mais curto) para qualquer texto (mas não números) que serão localizados.
-   **Escolha a altura da caixa de listagem que exibe um número integral de itens.** Evite truncar itens verticalmente.
-   **Escolha a altura da caixa de listagem que elimina a rolagem vertical desnecessária.** As caixas de listagem devem ser exibidas entre 3 e 20 itens sem a necessidade de rolagem. Considere tornar uma caixa de listagem um pouco mais demorada se isso eliminar a barra de rolagem vertical. Listas com potencialmente muitos itens devem exibir pelo menos cinco itens para facilitar a rolagem mostrando mais itens de cada vez e facilitando a posição da barra de rolagem.
-   **Se os usuários se beneficiarem de tornar a caixa de listagem maior, torne a caixa de listagem e sua janela pai redimensionável.** Isso permite que os usuários ajustem o tamanho da caixa de listagem conforme necessário. No entanto, as caixas de listagem redimensionáveis não devem exibir menos de três itens.

## <a name="labels"></a>Rótulos

**Rótulos de controle**

-   Todas as caixas de listagem precisam de rótulos. Escreva o rótulo como uma palavra ou frase, não como uma frase; Use dois pontos no final do rótulo.

**Exceção:** Omita o rótulo se for meramente uma recondição de uma [instrução principal](glossary.md)da caixa de diálogo. Nesse caso, a instrução principal leva os dois-pontos (a menos que seja uma pergunta) e a chave de acesso.

**Aceitável:** ![ captura de tela de lista com rótulo redundante ](images/ctrl-list-boxes-image20.png)

Neste exemplo, o rótulo da caixa de listagem apenas renomeia a instrução principal.

**Melhor:** ![ captura de tela de lista sem rótulo redundante ](images/ctrl-list-boxes-image21.png)

Neste exemplo, o rótulo redundante é removido e, portanto, a instrução Main usa a tecla de acesso e os dois-pontos.

-   Se uma caixa de listagem for subordinada a um botão de opção ou caixa de seleção e for introduzida pelo rótulo desse controle terminando com dois-pontos, não coloque um rótulo adicional no controle caixa de listagem.

![captura de tela de botão e lista usando o mesmo rótulo ](images/ctrl-list-boxes-image22.png)

Neste exemplo, a caixa de listagem é subordinada a um botão de opção e compartilha seu rótulo.

-   Atribua uma [chave de acesso](glossary.md)exclusiva. Para obter diretrizes, consulte [teclado](inter-keyboard.md).
-   Use [a capitalização no estilo de frase](glossary.md).
-   Posicione o rótulo à esquerda ou acima do controle e alinhe o rótulo com a borda esquerda do controle.
    -   Se o rótulo estiver à esquerda, alinhe verticalmente o texto do rótulo com a primeira linha de texto no controle.

**Correto:** ![ captura de tela de lista com rótulo alinhado à esquerda acima ](images/ctrl-list-boxes-image23.png)![ da captura de tela da lista com rótulo alinhado por texto à esquerda ](images/ctrl-list-boxes-image24.png)

Nesses exemplos, o rótulo na parte superior alinha com a borda esquerda da caixa de listagem e o rótulo à esquerda é alinhado com o texto na caixa de listagem.

**Incorreto:** ![ captura de tela de lista com rótulo alinhado por texto acima ](images/ctrl-list-boxes-image25.png)![ da captura de tela da lista com o rótulo alinhado em cima à esquerda ](images/ctrl-list-boxes-image26.png)

Nesses exemplos incorretos, o rótulo na parte superior alinha com o texto na caixa de listagem e o rótulo à esquerda é alinhado com a parte superior da caixa de listagem.

-   Para caixas de listagem de seleção múltipla, use um rótulo que indica claramente que várias seleções são possíveis. Os rótulos da lista de caixas de seleção podem ser menos explícitos.

**Correto:** ![ captura de tela de lista com selecionar um ou mais rótulos ](images/ctrl-list-boxes-image27.png)

Neste exemplo, o rótulo indica claramente que é possível selecionar várias seleções.

**Incorreto:** ![ captura de tela da caixa de listagem com rótulo de Complementos ](images/ctrl-list-boxes-image28.png)

Neste exemplo, o rótulo não fornece nenhuma informação óbvia sobre a seleção múltipla.

**Melhor:** ![ captura de tela da lista de caixas de seleção com rótulo de Complementos ](images/ctrl-list-boxes-image29.png)

Neste exemplo, as caixas de seleção indicam claramente que a seleção múltipla é possível, portanto, o rótulo não precisa ser explícito.

-   Você pode especificar unidades (segundos, conexões e assim por diante) entre parênteses após o rótulo.

**Texto da opção**

-   Atribua um nome exclusivo a cada opção.
-   Use [maiúsculas e minúsculas no estilo de frase](glossary.md), a menos que um item seja um substantivo adequado.
-   Grave o rótulo como uma palavra ou frase, não como uma frase e não use pontuação final.
-   Use frases paralelas e tente manter o comprimento sobre o mesmo para todas as opções.

**Instruções e texto suplementar**

-   Se você precisar adicionar texto de instruções sobre uma caixa de listagem, adicione-a acima do rótulo. Use frases completas com pontuação final.
-   Use [a capitalização no estilo de frase](glossary.md).
-   Informações adicionais que são úteis, mas não necessárias, devem ser mantidas curtas. Coloque esse texto entre parênteses entre o rótulo e os dois-pontos ou sem parênteses abaixo do controle.

![captura de tela da lista de caixas de seleção e texto descritivo ](images/ctrl-list-boxes-image30.png)

Neste exemplo, o texto suplementar é colocado abaixo da lista.

## <a name="documentation"></a>Documentação

Ao fazer referência a caixas de listagem:

-   Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua a tecla de acesso sublinhado ou dois-pontos. Inclua a lista de palavras. Não faça referência a uma caixa de listagem como uma caixa de listagem ou um campo.
-   Para itens de lista, use o texto exato do item, incluindo sua capitalização.
-   Em programação e outras documentações técnicas, consulte as caixas de listagem como caixas de listagem. Em qualquer outra parte, use List.
-   Para descrever a interação do usuário, use SELECT.
-   Quando possível, formate o rótulo e os itens de lista usando texto em negrito. Caso contrário, coloque o rótulo e os itens entre aspas somente se necessário para evitar confusão.

Exemplo: na lista **ir para** , selecione **indicador**.

